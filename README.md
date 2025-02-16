[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/sigscale-cgf)](https://artifacthub.io/packages/search?repo=sigscale-cgf)

# cgf-helm
Helm chart for deploying SigScale CGF on Kubernetes

## Deploy a SigScale CGF StatefulSet
	helm install cgf-1 sigscale-cgf

## List Helm releases
	helm list

## Remove a SigScale CGF StatefulSet
	helm uninstall cgf-1

## Deploy with localization overides in sys.config
	helm install \
			--set cgfConfig.create=true \
			--set-file cgfConfig.sysConfig=sys.config \
			cgf-1 sigscale-cgf

