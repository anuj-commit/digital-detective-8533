# Mission 7 - Networking and the internet

## 1. Task / objective

Learn common network terms, use Terminal to check a public domain and local routing, and explain what happens when a browser opens a website.

## 2. Work completed

### Task 7.1 - Network concepts

| Concept | My explanation | Example |
|---|---|---|
| LAN | Connects devices in a small area. | Devices on a home network. |
| MAN | Covers a larger area such as a city or campus. | A network connecting buildings across a campus. |
| WAN | Connects networks over long distances. | The internet. |
| IP address | A number used to identify a device or service on a network so data can be sent to it. | A router forwards traffic toward the IP address for a website. |
| DNS | Looks up the IP address associated with a domain name. | Looking up `example.com` before the browser connects. |
| Router | Forwards traffic between networks, using a route toward the destination. | A home router passes traffic between the local network and the internet. |
| Protocol | Agreed rules for sending and receiving data. | HTTP or HTTPS for web pages. |
| Packet switching | Breaks data into packets that can travel through a network and be put back together. | A web page response arrives as packets. |
| Client-server | The client requests something and the server sends a response. | A browser asks a web server for a page. |

### Task 7.2 - Network checks

I ran `ping -c 4 example.com`. The four packets came back, with 0% packet loss. The average round-trip time in this run was about 61 ms. This checks whether the domain could be reached by the ping test at that moment; it does not prove every part of a website is working.

`nslookup example.com` returned two address records in this run:

```text
Name:    example.com
Address: 104.20.23.154
Name:    example.com
Address: 172.66.147.243
```

These are public addresses for the example domain, not my computer's address. A DNS lookup asks a DNS server to translate a name into one or more network addresses. The answers can vary over time or by location.

I also checked the local connection and routing. `route -n get default` showed that the default route uses interface `en0`; the gateway address is `[redacted]`. `ipconfig getifaddr en0` returned my local address, which is `[redacted]`. I did not include the local route table because it contains local addresses and hardware details.

### Task 7.3 - What happens when I open a website

1. I enter a website name in the browser. The browser is the client and prepares a request for the site.
2. DNS looks up the name and returns an IP address for the server.
3. The computer sends network packets toward that address. The router forwards them from the local network toward the internet.
4. The browser uses HTTP to request the page. With HTTPS, the connection is protected with TLS while the request and response travel between the client and server.
5. The server processes the request and sends back a response, such as page text, images or other files.
6. The packets return to the computer, and the browser puts the response together and displays the page.

## 3. Commands / tools used

- `ping -c 4 example.com` - sent four connectivity checks to the example domain.
- `nslookup example.com` - looked up the domain's DNS address records.
- `route -n get default` - checked the default route and network interface; the local gateway address is redacted.
- `ipconfig getifaddr en0` - checked the local address for the interface; the result is redacted.
- `netstat -rn -f inet` - viewed the local IPv4 routing table; I left out entries that showed local addresses or hardware details.

## 4. My understanding

An IP address lets network traffic be directed to a device or service. DNS means I can use a readable domain name and have it looked up as an address. The router moves packets toward other networks, and packet switching means the parts of a response can travel as separate packets before the computer puts them back together.

HTTP is the request-and-response protocol used by a browser and web server. HTTPS adds TLS protection for the connection. The browser is the client, and the computer answering the request is the server.

## 5. Difficulties faced

My first `ping` attempt said it could not resolve `example.com`, and `nslookup` showed an “operation not permitted” message. I was not sure whether the domain was down or the lookup was being blocked.

## 6. How I resolved them

I checked the error and retried the read-only network commands when Terminal could access the network. `nslookup` then returned the domain's addresses, and `ping -c 4 example.com` received all four replies with no packet loss. I kept my local IP address and gateway redacted in these notes.

## 7. Evidence / files

- This README contains the network terms, privacy-safe command observations and website steps.
- My local IP address and gateway are shown as `[redacted]`; no Wi-Fi name, MAC address, device name or serial number is included.

## 8. Commit details

- Commit message: `Explain networking concepts and website communication`
- Status: committed locally on `main`; not pushed to GitHub.
