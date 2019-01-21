# Rendu TP 3
Je précise avant tout qu'avant d'entamer la partie 3, j'ai eu un problème sur mon pc qui m'a fait perdre mes VM... Louis m'a donc dépanné en me passant sa VM. Il est donc normal de voir louis en nom lors des screen de la partie 3.

## I. Création et utilisation simples d'une VM CentOS

(Début fait tous ensemble en classe)

### 5. Faire joujou avec quelques commandes

 #### ping hôte -> VM et ping VM -> hôte :

 ![alt text](https://github.com/MathieuCaselles/b1-tp3/blob/master/screen/1.png)  

#### Affichage de la table de routage sur la VM :

![alt text](https://github.com/MathieuCaselles/b1-tp3/blob/master/screen/2.png)  
_Ligne qui leur permet de discuter via le réseau host-only :_

    192.168.127.0/24 dev enp0s8 proto kernel scope link src 192.168.127.10

#### Affichage de la table de routage hôte :

![alt text](https://github.com/MathieuCaselles/b1-tp3/blob/master/screen/3.png)  
_Ligne qui leur permet de discuter via le réseau host-only :_

    192.168.127.0    255.255.255.0         On-link     192.168.127.1    281

Utilisation de curl :  

![alt text](https://github.com/MathieuCaselles/b1-tp3/blob/master/screen/4.png)  

Utilisation de dig :


#### Dig Ynov


    [root@localhost ~]# dig ynov.com

    ; <<>> DiG 9.9.4-RedHat-9.9.4-72.el7 <<>> ynov.com
    ;; global options: +cmd
    ;; Got answer:
    ;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 8349
    ;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 13, ADDITIONAL: 27

    ;; OPT PSEUDOSECTION:
    ; EDNS: version: 0, flags:; udp: 4096
    ;; QUESTION SECTION:
    ;ynov.com.                      IN      A

    ;; ANSWER SECTION:
    ynov.com.               823     IN      A       217.70.184.38

    ;; AUTHORITY SECTION:
    com.                    79468   IN      NS      c.gtld-servers.net.
    com.                    79468   IN      NS      a.gtld-servers.net.
    com.                    79468   IN      NS      i.gtld-servers.net.
    com.                    79468   IN      NS      d.gtld-servers.net.
    com.                    79468   IN      NS      l.gtld-servers.net.
    com.                    79468   IN      NS      f.gtld-servers.net.
    com.                    79468   IN      NS      e.gtld-servers.net.
    com.                    79468   IN      NS      m.gtld-servers.net.
    com.                    79468   IN      NS      g.gtld-servers.net.
    com.                    79468   IN      NS      b.gtld-servers.net.
    com.                    79468   IN      NS      h.gtld-servers.net.
    com.                    79468   IN      NS      k.gtld-servers.net.
    com.                    79468   IN      NS      j.gtld-servers.net.

    ;; ADDITIONAL SECTION:
    a.gtld-servers.net.     79468   IN      A       192.5.6.30
    a.gtld-servers.net.     79468   IN      AAAA    2001:503:a83e::2:30
    b.gtld-servers.net.     79468   IN      A       192.33.14.30
    b.gtld-servers.net.     79468   IN      AAAA    2001:503:231d::2:30
    c.gtld-servers.net.     79468   IN      A       192.26.92.30
    c.gtld-servers.net.     79468   IN      AAAA    2001:503:83eb::30
    d.gtld-servers.net.     79468   IN      A       192.31.80.30
    d.gtld-servers.net.     79468   IN      AAAA    2001:500:856e::30
    e.gtld-servers.net.     79468   IN      A       192.12.94.30
    e.gtld-servers.net.     79468   IN      AAAA    2001:502:1ca1::30
    f.gtld-servers.net.     79468   IN      A       192.35.51.30
    f.gtld-servers.net.     79468   IN      AAAA    2001:503:d414::30
    g.gtld-servers.net.     79468   IN      A       192.42.93.30
    g.gtld-servers.net.     79468   IN      AAAA    2001:503:eea3::30
    h.gtld-servers.net.     79468   IN      A       192.54.112.30
    h.gtld-servers.net.     79468   IN      AAAA    2001:502:8cc::30
    i.gtld-servers.net.     79468   IN      A       192.43.172.30
    i.gtld-servers.net.     79468   IN      AAAA    2001:503:39c1::30
    j.gtld-servers.net.     79468   IN      A       192.48.79.30
    j.gtld-servers.net.     79468   IN      AAAA    2001:502:7094::30
    k.gtld-servers.net.     79468   IN      A       192.52.178.30
    k.gtld-servers.net.     79468   IN      AAAA    2001:503:d2d::30
    l.gtld-servers.net.     79468   IN      A       192.41.162.30
    l.gtld-servers.net.     79468   IN      AAAA    2001:500:d937::30
    m.gtld-servers.net.     79468   IN      A       192.55.83.30
    m.gtld-servers.net.     79468   IN      AAAA    2001:501:b1f9::30

    ;; Query time: 5 msec
    ;; SERVER: 10.33.10.20#53(10.33.10.20)
    ;; WHEN: Tue Jan 15 10:13:07 CET 2019
    ;; MSG SIZE  rcvd: 849


#### Dig Google


    [root@localhost ~]# dig google.com

    ; <<>> DiG 9.9.4-RedHat-9.9.4-72.el7 <<>> google.com
    ;; global options: +cmd
    ;; Got answer:
    ;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 6271
    ;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 13, ADDITIONAL: 27

    ;; OPT PSEUDOSECTION:
    ; EDNS: version: 0, flags:; udp: 4096
    ;; QUESTION SECTION:
    ;google.com.                    IN      A

    ;; ANSWER SECTION:
    google.com.             5       IN      A       172.217.22.142

    ;; AUTHORITY SECTION:
    com.                    78995   IN      NS      j.gtld-servers.net.
    com.                    78995   IN      NS      b.gtld-servers.net.
    com.                    78995   IN      NS      l.gtld-servers.net.
    com.                    78995   IN      NS      g.gtld-servers.net.
    com.                    78995   IN      NS      e.gtld-servers.net.
    com.                    78995   IN      NS      c.gtld-servers.net.
    com.                    78995   IN      NS      i.gtld-servers.net.
    com.                    78995   IN      NS      f.gtld-servers.net.
    com.                    78995   IN      NS      a.gtld-servers.net.
    com.                    78995   IN      NS      m.gtld-servers.net.
    com.                    78995   IN      NS      k.gtld-servers.net.
    com.                    78995   IN      NS      h.gtld-servers.net.
    com.                    78995   IN      NS      d.gtld-servers.net.

    ;; ADDITIONAL SECTION:
    a.gtld-servers.net.     78995   IN      A       192.5.6.30
    a.gtld-servers.net.     78995   IN      AAAA    2001:503:a83e::2:30
    b.gtld-servers.net.     78995   IN      A       192.33.14.30
    b.gtld-servers.net.     78995   IN      AAAA    2001:503:231d::2:30
    c.gtld-servers.net.     78995   IN      A       192.26.92.30
    c.gtld-servers.net.     78995   IN      AAAA    2001:503:83eb::30
    d.gtld-servers.net.     78995   IN      A       192.31.80.30
    d.gtld-servers.net.     78995   IN      AAAA    2001:500:856e::30
    e.gtld-servers.net.     78995   IN      A       192.12.94.30
    e.gtld-servers.net.     78995   IN      AAAA    2001:502:1ca1::30
    f.gtld-servers.net.     78995   IN      A       192.35.51.30
    f.gtld-servers.net.     78995   IN      AAAA    2001:503:d414::30
    g.gtld-servers.net.     78995   IN      A       192.42.93.30
    g.gtld-servers.net.     78995   IN      AAAA    2001:503:eea3::30
    h.gtld-servers.net.     78995   IN      A       192.54.112.30
    h.gtld-servers.net.     78995   IN      AAAA    2001:502:8cc::30
    i.gtld-servers.net.     78995   IN      A       192.43.172.30
    i.gtld-servers.net.     78995   IN      AAAA    2001:503:39c1::30
    j.gtld-servers.net.     78995   IN      A       192.48.79.30
    j.gtld-servers.net.     78995   IN      AAAA    2001:502:7094::30
    k.gtld-servers.net.     78995   IN      A       192.52.178.30
    k.gtld-servers.net.     78995   IN      AAAA    2001:503:d2d::30
    l.gtld-servers.net.     78995   IN      A       192.41.162.30
    l.gtld-servers.net.     78995   IN      AAAA    2001:500:d937::30
    m.gtld-servers.net.     78995   IN      A       192.55.83.30
    m.gtld-servers.net.     78995   IN      AAAA    2001:501:b1f9::30

    ;; Query time: 12 msec
    ;; SERVER: 10.33.10.20#53(10.33.10.20)
    ;; WHEN: Tue Jan 15 10:21:00 CET 2019
    ;; MSG SIZE  rcvd: 851


## II. Notion de ports et SSH

### 1. Exploration des ports locaux

#### utiliser la commande ss


    [root@localhost ~]# ss
    Netid  State      Recv-Q Send-Q                 Local Address:Port                                  Peer Address:Port
    u_str  ESTAB      0      0                                  * 24536                                            * 24537
    u_str  ESTAB      0      0                                  * 24522                                            * 24523
    u_str  ESTAB      0      0                                  * 24537                                            * 24536
    u_str  ESTAB      0      0                                  * 24578                                            * 24579
    u_str  ESTAB      0      0                                  * 24523                                            * 24522
    u_str  ESTAB      0      0                                  * 20884                                            * 20885
    u_str  ESTAB      0      0                                  * 24575                                            * 24576
    u_str  ESTAB      0      0                                  * 24576                                            * 24575
    u_str  ESTAB      0      0                                  * 24540                                            * 24539
    u_str  ESTAB      0      0                                  * 24581                                            * 24582
    u_str  ESTAB      0      0                                  * 21050                                            * 21051
    u_str  ESTAB      0      0                                  * 24582                                            * 24581
    u_str  ESTAB      0      0        /run/dbus/system_bus_socket 20885                                            * 20884
    u_str  ESTAB      0      0                                  * 24579                                            * 24578
    u_str  ESTAB      0      0                                  * 24539                                            * 24540
    u_str  ESTAB      0      0                                  * 24532                                            * 24533
    u_str  ESTAB      0      0                                  * 24529                                            * 24530
    u_str  ESTAB      0      0                                  * 24530                                            * 24529
    u_str  ESTAB      0      0                                  * 23720                                            * 23721
    u_str  ESTAB      0      0                                  * 20318                                            * 20430
    u_str  ESTAB      0      0        /run/dbus/system_bus_socket 24770                                            * 24769
    u_str  ESTAB      0      0                                  * 24525                                            * 24526
    u_str  ESTAB      0      0                                  * 24533                                            * 24532
    u_str  ESTAB      0      0        /run/systemd/journal/stdout 23772                                            * 23771
    u_str  ESTAB      0      0                                  * 23771                                            * 23772
    u_str  ESTAB      0      0                                  * 24549                                            * 24548
    u_str  ESTAB      0      0                                  * 24548                                            * 24549
    u_str  ESTAB      0      0                                  * 24546                                            * 24545
    u_str  ESTAB      0      0                                  * 24545                                            * 24546
    u_str  ESTAB      0      0                                  * 24551                                            * 24552
    u_str  ESTAB      0      0                                  * 24584                                            * 24585
    u_str  ESTAB      0      0                                  * 22124                                            * 22125
    u_str  ESTAB      0      0                                  * 24769                                            * 24770
    u_str  ESTAB      0      0                                  * 24585                                            * 24584
    u_str  ESTAB      0      0        /run/dbus/system_bus_socket 22125                                            * 22124
    u_str  ESTAB      0      0        /run/systemd/journal/stdout 21185                                            * 21184
    u_str  ESTAB      0      0                                  * 24587                                            * 24588
    u_str  ESTAB      0      0                                  * 24588                                            * 24587
    u_str  ESTAB      0      0                                  * 24590                                            * 24591
    u_str  ESTAB      0      0                                  * 24569                                            * 24570
    u_str  ESTAB      0      0                                  * 24570                                            * 24569
    u_str  ESTAB      0      0                                  * 21122                                            * 21123
    u_str  ESTAB      0      0                                  * 21326                                            * 21327
    u_str  ESTAB      0      0                                  * 24572                                            * 24573
    u_str  ESTAB      0      0        /run/dbus/system_bus_socket 21123                                            * 21122
    u_str  ESTAB      0      0        /run/systemd/journal/stdout 20866                                            * 20865
    u_str  ESTAB      0      0                                  * 24573                                            * 24572
    u_str  ESTAB      0      0                                  * 20865                                            * 20866
    u_str  ESTAB      0      0        /run/dbus/system_bus_socket 20430                                            * 20318
    u_str  ESTAB      0      0                                  * 20429                                            * 20428
    u_str  ESTAB      0      0                                  * 20428                                            * 20429
    u_str  ESTAB      0      0                                  * 15792                                            * 15793
    u_str  ESTAB      0      0                                  * 20563                                            * 20564
    u_str  ESTAB      0      0        /run/systemd/journal/stdout 15793                                            * 15792
    u_str  ESTAB      0      0                                  * 24526                                            * 24525
    u_str  ESTAB      0      0                                  * 24560                                            * 24561
    u_str  ESTAB      0      0        /run/systemd/journal/stdout 23721                                            * 23720
    u_str  ESTAB      0      0                                  * 15618                                            * 15619
    u_str  ESTAB      0      0                                  * 24561                                            * 24560
    u_str  ESTAB      0      0        /run/systemd/journal/stdout 15619                                            * 15618
    u_str  ESTAB      0      0                                  * 24563                                            * 24564
    u_str  ESTAB      0      0        /run/dbus/system_bus_socket 21051                                            * 21050
    u_str  ESTAB      0      0        /run/dbus/system_bus_socket 21327                                            * 21326
    u_str  ESTAB      0      0                                  * 24564                                            * 24563
    u_str  ESTAB      0      0        /run/systemd/journal/stdout 20363                                            * 20362
    u_str  ESTAB      0      0                                  * 24566                                            * 24567
    u_str  ESTAB      0      0                                  * 20362                                            * 20363
    u_str  ESTAB      0      0                                  * 24567                                            * 24566
    u_str  ESTAB      0      0                                  * 21184                                            * 21185
    u_str  ESTAB      0      0                                  * 24555                                            * 24554
    u_str  ESTAB      0      0                                  * 24591                                            * 24590
    u_str  ESTAB      0      0                                  * 20141                                            * 20142
    u_str  ESTAB      0      0                                  * 24554                                            * 24555
    u_str  ESTAB      0      0                                  * 20142                                            * 20141
    u_str  ESTAB      0      0                                  * 24593                                            * 24594
    u_str  ESTAB      0      0                                  * 24552                                            * 24551
    u_str  ESTAB      0      0                                  * 24594                                            * 24593
    u_str  ESTAB      0      0                                  * 24558                                            * 24557
    u_str  ESTAB      0      0        /run/systemd/journal/stdout 20564                                            * 20563
    u_str  ESTAB      0      0                                  * 24596                                            * 24597
    u_str  ESTAB      0      0                                  * 24557                                            * 24558
    u_str  ESTAB      0      0                                  * 24597                                            * 24596
    tcp    ESTAB      0      0                     192.168.127.10:ssh                                  192.168.127.1:resacommunity


#### utiliser ss -4


    [root@localhost ~]# ss -4
    Netid  State      Recv-Q Send-Q                 Local Address:Port                                  Peer Address:Port
    tcp    ESTAB      0      36                    192.168.127.10:ssh                                  192.168.127.1:resacommunity

#### utiliser ss -t pour TCP


    [root@localhost ~]# ss -t
    State      Recv-Q Send-Q                    Local Address:Port                                     Peer Address:Port
    ESTAB      0      36                       192.168.127.10:ssh                                     192.168.127.1:resacommunity


#### utiliser ss -l pour listening


    [root@localhost ~]# ss -l
    Netid  State      Recv-Q Send-Q                 Local Address:Port                                  Peer Address:Port
    nl     UNCONN     0      0                               rtnl:NetworkManager/2707                               *
    nl     UNCONN     0      0                               rtnl:kernel                                            *
    nl     UNCONN     0      0                               rtnl:NetworkManager/2707                               *
    nl     UNCONN     768    0                            tcpdiag:kernel                                            *
    nl     UNCONN     4352   0                            tcpdiag:ss/3771                                           *
    nl     UNCONN     0      0                               xfrm:kernel                                            *
    nl     UNCONN     0      0                            selinux:kernel                                            *
    nl     UNCONN     0      0                            selinux:systemd/1                                         *
    nl     UNCONN     0      0                            selinux:dbus-daemon/2657                                  *
    nl     UNCONN     0      0                            selinux:dbus-daemon/2657                                  *
    nl     UNCONN     0      0                            selinux:systemd/1                                         *
    nl     UNCONN     0      0                              audit:systemd/1                                         *
    nl     UNCONN     0      0                              audit:kernel                                            *
    nl     UNCONN     0      0                              audit:auditd/2629                                       *
    nl     UNCONN     0      0                          fiblookup:kernel                                            *
    nl     UNCONN     0      0                          connector:kernel                                            *
    nl     UNCONN     0      0                                nft:kernel                                            *
    nl     UNCONN     0      0                             uevent:kernel                                            *
    nl     UNCONN     0      0                             uevent:systemd-logind/2656                               *
    nl     UNCONN     0      0                             uevent:-4129                                             *
    nl     UNCONN     0      0                             uevent:tuned/3214                                        *
    nl     UNCONN     0      0                             uevent:systemd/1                                         *
    nl     UNCONN     0      0                             uevent:NetworkManager/2707                               *
    nl     UNCONN     0      0                             uevent:-4107                                             *
    nl     UNCONN     0      0                             uevent:systemd-udevd/1460                                *
    nl     UNCONN     0      0                             uevent:-4118                                             *
    nl     UNCONN     0      0                             uevent:-4117                                             *
    nl     UNCONN     0      0                             uevent:-4119                                             *
    nl     UNCONN     0      0                             uevent:tuned/3214                                        *
    nl     UNCONN     0      0                             uevent:-4129                                             *
    nl     UNCONN     0      0                             uevent:NetworkManager/2707                               *
    nl     UNCONN     0      0                             uevent:-4119                                             *
    nl     UNCONN     0      0                             uevent:-4118                                             *
    nl     UNCONN     0      0                             uevent:-4117                                             *
    nl     UNCONN     0      0                             uevent:systemd-logind/2656                               *
    nl     UNCONN     0      0                             uevent:-4107                                             *
    nl     UNCONN     0      0                             uevent:systemd/1                                         *
    nl     UNCONN     0      0                               genl:kernel                                            *
    nl     UNCONN     0      0                         scsi-trans:kernel                                            *
    p_raw  UNCONN     0      0                                  *:enp0s3                                            *
    p_dgr  UNCONN     0      0                                arp:enp0s8                                            *
    u_dgr  UNCONN     0      0                /run/systemd/notify 7439                                             * 0
    u_dgr  UNCONN     0      0         /run/systemd/cgroups-agent 7441                                             * 0
    u_str  LISTEN     0      128      /run/systemd/journal/stdout 7456                                             * 0
    u_dgr  UNCONN     0      0        /run/systemd/journal/socket 7459                                             * 0
    u_dgr  UNCONN     0      0                           /dev/log 7461                                             * 0
    u_str  LISTEN     0      100                    public/pickup 24565                                            * 0
    u_str  LISTEN     0      128      /run/dbus/system_bus_socket 20304                                            * 0
    u_str  LISTEN     0      128         /run/lvm/lvmpolld.socket 14943                                            * 0
    u_str  LISTEN     0      100                  private/rewrite 24579                                            * 0
    u_str  LISTEN     0      100                   private/bounce 24582                                            * 0
    u_str  LISTEN     0      100                    private/defer 24585                                            * 0
    u_str  LISTEN     0      100                    private/trace 24588                                            * 0
    u_str  LISTEN     0      100                   private/verify 24591                                            * 0
    u_str  LISTEN     0      100                 private/proxymap 24597                                            * 0
    u_str  LISTEN     0      100               private/proxywrite 24600                                            * 0
    u_str  LISTEN     0      100                     private/smtp 24603                                            * 0
    u_str  LISTEN     0      100                    private/relay 24606                                            * 0
    u_str  LISTEN     0      100                    private/error 24612                                            * 0
    u_str  LISTEN     0      100                    private/retry 24615                                            * 0
    u_str  LISTEN     0      100                  private/discard 24618                                            * 0
    u_str  LISTEN     0      100                    private/local 24621                                            * 0
    u_str  LISTEN     0      100                  private/virtual 24624                                            * 0
    u_str  LISTEN     0      100                     private/lmtp 24627                                            * 0
    u_str  LISTEN     0      100                    private/anvil 24630                                            * 0
    u_str  LISTEN     0      100                   private/scache 24633                                            * 0
    u_str  LISTEN     0      100                   public/cleanup 24569                                            * 0
    u_str  LISTEN     0      100                      public/qmgr 24572                                            * 0
    u_str  LISTEN     0      100                     public/flush 24594                                            * 0
    u_str  LISTEN     0      100                     public/showq 24609                                            * 0
    u_str  LISTEN     0      10     /var/run/NetworkManager/private-dhcp 22943                                            * 0             
    u_str  LISTEN     0      128             /run/systemd/private 14759                                            * 0
    u_seq  LISTEN     0      128                /run/udev/control 14805                                            * 0
    u_str  LISTEN     0      128          /run/lvm/lvmetad.socket 14809                                            * 0
    u_str  LISTEN     0      100                   private/tlsmgr 24576                                            * 0
    u_dgr  UNCONN     0      0             /run/systemd/shutdownd 14835                                            * 0
    u_dgr  UNCONN     0      0                                  * 21447                                            * 7461
    u_dgr  UNCONN     0      0                                  * 24657                                            * 7461
    u_dgr  UNCONN     0      0                                  * 24012                                            * 7461
    u_dgr  UNCONN     0      0                                  * 25309                                            * 7461
    u_dgr  UNCONN     0      0                                  * 23060                                            * 7461
    u_dgr  UNCONN     0      0                                  * 20149                                            * 7461
    u_dgr  UNCONN     0      0                                  * 21349                                            * 7461
    u_dgr  UNCONN     0      0                                  * 15259                                            * 7439
    u_dgr  UNCONN     0      0                                  * 15848                                            * 15847
    u_dgr  UNCONN     0      0                                  * 21106                                            * 7461
    u_dgr  UNCONN     0      0                                  * 15847                                            * 15848
    u_dgr  UNCONN     0      0                                  * 21118                                            * 7461
    u_dgr  UNCONN     0      0                                  * 15738                                            * 7459
    u_dgr  UNCONN     0      0                                  * 15269                                            * 7459
    u_dgr  UNCONN     0      0                                  * 24673                                            * 7461
    u_dgr  UNCONN     0      0                                  * 20646                                            * 7459
    u_dgr  UNCONN     0      0                                  * 24537                                            * 7461
    raw    UNCONN     0      0                                 :::ipv6-icmp                                       :::*
    udp    UNCONN     0      0                                  *:bootpc                                           *:*
    tcp    LISTEN     0      128                                *:ssh                                              *:*
    tcp    LISTEN     0      100                        127.0.0.1:smtp                                             *:*
    tcp    LISTEN     0      128                               :::ssh                                             :::*
    tcp    LISTEN     0      100                              ::1:smtp                                            :::*



#### ss avec -n et -p


    [root@localhost ~]# ss -4np
    Netid  State      Recv-Q Send-Q                   Local Address:Port                                  Peer Address:Port
    tcp    ESTAB      0      36                      192.168.127.10:22                                   192.168.127.1:2169                users:(("sshd",pid=3843,fd=3))

J'ai bien une application qui écoute sur le port 22



### 2 SSH

#### Pour me connecter en ssh a la vm je n'ai pas besoin de putty mais juste de ssh:

    PS C:\WINDOWS\system32> ssh root@192.168.127.10
    root@192.168.127.10's password:
    Last login: Tue Jan 15 12:17:18 2019 from 192.168.127.1
    [root@localhost ~]#

### 3. Firewall

#### SSH :
Je change le port et met 2222 à la place comme dans l'exemple puis je reboot.  
comme le montre le screer ci-dessous, la connexion échoue car cela veut se connecter au port 22.  
je fini donc par lui dire de passer par le port 2222 et cela fonctionne:


![alt text](https://github.com/MathieuCaselles/b1-tp3/blob/master/screen/5.png)  


## III. Routage statique

### 1. Préparation des hôtes (vos PCs)

Pierre se met dans le réseau 12 sur Windows

![alt text](https://github.com/MathieuCaselles/b1-tp3/blob/master/screen/9.png)  

Il modifie mon reseau host only en mode pc1

![alt text](https://github.com/MathieuCaselles/b1-tp3/blob/master/screen/16.png)  

#### Check



Il ping le PC 2 qui est le mien et il est bien répondu

![alt text](https://github.com/MathieuCaselles/b1-tp3/blob/master/screen/10.png)  

Pour changer l&#39;ip dans CentOS je tape nano /etc/sysconfig/network-scripts/ifcfg-enp0s8

![alt text](https://github.com/MathieuCaselles/b1-tp3/blob/master/screen/11.png)  

J&#39;arrive ici et je modifie l&#39;ip en 192.168.101.10 et je quitte en sauvegardant

Il ping sa vm1 a son pc1 et ça répond correctement

![alt text](https://github.com/MathieuCaselles/b1-tp3/blob/master/screen/12.png)  

Je me ping de vm2 à pc2 et ça fonctionne aussi

#### Activation du routage sur les PCs

##### Windows

Je vais dans le regedit et à la direction HKEY\_LOCAL\_MACHINE\SYSTEM\CurrentControlSet\ Services\Tcpip\Parameters\IPEnableRouter et je mets la valeur a 1

![alt text](https://github.com/MathieuCaselles/b1-tp3/blob/master/screen/13.png)  

Je vais ensuite mettre en automatique Routage a accès distant dans services.msc et je redémarre mon pc.

Le service ne réussira pas à se lancer pour pierre qui est sous windows 8 après 1h30 de tentative de fix le problème, mais moi en w10 j'aurais mon service qui marchera.

On continue donc en faisant comme si ça marchais pour Pierre et en simulant. ( on en a parlé discord )

### 2. Configuration du routage

#### PC1

Pierre tape dans le powershell route 192.168.102.10/24 mask 255.255.255.0 192.168.112.2

#### PC2

Je fais l&#39;opération inverse soit route add 192.168.101.1/24 mask 255.255.255.0 192.168.112.1

Le cmd répond : OK !

Je réussit donc à le ping

#### VM2

Je tape donc
![alt text](https://github.com/MathieuCaselles/b1-tp3/blob/master/screen/14.png)  

Les ping en theorie sont donc censé marcher puisque nous avons ajouté les routes pour qu&#39;ils le puissent

### 3. Configuration des noms de domaine

Pour changer le nom de domaine je tape nano /etc/hosts

Et j&#39;ajoute les ip et je met comme hostname vm et domaine tp3.b1

Je fais de meme pour le reste

Sur windows je vais dans C:\Windows\System32\drivers\etc et j&#39;ajoute l&#39;ip le hostname pc et domaine tp3.b1

Je fais de même pour le reste et ajoute à chaque fois les 4

![alt text](https://github.com/MathieuCaselles/b1-tp3/blob/master/screen/15.png)  
Cela fonctionne donc les fichiers hosts sont donc bien configurés
