# Unraiad_Docker_Templates


## Configuration

### datomic-free
You will need to set the location where you wish the database to be stored.  

Set "Data Path" to your prefered appdata folder.  
The "Datomic Password" and "Datomic Admin Password"  will need to match between this and the Orcpub2-server container.  
You should not have to adjust the port settings.  


### Orcpub2-server  
In oder for accounts to be created, you will need to provide SMTP details for your preferred provider.  

The following settings need to be adjusted.  

"Datomic URL" - Change <DATABASE_URL> to the IP address of your server, and channgne <DATABASE_PASSWORD> to the "Datomic Password"
"Datomic Admin Password" and "Datomic Password" - These should match with what you set in the datomic container.
"Host Port 1" - 
