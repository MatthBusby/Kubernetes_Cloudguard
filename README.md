# Kubernetes + Cloudguard
Written by Michael Braun

![Build](https://github.com/metalstormbass/Kubernetes_Cloudguard/workflows/Build/badge.svg?event=push)

<p align="left">
    <img src="https://img.shields.io/badge/Version-1.0.0-green" />
</p>    

This is a Helm Chart that deploys the OWASP Juice Shop application and Cloudguard WAAP. <br>

<b>Credit to Mark Nichols for assisting me with Helm.</b> I "borrowed" a lot from his project, located [HERE](https://github.com/mnichols62/cpWaapJuice). <br>

This deployment can be done directly on an AKS Cluster or with Github Actions to deploy AKS, Juice Shop and Log.IC. These instructions will outline how to deploy using a CI/CD pipeline. <br><br>



![](images/cloudguard_kubernetes.PNG)


The build pipeline performs the following actions:<br>

1. Login to Azure and create AKS cluster<br>
2. Package Helm Chart<br>
3. Deploy Helm Chart to AKS<br>
4. Add K8 account to Check Point CSPM<br>
5. Deploy Check Point CPSM Helm Chart for onboarding.<br>

The destroy pipeline performs the following actions: <br>
1. Deletes the Azure environment created by the build pipeline<be>
2. Removes the K8 account from CSPM<br>

<b> Get started by Forking this responsitory!</b>

## Prerequisites


