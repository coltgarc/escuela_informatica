### Networking models categorize and provide a structure for networking protocols and standards.

----

#### protocols
a set of (logical) rules defining how networking devices and software should work
#### networking model 
protocol protocol protocol standard
protocol protocol protocol standard
protocol protocol protocol standard
#### networks without standardization
cannot communicate with each other, so everything is standardized

### Data is encapsulated as it goes DOWN the stack
### Data is de-encapsulated as it goes UP the stack

#### Open Systems Interconnection model
a conceptual model that categorizes and standardizes the different functions in a network
created by the ISO
functions are divided into 7 layers

----
## The 7 layers

### A)ll P)eople S)eem T)o N)eed D)ata P)rocessing

### The Top 3 (PDU = "Data")
#### 7) Application layer
interacts with software applications like web browsers
HTTP and HTTPS are layer 7 protocols
functions of layer 7
	identifying communication partners
	synchronizing communication

#### 6) Presentation layer
data in the application layer is in "Application format"
it needs to be translated to a different format to be sent over the network
the presentation layer's job is to translate between application and network formats.
for example, encryption of data as it is sent, and decryption of data as it is received.
also translates between different application-layer formats

#### 5) Session Layer
controls dialogues (sessions) between hosts
establishes, manages and terminates connections between the local application (for example, your web browser) and the remote application (for example, youtube).

----
#### 4) Transport Layer (PDU = Segment)
segments and reassembles data for communications between end hots
breaks large pieces of data into smaller segments which prevents errors and is easier to transfer
provides host-to-host communication
	or (end to end communication)
adds a "L4 header" to the end of the data being encapsulated to create a segment.

----

#### 3) Network Layer (PDU = Packet)
another header, "L3 header," is appended to the data unit
provides connectivity between end hosts on different networks (ie. outside of the lan)
provides logical addressing (ip addresses)
provides **Path Selection** between source and destination
routers operate at layer 3

----
#### 2) Data Link Layer (PDU = Frame)
Layer 2 header AND trailer
provides node-to-node connectivity and data transfer
1) like pc to switch, switch to router, router to router
**defines how data is formatted for transmission over a physical medium**
detects and possibly corrects physical layer errors
uses layer 2 addressing, separate from layer 3 addressing
**Switches operate at this layer**

----

#### 1) Physical Layer (PDU = Bit)
defines physical characteristics of the medium used to transfer data between devices
for example, voltage, max transmission distances, physical connectors
digital bits are converted into **electrical (copper/UTP), radio (wireless), or optical (fiber-optic)** 
all of the information in day 2's video are from Layer 1, the physical layer of the OSI model
the bits are sent over, physically