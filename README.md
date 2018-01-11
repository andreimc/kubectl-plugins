*Seriously someone just do this readme for me...lol*

# kubectl-plugins

A collection of plugins for kubectl integration
 - Requires jq ( brew install jq )

## Install on Linux
  Just create the ~/.kube/plugins folder and copy the plugin folders there..
  
## Install via homebrew: 
  **brew tap bitbrew/kubectl**

  **brew install plugins**

  **install-plugins**


### kubectl deploy [options]
   [-f, --file] (Ex: -f 20-actions.yml) File to deploy. At this time, only accepts a single file. Required.
  
   [-i, --image] (Ex: -i kafka:v1.0.0 **or** -i kafka) Docker image/tag to use. If only the image name is passed, it displays a list of images to choose from. Optional.
  
   [-d, --dry-run] (Ex: -d true) Runs the command in dry-run mode. Optional.
  
   [-n, --namespace] (Ex: -n preprod) Namespace/Environment to deploy to (defaults to current ns). Optional
   
   Example: kubectl deploy -f 40-actions.yml -i actions -n staging


 ### kubectl uptime
  - Displays total uptime for pods/statefulsets in the user namespace.


 ### kubectl switch [options]
  - View current namespace: kubectl switch
  - Switch namespace: kubectl switch preprod
  - Switch cluster: kubectl switch cluster


 ### kubectl get-node-ip
  - Outputs the node location and IP for a given application e.g., kubectl get-nodes ingestion
  
  - Usage: kubectl get-node-ip <app or statefulset name>


 ### kubectl ssh
  - Like kubectl exec, but offers a --user flag to exec as root (or any other user) if you're running in GKE
  
  - Usage: kubectl ssh -p pod-name -u user

