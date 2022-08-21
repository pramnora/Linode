# Linode
Linode, create/build/run your own online servers...for a price.

# TOC/(T)able (O)f (C)ontents:-  

## CREATING/BUILDING/RUNNING ONLINE SERVERS AT LINODE.COM  
### - Running Linode Server, Charges...  
### - Registering to use the Linode Service...  
### - Creating your 1st server instance on Linode...  
### - Runing the server...using Linode online Web Browser console window...   

## Setting up the Linux system to work...
### - Select your own hostname(optional)... 
### - Add newuser to go sign in with...
### - Set date/timezone...

## How to Stop/Delete server...  
### - How to 'stop' the server running...; meaning, put it on pause...(ready to run, again/with all your data/configuration still intact)...  
### - How to 'delete' the server, altogether...; and, not just merely pause/'stop' it running...(will also delete all previous data/configuration)...            

## Using SSH to operate the server remotely...
### - Running the server remotely...using SSH/Secure Shell...in Windows MS DOS/or, Powershell   
### - Running the server using Putty software...
### - Running the server using FTP software/FileZilla...

## Some basic LINUX commands...
## Linux text editor(s): Nano/Vim/Vi/-etc.
### - Using Nano text editor...
## Setting Linux file permissions...
## Creating/running scripts...
### - Creating/running your first BASH shell script...

## Installing programs...
### - Installing Python...
### - To create and run a python program file: [.py]...   

### Installing Redis database...
### - Check Redis is fully up and working
### - How to run Redis
### - How to quit redis
### - Check if you can SET/GET data back
### - Multiple SET/GET
### - Additional notes: Where to go in order to learn more...

## Create your own Web Server
### - Setting up
### - Checking the default test web page inside of your browser
### - Replacing the default test web page with your own web page, instead
### - View your test web page inside of any web browser
### - Additional notes 



## CURRENT PROBLEMS...

## CONCLUSION

## LINKS...
### - Linode Guides...
### - Web site hosting...
### - Object storage...

## CREATING/BUILDING/RUNNING ONLINE SERVERS AT LINODE.COM  

### - Running Linode Server, Charges...  

Today, 29 September 2021, I had a most truly remarkable experience; namely, I visited the 'cloud hosting' service...    
- https://www.linode.com  
...and, after reading up about the charges for creating/building/running your own online server...;    
discovered the price is, in fact, fairly 'cheap'; namely,...    
- £0.01p per hour  
- £5.00 monthly  

**NOTE(1)**: Remember to select the right tab...which says: 'Shared hosting'/together with a computer equipped with: 1GB RAM/4GB memory. (least expensive package)   

**NOTE(2)**: Unless you do remember to take the server down, completely...; then, they will charge you whether the server is actually up and running/or, not...?!    
 
### - Registering to use the Linode Service...  

Basically, all one has to do to register with the Linode service is...give them your...    
- name: First Name/Last Name      
- email  
- credit card  details  
...they will send you an email which you click on to confirm it's you;   
and, that's it you're, now, fully registered to use their services.  

### - Creating your 1st server instance on Linode...  

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

### - Running the server...using Linode online Web Browser console window...   

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

## Setting up the Linux system to work...

There are certain things you need to do, first; when you set up and run a 'new' Ubuntu Linux server... 

### - Make sure the system is fully updated... 

The first thing you should do is make sure your server is fully up to date with the very latest packages/security fixes/-etc.    
type:   

>> root@hostname~: apt update && apt upgrade  

...then, wait for the updating/upgrading process to be done.    

### - Select your own hostname(optional)... 

The next thing you may, optionally, wish to do is change the hostname prompt which says:   

>>root@hostname~:  

...to become a 'new' hostname that you might prefer...type in...  

>>root@hostname~: hostnamectl set-hostname yourPreferredHostName  

-(now you will need to logout out...by typing: exit...then, log back in, again...to see the prompt change to become...)    

>>yourPreferredHostName@~:    

### - Add newuser to go sign in with...

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

### - Set date/timezone...

>>timedatectl list-timezones  

...use arrow keys: up/down...to navigate to seeing what is your correct location timezone: Europe/London; then, press 'q' to quit navigating through the list...  

>>timedatectl set-timezone 'Europe/London'  

...next, check the date/time is correct...

>>root@hostname~: date  
>>Fri 1st Oct 2021 06:17:14 AM BST  

## How to Stop/Delete server...  

### - How to 'stop' the server running...; meaning, put it on pause...(ready to run, again/with all your data/configuration still intact)...  

In order to 'stop the server running...you will need to do 2 things...  

- Type: exit, to quit running the Linux sesssion.   
- Click the web browser console button: [Power Off]    

### - How to 'delete' the server, altogether...; and, not just merely pause/'stop' it running...(will also delete all previous data/configuration)...            

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

## Using SSH to operate the server remotely...

SSH/Secure SHell...is a way you can run a server remotely...by using special software build for that same purpose.  

### - Running the server remotely...using SSH/Secure Shell...in Windows MS DOS/or, Powershell   

What really surprised me, somewhat...  
-(though, I have used Windows 'Putty' software to remotely SSH into my Raspberry Pi single board computer machine, before)-    
...was realising I don't need to use Linode web browser interface to connect to my server;    
instead, I can use either: MS DOS Command Prompt/or, Powershell...; either way the instructions are the same...  

>> ssh root@xx.xx.xx.xx  
>> password:   
>> root@~:  

...then, it's possible to issue all of the same linux commands as is usual.  

### - Running the server using Putty software...

I tried SSH-ing into Linode server using Putty software...  

First, you type in the IP Address as: xx.xx.xx.xx  
Next, you click [Open session]  
Then, you are asked for your name: root  
followed by password:  
...if you typed your password, correctly; then, you are let in.  

>>root@localhost~:

### - Running the server using FTP software/FileZilla...

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







## Linux text editor(s)...

Linux, comes with many text editors: Nano/VIM/Vi/-etc.  

### - Using Nano text editor...

By far the simplest text editor for beginner's to use is Nano...;    
you can load Nano text editor like so...  

>>root@localhost~: nano  

...alternatively, if you wish to load nano text editor/whilst, at the same time, giving the file a name; then, use...  

>>root@ localhost~: nano fileName  

-(**NOTE**: Unlike in Windows...Linux filenames do not need a dot(.) + fileNameExtension...; so, just the filename alone will do;  
unless you wish to share/(FTP) files between Windows and Linux...; in the which case, I would include both the .fileNameExtension.)-  

Next, write a few lines of text into Nano text editor...  

>>This is   
>>my first   
>>text file  
>>created using   
>>Nano editor.  

...you can use the arrow keys: 'up/down/left/right'...to navigate your way around the file...    
...and, also, select where you wish to either...    
add characters...by typing in some more text.../    
or, delete characters...by using the [Backspace] key...    
...use [CTRL] + [X] to exit from Nano file editor...    
it will ask you: save modified buffer...type: Y...  
-(if you wish to save the changes to your modified file)-;  
next, it will ask you: File name to write: fileName  
-(if you did already set up a filename/but, if not...then, you can type in your file name here)-    
press the [Enter] key to confirm; and, you will be led straight back to the Linux prompt.   

>>root@localhost~:  

...if you wish to see the file changes you just made...then, just use: 'ls'...  
-(to check the file exists inside of the current folder directory...)-  

>>root@localhost~: ls  
>>filename  

...then, use 'cat'...which will display the file text on screen...  

>>root@localhost~: cat filename   

This is  
my first  
text file  
created using  
Nano editor  








## Setting Linux file permissions...

Each file on linux has set permissions...represented by a series of 10 dashes: (-)...     

>> (- --- --- ---)    

The first dash indicates if the file is either...

>> d (a folder)  
>> (-) (a file)  

Each next set of 3 x 3 dashes: (---) represents, successively...  

1> owner  
2> group  
3> other  

Each set of 3 x 3 dashes may show as being a successive letter: (rwx)/or: (-)...    

1> r = read permission   
2> w = write permission     
3> x = execute permission        
4> (-) = nil permission  

In order to view files with their permissions set...; use...   

>>root@localhost~: ls -l    

...which, then, shows not just the filenames, alone, as with the command: (ls)...;   
but, also, displays what file permissions have been given to each file.        

In order to set file permissions...use the command: (chmod)...

> chmod 0 filename = nil permission         
> chmod 1 filename = execute      
> chmod 2 filename = read    
> chmod 3 filename = execute/read  
> chmod 4 filename = write    
> chmod 5 filename = execute/write  
> chmod 6 filename = read/write  
> chmod 7 filename = read/write/execute       

**NOTE**: These numbers can be added up to form totals...so, 1(x)+2(r)+4(w)=7...; or, 'rwx'...meaning, all permissions being granted.  

-(**NOTE(2)**: I'm not absolutely 100% sure I got all of these numbers quite right...; so, will have to go do a check...?!)-  

...so, the command...    

> chmod 777 filename  

...would mean...owner:read/write/execute group:read/write/execute other:read/write/execute    
-(in other words everybody can execute that particular file)-  

> chmod 000 filename...    

...would mean...no permissions being granted to anyone.  

## Creating/running scripts...

Linux, allows users to create/run scripts...  

- Sh  
- Bash (which is the most common)  
- Csh  
- Tcsh 

### - Creating/running your first BASH shell script...

Open Nano...; and, give it a filename to save of: script01...  

>>root@localhost~: nano script01   

...next, type in the following lines of BASH related code...  

>>#!/bin/bash  
>># # Lines prefixed with the hash symbol: (#) means...This is a comment    
>>echo This is my first BASH script.  

Use [CTRL] + [X] to exit from Nano editor; [Y] to save; [Enter] to confirm the file name...  

>>root@localhost~:                    <----      (this is the normal Linux root prompt)  
>>chmod 744 script01                  <----      (this line sets the file 'rwx-read/write/execute' permissions: owner: 7=rwx/group: 4=r, only/other: 4=r, only)  
>>ls -l                               <----      (this line displays files with their permissions)   
>>-rwxr--r--                          <----      (this line shows the file permissions)     
>>bash script01                       <----      (this line executes the script file code)    
>>This is my first script             <----      (this the script file output)    







## Installing programs...

It's possible to use Linux to install further programs...  








### - Installing Python...

First, I did a check to see if Python was already installed...    

>>root@localhost~: python    

...the answer came back, no. So, I decided to install it using...    

>>root@localhost~: apt install python    

...then, to check which python version I had just installed...  

>>root@localhost:~: python  
>>Python 2.7.18 (default, Mar  8 2021, 13:02:45)  
>>[GCC 9.3.0] on linux2  
>>Type "help", "copyright", "credits" or "license" for more information.  
>>(>>>)  

-(**NOTE**: The 3 right pointing chevrons:(>>>) are the Python prompt...;     
after which you type in Python code which will then be evaluated.)-   

To run 2.7.18 python code...   

>>(>>>)print 1+1    
>>(>>>)2    
>>(>>>)exit()  
>>root@test-server~:     

**NOTE**: Use 'exit()' to exit out of the Python coding environment.  

### - To create and run a python program file: [.py]...   

>>nano python01.py  
>>(#) This is my first python script...   
>>print "Hello, world!"  

...type: [CTRL]+[X] to quit Nano editor/type: [CTRL]+[Y] to save/type: [Enter] to keep what is the current file name.  

>>chmod 744 python01.py  
>>ls -l  
>>-rwxr--r-- python01.py   
>>python python01.py  
>>Hello, world!   








### Installing Redis database...

apt-get install redis

### - Check Redis is fully up and working

redis-server

### - How to run Redis
redis-cli

### - How to quit redis

127.0.0.1:6379>quit

### - Check if you can SET/GET data back

redis-cli
127.0.0.1:6379>SET name Paul
OK
127.0.0.1:6379>GET name
"paul"
127.0.0.1:6379>

### - Multiple SET/GET

MSET a 1 b 2 c 3
MGET a b c
1
2
3

### - Additional notes: Wehre to go in order to learn more...

- Go to Redis main web site to learn more
- Study Redis vidos on You Tube








## Create your own Web Server  

Believe it or not...; but, setting up and running your own Apache web server is really quite simple and easy to do...    

### - Setting up

First, download the Apache software...  

>>apt install apache2  

Next, check that the software is properly installed...   

>>systemctl status apache2  

### - Checking the default test web page inside of your browser

Now, type in the following command to discover what is your IP address...  

>>hostname -I  
>>xx.xx.xx.xx   (-etc.)   

Move over to your normal web browser software...; and, type in the IP address just as you see it above...in dotted quad format...;    
and, you should see an Apache Web Server 'test page'...waiting to be replaced.  

### - Replacing the default test web page with your own web page, instead

Next, move to...  

>>cd var/www/html  
>>ls   

...and, there you should see a web page called: [index.html];    
this is the standard Apache Web Server page that we wish to replace.    

Replace this file by either deleting it/or else, by simply renaming it...    

>>mv index.html index2.bak    

Open up nano text editor...; and, write a replacement web page...    

>>nano index.html   
>>Just a test...  

Press [CTRL]+[X], [Y] to confirm, [Enter] to re-write.  

### - View your test web page inside of any web browser

Now, just like before, go over to your web browser software...; and, press the [F5] key to do a page refresh...;  
and, you should see the test [index.html] web page...that you just went and created.  

### - Additional notes 

**NOTE(S)**:-     
The above 'quick 'set up route...is, most definitely, **NOT** the safest way to do it...; instead, it's totally *unsafe*...?!         
-(I merely showed it to you...in this really 'quick' manner...just to prove how fast these things can be done;       
  with the sole intention of putting up a web page...and, then, serving it over the internet.   
  but, if you want to make sure your web server/ports are secure...; then, you will need to follow some further steps.)    

1> This web page is served up using 'http' protocol...; so, it is not a secure 'encrypted' connection such as is: 'https://'    
2> The web server ports need to be properly secured...; otherwise, your web server could be open to all sorts of internet attacks.    

In order to read more about how to set up/run Apache 'safely'...go check out the following link...   
https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-ubuntu-20-04    

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

 - I still haven't written any C programs to run yet.  
   I believe that straight out of the box...without needing to do any further setting up...   
   you can run...  
   
   - BASH scripts  
   - C programs  
   
   ...I believe, I did it using my Raspberry Pi's Linux; but, forgot how...?!  
   
 - By far the biggest problem I have with running a Linode server is the steadily accruing charges...;  
   and, especially, if you leave the server up...without deleting it; because whether it is powered on/or, off...  
   you will still be accumlating charges.  
   
   I believe that the 'cheapest' way to test out Linux system...is to use something like VMWare...;  
   which emulates an operating system...; and, then, you can test it on your Windows based computer for FREE.  
   Otherwise, if you choose to do things this way, instead...; it could all cost you a pretty penny, I'm afraid!  
   The only way to keep the cost of running the server down to pennies...as opposed to pounds...;  
   is to delete the server straight after using it; otherwise, you will still be charged for a server you are NOT using...  
   even while you sleep...!  


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
  - Run your own Web Server: Apache2 (serve up your own web pages viewable over the internet)     
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

### - Linode Guides...

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

### - Web site hosting...

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

