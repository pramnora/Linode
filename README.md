# Linode
Linode, create/build/run your own online servers...for a price.

## CREATING/BUILDING/RUNNING ONLINE SERVERS AT LINODE.COM  

### Running Linode Server, Charges...  

Today, 29 September 2021, I had a most truly remarkable experience; namely, I visited the 'cloud hosting' service...    
- https://www.linode.com  
...and, after reading up about the charges for creating/building/running your own online server...;    
discovered the price is, in fact, fairly 'cheap'; namely,...    
- £0.01p per hour  
- £5.00 monthly  

**NOTE(1)**: Remember to select the right tab...which says: 'Shared hosting'/together with a computer equipped with: 1GB RAM/4GB memory. (least expensive package)   

**NOTE(2)**: Unless you do remember to take the server down, completely...; then, they will charge you whether the server is actually up and running/or, not...?!    
 
### Registering to use the Linode Service...  

Basically, all one has to do to register with the Linode service is...give them your...    
- name: First Name/Last Name      
- email  
- credit card  details  
...they will send you an email which you click on to confirm it's you;   
and, that's it you're, now, fully registered to use their services.  

### Creating your 1st server instance on Linode...  

As you sign in to Linode...there is a menu of the left hand side...;  
automatically, selected is the option: Linodes.  

Then, you just configure the page how you want...  
- What type of server: Debian/UBuntu/-etc. (I choose Ubuntu 20:04 LTS)    
- Select how much server capacity you want. (I choose 1GB RAM/4GB HDD...which was the 'cheapest' option)      
- Give the server a reference name: Ubuntu-2004-server1  
- Choose the location which is nearest you: London/UK  
- Select a 'root' password to use with your server.   
- Finally, click on button: [Create]  
...and, basically, that was it...I had Linode server 'up and running'...;    
you are given an IP address to SSH/Secure Shell into...  
root@xx.xx.xx.xx

### Runing the server...using Linode online Web Browser console window...   

In order to make the server run...      
- click on [Power On]  
...the button light will go from gray/yellow/orange/green;  
(green light meaning it's fully on...and, ready to take commands;  
 gray light meaning it's, now, off; and, therefore, no longer running.)         

Also, click where it says: [Launch LISH console]...;    
...which will launch the 'web browser based' sever console.  

Next, you can sign in to the online web browser based console, type...  

>> root    
>> password:    
>> root@hostname~:  

...and, that's it, once you can witness seeing the Linux prompt...  

>> root@hostname~:  

...this means, you are now running your very own web server 'live'...;    
-(though, it might take a minute or two getting it to fully provision/boot up...)-;    
and, can now run all sorts of Linux based commands such as: cal/ls/pwd/-etc.  

**NOTE(1)**: Using the Linode web browser console: LISH/GLISH...;  at first, I typed in...   

>>root@xx.xx.xx.xx  

...which worked...; then, later on, stopped working?! Instead, I had to type in, simply...  

>>root  

...in order to get things back up and working, again.  

**NOTE(2)**: Using any other SSH method -(Putty/MS DOS/Powershell/FileZilla)- I found that signing in as...  

>>root@xx.xx.xx.xx  

...worked just fine.  

### Setting up the Linux system to work...

There are certain things you need to do, first; when you set up and run a 'new' Ubuntu Linux server... 

#### Make sure the system is fully updated... 

The first thing you should do is make sure your server is fully up to date with the very latest packages/security fixes/-etc.    
type:   

>> root@hostname~: apt update && apt upgrade  

...then, wait for the updating/upgrading process to be done.    

#### Select your own hostname(optiona)... 

The next thing you may, optionally, wish to do is change the hostname prompt which says:   

>>root@hostname~:  

...to become a 'new' hostname that you might prefer...type in...  

>>root@hostname~: hostnamectl set-hostname yourPreferredHostName  

-(now you will need to logout out...by typing: exit...then, log back in, again...to see the prompt change to become...)    

>>yourPreferredHostName@~:    

#### Add newuser to go sign in with...

It is not recommended that you sign in to your server using your 'root' a/c.; which has the privilige to do absolutely anything...;    
but, instead, you should go and create a 'new' user account to go sign in with, instead...; that has 'limited' privileges.

>>root@hostname~: adduser guest

...next, you will be asked to supply a 'password' for the new guest user. After supplying the password...;     
next, keep on pressing [Enter] key to accept the default settings for such things as: add name/number/-etc.     
until you return back to the usual prompt; then, type: exit...  

>>root@hostname~: exit

...this will sign your root /ac. out; and, thus, force you to sign back into the Linux system, again...;  
only this time you will sign in as...  

>>ssh guest@xx.xx.xx.xx
>>password:  

...then, when you enter back into the system...the system prompt should change to say...

>>guest@hostname~: 

...meaning you are now signed into the system as, guest.

-(**NOTE**: Guest, does not have access to the root system user files/nor are they allowed to add 'new users' themselves.)-  

#### Set date/timezone...

>>timedatectl list-timezones  

...use arrow keys: up/down...to navigate to seeing what is your correct location timezone: Europe/London; then, press 'q' to quit navigating through the list...  

>>timedatectl set-timezone 'Europe/London'  

...next, check the date/time is correct...

>>root@hostname~: date  
>>Fri 1st Oct 2021 06:17:14 AM BST  

### How to 'stop' the server running...; meaning, put it on pause...(ready to run, again/with all your data/configuration still intact)...  

In order to 'stop the server running...you will need to do 2 things...  

- Type: exit, to quit running the Linux sesssion.   
- Click the web browser console button: [Power Off]    

### How to 'delete' the server, altogether...; and, not just merely pause/'stop' it running...(will also delete all previous data/configuration)...            

**NOTE**: Because, as long as you own an instance server...that's always ready and waiting to run...;    
          which, at the same time, is storing 'your' data on it.../and, 'your' configuration set up...;  
          you will, of course, still be charged money  
          whether that server is actually up and running still/or, not...?!   
   
          Therefore, if you don't wish to maintain running the server, constantly...;   
          and, thus, prevent any charges from further accumulating...;    
          it's best to 'delete' the server instance, altogether.   
          Just try looking for the 3 dots ellipses: ...; next, to option [Power on]...;    
          then, a drop down menu will appear...all you have to do is click option: [Delete].  
          
          -(However, when you do 'delete' the server altogether;  
          then, next time, you will have to set up running a brand 'new' server instance...starting, again, from total scratch;    
          and, also, be given a brand new IP address...to connect to...;  
          too, all of your previously entered server data/configurations would have completely vanished/gone...?!)-   

### Running the server remotely...using SSH/Secure Shell...in Windows MS DOS/or, Powershell   

What really surprised me, somewhat...  
-(though, I have used Windows 'Putty' software to remotely SSH into my Raspberry Pi single board computer machine, before)-    
...was realising I don't need to use Linode web browser interface to connect to my server;    
instead, I can use either: MS DOS Command Prompt/or, Powershell...; either way the instructions are the same...  

>> ssh root@xx.xx.xx.xx  
>> password:   
>> root@~:  

...then, it's possible to issue all of the same linux commands as is usual.  

### Running the server using Putty software...

I tried SSH-ing into Linode server using Putty software...  

First, you type in the IP Address as: xx.xx.xx.xx  
Next, you click [Open session]  
Then, you are asked for your name: root  
followed by password:  
...if you typed your password, correctly; then, you are let in.  

>>root@localhost~:

### Running the server using FTP software/FileZilla...

I decided to try out connecting to the remote web server using FileZilla FTP software...

>>host: xx-xx-xx-xx  
>>name: root  
>>password:   
>>port: 22  

...and, much to my surprise it actually worked.   
Horray, I can now very easily both create/transfer: 'upload/download' files...in between Windows 10 Pro/Linux Ubuntu 20.04 LTS! ;-)  

-(**NOTE**: There may be some diffence between the two file systems...; for example Linux doesn't need to use any dot + fileNameExtension.)-   

## Some basic LINUX commands...

List files/folders...  
>>root@localhost~: ls  

Show what is the current working folder directory path/(print working directory)...  
>>root@localhost~: pwd  

Create a new file...  
>>root@localhost~: touch fileName.fileNameExtension  

**NOTE**: Linux files don't need to have any 3 letter file name extension at all/(unlike Windows)     

Make a folder...  
>>root@localhost~: mkdir dirName  
  
Move to a different folder...
>>root@localhost~: cd dirName  

Move backwards...  
>>root@localhost~: cd ..  

Show the current calender date...
>>root@localhost~: cal  

Open a text editor...(all on it's own)...  
>>root@localhost~: nano 

Open a text editor...(with a fileName)...  
>>root@localhost~: nano fileName.fileNameExtension    

Switch to system root...    
>>root@localhost~: cd /  
...will take you directly into the Linux system root...    
which when you do an: ls...will list all of the most important folder directories.  
in order to return back to the normal prompt...  
>>cd home/username  
...where username in this case would be, root  

**NOTE**: Either reading a good Linux tutorial book...  
-(especially, concerning what is the particular Linux distribution you wish to use)-;    
or, watching a few YouTube Linux command tutorials...would most certainly help out an awful lot     
before you try running any Linux based server.     

## CURRENT PROBLEMS...

Here are a few of the difficulties I'm having...

- Being mostly 'unfamiliar' with the use of Linux commands...;    
  therefore, it is really very 'limited' the type of things I can do...?!        
  
- Instead, of having to communicate with the Linux server through using a CLI/Command Line Interface...meaning, all 'text' based commands;      
  I would have much preferred using a GUI/Graphical User Interface, instead; just not sure how to set this up...?    

- I saw it mentioned somewhere that if you use, instead of:   
  ssh root@xx.xx.xx.xx      
  ...add a -X...         
  ssh -X root@xx.xx.xx.xx  
  ...then, the graphical interface might work;   
  but, when I tried doing that...  
  after, first, installing...  
  apt get firefox  
  ...then, calling up...    
  firefox  
  ...it didn't work?!  
  
- At first, I was able to get in using [Launch LISH Console]...;      
  but, then, each time I tried doing the same thing, later on...;   
  I'd gone and created 2 brand new sever instances...  
  it didn't work...?!      
  The error message kept on saying...  
  Login incorrect  
  ...after trying, again and again, repeatedly; I decided to quit using that method;  
  (even, though, I was able to get in through using other methods: MS DOS/Powershell/Putty;  
   so, I'm not exactly sure what I did wrong...?!)  
 
- As well as, [LISH]/I noticed something beside it called: GLISH...;    
  I don't know if GLISH is meant to be the Graphical UI, possibly...;    
  anyway, both LISH/GLISH wouldn't let me in, anymore...;      
  (either the way I tried connecting using root/password/or, something not quite working...)?!    

 - Normally, the server when you hit [Power off] would shut down in under 1 minute long...;    
   however, one time I tried shutting it down...; and, it took over 4 minutes long to to shut down...;     
   which made me wonder if it was ever going to shut down at all...?! But, it did, eventually.   
   
 - When signed into the very first page of Linode system;   
   select 'Account' from the main menu on the left...;    
   which will allow you to be able to...   
   ...view how much money you owe  
   ...make pre-payments towards your account, immediately  
   
 ## CONCLUSION
 
 I do not have any regrets at all about going and signing up with the 'cloud provider', Linode.      
 Their online service is really pretty straight forwards/and, therefore, simple and easy to use...;    
 -(some of these other 'cloud providers': Amazon AWS/Azure/Google/-etc.;     
   their public offerings seem to be really 'complex'...in direct comparison?!)-   
 also, the Linode site itself, offers a lot of online documention in the form of both...  

 - help files  
 - YouTube channel help/(videos)  
 
 ...in addition to which the service if properly used can also be, relatively, 'inexpensive';    
 costing only £5.00 a month...is not so bad to have public server, constantly, up and running;  
 into which you can...
 
  - practice using the Linux system commands...(and, for many different varieties of Linux: Debian/Ubuntu/-etc.)     
  - run Linux based program files: C/BASH shell scripts  
  - experiment with Linux editors: Nano/Vim    
  - FTP/File Transfer Protocol (exchanging files between Windows & Linux)      
  - display files   
  - store files  
  - add web pages  
  - etc.  

If all you wished to do...was to simply...    
- start a server/(and, keep it running for just a few minutes/hours...)  
- test it  
- stop it, running  
- then, delete it, afterwards.    
...then, the actual price you would pay to do that is just merely pennies/NOT pounds.    

Alongside the advent of modern day 'cloud computing'...  
computer operators/programmers can both study/learn 'hands on', very cheaply, indeed;      
if not entirely all for FREE.  
This is because they are no longer 'forced' to...   
- buy programming languages/manuals  (many of which can be downloaded for FREE)  
- buy computer boxes.../containing different operating systems inside   

...which makes the learning process both a lot less costly/and, also, makes learning 'fast'.         

## LINKS...

### Linode Guides...

Website guides  
- https://www.linode.com/docs/guides/websites/  

Getting Started with Linode  
- https://www.linode.com/docs/guides/getting-started/  

Securing Your Server  
- https://www.linode.com/docs/guides/securing-your-server/  

connnect to your linode via ssh  
- https://www.linode.com/docs/guides/getting-started/#connect-to-your-linode-via-ssh  

Website Hosting...  
- https://www.linode.com/docs/guides/websites/hosting/  
- https://www.linode.com/community/questions/18479/how-do-i-host-my-website-with-linode  

StackScripts...  
- https://www.linode.com/docs/guides/platform/stackscripts/  

### Web site hosting...

YouTube videos...

WordPress on Linode Hosting Tutorial Video  
- https://www.youtube.com/watch?v=OpifyG32CMs  

DIY Linux Webserver from Start to Finish Hosted by Linode  
- https://www.youtube.com/watch?v=H8K-Rg_7Tbo 

### Object storage...

S3 Object Storage on Linode | Getting Started  
- https://www.youtube.com/watch?v=q88OKsr5l6c  

Deploy A Static Website Using The Linode CLI | Object Storage Tutorial  
- https://www.youtube.com/watch?v=ZfGyeJ8jYxI  






