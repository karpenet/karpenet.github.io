### Step 1: Install SSH Server on Home Ubuntu Computer
1. Open a terminal on your home Ubuntu computer.
2. Install the OpenSSH server:
    ```
    sudo apt update
    sudo apt install openssh-server
    ```

### Step 2: Configure Your Router for Port Forwarding
1. Log in to your router's web interface. This is usually done by typing the router's IP address into a web browser (e.g., 192.168.1.1 or 192.168.0.1).
2. Find the Port Forwarding section. This may be under "Advanced," "Firewall," or "NAT" settings.
3. Add a new port forwarding rule:
    - Service Name: SSH
    - External Port: 22
    - Internal Port: 22
    - Internal IP Address: The local IP address of your Ubuntu machine (e.g., 192.168.1.100)
    - Protocol: TCP

### Step 3: Find Your Home IP Address
1. Visit a website like WhatIsMyIP from your home Ubuntu machine to find your public IP address.

### Step 4: Configure SSH on Work Computer
1. In a terminal on your work computer use the following command to connect to your home computer:
    ```
    ssh username@your_home_ip
    ```

### Step 5 [Optional]: Setup SSH Key Authentication
1. Generate an SSH key pair on your work computer:
    ```
    ssh-keygen
    ```
2. Copy the public key to your home Ubuntu computer:
    ```
    ssh-copy-id -F key_path username@your_home_ip
    ```

### Step 6 [Optional]: Add SSH Config
1. In a terminal on your work computer edit (or create if it doesn't exist) the SSH configuration file:
    ```
    vim ~/.ssh/config
    ```
2. Add the following lines to the ~/.ssh/config file:
    ```
    Host <host_alias> # Choose your own name
    HostName <host_ip_address>
    User <user_name_on_host>
    Port 22  # Change this if you have configured SSH to use a different port
    ```
3. In the terminal, simply type:
    ```
    ssh host_alias
    ```
    This should connect you to your home Ubuntu computer without needing to specify the username and IP address each time.