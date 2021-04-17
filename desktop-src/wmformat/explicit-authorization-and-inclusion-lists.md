---
title: Listes d’autorisations et d’inclusion explicites
description: Listes d’autorisations et d’inclusion explicites
ms.assetid: b2e1cdd4-ea3c-4b05-a53a-2cdc12440645
keywords:
- Windows Media Format SDK, exportation DRM
- Windows Media Format SDK, exporter
- Windows Media Format SDK, liste d’autorisations et d’inclusion explicites
- Windows Media Format SDK, listes d’autorisations
- Windows Media Format SDK, listes d’inclusion
- gestion des droits numériques (DRM), exportation
- DRM (gestion des droits numériques), exportation
- gestion des droits numériques (DRM), listes d’autorisation et d’inclusion explicites
- DRM (gestion des droits numériques), listes d’autorisation et d’inclusion explicites
- gestion des droits numériques (DRM), listes d’autorisations
- DRM (gestion des droits numériques), listes d’autorisations
- gestion des droits numériques (DRM), listes d’inclusion
- DRM (gestion des droits numériques), listes d’inclusion
- API étendues du client DRM, listes d’autorisations et d’inclusion explicites
- API étendues clientes, listes d’autorisations et d’inclusion explicites
- API étendues du client DRM, listes d’autorisations
- API étendues clientes, listes d’autorisations
- API étendues du client DRM, listes d’inclusion
- API étendues clientes, listes d’inclusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2309bed28ffd3add2a75c1cd90488b9ef454659b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381489"
---
# <a name="explicit-authorization-and-inclusion-lists"></a><span data-ttu-id="4dd5c-122">Listes d’autorisations et d’inclusion explicites</span><span class="sxs-lookup"><span data-stu-id="4dd5c-122">Explicit Authorization and Inclusion Lists</span></span>

<span data-ttu-id="4dd5c-123">Les licences peuvent contenir une liste d’inclusion pour autoriser explicitement l’exportation de contenu protégé par Windows Media DRM vers d’autres schémas de protection de contenu (CPS).</span><span class="sxs-lookup"><span data-stu-id="4dd5c-123">Licenses can contain an inclusion list to explicitly authorize the exporting of content protected by Windows Media DRM to other content protection schemes (CPS).</span></span> <span data-ttu-id="4dd5c-124">Conformément aux termes du contrat de licence que vous entrez avec Microsoft pour activer l’exportation DRM, vous pouvez exporter uniquement vers un CPS valide identifié dans la liste d’inclusion d’une licence.</span><span class="sxs-lookup"><span data-stu-id="4dd5c-124">As per the terms of the license agreement you enter into with Microsoft to enable DRM Export you can export only to a valid CPS that is identified in the inclusion list of a license.</span></span>

<span data-ttu-id="4dd5c-125">Une liste d’inclusion est un tableau limité d’identificateurs globaux uniques (GUID) qui représente chacun un CPS autorisé spécifique sur lequel le contenu peut être exporté.</span><span class="sxs-lookup"><span data-stu-id="4dd5c-125">An inclusion list is a bounded array of globally unique identifiers (GUIDs) that each represents a specific authorized CPS to which the content can be exported.</span></span> <span data-ttu-id="4dd5c-126">Les GUID répertoriés dans une liste d’inclusion sont indépendants des niveaux de protection de sortie (OPL) et des niveaux de protection de contenu (CPL).</span><span class="sxs-lookup"><span data-stu-id="4dd5c-126">The GUIDs listed in an inclusion list are independent of the output protection levels (OPL) and content protection levels (CPL).</span></span> <span data-ttu-id="4dd5c-127">L’application de ces restrictions est la responsabilité de votre application.</span><span class="sxs-lookup"><span data-stu-id="4dd5c-127">Enforcing these restrictions is the responsibility of your application.</span></span>

> [!Note]  
> <span data-ttu-id="4dd5c-128">Lorsque vous effectuez l’exportation DRM Windows Media sur du contenu compressé, vous accédez à la liste d’inclusion par le biais de la méthode [**IWMDRMLicense :: GetInclusionList**](iwmdrmlicense-getinclusionlist.md) .</span><span class="sxs-lookup"><span data-stu-id="4dd5c-128">When performing Windows Media DRM Export on compressed content, you access the inclusion list through the [**IWMDRMLicense::GetInclusionList**](iwmdrmlicense-getinclusionlist.md) method.</span></span> <span data-ttu-id="4dd5c-129">Lorsque vous effectuez l’exportation DRM Windows Media sur du contenu non compressé, utilisez la méthode [**IWMDRMReader3 :: GetInclusionList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist) .</span><span class="sxs-lookup"><span data-stu-id="4dd5c-129">When performing Windows Media DRM Export on uncompressed content, use the [**IWMDRMReader3::GetInclusionList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist) method.</span></span>

 

<span data-ttu-id="4dd5c-130">Pour inscrire un nouveau système de protection de contenu comme une exportation autorisée Windows Media DRM dans les règles de conformité d’exportation DRM Windows Media, contactez wmla@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="4dd5c-130">To register a new content protection system as a Windows Media DRM Permitted Export in the Windows Media DRM export compliance rules, please contact wmla@microsoft.com.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4dd5c-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4dd5c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dd5c-132">**Exportation DRM**</span><span class="sxs-lookup"><span data-stu-id="4dd5c-132">**DRM Export**</span></span>](drm-export.md)
</dt> </dl>

 

 




