# Install Kivy on Ubuntu  
  
In ubuntu Kivy is built from the packages `python-kivy`, `python-kivy-examples`.  
So install these packages by run   
    
```
sudo apt-get install python-kivy python-kivy-examples debhelper python python-all-dev cython libgl1-mesa-dev libgles2-mesa-dev
```    
   
    


# Buildozer
Buildozer is a tool that aim to package mobiles application easily. It automates the entire build process, download the prerequisites like python-for-android, Android SDK, NDK, etc.  

# How to install ?
prerequisite :- You must have to use Mac os or linux    
  
First of all download buildozer    
```
git clone https://github.com/kivy/buildozer.git
```
  
Install Python    
```
sudo apt install python3.6
```    
    
Install Setup tools    
```
sudo apt-get install python3-setuptools
```    
    
Go to buildozer directory   
```
cd buildozer
```    
    
Install `setup.py` by this command    
```
sudo python3 setup.py install
```    
 
 
Install some packages

```
sudo apt install -y git zip unzip openjdk-8-jdk python3-pip autoconf libtool pkg-config zlib1g-dev libncurses5-dev libncursesw5-dev libtinfo5 cmake libffi-dev libssl-dev
```  
  
```
pip3 install --user --upgrade Cython==0.29.19 virtualenv
```  
  
```
export PATH=$PATH:~/.local/bin/
```

Install Cython

`sudo apt-get install cython`

# Convert Your App to APK
  
Move to the directory where your kivy project present

Initialize Buildozer

`buildozer init`

Write `nano buildozer.spec`




Do some changes 

```python
#(str) Title of your application    
title = My Application (name of your applications)

#(str) Package name    
package.name = myapp (package name)    

```
And also change this

```python
#(str) Android logcat filters to use    
#android.logcat_filters = *:S python:D    

```
to 

```python
#(str) Android logcat filters to use    
android.logcat_filters = *:S python:D    

```

run the last command     
`
buildozer android debug deploy run    

`
