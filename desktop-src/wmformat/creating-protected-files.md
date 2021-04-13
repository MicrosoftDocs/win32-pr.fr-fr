---
title: Création de fichiers protégés
description: Création de fichiers protégés
ms.assetid: 5237e797-72ec-402e-81ec-ab379747e464
keywords:
- Windows Media Format SDK, création de fichiers protégés
- Windows Media Format SDK, fichiers protégés
- ASF (Advanced Systems Format), création de fichiers protégés
- ASF (format des systèmes avancés), création de fichiers protégés
- ASF (Advanced Systems Format), fichiers protégés
- ASF (Advanced Systems Format), fichiers protégés
- ASF (Advanced Systems Format), WMStubDRM. lib
- ASF (format avancé des systèmes), WMStubDRM. lib
- WMStubDRM. lib, création de fichiers protégés
- WMStubDRM. lib, fichiers protégés
- gestion des droits numériques (DRM), WMStubDRM. lib
- DRM (gestion des droits numériques), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160a14d96da924bdb2a307bc804514a1ec3de083
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314263"
---
# <a name="creating-protected-files"></a><span data-ttu-id="ee572-115">Création de fichiers protégés</span><span class="sxs-lookup"><span data-stu-id="ee572-115">Creating Protected Files</span></span>

<span data-ttu-id="ee572-116">Pour créer des fichiers multimédias numériques protégés à l’aide de DRM version 1 ou DRM 7 et versions ultérieures, créez un lien vers le fichier WMStubDRM. lib que vous avez obtenu auprès de Microsoft et créez l’objet enregistreur.</span><span class="sxs-lookup"><span data-stu-id="ee572-116">To create protected digital media files using either DRM version 1 or DRM versions 7 and later, link to the WMStubDRM.lib file that you obtained from Microsoft, and create the writer object.</span></span> <span data-ttu-id="ee572-117">Pour la protection de la version 1, utilisez l’interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) pour définir les attributs DRM que vous souhaitez appliquer.</span><span class="sxs-lookup"><span data-stu-id="ee572-117">For version 1 protection, use the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface to set the DRM attributes you want to apply.</span></span> <span data-ttu-id="ee572-118">Pour les versions 7 et ultérieures, utilisez les méthodes de l’interface [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) .</span><span class="sxs-lookup"><span data-stu-id="ee572-118">For versions 7 and later, use the [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) interface methods.</span></span>

<span data-ttu-id="ee572-119">Les rubriques suivantes décrivent en détail comment protéger des fichiers.</span><span class="sxs-lookup"><span data-stu-id="ee572-119">The following topics describe in detail how to protect files.</span></span>

-   [<span data-ttu-id="ee572-120">Protection des fichiers avec DRM version 1</span><span class="sxs-lookup"><span data-stu-id="ee572-120">Protecting Files with DRM Version 1</span></span>](protecting-files-with-drm-version-1.md)
-   [<span data-ttu-id="ee572-121">Protection des fichiers avec DRM version 7 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="ee572-121">Protecting Files with DRM Version 7 or Later</span></span>](protecting-files-with-drm-version-7-or-later.md)

> [!Note]  
> <span data-ttu-id="ee572-122">DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="ee572-122">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ee572-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ee572-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee572-124">**Liste des attributs DRM**</span><span class="sxs-lookup"><span data-stu-id="ee572-124">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="ee572-125">**Propriétés DRM**</span><span class="sxs-lookup"><span data-stu-id="ee572-125">**DRM Properties**</span></span>](drm-properties.md)
</dt> <dt>

[<span data-ttu-id="ee572-126">**Versions DRM**</span><span class="sxs-lookup"><span data-stu-id="ee572-126">**DRM Versions**</span></span>](drm-versions.md)
</dt> <dt>

[<span data-ttu-id="ee572-127">**Activation de la prise en charge de DRM**</span><span class="sxs-lookup"><span data-stu-id="ee572-127">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="ee572-128">**Obtention de la bibliothèque DRM requise**</span><span class="sxs-lookup"><span data-stu-id="ee572-128">**Obtaining the Required DRM Library**</span></span>](obtaining-the-required-drm-library.md)
</dt> <dt>

[<span data-ttu-id="ee572-129">**Lecture des fichiers protégés**</span><span class="sxs-lookup"><span data-stu-id="ee572-129">**Reading Protected Files**</span></span>](reading-protected-files.md)
</dt> </dl>

 

 




