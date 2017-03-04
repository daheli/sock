# sock
Richard Stevens' sock program
##Introduction
In TCP/IP Illustrated Vol. 1, Richard Stevens used a program called "sock" to demonstrate the many properties of TCP/IP. Unfortunately, the book only speaks about how to use the program but does not point to a site for downloading its sources. While sock is contained in the code package accompanying UNIX Network Programming, this code is also getting dated.

Recently I came across a standalone version of sock on a T/TCP project page. It was likewise indicating signs of bitrot, so I dusted it off and updated it to build on at least Linux, FreeBSD, OpenBSD, and MacOS, and made it available for download here.

I'm more than happy to include build fixes for other platforms, but I can not provide general build support, etc.

##News
0.3.2 is out, with minor compatibility updates. 01.06.10

##Features
You want to have a look at the book for this, but here's the help output:


       usage: sock [ options ] <host> <port>       (for client; default)
       sock [ options ] -s [ <IPaddr> ] <port>     (for server)
       sock [ options ] -i <host> <port>           (for "source" client)
       sock [ options ] -i -s [ <IPaddr> ] <port>  (for "sink" server)
       options: -b n  bind n as client's local port number
         -c    convert newline to CR/LF & vice versa
         -f a.b.c.d.p  foreign IP address = a.b.c.d, foreign port# = p
         -g a.b.c.d  loose source route
         -h    issue TCP half close on standard input EOF
         -i    "source" data to socket, "sink" data from socket (w/-s)
         -j a.b.c.d  join multicast group
         -k    write or writev in chunks
         -l a.b.c.d.p  client's local IP address = a.b.c.d, local port# = p
         -n n  #buffers to write for "source" client (default 1024)
         -o    do NOT connect UDP client
         -p n  #ms to pause before each read or write (source/sink)
         -q n  size of listen queue for TCP server (default 5)
         -r n  #bytes per read() for "sink" server (default 1024)
         -s    operate as server instead of client
         -t n  set multicast ttl
         -u    use UDP instead of TCP
         -v    verbose
         -w n  #bytes per write() for "source" client (default 1024)
         -x n  #ms for SO_RCVTIMEO (receive timeout)
         -y n  #ms for SO_SNDTIMEO (send timeout)
         -A    SO_REUSEADDR option
         -B    SO_BROADCAST option
         -C    set terminal to cbreak mode
         -D    SO_DEBUG option
         -E    IP_RECVDSTADDR option
         -F    fork after connection accepted (TCP concurrent server)
         -G a.b.c.d  strict source route
         -H n  IP_TOS option (16=min del, 8=max thru, 4=max rel, 2=min$)
         -I    SIGIO signal
         -J n  IP_TTL option
         -K    SO_KEEPALIVE option
         -L n  SO_LINGER option, n = linger time
         -N    TCP_NODELAY option
         -O n  #ms to pause after listen, but before first accept
         -P n  #ms to pause before first read or write (source/sink)
         -Q n  #ms to pause after receiving FIN, but before close
         -R n  SO_RCVBUF option
         -S n  SO_SNDBUF option
         -T    SO_REUSEPORT option
         -U n  enter urgent mode before write number n (source only)
         -V    use writev() instead of write(); enables -k too
         -W    ignore write errors for sink client
         -X n  TCP_MAXSEG option (set MSS)
         -Y    SO_DONTROUTE option
         -Z    MSG_PEEK
	 
