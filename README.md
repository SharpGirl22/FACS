# FACS
This project is a 3-legged stool of sorts, made up of three solutions: 
1. web piece - IDHWDataSharing - allows customers to search for shared juveniles, and provides them with contact information (among other details) when a matched ID is found by calling the DataRequest class of the API
2. matching service - IDHWService - service that runs every 20 minutes, calling the API (ClientSeach & NotificationEvent classes) for each event record found in the "staging" table
3. lookup & event notification - IDHW-API - contacts IDHW with formatted JSON for each 'event' record collected during that 20 minute timeframe, creating links for newly matched juveniles & event notifications for previously matched juveniles
