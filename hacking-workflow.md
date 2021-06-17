
# Ransomware-Leselinks



- https://zero.bs/ransomware-vs-infrastruktur-de.html
- https://zero.bs/ransomware-operations-part-1-intro.html part 1 - 4
- https://www.zdnet.com/article/heres-a-list-of-all-the-ransomware-gangs-who-will-steal-and-leak-your-data-if-you-dont-pay/
- https://www.intel471.com/blog/revil-ransomware-interview-russian-osint-100-million
- https://therecord.media/i-scrounged-through-the-trash-heaps-now-im-a-millionaire-an-interview-with-revils-unknown/
- https://cybernews.com/security/how-we-applied-to-work-with-ransomware-gang/




# Recon + Weaponizing


## Domain -> IP -> RZ


~~~

host spiegel.de

spiegel.de has address 128.65.210.8
spiegel.de mail is handled by 0 spiegel-de.mail.protection.outlook.com.


~~~

- bgp.he-net -> translate IP to AS/RZ
- https://bgp.he.net/ip/128.65.210.8
- shodan, binaryedge



## Domain -> Subdomain -> Appliances and Software

- dnsdumpster https://dnsdumpster.com/
- certificate-db https://crt.sh
- passivedns https://securitytrails.com/


## RZ-AttackSurface & internet wide scans

- Shodan https://shodan.io
- Binaryedge https://app.binaryedge.io/
- Luup https://luup.zero.bs
- censys https://censys.io/ipv4
- cysmo https://cysmo.de

- rapid7 (formerly scans.io) https://opendata.rapid7.com/

## Exploits 

- F5 BigIP CVE-2020-5902
- CiscoASA CVE-2020-3452



## Persistenz & priviledge escalation (DomainAdmin)


- [mimikatz](https://blog.varonis.de/was-ist-mimikatz-eine-einfuhrung/)
- [bloodhound](https://www.pentestpartners.com/security-blog/bloodhound-walkthrough-a-tool-for-many-tradecrafts/)
- [Darknet.org: Bloodhound](https://www.darknet.org.uk/2019/06/bloodhound-hacking-active-directory-trust-relationships/)

## vertical movement

- [dns takeover](https://blog.fox-it.com/2018/01/11/mitm6-compromising-ipv4-networks-via-ipv6/)
- [arp poisoning](https://en.wikipedia.org/wiki/ARP_spoofing)

## Tools und Dojos

- [OverTheWire](https://overthewire.org/wargames/)
- [HackTheBox](https://www.hackthebox.eu/)
- [CompassSecurity HackingLab](https://compass-security.com/de/produkte/hacking-lab)
- [EU CyberSecurityChallenge](https://compass-security.com/de/news/detail/cyber-security-challenge-germany)

# physical

- [bashbunny](https://shop.hak5.org/products/bash-bunny)

- [opening doors](https://www.youtube.com/watch?v=SDl4AO4ancI)
- [entry gate and ladder ](https://www.youtube.com/watch?v=LQCEshM03IY)
- [I'll Let Myself In: Tactics of Physical Pen Tester](https://www.youtube.com/watch?v=rnmcRTnTNC8)
- [You’re Probably Not Red Teaming... And Usually I’m Not, Either](https://www.youtube.com/watch?v=mj2iSdBw4-0)

# filme & social engineering

- [takedown](https://www.youtube.com/watch?v=md-3lzwqeek)
- [the kgb the computer and me](https://www.youtube.com/watch?v=EcKxaq1FTac)
- [APT-Operations by gruq](https://www.youtube.com/watch?v=wP2J9aYM6Oo)
- [Gebäudesicherheit](https://www.youtube.com/watch?v=rnmcRTnTNC8)


# wifi

- Ticonderoga - attack
  - campus-attack
  - wifi-recon
  - building a custom attack-module with raspi and drone
  - test attack- sizing with a partner
  - fire in the whole!  


# credentialstuffing


- bundestag.de.list



# scans

~~~

bigip 
./nuclei_scan.py CVE-2021-22986 f5_bigip_rce-big_ip_all.list-2021-02-08.ips.ports

vmware
./nuclei_scan.py CVE-2021-21985 vmware_vcenter_rce-b71ad3c6-vcenter_all.gz-2021-05-31.ips.ports

cisco 
./nuclei_scan.py cve-2020-3452 cisco_asa_fileread_vulnscan-cisco_asa_latest.list-2021-02-08.ips.ports

solr
./nuclei_scan.py CVE-2021-27905 apache_solr-391e8612-solr.gz-2021-06-15.ips.ports

weblogic
./nuclei_scan.py CVE-2020-14882 weblogic_attack-oracle_weblogic.list-2021-02-12.ips.ports


~~~
