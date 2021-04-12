---
title: Protection DRM et distribution des licences de contenu
description: Protection DRM et distribution des licences de contenu
ms.assetid: 147fef8c-7298-450d-a1a9-345c03c49bec
keywords:
- Windows Media Format SDK, protection de contenu DRM
- Windows Media Format SDK, licences DRM
- ASF (Advanced Systems Format), protection du contenu DRM
- ASF (format de systèmes avancés), protection de contenu DRM
- ASF (Advanced Systems Format), distribution de licences DRM
- ASF (format de systèmes avancés), distribution de licences DRM
- gestion des droits numériques (DRM), protection du contenu
- DRM (gestion des droits numériques), protection du contenu
- gestion des droits numériques (DRM), distribution de licences
- DRM (gestion des droits numériques), distribution de licences
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25af13947828885d70f3e0fd9fe8bf035eb8c5e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311452"
---
# <a name="drm-protection-and-content-license-distribution"></a><span data-ttu-id="95fca-113">Protection DRM et distribution des licences de contenu</span><span class="sxs-lookup"><span data-stu-id="95fca-113">DRM Protection and Content License Distribution</span></span>

<span data-ttu-id="95fca-114">Du côté de la création, la technologie de gestion des droits numériques implique deux processus principaux : (1) la protection du contenu et (2) la fourniture de licences pour le contenu.</span><span class="sxs-lookup"><span data-stu-id="95fca-114">On the creation side, digital rights management technology involves two main processes: (1) protecting the content and (2) providing licenses for the content.</span></span> <span data-ttu-id="95fca-115">La protection d’un fichier implique essentiellement le chiffrement du contenu, ainsi que l’ajout d’une URL dans l’en-tête de fichier qui spécifie l’emplacement où une licence pour le contenu peut être obtenue.</span><span class="sxs-lookup"><span data-stu-id="95fca-115">Protecting a file basically involves encrypting the content, and including a URL in the file header that specifies where a license for the content may be obtained.</span></span> <span data-ttu-id="95fca-116">Si vous souhaitez protéger des fichiers avec et distribuer les fichiers à d’autres ordinateurs ou périphériques, vous pouvez utiliser le kit de développement logiciel (SDK) Windows Media format ou le kit de développement logiciel (SDK) Windows Media Rights Manager pour protéger le fichier.</span><span class="sxs-lookup"><span data-stu-id="95fca-116">If you want to protect files with and then distribute the files to other computers or devices, you can use either the Windows Media Format SDK or the Windows Media Rights Manager SDK to protect the file.</span></span> <span data-ttu-id="95fca-117">Pour les scénarios de DRM actifs, vous devez utiliser le kit de développement logiciel (SDK) Windows Media format pour protéger le contenu lors de son encodage.</span><span class="sxs-lookup"><span data-stu-id="95fca-117">For live-DRM scenarios, you must use the Windows Media Format SDK to protect the content as it is being encoded.</span></span>

<span data-ttu-id="95fca-118">Pour créer et émettre des licences pour du contenu protégé, vous pouvez créer votre propre solution personnalisée à l’aide des objets du kit de développement logiciel (SDK) Windows Media Rights Manager, ou vous pouvez utiliser un service exécuté par un tiers.</span><span class="sxs-lookup"><span data-stu-id="95fca-118">To create and issue licenses for protected content, you can create your own custom solution using the objects of the Windows Media Rights Manager SDK, or you can use a service run by a third party.</span></span>

<span data-ttu-id="95fca-119">Quelle que soit la méthode utilisée, les fichiers protégés que vous créez contiendront, dans l’en-tête DRM, une URL qui indique aux applications clientes où obtenir une licence pour le contenu.</span><span class="sxs-lookup"><span data-stu-id="95fca-119">Whichever method you use, the protected files that you create will contain, in the DRM header object, a URL that tells client applications where to obtain a license for the content.</span></span>

> [!Note]  
> <span data-ttu-id="95fca-120">Le kit de développement logiciel (SDK) Windows Media format ne prend pas en charge la création ou l’émission de licences.</span><span class="sxs-lookup"><span data-stu-id="95fca-120">The Windows Media Format SDK does not provide support for creating or issuing licenses.</span></span>

 

<span data-ttu-id="95fca-121">Du côté de la lecture, une application DRM doit être en mesure d’obtenir des licences pour du contenu protégé, de déchiffrer ce contenu à l’aide de la clé contenue dans la licence et d’appliquer les restrictions de licence, telles que le nombre de fois où un fichier peut être lu ou si le fichier peut être copié sur un autre appareil.</span><span class="sxs-lookup"><span data-stu-id="95fca-121">On the playback side, a DRM-enabled application must be able to obtain licenses for protected content, to decrypt that content using the key contained in the license, and to enforce the license restrictions, such as the number of times a file may be played, or whether the file can be copied to another device.</span></span> <span data-ttu-id="95fca-122">Le kit de développement logiciel (SDK) Windows Media Format fournit la prise en charge requise pour créer une application de lecture DRM entièrement activée.</span><span class="sxs-lookup"><span data-stu-id="95fca-122">The Windows Media Format SDK provides all the support required to create a fully enabled DRM playback application.</span></span>

> [!Note]  
> <span data-ttu-id="95fca-123">DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="95fca-123">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="95fca-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="95fca-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95fca-125">**Fonctionnalités de Rights Management numérique**</span><span class="sxs-lookup"><span data-stu-id="95fca-125">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="95fca-126">**Activation de la prise en charge de DRM**</span><span class="sxs-lookup"><span data-stu-id="95fca-126">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




