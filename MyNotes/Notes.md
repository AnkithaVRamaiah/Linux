# What is Internet?

"When we search for something on Google or open a website like **google.com**, we use the **internet**. Internet Service Providers (**ISPs**) like Airtel and Jio help us connect to the internet. However, computers do not understand names like 'google.com'; they only recognize numbers called **IP addresses**.  

So, when we type **google.com** in a browser, our computer first contacts a system called **DNS (Domain Name System)** to find the IP address of google.com. The **DNS searches for the correct IP address** and sends it back to our computer. Once our computer receives the IP address, it connects to **Google’s server**, and the website loads in our browser."  

--- 

# What is server?

"A **server** is a computer that stores websites, apps, and files. It responds to requests from other computers, which are called **clients**.  

For example, when I type **www.youtube.com** in my browser, my browser sends a **request** to the YouTube server. This server stores YouTube’s web pages. When the server receives my request, it finds the webpage and sends it back to my computer so I can see it.  

### How does a server work?  
1. My computer (the client) sends a request to the server.  
2. The server finds the data I asked for.  
3. Instead of sending all the data at once, it is **broken into smaller pieces** called **packets**.  
4. These packets travel through the internet and reach my device.  
5. My computer **reassembles the packets** to display the webpage correctly.  

This process happens very quickly, so we don’t notice the delay. This is how a server works!"  

---

# **Web Server and Application Server:**

There are two main types of servers: **web servers** and **application servers**.

1. **Web Server:**
   - A **web server** is responsible for delivering **static content** over the internet. **Static content** means the files that don’t change often, such as **HTML pages, images, videos, and CSS files**.  
   - For example, when you type **google.com** in your browser, the **web server** sends the Google homepage, which is a static **HTML file**. This page is **static**, meaning it stays the same unless the website owner updates it on the server.

2. **Application Server:**
   - An **application server** handles **dynamic content**, which means the content changes based on user interactions.  
   - For example, when you log into **Instagram**, the application server asks for your **username and password**. It checks the database to verify your details. Once verified, it generates a **customized homepage** for you, displaying your personalized feed.
   - If a different user logs in, the application server will generate a **different feed** based on their data. This is **dynamic content**, which means it changes based on the user's request or activity.

---

# **What is Linux?**

**Linux** is an **operating system**. An operating system is software that helps you interact with your computer. It is like **Windows** or **macOS**. 

Think of it like a bridge between your **computer hardware** (like the screen, keyboard, CPU, etc.) and the software (like apps or programs you use on your computer). It makes sure everything works together smoothly.

### **Why Linux?**

1. **Security**:  
   Linux is **more secure** than Windows. It's less likely to get viruses or other attacks because of how it is built.

2. **Customizable**:  
   You can change almost anything on Linux to make it work the way you want. It’s great for people who like to have control over their system, like developers.

3. **Free and Open Source**:  
   Linux is **free to use**. You don’t need to pay for it. Plus, it’s **open source**, meaning anyone can look at the code and even improve it if they want.

4. **Updates**:  
   Linux gets **regular updates** to make it work better and fix any issues. These updates happen less often compared to Windows and are easy to install.

5. **User-Friendliness**:  
   While Windows is easier for regular people, Linux is **better for those who need control** or care about **security**. It is a bit more technical but powerful.

6. **Multiple Users**:  
   **Many people** can use Linux on the same computer at the same time without any problems. This is useful for businesses or servers.

7. **Software Alternatives**:  
   Linux doesn’t run many **Windows programs**. But, it has **free alternatives** for most of them. For example, you can use **LibreOffice** instead of Microsoft Office.

8. **Great for Developers**:  
   Linux is popular with **developers** because it has lots of tools for coding and building web applications. It is also widely used for **web servers**.

---

# what is kernel?

The **kernel** is the core part of an operating system that acts as a bridge between the computer’s hardware and the software applications you use. It is responsible for managing system resources like the CPU, memory, and input/output devices, ensuring that everything works efficiently. When you run a program, the kernel allocates the necessary resources to it and manages communication with hardware. 

For example, if you open a text editor, the kernel decides how much memory the program needs and makes sure it can access the keyboard and display. The kernel also handles multitasking, allowing multiple programs to run simultaneously without interfering with each other. When you interact with the computer through a shell or a graphical interface, the kernel processes those requests in the background, handling everything from reading files to connecting to the internet.

In short, the kernel manages the system's hardware and ensures that all software can run smoothly by allocating resources and handling communication between hardware and software.

---

# What is BootLoader?

When you turn on your computer, the first thing that happens is the **BIOS/UEFI** performs a test (called **POST**) to check if all hardware is working. Then, it looks for a device (like a hard drive or USB) that contains the operating system. Once it finds one, the BIOS/UEFI loads a small program called the **bootloader** from the device into memory. For example, if you are using Linux, the bootloader is called **GRUB**. This bootloader's job is to load the **kernel**, the core part of the operating system, into memory. Once the kernel is loaded, it starts to set up the computer by initializing hardware, loading necessary drivers, and starting basic system services. After that, the system is ready, and you can interact with it using the **shell** (such as a terminal on Linux). In the shell, you can type commands like `ls` to list files. The shell sends these commands to the kernel, which processes them and shows the results back in the terminal.

---

# What is shell?

The **shell** is a program that provides a way for users to interact with the operating system. It acts as an interface between the user and the kernel. When you type a command in the shell, the shell sends that command to the **kernel** to execute. The kernel processes the command and returns the result, which the shell then displays to you. For example, if you type the command `ls` in a Linux terminal, the shell sends the command to the kernel to list the files in a directory. The kernel fetches that information and sends it back to the shell, which shows you the list of files on your screen. The shell can be either a **command-line interface (CLI)**, where you type text commands, or a **graphical user interface (GUI)**, where you click on icons and buttons. Shells are an essential tool for developers and system administrators because they allow efficient control over the system using simple text-based commands.

---

