### Video Streaming - Computer Networking Assignment - HCMUT

#### Teacher: Bui Xuan Giang
#### Student:
    1. Tran Quang Huy

    2. Huynh Trung Nghia

    3. Nguyen Van Huu

### Specification
[1. Description:]
    [1.1 Client, ClientLauncher]
        The ClientLauncher starts the Client and the user interface which you use to send RTSP commands and which is used to display the video. In the Client class, you will need to implement the actions that are taken when the buttons are pressed. You do not need to modify the ClientLauncher module.

    [1.2 Server, ServerWorker]
        These two modules implement the server which responds to the RTSP requests and streams back the video. The RTSP interaction is already implemented and the ServerWorker calls methods from the RtpPacket class to packetize the video data. You do not need to modify these modules.

    [1.3 RtpPacket]
        This class is used to handle the RTP packets. It has separate methods for handling the received packets at the client side and you do not need to modify them. The Client also de-packetizes (decodes) the data and you do not need to modify this method. You will need to complete the implementation of video data RTPpacketization (which is used by the server).

    [1.6 VideoStream]
        This class is used to read video data from the file on disk. You do not need to modify this class.

[2. How to run:]
    - First, start the server with the command:

    > python Server.py <server_port>

    where server_port is the port your server listens to for incoming RTSP connections. The standard RTSP port is 554, but you will need to choose a port number greater than 1024.

    Then, start the client with the command:
    
    > python ClientLauncher.py <server_host> <server_port> <RTP_port> <video_file>

    where server_host is the name of the machine where the server is running, server_port is the port where the server is listening on, RTP_port is the port where the RTP packets are received, and video_file is the name of the video file you want to request (we have provided one example file movie.Mjpeg). The file format is described in Appendix section.


More info see in "HK1_2021_Assignment 1.pdf" and "Report Network.pdf"