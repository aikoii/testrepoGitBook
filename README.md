---
hidden: true
noIndex: true
---

# 🐙 Octopus

{% updates format="full" %}
{% update date="2025-12-18" %}
## Dec 18

Extracting Tables: The extract a table procedure now supports a file\_upload mode for PDF documents, allowing you to send a file directly to an LLM for significantly improved performance.\
Comment on block\
Playground Responsiveness: We've optimized the Playground editor by improving data handling and limiting undo/redo history size, resulting in a more responsive experience.
{% endupdate %}
{% endupdates %}

{% updates format="full" %}
{% update date="2025-12-18" %}
##




{% endupdate %}
{% endupdates %}

## In-place workload right-sizing

{% include ".gitbook/includes/autonomous-workload-optimiz... (1).md" %}

{% include ".gitbook/includes/in-place-concept.md" %}

{% include ".gitbook/includes/the-standard-pod-scaling-ap....md" %}

1. **Keep infrastructure reliable** by eliminating the risks associated with restarts.
2. **Stay continuously optimized** without service disruption.
3. **Maintain operational productivity** without the overhead of time-consuming manual investigation and optimization.

You can find more details about in-place changes on the official Kubernetes website:[![](https://images.gitbook.com/__img/dpr=1.7999999523162842,width=32,onerror=redirect,height=32,fit=contain,format=auto,signature=-1084863014/https%3A%2F%2Fkubernetes.io%2Ficons%2Ficon-128x128.png)Kubernetes v1.33: In-Place Pod Resize Graduated to BetaKubernetes](https://kubernetes.io/blog/2025/05/16/kubernetes-v1-33-in-place-pod-resize-beta/)

### Prerequisites <a href="#prerequisites" id="prerequisites"></a>

{% content-ref url="./" %}
[.](./)
{% endcontent-ref %}

To start leveraging in-place workload right-sizing, your cluster must support in-place changes.🎯 Update Kubernetes to **version 1.33 or later** and **enable the beta** `InPlacePodVerticalScaling` [**feature gate**](https://kubernetes.io/docs/reference/command-line-tools-reference/feature-gates/) for your control plane and for all nodes in your cluster. After that, PerfectScale will automatically perform in-place workload right-sizing without additional effort from your side.No additional configurations are needed, as PerfectScale automatically applies changes in place, delivering instant optimization.

### In-place resizing limitations <a href="#in-place-resizing-limitations" id="in-place-resizing-limitations"></a>

|                          |                                                                                                                                                                                      |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Supported workload types | **DeploymentStatefulSetDaemonSet**                                                                                                                                                   |
| Resizable resources      | <p><strong>CPU</strong></p><ul><li>request</li><li>limit</li></ul><p><strong>Memory</strong></p><ul><li>request</li><li>limit (increase only)</li></ul>                              |
| Operating system         | Windows pods do not support in-place                                                                                                                                                 |
| Kubernetes version       | **1.33** or later                                                                                                                                                                    |
| Container resize policy  | **restartPolicy: NotRequired** (apply the resource change to the running container without restarting it). If **restartPolicy: RestartContainer** - in-place changes will not apply. |
| QoS Class                | The Pod's original QoS class is determined at creation and cannot be changed by a resize.                                                                                            |

In-place right-sizing with PerfectScale AutomationIn-place pod resizing combined with PerfectScale Automation provides a complete solution for graceful and effective workload right-sizing. It eliminates manual effort associated with identifying inefficiencies and risks due to guestimated allocations, enabling continuous safe cost-reduction.If in-place resizing is not supported, PerfectScale’s safe automation algorithm will apply changes with a traditional scaling approach, ensuring your clusters remain reliable and stable.For automated pods that support in-place changes, when an over-provisioned or under-provisioned workload is detected, PerfectScale instantly applies data-driven recommendations without pod restart, ensuring safe K8s optimization.When PerfectScale applies in-place changes to right-size workloads, it unifies pod resources, guaranteeing consistency of the resources across the cluster.PodResizePending handlingYou may encounter a situation where it is impossible to apply new resources to a pod. In this case, the pod will get the PodResizePending status. This can happen due to:The requested resize is impossible on the current node (for example, requesting more resources than the node can provide).The requested resize is not currently possible, but may become possible later (for example, if another pod is removed and resources become available).To handle such cases, you can configure the PodResizePending strategy in the automation configuration CR by specifying one of the following values:rollingRestart (default)All pods will be restarted in order to update resources.deleteRecreatePendingPodOnly pods in the PodResizePending status will be deleted to trigger rescheduling. Conditions:The number of pods in the PodResizePending state is below the 20% threshold.At least 5 pods were successfully updated If any condition fails, a rollingRestart will be applied.CR example:The Automation Strategy can be configured at the cluster, namespace, or workload level.

### Title here

Some more tadjkwcjkwekdsj<br>

|   |   |   |
| - | - | - |
|   |   |   |
|   |   |   |
|   |   |   |

{% openapi-operation spec="UN" path="/geodata/api/vector/info" method="get" %}
[OpenAPI UN](https://feature.data-humdata-org.ahconu.org/geodata/openapi.json)
{% endopenapi-operation %}

{% openapi-operation spec="UN" path="/geodata/api/vector/filter" method="get" %}
[OpenAPI UN](https://feature.data-humdata-org.ahconu.org/geodata/openapi.json)
{% endopenapi-operation %}

{% openapi-operation spec="UN" path="/geodata/api/vector/simplify" method="get" %}
[OpenAPI UN](https://feature.data-humdata-org.ahconu.org/geodata/openapi.json)
{% endopenapi-operation %}

<table data-view="cards"><thead><tr><th></th><th data-type="content-ref"></th><th data-hidden data-card-cover data-type="image">Cover image</th><th data-hidden data-card-cover-dark data-type="image">Cover image (dark)</th></tr></thead><tbody><tr><td>conditional content</td><td><a href="https://app.gitbook.com/o/mZBC2rNDPE9yemCtBJTY/s/77WZwk5TAlC30s4FByo2/">Product Docs</a></td><td data-object-fit="cover"><a href=".gitbook/assets/CleanShot 2024-05-24 at 13.42.54@2x.png">CleanShot 2024-05-24 at 13.42.54@2x.png</a></td><td><a href=".gitbook/assets/Screenshot 2025-06-19 at 14.25.31.png">Screenshot 2025-06-19 at 14.25.31.png</a></td></tr><tr><td>ewdshjb shiuhwi</td><td></td><td><a href=".gitbook/assets/teapotnewA6.webp">teapotnewA6.webp</a></td><td><a href=".gitbook/assets/Screenshot 2025-06-19 at 14.45.36.png">Screenshot 2025-06-19 at 14.45.36.png</a></td></tr><tr><td>link</td><td></td><td><a href=".gitbook/assets/web2.webp">web2.webp</a></td><td><a href=".gitbook/assets/file.excalidraw (2).svg">file.excalidraw (2).svg</a></td></tr><tr><td></td><td></td><td><a href=".gitbook/assets/image.png">image.png</a></td><td><a href=".gitbook/assets/Latex.svg">Latex.svg</a></td></tr></tbody></table>



|                                                           |                                                                                                          |                                                                                                      |
| :-------------------------------------------------------: | -------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
|                        dfscbjwebhds                       |                                                                                                          |                                                                                                      |
|                        PKqqbuy22a6R                       |                                                                                                          |                                                                                                      |
|                                                           | Cover image                                                                                              | Cover image (dark)                                                                                   |
|                                                           | [CleanShot 2024-05-24 at 13.42.54@2x.png](.gitbook/assets/CleanShot%202024-05-24%20at%2013.42.54@2x.png) | [Screenshot 2025-06-19 at 14.25.31.png](.gitbook/assets/Screenshot%202025-06-19%20at%2014.25.31.png) |
|                            link                           | [teapotnewA6.webp](.gitbook/assets/teapotnewA6.webp)                                                     | [Screenshot 2025-06-19 at 14.45.36.png](.gitbook/assets/Screenshot%202025-06-19%20at%2014.45.36.png) |
|                            link                           | [web2.webp](.gitbook/assets/web2.webp)                                                                   | [file.excalidraw (2).svg](.gitbook/assets/file.excalidraw%20\(2\).svg)                               |
|                                                           | [image.png](.gitbook/assets/image.png)                                                                   | [Latex.svg](.gitbook/assets/Latex.svg)                                                               |
| ![](<.gitbook/assets/KeeperPAM Integration with Git.jpg>) |                                                                                                          |                                                                                                      |

{% columns %}
{% column %}

{% endcolumn %}

{% column %}

{% endcolumn %}
{% endcolumns %}

{% hint style="info" %}
my hiiiint
{% endhint %}

{% tabs %}
{% tab title="First Tab" %}
<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-cover data-type="image">Cover image</th></tr></thead><tbody><tr><td></td><td><a href=".gitbook/assets/morningtinypawws_det1+copy (1).jpeg">morningtinypawws_det1+copy (1).jpeg</a></td></tr><tr><td></td><td><a href=".gitbook/assets/CleanShot 2023-02-28 at 17.12.36@2x (1).png">CleanShot 2023-02-28 at 17.12.36@2x (1).png</a></td></tr></tbody></table>
{% endtab %}

{% tab title="Second Tab" %}
<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-cover data-type="image">Cover image</th></tr></thead><tbody><tr><td></td><td><a href="https://images.unsplash.com/photo-1763641683842-3b4f09950d67?crop=entropy&#x26;cs=srgb&#x26;fm=jpg&#x26;ixid=M3wxOTcwMjR8MHwxfHJhbmRvbXx8fHx8fHx8fDE3NjQwNTAzMDV8&#x26;ixlib=rb-4.1.0&#x26;q=85">https://images.unsplash.com/photo-1763641683842-3b4f09950d67?crop=entropy&#x26;cs=srgb&#x26;fm=jpg&#x26;ixid=M3wxOTcwMjR8MHwxfHJhbmRvbXx8fHx8fHx8fDE3NjQwNTAzMDV8&#x26;ixlib=rb-4.1.0&#x26;q=85</a></td></tr><tr><td></td><td><a href="https://images.unsplash.com/photo-1743961117237-a65e1abcab84?crop=entropy&#x26;cs=srgb&#x26;fm=jpg&#x26;ixid=M3wxOTcwMjR8MHwxfHJhbmRvbXx8fHx8fHx8fDE3NjQwNTAzMDV8&#x26;ixlib=rb-4.1.0&#x26;q=85">https://images.unsplash.com/photo-1743961117237-a65e1abcab84?crop=entropy&#x26;cs=srgb&#x26;fm=jpg&#x26;ixid=M3wxOTcwMjR8MHwxfHJhbmRvbXx8fHx8fHx8fDE3NjQwNTAzMDV8&#x26;ixlib=rb-4.1.0&#x26;q=85</a></td></tr></tbody></table>
{% endtab %}
{% endtabs %}

#### ewdbubw2ejks

newkdsnck,me dm,s

<a href="./#my-heading" class="button secondary" data-icon="paw">Tint color</a>

<a href="spider/" class="button primary" data-icon="spade">Primary color</a>

<figure><img src=".gitbook/assets/CleanShot 2023-02-28 at 17.12.36@2x (1).png" alt=""><figcaption></figcaption></figure>

<details>

<summary></summary>

dchbjkens

dbsknjz

</details>

{% hint style="info" %}
message her

e
{% endhint %}

{% columns %}
{% column %}
<details>

<summary>dhjbschjkbds</summary>

dsbajknxns

</details>
{% endcolumn %}

{% column %}
```

// Some code
```
{% endcolumn %}
{% endcolumns %}

<table><thead><tr><th></th><th data-type="image"></th><th data-type="content-ref"></th></tr></thead><tbody><tr><td>Alpha</td><td></td><td><a href="./">.</a></td></tr><tr><td>Beta <img src=".gitbook/assets/CleanShot 2023-02-28 at 17.12.36@2x (1).png" alt="" data-size="line"></td><td></td><td><a href="spider/">spider</a></td></tr><tr><td>Omega </td><td></td><td><a href="my-group/wolfff/">wolfff</a></td></tr></tbody></table>

{% include ".gitbook/includes/duis-vel-lacus-sit-amet-dolor.md" %}

<img src=".gitbook/assets/file.excalidraw (1).svg" alt="" class="gitbook-drawing">

{% content-ref url="spider/" %}
[spider](spider/)
{% endcontent-ref %}

***

<figure><img src=".gitbook/assets/02copy_e10246bc-98bb-4363-b06b-35d81f1ac8ad.webp" alt=""><figcaption></figcaption></figure>

{% embed url="https://glif.app/@dham/glifs/cm8ekte9h000el40c4kpcqwep" %}



{% include ".gitbook/includes/cards-test.md" %}

<figure><img src=".gitbook/assets/CleanShot 2023-01-25 at 19.27.15@2x.png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/morningtinypawws_det1+copy (1).jpeg" alt=""><figcaption></figcaption></figure>

Typing and referencing another page [#my-heading](./#my-heading "mention")

|       |                                                                |      |
| ----- | -------------------------------------------------------------- | ---- |
| edwe  | text                                                           |      |
| here  | can't type                                                     | 1234 |
| cant  |                                                                | nope |
|       | ![](<.gitbook/assets/Screenshot 2025-01-17 at 8.18.39 PM.png>) |      |

[Storylane ](#user-content-fn-1)[^1]records the full, no-code replica (HTML and CSS) of each screen, allowing you to fully tailor it later for your audience. Best when you need to edit screens and create a sales demo environment.

(For example, capturing your product's dashboard to personalize the logo for different customers, remove/blur elements, add different personalization tokens, add media, or customize HTML...)

{% @storylane/embed subdomain="app" linkvalue="d7h8qoqynzgn" url="https://app.storylane.io/share/d7h8qoqynzgn" %}

* Open the tab you wish to capture.
* Launch Storylane's Chrome Extension.
* Click "Create New Demo" (or Add to Existing Demo, if you have a demo already created)

{% stepper %}
{% step %}
**Prepare Ingredients**

Gather flour, sugar, salt, yeast, milk, butter, and eggs.

<figure><img src="https://images.unsplash.com/photo-1450862479751-84eeaf2fcca4?crop=entropy&#x26;cs=srgb&#x26;fm=jpg&#x26;ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHw5fHxjcm9pc3NhbnR8ZW58MHx8fHwxNzM0MDIxMTg3fDA&#x26;ixlib=rb-4.0.3&#x26;q=85" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Make Dough**

Mix dry ingredients, add wet ingredients, and knead until smooth.
{% endstep %}
{% endstepper %}

{% stepper %}
{% step %}
**Prepare Ingredients**:

Gather flour, sugar, salt, yeast, milk, butter, and eggs.

1. **Make Dough**: Mix dry ingredients, add wet ingredients, and knead until smooth.
2. **Chill Dough**: Refrigerate the dough for at least 30 minutes.
3. **Roll and Fold**: Roll out dough, layer with butter, and fold several times.
4. **Shape Croissants**: Cut into triangles and roll into crescent shapes.
5. **Proof Croissants**: Let them rise until doubled in size.
6. **Preheat Oven**: Set your oven to 375°F (190°C).
7. **Bake**: Bake for 15-20 minutes, or until golden brown.
8. **Prepare Ingredients**: Gather flour, sugar, salt, yeast, milk, butter, and eggs.
9. **Make Dough**: Mix dry ingredients, add wet ingredients, and knead until smooth.
10. **Chill Dough**: Refrigerate the dough for at least 30 minutes.
11. **Roll and Fold**: Roll out dough, layer with butter, and fold several times.
12. **Shape Croissants**: Cut into triangles and roll into crescent shapes.
13. **Proof Croissants**: Let them rise until doubled in size.
14. **Preheat Oven**: Set your oven to 375°F (190°C).
15. **Bake**: Bake for 15-20 minutes, or until golden br

\{% endstep %

<figure><img src=".gitbook/assets/Screenshot 2025-01-17 at 10.21.30 PM.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Make Dough**:

Making a change

* **Chill Dough**: Refrigerate the dough for at least 30 minutes.
* **Roll and Fold**: Roll out dough, layer with butter, and fold several times.
* **Shape Croissants**: Cut into triangles and roll into crescent shapes.
* **Proof Croissants**: Let them rise until doubled in size.
* **Preheat Oven**: Set your oven to 375°F (190°C).
* **Bake**: Bake for 15-20 minutes, or until golden brown.
* **Prepare Ingredients**: Gather flour, sugar, salt, yeast, milk, butter, and eggs.
* **Make Dough**: Mix dry ingredients, add wet ingredients, and knead until smooth.
* **Chill Dough**: Refrigerate the dough for at least 30 minutes.
* **Roll and Fold**: Roll out dough, layer with butter, and fold several times.
* **Shape Croissants**: Cut into triangles and roll into crescent shapes.
* **Proof Croissants**: Let them rise until doubled in size.

<figure><img src=".gitbook/assets/CleanShot 2023-01-25 at 19.27.15@2x.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
Step 3 Adding smth here
{% endstep %}

{% step %}

{% endstep %}

{% step %}

{% endstep %}

{% step %}

{% endstep %}
{% endstepper %}

1. **Make Dough**: Mix dry ingredients, add wet , and knead until smooth.
2. **Chill Dough**: Refrigerate the dough for at least 30 minutes.
3. **Roll and Fold**: Roll out dough, layer with butter, and fold several times.
4. **Shape Croissants**: Cut into triangles and roll into crescent shapes.
5. **Proof Croissants**: Let them rise until doubled in size.
6. **Preheat Oven**: Set your oven to 375°F (190°C).
7. **Bake**: Bake for 15-20 minutes, or until golden brown.
8. **Prepare Ingredients**: Gather flour, sugar, salt, yeast, milk, butter, and eggs.
9. **Make Dough**: Mix dry ingredients, add wet ingredients, and knead until smooth.
10. **Chill Dough**: Refrigerate the dough for at least 30 minutes.
11. **Roll and Fold**: Roll out dough, layer with butter, and fold several times.
12. **Shape Croissants**: Cut into triangles and roll into crescent shapes.
13. **Proof Croissants**: Let them rise until doubled in size.
14. **Preheat Oven**: Set your oven to 375°F (190°C).
15. **Bake**: Bake for 15-20 minutes, or until golden br

changes

{% include ".gitbook/includes/ingredients.md" %}

{% stepper %}
{% step %}

{% endstep %}

{% step %}

{% endstep %}

{% step %}

{% endstep %}

{% step %}

{% endstep %}
{% endstepper %}

### MY heading

<details>

<summary></summary>



</details>

<figure><img src=".gitbook/assets/02copy_e10246bc-98bb-4363-b06b-35d81f1ac8ad.webp" alt=""><figcaption></figcaption></figure>

### Verify Signing

From a repository, let's do a quick empty commit to test the signing process:

```
git commit --allow-empty -m "Test commit with SSH signing"
```

This immediately will trigger a Keeper dialog to authorize the key.

<figure><img src=".gitbook/assets/Screenshot 2025-01-17 at 8.18.39 PM.png" alt=""><figcaption></figcaption></figure>

To verify that the signature was applied to the commit, run the following:

```
git log --show-signature
```

The response will display something like this:

```
commit 52319faf2e7c02a (HEAD -> main)
Good "git" signature for craig@keeperdemo.io with ECDSA key SHA256:xxxxxxx
Author: Craig Lurey <craig@keeperdemo.io>
Date:   Fri Jan 17 20:18:19 2025 -0800

    Test commit with SSH signing
```

Setup is complete.

<figure><img src=".gitbook/assets/KeeperPAM Integration with Git.jpg" alt=""><figcaption></figcaption></figure>

Keeper's SSH Agent integrates seamlessly with Git for authentication and commit signing, ensuring private keys are securely stored in the Keeper Vault instead of being saved locally on the device. This approach enhances security by protecting sensitive keys from local exposure.

In this guide, we'll create and configure separate authentication and signing keys for use with GitHub, all managed securely by Keeper. Using distinct keys for authentication and signing helps maintain a clear separation of roles, further strengthening your security posture.

<figure><img src="https://images.unsplash.com/photo-1764513168260-391d5a3ea21a?crop=entropy&#x26;cs=srgb&#x26;fm=jpg&#x26;ixid=M3wxOTcwMjR8MHwxfHJhbmRvbXx8fHx8fHx8fDE3NjY0ODA5NjV8&#x26;ixlib=rb-4.1.0&#x26;q=85" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/Screenshot 2025-01-17 at 10.21.30 PM.png" alt=""><figcaption></figcaption></figure>

## Prerequisites

* Ensure that [SSH Agent is active](/broken/pages/vQsOJxrMLWwGa6F7vcBP) on the Keeper Desktop
* [Terminal Configuration](/broken/pages/vQsOJxrMLWwGa6F7vcBP#terminal-configuration) is performed

## Features

* [GitHub Authentication](./#github-authentication)
* [Signing Commits](./#signing-commits)

## GitHub Authentication

To authenticate with GitHub using Keeper, follow the below steps.

{% stepper %}
{% step %}
### Create a Keeper record

* Create a record in Keeper such as an **SSH Key** type or **PAM User** type.
* Generate a strong password
{% endstep %}

{% step %}
### Generate SSH Key

Generate SSH key on your terminal with the password generated by Keeper. For example:

```
ssh-keygen -t ecdsa -b 521 -C "craig@keeperdemo.io"

Enter passphrase (empty for no passphrase): *********
Enter same passphrase again: *********
```

This will create the public and private keys locally on your machine.

For example:

```
/Users/craig/.ssh/id_ecdsa
/Users/craig/.ssh/id_ecdsa.pub
```
{% endstep %}

{% step %}
### Add Key to Record

Add the contents from the public and private keys generated in Step 2 into the Keeper record. Copy paste the Public Key and Private Key into the fields of Keeper.

<div align="left"><figure><img src=".gitbook/assets/Screenshot 2025-01-17 at 10.21.30 PM.png" alt="" width="375"><figcaption><p>Keeper SSH Key for Github Authentication</p></figcaption></figure></div>
{% endstep %}

{% step %}
### Add Key to Github

* From Github.com, go to **Settings** > **SSH and GPG keys** > **New SSH Key** > and select Key type of "**Authentication Key**".&#x20;
* Assign a title, and paste the **public key** contents from `id_ecdsa.pub` in Step 2.
* Save the key.
{% endstep %}

{% step %}
### Add Key to SSH Agent

From the Keeper Desktop App, open **Settings** > **Developer** > **SSH Agent** > **Edit** and select your "Github Auth key" created in step3  from the list of available keys.

Click "**Update**" to save the settings.

<div align="left"><figure><img src=".gitbook/assets/Screenshot 2025-01-17 at 10.43.06 PM.png" alt="" width="375"><figcaption><p>Select Github Auth Key from Keeper SSH Agent</p></figcaption></figure></div>
{% endstep %}

{% step %}
### Delete the local key

At this point, it's a good idea to delete the local key, since it is now stored and managed by Keeper.  In this case, you can delete both the public and private key.

```
rm /Users/craig/.ssh/id_ecdsa
rm /Users/craig/.ssh/id_ecdsa.pub
```
{% endstep %}

{% step %}
### Authenticating with Github

From a terminal in some repo, perform an authorized request with Github:

```
git pull
```
{% endstep %}

{% step %}
This immediately will trigger a Keeper dialog to authorize the Github Authentication key.

<figure><img src=".gitbook/assets/Screenshot 2025-01-17 at 10.19.07 PM.png" alt=""><figcaption><p>Authorize the use of Github Auth Key in Keeper</p></figcaption></figure>

Clicking "Authorize" will use the key stored in Keeper to authenticate with Github.

Your setup is complete.
{% endstep %}
{% endstepper %}

## Signing Commits

{% tabs %}
{% tab title="First Tab" %}
<figure><img src="https://images.unsplash.com/photo-1764591702433-4a304936c966?crop=entropy&#x26;cs=srgb&#x26;fm=jpg&#x26;ixid=M3wxOTcwMjR8MHwxfHJhbmRvbXx8fHx8fHx8fDE3NjY0ODA5OTZ8&#x26;ixlib=rb-4.1.0&#x26;q=85" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}

To sign GitHub commits with Keeper, we will create a separate key that is specifically used for the signing process. Follow the steps below.

{% stepper %}
{% step %}
### Create a Keeper record

* Create a record in Keeper such as an **SSH Key** type or **PAM User** type.
* Generate a strong password
{% endstep %}

{% step %}
### Generate SSH Key

Generate SSH key on your terminal with the password generated by Keeper. For example:

```
ssh-keygen -t ecdsa -b 521 -C "craig@keeperdemo.io"

Enter passphrase (empty for no passphrase): *********
Enter same passphrase again: *********
```

This will create the public and private keys locally on your machine.

For example:

```
/Users/craig/.ssh/id_ecdsa
/Users/craig/.ssh/id_ecdsa.pub
```
{% endstep %}

{% step %}
### Add Key to Record

Add the contents from the public and private keys generated in Step 2 into the Keeper record. Copy paste the Public Key and Private Key into the fields of Keeper.

<div align="left"><figure><img src=".gitbook/assets/Screenshot 2025-01-17 at 7.59.02 PM.png" alt="" width="375"><figcaption></figcaption></figure></div>
{% endstep %}

{% step %}
### Add Key to Github

* From Github, go to Settings > SSH and GPG keys > New SSH Key > and select Key type of "Signing Key".&#x20;
* Assign a title, and paste the public key contents from Step 2.
* Save the key.
{% endstep %}

{% step %}
### Add Key to SSH Agent

From Keeper, open **Settings** > **Developer** > **SSH Agent** > **Edit** and select the Github signing key.

Click "Update" to save the settings.
{% endstep %}

{% step %}
### Delete the local private key

<figure><img src=".gitbook/assets/KeeperPAM Integration with Git.jpg" alt=""><figcaption></figcaption></figure>

We will only delete the local private key, since it is now stored and managed by Keeper. The public key (xxx.pub) needs to stay, as it will be used for identifying which key to use for signing.

```
rm /Users/craig/.ssh/id_ecdsa
```

Let's also rename the public key to something more specific:

```
cd ~/.ssh
mv id_ecdsa.pub git_signing_key.pub
```

Place the username and the contents of the public key into a file called `~/.ssh/allowed_signers`. For example:

```
craig@keeperdemo.io <contents of git_signing_key.pub>
AikidoMiddleware::class,
// Append AikidoMiddleware to other groups ('api' for example)

```

In this example, the file looks like this:

<figure><img src=".gitbook/assets/KeeperPAM Integration with Git.jpg" alt=""><figcaption></figcaption></figure>

{% code overflow="wrap" %}
```
craig@keeperdemo.io ecdsa-sha2-nistp521 AAAAE2VjZHNhLXNoYTItbmlzdHA1MjEAAAAIbmlzdHA1MjEAAACFBAD2VeqOZ9bk2ABF6AZ63qJY2sDfz0kJJPfDW0zpres0/p1YGGJBYtyU4l3nIgwx0K2iEKFty429N2NNfIMBsqI+ngDq3/VGaexmZxymJnCzOl9+J1IQr6u05jZHLsk1FOALjOSm9jv4bF/DyK4oh5shKMlTHAeDWPfqMd3JwncSYBzKfA== craig@keeperdemo.io
```
{% endcode %}
{% endstep %}

{% step %}
### Enable Git Signing

From the terminal, instruct Github to sign commits using this new key and allowed signers.

```
git config --global user.signingkey ~/.ssh/git_signing_key.pub
git config --global gpg.format ssh
git config --global commit.gpgsign true
git config --global gpg.ssh.allowedSignersFile ~/.ssh/allowed_signers
```

This basically has the effect of adding several lines to `~/.gitconfig` and applies the changes globally. You can also configure individual repos instead of making these changes globally.
{% endstep %}

{% step %}
### Verify Signing

From a repository, let's do a quick empty commit to test the signing process:

```
git commit --allow-empty -m "Test commit with SSH signing"
```

This immediately will trigger a Keeper dialog to authorize the key.

<figure><img src=".gitbook/assets/Screenshot 2025-01-17 at 8.18.39 PM.png" alt=""><figcaption></figcaption></figure>

To verify that the signature was applied to the commit, run the following:

```
git log --show-signature
```

The response will display something like this:

<figure><img src=".gitbook/assets/Screenshot 2025-01-17 at 8.18.39 PM.png" alt=""><figcaption></figcaption></figure>

```
commit 52319faf2e7c02a (HEAD -> main)
Good "git" signature for craig@keeperdemo.io with ECDSA key SHA256:xxxxxxx
Author: Craig Lurey <craig@keeperdemo.io>
Date:   Fri Jan 17 20:18:19 2025 -0800

    Test commit with SSH signing
    AikidoMiddleware::class,
// Append AikidoMiddleware to other groups ('api' for example)

```

Setup is complete.
{% endstep %}
{% endstepper %}

<div><figure><img src=".gitbook/assets/CleanShot 2023-02-28 at 17.12.36@2x (1).png" alt=""><figcaption></figcaption></figure> <figure><img src=".gitbook/assets/KeeperPAM Integration with Git.jpg" alt=""><figcaption></figcaption></figure> <figure><img src=".gitbook/assets/Screenshot 2025-01-17 at 10.21.30 PM.png" alt=""><figcaption></figcaption></figure></div>

<table><thead><tr><th width="243.1431884765625" align="center"></th><th width="135.08587646484375" valign="middle"></th><th data-type="checkbox"></th><th></th></tr></thead><tbody><tr><td align="center">dfscbjwebhds</td><td valign="middle">NaN</td><td>false</td><td></td></tr><tr><td align="center">PKqqbuy22a6R</td><td valign="middle">23456</td><td>true</td><td><button type="button" class="button primary" data-action="search" data-icon="magnifying-glass">Searctexth...</button></td></tr><tr><td align="center">link</td><td valign="middle"></td><td>false</td><td><a href=".gitbook/assets/Screenshot%202025-06-19%20at%2014.45.36.png">Screenshot 2025-06-19 at 14.45.36.png</a></td></tr><tr><td align="center"></td><td valign="middle"></td><td>false</td><td>Cover image (dark)</td></tr><tr><td align="center"></td><td valign="middle"></td><td>false</td><td></td></tr><tr><td align="center">link</td><td valign="middle">text here</td><td>false</td><td><a href=".gitbook/assets/file.excalidraw%20(2).svg">file.excalidraw (2).svg</a></td></tr><tr><td align="center"></td><td valign="middle">can'r reprodcue</td><td>false</td><td><a href=".gitbook/assets/Latex.svg">Latex.svg</a></td></tr><tr><td align="center"><img src=".gitbook/assets/KeeperPAM Integration with Git.jpg" alt=""></td><td valign="middle"><i class="fa-layer-plus">:layer-plus:</i> GitBook</td><td>false</td><td><code class="expression"></code></td></tr></tbody></table>

{% tabs %}
{% tab title="First Tab" %}
<figure><img src=".gitbook/assets/KeeperPAM Integration with Git.jpg" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}

[^1]: annotate
