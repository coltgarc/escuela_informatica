Ethernet headers+trailers are added in layer 2 of the OSI model (data link)
Eth. headers are composed of:
	Preamble
	S.tart F.rame D.elimiter
	Destination
	Source
	Type
Eth. trailers:
	F.rame C.heck S.equence
		detects any errors that might have occurred in transmission
# Header
## Preamble
	length: 7 bytes long
	alternating 1's and 0's (10101010 * 7)
	Allows devices to synchronize their receiver clocks
## SFD - Start Frame Delimiter
	Length: 1 byte (8 bits)
	1010101011
	Marks the end of the Preamble and the beginning of the rest of the frame

## Destination + Source
	Destination length: 6 bytes (48-bit)
	Source length: 6 bytes (48-bit)
	Indicates the devices sending and receiving the frame
	Consists of TWO (2) M.edia A.ccess C.ontrol addresses
		MAC = 6 bytes (48-bit) address of the physical devices

## Type/Length
	length: 4 bytes (16-bit), 2 fields of 2
	value of 1500 or less -> it's indicating the length in bytes
	value of 1536 or greater -> it's the Type (usually IPv4 or IPv6)
		ex) 0x0800 (2048 in decimal) -> IPv4
		ex) 0x86DD (34525 in decimal) -> IPv6
# Trailer
## FCS - Frame Check Sequence
	length: 4 bytes (32 bits)
	detects corrupted data by running CRC algorithms over the received data
	CRC - Cyclic Redundancy Check
		further reading: wikipedia

# Header + Trailer: 26 bytes (208-bit)

# MAC Addresses
6-byte (48-bit) physical address assigned to the devices when it is made
aka Burned-In Address (BIA)
globally unique
first 3 bytes is the OUI (organizationally unique identifier)
	assigned to company making the devices
last 3 bytes are unique to the device
written as 12 hexademical character
## MAC Address Table
	Switches "Dynamically Learn" MAC addresses as they pass data through them
		called Dynamic MAC Addresses
	It saves the MAC address in relation to interfaces (like F0/1)
	Unknown Unicast frame = FLOOD all interfaces (except source)
	Known Unicast frames = FORWARD directly to single interface
	Dynamic MAC Addresses are forgotten after 5 minutes of AFK
	
# Decimal
10 possible digits
0     10     20     30      40      50      60      70
1     11     21     31      41      51      61      71
2     12     22     32      42      52      62      72
3     13     23     33      43      53      63      73
4     14     24     34      44      54      64      74
5     15     25     35      45      55      65      75
6     16     26     36      46      56      66      76
7     17     27     37      47      57      67      77
8     18     28     38      48      58      68      78
9     19     29     39      49      59      69      79

# Hexadecimal
16 possible digits
0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F
A = 10
B = 11
C = 12
D = 13
E = 14
F = 15
![[hexadecimalchart.png]]

