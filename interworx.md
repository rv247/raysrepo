1. Create Oracle Instance

2. Go to VCN and add Security Group named 'interworx' with ingress ports 80,443,2443

3. Attach Security Group 'interworx' to Oracle Instance

4. Login to Oracle Instance over SSH

5. Run these commands
```
   sudo -i
   cat /etc/redhat-release
   yum repolist; yum upgrade -y
   sh <((curl -sL updates.interworx.com/interworx/7/install.sh)) -l -f
```

6. Once complete, you should be able to access from the browser -- run this command to get the URL (you'll need a license; see step 7)
```
   VPSIP=`curl icanhazip.com -4 2>/dev/null` ; echo  "Go to this site in the browser https://$VPSIP:2443/nodeworx/"
```
7. Go to Interworx website and request a Demo License (can take about 48 hours)
   - https://www.interworx.com/interworx-demos/
