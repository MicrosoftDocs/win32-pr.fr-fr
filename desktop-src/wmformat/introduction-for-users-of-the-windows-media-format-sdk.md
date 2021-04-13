---
title: Présentation pour les utilisateurs du kit de développement logiciel (SDK) Windows Media format
description: Présentation pour les utilisateurs du kit de développement logiciel (SDK) Windows Media format
ms.assetid: 21f06c43-213e-4fbf-a33a-c1890b4b40ce
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
ms.openlocfilehash: 538978305e4df952ed97e063b3512ce9fd5cfc34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379987"
---
# <a name="introduction-for-users-of-the-windows-media-format-sdk"></a><span data-ttu-id="e25d6-116">Présentation pour les utilisateurs du kit de développement logiciel (SDK) Windows Media format</span><span class="sxs-lookup"><span data-stu-id="e25d6-116">Introduction for Users of the Windows Media Format SDK</span></span>

<span data-ttu-id="e25d6-117">La plupart des fonctionnalités offertes par les API étendues du client Windows Media DRM sont les mêmes que celles fournies par les objets du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e25d6-117">Much of the functionality provided by the Windows Media DRM Client Extended APIs is the same as the functionality provided by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="e25d6-118">Le kit de développement logiciel (SDK) du format Windows Media offre aux développeurs les objets nécessaires pour créer, accéder et manipuler des fichiers multimédias qui utilisent la structure de fichiers ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="e25d6-118">The Windows Media Format SDK provides developers with the objects needed to create, access, and manipulate media files that use the Advanced Systems Format (ASF) file structure.</span></span> <span data-ttu-id="e25d6-119">Étant donné que Windows Media DRM est conçu pour protéger les fichiers ASF, les fonctionnalités DRM côté client étaient incluses dans le kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="e25d6-119">Because Windows Media DRM is intended to protect ASF files, client-side DRM functionality was included in the Windows Media Format SDK.</span></span>

<span data-ttu-id="e25d6-120">Les API étendues du client Windows Media DRM sont publiées en même temps que la plateforme multimédia numérique nouvelle génération de Microsoft, le kit de développement logiciel (SDK) Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e25d6-120">The Windows Media DRM Client Extended APIs are being released in conjunction with Microsoft's next-generation digital media platform, the Microsoft Media Foundation SDK.</span></span> <span data-ttu-id="e25d6-121">Media Foundation inclura des fonctionnalités ASF qui chevauchent certaines des fonctionnalités du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e25d6-121">Media Foundation will include ASF functionality that overlaps some of the features of the Windows Media Format SDK.</span></span> <span data-ttu-id="e25d6-122">Étant donné qu’il existe désormais deux kits de développement logiciel (SDK) Microsoft qui manipulent les fichiers ASF, les fonctionnalités DRM côté client sont séparées du Windows Media Format SDK dans les API étendues du client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="e25d6-122">Because there are now two Microsoft SDKs that manipulate ASF files, the client-side DRM functionality is being separated from the Windows Media Format SDK into the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="e25d6-123">Ces API sont accessibles aux utilisateurs du kit de développement logiciel (SDK) du format Windows Media et du kit de développement logiciel (SDK) Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e25d6-123">These APIs can be accessed by users of both the Windows Media Format SDK and the Media Foundation SDK.</span></span> <span data-ttu-id="e25d6-124">À l’heure actuelle, ces API sont incluses dans le package d’installation du SDK Windows Media format et sont documentées dans le cadre du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e25d6-124">At present, these APIs are included as part of the Windows Media Format SDK installation package and are documented as part of the Windows Media Format SDK.</span></span> <span data-ttu-id="e25d6-125">Toutefois, les API étendues du client Windows Media DRM sont implémentées dans leur propre bibliothèque et ont leur propre fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="e25d6-125">However, the Windows Media DRM Client Extended APIs are implemented in their own library and have their own header file.</span></span> <span data-ttu-id="e25d6-126">Après l’installation du kit de développement logiciel (SDK) Windows Media format, ces API peuvent être utilisées une seule fois, sans inclure les bibliothèques ou les en-têtes du kit de développement logiciel (SDK) du format Windows Media dans votre application.</span><span class="sxs-lookup"><span data-stu-id="e25d6-126">After installing the Windows Media Format SDK, these APIs can be used one their own, without including any Windows Media Format SDK headers or libraries in your application.</span></span>

<span data-ttu-id="e25d6-127">Si vous développez des applications qui utilisent le kit de développement logiciel (SDK) Windows Media format, vous devez décider s’il faut utiliser les fonctionnalités DRM fournies par le kit de développement logiciel, ou utiliser les API étendues du client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="e25d6-127">If you develop applications that use the Windows Media Format SDK you must decide whether to use the DRM functionality that SDK provides, or to use the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="e25d6-128">Alors que la plupart des fonctionnalités de ces deux kits SDK sont très similaires, les API étendues du client Windows Media DRM offrent les fonctionnalités suivantes qui ne sont pas disponibles pour les utilisateurs des routines DRM plus anciennes :</span><span class="sxs-lookup"><span data-stu-id="e25d6-128">While many of the features of these two SDKs are very similar, the Windows Media DRM Client Extended APIs offer the following features not available to users of the older DRM routines:</span></span>

-   <span data-ttu-id="e25d6-129">Possibilité d’importer du contenu protégé par un système de gestion des droits tiers.</span><span class="sxs-lookup"><span data-stu-id="e25d6-129">Ability to import content protected by a third-party rights management system.</span></span>
-   <span data-ttu-id="e25d6-130">Possibilité d’exporter du contenu protégé par Windows Media DRM vers un système de gestion des droits tiers.</span><span class="sxs-lookup"><span data-stu-id="e25d6-130">Ability to export content protected by Windows Media DRM to a third-party rights management system.</span></span>
-   <span data-ttu-id="e25d6-131">Énumération directe des licences dans le magasin de licences.</span><span class="sxs-lookup"><span data-stu-id="e25d6-131">Direct enumeration of licenses in the license store.</span></span>
-   <span data-ttu-id="e25d6-132">Requêtes de droits simples et agrégées basées sur l’ID de clé (inutile de charger le fichier multimédia).</span><span class="sxs-lookup"><span data-stu-id="e25d6-132">Simple, aggregated rights querying based on key ID (no need to load the media file).</span></span>
-   <span data-ttu-id="e25d6-133">Possibilité de renouveler des composants révoqués à l’aide de l’interface Media Foundation standard, **IMFContentEnabler**.</span><span class="sxs-lookup"><span data-stu-id="e25d6-133">Ability to renew revoked components by using the standard Media Foundation interface, **IMFContentEnabler**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e25d6-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e25d6-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e25d6-135">**À propos des API étendues du client Windows Media DRM**</span><span class="sxs-lookup"><span data-stu-id="e25d6-135">**About the Windows Media DRM Client Extended APIs**</span></span>](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




