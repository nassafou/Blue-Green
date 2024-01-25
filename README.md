# Blue-Green
Create a Blue/Green Setup for an Existing Deployment

Create a blue/green Deployment setup for the existing web-frontend Deployment in the bluegreen Namespace.

You can find a Deployment manifest for web-frontend on the CLI server at web-frontend.yml. Feel free to copy this manifest in order to create your green Deployment.

Give the green Deployment the name web-frontend-green and set the env label to green in the Pod template.

Once you have created the green Deployment and verified that it is working, modify the web-frontend-svc Service so that it points only to the new green Deployment's Pods. This is a NodePort Service, and you can test it by reaching out to port 30081 on any of the cluster nodes, for example: curl controlplane:30081
