---
title: Provisionner un profil Wi-Fi via un site web
description: Autorisez les utilisateurs à télécharger un profil à partir d’un site Web et à le configurer.
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: e34c83fbee100316256293e27eac96dae685c37d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941338"
---
# <a name="provision-a-wi-fi-profile-via-a-website"></a><span data-ttu-id="f0a10-103">Provisionner un profil Wi-Fi via un site web</span><span class="sxs-lookup"><span data-stu-id="f0a10-103">Provision a Wi-Fi profile via a website</span></span>

<span data-ttu-id="f0a10-104">Le flux de travail décrit dans cette rubrique a été introduit dans Windows 10, version 2004.</span><span class="sxs-lookup"><span data-stu-id="f0a10-104">The workflow described in this topic was introduced in Windows 10, version 2004.</span></span> <span data-ttu-id="f0a10-105">Cette rubrique montre comment configurer un site Web pour qu’un utilisateur puisse configurer un profil pour un réseau Passpoint (ou pour un réseau normal) avant de se déplacer dans la plage des points d’accès Wi-Fi correspondants.</span><span class="sxs-lookup"><span data-stu-id="f0a10-105">This topic shows how to configure a website so that a user can provision a profile for a Passpoint network (or for a normal network) prior to moving into range of the corresponding Wi-Fi access points.</span></span> <span data-ttu-id="f0a10-106">Un exemple de scénario est celui d’un utilisateur qui envisage de visiter un aéroport ou une conférence pour la première fois, et il souhaite préparer à l’avance en téléchargeant et en configurant un profil à la résidence.</span><span class="sxs-lookup"><span data-stu-id="f0a10-106">An example scenario is that of a user who might be planning to visit an airport or a conference for the first time, and they want to prepare in advance by downloading and provisioning a profile at home.</span></span>

<span data-ttu-id="f0a10-107">En tant que développeur, vous activez le workflow en fournissant un profil XML et en configurant un site Web.</span><span class="sxs-lookup"><span data-stu-id="f0a10-107">As a developer, you enable the workflow by providing an XML profile, and configuring a website.</span></span> <span data-ttu-id="f0a10-108">Vos utilisateurs peuvent ensuite approvisionner un profil de Wi-Fi en le téléchargeant à partir de votre site Web via un navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="f0a10-108">Your users can then provision a Wi-Fi profile by downloading it from your website via a web browser.</span></span> <span data-ttu-id="f0a10-109">Sur l’appareil de l’utilisateur, le profil de Wi-Fi est ensuite configuré à l’aide de l’activation d’URI et de l’application **paramètres** Windows.</span><span class="sxs-lookup"><span data-stu-id="f0a10-109">On the user's device, the Wi-Fi profile is then provisioned by using URI activation and the Windows **Settings** app.</span></span>

<span data-ttu-id="f0a10-110">Ce flux de travail remplace le mécanisme dans Internet Explorer pour l’approvisionnement des profils Wi-Fi, qui s’appuie sur des API JavaScript spécifiques à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f0a10-110">This workflow supersedes the mechanism in Internet Explorer for provisioning Wi-Fi profiles, which relies on Microsoft-specific JavaScript APIs.</span></span> <span data-ttu-id="f0a10-111">Ce nouveau flux de travail est censé fonctionner avec tous les principaux navigateurs.</span><span class="sxs-lookup"><span data-stu-id="f0a10-111">This new workflow is expected to work with all major browsers.</span></span>

## <a name="the-workflow-in-more-detail"></a><span data-ttu-id="f0a10-112">Le flux de travail plus en détail</span><span class="sxs-lookup"><span data-stu-id="f0a10-112">The workflow in more detail</span></span>

<span data-ttu-id="f0a10-113">Vous pouvez activer ce flux de travail à partir d’un lien hypertexte qui comprend comme argument l’URI de téléchargement du document XML d’approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="f0a10-113">You can activate this workflow from a hyperlink that includes as an argument the download URI of the provisioning XML document.</span></span>

```xml
ms-settings:wifi-provisioning?uri={download_uri}
```

<span data-ttu-id="f0a10-114">Par exemple, le balisage HTML suivant donne un lien pour installer le ou les profils qui se trouvent dans un document hypothétique `http://contoso.com/ProvisioningDoc.xml` .</span><span class="sxs-lookup"><span data-stu-id="f0a10-114">For example, the following HTML markup gives a link to install the profile(s) that are found in a hypothetical document `http://contoso.com/ProvisioningDoc.xml`.</span></span>

```html
<a href="ms-settings:wifi-provisioning?uri=http://contoso.com/ProvisioningDoc.xml">Install</a>
```

<span data-ttu-id="f0a10-115">Votre code XML doit adhérer au schéma de configuration (voir [approvisionnement de comptes](/windows-hardware/drivers/mobilebroadband/account-provisioning)).</span><span class="sxs-lookup"><span data-stu-id="f0a10-115">Your XML must adhere to the provisioning schema (see [Account provisioning](/windows-hardware/drivers/mobilebroadband/account-provisioning)).</span></span> <span data-ttu-id="f0a10-116">Votre code XML doit également inclure un ou plusieurs éléments [WLANProfile](./wlan-profileschema-wlanprofile-element.md)   .</span><span class="sxs-lookup"><span data-stu-id="f0a10-116">Your XML must also include one or more [WLANProfile](./wlan-profileschema-wlanprofile-element.md) elements.</span></span><span data-ttu-id="f0a10-117">Chaque profil sera affiché dans la boîte de dialogue **Ajouter** décrite ci-après.</span><span class="sxs-lookup"><span data-stu-id="f0a10-117"> Each profile will be displayed in the **Add** dialog described next.</span></span>

<span data-ttu-id="f0a10-118">Quand l’utilisateur clique sur votre lien HTML, le flux de travail d’installation est appelé dans l’application **paramètres** .</span><span class="sxs-lookup"><span data-stu-id="f0a10-118">When the user clicks your HTML link, the installation workflow is invoked in the **Settings** app.</span></span> <span data-ttu-id="f0a10-119">Votre document XML de provisionnement est téléchargé par l’application **paramètres** .</span><span class="sxs-lookup"><span data-stu-id="f0a10-119">Your provisioning XML document is downloaded by the **Settings** app.</span></span> <span data-ttu-id="f0a10-120">Une fois téléchargés, des informations sur les profils, la signature et le signataire sont affichées (à condition que le document adhère au schéma).</span><span class="sxs-lookup"><span data-stu-id="f0a10-120">Once it's downloaded, information about the profiles, signature, and signer are displayed (provided that the document adheres to the schema).</span></span>

![L’application paramètres](images/install-dialog.png)

<span data-ttu-id="f0a10-122">Le bouton **Ajouter** dans la boîte de dialogue de l’application **paramètres** est activé uniquement si le fichier de configuration est signé et approuvé.</span><span class="sxs-lookup"><span data-stu-id="f0a10-122">The **Add** button in the dialog in the **Settings** app is enabled only if the provisioning file is signed and trusted.</span></span>

## <a name="in-your-web-page-determine-whether-this-workflow-is-supported"></a><span data-ttu-id="f0a10-123">Dans votre page Web, déterminez si ce flux de travail est pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0a10-123">In your web page, determine whether this workflow is supported</span></span>

<span data-ttu-id="f0a10-124">JavaScript n’a aucun moyen de déterminer la version de build exacte de Windows.</span><span class="sxs-lookup"><span data-stu-id="f0a10-124">There is no way in JavaScript to determine the exact build version of Windows.</span></span> <span data-ttu-id="f0a10-125">Toutefois, si votre utilisateur utilise le navigateur Web Microsoft Edge, vous pouvez déterminer la version de Edge en inspectant la valeur de l' `User-agent` en-tête http.</span><span class="sxs-lookup"><span data-stu-id="f0a10-125">But if your user is using the Microsoft Edge web browser, then you can determine the version of Edge by inspecting the value of the `User-agent` HTTP header.</span></span> <span data-ttu-id="f0a10-126">Si la version est supérieure ou égale à `18.nnnnn` , le flux de travail est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f0a10-126">If the version is greater than or equal to `18.nnnnn`, then the workflow is supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0a10-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f0a10-127">Related topics</span></span>

* [<span data-ttu-id="f0a10-128">Approvisionnement de comptes</span><span class="sxs-lookup"><span data-stu-id="f0a10-128">Account provisioning</span></span>](/windows-hardware/drivers/mobilebroadband/account-provisioning)
* [<span data-ttu-id="f0a10-129">Élément WLANProfile</span><span class="sxs-lookup"><span data-stu-id="f0a10-129">WLANProfile element</span></span>](./wlan-profileschema-wlanprofile-element.md)