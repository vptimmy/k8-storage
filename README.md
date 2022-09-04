# This is my storageClass drivers for Kubernetes.

I have configured NFS on my Synology NAS.  Below is the installation to create dynamic PV on the NAS.  

`helm repo add csi-driver-nfs https://raw.githubusercontent.com/kubernetes-csi/csi-driver-nfs/master/charts`
`helm install csi-driver-nfs csi-driver-nfs/csi-driver-nfs --namespace kube-system --version v4.1.0`
`kubectl apply -f storageClass.yaml`

