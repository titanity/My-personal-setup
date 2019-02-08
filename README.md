sudo apt-get update && sudo apt-get upgrade && sudo apt-get dist-upgrade -y


sudo apt-get install gkrellm gkrellm-cpufreq synaptic gparted tightvncserver uuid-runtime mtools dosfstools 
nemo python xorg leafpad geany parted gnome-disk-utility yum wget qemu digikam limba limba-devtools libxcb-util0 device-tree-compiler linaro-image-tools perl build-essential libc6-armel-cross libncurses5-dev git-core git-gui gitk git libssl-dev xapian-tools cryptsetup dwww menu deborphan apt-xapian-index tasksel software-properties-gtk pmount libncurses5-dev software-properties-common binfmt-support python-dbus python-debian python-parted python-apt python-yaml libssl-dev uget git-daemon-run git-cvs git-mediawiki git-svn curl vlc fakeroot libssl-dev lzop debhelper gccgo gnome-system-tools gnome-control-center gnome-disk-utility gnome-keyring gnome-menus gnome-software

install a DEB package
dpkg -i pkg.deb – (Debian / Ubuntu / Linux Mint)


sudo add-apt-repository ppa:linaro-maintainers/tools
sudo apt-get update
sudo apt-get install linaro-image-tools

Zram!

Download the script and copy to /usr/bin/ folder
sudo wget -O /usr/bin/zram.sh https://raw.githubusercontent.com/novaspirit/rpi_zram/master/zram.sh
make file executable
sudo chmod +x /usr/bin/zram.sh
edit /etc/rc.local file to run script on boot
sudo nano /etc/rc.local
add line before exit 0
/usr/bin/zram.sh &

Katoolin!

apt-get install git
git clone https://github.com/LionSec/katoolin.git && cp katoolin/katoolin.py /usr/bin/katoolin
chmod +x  /usr/bin/katoolin
sudo katoolin

tinkerboard overclock

https://tinkerboarding.co.uk/forum/thread-654-post-3805.html#pid3805

Lazy script

git clone https://github.com/arismelachroinos/lscript.git

Airgeddon

git clone https://github.com/v1s1t0r1sh3r3/airgeddon.git


System Info
date – Show the current date and time
cal – Show this month's calendar
uptime – Show current uptime
w – Display who is online
whoami – Who you are logged in as
finger user – Display information about user
uname -a – Show kernel information
cat /proc/cpuinfo – CPU information
cat /proc/meminfo – Memory information
df -h – Show disk usage
du – Show directory space usage
free – Show memory and swap usage

# Disable the ACT LED.
dtparam=act_led_trigger=none
dtparam=act_led_activelow=off

# Disable the PWR LED.
dtparam=pwr_led_trigger=none
dtparam=pwr_led_activelow=off

Keyboard Shortcuts
Enter – Run the command
Up Arrow – Show the previous command
Ctrl + R – Allows you to type a part of the command you're looking for and finds it

Ctrl + Z – Stops the current command, resume with fg in the foreground or bg in the background
Ctrl + C – Halts the current command, cancel the current operation and/or start with a fresh new line
Ctrl + L – Clear the screen

command | less – Allows the scrolling of the bash command window using Shift + Up Arrow and Shift + Down Arrow
!! – Repeats the last command
command  !$ – Repeats the last argument of the previous command
Esc + . (a period) – Insert the last argument of the previous command on the fly, which enables you to edit it before executing the command

Ctrl + A – Return to the start of the command you're typing
Ctrl + E – Go to the end of the command you're typing
Ctrl + U – Cut everything before the cursor to a special clipboard, erases the whole line
Ctrl + K – Cut everything after the cursor to a special clipboard
Ctrl + Y – Paste from the special clipboard that Ctrl + U and Ctrl + K save their data to
Ctrl + T – Swap the two characters before the cursor (you can actually use this to transport a character from the left to the right, try it!)
Ctrl + W – Delete the word / argument left of the cursor in the current line

Ctrl + D – Log out of current session, similar to exit

Learn the Commands
apropos subject – List manual pages for subject
man -k keyword – Display man pages containing keyword
man command – Show the manual for command
man -t man | ps2pdf - > man.pdf  – Make a pdf of a manual page
which command – Show full path name of command
time command – See how long a command takes

whereis app – Show possible locations of app
which app – Show which app will be run by default; it shows the full path

Searching
grep pattern files – Search for pattern in files
grep -r pattern dir – Search recursively for pattern in dir
command | grep pattern – Search for pattern in the output of command
locate file – Find all instances of file
find / -name filename – Starting with the root directory, look for the file called filename
find / -name ”*filename*” – Starting with the root directory, look for the file containing the string filename
locate filename – Find a file called filename using the locate command; this assumes you have already used the command updatedb (see next)
updatedb – Create or update the database of files on all file systems attached to the Linux root directory
which filename – Show the subdirectory containing the executable file  called filename
grep TextStringToFind /dir – Starting with the directory called dir, look for and list all files containing TextStringToFind

File Permissions
chmod octal file – Change the permissions of file to octal, which can be found separately for user, group, and world by adding: 4 – read (r), 2 – write (w), 1 – execute (x)
Examples:
chmod 777 – read, write, execute for all
chmod 755 – rwx for owner, rx for group and world
For more options, see man chmod.

File Commands
ls – Directory listing
ls -l – List files in current directory using long format
ls -laC – List all files in current directory in long format and display in columns
ls -F – List files in current directory and indicate the file type
ls -al – Formatted listing with hidden files

cd dir – Change directory to dir
cd – Change to home
mkdir dir – Create a directory dir
pwd – Show current directory

rm name – Remove a file or directory called name
rm -r dir – Delete directory dir
rm -f file – Force remove file
rm -rf dir – Force remove an entire directory dir and all it’s included files and subdirectories (use with extreme caution)

cp file1 file2 – Copy file1 to file2
cp -r dir1 dir2 – Copy dir1 to dir2; create dir2 if it doesn't exist
cp file /home/dirname – Copy the filename called file to the /home/dirname directory

mv file /home/dirname – Move the file called filename to the /home/dirname directory
mv file1 file2 – Rename or move file1 to file2; if file2 is an existing directory, moves file1 into directory file2

ln -s file link – Create symbolic link link to file
touch file – Create or update file
cat > file – Places standard input into file
cat file – Display the file called file

more file – Display the file called file one page at a time, proceed to next page using the spacebar
head file – Output the first 10 lines of file
head -20 file – Display the first 20 lines of the file called file
tail file – Output the last 10 lines of file
tail -20 file – Display the last 20 lines of the file called file
tail -f file – Output the contents of file as it grows, starting with the last 10 lines

Compression
tar cf file.tar files – Create a tar named file.tar containing files
tar xf file.tar – Extract the files from file.tar

tar czf file.tar.gz files – Create a tar with Gzip compression
tar xzf file.tar.gz – Extract a tar using Gzip

tar cjf file.tar.bz2 – Create a tar with Bzip2 compression
tar xjf file.tar.bz2 – Extract a tar using Bzip2

gzip file – Compresses file and renames it to file.gz
gzip -d file.gz – Decompresses file.gz back to file

Network
ifconfig – List IP addresses for all devices on the local machine
iwconfig – Used to set the parameters of the network interface which are specific to the wireless operation (for example: the frequency)
iwlist – used to display some additional information from a wireless network interface that is not displayed by iwconfig
ping host – Ping host and output results
whois domain – Get whois information for domain
dig domain – Get DNS information for domain
dig -x host – Reverse lookup host
wget file – Download file
wget -c file – Continue a stopped download

SSH
ssh user@host – Connect to host as user
ssh -p port user@host – Connect to host on port port as user
ssh-copy-id user@host – Add your key to host for user to enable a keyed or passwordless login

User Administration
adduser accountname – Create a new user call accountname
passwd accountname – Give accountname a new password
su – Log in as superuser from current login
exit – Stop being superuser and revert to normal user

Process Management
ps – Display your currently active processes
top – Display all running processes
kill pid – Kill process id pid
killall proc – Kill all processes named proc (use with extreme caution)
bg – Lists stopped or background jobs; resume a stopped job in the background
fg – Brings the most recent job to foreground
fg n – Brings job n to the foreground

Installation from source
./configure
make
make install
dpkg -i pkg.deb – install a DEB package (Debian / Ubuntu / Linux Mint)
rpm -Uvh pkg.rpm – install a RPM package (Red Hat / Fedora)

Stopping & Starting
shutdown -h now – Shutdown the system now and do not reboot
halt – Stop all processes - same as above
shutdown -r 5 – Shutdown the system in 5 minutes and reboot
shutdown -r now – Shutdown the system now and reboot
reboot – Stop all processes and then reboot - same as above
startx – Start the X system

How do I determine the current MHz?
Run this in a terminal: 

   sudo cat /sys/devices/system/cpu/cpu0/cpufreq/cpuinfo_max_freq

It will display the maximum CPU frequence

How can stress test or benchmark?

This will install sysbench: sudo apt-get install sysbench

This command will Run a prime number benchmark to 20000: sysbench --test=cpu --cpu-max-prime=20000 --num-threads=4 run
Overclock profiles

1.45Ghz CPU 500Mhz gpu Overclock profile

arm_freq=1500
gpu_freq=500
core_freq=500
sdram_freq=500
sdram_schmoo=0x02000020
over_voltage=2
sdram_over_voltage=2

1.5Ghz CPU NO gpu Overclock profile

arm_freq=1500
over_voltage=6


1.5Ghz CPU 500Mhz gpu Overclock profile

arm_freq=1500
gpu_freq=500
core_freq=500
sdram_freq=500
sdram_schmoo=0x02000020
over_voltage=6
sdram_over_voltage=2



1.57Ghz CPU 500Mhz gpu Overclock profile

arm_freq=1575
gpu_freq=500
core_freq=500
sdram_freq=500
sdram_schmoo=0x02000020
over_voltage=6
sdram_over_voltage=2



1.6Ghz CPU 500Mhz gpu Overclock profile

arm_freq=1600
gpu_freq=500
core_freq=500
sdram_freq=500
sdram_schmoo=0x02000020
over_voltage=6
sdram_over_voltage=2
