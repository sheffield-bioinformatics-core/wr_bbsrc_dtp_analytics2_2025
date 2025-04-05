# Analytics 2: Introduction to the command-line for Bioinformatics

## Course Content


This course offers an introduction to working with Linux. We will describe the Linux environment so that participants can start to utilize command-line tools and feel comfortable using a text-based way of interacting with a computer. We will also introduce the "Git" version control system, which is a very powerful tool to help us secure our code from data loss. We’ll cover the terminology, how you can use it for your own projects and then how you can use it to make collaboration on a project easy.

## Pre-requisites

No prior programming experience is required. Computers will be provided. You can bring your own laptop to the workshop if you wish but it will need a working wi-fi connection and you will have to let the tutor know in advance so a temporary York password can be created for you.

## Learning Outcomes

After this course you should be able to:

- Connect to a Unix / Linux system
- Navigate around a file system by issuing commands; rather than using a Desktop environment
- Move and copy files and directories within the Linux system
- Work with text files
- Run programs from the command-line
- Write short scripts to document an analysis
- Use version control (git) to track and document changes to a file

## Schedule (Provisional)

- 09:30 - 10:00 [Introduction and Course Setup](https://sbc.shef.ac.uk/wr_bbsrc_dtp_analytics2_2025/part0.nb.html)
- 10:00 - 11:00
    + [Introduction to the command line](https://datacarpentry.org/shell-genomics/01-introduction/)
    + [Navigating files and directories](https://datacarpentry.github.io/shell-genomics/02-the-filesystem.html)
- 11:00 - 11:30 BREAK
- 11:30 - 12:15
    + [Working wih files and directories](https://datacarpentry.github.io/shell-genomics/03-working-with-files.html)
    + [Redirection](https://datacarpentry.github.io/shell-genomics/04-redirection.html)
    + [Writing scripts and working with data](https://datacarpentry.github.io/shell-genomics/05-writing-scripts.html)
- 12:15 - 13:00 LUNCH
- 13:00 - 14:30 [Obtaining Sequencing data and quality assessment]()

## Amazon details (for setup)

- ami-0f9124f7452cdb2a6
- User data
```
#!/bin/bash

sudo apt-get update
sudo apt-get install -y docker.io
sudo service docker start
sudo usermod -aG docker $username
sudo docker pull sheffieldbioinformatics/unix-training
docker run -v --rm -d -p 5901:5901 -p 6901:6901 --privileged sheffieldbioinformatics/unix-training
```

- Default security group
- white_rose_analytics2 RSA key
