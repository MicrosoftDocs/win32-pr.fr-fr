---
title: MediaType (attribut)
description: L’attribut MediaType est le type de contenu de l’élément.
ms.assetid: 0d8a6937-32d8-4a4a-87e5-0002f077fefe
keywords:
- Attribut MediaType lecteur Windows Media
topic_type:
- apiref
api_name:
- MediaType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5779552f62007aa3dd3da0e2f4253fcf5499a6be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542325"
---
# <a name="mediatype-attribute"></a><span data-ttu-id="77e20-104">MediaType (attribut)</span><span class="sxs-lookup"><span data-stu-id="77e20-104">MediaType Attribute</span></span>

<span data-ttu-id="77e20-105">L’attribut **MediaType** est le type de contenu de l’élément.</span><span class="sxs-lookup"><span data-stu-id="77e20-105">The **MediaType** attribute is the type of content in the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="77e20-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="77e20-106">Applies To</span></span>

-   [<span data-ttu-id="77e20-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="77e20-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="77e20-108">Autres éléments</span><span class="sxs-lookup"><span data-stu-id="77e20-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="77e20-109">Éléments de photo</span><span class="sxs-lookup"><span data-stu-id="77e20-109">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="77e20-110">Sélections</span><span class="sxs-lookup"><span data-stu-id="77e20-110">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="77e20-111">Éléments radio</span><span class="sxs-lookup"><span data-stu-id="77e20-111">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="77e20-112">Éléments vidéo</span><span class="sxs-lookup"><span data-stu-id="77e20-112">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="77e20-113">Notes</span><span class="sxs-lookup"><span data-stu-id="77e20-113">Remarks</span></span>

<span data-ttu-id="77e20-114">Cet attribut est stocké uniquement dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="77e20-114">This attribute is stored only in the library.</span></span>

<span data-ttu-id="77e20-115">Cet attribut a l’une des valeurs suivantes : « audio », « other », « photo », « playlist », « radio » ou « Video ».</span><span class="sxs-lookup"><span data-stu-id="77e20-115">This attribute has one of the following values: "audio", "other", "photo", "playlist", "radio", or "video".</span></span> <span data-ttu-id="77e20-116">Utilisez cet attribut avec *MediaCollection*. méthode **getByAttribute** pour récupérer une sélection contenant tous les éléments d’un type particulier.</span><span class="sxs-lookup"><span data-stu-id="77e20-116">Use this attribute with the *MediaCollection*.**getByAttribute** method to retrieve a playlist containing all of the items of a particular type.</span></span>

<span data-ttu-id="77e20-117">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="77e20-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="77e20-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77e20-118">Requirements</span></span>



| <span data-ttu-id="77e20-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77e20-119">Requirement</span></span> | <span data-ttu-id="77e20-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="77e20-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="77e20-121">Version</span><span class="sxs-lookup"><span data-stu-id="77e20-121">Version</span></span><br/> | <span data-ttu-id="77e20-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="77e20-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="77e20-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77e20-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77e20-124">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="77e20-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="77e20-125">**MediaCollection.getByAttribute**</span><span class="sxs-lookup"><span data-stu-id="77e20-125">**MediaCollection.getByAttribute**</span></span>](mediacollection-getbyattribute.md)
</dt> </dl>

 

 





