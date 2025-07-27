# The-Art-of-Networking

Networking is the process of establishing communication links between devices. These physical or logical connections form what is known as a network topology. Let's try to dicuss the basics one step at the time.

## 📚 Contents
- [Building-a-Network-of-2-PCs](#building-a-network-of-2-pcs)
- [Introducing-a-Hub](#introducing-a-hub)
- [Disclaimer](#disclaimer)

## Building a Network of 2 PCs

Let's first build a simple network containing two devices: PC1 and Laptop1. We need to make a communication link between the two by just building the network illustration below (I use Packet Tracer to build this figure):

![image](Images/01-Your-First-Topology/01-Two-PCs-topology.png)

To build this in Packet Tracer, place 1 PC and 1 Laptop. Connect them with copper cross-over cable (denoted by a dashed line). Configure your PC and laptop IP address with value of 192.168.1.1/24 and 192.168.1.2/24 respectively by opening the __Config__ tab when you click the PC icon like the image below.

![image](Images/01-Your-First-Topology/02-Configure-IP-Address-to-PC.png)

Now, we use the __ping__ command to check if PC1 can connect to Laptop1 and vice-versa. In PC1, ping the 192.168.1.2 of Laptop1 and do the reverse. You should notice the following output ensuring your network topology works.

![image](Images/01-Your-First-Topology/03-Ping-Each-IP.png)

Nice! You have created a working network. What if we would like to introduce another PC in the topology. Just simply connect another cable, right? But if you'll look at the __Physical__ tab of the PC1, there is only one FastEthernet port to be used like the image below. This can be fixed by adding Ethernet ports or external adapters to extend the number of current ports we are using (however, Packet Tracer does not allow us to do this).

![image](Images/01-Your-First-Topology/04-Physical-Tab-of-PC.png)

Let's say, we managed to extend the number of Ethernet ports of each PC. And imagine we assumed we are able to connect 3 PCs. 5 PCs. 10 PCs. The cable management could be very messy! Plus Ethernet ports of PCs are limited.

![image](Images/01-Your-First-Topology/05-Messy-Topology.png)

That's why someone invented a hub!

---

## Introducing a Hub

Let's focus on the fact that our ports are limited. We cannot plug more PCs to a PC by just directly plugging an Ethernet cable to it. This is the major role of the __HUB__ device. It is often referred as port extenders or even repeaters (to repeat the packets coming from a port to another port).

In networking, a hub is a device that links multiple computers and devices together. Hubs can also be referred to as repeaters or concentrators, and they serve as the center of a local area network (LAN). In a hub, each connected device is on the same subnet and receives all data sent to the hub. 

Let's say we have three PCs to connect at the same time with different IPs designated to them. By connecting them with a hub, every single PC can ping each other.

TO-DO: Provide snapshot of three PCs connected via hub.

It's cool, right? If your hub contains 24 port, then you can connect up to 24 PCs. If it contains 48 port, then you can connect up to 48 PCs. Very powerful, right?

TO-DO: Provide snapshot of 24-port Hub with 24 PCs connected to each port.

Let's try the powerful tool of Packet Tracer, the simulator. This tool allows to simulate the environment to run in slow-motion for us to observe the life of a packet. Just simply build the three-PC topology with hub and enter simulate.

TO-DO: Provide snapshot of three PC topology with hub with simulate in the tab.

With the two PCs connected with the hub, ping the third PC at the same time. Observe what will happen to the packets.


Did the packets reach the third PC? No, they just burned based on the Packet Tracer simulator. What happened is those packets got collided as they both transmitted in the same
wire or cable. Thus, ping from PC1 and PC2 collided with each other making the packets corrupted.

So, we don't use hub?

---

## Introducing a Switch


---

## Introducing a Router

---

## Disclaimer

I'm inspired with The-Art-of-Command-Line repo. So, why not create one for Networking?

There are many things to learn in networking. There is no need to learn everything at the same time!
