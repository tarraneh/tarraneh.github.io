---
title: This is the third test post.
description: This is the third test post.
header: Test Post 3
---

<p>Hackintosh computers have been online for nearly a decade now (since the switch to Intel processors), allowing users to implement Mac OS X on non-Apple branded hardware, achieving performance close to or comparable to the latest Mac Pros for a fraction of the cost. In addition to installing Mac OS X on a custom-configured computer -- optimized for your needs -- dual-booting Windows on a Hackintosh allows for your computer to moonlight as a high-end gaming machine (depending on your hardware, of course).</p>

<p>But the road to a fully-functioning, stable Hackintosh is not for the meek of heart. It requires a willingness to hunker down and troubleshoot when things go wrong -- and things will go wrong. The following post is meant to help you navigate your way to Hackintosh glory.</p>

<strong>Choosing your components.</strong>

<p>The key thing to remember in building your Hackintosh is that the end goal requires installing software on non-native hardware, or hardware that simply wasn't designed with this particular function in mind. Rectifying this discord is best done by carefully selecting your parts based on whether or not they will be supportd by Mac OS X. Often, hardware which is technically supported might prove to be significantly more difficult than the alternative. Hackintosh aficionados will, for instance, generally suggest you avoid AMD CPUs and turn instead to the more agreeable 6th Generation Intel Core (Skylake) CPUs. That's not to say that you're out of luck with an AMD CPU, but you may have a harder time getting things going. In other words, your mileage may vary. </p>

<p>One of the absolute best resources out there for building your Hackintosh and choosing compatible components -- which I would be remiss not to mention -- is [TonyMacx86.com](http://www.tonymacx86.com/). There, you'll find not only extensive guides and lists specifiying Hackintosh compatible hardware, but also, a community of like-minded brave souls who will more likely than not have encountered each and every obstacle you will undoubtedly meet along the way.</p> 


<p>I won't go into the details of my build (feel free to e-mail me if you're interested), but I will mention that if you're planning on dual-booting, it is generally advised that you install each operating system on separate Solid State Drives (SSD). This is not only the easiest way to dual-boot, but it's also the cleanest and less prone to catastrophic failure-way. And of course, while you don't need to use SSDs in the place of Hard Disk Drives (HDDs), installing your OS on an SSD will decrease your bootup time substantially. Similarly, any apps that you install on the SSD will bootup much faster than they would otherwise. That being said, you can use SSDs to install your operating systems, and then opt for an HDD (or two or three) for general storage purposes.</p>

<strong>The Build</strong>

<p>This part of your journey is really no different than building a regular PC. There are plenty of [guides](https://www.youtube.com/watch?v=VIF43-0mDk4&feature=youtu.be) out there, but barring a few caveats, it's pretty straight forward. A couple of important (and commonly overlooked) things to keep in mind: <em>1. Don't forget the motherboard standoffs. </em> These ensure that there's extra space between the motherboard and the case, preventing short-circuits between the back of the board and the case. <em>2. If you're mounting the SSDs on the motherboard backplate, take a look at the SATA power cables that come with your power supply.</em> There's very little clearance at the input to the SSD, and depending on the angle of the connector, the connection may or may not be possible. I learned this the hard way, and was forced to remove my motherboard and peripherals and move the SSDs into the drive rack.</p>

                                

<strong>Installing OS X</strong>

<p>You've made it to the fun part. At this point in the game, you'll need to create a bootable USB containing an OS X El Capitan install which you can purchase from the Apple store or download as an update by using your pre-existing Mac computer. You'll also need to download the latest version of [Clover EFI Bootloader](https://sourceforge.net/projects/cloverefiboot/). There's a great guide for installing OS X using Clover [here](http://www.tonymacx86.com/threads/how-to-install-os-x-yosemite-using-clover.144426/). Once you have Clover installed, you need to make the appropriate changes to the config.plist file (allowing for audio injection, patching your motherboard to allow booting into OS X). There are also a number of kexts (kernel extensions; essentially drivers) that you'll need to include as part of the Clover configuration. These include:</p>

                                <ul>
                                <li>USBInjectAll.kext</li>
                                <li>AppleALC.kext</li>
                                <li>IntelMausiEthernet.kext</li>
                                <li>FakeSMC.kext</li>
                                </ul>

<p>These kexts provide basically the necessary 'bare-bones' of your build. Once your computer is up and running, you'll likely find that there are a number of other kexts you'll have to track down in order to get things like audio, iMessenger, and the like, fully-functioning. This is really where your Hackintosh will ask the most of you. Carefully editing your config.plist file and installing the appropriate kexts hold the key to unlocking your Hackintosh. </p>



<p>I've obviously glossed over many of the subtleties which turn out to be rather important when it comes to your build (see config.plist edits!), but there are truly plenty of guides and resources out there to get you going (among others, I also recommend [r/hackintosh](http://reddit.com/r/hackintosh) on reddit. At the end of the day, if you're looking to spend a minimal amount of time troubleshooting your computer, and indeed, if you are relying on your computer for sensitive work related tasks and processes, a Hackintosh may not be the best idea. It's important to keep in mind that Hackintosh computers are ultimately a series of hacks developed to run Apple software on hardware that was not designed to do so. There are bound to be issues along the way.  Per Apple's EULA, Apple will not provide support for your Hackintosh, so you are largely on your own. That being said, if you're committed to the pursuit, Hackintosh computers really do allow for a cheaper and more customizable alternative to traditional Mac computers. </p>