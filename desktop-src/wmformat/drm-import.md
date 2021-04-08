---
title: Importation DRM
description: Importation DRM
ms.assetid: 5e67a721-830b-4d99-9f90-4cb2d7c61104
keywords:
- SDK Windows Media format, API étendues du client DRM
- Windows Media Format SDK, API étendues du client
- Windows Media Format SDK, API étendues
- Windows Media Format SDK, API
- Kit de développement logiciel (SDK) Windows Media format, gestion des droits numériques (DRM)
- Windows Media Format SDK, importation DRM
- Windows Media Format SDK, importer
- SDK Windows Media format, système de protection du contenu (CPS)
- gestion des droits numériques (DRM), API étendues du client
- DRM (gestion des droits numériques), API étendues du client
- gestion des droits numériques (DRM), API étendues
- DRM (gestion des droits numériques), API étendues
- gestion des droits numériques (DRM), API
- DRM (gestion des droits numériques), API
- gestion des droits numériques (DRM), importation
- DRM (gestion des droits numériques), importation
- gestion des droits numériques (DRM), système de protection du contenu (CPS)
- DRM (gestion des droits numériques), système de protection du contenu (CPS)
- API étendues du client DRM, importation
- API étendues du client, importation
- API étendues du client DRM, système de protection du contenu (CPS)
- API étendues clientes, système de protection du contenu (CPS)
- système de protection du contenu (CPS)
- CPS (système de protection du contenu)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fc20cfd682df975c10a8f39785c0e8d69610d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673618"
---
# <a name="drm-import"></a><span data-ttu-id="85de8-127">Importation DRM</span><span class="sxs-lookup"><span data-stu-id="85de8-127">DRM Import</span></span>

<span data-ttu-id="85de8-128">Les sections suivantes expliquent comment convertir du contenu multimédia d’un système de protection de contenu (CPS) tiers en Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="85de8-128">The following sections explain how to convert media content from a third-party content protection system (CPS) to Windows Media DRM.</span></span> <span data-ttu-id="85de8-129">Ce processus est connu sous le nom d’importation DRM et se compose essentiellement des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="85de8-129">This process is known as DRM Import and consists essentially of the following steps:</span></span>

1.  <span data-ttu-id="85de8-130">Création du fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="85de8-130">Creating the ASF file.</span></span>
2.  <span data-ttu-id="85de8-131">Création de la licence.</span><span class="sxs-lookup"><span data-stu-id="85de8-131">Creating the license.</span></span>
3.  <span data-ttu-id="85de8-132">Vous pouvez éventuellement supprimer la licence.</span><span class="sxs-lookup"><span data-stu-id="85de8-132">Optionally deleting the license.</span></span>

<span data-ttu-id="85de8-133">L’importation DRM est expliquée dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="85de8-133">DRM Import is explained in the following sections.</span></span>



| <span data-ttu-id="85de8-134">Section</span><span class="sxs-lookup"><span data-stu-id="85de8-134">Section</span></span>                                                                              | <span data-ttu-id="85de8-135">Description</span><span class="sxs-lookup"><span data-stu-id="85de8-135">Description</span></span>                                                                          |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="85de8-136">Importation de la licence et du matériel de clé</span><span class="sxs-lookup"><span data-stu-id="85de8-136">Importing License and Key Material</span></span>](importing-license-and-key-material.md)         | <span data-ttu-id="85de8-137">Décrit comment émettre des licences localement et les importer dans Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="85de8-137">Describes how to issue licenses locally and import them into Windows Media DRM.</span></span>      |
| [<span data-ttu-id="85de8-138">Vérification de la révocation des certificats</span><span class="sxs-lookup"><span data-stu-id="85de8-138">Checking Certificate Revocation</span></span>](checking-certificate-revocation.md)               | <span data-ttu-id="85de8-139">Décrit comment vérifier la révocation de certificats.</span><span class="sxs-lookup"><span data-stu-id="85de8-139">Describes how to check certificate revocation.</span></span>                                       |
| [<span data-ttu-id="85de8-140">Génération d’une licence XMR</span><span class="sxs-lookup"><span data-stu-id="85de8-140">Building an XMR License</span></span>](building-an-xmr-license.md)                               | <span data-ttu-id="85de8-141">Décrit comment créer une licence XMR et la passer au sous-système DRM.</span><span class="sxs-lookup"><span data-stu-id="85de8-141">Describes how to create an XMR license and pass it to the DRM subsystem.</span></span>             |
| [<span data-ttu-id="85de8-142">Création et initialisation d’un enregistreur DRM</span><span class="sxs-lookup"><span data-stu-id="85de8-142">Creating and Initializing a DRM Writer</span></span>](creating-and-initializing-a-drm-writer.md) | <span data-ttu-id="85de8-143">Décrit comment initialiser un objet Writer ASF pour préparer l’importation DRM.</span><span class="sxs-lookup"><span data-stu-id="85de8-143">Describes how to initialize an ASF writer object to prepare for DRM Import.</span></span>          |
| [<span data-ttu-id="85de8-144">Chiffrement et importation d’exemples de médias</span><span class="sxs-lookup"><span data-stu-id="85de8-144">Encrypting and Importing Media Samples</span></span>](encrypting-and-importing-media-samples.md) | <span data-ttu-id="85de8-145">Décrit comment chiffrer et importer des exemples de médias individuels dans Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="85de8-145">Describes how to encrypt and import individual media samples into Windows Media DRM.</span></span> |
| [<span data-ttu-id="85de8-146">Suppression de la licence</span><span class="sxs-lookup"><span data-stu-id="85de8-146">License Deletion</span></span>](license-deletion.md)                                             | <span data-ttu-id="85de8-147">Décrit comment supprimer des licences créées localement.</span><span class="sxs-lookup"><span data-stu-id="85de8-147">Describes how to delete locally created licenses.</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="85de8-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="85de8-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85de8-149">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="85de8-149">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




