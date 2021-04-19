---
title: Pré-remise de licence
description: Pré-remise de licence
ms.assetid: 184d9118-5b60-4871-a1e3-75c45153460d
keywords:
- Windows Media Format SDK, pré-remise de licences
- Windows Media Format SDK, licences
- gestion des droits numériques (DRM), pré-remise de licences
- DRM (gestion des droits numériques), pré-remise de licences
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- API étendues du client DRM, pré-remise de licences
- API étendues clientes, pré-remise de licences
- pré-remise de licences
- licences, pré-remise de licences
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7691c48233ed986d85c47ae9c99df078d0ed1039
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510899"
---
# <a name="license-pre-delivery"></a><span data-ttu-id="84fbe-113">Pré-remise de licence</span><span class="sxs-lookup"><span data-stu-id="84fbe-113">License Pre-Delivery</span></span>

<span data-ttu-id="84fbe-114">La pré-remise de licence est le processus utilisé pour extraire des licences sur un ordinateur client de manière préventive.</span><span class="sxs-lookup"><span data-stu-id="84fbe-114">License pre-delivery is the process used to pull licenses to a client computer preemptively.</span></span> <span data-ttu-id="84fbe-115">Un scénario courant pour l’utilisation de la pré-remise est lorsqu’un utilisateur s’abonne à un service musical.</span><span class="sxs-lookup"><span data-stu-id="84fbe-115">A common scenario for using pre-delivery is when a user subscribes to a music service.</span></span> <span data-ttu-id="84fbe-116">Si vous n’avez pas besoin de licences, l’utilisateur doit attendre l’acquisition de la licence pour chaque nouvelle chanson.</span><span class="sxs-lookup"><span data-stu-id="84fbe-116">Without delivering licenses before they are needed, the user would have to wait for license acquisition for each new song.</span></span>

<span data-ttu-id="84fbe-117">Étant donné que la pré-remise n’est pas effectuée en réponse à une tentative d’accès, elle est généralement effectuée uniquement par le propriétaire du contenu.</span><span class="sxs-lookup"><span data-stu-id="84fbe-117">Because pre-delivery is not done as a response to attempted access, it is typically performed only by the content owner.</span></span> <span data-ttu-id="84fbe-118">Autrement dit, vous ne pouvez pré-fournir des licences que pour le contenu que vous contrôlez.</span><span class="sxs-lookup"><span data-stu-id="84fbe-118">That is, you can only pre-deliver licenses for content that you control.</span></span> <span data-ttu-id="84fbe-119">Le processus de pré-remise est une coordination entre un composant client et un serveur de licences créé à l’aide des objets du kit de développement logiciel (SDK) Windows Media Digital Rights Management.</span><span class="sxs-lookup"><span data-stu-id="84fbe-119">The pre-delivery process is a coordination between a client component and a license server built by using the objects of the Windows Media Digital Rights Management SDK.</span></span>

<span data-ttu-id="84fbe-120">La pré-remise de licence est similaire à l' [acquisition de licence non silencieuse](non-silent-license-acquisition.md).</span><span class="sxs-lookup"><span data-stu-id="84fbe-120">License pre-delivery is similar to [Non-Silent License Acquisition](non-silent-license-acquisition.md).</span></span> <span data-ttu-id="84fbe-121">Suivez les mêmes étapes, sauf que vous n’avez pas d’en-tête DRM à transmettre à [**IWMDRMLicenseManagement :: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md).</span><span class="sxs-lookup"><span data-stu-id="84fbe-121">Follow the same steps, except that you don't have a DRM header to pass to [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md).</span></span> <span data-ttu-id="84fbe-122">La méthode génère une stimulation qui n’est pas spécifique au contenu que vous pouvez envoyer à votre serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="84fbe-122">The method will generate a challenge that is not content-specific that you can send to your license server.</span></span>

<span data-ttu-id="84fbe-123">Vous pouvez également utiliser le [Gestionnaire de droits Windows Media](/previous-versions//bb676133(v=technet.10)) pour prédistribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="84fbe-123">Alternatively you can use the [Windows Media Rights Manager](/previous-versions//bb676133(v=technet.10)) to pre-deliver licenses.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84fbe-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="84fbe-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84fbe-125">**Acquisition de licences**</span><span class="sxs-lookup"><span data-stu-id="84fbe-125">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="84fbe-126">**Utilisation du modèle d’événement Media Foundation**</span><span class="sxs-lookup"><span data-stu-id="84fbe-126">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> </dl>

 

 