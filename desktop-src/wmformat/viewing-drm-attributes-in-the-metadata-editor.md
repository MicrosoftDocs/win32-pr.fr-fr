---
title: Affichage des attributs DRM dans l’éditeur de métadonnées
description: Affichage des attributs DRM dans l’éditeur de métadonnées
ms.assetid: e25fb8c8-8f4d-40fd-aa6f-675921e0ccdd
keywords:
- Windows Media Format SDK, affichage des attributs DRM
- gestion des droits numériques (DRM), affichage des attributs
- DRM (gestion des droits numériques), affichage des attributs
- Windows Media Format SDK, éditeur de métadonnées
- gestion des droits numériques (DRM), éditeur de métadonnées
- DRM (gestion des droits numériques), éditeur de métadonnées
- Windows Media Format SDK, interface IWMDRMEditor
- gestion des droits numériques (DRM), interface IWMDRMEditor
- DRM (gestion des droits numériques), interface IWMDRMEditor
- Éditeur de métadonnées, affichage des attributs DRM
- Éditeur de métadonnées, interface IWMDRMEditor
- IWMDRMEditor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8541444ad7704ecc340476929f1205f11ccd61
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314317"
---
# <a name="viewing-drm-attributes-in-the-metadata-editor"></a><span data-ttu-id="9c22b-115">Affichage des attributs DRM dans l’éditeur de métadonnées</span><span class="sxs-lookup"><span data-stu-id="9c22b-115">Viewing DRM Attributes in the Metadata Editor</span></span>

<span data-ttu-id="9c22b-116">L’éditeur de métadonnées expose l’interface IWMDRMEditor, qui permet aux applications de modification d’examiner certains attributs d’un en-tête DRM dans un fichier ASF protégé, et les attributs de la licence de contenu, le cas échéant, même si l’application n’a pas la bibliothèque statique spécifique à DRM (wmstubdrm. lib) qui est requise pour les applications de lecteur et d’écriture DRM entièrement compatibles.</span><span class="sxs-lookup"><span data-stu-id="9c22b-116">The Metadata Editor exposes the IWMDRMEditor interface, which enables editing applications to examine certain attributes of a DRM header in a protected ASF file, and attributes in the content license, if one is present, even if the application doesn't have the DRM-specific static library (wmstubdrm.lib) that is required for fully-enabled DRM player and writer applications.</span></span>

> [!Note]  
> <span data-ttu-id="9c22b-117">DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="9c22b-117">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9c22b-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9c22b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c22b-119">**Fonctionnalités de Rights Management numérique**</span><span class="sxs-lookup"><span data-stu-id="9c22b-119">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="9c22b-120">**Interface IWMDRMEditor**</span><span class="sxs-lookup"><span data-stu-id="9c22b-120">**IWMDRMEditor Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)
</dt> </dl>

 

 




