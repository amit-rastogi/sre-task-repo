Week 1 Project - SRE Fundamentals with Google

This project uses github codespaces to setup a minikube cluster to deploy the UpCommerce application.

Steps-
1. Start minikube
2. Create namespace sre
3. Add the alerts in prometheus.yml
4. Use helm to install prometheus
5. Create UpCommerce deployment and service
6. Test the alerts
7. For slack notification attached the slack notification png file captured during slack notification testing.
   The slack webhook URL was directly created and updated in the configmap of the alert manager and slack notifications were sent to the #upcommerce-devs channel. The relevant snippet of the config map having slack notification changes-
   data:
     alertmanager.yml: "global:\n  resolve_timeout: 1m\nreceivers:\n- name: 'slack-notifier'\n
      \ slack_configs:\n  - channel: '#upcommerce-devs'\n    send_resolved: true\n    api_url:
      'https://hooks.slack.com/services/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'
      \nroute:\n  group_interval: 2m\n  group_wait: 10s\n  receiver: 'slack-notifier'\n
      \ repeat_interval: 2m\ntemplates:\n- /etc/alertmanager/*.tmpl\n"
