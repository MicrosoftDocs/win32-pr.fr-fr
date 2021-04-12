---
title: API étendues du client Windows Media DRM
description: API étendues du client Windows Media DRM
ms.assetid: c0397aa8-1f5a-48f5-a96b-555079e9a292
keywords:
- SDK Windows Media format, API étendues du client DRM
- Windows Media Format SDK, API étendues du client
- Windows Media Format SDK, API étendues
- Windows Media Format SDK, API
- Kit de développement logiciel (SDK) Windows Media format, gestion des droits numériques (DRM)
- gestion des droits numériques (DRM), API étendues du client
- DRM (gestion des droits numériques), API étendues du client
- gestion des droits numériques (DRM), API étendues
- DRM (gestion des droits numériques), API étendues
- gestion des droits numériques (DRM), API
- DRM (gestion des droits numériques), API
- API étendues du client DRM, à propos de
- API étendues du client, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01c33ef3649f2cda63713ebd22a0116fdd025144
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382035"
---
# <a name="windows-media-drm-client-extended-apis"></a><span data-ttu-id="d42d4-116">API étendues du client Windows Media DRM</span><span class="sxs-lookup"><span data-stu-id="d42d4-116">Windows Media DRM Client Extended APIs</span></span>

<span data-ttu-id="d42d4-117">\[La fonctionnalité Windows Media DRM est déconseillée et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="d42d4-117">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="d42d4-118">Utilisez plutôt [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="d42d4-118">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="d42d4-119">Cette documentation décrit les interfaces de programmation d’applications (API) étendues du client Microsoft Windows Media Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="d42d4-119">This documentation describes the Microsoft Windows Media Digital Rights Management (DRM) Client Extended Application Programming Interfaces (APIs).</span></span> <span data-ttu-id="d42d4-120">Les API étendues du client Windows Media DRM incluent des objets qui peuvent être utilisés pour gérer les opérations de Rights Management Windows Media Digital (DRM) sur un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="d42d4-120">The Windows Media DRM Client Extended APIs include objects that can be used to manage Windows Media Digital Rights Management (DRM) operations on a client computer.</span></span>

<span data-ttu-id="d42d4-121">L’objectif principal de ces API est la gestion des licences pour le contenu multimédia numérique protégé.</span><span class="sxs-lookup"><span data-stu-id="d42d4-121">The primary focus of these APIs is the management of licenses for protected digital media content.</span></span> <span data-ttu-id="d42d4-122">En outre, les API peuvent être utilisées pour mettre à jour les composants DRM sur l’ordinateur client et pour créer des applications qui transmettent du contenu à l’aide de Windows Media DRM pour les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="d42d4-122">In addition, the APIs can be used to update the DRM components on the client computer and to create applications that transmit content using Windows Media DRM for Network Devices.</span></span>

<span data-ttu-id="d42d4-123">Ces API constituent l’équivalent côté client du kit de développement logiciel (SDK) Windows Media Rights Manager.</span><span class="sxs-lookup"><span data-stu-id="d42d4-123">These APIs constitute the client-side counterpart to the Windows Media Rights Manager SDK.</span></span> <span data-ttu-id="d42d4-124">Lorsque le gestionnaire de droits Windows Media est utilisé pour créer des services en ligne qui protègent les fichiers et émettent des licences, les API étendues du client Windows Media DRM sont utilisées pour créer des applications qui utilisent ce contenu.</span><span class="sxs-lookup"><span data-stu-id="d42d4-124">Where Windows Media Rights Manager is used to create online services that protect files and issue licenses, the Windows Media DRM Client Extended APIs are used to create applications that consume that content.</span></span>

<span data-ttu-id="d42d4-125">Ce document comprend les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="d42d4-125">This document includes the following sections.</span></span>



| <span data-ttu-id="d42d4-126">Section</span><span class="sxs-lookup"><span data-stu-id="d42d4-126">Section</span></span>                                                                                                  | <span data-ttu-id="d42d4-127">Description</span><span class="sxs-lookup"><span data-stu-id="d42d4-127">Description</span></span>                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d42d4-128">À propos des API étendues du client Windows Media DRM</span><span class="sxs-lookup"><span data-stu-id="d42d4-128">About the Windows Media DRM Client Extended APIs</span></span>](about-the-windows-media-drm-client-extended-apis.md) | <span data-ttu-id="d42d4-129">Fournit une vue d’ensemble et des informations générales que vous devez connaître avant de développer des applications qui utilisent les API.</span><span class="sxs-lookup"><span data-stu-id="d42d4-129">Provides overview and background information that you should be familiar with before developing applications that use the APIs.</span></span>                                                        |
| [<span data-ttu-id="d42d4-130">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="d42d4-130">Programming Guide</span></span>](drm-programming-guide.md)                                                           | <span data-ttu-id="d42d4-131">Fournit des instructions détaillées pour effectuer diverses opérations DRM côté client.</span><span class="sxs-lookup"><span data-stu-id="d42d4-131">Provides detailed instructions for performing various client-side DRM operations.</span></span>                                                                                                      |
| [<span data-ttu-id="d42d4-132">Guide de référence de programmation</span><span class="sxs-lookup"><span data-stu-id="d42d4-132">Programming Reference</span></span>](drm-programming-reference.md)                                                   | <span data-ttu-id="d42d4-133">Fournit des informations de référence sur les interfaces, les méthodes, les fonctions, les structures, les types d’énumération et les constantes incluses dans les API étendues du client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="d42d4-133">Provides reference information about the interfaces, methods, functions, structures, enumeration types, and constants that are included in the Windows Media DRM Client Extended APIs.</span></span> |



 

 

 