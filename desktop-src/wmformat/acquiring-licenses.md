---
title: Acquisition de licences
description: Acquisition de licences
ms.assetid: dde33d57-6c63-4e1a-8398-5db466fb22fa
keywords:
- SDK Windows Media format, API étendues du client DRM
- Windows Media Format SDK, API étendues du client
- Windows Media Format SDK, API étendues
- Windows Media Format SDK, API
- Kit de développement logiciel (SDK) Windows Media format, gestion des droits numériques (DRM)
- Windows Media Format SDK, acquisition de licences
- Windows Media Format SDK, licences
- gestion des droits numériques (DRM), API étendues du client
- DRM (gestion des droits numériques), API étendues du client
- gestion des droits numériques (DRM), API étendues
- DRM (gestion des droits numériques), API étendues
- gestion des droits numériques (DRM), API
- DRM (gestion des droits numériques), API
- gestion des droits numériques (DRM), acquisition de licences
- DRM (Digital Rights Management), acquisition de licences
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- API étendues du client DRM, acquisition de licences
- API étendues clientes, acquisition de licences
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c024789823ca0cd1b38959d78535ce71e2514897
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379631"
---
# <a name="acquiring-licenses"></a><span data-ttu-id="b706e-122">Acquisition de licences</span><span class="sxs-lookup"><span data-stu-id="b706e-122">Acquiring Licenses</span></span>

<span data-ttu-id="b706e-123">Un scénario courant pour acquérir des licences est lorsqu’un utilisateur dispose d’un fichier Windows Media protégé et tente d’accéder au contenu pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="b706e-123">A common scenario for acquiring licenses is when a user has a protected Windows Media file and tries to access the content for the first time.</span></span> <span data-ttu-id="b706e-124">Étant donné que les API étendues du client Windows Media DRM sont distinctes des routines de gestion de fichiers ASF, le scénario d’acquisition de licence de base, bien qu’pris en charge, nécessite plus d’appels d’API que l’utilisation du kit de développement logiciel (SDK) du format Windows Media et du SDK Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="b706e-124">Because the Windows Media DRM Client Extended APIs are separate from ASF file handling routines, the basic license acquisition scenario, while supported, requires more API calls than using the Windows Media Format SDK and the Media Foundation SDK.</span></span>

<span data-ttu-id="b706e-125">Cette section décrit comment utiliser les API étendues du client Windows Media DRM pour acquérir des licences stockées dans le magasin de licences local sur un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="b706e-125">This section describes how to use the Windows Media DRM Client Extended APIs to acquire licenses that are stored in the local license store on a client computer.</span></span> <span data-ttu-id="b706e-126">Elle contient les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="b706e-126">It contains the following topics.</span></span>



| <span data-ttu-id="b706e-127">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b706e-127">Topic</span></span>                                                                | <span data-ttu-id="b706e-128">Description</span><span class="sxs-lookup"><span data-stu-id="b706e-128">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b706e-129">Acquisition de licence en mode silencieux</span><span class="sxs-lookup"><span data-stu-id="b706e-129">Silent License Acquisition</span></span>](silent-license-acquisition.md)         | <span data-ttu-id="b706e-130">Décrit comment acquérir des licences sans intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b706e-130">Describes how to acquire licenses without user intervention.</span></span>                                                                               |
| [<span data-ttu-id="b706e-131">Acquisition de licence non silencieuse</span><span class="sxs-lookup"><span data-stu-id="b706e-131">Non-Silent License Acquisition</span></span>](non-silent-license-acquisition.md) | <span data-ttu-id="b706e-132">Décrit comment acquérir des licences lorsque l’intervention de l’utilisateur (par exemple, le paiement du contenu) est requise.</span><span class="sxs-lookup"><span data-stu-id="b706e-132">Describes how to acquire licenses when user intervention (such as paying for the content) is required.</span></span>                                     |
| [<span data-ttu-id="b706e-133">Pré-remise de licence</span><span class="sxs-lookup"><span data-stu-id="b706e-133">License Pre-Delivery</span></span>](license-pre-delivery.md)                     | <span data-ttu-id="b706e-134">Décrit comment extraire des licences d’un serveur de licences vers un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="b706e-134">Describes how to pull licenses from a license server to a client computer.</span></span>                                                                 |
| [<span data-ttu-id="b706e-135">Création de licences localement</span><span class="sxs-lookup"><span data-stu-id="b706e-135">Creating Licenses Locally</span></span>](creating-licenses-locally.md)           | <span data-ttu-id="b706e-136">Décrit comment créer vos propres licences sans les télécharger à partir d’un serveur de licences et comment les stocker dans le magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="b706e-136">Describes how to create your own licenses without downloading them from a license server and how to store them in the local license store.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b706e-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b706e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b706e-138">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="b706e-138">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




