# ArgoCD-Tekton - CICD Deploy

## Intro

All the necessary yaml files to deploy the generic golang-cicd pipelines, tasks and triggers in kubernetes

## CICD folder structure

The folder structure is as follows :

```bash

      --- environments
      |     |
      |     --- overlays
      |           |
      |           --- cicd
      |                 |
      |                 --- namespace
      |                 |     |
      |                 |     --- limit-range.yaml
      |                 |     --- namespace.yaml
      |                 |     --- resource-quota.yaml
      |                 --- shared
      |                 |     |
      |                 |     --- pipeline-pvc.yaml
      |                 |
      |                 --- kustermization.yaml
      |
      --- manifests
            |
            --- tekton
                  |
                  --- tasks
                  |     |
                  |     --- base
                  |           |
                  |           --- golang-build-dev.yaml
                  |           --- golang-clean-dev.yaml
                  |           --- golang-sonarqube-dev.yaml
                  |           --- golang-test-dev.yaml
                  --- secrets
                  |     |
                  |     --- base
                  |           |             
                  |           --- git-argocd-http-secret.yaml
                  |           --- git-http-secret.yaml
                  |           --- git-infra-ssh-secret.yaml
                  |           --- image-pull-secret.yaml
                  |           --- quay-secret.yaml
                  |           --- sonarqube-secret.yaml
                  --- triggers
                  |     |
                  |     --- base
                  |           |             
                  |           --- trigger-binding-dev.yaml
                  |           --- trigger-binding-uat.yaml
                  |           --- trigger-event-listener-dev.yaml
                  |           --- trigger-event-listener-prd.yaml
                  |           --- trigger-event-listener-uat.yaml
                  |           --- trigger-template-dev.yaml
                  |           --- trigger-template-prd.yaml
                  |           --- trigger-template-uat.yaml
                  --- rbac
                  |     |
                  |     --- base
                  |           |    
                  |           --- admin.yaml
                  |           --- edit.yaml
                  |           --- view.yaml
                  |           --- kustermization.yaml
                  --- pipelines
                        |
                        --- base
                              |    
                              --- pipeline-dev.yaml
                              --- pipeline-uat.yaml
                              --- pipeline-prd.yaml
```
            

