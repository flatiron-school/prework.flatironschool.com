desc "Setup GitHub Pages Branch"
task :setup do
  all_branches = IO.popen("git branch -a").readlines
  if all_branches.any? {|line| line.match(/gh-pages/)}
    local_branches = IO.popen("git branch -v").readlines
    if !local_branches.any? {|line| line.match(/gh-pages/)}
      `git checkout gh-pages --quiet && git checkout master --quiet`
    end
    puts "Already setup!"
  else
    `git checkout -b gh-pages --quiet && git checkout master --quiet`
    puts "Done."
  end
end

desc "Generate site and deploy to GitHub Pages"
task :deploy do
  `git remote update > /dev/null 2>&1`
  diff = `git rev-list HEAD...origin/master --count`.to_i
  uncommitted = `git status --porcelain 2>/dev/null| grep "^M" | wc -l`.to_i
  unstaged = `git status --porcelain 2>/dev/null| grep "^ M" | wc -l`.to_i
  total_uncommitted = `git status --porcelain 2>/dev/null| egrep "^(M| M)" | wc -l`.to_i
  
  if uncommitted != 0
    puts "You have uncommitted changes that will be lost if you deploy."
  elsif unstaged != 0
    puts "You have unstaged changes that will be lost if you deploy."
  elsif total_uncommitted != 0
    puts "You have uncommitted or unstaged changes that will be lost if you deploy."
  elsif diff != 0
    puts "You must pull and push changes before deploying."
  else
    current_dir = Dir.pwd
    commit_message = IO.popen("git log -1 --pretty=%B").
      readlines.first.strip.gsub('"', "'")
    `git rev-parse && cd "$(git rev-parse --show-cdup)"`
    puts "Generating site with Jekyll..."
    build_result = `jekyll build 2>&1`
    if $? == 0
      `cp -rp _site/ ../tmp/`
      puts "Updating site locally..."
      `git checkout gh-pages --quiet`
      `rm -rf _includes > /dev/null 2>&1`
      `rm -rf _layouts > /dev/null 2>&1`
      `rm -rf _posts > /dev/null 2>&1`
      `rm -rf _site > /dev/null 2>&1`
      `rm -rf css > /dev/null 2>&1`
      `rm -rf font > /dev/null 2>&1`
      `rm -rf js > /dev/null 2>&1`
      `rm -rf jekyll > /dev/null 2>&1`
      `rm .gitignore > /dev/null 2>&1`
      `rm _config.yml > /dev/null 2>&1`
      `rm CNAME > /dev/null 2>&1`
      `rm index.md > /dev/null 2>&1`
      `rm Rakefile > /dev/null 2>&1`
      `rm index.html > /dev/null 2>&1`
      `cp -r ../tmp/ ./`
      `rm -rf ../tmp > /dev/null 2>&1`
      puts "Deploying..."
      `git add --all && git commit -m "#{commit_message}" --quiet && git push -f origin gh-pages --quiet`
      `git checkout master --quiet`
      `cd #{current_dir}`
      puts "Done."
    else
      puts "Error generating site:"
      puts "#{build_result}"
    end
  end
end