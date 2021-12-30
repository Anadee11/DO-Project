# DO Kubernetes Challenge

## Deploying MongoDB Cluster on Kubernetes with DigitalOcean

### Prerequisites:
- A Digital Ocean Account : [DigitalOcean](https://www.digitalocean.com/)
- doctl setup : [Installing doctl](https://docs.digitalocean.com/reference/doctl/how-to/install/#step-1-install-doctl)
- kubectl installed : [Installing kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)

## Let's Get Started

- [ ] Creating a Kubernetes Cluster
1. Head over to the control section in your project on the Digital Ocean Website and click on **Create**  .
2. Select **Kubernetes** from the drop-down(as we wish to create a Kubernetes Cluster) .
3. Fill in the region where you wish to create the cluster .
4. Select the number of nodes you wish to create and other details .
5. Give a name to your cluster and click on Create .
- Note: The cluster takes 4-5 mins to create, be patient and wait for it to finish .

- [ ] Connecting to the Cluster
1. After the cluster is successfully created, move to the overview tab .
2. In the **Connecting to Kubernetes** part, copy the command and paste it to run in your terminal .
3. As we have to deploy MongoDB in this cluster, we have skipped the **Installing 1-Click Apps** and others parts .
4. Directly click on **Great, I am done** .

- [ ] Deploying MongoDB 
1. Clone my repository [DO-Project Repository](https://github.com/Anadee11/DO-Project) .
  ( Use `git clone https://github.com/Anadee11/DO-Project.git ` ) .
2. Run ` kubectl apply -f .` for deploying the MongoDB cluster.
3. To check the deployment status run, ` kubectl get all`.

- [ ] Verifying the Deployment
1. Run the following to connect to the MongoDB cluster.
        `kubectl exec deployment/mongo-client -it -- /bin/bash` 
2. After the above runs, successfully.  Run :
         ` mongo --host mongo-nodeport-svc --port 27017 -u #username -p  #password `

 - Note: If 2 doesn’t work, simply run the following command :
`mongo`

#### HURRAYY!!!
- [ ] CELEBRATE as you have successfully deployed a MongoDB cluster on Kubernetes with the help of DigitalOcean.
# [![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://forthebadge.com) [![forthebadge](https://forthebadge.com/images/badges/built-by-developers.svg)](https://forthebadge.com)
