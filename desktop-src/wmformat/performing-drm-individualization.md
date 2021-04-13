---
title: Réalisation de l’individualisation DRM
description: Réalisation de l’individualisation DRM
ms.assetid: daad1a31-f0a7-43ab-b920-94b9f050a44e
keywords:
- SDK Windows Media format, API étendues du client DRM
- Windows Media Format SDK, API étendues du client
- Windows Media Format SDK, API étendues
- Windows Media Format SDK, API
- Kit de développement logiciel (SDK) Windows Media format, gestion des droits numériques (DRM)
- Windows Media Format SDK, individualisation DRM
- Windows Media Format SDK, individualisation
- gestion des droits numériques (DRM), API étendues du client
- DRM (gestion des droits numériques), API étendues du client
- gestion des droits numériques (DRM), API étendues
- DRM (gestion des droits numériques), API étendues
- gestion des droits numériques (DRM), API
- DRM (gestion des droits numériques), API
- gestion des droits numériques (DRM), individualisation
- DRM (gestion des droits numériques), individualisation
- gestion des droits numériques (DRM), individualisation DRM
- DRM (gestion des droits numériques), individualisation DRM
- API étendues du client DRM, individualisation
- API étendues clientes, individualisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d8f7f04add4ed626985651d5220e69ea713e4d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310897"
---
# <a name="performing-drm-individualization"></a><span data-ttu-id="2d4c7-122">Réalisation de l’individualisation DRM</span><span class="sxs-lookup"><span data-stu-id="2d4c7-122">Performing DRM Individualization</span></span>

<span data-ttu-id="2d4c7-123">L’individualisation est le processus qui consiste à mettre à jour le composant DRM sur l’ordinateur client, à le chiffrer et à le rendre unique.</span><span class="sxs-lookup"><span data-stu-id="2d4c7-123">Individualization is the process of updating the DRM component on the client computer, encrypting it, and making it unique.</span></span> <span data-ttu-id="2d4c7-124">Lorsqu’un ordinateur est individualisé, le composant DRM est lié à l’ordinateur et ne peut pas décoder le contenu sur un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2d4c7-124">When a computer is individualized, the DRM component is tied to the computer and will not be able to decode content on any other computer.</span></span> <span data-ttu-id="2d4c7-125">Les API étendues du client Windows Media DRM prennent en charge l’individualisation du composant DRM sur les ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="2d4c7-125">The Windows Media DRM Client Extended APIs provide support for individualizing the DRM component on client computers.</span></span>

<span data-ttu-id="2d4c7-126">L’individualisation est effectuée en appelant la méthode [**IWMDRMSecurity ::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) .</span><span class="sxs-lookup"><span data-stu-id="2d4c7-126">Individualization is performed by calling the [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) method.</span></span> <span data-ttu-id="2d4c7-127">Vous pouvez appeler **PerformSecurityUpdate** pour qu’il soit personnalisable uniquement si la version sur le serveur est plus récente que celle installée sur l’ordinateur client, ou vous pouvez forcer l’individualisation sans tenir compte des versions de sécurité relatives.</span><span class="sxs-lookup"><span data-stu-id="2d4c7-127">You can call **PerformSecurityUpdate** so that it will individualize only if the version on the server is newer than the one installed on the client computer, or you can force individualization without regard to the relative security versions.</span></span> <span data-ttu-id="2d4c7-128">L’indicateur de l’individualisation en tant que nécessaire est la \_ sécurité WMDRM \_ perform \_ indiv.</span><span class="sxs-lookup"><span data-stu-id="2d4c7-128">The flag for as-needed individualization is WMDRM\_SECURITY\_PERFORM\_INDIV.</span></span> <span data-ttu-id="2d4c7-129">L’indicateur de l’individualisation forcée est la \_ sécurité WMDRM \_ perform \_ force \_ indiv.</span><span class="sxs-lookup"><span data-stu-id="2d4c7-129">The flag for forced individualization is WMDRM\_SECURITY\_PERFORM\_FORCE\_INDIV.</span></span>

<span data-ttu-id="2d4c7-130">**PerformSecurityUpdate** est un appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2d4c7-130">**PerformSecurityUpdate** is an asynchronous call.</span></span> <span data-ttu-id="2d4c7-131">Elle retournera rapidement, puis générera des événements pour fournir des informations d’État sur le processus d’individualisation.</span><span class="sxs-lookup"><span data-stu-id="2d4c7-131">It will return quickly and then generate events to provide status information about the individualization process.</span></span> <span data-ttu-id="2d4c7-132">La majorité des événements générés sont les événements **MEWMDRMIndividualizationProgress** et chacun d’eux est associé à une interface [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="2d4c7-132">The majority of the events generated will be **MEWMDRMIndividualizationProgress** events, and each has an associated [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) interface.</span></span> <span data-ttu-id="2d4c7-133">Pour obtenir l’interface d’État, vous devez appeler **IMFMediaEvent :: GetValue** pour récupérer un pointeur **IUnknown** qui se trouve sur le même objet, puis l’interroger pour **IWMDRMIndividualizationStatus**.</span><span class="sxs-lookup"><span data-stu-id="2d4c7-133">To get the status interface, you must call **IMFMediaEvent::GetValue** to retrieve an **IUnknown** pointer that is on the same object and then query it for **IWMDRMIndividualizationStatus**.</span></span>

<span data-ttu-id="2d4c7-134">Vous pouvez obtenir des données pour une structure d’état de l' [**\_ \_ individualisation WM**](drmwm-individualize-status.md) en appelant [**IWMDRMIndividualizeStatus :: GetStatus**](iwmdrmindividualizationstatus-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="2d4c7-134">You can get data for a [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure by calling [**IWMDRMIndividualizeStatus::GetStatus**](iwmdrmindividualizationstatus-getstatus.md).</span></span> <span data-ttu-id="2d4c7-135">Chaque événement généré a son propre objet avec l’État. vous devez donc suivre le processus d’obtention de la valeur de l’événement et de l’interrogation de l’interface d’État à chaque fois.</span><span class="sxs-lookup"><span data-stu-id="2d4c7-135">Each event that is generated has its own object with status, so you must go through the process of getting the event value and querying for the status interface every time.</span></span>

<span data-ttu-id="2d4c7-136">Selon la taille du téléchargement, il peut y avoir des dizaines ou des centaines d’événements **MEWMDRMIndividualizationProgress** .</span><span class="sxs-lookup"><span data-stu-id="2d4c7-136">Depending on the size of the download, there may be dozens or hundreds of **MEWMDRMIndividualizationProgress** events.</span></span> <span data-ttu-id="2d4c7-137">Lorsque le processus d’individualisation est terminé, un événement **MEWMDRMIndividualizationCompleted** est généré.</span><span class="sxs-lookup"><span data-stu-id="2d4c7-137">When the individualization process is finished, an **MEWMDRMIndividualizationCompleted** event is generated.</span></span>

<span data-ttu-id="2d4c7-138">Lorsque l’individualisation est terminée, les seuls objets existants qui reflètent le nouvel État individualisé sont ceux qui héritent de [**IWMDRMSecurity**](iwmdrmsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="2d4c7-138">When individualization is completed, the only existing objects that will reflect the new individualized state are those that inherit from [**IWMDRMSecurity**](iwmdrmsecurity.md).</span></span> <span data-ttu-id="2d4c7-139">Tous les autres objets existants ne seront pas mis à jour.</span><span class="sxs-lookup"><span data-stu-id="2d4c7-139">All other existing objects will not be updated.</span></span> <span data-ttu-id="2d4c7-140">Vous devez libérer et recréer tous les autres objets pour qu’ils reflètent le nouvel État individualisé.</span><span class="sxs-lookup"><span data-stu-id="2d4c7-140">You must release and re-create any other objects so that they will reflect the new individualized state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d4c7-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2d4c7-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d4c7-142">**Exemple d’individualisation DRM**</span><span class="sxs-lookup"><span data-stu-id="2d4c7-142">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="2d4c7-143">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="2d4c7-143">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="2d4c7-144">**Utilisation du modèle d’événement Media Foundation**</span><span class="sxs-lookup"><span data-stu-id="2d4c7-144">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> <dt>

<span data-ttu-id="2d4c7-145">[Meilleures pratiques pour l’individualisation DRM Windows Media](/previous-versions/ms867216(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="2d4c7-145">[Windows Media DRM Individualization Best Practices](/previous-versions/ms867216(v=msdn.10))</span></span>
</dt> </dl>

 

 




