In this lab, we deployed a customized NGINX web server on Kubernetes, focusing on configuration, persistence, and external access. Instead of relying on the default NGINX settings, we created a custom nginx.conf file that returned a simple text message. This configuration was turned into a ConfigMap, allowing it to be mounted into the container at runtime.

To ensure data was not lost during restarts or redeployments, we created a Persistent Volume Claim (PVC) and attached it to the server’s content directory. This setup ensures that static files remain intact even if the pod is recreated.

We then exposed the deployment using a Kubernetes Service of type LoadBalancer, enabling access via a public-facing IP. Using minikube service, we retrieved the URL and confirmed the deployment worked by accessing it through a browser.

To monitor and manage the deployment, we also launched the Kubernetes dashboard, which provided a user-friendly view of our pods, volumes, and services.