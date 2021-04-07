---
title: Affichage des attributs des fichiers protégés
description: Affichage des attributs des fichiers protégés
ms.assetid: fbfa1a1b-afd0-4f61-86ae-488716e16355
keywords:
- Windows Media Format SDK, affichage des attributs des fichiers protégés
- Windows Media Format SDK, attributs des fichiers protégés
- Windows Media Format SDK, fichiers protégés
- ASF (Advanced Systems Format), affichage des attributs des fichiers protégés
- ASF (format des systèmes avancés), affichage des attributs des fichiers protégés
- ASF (Advanced Systems Format), attributs des fichiers protégés
- ASF (format des systèmes avancés), attributs des fichiers protégés
- ASF (Advanced Systems Format), fichiers protégés
- ASF (Advanced Systems Format), fichiers protégés
- gestion des droits numériques (DRM), affichage des attributs des fichiers protégés
- DRM (Digital Rights Management), affichage des attributs des fichiers protégés
- gestion des droits numériques (DRM), attributs des fichiers protégés
- DRM (gestion des droits numériques), attributs des fichiers protégés
- gestion des droits numériques (DRM), fichiers protégés
- DRM (gestion des droits numériques), fichiers protégés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642e9f580c3dffa1d3785985d548a5f971cfc218
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723395"
---
# <a name="viewing-attributes-of-protected-files"></a><span data-ttu-id="6b3da-118">Affichage des attributs des fichiers protégés</span><span class="sxs-lookup"><span data-stu-id="6b3da-118">Viewing Attributes of Protected Files</span></span>

<span data-ttu-id="6b3da-119">Dans certains scénarios, vous devrez peut-être récupérer certains attributs DRM dans un fichier sans avoir à accéder au contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="6b3da-119">In some scenarios, you may need to retrieve certain DRM attributes in a file without actually accessing the contents of the file.</span></span> <span data-ttu-id="6b3da-120">Cette fonctionnalité est utile, par exemple, dans les applications qui traitent des lots de fichiers de différentes manières en fonction des informations contenues dans l’en-tête de fichier.</span><span class="sxs-lookup"><span data-stu-id="6b3da-120">This capability is useful, for example, in applications that process batches of files in different ways based on information in the file header.</span></span> <span data-ttu-id="6b3da-121">Dans les versions précédentes du kit de développement logiciel (SDK) du format Windows Media, les applications devaient être liées à la bibliothèque statique DRM afin d’ouvrir n’importe quel fichier protégé.</span><span class="sxs-lookup"><span data-stu-id="6b3da-121">In previous versions of the Windows Media Format SDK, applications were required to link to the DRM static library in order to open any protected file.</span></span> <span data-ttu-id="6b3da-122">Les applications qui ne disposent pas de la bibliothèque DRM peuvent utiliser l’interface [**IWMDRMEditor :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) sur l’objet de l’éditeur de métadonnées pour examiner certains attributs DRM.</span><span class="sxs-lookup"><span data-stu-id="6b3da-122">Applications that do not have the DRM library can use the [**IWMDRMEditor::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) interface on the metadata editor object to examine certain DRM attributes.</span></span>

> [!Note]  
> <span data-ttu-id="6b3da-123">DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="6b3da-123">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6b3da-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6b3da-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b3da-125">**Liste des attributs DRM**</span><span class="sxs-lookup"><span data-stu-id="6b3da-125">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="6b3da-126">**Activation de la prise en charge de DRM**</span><span class="sxs-lookup"><span data-stu-id="6b3da-126">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="6b3da-127">**Interface IWMDRMEditor**</span><span class="sxs-lookup"><span data-stu-id="6b3da-127">**IWMDRMEditor Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)
</dt> </dl>

 

 




