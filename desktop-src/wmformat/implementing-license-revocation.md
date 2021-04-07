---
title: Implémentation de la révocation des licences
description: Implémentation de la révocation des licences
ms.assetid: 50ecfeaa-89cd-4788-a25a-ee0ae8973bf0
keywords:
- Windows Media Format SDK, implémentation de la révocation des licences
- Windows Media Format SDK, révocation de licence
- Windows Media Format SDK, révocation des licences
- ASF (Advanced Systems Format), implémentation de la révocation des licences
- ASF (format avancé des systèmes), implémentation de la révocation des licences
- ASF (Advanced Systems Format), révocation de licence
- ASF (format de systèmes avancés), révocation de licence
- ASF (Advanced Systems Format), révocation des licences
- ASF (format des systèmes avancés), révocation des licences
- gestion des droits numériques (DRM), implémentation de la révocation des licences
- DRM (gestion des droits numériques), implémentation de la révocation des licences
- gestion des droits numériques (DRM), révocation des licences
- DRM (gestion des droits numériques), révocation de licence
- gestion des droits numériques (DRM), révocation des licences
- DRM (gestion des droits numériques), révocation des licences
- révocation de licence, implémentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e83bfb1a512b031f5b7c297ecede4ed33fba8f2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723570"
---
# <a name="implementing-license-revocation"></a><span data-ttu-id="2a3fb-119">Implémentation de la révocation des licences</span><span class="sxs-lookup"><span data-stu-id="2a3fb-119">Implementing License Revocation</span></span>

<span data-ttu-id="2a3fb-120">Le kit de développement logiciel (SDK) Windows Media Rights Manager 10 comprend une fonctionnalité appelée révocation de licence.</span><span class="sxs-lookup"><span data-stu-id="2a3fb-120">The Windows Media Rights Manager 10 SDK includes a feature called license revocation.</span></span> <span data-ttu-id="2a3fb-121">Cette fonctionnalité permet aux serveurs de licences de demander que les licences soient supprimées de l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="2a3fb-121">This feature enables license servers to request that licenses be removed from the client computer.</span></span> <span data-ttu-id="2a3fb-122">Le kit de développement logiciel (SDK) du format Windows Media fournit des méthodes qui traitent les messages de révocation et suppriment les licences du magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="2a3fb-122">The Windows Media Format SDK provides methods that process revocation messages and remove the licenses from the local license store.</span></span>

<span data-ttu-id="2a3fb-123">Le processus de révocation de licence est initié par un service fourni par l’émetteur de licence.</span><span class="sxs-lookup"><span data-stu-id="2a3fb-123">The license revocation process is initiated by a service provided by the license issuer.</span></span> <span data-ttu-id="2a3fb-124">Votre application peut héberger ce service, ou il peut s’agir d’une application Web.</span><span class="sxs-lookup"><span data-stu-id="2a3fb-124">Your application can host this service, or it can be a Web application.</span></span> <span data-ttu-id="2a3fb-125">Dans les deux cas, votre application doit être en mesure de recevoir une demande de licence créée par le service.</span><span class="sxs-lookup"><span data-stu-id="2a3fb-125">In either case, your application must be able to receive a license challenge created by the service.</span></span>

<span data-ttu-id="2a3fb-126">Pour supprimer des licences du magasin de licences, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="2a3fb-126">To remove licenses from the license store, perform the following steps:</span></span>

1.  <span data-ttu-id="2a3fb-127">Lors de la réception d’une demande de licence de l’émetteur de licence, appelez la fonction [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) pour créer un objet agent de révocation de licence et obtenir un pointeur vers l’interface [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) .</span><span class="sxs-lookup"><span data-stu-id="2a3fb-127">Upon receiving a license challenge from the license issuer, call the [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) function to create a license revocation agent object and obtain a pointer to the [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) interface.</span></span>
2.  <span data-ttu-id="2a3fb-128">Appelez la méthode [**IWMLicenseRevocationAgent :: GetLRBChallenge**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-getlrbchallenge) pour générer la réponse de stimulation.</span><span class="sxs-lookup"><span data-stu-id="2a3fb-128">Call the [**IWMLicenseRevocationAgent::GetLRBChallenge**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-getlrbchallenge) method to generate the challenge response.</span></span>
3.  <span data-ttu-id="2a3fb-129">Renvoyez la réponse de la demande de remboursement au composant du service de licence à partir duquel vous avez reçu le problème.</span><span class="sxs-lookup"><span data-stu-id="2a3fb-129">Send the challenge response back to the license service component from which you received the challenge.</span></span>
4.  <span data-ttu-id="2a3fb-130">Le composant de service de licence envoie un objet blob de révocation de licence (LRB) signé à votre application.</span><span class="sxs-lookup"><span data-stu-id="2a3fb-130">The license service component sends a signed license revocation blob (LRB) to your application.</span></span> <span data-ttu-id="2a3fb-131">Lorsque vous le recevez, appelez la méthode [**IWMLicenseRevocationAgent ::P rocesslrb**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-processlrb) .</span><span class="sxs-lookup"><span data-stu-id="2a3fb-131">When you receive it, call the [**IWMLicenseRevocationAgent::ProcessLRB**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-processlrb) method.</span></span> <span data-ttu-id="2a3fb-132">**ProcessLRB** crée un message d’accusé de réception que vous devez renvoyer au service de licence pour vérifier que les licences ont été supprimées.</span><span class="sxs-lookup"><span data-stu-id="2a3fb-132">**ProcessLRB** creates an acknowledgement message that you must send back to the license service to verify that the licenses were removed.</span></span>

> [!Note]  
> <span data-ttu-id="2a3fb-133">DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="2a3fb-133">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2a3fb-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2a3fb-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a3fb-135">**Activation de la prise en charge de DRM**</span><span class="sxs-lookup"><span data-stu-id="2a3fb-135">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="2a3fb-136">**Interface IWMLicenseRevocationAgent**</span><span class="sxs-lookup"><span data-stu-id="2a3fb-136">**IWMLicenseRevocationAgent Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent)
</dt> </dl>

 

 




