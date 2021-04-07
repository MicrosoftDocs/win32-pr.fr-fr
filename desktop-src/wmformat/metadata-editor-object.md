---
title: Éditeur de métadonnées, objet
description: Éditeur de métadonnées, objet
ms.assetid: 224eea1c-1d0d-47ac-9d99-c13674284f6d
keywords:
- Windows Media Format SDK, objets de l’éditeur de métadonnées
- ASF (Advanced Systems Format), objets de l’éditeur de métadonnées
- ASF (format des systèmes avancés), objets de l’éditeur de métadonnées
- objets, objets de l’éditeur de métadonnées
- objets de l’éditeur de métadonnées, à propos de
- métadonnées, objets Editor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27a30f5bd22bef9533352927901ad2b8a9e44fe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724098"
---
# <a name="metadata-editor-object"></a><span data-ttu-id="c91f0-109">Éditeur de métadonnées, objet</span><span class="sxs-lookup"><span data-stu-id="c91f0-109">Metadata Editor Object</span></span>

<span data-ttu-id="c91f0-110">L’objet de l’éditeur de métadonnées permet de modifier les informations stockées dans la section d’en-tête des fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="c91f0-110">The metadata editor object is used to edit information stored in the header section of ASF files.</span></span> <span data-ttu-id="c91f0-111">Les éléments les plus courants manipulés par cet objet sont les attributs de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="c91f0-111">The most common things manipulated by this object are metadata attributes.</span></span> <span data-ttu-id="c91f0-112">En outre, l’éditeur de métadonnées traite des [*marqueurs*](wmformat-glossary.md) et des commandes de script.</span><span class="sxs-lookup"><span data-stu-id="c91f0-112">Additionally, the metadata editor deals with [*markers*](wmformat-glossary.md) and script commands.</span></span> <span data-ttu-id="c91f0-113">La seule fois où vous devez utiliser l’éditeur de métadonnées, c’est lorsque vous souhaitez modifier l’en-tête d’un fichier existant sans le visionner.</span><span class="sxs-lookup"><span data-stu-id="c91f0-113">The only time you need to use the metadata editor is when you want to edit the header of an existing file without playing it.</span></span>

<span data-ttu-id="c91f0-114">L’objet de l’éditeur de métadonnées est créé par la fonction [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor), qui définit un pointeur vers une interface **IWMMetadataEditor** .</span><span class="sxs-lookup"><span data-stu-id="c91f0-114">The metadata editor object is created by the function [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor), which sets a pointer to an **IWMMetadataEditor** interface.</span></span> <span data-ttu-id="c91f0-115">Les autres interfaces de l’objet de l’éditeur de métadonnées peuvent être obtenues en appelant la méthode **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="c91f0-115">The other interfaces of the metadata editor object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="c91f0-116">Les interfaces suivantes sont prises en charge par l’objet de l’éditeur de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="c91f0-116">The following interfaces are supported by the metadata editor object.</span></span>



| <span data-ttu-id="c91f0-117">Interface</span><span class="sxs-lookup"><span data-stu-id="c91f0-117">Interface</span></span>                                        | <span data-ttu-id="c91f0-118">Description</span><span class="sxs-lookup"><span data-stu-id="c91f0-118">Description</span></span>                                                                                                                                                                                            |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c91f0-119">**IWMDRMEditor**</span><span class="sxs-lookup"><span data-stu-id="c91f0-119">**IWMDRMEditor**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)             | <span data-ttu-id="c91f0-120">Permet aux applications de modifier d’examiner les propriétés [*DRM*](wmformat-glossary.md) d’un fichier ASF sans disposer de droits pour lire le contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="c91f0-120">Enables editing applications to examine the [*DRM*](wmformat-glossary.md) properties of an ASF file without having any rights to play the protected content.</span></span> |
| [<span data-ttu-id="c91f0-121">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="c91f0-121">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="c91f0-122">Manipule les attributs, les marqueurs et les commandes de script dans l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="c91f0-122">Manipulates attributes, markers, and script commands in the header.</span></span>                                                                                                                                    |
| [<span data-ttu-id="c91f0-123">**IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="c91f0-123">**IWMHeaderInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)         | <span data-ttu-id="c91f0-124">Récupère des informations de codec.</span><span class="sxs-lookup"><span data-stu-id="c91f0-124">Retrieves codec information.</span></span> <span data-ttu-id="c91f0-125">Hérite de toutes les méthodes de **IWMHeaderInfo**.</span><span class="sxs-lookup"><span data-stu-id="c91f0-125">Inherits all of the methods of **IWMHeaderInfo**.</span></span>                                                                                                                         |
| [<span data-ttu-id="c91f0-126">**IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="c91f0-126">**IWMHeaderInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)         | <span data-ttu-id="c91f0-127">Offre une prise en charge avancée des attributs, y compris des attributs volumineux, des langages multiples et des noms d’attributs en double.</span><span class="sxs-lookup"><span data-stu-id="c91f0-127">Provides advanced support for attributes, including large attributes, multiple languages, and duplicate attribute names.</span></span> <span data-ttu-id="c91f0-128">Hérite de toutes les méthodes de **IWMHeaderInfo** et **IWMHeaderInfo2**.</span><span class="sxs-lookup"><span data-stu-id="c91f0-128">Inherits all of the methods of **IWMHeaderInfo** and **IWMHeaderInfo2**.</span></span>      |
| [<span data-ttu-id="c91f0-129">**IWMMetadataEditor**</span><span class="sxs-lookup"><span data-stu-id="c91f0-129">**IWMMetadataEditor**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor)   | <span data-ttu-id="c91f0-130">Ouvre, ferme et enregistre les modifications apportées à l’en-tête d’un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="c91f0-130">Opens, closes, and saves changes to the header of an ASF file.</span></span>                                                                                                                                         |
| [<span data-ttu-id="c91f0-131">**IWMMetadataEditor2**</span><span class="sxs-lookup"><span data-stu-id="c91f0-131">**IWMMetadataEditor2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor2) | <span data-ttu-id="c91f0-132">Ouvre un fichier ASF pour la modification d’en-tête avec plusieurs options d’accès aux fichiers et de partage.</span><span class="sxs-lookup"><span data-stu-id="c91f0-132">Opens an ASF file for header editing with multiple file access and sharing options.</span></span> <span data-ttu-id="c91f0-133">Hérite de toutes les méthodes de **IWMMetadataEditor**.</span><span class="sxs-lookup"><span data-stu-id="c91f0-133">Inherits all of the methods of **IWMMetadataEditor**.</span></span>                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="c91f0-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c91f0-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c91f0-135">**Marqueurs**</span><span class="sxs-lookup"><span data-stu-id="c91f0-135">**Markers**</span></span>](markers.md)
</dt> <dt>

[<span data-ttu-id="c91f0-136">**Metadata**</span><span class="sxs-lookup"><span data-stu-id="c91f0-136">**Metadata**</span></span>](metadata.md)
</dt> <dt>

[<span data-ttu-id="c91f0-137">**Objets**</span><span class="sxs-lookup"><span data-stu-id="c91f0-137">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="c91f0-138">**Commandes de script**</span><span class="sxs-lookup"><span data-stu-id="c91f0-138">**Script Commands**</span></span>](script-commands.md)
</dt> <dt>

[<span data-ttu-id="c91f0-139">**Utilisation des métadonnées**</span><span class="sxs-lookup"><span data-stu-id="c91f0-139">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




