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
"External Port" - The port that you will use to access the website.  
"Server Internal Port" - The port that the server runs on in internally.  
"Datomic host IP address" - This must be filled in with the IP address of the datomic IP address.  
"Error Email" - The email address that you wish to send errors to.  


### Nginx Proxy  

#### Enable built in homebrew.  
I personally use Nginx Proxy Manager provided via Community Apps.  

You will need to add a proxy host with SSL to use orcpub. To enable embedded homebrew, you will need to add the below line under the advanced tab.
~~~~ 
location /homebrew.orcbrew {root /usr/share/nginx/html/homebrew; } 
~~~~

You will also need to add a volume to store your "homebrew.orcbrew" where Nginx can access it.  
Mount the below location in the container to a location that you can access.
~~~~
/usr/share/nginx/html/homebrew/
~~~~
