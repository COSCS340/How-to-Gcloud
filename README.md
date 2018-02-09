## The Gcloud assignment

Make a new `webserver` repo on your github user, then

![image0006](images/image0006.png)

Make an index.html

![image0007](images/image0007.png)

![image0008](images/image0008.png)

For Dockerfile:

![image0061](images/image0061.png)

![image0009](images/image0009.png)

Got Dockerfile and index?

![image0060](images/image0060.png)

Ok ready for next part

#### > create dockerhub account [hub.docker.com](http://hub.docker.com)

![image0010](images/image0010.png)

![image0012](images/image0012.png)

`Create automated build`

![image0013](images/image0013.png)

Select the repo

![image0059](images/image0059.png)

![image0015](images/image0015.png)

![image0058](images/image0058.png)

Go to "Build Settings" and hit the trigger button for master:

![image0062](images/image0062.png)

Done with the docker stuff for now.

# Now to Google Cloud

Get dat URL from the lectures repo.

![image0017](images/image0017.png)

Set up yer account

![image0018](images/image0018.png)

Make a new cs340 project if you don't have one yet:

![image0064](images/image0064.png)

Select the cs340 project

![image0022](images/image0022.png)

![image0024](images/image0024.png)

Click on the compute engine to set it up for the project:

![image0065](images/image0065.png)

![image0026](images/image0026.png)

Hmm this seems to be taking awhile...

Ok done.

![image0027](images/image0027.png)

Click on the VM instances or the link below

![image0028](images/image0028.png)

![image0029](images/image0029.png)

or go to [https://console.cloud.google.com/compute/instances](https://console.cloud.google.com/compute/instances) to create a VM instance if you don't see that button

![image0063](images/image0063.png)

"Create"

![image0030](images/image0030.png)

Check the "Deploy a container image" so that we can use our docker container.

Remember this?

![image0054](images/image0054.png)

Put that title into this:

![image0055](images/image0055.png)

Add HTTP for the firewall:

![image0033](images/image0033.png)

Click that more config stuff dropdown:

![image0056](images/image0056.png)

Now add this into the boot script: (modify it first)

```
#!/bin/bash
docker rm ws
docker run -d --name ws -p80:80 YOURGITHUBUSER/webserver
```

![image0057](images/image0057.png)

Done here.

![image0034](images/image0034.png)

Being created:

![image0035](images/image0035.png)

Done:

![image0036](images/image0036.png)

Click on that IP: WEBSITE!

E.x. [http://35.196.184.168/](http://35.196.184.168/)

Now remember to add your IP for your site to the *LAST LINE* of your markdown file in https://github.com/COSCS340/students !
