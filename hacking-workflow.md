


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



# wifi

- Ticonderoga - attack
  - campus-attack
  - wifi-recon
  - building a custom attack-module with raspi and drone
  - test attack- sizing with a partner
  - fire in the whole!  


# credentialstuffing


- bundestag.de.list



#addix

~~~

if in_type == "b":
  jq_cmd_raw = " | jq .target.ip"
  jq_cmd_ports = """ | jq ' .target.ip + "|" + "\(.target.port)" + "|" + "\(.origin.ts)" + "|" + .result.data.request.url '"""
elif in_type == "s":
  jq_cmd_raw = " | jq .ip_str"
  jq_cmd_ports = """ | jq ' .ip_str + "|" + "\(.port)" + "|" + .timestamp + "|" + .result.data.request.url ' """
elif in_type == "p":
  jq_cmd_raw = ""
  jq_cmd_ports = ""


~~~



