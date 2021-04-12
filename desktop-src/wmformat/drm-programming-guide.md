---
title: Guide de programmation du client Microsoft Windows Media DRM
description: Guide de programmation du client Microsoft Windows Media DRM
ms.assetid: e7b179b3-ed14-4ea0-9a00-9d96557a2e2e
keywords:
- SDK Windows Media format, API étendues du client DRM
- Windows Media Format SDK, API étendues du client
- Windows Media Format SDK, API étendues
- Windows Media Format SDK, API
- Kit de développement logiciel (SDK) Windows Media format, gestion des droits numériques (DRM)
- Windows Media Format SDK, Guide de programmation
- gestion des droits numériques (DRM), API étendues du client
- DRM (gestion des droits numériques), API étendues du client
- gestion des droits numériques (DRM), API étendues
- DRM (gestion des droits numériques), API étendues
- gestion des droits numériques (DRM), API
- DRM (gestion des droits numériques), API
- gestion des droits numériques (DRM), Guide de programmation
- DRM (gestion des droits numériques), Guide de programmation
- API étendues du client DRM, à propos de
- API étendues du client, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b338ea6ebd9cb132c8e6b1c76c8e1d7f6c6aa182
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464087"
---
# <a name="microsoft-windows-media-drm-client-programming-guide"></a><span data-ttu-id="caaa4-119">Guide de programmation du client Microsoft Windows Media DRM</span><span class="sxs-lookup"><span data-stu-id="caaa4-119">Microsoft Windows Media DRM Client Programming Guide</span></span>

<span data-ttu-id="caaa4-120">Ce guide fournit des informations sur l’utilisation des fonctionnalités des API étendues du client Windows Media DRM dans vos applications.</span><span class="sxs-lookup"><span data-stu-id="caaa4-120">This guide provides information about using the features of the Windows Media DRM Client Extended APIs in your applications.</span></span> <span data-ttu-id="caaa4-121">Les sections suivantes expliquent en détail les étapes à suivre pour implémenter des fonctionnalités DRM.</span><span class="sxs-lookup"><span data-stu-id="caaa4-121">The following sections explain, in detail, the steps involved in implementing DRM features.</span></span>



| <span data-ttu-id="caaa4-122">Section</span><span class="sxs-lookup"><span data-stu-id="caaa4-122">Section</span></span>                                                                                                                          | <span data-ttu-id="caaa4-123">Description</span><span class="sxs-lookup"><span data-stu-id="caaa4-123">Description</span></span>                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="caaa4-124">Prise en main</span><span class="sxs-lookup"><span data-stu-id="caaa4-124">Getting Started</span></span>](drm-getting-started.md)                                                                                       | <span data-ttu-id="caaa4-125">Fournit des informations sur la configuration de projets C++ qui utilisent les API étendues du client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="caaa4-125">Provides information about setting up C++ projects that use the Windows Media DRM Client Extended APIs.</span></span>    |
| [<span data-ttu-id="caaa4-126">Acquisition de licences</span><span class="sxs-lookup"><span data-stu-id="caaa4-126">Acquiring Licenses</span></span>](acquiring-licenses.md)                                                                                     | <span data-ttu-id="caaa4-127">Décrit comment récupérer des licences sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="caaa4-127">Describes how to get licenses on the client computer.</span></span>                                                      |
| [<span data-ttu-id="caaa4-128">Obtention d’informations à partir de licences dans le magasin de licences local</span><span class="sxs-lookup"><span data-stu-id="caaa4-128">Getting Information from Licenses in the Local License Store</span></span>](getting-information-from-licenses-in-the-local-license-store.md) | <span data-ttu-id="caaa4-129">Décrit comment obtenir des informations sur les droits pour le contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="caaa4-129">Describes how to get information about rights for protected content.</span></span>                                       |
| [<span data-ttu-id="caaa4-130">Réalisation de l’individualisation DRM</span><span class="sxs-lookup"><span data-stu-id="caaa4-130">Performing DRM Individualization</span></span>](performing-drm-individualization.md)                                                         | <span data-ttu-id="caaa4-131">Décrit comment mettre à jour et individualiser le composant DRM sur l’ordinateur client pour le rendre plus sécurisé.</span><span class="sxs-lookup"><span data-stu-id="caaa4-131">Describes how to update and individualize the DRM component on the client computer to make it more secure.</span></span> |
| [<span data-ttu-id="caaa4-132">Exportation DRM</span><span class="sxs-lookup"><span data-stu-id="caaa4-132">DRM Export</span></span>](drm-export.md)                                                                                                     | <span data-ttu-id="caaa4-133">Décrit comment exporter du contenu protégé par Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="caaa4-133">Describes how to export content protected by Windows Media DRM.</span></span>                                            |
| [<span data-ttu-id="caaa4-134">Importation DRM</span><span class="sxs-lookup"><span data-stu-id="caaa4-134">DRM Import</span></span>](drm-import.md)                                                                                                     | <span data-ttu-id="caaa4-135">Décrit comment importer le contenu protégé par Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="caaa4-135">Describes how to import content protected by Windows Media DRM.</span></span>                                            |
| [<span data-ttu-id="caaa4-136">Révocation de licence</span><span class="sxs-lookup"><span data-stu-id="caaa4-136">License Revocation</span></span>](drm-license-revocation.md)                                                                                 | <span data-ttu-id="caaa4-137">Décrit comment supprimer des licences du magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="caaa4-137">Describes how to remove licenses from the local license store.</span></span>                                             |
| [<span data-ttu-id="caaa4-138">Révocation et renouvellement de composants automatisés</span><span class="sxs-lookup"><span data-stu-id="caaa4-138">Automated Component Revocation and Renewal</span></span>](automated-component-revocation-and-renewal.md)                                     | <span data-ttu-id="caaa4-139">Décrit le système de révocation et de renouvellement automatisé Windows Media DRM à l’aide des activateurs du contenu.</span><span class="sxs-lookup"><span data-stu-id="caaa4-139">Describes the Windows Media DRM automated revocation and renewal system using content enablers.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="caaa4-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="caaa4-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="caaa4-141">**API étendues du client Windows Media DRM**</span><span class="sxs-lookup"><span data-stu-id="caaa4-141">**Windows Media DRM Client Extended APIs**</span></span>](windows-media-drm-client-extended-apis.md)
</dt> <dt>

<span data-ttu-id="caaa4-142">[SDK Windows Media Rights Manager](/previous-versions/ms986509(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="caaa4-142">[Windows Media Rights Manager SDK](/previous-versions/ms986509(v=msdn.10))</span></span>
</dt> </dl>

 

 
