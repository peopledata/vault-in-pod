# vault-in-pod

Manifests to setup peoplevault server in kubernetes pod.

Kubernetes default secret object is just base64 encoded. You need a good KMS tools and workflow to manage secret storage and retrieval for production uses cases.

Hashicorp/Vault is one of the best open-source KMS tools that has good integration with Kubernetes to store and retrieve secrets.

PeopleVault is a two-tier KMS, which a Root Vault is deployed close with individual person and a Vault Pod in remote cloud. The Root Vault is the root of the Vault Pod, and invesibale from outside. The Vault Pod is intermediate Vault which provider major KMS service to outside. The individual person just manage the Root vault and hold a root phase word/pin only, the rest KMS service will be automatically processed by Root Vault and Vault Pod.

**vault-in-pod** is the second tier KMS of PeopleVault, which deplyed in Kubernetes pod.

Let's start with two basic tutorial which help you understand how vault-in-pod works:

## Tutorial
1. [Setup the Vault in Kubernetes](https://github.com/peopledata/vault-in-pod/blob/ffdbf5e061a3d3cc9d04f3d8d80d87ec002da280/vault-in-pod-tutorial.md)

2. [Vault Agent Injector Tutorial](https://github.com/peopledata/vault-in-pod/blob/6e80fcc6b9b549ad8b7bae63ea148e64fcd9c85d/vault-injector/tutorial.md)

## How to use vault-in-pod
Choose the deployment yaml files and make adjustment depned on your production environment, the do as you learned from above tutorial.

A Community Quickstart Scripts will be relased.

