## Core Data

Core Data is a persistent data store. It is not a database. This is seriously
one of the most confusing technologies in the iOS ecosystem, but it is
something *you must learn*. In the integrating with APIs section you'll learn
even more about Core Data and how to save both locally and sync up to the
cloud. Think about all of the apps you use. Most of them can be boiled to down
to displaying some data that is synced to a service.

### App
Try and save your ToDos locally using Core Data. 

### Learning Objectives
  - Understand how read and write data from the NSManagedObjectContext
  - Persistant CoreData to the device using sqlite3
  - Work with CoreData with TableViews
  - Autogenerate, and extend CoreData Model files
    16 is great for this.

### Advanced
  - Chapter 9 of Learning iOS Development
  - [Pro Core Data for
    iOS](http://www.amazon.com/Pro-Core-Data-Second-Edition/dp/1430236566/ref=pd_sim_b_26 "Pro Core Data For iOS")
    - Told you it was a big topic.
  - [Core Data Tutorial for iOS: Getting
    Started](http://www.raywenderlich.com/934/core-data-tutorial-for-ios-getting-started "Core Data Tutorial for iOS: Getting Started")
    - Practical example on how make a Core Data app. Make sure you read all three parts. The NSFetchedResultsController part
      is super important and how you connect Core Data to UITableViews.

### Libraries

  - [MagicalRecord](https://github.com/magicalpanda/MagicalRecord "Magical
    Record GitHub Page")
    - Library that automates a lot of the common CoreData stuff and implements
      some best practices.


### Reference

  - [Core Data Quickie](http://borkware.com/quickies/one?topic=Core%20Data
    "Core Data Quickies")
