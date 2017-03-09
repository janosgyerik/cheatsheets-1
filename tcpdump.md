Common prefix for brevity:

    prefix='sudo tcpdump -i eth0'

Monitor HTTP headers going to some host:

    $prefix -A dst host HOSTNAME
    
This looks useful: https://danielmiessler.com/study/tcpdump/#gs.2D_vaZw
