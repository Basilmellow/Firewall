 Project Description
This project involves building and configuring a firewall on a Linux operating system using UFW (Uncomplicated Firewall).
The firewall will be designed to monitor and control incoming and outgoing network traffic based on predetermined security rules.
The project also includes advanced configurations such as logging, setting default policies, and using application profiles.

 Technologies Used
- Operating System: Linux
- Firewall Software: UFW (Uncomplicated Firewall)
- Tools: Terminal, SSH

 Installation Instructions

 Prerequisites
1. Operating System**: Ensure you are running a Linux distribution (e.g., Ubuntu 20.04)
2. Software Dependencies**: Install UFW
  
   sudo apt-get update
   sudo apt-get install -y ufw
   

  Setup
1. Enable UFW
   
   sudo ufw enable
   

2. Allow Necessary Services and Ports
  
   sudo ufw allow ssh
   sudo ufw allow 80/tcp   # HTTP
   sudo ufw allow 443/tcp  # HTTPS
  

3. Deny Unnecessary Services and Ports
   
   sudo ufw deny 23/tcp    # Telnet
   sudo ufw deny 21/tcp    # FTP
   

4. Advanced Configuration
   - Logging
     
     sudo ufw logging on
     
   - Default Policies
     
     sudo ufw default deny incoming
     sudo ufw default allow outgoing
     
   - Application Profiles
     Create or edit application profiles in `/etc/ufw/applications.d/`.

5. Test Firewall for Open Ports
   Use tools like `nmap` to scan and verify the firewall configuration.
   
   sudo apt-get install -y nmap
   nmap -v your_server_ip
  

 Usage
 Basic Commands
- Enable UFW
  
  sudo ufw enable
  
- Disable UFW
  
  sudo ufw disable
  
- Check Status
 
  sudo ufw status
  
- Allow a Service or Port
  
  sudo ufw allow <service/port>
  
- Deny a Service or Port
  
  sudo ufw deny <service/port>
  

Contributing
If you would like to contribute to this project, please fork the repository and submit a pull request with your changes.

License
This project is licensed under the MIT License.
