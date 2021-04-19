---
title: Interface IWMPMetadataPicture (VB et C) (WMP. h)
description: Fournit des propriétés pour obtenir des informations sur l’image contenue dans un fichier multimédia numérique qui est représenté par un attribut WM/Picturemetadata.
ms.assetid: f8260882-dfb8-4ff0-954c-5060cb7a6995
keywords:
- IWMPMetadataPicture (VB et C) interface Windows Media Player
- Interface IWMPMetadataPicture (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPMetadataPicture (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3b462c431a136745974dcde5716c3bd81226f15
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541681"
---
# <a name="iwmpmetadatapicture-vb-and-c-interface"></a><span data-ttu-id="c553f-105">Interface IWMPMetadataPicture (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="c553f-105">IWMPMetadataPicture (VB and C#) interface</span></span>

<span data-ttu-id="c553f-106">Fournit des propriétés pour obtenir des informations sur l’image contenue dans un fichier multimédia numérique représenté par un attribut de métadonnées [**WM/Picture**](/windows/desktop/wmformat/wmpicture).</span><span class="sxs-lookup"><span data-stu-id="c553f-106">Provides properties for getting information about the image contained in a digital media file that is represented by a [**WM/Picture**](/windows/desktop/wmformat/wmpicture)metadata attribute.</span></span> <span data-ttu-id="c553f-107">Cet attribut correspond aux images de la pochette d’album contenues dans un fichier multimédia numérique, et non à une pochette d’album téléchargée sur Internet.</span><span class="sxs-lookup"><span data-stu-id="c553f-107">This attribute corresponds to album art images contained in a digital media file, not to album art downloaded over the Internet.</span></span>

<span data-ttu-id="c553f-108">L’interface **IWMPMetadataPicture** expose les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c553f-108">The **IWMPMetadataPicture** interface exposes the following properties.</span></span>



| <span data-ttu-id="c553f-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="c553f-109">Property</span></span>                                                                                   | <span data-ttu-id="c553f-110">Description</span><span class="sxs-lookup"><span data-stu-id="c553f-110">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="c553f-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="c553f-111">**Description**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-description--vb-and-c.md) | <span data-ttu-id="c553f-112">Obtient la description de l’image représentée par l’attribut de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="c553f-112">Gets the description of the image represented by the metadata attribute.</span></span>  |
| [<span data-ttu-id="c553f-113">**mimeType**</span><span class="sxs-lookup"><span data-stu-id="c553f-113">**mimeType**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-mimetype--vb-and-c.md)       | <span data-ttu-id="c553f-114">Obtient le type MIME de l’image représentée par l’attribut de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="c553f-114">Gets the MIME type of the image represented by the metadata attribute.</span></span>    |
| [<span data-ttu-id="c553f-115">**Picture**</span><span class="sxs-lookup"><span data-stu-id="c553f-115">**pictureType**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-picturetype--vb-and-c.md) | <span data-ttu-id="c553f-116">Obtient le type d’image de l’image représentée par l’attribut de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="c553f-116">Gets the picture type of the image represented by the metadata attribute.</span></span> |
| [<span data-ttu-id="c553f-117">**URL**</span><span class="sxs-lookup"><span data-stu-id="c553f-117">**URL**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-url--vb-and-c.md)                 | <span data-ttu-id="c553f-118">À usage interne uniquement</span><span class="sxs-lookup"><span data-stu-id="c553f-118">Internal use only.</span></span>                                                        |



 

<span data-ttu-id="c553f-119">Récupérez une interface **IWMPMetadataPicture** en passant le nom d’attribut [**WM/Picture**](/windows/desktop/wmformat/wmpicture) à la méthode suivante et en effectuant un cast de l’objet retourné.</span><span class="sxs-lookup"><span data-stu-id="c553f-119">Get an **IWMPMetadataPicture** interface by passing in the attribute name [**WM/Picture**](/windows/desktop/wmformat/wmpicture) to the following method and casting the object that is returned.</span></span>



| <span data-ttu-id="c553f-120">Interface</span><span class="sxs-lookup"><span data-stu-id="c553f-120">Interface</span></span>                                  | <span data-ttu-id="c553f-121">Propriété</span><span class="sxs-lookup"><span data-stu-id="c553f-121">Property</span></span>                                                                             |
|--------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="c553f-122">**IWMPMedia3**</span><span class="sxs-lookup"><span data-stu-id="c553f-122">**IWMPMedia3**</span></span>](iwmpmedia3--vb-and-c.md) | [<span data-ttu-id="c553f-123">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="c553f-123">**getItemInfoByType**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md) |



 

## <a name="members"></a><span data-ttu-id="c553f-124">Membres</span><span class="sxs-lookup"><span data-stu-id="c553f-124">Members</span></span>

<span data-ttu-id="c553f-125">L’interface **IWMPMetadataPicture (VB et C#)** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="c553f-125">The **IWMPMetadataPicture (VB and C#)** interface does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="c553f-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c553f-126">Requirements</span></span>



| <span data-ttu-id="c553f-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c553f-127">Requirement</span></span> | <span data-ttu-id="c553f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="c553f-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c553f-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="c553f-129">Header</span></span><br/> | <dl> <span data-ttu-id="c553f-130"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="c553f-130"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c553f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c553f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c553f-132">**Interfaces pour Visual Basic .NET et C #**</span><span class="sxs-lookup"><span data-stu-id="c553f-132">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

