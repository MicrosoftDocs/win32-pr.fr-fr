---
title: Exportation DRM
description: Exportation DRM
ms.assetid: 0b44f2e5-e63c-4bdb-8123-097a5d5e3756
keywords:
- SDK Windows Media format, API étendues du client DRM
- Windows Media Format SDK, API étendues du client
- Windows Media Format SDK, API étendues
- Windows Media Format SDK, API
- Kit de développement logiciel (SDK) Windows Media format, gestion des droits numériques (DRM)
- Windows Media Format SDK, exportation DRM
- Windows Media Format SDK, exporter
- gestion des droits numériques (DRM), API étendues du client
- DRM (gestion des droits numériques), API étendues du client
- gestion des droits numériques (DRM), API étendues
- DRM (gestion des droits numériques), API étendues
- gestion des droits numériques (DRM), API
- DRM (gestion des droits numériques), API
- gestion des droits numériques (DRM), exportation
- DRM (gestion des droits numériques), exportation
- API étendues du client DRM, exporter
- API étendues clientes, exporter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2917cfd0c9042f4547540618b44ed4c2f324edb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310173"
---
# <a name="drm-export"></a><span data-ttu-id="d79c6-120">Exportation DRM</span><span class="sxs-lookup"><span data-stu-id="d79c6-120">DRM Export</span></span>

<span data-ttu-id="d79c6-121">La fonctionnalité d’exportation de Windows Media DRM vous permet de créer des applications sous licence qui déchiffrent du contenu protégé par Windows Media DRM, puis de nouveau le chiffrement dans un schéma de protection de contenu (CPS) de sortie spécifié explicitement par l’émetteur de licence associé.</span><span class="sxs-lookup"><span data-stu-id="d79c6-121">Windows Media DRM export functionality enables you to create licensed applications that decrypt content protected by Windows Media DRM, and re-encrypt in an output content protection scheme (CPS) explicitly specified by the associated license issuer.</span></span> <span data-ttu-id="d79c6-122">L’émetteur de licence autorise explicitement l’exportation de contenu vers un CPS spécifique par le biais d’une liste d’inclusion.</span><span class="sxs-lookup"><span data-stu-id="d79c6-122">The license issuer explicitly authorizes the export of content to a specific CPS through an inclusion list.</span></span>

> [!Note]  
> <span data-ttu-id="d79c6-123">Pour accéder à la fonctionnalité d’exportation, vous devez demander un [certificat d’application d’exportation](export-application-certificate.md) de la part de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d79c6-123">To access export functionality, you must apply for an [Export Application Certificate](export-application-certificate.md) from Microsoft.</span></span>

 

<span data-ttu-id="d79c6-124">La fonctionnalité d’exportation DRM Windows Media est expliquée dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="d79c6-124">Windows Media DRM export functionality is explained in the following sections.</span></span>



| <span data-ttu-id="d79c6-125">Section</span><span class="sxs-lookup"><span data-stu-id="d79c6-125">Section</span></span>                                                                                      | <span data-ttu-id="d79c6-126">Description</span><span class="sxs-lookup"><span data-stu-id="d79c6-126">Description</span></span>                                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d79c6-127">Exporter un certificat d’application</span><span class="sxs-lookup"><span data-stu-id="d79c6-127">Export Application Certificate</span></span>](export-application-certificate.md)                         | <span data-ttu-id="d79c6-128">Décrit un certificat d’application d’exportation.</span><span class="sxs-lookup"><span data-stu-id="d79c6-128">Describes an export application certificate.</span></span>                                                        |
| [<span data-ttu-id="d79c6-129">Listes d’autorisations et d’inclusion explicites</span><span class="sxs-lookup"><span data-stu-id="d79c6-129">Explicit Authorization and Inclusion Lists</span></span>](explicit-authorization-and-inclusion-lists.md) | <span data-ttu-id="d79c6-130">Explique le processus d’autorisation explicite et le mode de fonctionnement des listes d’inclusion.</span><span class="sxs-lookup"><span data-stu-id="d79c6-130">Explains the process of explicit authorization, and how inclusions lists work.</span></span>                      |
| [<span data-ttu-id="d79c6-131">Exportation du contenu compressé</span><span class="sxs-lookup"><span data-stu-id="d79c6-131">Exporting Compressed Content</span></span>](exporting-compressed-content.md)                             | <span data-ttu-id="d79c6-132">Décrit comment exporter du contenu compressé à partir du contenu audio ou vidéo protégé par DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d79c6-132">Describes how to export compressed content from Windows Media DRM protected audio or video content.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d79c6-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d79c6-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d79c6-134">**Listes d’autorisations et d’inclusion explicites**</span><span class="sxs-lookup"><span data-stu-id="d79c6-134">**Explicit Authorization and Inclusion Lists**</span></span>](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[<span data-ttu-id="d79c6-135">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="d79c6-135">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




