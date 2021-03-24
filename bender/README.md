Helm chart for [Bender](https://github.com/ValentinLevitov/bender) deployment under Kubernetes, OpenShift or OKD.
Download the repository, update schedules in files/crontab and rules in files/rules.xml, then call command
```bash
helm upgrade bender ./ --set \
jira.rootUri=https://your-jira-instance.organization.com\
,jira.userName=your-jira-user\
,jira.password=your-jira-password\
,smtp.host=your.smtp.server\
,smtp.port=25\
,smtp.userName=smtp-server-user-name\
,smtp.password=smtp-server-user-password\
,smtp.enableSsl=true\
,smtp.from=your-user@example.com\
,application.supervisors=your-user@example.com
```
Or you can set the parameters in values.yaml file and just call
```bash
helm upgrade bender ./
```