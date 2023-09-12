### OpenShift APIServer

Implementation of an aggregated API Server for Kubernetes which is responsible for the following APIs:
* apps.openshift.io/v1
* authorization.openshift.io/v1
* build.openshift.io/v1
* image.openshift.io/v1
* project.openshift.io/v1
* quota.openshift.io/v1
* route.openshift.io/v1
* security.openshift.io/v1
* template.openshift.io/v1


The provided custom resource types are as below:

| Resource Name | API Version | Namespaced |
| ------------- | ------------- | ------------- | 
| deploymentconfigs | apps.openshift.io/v1 | true |
| clusterrolebindings | authorization.openshift.io/v1 | false |
| clusterroles | authorization.openshift.io/v1 | false |
| localresourceaccessreviews | authorization.openshift.io/v1 | true |
| localsubjectaccessreviews | authorization.openshift.io/v1 | true |
| resourceaccessreviews | authorization.openshift.io/v1 | false |
| rolebindingrestrictions | authorization.openshift.io/v1 | true |
| rolebindings | authorization.openshift.io/v1 | true |
| roles | authorization.openshift.io/v1 | true |
| selfsubjectrulesreviews | authorization.openshift.io/v1 | true |
| subjectaccessreviews | authorization.openshift.io/v1 | false |
| subjectrulesreviews | authorization.openshift.io/v1 | true |
| buildconfigs | build.openshift.io/v1 | true |
| builds | build.openshift.io/v1 | true |
| images | image.openshift.io/v1 | false |
| imagesignatures | image.openshift.io/v1 | false |
| imagestreamimages | image.openshift.io/v1 | true |
| imagestreamimports | image.openshift.io/v1 | true |
| imagestreammappings | image.openshift.io/v1 | true |
| imagestreams | image.openshift.io/v1 | true |
| imagestreamtags | image.openshift.io/v1 | true |
| imagetags | image.openshift.io/v1 | true |
| projectrequests | project.openshift.io/v1 | false |
| projects | project.openshift.io/v1 | false |
| appliedclusterresourcequotas | quota.openshift.io/v1 | true |
| clusterresourcequotas | clusterquota | quota.openshift.io/v1 | false |
| routes | route.openshift.io/v1 | true |
| podsecuritypolicyreviews | security.openshift.io/v1 | true |
| podsecuritypolicyselfsubjectreviews | security.openshift.io/v1 | true |
| podsecuritypolicysubjectreviews | security.openshift.io/v1 | true |
| rangeallocations | security.openshift.io/v1 | false |
| securitycontextconstraints | security.openshift.io/v1 | false |
| brokertemplateinstances | template.openshift.io/v1 | false |
| processedtemplates | template.openshift.io/v1 | true |
| templateinstances | template.openshift.io/v1 | true |
| templates | template.openshift.io/v1 | true |

The APIServer is also responsible for setting a number of sane defaults for Namespaces, such as the SCC configuration for Namespaces[0].
