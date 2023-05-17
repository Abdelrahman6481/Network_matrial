# Network II 

## ip protocol

The Internet Protocol (`IP`) is a network-layer protocol that facilitates
the routing of data packets across a network.   
It operates as a connectionless protocol, meaning it doesn't establish a 
dedicated connection between source and destination devices prior to transmitting
data.

IP addresses are allocated to devices on a network to uniquely identify them and
enable communication with other devices, either on the same network
or different networks. An IP address comprises four sets of numbers, 
ranging from `0 to 255`, separated by periods. 
For instance, `192.168.1.1` is a commonly used IP address for routers.

When a device intends to send data to another device on a network
, it examines the destination IP address to determine if it belongs to 
the same network or a different one. If the destination is within the same network
, the device transmits the data directly to the recipient using its `MAC address` .
On the other hand, if the destination is on a separate network, 
the data is sent to the `default gateway`, which serves as the connection 
between the local network and other networks. The gateway then forwards 
the data to the appropriate network until it reaches the intended destination.

The prevalent version of IP in use today is `IPv4`, which employs `32-bit` addresses
and can support around `4 billion unique addresses`. However, due to
the internet's rapid expansion, the availability of IPv4 addresses is
nearly exhausted. Consequently, a newer version of IP called `IPv6` has 
been developed. `IPv6 utilizes 128-bit addresses`, 
enabling approximately `3.4×10^38 unique addresses`.

IP serves as a fundamental protocol for the internet and i
s utilized by numerous other protocols such as `TCP` and `UDP`. 
These protocols rely on IP to ensure efficient and reliable transmission of data
packets across networks.



## Non-routable Ips:

`Non-routable IP addresses` are IP addresses that are reserved for use in `private networks` and 
cannot be used to access devices or services on the internet.
These IP addresses are not unique and are used in many private networks around the world, making it possible 
for devices on different private networks to use the same IP address ranges without conflict.

#### The most commonly used non-routable IP address ranges are:
 > 1. 10.0.0.0 – 10.255.255.255 (10.0.0.0/8)
 > 2. 172.16.0.0 – 172.31.255.255 (172.16.0.0/12)
 > 3. 192.168.0.0 – 192.168.255.255 (192.168.0.0/16)

These IP address ranges are reserved by the Internet Assigned Numbers Authority (`IANA`) 
for use in private networks and are not routed on the internet. This means that devices with 
non-routable IP addresses can communicate with each other within the same private network,
but they cannot be accessed directly from the internet.
Non-routable IP addresses are commonly used in home and small office networks,
where they provide a way for devices to communicate with each other without requiring a unique public IP address
for each device. Instead, a single public IP address is assigned to the router, 
which then assigns non-routable IP addresses to each device on the private network.
This is known as network address translation (`NAT`) and is used to conserve public IP addresses and enhance 
network security by hiding the private network from the internet.


## Device cascading:

`Device cascading` is a network topology where multiple devices are connected in a series,
with data passing through each device to reach its destination. In device cascading,
one device is connected to another device, which in turn is connected to another device, 
and so on. This can be achieved using different types of network devices, such as `switches`, `hubs`, and `routers`.
The main advantage of device cascading is that it allows for the expansion of a network beyond the number of ports
available on a single device. `For example`, 
>if a switch has a limited number of ports,
additional switches can be cascaded to provide more ports for connecting devices.
> 
However, device cascading can also have some disadvantages. One potential issue is the 
introduction of latency or network congestion, as data has to pass through multiple devices
before reaching its destination. Additionally, cascaded devices can be more difficult 
to manage and troubleshoot, as there are multiple points of potential failure and configuration
can become more complex.
Overall, device cascading can be a useful technique for expanding a network beyond 
the capacity of a single device, but it should be implemented with care to avoid performance and management
issues.


## Network ports:

A `network port` is an endpoint on a computer or network device that identifies a specific process or service.
Ports are identified by `port` numbers ranging from` 0 to 65535`.
There are two types of ports: `TCP and UDP`. `TCP` is a connection-oriented protocol that establishes a connection
before data transmission, while `UDP` is a connectionless protocol that doesn't establish a 
connection and doesn't guarantee data delivery.

Applications and services use specific port numbers to communicate. `For example`,
>web servers use port 80 for HTTP and port 443 for HTTPS, 
while email servers use port 25 for SMTP and port 110 for POP3.

Network administrators can control access to ports through firewalls and security devices,
allowing or blocking traffic to specific ports. This helps protect against unauthorized access and network
attacks.


## Modem:

A `modem` is a device that converts digital signals to analog signals and vice versa, 
allowing digital devices to communicate over analog channels like telephone lines or cable TV lines.
It has a data port to connect to digital devices and a communication port for analog channels.
The modem converts digital signals to analog for transmission and analog signals to digital for the
digital device.

Modems operate at different speeds, measured in bits per second (`bps`), 
determining the data transmission rate between the digital device and analog channel.
Modem speeds have evolved from slower speeds in the past to modern broadband modems with gigabit speeds.

Modems serve various purposes, including internet access, `VoIP`, and `M2M` communication.
For instance, a modem connected to a telephone line enables dial-up internet access, 
while a cable modem connected to a cable TV line offers broadband internet access.3


## Switch VS router:

A `switch and a router` are both network devices that are used to connect devices on a computer network,
but they perform different functions.
A `switch` is a network device that is used to connect devices on a local area network (`LAN`). 
It works at the data link layer (`Layer 2`) of the OSI model and is responsible for forwarding
data packets between devices on the same network. A switch reads the destination `MAC address` of a packet 
and forwards it to the correct device on the `same network`. Switches are designed to work with Ethernet 
networks and are often used in small to medium-sized networks.
A `router`, on the other hand,
is a network device that is used to connect devices on `different networks`, including the internet. 
It works at the network layer (`Layer 3`) of the OSI model and is responsible for routing data packets
between networks. A router reads the destination `IP address` of a packet and forwards it to the correct network.
Routers are more complex than switches and are designed to work with different network 
protocols, including `IP`, `TCP`, and `UDP`. They are often used in larger networks that require 
connectivity to multiple networks, including the internet.
>In summary, switches are used to connect devices on the same network, while routers are used to connect devices
on different networks. Switches operate at the data link layer, while routers operate at the network layer.
>

## Router VS bridge:

`Routers and bridges` are both network devices used to connect multiple devices together, 
but they serve different purposes and operate at different levels of the network.
A router is a network device that connects two or more networks together and routes data packets between them.
Routers operate at the network layer (`Layer 3`) of the OSI model, and they use routing tables to 
determine the best path for data packets to travel from one network to another. Routers can also perform 
network address translation (`NAT`) to allow devices with private IP addresses to connect to the Internet.

A `bridge`, on the other hand, is a network device used to connect two or more devices together 
within the `same network`. Bridges operate at the data link layer (`Layer 2`) of the OSI model,
and they use `MAC addresses` to direct data packets between devices. Bridges are often used to 
extend the reach of a network by connecting multiple LAN segments together.
One key difference between routers and bridges is that routers are able to connect multiple networks together
, while bridges only connect devices within the same network. Routers are also able to provide more 
advanced network functions, such as security features and the ability to prioritize certain types of traffic.
However, bridges are typically simpler and less expensive than routers, making them a good option 
for smaller networks or those with limited needs.

>In summary, routers are used to connect multiple networks together, while bridges are used to connect devices 
within the same network. Routers operate at the network layer (Layer 3) of the OSI model,
while bridges operate at the data link layer (Layer 2).
>


## Proxy server:

A `proxy server `is a computer or software application that acts as an intermediary 
between a client device (`such as a web browser`) and a server. When a client requests a resource from a server,
the request is first sent to the proxy server, which then forwards the request to the server on behalf 
of the client. The server then sends the response back to the proxy server, which in turn sends the 
response to the client.

#### There are several reasons why a proxy server may be used, including:
> - Privacy and security: A proxy server can be used to hide the IP address of the client, making it more difficult for third parties to track the client's online activity. It can also be used to filter and block certain types of content, such as malicious websites or inappropriate content.
> - Content caching: A proxy server can cache frequently accessed web pages, images, or other resources, which can improve performance and reduce bandwidth usage.
> - Load balancing: A proxy server can distribute requests across multiple servers, which can help to balance the load on each server and improve overall performance.
> - Access control: A proxy server can be used to restrict access to certain websites or resources, either for security reasons or to enforce corporate policies.
>
Proxy servers can be deployed on a network or accessed through a web browser configuration.
There are also many publicly available proxy servers that can be used for free or for a fee, 
but caution should be used when using public proxy servers as they can potentially expose sensitive 
data or introduce security risks.


## DHCP:

`DHCP`, or Dynamic Host Configuration Protocol, is a network protocol used to automatically 
assign IP addresses and other network configuration settings to devices on a network.
When a device joins a network, it sends a broadcast message requesting an IP address. 
A DHCP server on the network receives the request and assigns an available IP address to the device.
The DHCP server can also provide additional network configuration settings, such as the subnet mask, 
default gateway, and DNS server addresses, to the device.
Using DHCP eliminates the need for manual configuration of IP addresses on every device in a network,
which can be time-consuming and error-prone. DHCP also allows for more efficient use of IP addresses,
as IP addresses are assigned only when devices are connected to the network and released when devices 
are disconnected.
DHCP operates on a `client-server model`, with one or more DHCP servers on the network responsible for
assigning IP addresses and other network configuration settings to clients that request them. 
DHCP servers can be configured to provide different IP address ranges and network settings to different 
clients based on their specific requirements.
DHCP can be used in both wired and wireless networks and is widely used in home and business networks.
It is also used in larger enterprise networks where centralized management of IP addresses and network 
configuration settings is necessary.


## Access point:

An `access point` is a networking device that allows wireless devices to connect to a wired network.
It acts as a bridge between a wired network and wireless devices such as `laptops`, `smartphones`, and `tablets`.
Access points are commonly used in `Wi-Fi networks` to provide wireless connectivity to devices that are 
not connected directly to the wired network, such as mobile devices, smart home devices, 
and Internet of Things (`IoT`) devices.
An access point typically connects to a wired network through an Ethernet cable and broadcasts a wireless
signal using Wi-Fi technology. The wireless devices within range of the access point can then 
connect to the network and access resources such as the Internet or shared files and printers.
Access points can be standalone devices or integrated into other networking equipment such as routers 
or switches. Some access points also have advanced features such as multiple SSIDs (`Service Set Identifiers`), 
which allow different wireless networks to be set up with different security and access policies.
Access points can be used in a variety of settings, including `homes`, `offices`, `schools`, `airports`, 
and `public spaces` such as c`offee shops` and `libraries`. They are an important component of modern wireless 
networks and are essential for providing reliable wireless connectivity to a wide range of devices.


## VPN:

A `Virtual Private Network` (`VPN`) is a type of network technology that allows users to create a secure and 
private connection over the internet. VPNs are often used to protect sensitive data and online activities
from unauthorized access and surveillance, particularly when accessing public networks or when working remotely.
A VPN works by creating a virtual tunnel `between the user's device` and a `remote server`, through which 
all internet traffic is routed. This tunnel is encrypted, which means that any data that is transmitted 
over the VPN is protected from interception and monitoring by third parties, including internet service 
providers (`ISPs`),` hackers`, and `government agencies`.

#### VPNs can be used to accomplish a variety of tasks, including:
> - Providing remote access to a company's internal network for employees who work from home or travel frequently.
> - Protecting sensitive data and communications while using public Wi-Fi networks or other unsecured internet connections.
> - Bypassing internet censorship and geo-restrictions, allowing users to access websites and online services that may be blocked in their location.
> - Hiding the user's IP address and online activities from ISPs and other third parties who may be tracking their internet usage.
>

VPNs can be set up on a variety of devices, including `desktop` and `laptop computers`, `smartphones`, and `tablets`.
They are often provided by VPN service providers, who may offer both free and paid plans with varying 
levels of features and functionality.
Overall, VPNs are a valuable tool for maintaining online privacy and security, and can be an essential 
component of a comprehensive online security strategy.


## Symmetric encryption:

`Symmetric encryption` is a type of encryption where the same secret key is used for both encrypting
and decrypting data. In other words, the same key that is used to encrypt the data is also used to decrypt it.
This makes symmetric encryption a faster and more efficient way of encrypting data than
asymmetric encryption, where two different keys are used for encryption and decryption.
In symmetric encryption, the plaintext (`original message`) is transformed into ciphertext (`encrypted message`) 
using the secret key, which is a random string of bits. The recipient of the ciphertext can 
then use the same secret key to decrypt the message and recover the plaintext.
There are several symmetric encryption algorithms, such as Advanced Encryption Standard (`AES`), 
Data Encryption Standard (`DES`), and Blowfish. These algorithms differ in the way they 
transform the plaintext into ciphertext and the strength of the encryption they provide.
Symmetric encryption is commonly used to secure data in `transit`, `such as emails`, `instant messages`, 
and data transfers over a network. It is also used to secure data at rest, such as files and databases stored 
on a computer or a server. However, since the same key is used for both encryption and decryption, 
the security of symmetric encryption relies heavily on keeping the key secret and ensuring that 
it does not fall into the wrong hands.


## Asymmetric encryption:

Asymmetric encryption, also known as public-key cryptography, is a type of encryption
where two different keys are used for encryption and decryption. One key,
called the public key, is used for encrypting data, while the other key, called the private key, 
is used for decrypting data. Unlike symmetric encryption, where the same key is used for both encryption and decryption, in asymmetric encryption, the two keys are mathematically related but are not the same.
In asymmetric encryption, the public key is widely distributed and can be freely shared, 
while the private key is kept secret and only known to the owner. When someone wants to send an encrypted message to the owner of the public key, they use the public key to encrypt the message. Only the owner of the private key can then decrypt the message using their private key.
Asymmetric encryption provides several advantages over symmetric encryption.
First, it eliminates the need for a secure channel for key exchange, as the public key can be 
freely distributed. Second, it provides a way to ensure the authenticity of the message sender,
as the private key is only known to the owner and can be used to sign messages. Third,
it provides a way to establish secure communications with multiple parties, as each party can have their
own public and private keys.
Some examples of asymmetric encryption algorithms include RSA, Diffie-Hellman, 
and Elliptic Curve Cryptography (ECC). Asymmetric encryption is commonly used to secure sensitive 
information such as passwords, credit card numbers, and other personal information in online transactions, 
as well as to secure communication channels between individuals and organizations.
