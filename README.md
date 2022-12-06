# Nginx logrotate s3 backup poc
This is a proof of concept on how to implement logrotation and aws s3 backup for nginx logs. This configuration keeps a single backup of nginx logs and copies it to s3 bucket on a weekly basis. 

### Required tools on the server
* awscli
* logrotate (preinstalled on ubuntu vms)

### Implementation steps
* copy <code>nginx_logrotate_s3_backup_poc/logrotate.d/nginx</code> to <code>/etc/logrotate.d/nginx</code>
* edit <code>/etc/logrotate.d/nginx</code> and change <code>\<bucketname></code> to correct bucket name
* run <code>sudo aws configure</code> and add awscli credentials 

