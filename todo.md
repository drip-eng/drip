# Scalability

* Above all, split the app into microservices.  Web delivery/core-app, ingress, analytics, and databases should all be separate and independently scalable.

* Build for fault tolerance.  We will have to decide if this is a simple matter of elastic IP/georeplication, or if we need to start talking SQS.

* Move to RDS, providing easy scalability and automated management and replication.

* Move to a sharded model -- for geospatial data this will result in MASSIVE improvements in performance.  Discord has a great blog post on sharding that you guys should check out: https://blog.discordapp.com/how-discord-indexes-billions-of-messages-e3d5e9be866f

* Architect with the potential for Elastic Load Balancing in mind.  We will have a lot of runway for the core app (separate from the database) to be scaled vertically, however at some point we will have to start thinking horizontal.  

# UX

* Establish UX and design guidelines throughout the app.  

# Analytics

* Get to hello-world with PDF generation.  Our library takes HTML/CSS input, so we can tightly integrate it with our current templating system.

* Discuss key metrics that we want to focus on and figure out how to provide the most value to users.

* Build out our tensorflow/ML implementation.  Vincent already well versed, david has been reading and watching fanatically for a few weeks.

* Potentially implement a messaging/notification/email service for water rights expiry?  Is this feasable?

# Productization

* Implement authentication system.

* Implement "saved queries/documents/reports" type of interface.

* Implement payment/subscription system, and provide a way to offer free use to affiliate marketers -- i.e., people in the real estate industry giving their clients pay-per-use promo codes and receiving free use-time in return.

* Decide on how to best promote product on outlets like facebook and industry meetups.
