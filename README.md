# Computer-Networking

長庚資管106電腦網路  
TA: 邱珮瑜  
TA Email : cindy0344112@gmail.com  
Office Hour: Wed. 1500-1700

-----

# Contents
+ ### CH1 Computer Networks & The Internet
    + #### 1.1
    + #### 1.2
        + #### 1.2.1
        + #### 1.2.2
    + #### 1.3
        + #### 1.3.1
        + #### 1.3.2
        + #### 1.3.3
    + #### 1.4
        + #### 1.4.1
        + #### 1.4.2
        + #### 1.4.3
        + #### 1.4.4
    + #### 1.5
    + #### 1.6
    + #### 1.7

+ ### CH2 Application Layer


## CH1 Computer Networks & The Internet
### 1.1 What is The Internet
### 1.2 The Network Edge
#### 1.2.1 Access Network
+ Home Access
    - DSL, Digital Subscriber Line  
    
        數位用戶迴路指的是透過一般銅質電話線，使用數據機 (Modem) 連接電腦系統與數位迴路，將高頻寬資訊帶給一般家庭與小企業用戶的持續性數位迴路。  
    <br />
        以現有的電話線路， 在不同頻率上分出一條通道來傳輸資料，即當連線傳輸資料的時候，是不影響到電話的使用。  

        The residential telephone line carries both data and traditional telephone signals simultaneously, which are encoded at different frequencies : 

        - High Speed Downstream channel : 50 kHz to 1 MHz band
        - Midium Speed Upstream channel : 4 kHz to 50 kHz band
        - Ordinary two-way telephone channel : 0 to 4 kHz band

    - Cable (Cable Internet Access)
        - HFC, Hybrid Fiber Coax
    - FTTH, Fiber To The Home
        - 遠快於網際網路速率，且也可提供電視及電話服務
        - 光學傳播網路架構
            - Passive Optical Network (PON, 被動)
            - Active Optical Network (AON, 主動)
        - 上傳: 2 ~ 10 Mbps
        - 下載: 10 ~ 20 Mbps


    - Dial - Up
    - Satallite
+ Enterprise Access (and Home)
    - Ethernet
    - WiFi
+ Wide-Area Wireless Access
    - 3G
    - LTE, Long Term Evolution
    - 4G
    - 5G


#### 1.2.2 Physical Media
- Guided Media 引導式媒介
    + Twisted-Pair Copper Wire
        - The wires are twisted together to **reduce the electrical interference** from similar pairs close by.
        - In the pass, people use twisted pair to transmit **Analog Signal** , today twisted pair can also transmit **Digital Signal**.
        #### Catagories
        - UTP, Unshielded Twisted Pair
            - UTP is commonly used for computer networks.
            - Data rates for LANs using twisted pair range from 10 Mbps to 10 Gbps.
            - The data rates that achieved depend on the thickness of the wire and the distance between transmitter & receiver.
        - STP, Shielded Twisted Pair
            - 4 pairs of twisted copper wire
            - 可以進一步屏蔽傳輸線，使之較不受外部電磁場干擾，為避免天線效應，一般建議需確實接地。但這種額外的保護結構降低了線材的彈性。
        #### Types
        - CAT-1 : 主要用於傳輸語音，用於資料傳輸
        - CAT-2 : 傳輸頻率為1MHz，用於語音傳輸和最高傳輸速率4Mbps的資料傳輸，常見於使用4Mbps規範 token ring in token passing
        - CAT-3 : 指目前在ANSI和EIA/TIA568標準中指定的電纜。該電纜的傳輸頻率為16MHz，用於語音傳輸及最高傳輸速率為10Mbps的資料傳輸，主要用於10BASE-T。
        - CAT-4 : 該類電纜的傳輸頻率為20MHz,用於語音傳輸和最高傳輸速率16Mbps的資料傳輸，主要用於基於令牌的區域網路和10BASE-T/100BASE-T。
        - CAT-5 : 該類電纜增加了繞線密度，外套一種高品質的絕緣材料，傳輸頻率為100MHz,用於語音傳輸和最高傳輸速率為100Mbps的資料傳輸，主要用於100BASE-T和10BASE-T網路，這是最常用的乙太網電纜。
        - CAT-5e : 超5類具有衰減小，串擾少，並且具有更高的衰減與串擾的比值（ACR）和訊號雜訊比（Structural Return Loss）、更小的時延誤差，效能得到很大提高。
        - CAT-6 : 10BASE-T/100BASE-T/1000BASE-T，傳輸頻率為250MHz傳輸速度為10Gbps標準外徑6mm。
        - CAT-6A : 擴展6類，10GBASE-T，傳輸頻率為500MHz傳輸速度為10Gbps標準外徑9mm。
        - CAT-6e : 傳輸頻率為500MHz傳輸速度為10Gbps標準外徑6mm。
        - CAT-7 : 傳輸頻率為600MHz傳輸速度為10Gbps單線標準外徑8mm多芯線標準外徑6mm。
        - CAT-8/8.1 : 在開發中（ANSI / TIA-568-C.2-1，ISO / IEC 11801第3版）
        - CAT-8.2 : 在開發中（ISO / IEC 11801第3版）
    + Coaxial Cable [同軸纜線(wiki)](https://zh.wikipedia.org/zh-tw/同轴电缆)
        - Quite common in cable television systems
        - Guided **shared medium**
    + Fiber Optics (光學)
        - 玻璃纖維
        - Conducts pulses of light, which each pulse representing a bit
        - Very low signal attenuation up to 100 km
        - The Optical Carrier (OC) standard link speeds range from 51.8 Mbps to 39.8 Gbps.
            - Standards today include OC-1, OC-3, OC-12, OC-24, ...
            - as OC-n, the link speed equals to n x 51.8 Mbps
- Unguided Media 非引導式媒介
    + Terrestrial Radio Channel
        - Environmental Considerations
            - Path loss & Shadow fading ([遮蔽衰弱](http://wshnt.kuas.edu.tw/network/s4/Data/Shadow.htm))
            - Multipath fading ([多重路徑衰減](http://wshnt.kuas.edu.tw/network/n11/Multipath%20Delay%20Spread.htm))
            - Interference (Due to other transmissions and electromagnetic signals)
    + Satellite Radio Channel
        + Geostationary Satellite 同步衛星
            - Achieved by placing in orbit at 36000 km
                - Cause the huge distance from ground station through satellite back to ground station introduces a substantial signal propagation delay of 280 ms
        + Low-Earth Orbiting (LEO) Satellite 近地軌道衛星
            - [Satellite Constellation](https://en.wikipedia.org/wiki/Satellite_constellation)


### 1.3 The Network Core
#### 1.3.1 Packet Switching
- Store & Forward Transmission

- Queuing Delay
    - In addition to the store-and-forward delays, packet suffer output buffer **queuing delays**.
    - Varibles, depend on the level of congestion in the network.
- Packet Loss
    - Occur when arriving packet find that the buffer is completely full with other packets waiting for transmission.
    - Either the "arriving packet" or one of the already-queued packets will be dropped.

- Forwarding Tables & Routing Protocols
    - Forwarding Table that maps destination addresses or portions of the destination addresses to that router's outbound link.
    - When a packet arrives a router, the router examines the address and search its forwarding table, using this destination address, to find the appropriate outbound link.  

#### 1.3.2 Circuit Switching
The resources needed along a path to provide for communication between the end systems are ***reserved*** for the duration for communication session.

> Traditional telephone networks are examples of circuit-switched networks.  


- Multiplexing in Circuit-Switched Networks
    - FDM, Frequence-Division Multiplexing
        - In telephones network, this frequency band typically has a width of 4 kHz.
        - FM radio station share the frequency spectrum between 88 MHz and 108 MHz.
    - TDM, Time-Division Multiplexing

#### Packet Switching vs. Circuit Switching

#### 1.3.3 A Network of Networks

### 1.4 Delay, Loss, Throughput in Packet-Switched Networks

#### 1.4.1 Overview of Delay in Packet-Switched Networks
- Nodal Processoring Delay
    - The time required to examine the packet's header and determine where to direct the packet.
    - Include the time needed to check for bit-level errors in the packet that occured in transmitting the packet's bit from upstream node to router.

   #### d<sub>nodal</sub> = d<sub>process</sub> + d<sub>queue</sub> + d<sub>trans</sub> + d<sub>propagation</sub>

- Queuing Delay
    - Packet waits to be transmitted onto the link.
    - The length of queuing delay depends on number of early-arriving packets which are queued and waiting for transmission.
    - If queue is empty or no other packet is currently being transmitted, the queuing delay will be 0.
- Transmissoin Delay
    - Denote the length of packet by L bits, and the transmission rate of the link from router A to router B by R bits/sec.
    - The transmission delay is **L/R**
- Propagation Delay
    - The prpagation speed depends on the physical medium of the link, and is in range of 2．10<sup>8</sup> meters/sec to 3．10<sup>8</sup> meters/sec
    - The propagation delay is _d_/_s_, _d_ is the distance between router A & B, _s_ is the propagation of link.

#### 1.4.2 Queuing Delay & Packet Loss
- Traffic Intensity 通訊密度, 流量強度
    - **La/R**, denote which L by all packets consist of L bits, _a_ as average rate at which packets arrive at the queue  (in units of packets/sec), _R_ is the transmossion rate  (in bits/sec)
    
    #### Consider with **L/R**

    - If **La/R** > 1, then the average rate at which bits arrive at the queue exceeds the rate at which the bits can be transmitted from the queue.
    - In case of **La/R** ≤ 1
        - If packets arrive periodically, each packet arrives every L/R seconds, then every packet will have no queuing delay.
        - If packets arrive in brusts but periodically, there can be a significant average queuing delay.
            - Suppose _N_ packets arrive simultaneously every (L/R)．N seconds, the first packet will be no queuing delay to transmit, the second packet transmitted with a L/R (in seconds) of queuing delay.
            - For general, the _N_th packet transmitted has a queuing delay of (_N_ -1)．L/R seconds 


    ![7](https://raw.githubusercontent.com/jason19970210/MarkdownPhotos/master/7.jpg)

- Packet Loss

#### 1.4.3 End-to-End Delay
_d_<sub>end-to-end</sub> = N．(_d_<sub>proc</sub> + _d_<sub>trans</sub> + _d_<sub>prop</sub>)

- Traceroute
- End System, Application & Other Delays
    - The source actually sends **3．_N_** packets to the destination.

#### 1.4.4 Throughput in Computer Networks
- Consider trasferring a large file froom Host A to Host B across computer networks.
- The instantaneous throughput (瞬間產生率) at any instant of time is the rate (in bits/sec) at which Host B is receiving the file.
- a network with _N_ links between the server and the client comsume the transmission rate being _R_<sub>1</sub>, _R_<sub>2</sub>, ..., _R_<sub>N</sub>. Found that the throughput for a file transfer from server to client is min {_R_<sub>1</sub>, _R_<sub>2</sub>, ..., _R_<sub>N</sub>}.

### 1.5 Protocol Layers & Their Service Models


### 1.6 Networks under Attack


### 1.7 History of Computer Networking and The Internet

----

## CH2 Application Layer
### 2.1 Principles of Networking Applications
#### 2.1.1 Network Application Architectures 網路應用程式架構
- Client-SErver Archtecture
    - Server : Always-on host
        - IP Address : Fixed, Well-known address
        - Data Center : Used to creating a powerful virtual server
            - Search Engines : Google, Bing
            - Internet Commerce : Amazon, e-Bay
            - Web-Based email : Gmail, Yahoo Mail
            - Social Networking : Facebook, Twitter
    - Client : Server requests from many other hosts
    > Client do not direct connect to each other
- P2P Archtecture
    Minimal  (or no) reliance on dedicated servers in data center. The application exploits direct communication between pairs of intermittenly connected hots, called peers. Communicate without passing through dedicated server.
    - Features
        - Self-Scalability
    - Applications
        - File Sharing : BitTorrent
        - Peer-Assisted download acceleration : Xunlei
        - Internet Telephony : Skype
        - IPTV : PPStream
    - 3 major challenges : 
        - ISP Friendly
        - Security
        - Incentives
#### 2.1.2 Process Communication
> A **sending process** creates and sends message into the network, a **receiving process** receives these messgae and possibly responds by sending message back.
- Client & Server Processes
- The Interface Between the Process & the Computer Network
- Addressing Processes
#### 2.1.3 Transport Services Available to Applications
#### 2.1.4 Transport Services Provided by the Internet
#### 2.1.5 Application-Layer Protocols
#### 2.1.6 Network Applications Converted This Book
### 2.2 The Web & The HTTP
#### 2.2.1 Overview of HTTP
#### 2.2.2 Non-Persistent & Persistent Connection
#### 2.2.3 HTTP Message Format
#### 2.2.4 User-Server Interaction Cookies
#### 2.2.5 Web Caching
#### 2.2.6 The Conditional GET
### 2.3 File Transfer : FTP
#### 2.3.1 FTP Commands and Replies
### 2.4 Electronic Mail in the Internet
#### 2.4.1 SMTP
#### 2.4.2 Compartion with HTTP
#### 2.4.3 Mail Message Format
#### 2.4.4 Mail Access Perotocols
### 2.5 DNS - The Internet's Dictionary Service
#### 2.5.1 Service Provided by DNS
#### 2.5.2 Overview of How DNS WOrks
#### 2.5.3 DNS Record & Messages
### 2.6 Peer-to-Peer Application (v6)
#### 2.6.1 P2P File Distribution
#### 2.6.2 Distributed Hash Tables (DHTs)
### 2.6 Video Streaming & Content Distribution Networks (v7)
#### 2.6.1 Internet Video
#### 2.6.2 HTTP Streaming & DASH
#### 2.6.3 Content Distribution Networks
#### 2.6.4 Case Studies : Netflix, Youtube, Kankan
### 2.7 Socket Programming : Creating Network Application
#### Socket Programming with UDP
#### Socket Programming with TCP 
