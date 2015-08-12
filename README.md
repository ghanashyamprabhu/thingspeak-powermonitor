# thingspeak-powermonitor
Example node js code to upload AC power readings from my power meter onto Thingspeak.com
Example uses the nodejs modules thingspeakclient - note this npm package has a dependency
on socket.io npm package

    Installing dependencies
        > npm install socket.io
        > npm install thingspeakclient 
        
        Optionally you can specify -g while installing these modules so that they are usable
        globally by code in any directory. 
   
    Thingspeak Setup

        a. Signup on Thingspeak.com and create a channel. 

        b. A channel can be private or public, choose which ever is appropriate for your 
        application. Once a channel is created, you can name the channel to whatever you 
        chose to but Thingspeak will allocate a channel ID. 
        My channel ID is 51269.
        
        c. You can also define fields for this channel - The values uploaded by your program
        will be per field. You can define multiple fields and your program can upload 
        multiple data per channel. 
        
        d. In my application, I will be uploading AC power numbers and RMS current values 

        e. Create the "Write Keys" by traversing to the Channels-> API Keys -> Generate 
        WriteKey. Thingspeak will generate a Alphanumeric Key that can be used in your 
        program which uploads data to this Channel.

    Your client program
        See below example for the client program uploading data to channel 51269!!

