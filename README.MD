# Using Vagrant for the TensorFlow and deep learning code lab

The code lab for [TensorFlow and deep learning, without a PhD](https://codelabs.developers.google.com/codelabs/cloud-tensorflow-mnist/#0)
requires Python 3, TensorFlow and Matplotlib all of the correct versions. It also requires Git to download the tutorial 
materials from GitHub.  
Since folks may already be using other versions of Python, etc. it made sense to create a VM with all necessary items installed.  
For anyone who wants to do the code lab without affecting their own local environment, I have provided a Vagrantfile.  
The Vagrantfile performs the necessary steps to install and configure a VirtualBox VM with Git, Python, Tensorflow, and Matplotlib.
To learn more about Vagrant go here: [Getting Started](https://www.vagrantup.com/docs/getting-started/)

Note: The VM created using this file will consume 4GB of RAM on the laptop or PC you run it on.

## Prerequisites to using the Vagrantfile on your laptop/PC

1. install the latest [Vagrant](https://www.vagrantup.com/downloads.html) software
2. install the latest [VirtualBox](https://www.virtualbox.org/) VM software
3. install [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) (if you don't have it already)

## Using the Vagrantfile

1. In the terminal window type in the git clone command for this repository:
       ```
       git clone https://github.com/AthenaMarine/tensorflow_codelab.git
       ```
   This will download the Vagrantfile and this README file into the directory you choose. 
   
2. Change, (cd command) to the directory where the Vagrant file exists. 

3. type in the command to start vagrant:
       ```
       vagrant up
       ```
   This will take 15-20 minutes as it is setting up everything.
   
4. When vagrant has finished, you will see a VirtualBox instance running an Ubuntu desktop display.
   This is the environment you will work in for the code lab   
   
5. To make the Ubuntu display larger, right-click on the desktop and from the menu browse to:
       Applications->Settings->Display
   Change the resolution to something larger, (1920 x 1600 for example,) and press the Apply button.

## Check that Everything Works

1. Run a terminal window from the TensorFlow project directory. Right-click on the desktop 
and from the menu browse to:
       Open Terminal Here
    Then change to the directory:
       ```
       cd /home/ubuntu/tensorflow-mnist-tutorial
       ```
    Then run the command:
       ```
       python3 mnist_1.0_softmax.py
       ```
       
    You should see a new window appear in the UI showing 6 different charts, and data in the terminal window. 
    ![alt text](https://github.com/AthenaMarine/tensorflow_codelab/blob/master/TensorFlowVM.png "Working TF Environment")
    
2. Now you can follow along in the tutorial.

3. If you will not be working on the tutorial right away, you can suspend the VM, and then bring it back up later with the following commands:

       ```
       vagrant suspend
       ```
       ```
       vagrant resume
       ```

## Final Clean-Up

1. When you are completely finished with the tutorial, you can destroy the VM with the command:

       ```
       vagrant destroy
       ```

