# pfSense OpenVPN & CasaOS Lab 🚀
​A secure OpenVPN implementation using pfSense in a VirtualBox environment, bridged through an MTN ISP Router. This setup enables encrypted remote access to CasaOS and secure web browsing via a full-tunnel VPN.


## ​🌐 Network Topology
​Public Internet → MTN Router (Port Forwarding UDP 1194)
​pfSense WAN (192.168.0.143) → Tunnel Network (10.0.8.0/24)
​DDNS: DuckDNS integration for dynamic IP tracking


## ​🛠️ Key Configurations
​Outbound NAT: Hybrid mode with manual mapping for 10.0.8.0/24 to enable internet access.
​Firewall: OpenVPN "Pass Any" rule and disabled "Block Private Networks" on WAN.
​Redirect Gateway: Forced all client traffic through the tunnel for secure remote browsing.
​DNS: Pushed Google (8.8.8.8) and Cloudflare (1.1.1.1) DNS to clients.


## ​📱 Supported Clients
​Windows: OpenVPN GUI using exported .ovpn profiles.
​Mobile: OpenVPN Connect via Inline Config exports.


## ​🧪 Testing
​Local Access: Successfully authenticated and reached CasaOS services.
​Internet Access: Verified public browsing via ping 8.8.8.8 after NAT configuration.
​DDNS: Verified remote connection using yourdomain.duckdns.org.
