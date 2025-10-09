# KeyBank Hackathon - IBM watsonx Code Assistant for Ansible

Welcome to the KeyBank Hackathon! This hands-on workshop will introduce you to **IBM watsonx Code Assistant for Red Hat Ansible Lightspeed**, an AI-powered tool that helps you create Ansible playbooks using natural language prompts.

---

## 📑 Table of Contents

### Pre-Hackathon Setup
1. [What You'll Learn](#1-what-youll-learn)
2. [Getting Started - Environment Setup](#2-getting-started---environment-setup)
   - [2.1 Create Your Red Hat Ansible Lightspeed Trial Account](#21-create-your-red-hat-ansible-lightspeed-trial-account)
   - [2.2 Install Git](#22-install-git)
   - [2.3 Install Visual Studio Code](#23-install-visual-studio-code)
   - [2.4 Clone the Hackathon Repository](#24-clone-the-hackathon-repository)
   - [2.5 Install the Red Hat Ansible Extension](#25-install-the-red-hat-ansible-extension)
   - [2.6 Connect to Ansible Lightspeed](#26-connect-to-ansible-lightspeed)
   - [2.7 Verify Your Setup & Pre-Hackathon Checklist](#27-verify-your-setup--pre-hackathon-checklist)

### Hackathon Exercises
3. [Workshop Exercises](#3-workshop-exercises)
   - [3.1 Warm-Up Exercise: Simple Web Server Configuration](#31-warm-up-exercise-simple-web-server-configuration)
   - [3.2 Main Exercise: End-to-End Apache Web Server Deployment](#32-main-exercise-end-to-end-apache-web-server-deployment)
     - [Exercise 1: Install and Configure httpd](#exercise-1-install-and-configure-httpd-role-1)
     - [Exercise 2: Configure httpd.conf](#exercise-2-configure-httpdconf-role-2)
     - [Exercise 3: Deploy index.html](#exercise-3-deploy-indexhtml-role-3)
   - [3.3 Exercise 4: Provision AWS EC2 Instance](#33-exercise-4-provision-aws-ec2-instance-cloud-infrastructure)

### Post-Hackathon
4. [Take-Home Optional Challenges](#4-take-home-optional-challenges)
   - [Challenge 1: PostgreSQL Database & PGAdmin Container Setup](#challenge-1-postgresql-database--pgadmin-container-setup)
   - [Challenge 2: Full Playbook Generation - RHEL Patching Workflow](#challenge-2-full-playbook-generation---rhel-patching-workflow)
5. [Additional Resources](#5-additional-resources)
6. [Hackathon Day Schedule](#6-hackathon-day-schedule)
7. [Tips for Success](#7-tips-for-success)
8. [Getting Help](#8-getting-help)
9. [Contact Information](#9-contact-information)
10. [Useful Resources](#10-useful-resources)
11. [Post-Workshop Feedback](#11-post-workshop-feedback)

---

## 1. 📋 What You'll Learn

- How to use AI to generate Ansible tasks and playbooks
- Single-task and multi-task generation with Ansible Lightspeed
- Best practices for writing Ansible playbooks with AI assistance
- Hands-on experience configuring Apache web servers using AI-generated code

---

## 2. 🚀 Getting Started - Environment Setup

### 2.1 Create Your Red Hat Ansible Lightspeed Trial Account

Before the hackathon, you **MUST** complete the following setup steps:

1. Visit the trial registration page:
   **https://www.ibm.com/products/watsonx-code-assistant-ansible-lightspeed/info/trial**

2. Click on **"Start your free trial"**

   ![Picture](images/image.png)

3. You will be directed to the Red Hat trial registration page. Click on the red **"Start Your Trial"** button to begin.

   ![Picture](images/image2.png)

   **Note:** To start this no-cost product trial, you must:
   - Have a Red Hat account (you'll be prompted to create one if you don't have one)
   - Accept the product trial terms and conditions
   - If you have previously activated this trial, you must wait at least 90 days from the last expiration date to start again

4. **Sign in** with your Red Hat credentials or **Register** for a new Red Hat account if you don't have one.

   ![Picture](images/image3.png)

5. Once registration is complete, you will see a welcome message confirming your trial activation.

   ![Picture](images/image4.png)

   **✅ Trial account created!** You now have a 60-day subscription to Red Hat® Ansible® Automation Platform with Lightspeed.

---

### 2.2 Install Git

**Git** is required to clone the hackathon repository. Follow the instructions for your operating system:

#### For Windows:

1. Download Git from: **https://git-scm.com/download/win**
2. Run the installer
3. During installation, accept the default settings (recommended)
4. Click **Install** and wait for completion
5. **Verify installation**: Open Command Prompt and type:
   ```
   git --version
   ```
   You should see something like `git version 2.x.x`

#### For macOS:

1. Open **Terminal** (Applications → Utilities → Terminal)
2. Type the following command and press Enter:
   ```
   git --version
   ```
3. If Git is not installed, macOS will prompt you to install it automatically
4. Follow the prompts to install **Command Line Developer Tools**
5. Once installed, verify by typing `git --version` again

#### For Linux:

1. Open Terminal
2. Install Git using your package manager:
   - **Ubuntu/Debian**: `sudo apt-get install git`
   - **Fedora**: `sudo dnf install git`
   - **CentOS**: `sudo yum install git`
3. Verify installation: `git --version`

---

### 2.3 Install Visual Studio Code

1. Download and install **Visual Studio Code** for your operating system:
   **https://code.visualstudio.com/download**

2. Choose the appropriate version:
   - **Windows** - Download and run the installer
   - **macOS** - Download the .dmg file and drag to Applications
   - **Linux** - Follow the instructions for your distribution

3. Launch Visual Studio Code after installation completes.

---

### 2.4 Clone the Hackathon Repository

Now you'll clone the hackathon repository directly into VS Code.

**Step 1: Open VS Code**

1. Launch **Visual Studio Code**

**Step 2: Open the Command Palette**

1. Click **View** → **Command Palette** (or press `Cmd+Shift+P` on Mac, `Ctrl+Shift+P` on Windows/Linux)
2. Type: `Git: Clone`
3. Select **Git: Clone** from the dropdown

**Step 3: Enter the Repository URL**

1. Paste this URL into the input box:
   ```
   https://github.com/baacha123/keybank-hakathon.git
   ```
2. Press **Enter**

**Step 4: Choose a Location**

1. A file browser will appear
2. Navigate to where you want to save the repository (e.g., **Desktop** or **Documents**)
3. Click **Select as Repository Destination** (or **Select Repository Location**)

**Step 5: Open the Repository**

1. VS Code will clone the repository (this may take a minute)
2. When prompted **"Would you like to open the cloned repository?"**, click **Open**
3. The repository folder will open in VS Code

**Step 6: Verify the Clone**

1. In the **left sidebar** (Explorer panel), you should see:
   - `README.md`
   - `images/` folder
   - `watsonx-code-assistant-for-ansible/` folder

**✅ Success!** You now have all the hackathon exercise files on your computer!

---

### 2.5 Install the Red Hat Ansible Extension

1. Open the Ansible extension marketplace page:
   **https://marketplace.visualstudio.com/items?itemName=redhat.ansible**

2. Click on the **Install** button on the webpage.

   ![Picture](images/image5.png)

3. Your browser will prompt you to **Open Visual Studio Code**. Click **Continue** or **Open** to proceed.

4. VS Code will open and begin installing the Red Hat Ansible extension automatically.

5. Click **Install** in VS Code to confirm the installation.

   ![Picture](images/image7.png)

6. Wait for the installation to complete. You can learn more about the extension here:
   https://marketplace.visualstudio.com/items?itemName=redhat.ansible

---

### 2.6 Connect to Ansible Lightspeed

**Step 1: Find the Ansible Extension**

1. Once the plugin is installed, look for the **Ansible icon** in the left sidebar panel of VS Code.

2. Click on the Ansible icon to open the Ansible panel.

   ![Picture](images/image8.png)

**Step 2: Connect to Lightspeed Service**

3. In the Ansible panel, click the **Connect** button.

   ![Picture](images/image8.png)

4. A popup will appear asking for permission to open an external website. This will redirect you to authenticate with your Red Hat trial credentials.

   ![Picture](images/image9.png)

5. Click **Open** to continue to the authentication page.

**Step 3: Authenticate with Red Hat**

6. On the authentication page, click **"Login with Red Hat"**.

   ![Picture](images/image10.png)

7. Log in using the **Red Hat credentials** you created in Step 1 for your 60-day trial.

8. After logging in, click **Authorize** to grant VS Code access to Ansible Lightspeed.

**Step 4: Verify Connection**

9. After clicking **Authorize**, you will be redirected back to VS Code.

   ![Picture](images/image11.png)

10. In the Ansible panel, you should now see:
    - Your Red Hat username
    - The **"Generate Playbook"** button
    - A **"Lightspeed"** indicator in the bottom-right corner of VS Code

**✅ Success!** You are now connected and ready to start generating Ansible playbooks with AI assistance.

---

### 2.7 Verify Your Setup & Pre-Hackathon Checklist

✅ **Complete by EOD October 20th, 2024:**

Please ensure all of the following are completed before the hackathon:

- [ ] **Git** installed on your laptop
- [ ] **Visual Studio Code** installed on your laptop
- [ ] **Hackathon repository** cloned from GitHub
- [ ] **Red Hat trial account** created and activated (60-day subscription)
- [ ] **Email sent** to workshop organizers confirming registration completion
- [ ] **Red Hat Ansible extension** installed in VS Code
- [ ] **Ansible Lightspeed** connected and authenticated
- [ ] **"Lightspeed" indicator** visible in the bottom-right corner of VS Code
- [ ] **"Generate Playbook" button** visible in the Ansible panel

**Having issues?** Contact the workshop organizers for assistance before the hackathon day.

---

## 3. 📚 Workshop Exercises

During the hackathon, you will complete hands-on exercises using IBM watsonx Code Assistant for Ansible Lightspeed. We'll start with a simple warm-up exercise, then move to a comprehensive Apache web server deployment.

---

### 3.1 🔰 Warm-Up Exercise: Simple Web Server Configuration

**Purpose**: Get comfortable with Ansible Lightspeed before the main exercise.

This exercise demonstrates both **single-task** and **multi-task** generation in a simple playbook.

---

#### Option A: Single-Task Generation

**Step 1: Create a New File in VS Code**

1. Open **Visual Studio Code**
2. Click **File** → **New File** (or press `Cmd+N` on Mac, `Ctrl+N` on Windows)
3. Click **File** → **Save** (or press `Cmd+S` on Mac, `Ctrl+S` on Windows)
4. Name the file: `simple-webserver.yml`
5. Choose a location on your computer to save it (e.g., create a folder called "KeyBank-Hackathon" on your Desktop)

**Step 2: Copy the Starting Template**

Copy and paste the following code into your new file:

```yaml
---
- name: Configure web servers
  hosts: all
  tasks:
    # TASK 1 - Used natural language prompt to generate syntactically correct Ansible Playbook task
    # - name: Install httpd package

    # TASK 2 - WCA suggestion uses best practices and defines file permissions, owner and group
    # - name: Copy httpd.conf.j2 template to /etc/httpd/conf/

    # TASK 3 - Ansible Lightspeed adds state: started and enabled: true based on the task description
    # - name: Start and enable httpd services
```

**Step 3: Generate TASK 1 with AI**

1. Find the line: `# - name: Install httpd package`
2. **Uncomment it** - Delete the `#` symbol and the space after it. The line should now look like:
   ```yaml
   - name: Install httpd package
   ```
3. **Click at the end of this line** (after "package")
4. **Press ENTER** on your keyboard
5. **Wait 2-3 seconds** - Ansible Lightspeed will show you a gray suggestion below
6. **Review the suggestion** - it should generate the correct Ansible code to install httpd
7. **Press TAB** to accept the suggestion
8. The AI has now written the code for you! ✨

**Step 4: Generate TASK 2**

1. Find the line: `# - name: Copy httpd.conf.j2 template to /etc/httpd/conf/`
2. **Uncomment it** - Delete the `#` symbol and space
3. **Click at the end of this line**
4. **Press ENTER**
5. **Wait for the AI suggestion** (shown in gray text below)
6. **Press TAB** to accept

**Step 5: Generate TASK 3**

1. Find the line: `# - name: Start and enable httpd services`
2. **Uncomment it** - Delete the `#` symbol and space
3. **Click at the end of this line**
4. **Press ENTER**
5. **Wait for the AI suggestion**
6. **Press TAB** to accept

**Step 6: Save Your Work**

1. Click **File** → **Save** (or press `Cmd+S` on Mac, `Ctrl+S` on Windows)

**✅ Success!** You've just created your first AI-generated Ansible playbook!

**What you'll learn**: How AI translates natural language into syntactically correct Ansible tasks with best practices.

---

#### Option B: Multi-Task Generation

**Step 1: Create a New File**

1. In VS Code, click **File** → **New File**
2. Click **File** → **Save**
3. Name the file: `simple-webserver-multi.yml`
4. Save it in the same folder as your previous file

**Step 2: Copy the Starting Template**

Copy and paste the following code:

```yaml
---
- name: Configure web servers
  hosts: webservers
  become: true

  tasks:
    # Install httpd package & Copy httpd.conf.j2 template to /etc/httpd/conf/ & Start and enable httpd service
```

**Step 3: Generate Multiple Tasks at Once**

1. Find the line starting with `# Install httpd package & Copy...`
2. **Uncomment it** - Delete the `#` symbol and space at the beginning
3. **Click at the end of this line**
4. **Press ENTER**
5. **Wait for the AI** - it will generate ALL THREE tasks at once! 🎯
6. **Press TAB** to accept all suggestions

**Step 4: Save Your Work**

1. Click **File** → **Save**

**✅ Amazing!** You just generated 3 tasks with a single prompt using the `&` separator!

**What you'll learn**: How to use the `&` separator for generating multiple related tasks in one go.

---

### 3.2 🏗️ Main Exercise: End-to-End Apache Web Server Deployment

**Purpose**: Build a production-ready Apache web server using Ansible roles and AI-generated code.

This comprehensive exercise uses **Ansible roles** to organize your playbook professionally.

---

### Exercise 1: Install and Configure httpd (Role 1)

**Step 1: Navigate to the Exercise Files**

If you haven't already, make sure the cloned repository is open in VS Code (you should have done this in section 2.4).

**Step 2: Open the Apache Exercise Folder**

1. In VS Code, in the **left sidebar** (Explorer panel), navigate to:
   - `watsonx-code-assistant-for-ansible` → `End to End complete Apache Install` → `Config`
2. You should see folders like `roles`, `demo-setup`, and files like `apacheservers.yml`

**Step 3: Navigate to the httpd Role File**

1. Click to expand: **roles** folder
2. Click to expand: **httpd** folder
3. Click to expand: **tasks** folder
4. **Click on the file**: `main.yml`
5. The file will open in the main editor area

You should see a file with commented lines starting with `#`

**Step 4: Generate Task 1 - Create Directory**

1. Find the line: `# - name: Create /ibmdata/htdocs directory root:root`
2. **Uncomment it** - Delete the `#` symbol and space. It should look like:
   ```yaml
   - name: Create /ibmdata/htdocs directory root:root
   ```
3. **Click at the end of this line** (after "root:root")
4. **Press ENTER**
5. **Wait 2-3 seconds** - you'll see gray text appear (this is the AI suggestion)
6. **Review the code** - the AI will generate the `ansible.builtin.file` module with proper parameters
7. **Press TAB** to accept
8. ✅ Task 1 complete!

**Step 5: Generate Task 2 - Install httpd**

1. Find the line: `# - name: Install httpd`
2. **Uncomment it** - Delete the `#` symbol and space
3. **Click at the end of the line** (after "httpd")
4. **Press ENTER**
5. **Wait for the gray suggestion**
6. **Press TAB** to accept
7. ✅ Task 2 complete!

**Step 6: Generate Task 3 - Configure SELinux Port**

1. Find the line: `# - name: Configure seport to listen on tcp 8080 and 8443 using community.general.seport`
2. **Uncomment it** - Delete the `#` symbol and space
3. **Click at the end of the line**
4. **Press ENTER**
5. **Wait for the suggestion** - notice how the AI understands "using community.general.seport" and uses that specific module!
6. **Press TAB** to accept
7. ✅ Task 3 complete!

**Step 7: Generate Task 4 - Enable httpd at Boot**

1. Find the line: `# - name: Enable httpd to start at boot`
2. **Uncomment it** - Delete the `#` symbol and space
3. **Click at the end of the line**
4. **Press ENTER**
5. **Wait for the suggestion**
6. **Press TAB** to accept
7. ✅ Task 4 complete!

**Step 8: Generate Task 5 - Open Firewall Ports**

1. Find the line: `# - name: Open firewall ports 8080 & 8443`
2. **Uncomment it** - Delete the `#` symbol and space
3. **Click at the end of the line**
4. **Press ENTER**
5. **Wait for the suggestion**
6. **Press TAB** to accept
7. ✅ Task 5 complete!

**Step 9: Save Your Work**

1. Click **File** → **Save** (or press `Cmd+S` / `Ctrl+S`)
2. You should see the dot on the file tab disappear (this means it's saved)

**✅ Exercise 1 Complete!** You've just created the httpd installation role with AI!

**What you'll learn**: Single-task generation where AI creates individual Ansible tasks from natural language prompts.

### Exercise 2: Configure httpd.conf (Role 2)

**Step 1: Open the httpd.conf Tasks File**

1. In the **left sidebar** (Explorer), navigate to: **roles** → **httpd.conf** → **tasks**
2. **Click on**: `main.yml`
3. The file opens showing 3 commented tasks

**Step 2: Generate Task 1 - Create Log Directory**

1. Find the line: `# - name: Create /var/log/httpd directory owned by root:root with 0750 permissions`
2. **Uncomment it** - Delete the `#` symbol and space
3. **Click at the end of the line**
4. **Press ENTER**
5. **Wait for the AI suggestion** - notice how it understands the ownership (root:root) and permissions (0750)!
6. **Press TAB** to accept
7. ✅ Task 1 complete!

**Step 3: Generate Task 2 - Deploy Template**

1. Find the line: `# - name: Create httpd.conf from a template and save as /etc/httpd/conf/httpd.conf`
2. **Uncomment it** - Delete the `#` symbol and space
3. **Click at the end of the line**
4. **Press ENTER**
5. **Wait for the AI** - it will use the `ansible.builtin.template` module
6. **Press TAB** to accept
7. ✅ Task 2 complete!

**Step 4: Generate Task 3 - Start httpd**

1. Find the line: `# - name: Start httpd`
2. **Uncomment it** - Delete the `#` symbol and space
3. **Click at the end of the line**
4. **Press ENTER**
5. **Wait for the suggestion**
6. **Press TAB** to accept
7. ✅ Task 3 complete!

**Step 5: Save Your Work**

1. Click **File** → **Save**

---

**Step 6: Create the Handler**

1. In the **left sidebar**, navigate to: **roles** → **httpd.conf** → **handlers**
2. **Click on**: `main.yml`
3. You'll see a commented line for the handler

**Step 7: Generate the Restart Handler**

1. Find the line: `# - name: Restart httpd`
2. **Uncomment it** - Delete the `#` symbol and space
3. **Click at the end of the line**
4. **Press ENTER**
5. **Wait for the AI** - it will create a systemd service restart task
6. **Press TAB** to accept
7. ✅ Handler complete!

**Step 8: Save Your Work**

1. Click **File** → **Save**

**✅ Exercise 2 Complete!** You've created configuration management tasks and a handler!

**What you'll learn**: Working with templates and handlers in Ansible using AI assistance.

---

### Exercise 3: Deploy index.html (Role 3)

**Step 1: Open the index.html Tasks File**

1. In the **left sidebar**, navigate to: **roles** → **index.html** → **tasks**
2. **Click on**: `main.yml`
3. The file opens showing 1 commented task

**Step 2: Generate the Task**

1. Find the line: `# - name: Create index.html from a template and save it as /ibmdata/htdocs/index.html owned by apache:apache`
2. **Uncomment it** - Delete the `#` symbol and space
3. **Click at the end of the line**
4. **Press ENTER**
5. **Wait for the AI suggestion** - notice how it understands:
   - Use a template
   - Save to the specific path
   - Set ownership to apache:apache
6. **Press TAB** to accept
7. ✅ Task complete!

**Step 3: Save Your Work**

1. Click **File** → **Save**

**✅ Exercise 3 Complete!** You've deployed web content with proper ownership!

**What you'll learn**: How AI-generated code handles file ownership and permissions correctly.

### Complete Playbook Structure

Your final playbook (`apacheservers.yml`) will use these roles:
- **httpd** - Install and configure Apache
- **httpd.conf** - Configure Apache settings
- **index.html** - Deploy web content

**Variables used**:
- `http_port: 8080`
- `apache_document_root: /ibmdata/htdocs`
- `server_type: apache`

---

### 3.3 🏗️ Exercise 4: Provision AWS EC2 Instance (Cloud Infrastructure)

**Purpose**: Learn how Ansible Lightspeed uses context and previously registered variables to generate accurate cloud infrastructure code.

**What you'll build**: Provision an AWS EC2 instance by gathering subnet information and using context-aware AI suggestions.

---

**Step 1: Create a New File**

1. In VS Code, click **File** → **New File**
2. Click **File** → **Save**
3. Name the file: `create_ec2_instance.yml`
4. Save it in your working folder

**Step 2: Copy the Starting Template**

Copy and paste this template into your new file:

```yaml
---
- name: EC2 Cloud Operations
  hosts: localhost
  connection: local
  gather_facts: false

  # module_defaults:
  #   group/aws:
  #     region: us-east-1

  # vars:
  #   ec2_instance:
  #     instName: lightspeed-instance-01
  #     key_name: lightspeed-keypair
  #     image_id: ami-016eb5d644c333ccb # RHEL 9 us-east-1
  #     tags:
  #       function: lightspeed-demo
  #     security_group: secgroup-lightspeed

  tasks:
        # TASK 1
        # 1a. Uncomment task description below and generate a task suggestion.
        #     Note - Best practices: The suggestion uses the Fully Qualified Collection Name (FQCN).
        #     Note - Context: Ansible Lightspeed uses the Playbook name "EC2 Cloud Operations" to use the correct "amazon.aws.ec2_vpc_subnet_info" module.
    # - name: Gather subnet info tag:Name subnet-lightspeed

        # TASK 2
        # 2a. Uncomment task description below and generate a task suggestion.
        #     Note - Context: The suggestion includes the previous task's registered variable in the suggestion.
        #     Note - Accuracy: The suggestion provides the correct key value from the previously task's registered variable.
    # - name: Create vpc_subnet_id var

        # TASK 3
        # 3a. Uncomment task description "Provision t3.micro instance" below and generate a task suggestion.
        #     Note - Efficiency: The suggestion provides practical variable examples to improve efficiency.
    # - name: Provision t3.micro instance

        # 3b. Remove the above task and suggestion.
        #     Uncomment 2nd task description "Provision t3.micro instance using ec2_instance var".
        #     Generate an updated suggestion.
        #     Note - Context: The updated suggestion includes the "ec2_instance variable fields in the suggestion"
    # - name: Provision t3.micro instance using ec2_instance var
```

**Step 3: Generate TASK 1 - Gather Subnet Information**

1. Scroll down to find the line: `# - name: Gather subnet info tag:Name subnet-lightspeed`
2. **Uncomment it** - Delete the `#` symbol and space at the beginning. It should look like:
   ```yaml
   - name: Gather subnet info tag:Name subnet-lightspeed
   ```
3. **Click at the end of this line**
4. **Press ENTER**
5. **Wait for the AI suggestion** - **Notice something amazing!**
   - The AI sees the playbook name "EC2 Cloud Operations"
   - It automatically knows to use AWS-specific modules
   - It uses the **Fully Qualified Collection Name** (amazon.aws.ec2_vpc_subnet_info)
6. **Press TAB** to accept
7. ✅ Task 1 complete!

**💡 Key Learning**: The AI understood context from the playbook name and chose the right AWS module!

---

**Step 4: Generate TASK 2 - Create Variable from Previous Task**

1. Find the line: `# - name: Create vpc_subnet_id var`
2. **Uncomment it** - Delete the `#` symbol and space
3. **Click at the end of this line**
4. **Press ENTER**
5. **Wait for the AI** - **This is incredible!**
   - The AI will automatically reference the variable that was registered in TASK 1
   - It knows the correct key values from the previous task's output
6. **Press TAB** to accept
7. ✅ Task 2 complete!

**💡 Key Learning**: The AI understands relationships between tasks and uses variables from previous tasks!

---

**Step 5: Generate TASK 3 (Part A) - Basic EC2 Instance**

1. Find the line: `# - name: Provision t3.micro instance`
2. **Uncomment it** - Delete the `#` symbol and space
3. **Click at the end of this line**
4. **Press ENTER**
5. **Wait for the AI** - It will generate a basic EC2 instance provisioning task
6. **Press TAB** to accept
7. **Review the generated code** - See what the AI created

---

**Step 6: Generate TASK 3 (Part B) - Enhanced with Variables**

Now let's see how using "using X var" in your prompt makes the AI suggestion even better:

1. **Select and delete** the entire task you just created in Step 5 (keep the tasks section intact, just remove what the AI generated)
2. Find the line: `# - name: Provision t3.micro instance using ec2_instance var`
3. **Uncomment it** - Delete the `#` symbol and space
4. **Click at the end of this line**
5. **Press ENTER**
6. **Wait for the AI** - **Compare the difference!**
   - Now the AI will use the `ec2_instance` variable that's defined at the top of the file
   - The suggestion will be more complete and use the variable fields
7. **Press TAB** to accept

**💡 Key Learning**: Adding "using X var" in your prompt tells the AI to use specific variables, giving you more sophisticated code!

---

**Step 7: Save Your Work**

1. Click **File** → **Save**

**✅ Exercise 4 Complete!** You've mastered context-aware AI suggestions!

---

**🎓 What You Learned**:

- **Context Awareness**: The AI analyzed "EC2 Cloud Operations" in the playbook name and automatically selected AWS modules
- **Variable Intelligence**: The AI referenced variables from previous tasks without you having to specify them
- **Best Practices**: The AI used Fully Qualified Collection Names (FQCN) like `amazon.aws.ec2_vpc_subnet_info`
- **Prompt Refinement**: Adding "using X var" gave you more sophisticated, variable-driven code
- **Cloud Infrastructure**: You can now automate AWS infrastructure with AI assistance!

**💡 Big Picture**: This exercise showed you that Ansible Lightspeed doesn't just generate code - it understands the context of your entire playbook and the relationships between tasks!

---

## 4. 🏠 Take-Home Optional Challenges

Want to continue learning after the hackathon? Try these additional exercises to expand your Ansible Lightspeed skills!

**How to use these challenges**:
- Work through these at your own pace after the hackathon
- Use the same techniques you learned in the main exercises
- Follow the pattern: Create file → Copy template → Uncomment lines → Press ENTER → Press TAB
- Experiment with both single-task and multi-task generation options

---

### Challenge 1: PostgreSQL Database & PGAdmin Container Setup

**What you'll build**: Install PostgreSQL database server and deploy PGAdmin as a containerized application using Podman.

**Skills you'll practice**:
- Database installation and initialization
- Container management with Podman
- Service configuration
- Working with variables in prompts (using `var_name` syntax)

---

#### Part 1: Install PostgreSQL Server

**Option A - Single Task Generation**

Create a new file called `install_pgsql-single-task.yml` and copy this template:

```yaml
---
- name: Configure Database servers
  hosts: databases
  become: true

  tasks:
    # TASK 1
    # - name: Install postgresql-server

    # TASK 2
    # Ansible Lightspeed will suggest the correct PostgreSQL CLI command to initiate the database
    # It uses best practices and keeps the task idempotent by including creates: /var/lib/pgsql/data/postgresql.conf
    # - name: Run postgresql setup command

    # TASK 3
    # Ansible Lightspeed adds state: started and enabled: true based on the task description
    # - name: Start and enable postgresql service
```

**Option B - Multi-Task Generation**

Create a new file called `install_pgsql-multi-task.yml` and copy this template:

```yaml
---
- name: Configure Database servers
  hosts: databases
  become: true

  tasks:
    # Install postgresql-server & Run postgresql setup command & Start and enable postgresql service
```

---

#### Part 2: Deploy PGAdmin Container

**Option A - Single Task Generation**

Create a new file called `demo_pgadmin_podman-single-task.yml` and copy this template:

```yaml
---
- name: Configure pgadmin container
  hosts: webservers
  become: true

  vars:
    pgadmin_service_name: app-pgadmin

    pgadmin_container:
      name: pgadmin
      restart: false
      image: docker.io/dpage/pgadmin4:7.5
      state: started
      env:
        PGADMIN_DEFAULT_EMAIL: student@example.com
        PGADMIN_DEFAULT_PASSWORD: learn_ansible
      generate_systemd:
        path: /etc/systemd/system/
        container_prefix: app
        restart_policy: always
      ports:
        - 8083:80
      network: bridge

  tasks:
    # - name: Run podman container using pgadmin_container var

    # - name: Start, enable and reload daemon for {{ pgadmin_service_name }}
```

**Option B - Multi-Task Generation**

Create a new file called `demo_pgadmin_podman-multi-task.yml` and copy this template:

```yaml
---
- name: Configure pgadmin container
  hosts: webservers
  become: true

  vars:
    pgadmin_service_name: app-pgadmin

    pgadmin_container:
      name: pgadmin
      restart: false
      image: docker.io/dpage/pgadmin4:7.5
      state: started
      env:
        PGADMIN_DEFAULT_EMAIL: student@example.com
        PGADMIN_DEFAULT_PASSWORD: learn_ansible
      generate_systemd:
        path: /etc/systemd/system/
        container_prefix: app
        restart_policy: always
      ports:
        - 8083:80
      network: bridge

  tasks:
    # Run podman container using pgadmin_container var & Start, enable and reload daemon for {{ pgadmin_service_name }}
```

**What you'll learn**:
- How Ansible Lightspeed understands and uses variables in prompts (the `pgadmin_container` variable)
- Container management with Podman using AI-generated code
- How to use keywords like "using X var" to get better suggestions

---

### Challenge 2: Full Playbook Generation - RHEL Patching Workflow

**What you'll build**: A complete enterprise-grade RHEL patching playbook using the **Playbook Generation** feature.

**How it works**: Instead of writing tasks manually, you'll use natural language to describe your entire workflow, and Ansible Lightspeed will generate a complete playbook!

#### How to Access Playbook Generation:
1. Click on the **'Ansible'** icon in VS Code's Activity Bar
2. Under **'Ansible Content Creator'** → **'Get Started'**
3. Under **'Create'** → **'Playbook with Ansible Lightspeed'**

#### Your Mission:
Copy and paste this natural language prompt into the textarea:

```
Create an Ansible playbook to patch RHEL Linux servers in one workflow, disable facts and then perform the following tasks:
Print a debug message saying 'Patching RHEL is starting.'
Get subscription identity (subscription-manager identity)
Fail if the system is not registered.
Get the available repositories for RPM package connectivity and check for any issues.
Fail the playbook if any repositories have problems.
Get space for the disk-based boot file system (/boot)
Fail if the disk-based boot file system (/boot) does not have at least 100MB of free space.
Unset the release version used by RHSM repositories, allowing updates to the latest version.
Update all installed packages to the latest versions.
Ensure the RPM package 'yum-utils' is installed.
Check if a reboot is required
Reboot the system to fully integrate all patches into the system if necessary.
Finally, print a message that says 'Patching RHEL has been successfully completed.'
```

**Steps**:
1. Press **"Analyze"** to proceed
2. Review the suggested steps for your playbook and modify as needed (prompt refinement)
3. Press **"Generate playbook"** to open a new tab with the full playbook

**What you'll learn**:
- How to use natural language to generate complete playbooks
- Enterprise patching workflows
- Error handling and validation in Ansible
- Real-world scenarios relevant to banking/enterprise environments

**Note**: This feature creates **self-contained** full playbooks — it does not generate Ansible roles.

---

## 5. 📚 Additional Resources for Self-Learning

- **Ansible Best Practices**: https://docs.ansible.com/ansible/latest/tips_tricks/ansible_tips_tricks.html
- **Ansible Galaxy (Roles & Collections)**: https://galaxy.ansible.com/
- **Red Hat Ansible Automation Platform**: https://www.redhat.com/en/technologies/management/ansible
- **IBM watsonx Code Assistant Documentation**: https://www.ibm.com/docs/watsonx-code-assistant

---

## 6.  Hackathon Day Schedule

**Date**: TBD, 2024
**Time**: TBD

### Agenda

- Welcome & Introduction to IBM watsonx Code Assistant
- Ansible Lightspeed Demo & Features Overview
- Hands-on Lab Exercises (Warm-up + Main Exercise)
- Challenge Exercise & Q&A
- Wrap-up & Next Steps

---

## 7. 💡 Tips for Success

1. **Write clear, descriptive task names** - The AI works best with specific, clear instructions
2. **Use the `&` separator** for multi-task generation
3. **Review AI suggestions carefully** before accepting them
4. **Press TAB to accept** suggestions, ESC to reject
5. **Leverage context** - Lightspeed understands your playbook structure

---

## 8. 🆘 Getting Help

- During the workshop, IBM instructors will be available to assist
- Raise your hand or use the chat function if you need help
- Common issues and solutions will be shared in real-time

---

## 9. 📞 Contact Information

For questions or issues with setup, please contact:
- [Workshop organizer contact information - to be added]

---

## 10. 🔗 Useful Resources

### Documentation
- [IBM watsonx Code Assistant Documentation](https://www.ibm.com/docs/watsonx-code-assistant)
- [Ansible Lightspeed Documentation](https://docs.ai.ansible.redhat.com/)
- [Ansible Documentation](https://docs.ansible.com/)

### Video Tutorials
- 🎥 [Playbook Generation using Ansible Lightspeed with IBM watsonx Code Assistant](https://youtu.be/oS7mSykl_D0?list=PLdu06OJoEf2bVLR899FuKc3AiuJvbIRZU) - by Anshul Behl, Principal Technical Marketing Manager at Red Hat®
- 🎥 [Ansible Playbook Creation with IBM watsonx Code Assistant](https://youtu.be/vG54TKeEwP4) - by Ian Smalley, Editor at IBM® Technology

### Advanced Features
- [Model Customization Guide](https://cloud.ibm.com/docs/watsonx-code-assistant?topic=watsonx-code-assistant-tutorial-tune-ansible#tune-ansible-prereqs) - Learn how to tune the AI model with your organization's Ansible data

### Questions or Issues?
- If you have questions or encounter issues, you can create an issue on the [GitHub Repository](https://github.com/IBM/watsonx-code-assistant-for-ansible/issues/)

---

## 11.  Post-Workshop Feedback

After the workshop, please complete our feedback survey to help us improve future sessions:
- [Feedback Survey Link - to be added]

---

**Ready to get started?** Complete the setup steps above and we'll see you at the hackathon! 🚀

*For technical support during setup, please email [support contact - to be added]*

---

## License

This workshop is based on the [IBM watsonx Code Assistant for Ansible Lightspeed](https://github.com/IBM/watsonx-code-assistant-for-ansible) repository.

**License**: [Apache License 2.0](http://www.apache.org/licenses/)

**Copyright**: ©️ Copyright IBM Corporation 2024
