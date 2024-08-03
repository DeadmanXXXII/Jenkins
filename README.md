# Jenkins
Jenkins Java CLI commands
Here is a comprehensive list of Jenkins CLI commands. Jenkins CLI allows you to manage Jenkins and its components from the command line, offering various functionalities including managing jobs, nodes, and configurations.

### **Jenkins CLI Commands**

#### **1. Basic Commands**

- **Get Jenkins CLI:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL help
  ```

- **Check Jenkins version:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL version
  ```

- **List available commands:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL help
  ```

#### **2. Job Management**

- **Create a new job from a job definition file (XML):**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL create-job JOB_NAME < job.xml
  ```

- **Delete a job:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL delete-job JOB_NAME
  ```

- **Build a job:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL build JOB_NAME
  ```

- **Build a job with parameters:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL build JOB_NAME -p PARAM1=VALUE1 -p PARAM2=VALUE2
  ```

- **Get job info:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL get-job JOB_NAME
  ```

- **Update job configuration:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL update-job JOB_NAME < config.xml
  ```

- **Get the build status of a job:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL build JOB_NAME --dry-run
  ```

#### **3. Node Management**

- **List all nodes:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL list-nodes
  ```

- **Get information about a specific node:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL get-node NODE_NAME
  ```

- **Delete a node:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL delete-node NODE_NAME
  ```

- **Create a new node:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL create-node NODE_NAME
  ```

#### **4. System Management**

- **Reload the Jenkins configuration from disk:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL reload-configuration
  ```

- **Safe restart Jenkins (waits for jobs to finish):**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL safe-restart
  ```

- **Restart Jenkins:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL restart
  ```

- **Get the current system information:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL system-info
  ```

- **Update Jenkins CLI jar:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL update-jar
  ```

#### **5. User Management**

- **List users:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL list-users
  ```

- **Create a new user:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL create-user USERNAME --password PASSWORD
  ```

- **Delete a user:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL delete-user USERNAME
  ```

#### **6. Plugin Management**

- **List installed plugins:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL list-plugins
  ```

- **Install a plugin:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL install-plugin PLUGIN_NAME
  ```

- **Uninstall a plugin:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL uninstall-plugin PLUGIN_NAME
  ```

- **Update plugins:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL upgrade-plugin PLUGIN_NAME
  ```

#### **7. Backup and Restore**

- **Backup Jenkins (copy config.xml and jobs):**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL backup
  ```

- **Restore Jenkins from a backup:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL restore-backup BACKUP_FILE
  ```

#### **8. Miscellaneous Commands**

- **Display Jenkins server logs:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL log
  ```

- **Get help for a specific command:**
  ```bash
  java -jar jenkins-cli.jar -s JENKINS_URL help COMMAND_NAME
  ```

### **Summary**

This list includes a broad range of Jenkins CLI commands for managing Jenkins jobs, nodes, system configurations, users, plugins, and more. The commands cover both common and advanced administrative tasks, enabling efficient management of Jenkins environments.
