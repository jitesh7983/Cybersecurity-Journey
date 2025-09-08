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


