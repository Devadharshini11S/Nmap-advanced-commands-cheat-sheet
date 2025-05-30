


ADVANCED NMAP COMMANDS CHEAT SHEET (WITH EXPLANATIONS)

Table of Contents

1. Basic Scanning
                 2. Port Scanning Techniques
                     3. Service & Version Detection
4. OS Detection   
              5. Timing and Performance
        6. Firewall/IDS Evasion
                      7. Nmap Scripting Engine (NSE)
8. Output Options
                  9. Miscellaneous & Advanced


1. Basic Scanning

1. `nmap 192.168.1.10`  
   Default TCP SYN scan on target.

2. `nmap -v 192.168.1.10`  
   Verbose output.

3. `nmap -Pn 192.168.1.10`  
   Skip host discovery (treat host as online).

4. `nmap -n 192.168.1.10`  
   No DNS resolution.

5. `nmap -sS 192.168.1.10`  
   TCP SYN stealth scan.

6. `nmap -sT 192.168.1.10`  
   TCP connect scan (non-stealth).

7. `nmap -sU 192.168.1.10`  
   UDP scan.

8. `nmap -sN 192.168.1.10`  
   TCP Null scan.

9. `nmap -sF 192.168.1.10`  
   FIN scan.

10. `nmap -sX 192.168.1.10`  
    Xmas scan (sets FIN, PSH, URG flags).


2. Port Scanning Techniques

11. `nmap -p 80,443 192.168.1.10`  
    Scan specific ports.

12. `nmap -p- 192.168.1.10`  
    Scan all 65535 TCP ports.

13. `nmap -F 192.168.1.10`  
    Fast scan (top 100 ports).

14. `nmap --top-ports 50 192.168.1.10`  
    Scan top 50 most common ports.

15. `nmap -r 192.168.1.10`  
    Scan ports in order (no randomization).

16. `nmap --exclude-ports 22,80 192.168.1.10`  
    Scan all ports except 22 and 80.

17. `nmap --exclude 192.168.1.11 192.168.1.10-20`  
    Scan range except one host.

18. `nmap --max-retries 1 192.168.1.10`  
    Reduce retries to speed scan.

19. `nmap --min-rate 1000 192.168.1.10`  
    Send packets at minimum rate of 1000/sec.

20. `nmap -sV -p- 192.168.1.10`  
    Service version detection on all ports.


3. Service & Version Detection

21. `nmap -sV 192.168.1.10`  
    Service/version detection.

22. `nmap --version-intensity 0 192.168.1.10`  
    Light version detection (faster).

23. `nmap --version-all 192.168.1.10`  
    Try every version detection probe (slow).

24. `nmap --version-light 192.168.1.10`  
    Use only most reliable version probes.

25. `nmap --version-trace 192.168.1.10`  
    Show version detection debugging info.

4. OS Detection

26. `nmap -O 192.168.1.10`  
    Enable OS detection.

27. `nmap --osscan-limit 192.168.1.10`  
    Skip OS detection on hosts without open ports.

28. `nmap --osscan-guess 192.168.1.10`  
    Guess OS if detection is inconclusive.

29. `nmap -A 192.168.1.10`  
    Enable OS detection + version detection + scripts + traceroute.

30. `nmap --fuzzy 192.168.1.10`  
    Use fuzzy logic for OS detection.

 5. Timing and Performance

31. `nmap -T0 192.168.1.10`  
    Paranoid timing (slowest, stealthiest).

32. `nmap -T1 192.168.1.10`  
    Sneaky timing.

33. `nmap -T2 192.168.1.10`  
    Polite timing (reduce load).

34. `nmap -T3 192.168.1.10`  
    Normal timing (default).

35. `nmap -T4 192.168.1.10`  
    Aggressive timing.

36. `nmap -T5 192.168.1.10`  
    Insane timing (fastest, less reliable).

6. Firewall/IDS Evasion

37. `nmap -D RND:5 192.168.1.10`  
    Use 5 random decoy IPs.

38. `nmap -D 192.168.1.100,192.168.1.101 192.168.1.10`  
    Use specified decoys.

39. `nmap -f 192.168.1.10`  
    Fragment packets.

40. `nmap --mtu 24 192.168.1.10`  
    Set MTU size.

41. `nmap --spoof-mac 00:11:22:33:44:55 192.168.1.10`  
    Spoof MAC address.

42. `nmap --ttl 10 192.168.1.10`  
    Set IP TTL value.

43. `nmap --data-length 50 192.168.1.10`  
    Append 50 bytes random data to packets.

7. Nmap Scripting Engine (NSE)

44. `nmap --script default 192.168.1.10`  
    Run default NSE scripts.

45. `nmap --script vuln 192.168.1.10`  
    Run vulnerability detection scripts.

46. `nmap --script "http-* and safe" 192.168.1.10`  
    Run safe HTTP scripts.

47. `nmap --script ssh-auth-methods 192.168.1.10`  
    Check SSH authentication methods.

48. `nmap --script smb-vuln-ms17-010 192.168.1.10`  
    Check for MS17-010 SMB vulnerability.

49. `nmap --script dns-zone-transfer 192.168.1.10`  
    Attempt DNS zone transfer.

50. `nmap --script ftp-anon 192.168.1.10`  
    Check for anonymous FTP access.

8. Output Options

51. `nmap -oN output.txt 192.168.1.10`  
    Save normal output.

52. `nmap -oX output.xml 192.168.1.10`  
    Save XML output.

53. `nmap -oG output.gnmap 192.168.1.10`  
    Save grepable output.

54. `nmap -oA output 192.168.1.10`  
    Save in all formats (normal, XML, grepable).

9. Miscellaneous & Advanced

55. `nmap --traceroute 192.168.1.10`  
    Trace network path to target.

56. `nmap --reason 192.168.1.10`  
    Show reason for each port state.

57. `nmap --script-timeout 10s 192.168.1.10`  
    Set max time per script.

58. `nmap --max-parallelism 10 192.168.1.10`  
    Limit parallel probes.

59. `nmap --min-hostgroup 256 192.168.1.10-20`  
    Minimum hosts scanned in parallel.

60. `nmap --max-hostgroup 256 192.168.1.10-20 
Max hosts scanned in parallel.


