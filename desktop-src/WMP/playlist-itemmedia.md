---
title: PLAYLIST. itemMedia
description: L’attribut itemMedia récupère l’objet Media correspondant à l’index donné dans l’élément PLAYLIST.
ms.assetid: 38085798-7986-432f-8c88-de886bfc2ac5
keywords:
- Lecteur Windows Media PLAYLIST. itemMedia
topic_type:
- apiref
api_name:
- PLAYLIST.itemMedia
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 269e9011ade69ee61d99c29c1fa5bd1b9fa3deeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542557"
---
# <a name="playlistitemmedia"></a><span data-ttu-id="6ae32-104">PLAYLIST. itemMedia</span><span class="sxs-lookup"><span data-stu-id="6ae32-104">PLAYLIST.itemMedia</span></span>

<span data-ttu-id="6ae32-105">L’attribut **itemMedia** récupère l’objet **Media** correspondant à l’index donné dans l’élément **playlist** .</span><span class="sxs-lookup"><span data-stu-id="6ae32-105">The **itemMedia** attribute retrieves the **Media** object corresponding to the given index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.itemMedia(index)
```

## <a name="possible-values"></a><span data-ttu-id="6ae32-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="6ae32-106">Possible Values</span></span>

<span data-ttu-id="6ae32-107">Cet attribut est un objet **multimédia** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6ae32-107">This attribute is a read-only **Media** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="6ae32-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ae32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ae32-109"><span id="index"></span><span id="INDEX"></span>*évaluer*</span><span class="sxs-lookup"><span data-stu-id="6ae32-109"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="6ae32-110">**Nombre**(**long**) contenant l’index d’un élément de sélection.</span><span class="sxs-lookup"><span data-stu-id="6ae32-110">**Number**(**long**) containing the index of a playlist item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ae32-111">Notes</span><span class="sxs-lookup"><span data-stu-id="6ae32-111">Remarks</span></span>

<span data-ttu-id="6ae32-112">La propriété **itemMedia** retourne des objets multimédias qui sont développés dans l’élément **playlist** .</span><span class="sxs-lookup"><span data-stu-id="6ae32-112">The **itemMedia** property will return media objects that are expanded in the **PLAYLIST** element.</span></span> <span data-ttu-id="6ae32-113">Par exemple, s’il existe une sélection qui contient trois clips multimédias qui ne sont pas développés dans l’élément **playlist** , **itemMedia**(0) retourne la playlist en tant qu’objet multimédia.</span><span class="sxs-lookup"><span data-stu-id="6ae32-113">For example, if there is a playlist that contains three media clips that is not expanded in the **PLAYLIST** element, **itemMedia**(0) will return the playlist as the media object.</span></span> <span data-ttu-id="6ae32-114">Si la sélection est développée, **itemMedia**(0) retourne le premier clip multimédia de la sélection.</span><span class="sxs-lookup"><span data-stu-id="6ae32-114">If the playlist is expanded, **itemMedia**(0) will return the first media clip in the playlist.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ae32-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ae32-115">Requirements</span></span>



| <span data-ttu-id="6ae32-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ae32-116">Requirement</span></span> | <span data-ttu-id="6ae32-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ae32-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="6ae32-118">Version</span><span class="sxs-lookup"><span data-stu-id="6ae32-118">Version</span></span><br/> | <span data-ttu-id="6ae32-119">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6ae32-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6ae32-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ae32-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ae32-121">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="6ae32-121">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="6ae32-122">**Élément PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="6ae32-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





