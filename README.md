# not-a-netstat
## Goals
1. modify netstat (Linux program to list connections) so that it initiates a reverse shell on user activation
2. conceals our network process from results
3. replace existing binary

## Process involved
1. Download the netstat source code and set up the environment for compilation.
2. Edit the netstat.c file and implement the backdoor function.
3. Compile the modified code to generate the Trojan netstat binary.
4. Integrate the backdoor function into the main function of the netstat code.
5. Modify the TCP function to hide connections to the Trojan server from the netstat output.
6. Test the Trojan netstat functionality, including both normal and root user executions.
7. Verify the non-malicious detection of the Trojan binary by scanning it with [VirusTotal](https://www.virustotal.com/gui/home/upload).
8. Replace the original netstat binary with the Trojan version.