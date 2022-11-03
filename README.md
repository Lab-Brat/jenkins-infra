### Jenkins-Infra

#### Agent configuration
* Dashboard >> Manage Jenkins >> Manage nodes and clouds
* \+ New node >> Permanent Agent
* Configure following settings:
    * name: agent1
    * description: vagrant jenkins-agent1.lab host
    * Number of executors: 2
    * Remote root directory: /var/lib/jenkins
    * Launch method: SSH
        * 192.168.56.121
        * choose credentials, create if doesn't exist
        * Host Key Verification Strategy: Manually trusted key Verification Strategy
        * Advanced: JavaPath = /bin/java
* Save
<br>

#### Agent server configuration
Agent server can be configured using `configure_agent.yaml` ansible playbook:
```
ansible-playbook configure_agent.yaml 
```
