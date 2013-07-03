# lightwaverf-app

A web app for lightwaverf. Install the gem, get a LightWaveRF wifi link http://amzn.to/V7yPPK and a remote socket http://amzn.to/RkukDo and you're away!

This is a sub-repo of http://github.com/pauly/lightwaverf so install that:

    gem install lightwaverf

## How to install the website in this repo on a raspberry pi

  * Install node https://gist.github.com/stolsma/3301813 (it takes an hour or so to build node on the pi.)
  * Then I built in authentication using twitter too, so that the site can be up and running and public, but you'd need to be authenticated to see the usage graphs, so to do that register an app at dev.twitter.com/apps - don't think it matters what you use for any settings but when it's done go to the oauth settings get  the consumer key and consumer secret, copy config/default.sh.sample config/default.sh and paste those values in. Then there are a couple of depencies I think so

    npm install

  * Then start the site with

    source config/default.sh && nohup node app.js &

  * hope that works and the site would then be running on port 3000 on your pi's ip address.

  * Not sure how stable it is but there is a file called "node" in the repo that you can copy into /etc/init.d/ and it should restart the server when the pi restarts. 

# Thanks

If you want to improve any of my docs or code then please fork this and send me a pull request and I'll merge it in.

