# DNS Security with pfBlockerNG + unbound

Today, let's dive into setting up a robust DNS security and ad-blocking solution using pfBlockerNG and unbound. This powerful combination not only enhances your network security but also ensures a seamless browsing experience by blocking those pesky ads.

Here's a step-by-step guide to get you started:

1. **Access Package Manager**: Begin by navigating to Package Manager under Systems in your pfSense interface.

2. **Download pfBlockerNG**: Search for pfBlockerNG and download it from the available packages.

3. **Enable Kill State**: To ensure smooth operation, enable kill state to restart all DNS queries effectively.

4. **Configure IP Interfaces**: In the IP interface section, set Inbound Firewall Rules as WAN and LAN interface as Outbound Firewall Rules.

5. **Optimize DNSBL Mode**: Change DNSBL mode to "unbound python mode" for faster and more efficient service.

6. **Enable Wildcard Blocking**: Activate "Wildcard Blocking (TLD)" to block all subdomains of blacklisted domains.

7. **Resolver Live Sync**: Ensure continuous functionality by enabling Resolver Live Sync, which maintains operation during updates or CRON jobs.

8. **DNSBL Python Blocking Mode**: Enable DNSBL python blocking mode to handle domains not blocked via DNSBL effectively.

9. **Python Regex Blocking**: Activate the Python Regex blocking feature and customize the Regex list according to your preferences.

10. **DNSBL Python Null Block Mode for HSTS Domains**: Enable the Null Block Mode for HSTS domains to prevent browser certificate errors.

11. **CNAME Validation**: Enhance security by enabling Python CNAME Validation, which evaluates all CNAMES against the DNSBL database.

12. **Python Group Policy Functionality**: Allow certain Local LAN IPs to bypass DNSBL by enabling Python Group Policy functionality.

13. **Action Configuration**: Set the action to Deny Both on the blocklist for comprehensive security.

14. **DNSBL Configuration**: Select Unbound to enable 'Domain Name' blocking for this Alias.

15. **DoH/DoT/DoQ Blocking**: Enable blocking for DNS over HTTPS (DoH), DNS over TLS (DoT), and DNS over QUIC (DoQ) by selecting all providers in the blocking list.

16. **Site Blocking Example**: As a demonstration, block "*.cnn.com" to showcase site blocking capabilities.

By following these steps, you'll create a robust DNS security and ad-blocking setup using pfBlockerNG and unbound. Enjoy a safer and ad-free browsing experience for all your network users!

Stay tuned for more tech tips and tricks on my professional blog.

Happy networking!
