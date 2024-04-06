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
   The slack webhook URL was directly created and updated in the configmap of the alert manager and slack notifications were sent to the #upcommerce-devs channel.
