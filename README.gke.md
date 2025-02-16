# Manage Google Kubernetes Engine (GKE)

## Create a GKE Autopilot Cluster
	gcloud container clusters create-auto cgf-cluster

## Configure `kubectl` to use the GKE Cluster
	gcloud container clusters get-credentials cgf-cluster

$# Get the Pods (after `helm install`)
	kubectl get pods

## Get the log of init container
	kubectl logs cgf-1-sigscale-cgf-0 -c cgf-init

## Get the log of container
	kubectl logs cgf-1-sigscale-cgf-0

## Describe the pod
	kubectl describe pod cgf-1-sigscale-cgf-0

## Attach to a GKE pod deployment which runs cgf container
	$ kubectl attach -ti cgf-1-sigscale-cgf-0 -c cgf -i -t
	(cgf@cgf-1-sigscale-cgf-0.otp-cgf.default.svc.cluster.local)5>
### There is no `detach` so you'll need to kill the `kubectl attach` process

