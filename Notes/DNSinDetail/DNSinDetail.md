# 🌍 DNS (Domain Name System)

DNS provides a simple way to communicate with devices on the internet without remembering complex IP addresses.  
Instead of remembering `104.26.10.229`, you can just type `tryhackme.com`.

---

## 🏷 Domain Hierarchy
![DNS Hierarchy](images/DomainHierarchy.png)

- **TLD (Top Level Domain)** → The right-most part of a domain.  
  - Example: `tryhackme.com` → `.com`  
  - Types:  
    - **gTLD (Generic)** → `.com`, `.org`, `.edu`, `.gov`  
    - **ccTLD (Country Code)** → `.in`, `.uk`, `.ca`  

- **Second-Level Domain (SLD)** → Appears before the TLD.  
  - Example: `tryhackme` in `tryhackme.com`  

- **Subdomain** → Placed before the SLD.  
  - Example: `admin` in `admin.tryhackme.com`

---

✅ **Summary**:  
- DNS = maps domain names → IP addresses  
- Domain hierarchy = TLD → SLD → Subdomain

---

# DNS Records  

DNS isn’t just for websites — multiple record types exist.  

---

### 🔹 Common DNS Record Types  

- **A Record**  
  Maps a domain to an **IPv4 address**.  
  Example: `104.26.10.229`  

- **AAAA Record**  
  Maps a domain to an **IPv6 address**.  
  Example: `2606:4700:20::681a:be5`  

- **CNAME Record**  
  Alias of another domain.  
  Example: `store.tryhackme.com → shops.shopify.com`  

- **MX Record**  
  Specifies **mail servers** for a domain, with priority for failover.  
  Example: `alt1.aspmx.l.google.com`  

- **TXT Record**  
  Free text data.  
  Common uses:  
  - Email security (SPF, DKIM)  
  - Domain ownership verification  

---
# What Happens When You Make a DNS Request  

When you request a domain, the lookup follows a series of steps until the IP is resolved:  

---

### 🔹 Steps in DNS Resolution  

1. **Local Cache Check**  
   - Your computer checks its own DNS cache.  
   - If found → returns immediately.  

2. **Recursive DNS Server**  
   - Usually provided by your ISP (can be Google, Cloudflare, etc.).  
   - Checks its cache.  
   - If not found → queries further.  

3. **Root DNS Servers**  
   - Act as the **backbone of the internet**.  
   - Direct the query to the appropriate **Top Level Domain (TLD) server**.  
   - Example: `.com`, `.org`, `.net`.  

4. **TLD DNS Servers**  
   - Provide the location of the **Authoritative Nameserver** for the domain.  
   - Example: for `tryhackme.com` → `kip.ns.cloudflare.com`, `uma.ns.cloudflare.com`.  

5. **Authoritative DNS Server**  
   - Holds the **actual DNS records** (A, MX, CNAME, etc.).  
   - Returns the final IP address.  

6. **Response & Caching**  
   - The Recursive DNS Server caches the record (for **TTL** seconds).  
   - Returns the answer to your computer.  
   - Caching avoids repeated lookups for the same domain.  

---

### 🔹 Diagram  

*(Add diagram here showing: Client → Recursive DNS → Root → TLD → Authoritative → Back to Client)*  

---

📌 **Key Term:**  
- **TTL (Time To Live):** Value (in seconds) that specifies how long the record is cached before expiring.  


📌 These records are the backbone of how domains resolve to IPs, mail servers, and services.




