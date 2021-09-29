# Linode
Linode, create/build/run your own online servers...for a price...

## CREATING/BUILDING/RUNNING ONLINE SERVERS AT LINODE.COM  

### Running Linode Server, Charges...  

Today, 29 September 2021, I had a most truly remarkable experience; namely, I visited the 'cloud hosting' service...    
- https://www.linode.com  
...and, after reading up about the charges for creating/building/running your own online server...;    
discovered the price is, in fact, fairly cheap; namely,...    
- £0.04p per hour  
- £30.00 monthly  
 
(**NOTE:** Unless you take the server down...; then, they will charge you whether the server is actually up and running/or, not...?!)  

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
- Select how much server capacity you want. (I choose 4GB/2 Cores...which was the 'cheapest' option)      
- Give the server a reference name: Ubuntu-2004-sever1  
- Choose the location which is nearest you: London/UK  
- Select a password to use with your server.   
- Finally, click on button: [Create]  
...and, basically, that was it...I had Linode server 'up and running'...;    
you are given an IP address to SSH/Secure Shell into...  
root@xx.xx.xx.xx

### Runing the server...using Linode online Web Browser console window...   

In order to make the server run...  
- click on [Start server]    
Next, you can sign in to the online web browser based console, type...  

>> root@xx.xx.xx.xx    
>> password:    
>> root@~:  

...and, that's it. Your now running your very own web server 'live'...;    
-(though, it might take a minute or two getting it to fully provision/boot up...)-;    
and, can now run all sorts of Linux based commands such as: cal/ls/pwd/-etc.  

The first thing you should do is make sure your server is fully up to date with the very latest packages/security fixes/-etc.    
type:   

>> root@~: apt update && apt upgrade  

...then, wait for the updating/upgrading process to be done.    

The next thing you may want to do...which is entirely 'optional'...is change the hostname which says:   

>>root@~:  

...to become a name you prefer...type in...  

>>root@~: hostnamectl set-hostname yourPreferredHostName  

-(now you will need to logout out...by typing: exit...then, log back in, again...to see the prompt change to become...)    

>>yourPreferredHostName@~:    

### Runing the server remotely...using SSH/Secure Shell...  

What really surprised me, somewhat...  
-(though, I have used Windows 'Putty' software to remotely SSH into my Raspbian Pi, before)-    
...was realising I don't need to use Linode web browser interface to connect to my server;    
instead, I can use either: MS DOS Command Prompt/or, Powershell...; either way the instructions are the same...  

>> ssh root@xx.xx.xx.xx  
>> password:   
>> yourPreferredHostName@~:  

...then, it's possible to issue all of the same linux commands as is usual.

## Some basic LINUX commands...

List files/folders...  
>>root~: ls  

Show what is the current working folder directory path/(print working directory)...  
>>root~: pwd  

Create a new file...  
>>root~: touch fileName.fileNameExtension  

**NOTE**: Linux files don't need to have any 3 letter file name extension at all/(unlike Windows)     

Make a folder...  
>>root~: mkdir dirName  
  
Move to foder...
>>root~: cd dirName  

Move backwards...  
>>root~: cd ..  

Show the current calender date...
>>root~: cal  

Open a text editor...
>>root~: nano fileName.fileNameExtension  

**NOTE**: Either reading a good Linux tutorial book...  
-(especially, concerning what is the particular Linux distribution you wish to use)-;    
or, watching a few YouTube Linux command tutorials...would most certainly help out an awful lot     
before you try running any Linux based server.     







