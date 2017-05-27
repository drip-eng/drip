# Scalability

* Above all, split the app into microservices.  Web delivery/core-app, ingress, analytics, and databases should all be separate and independently scalable.

* Setup development workflow with some sort of conditional or a separate dockerfile so that we can run it locally without SSL certs

* Build for fault tolerance.  We will have to decide if this is a simple matter of elastic IP/georeplication, or if we need to start talking SQS.

* Move to RDS, providing easy scalability and automated management and replication.

* Move to a sharded model -- for geospatial data this will result in MASSIVE improvements in performance.  Discord has a great blog post on sharding that you guys should check out: https://blog.discordapp.com/how-discord-indexes-billions-of-messages-e3d5e9be866f

* Architect with the potential for Elastic Load Balancing in mind.  We will have a lot of runway for the core app (separate from the database) to be scaled vertically, however at some point we will have to start thinking horizontal.  

# UX

* Establish UX and design guidelines throughout the app.  

# Feature Enhancements

* Add new datasets
  - Parcel data (probably a new dataset from each count. not all are available on CIM and we may need to contact individual counties.)
  - Oil & Gas leases
  - Oil & Gas structures
  
* Ability of user to turn off/on layers if not of interest
  
* Reports
  - Summarize in downloadable .pdf the data for items found within parcel of interest
  - Summarize in same report items found outside parcel in user-defined (distance or polygon) areq of interest 
  - Include in report analytics performed within area of interest
  
* Consider making the subscription tier a premium service (no change to plan on pay-per-use tier)
  - Create property profiles
  - Upload additional data on the property (imagery, DEMs, photos, etc.)
  - Map imagery shareable with customers
  
* OCR scanned documents

# Analytics

* Get to hello-world with PDF generation.  Our library takes HTML/CSS input, so we can tightly integrate it with our current templating system.

* Discuss key metrics that we want to focus on and figure out how to provide the most value to users.

* Build out our tensorflow/ML implementation.  Vincent already well versed, david has been reading and watching fanatically for a few weeks.

* Potentially implement a messaging/notification/email service for water rights expiry?  Is this feasable?

# Productization

* Implement authentication system.

* Implement "saved queries/documents/reports" type of interface.

* Implement payment/subscription system
  - Integrate app with commerce site
  - Integrate app with financial system that automatically invoices and charges credit cards for subscriptions

# Marketing

* Develop press kit
  - Write initial press releases
  - Write Drip origin story
  - Logos
  - Design guide
  - Bios

* Consider free use to affiliate marketers -- i.e., people in the real estate industry giving their clients pay-per-use promo codes and receiving free use-time in return.

* Create Social Media accounts
  - Decide on how to best promote product on outlets like facebook and Twitter
  
* Identify and join industry meetups

* Identify State of Colorado gov't agency personnel that may utilize Drip

* Identify water industry experts in Colorado
