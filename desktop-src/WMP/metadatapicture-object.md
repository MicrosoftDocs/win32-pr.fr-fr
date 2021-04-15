---
title: Objet MetadataPicture
description: L’objet MetadataPicture fournit un moyen de récupérer les valeurs de l’attribut de métadonnées WM/Picture. Cet attribut correspond à une pochette d’album contenue dans un fichier multimédia numérique, et non à une pochette d’album téléchargée sur Internet.
ms.assetid: c0d6f43d-1a88-4ac2-a7b3-c502f4d57afb
keywords:
- Objet MetadataPicture lecteur Windows Media
topic_type:
- apiref
api_name:
- MetadataPicture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 892b162ba05ab43740565c849b00bc4e3c52aad6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463554"
---
# <a name="metadatapicture-object"></a><span data-ttu-id="3fe5d-105">Objet MetadataPicture</span><span class="sxs-lookup"><span data-stu-id="3fe5d-105">MetadataPicture Object</span></span>

<span data-ttu-id="3fe5d-106">L’objet **MetadataPicture** fournit un moyen de récupérer les valeurs de l’attribut de métadonnées [**WM/Picture**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) .</span><span class="sxs-lookup"><span data-stu-id="3fe5d-106">The **MetadataPicture** object provides a way to retrieve the values of the [**WM/Picture**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) metadata attribute.</span></span> <span data-ttu-id="3fe5d-107">Cet attribut correspond à une pochette d’album contenue dans un fichier multimédia numérique, et non à une pochette d’album téléchargée sur Internet.</span><span class="sxs-lookup"><span data-stu-id="3fe5d-107">This attribute corresponds to album art contained in a digital media file, not to album art downloaded over the Internet.</span></span>

<span data-ttu-id="3fe5d-108">L’objet **MetadataPicture** prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3fe5d-108">The **MetadataPicture** object supports the following properties.</span></span>



| <span data-ttu-id="3fe5d-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="3fe5d-109">Property</span></span>                                           | <span data-ttu-id="3fe5d-110">Description</span><span class="sxs-lookup"><span data-stu-id="3fe5d-110">Description</span></span>                                       |
|----------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="3fe5d-111">**descriptive**</span><span class="sxs-lookup"><span data-stu-id="3fe5d-111">**description**</span></span>](metadatapicture-description.md) | <span data-ttu-id="3fe5d-112">Récupère une description de l’image de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3fe5d-112">Retrieves a description of the metadata image.</span></span>    |
| [<span data-ttu-id="3fe5d-113">**mimeType**</span><span class="sxs-lookup"><span data-stu-id="3fe5d-113">**mimeType**</span></span>](metadatapicture-mimetype.md)       | <span data-ttu-id="3fe5d-114">Récupère le type MIME de l’image de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3fe5d-114">Retrieves the MIME type of the metadata image.</span></span>    |
| [<span data-ttu-id="3fe5d-115">**Picture**</span><span class="sxs-lookup"><span data-stu-id="3fe5d-115">**pictureType**</span></span>](metadatapicture-picturetype.md) | <span data-ttu-id="3fe5d-116">Récupère le type d’image de l’image de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3fe5d-116">Retrieves the picture type of the metadata image.</span></span> |
| [<span data-ttu-id="3fe5d-117">**URL**</span><span class="sxs-lookup"><span data-stu-id="3fe5d-117">**URL**</span></span>](metadatapicture-url.md)                 | <span data-ttu-id="3fe5d-118">À usage interne uniquement</span><span class="sxs-lookup"><span data-stu-id="3fe5d-118">Internal use only.</span></span>                                |



 

<span data-ttu-id="3fe5d-119">L’objet **MetadataPicture** est accessible par le biais de la méthode suivante.</span><span class="sxs-lookup"><span data-stu-id="3fe5d-119">The **MetadataPicture** object is accessed through the following method.</span></span>



| <span data-ttu-id="3fe5d-120">Object</span><span class="sxs-lookup"><span data-stu-id="3fe5d-120">Object</span></span>                        | <span data-ttu-id="3fe5d-121">Méthode</span><span class="sxs-lookup"><span data-stu-id="3fe5d-121">Method</span></span>                                               |
|-------------------------------|------------------------------------------------------|
| [<span data-ttu-id="3fe5d-122">**Multimédia**</span><span class="sxs-lookup"><span data-stu-id="3fe5d-122">**Media**</span></span>](media-object.md) | [<span data-ttu-id="3fe5d-123">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="3fe5d-123">**getItemInfoByType**</span></span>](media-getiteminfobytype.md) |



 

<span data-ttu-id="3fe5d-124">À des fins d’illustration, `player.currentMedia.getItemInfoByType(name, language, index)` est utilisé dans les sections de syntaxe de référence.</span><span class="sxs-lookup"><span data-stu-id="3fe5d-124">For purposes of illustration, `player.currentMedia.getItemInfoByType(name, language, index)` is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="3fe5d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3fe5d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fe5d-126">**Référence du modèle objet pour l’écriture de scripts**</span><span class="sxs-lookup"><span data-stu-id="3fe5d-126">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 