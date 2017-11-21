# Takipi / OverOps Ansible Playbook


### Install takipi with options
#### example:
- install agent:<br>
``ansible-playbook takipi-setup.yml -e "hosts='all|1.1.1.1|group' secret='SXXXX...XXX' daemon_host=collector-host daemon_port=6060"``
- install collector:<br>
``ansible-playbook takipi-setup.yml -e "hosts='all|1.1.1.1|group' secret='SXXXX...XXX' listen_on_port=6060"``

 

### options: 
## required: 
- secret: (your secret key)
- hosts: the hosts to run on (see ansible inventory)
## optional:
based on takipi installation script --help 
```
        --installer_url      Specify installation tarball URL                                       
        --verbose            Enable verbose logging                                                 
        --non_interactive    Run in non-interactive mode                                            
        --skipjversion       Do not verify Java version                                             
        --install_jdk        Install the JDK                                                        
        --auto_agent                                                                                
        --config_attach                                                                             
        --ide_attach                                                                                
  -sk   --secret_key         Specify secret key                                                     
        --machine_name       Specify machine name                                                   
        --base_url           Specify server URL                                                     
        --s3_url             Specify S3 ping URL                                                    
        --listen_on_port     Specify daemon port to listen                                          
        --daemon_host        Specify a remote daemon host                                           
        --tmp_dir            TEMP folder for the installation                                       
        --tmp_dir_minimal_size TEMP folder minimal free space for the installation (in Bytes)         
        --daemon_port        Specify a remote daemon port                                           
        --passphrase         Specify an authentication token between Daemon and Agent               
        --installation_dir   Specify the installation directory                                     
        --installation_dir_minimal_size Specify the installation directory minimal free space (in Bytes)       
        --strict             Exit on first error or continue all validations                        
        --dry_run            If set will validate the pre requirements only                         
        --unpriviliged       Run in unpriviliged mode (different user then root)                    
        --user               Specify the user name                                                  
        --password           Specify the new user password                                          
        --shutdownGraceTime  Sleep on agent shutdown                                                
        --resourceFolderLimit Specify the resource folder limit in MB                                
        --https_proxy        An Https proxy used to connect to the Internet                         
        --no_check_certificate Skip certificate validation   
```