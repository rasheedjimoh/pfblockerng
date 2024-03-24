# DNS Security with pfBlockerNG + unbound

## Introduction
Today, let's dive into setting up a robust DNS security and ad-blocking solution using pfBlockerNG and unbound. This powerful combination not only enhances your network security but also ensures a seamless browsing experience by blocking those pesky ads.

![dnsbl-block stat](https://github.com/rasheedjimoh/pfblockerng/assets/157264080/485ee5c3-d6a9-44cf-a605-10ad163207cd)

## Why We Need It

Implementing DNS security with pfBlockerNG and unbound is essential for several reasons, including:

1. **Enhanced Network Security:**
   - By blocking malicious domains and ads at the DNS level, pfBlockerNG and unbound provide an additional layer of security for your network. This helps prevent access to potentially harmful websites and reduces the risk of malware infections and data breaches.

2. **Ad Blocking and Improved Browsing Experience:**
   - pfBlockerNG's ad-blocking capabilities ensure a smoother and more enjoyable browsing experience by eliminating intrusive ads and pop-ups. This not only enhances user productivity but also reduces the risk of accidental clicks on malicious advertisements.

3. **Protection Against DNS-Based Threats:**
   - DNS-based threats, such as DNS hijacking and DNS spoofing, pose significant risks to network security. By actively blocking malicious domains and enforcing secure DNS resolution, pfBlockerNG and unbound mitigate these threats and protect against DNS-related attacks.

4. **Customizable Security Policies:**
   - With pfBlockerNG, users have the flexibility to customize security policies according to their specific requirements. From enabling wildcard blocking to configuring Python Regex blocking rules, administrators can tailor the security setup to align with their network's unique needs and priorities.

5. **Continuous Monitoring and Updates:**
   - pfBlockerNG's Resolver Live Sync feature ensures continuous functionality by synchronizing DNSBL configurations in real-time. This allows for seamless updates and ensures that the security measures remain effective against emerging threats.

6. **Comprehensive Threat Intelligence Integration:**
   - By leveraging threat intelligence feeds and blacklists, pfBlockerNG enhances its blocking capabilities and stays up-to-date with the latest security threats. This proactive approach to threat intelligence integration ensures comprehensive protection against a wide range of malicious activities.

In summary, implementing DNS security with pfBlockerNG and unbound is essential for safeguarding network integrity, enhancing user privacy, and mitigating DNS-related threats. By blocking malicious domains and ads, organizations can create a safer and more secure browsing environment for all network users.

---

## Procedure / Process
Here's a step-by-step guide to get you started:

1. **Access Package Manager**: Begin by navigating to Package Manager under Systems in your pfSense interface.

2. **Download pfBlockerNG**: Search for pfBlockerNG and download it from the available packages.

3. **Enable Kill State**: To ensure smooth operation, enable kill state to restart all DNS queries effectively.

4. **Configure IP Interfaces**: In the IP interface section, set Inbound Firewall Rules as WAN and LAN interface as Outbound Firewall Rules.

![pfblockerng - stat](https://github.com/rasheedjimoh/pfblockerng/assets/157264080/dc05c402-c9bc-4603-a73e-9594b23f5dc0)


5. **Optimize DNSBL Mode**: Change DNSBL mode to "unbound python mode" for faster and more efficient service.

6. **Enable Wildcard Blocking**: Activate "Wildcard Blocking (TLD)" to block all subdomains of blacklisted domains.

7. **Resolver Live Sync**: Ensure continuous functionality by enabling Resolver Live Sync, which maintains operation during updates or CRON jobs.

8. **DNSBL Python Blocking Mode**: Enable DNSBL python blocking mode to handle domains not blocked via DNSBL effectively.

![dnsbl-reply stat](https://github.com/rasheedjimoh/pfblockerng/assets/157264080/13ec9e64-9e48-40ef-8e37-a1b2316dc8cb)


9. **Python Regex Blocking**: Activate the Python Regex blocking feature and customize the Regex list according to your preferences.

10. **DNSBL Python Null Block Mode for HSTS Domains**: Enable the Null Block Mode for HSTS domains to prevent browser certificate errors.

11. **CNAME Validation**: Enhance security by enabling Python CNAME Validation, which evaluates all CNAMES against the DNSBL database.

12. **Python Group Policy Functionality**: Allow certain Local LAN IPs to bypass DNSBL by enabling Python Group Policy functionality.

13. **Action Configuration**: Set the action to Deny Both on the blocklist for comprehensive security.

![pfblockerng - alerts](https://github.com/rasheedjimoh/pfblockerng/assets/157264080/04efa3ff-730b-4fb6-9ccb-735b281f37b1)


14. **DNSBL Configuration**: Select Unbound to enable 'Domain Name' blocking for this Alias.

15. **DoH/DoT/DoQ Blocking**: Enable blocking for DNS over HTTPS (DoH), DNS over TLS (DoT), and DNS over QUIC (DoQ) by selecting all providers in the blocking list.

16. **Site Blocking Example**: As a demonstration, block "*.cnn.com" to showcase site blocking capabilities.

![dnsbl - blocked cnn](https://github.com/rasheedjimoh/pfblockerng/assets/157264080/8210ced5-5aa0-4a0d-b5c3-2d22323f7533)

By following these steps, you'll create a robust DNS security and ad-blocking setup using pfBlockerNG and unbound. Enjoy a safer and ad-free browsing experience for all your network users!

## Conclusion

In conclusion, setting up DNS security with pfBlockerNG and unbound is a crucial step towards enhancing network security and improving the browsing experience for users. By following the outlined steps, organizations can create a robust ad-blocking and DNS security solution that effectively protects against malicious threats while ensuring seamless access to legitimate websites.

Happy networking!
Stay proactive, stay secure!
