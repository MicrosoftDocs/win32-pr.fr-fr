---
title: Événement Player. MediaCollectionMediaRemoved
description: L’événement MediaCollectionMediaRemoved se produit lorsqu’un élément multimédia est supprimé de la bibliothèque locale. | Événement Player. MediaCollectionMediaRemoved
ms.assetid: a1df6faf-38dc-4f5f-8f8a-953c91ea026c
keywords:
- Événement MediaCollectionMediaRemoved lecteur Windows Media
- Événement MediaCollectionMediaRemoved lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement MediaCollectionMediaRemoved
topic_type:
- apiref
api_name:
- Player.MediaCollectionMediaRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72af5fe4c5e90effeb34745ea71e3edb457da357
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531127"
---
# <a name="playermediacollectionmediaremoved-event"></a><span data-ttu-id="a3eae-107">Événement Player. MediaCollectionMediaRemoved</span><span class="sxs-lookup"><span data-stu-id="a3eae-107">Player.MediaCollectionMediaRemoved event</span></span>

<span data-ttu-id="a3eae-108">L’événement MediaCollectionMediaRemoved se produit lorsqu’un élément multimédia est supprimé de la bibliothèque locale.</span><span class="sxs-lookup"><span data-stu-id="a3eae-108">The MediaCollectionMediaRemoved event occurs when a media item is removed from the local library.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3eae-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3eae-109">Syntax</span></span>


```JScript
Player.MediaCollectionMediaRemoved(
  pdispMedia
)
```



## <a name="parameters"></a><span data-ttu-id="a3eae-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3eae-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3eae-111">*pdispMedia*</span><span class="sxs-lookup"><span data-stu-id="a3eae-111">*pdispMedia*</span></span> 
</dt> <dd>

<span data-ttu-id="a3eae-112">Objet **multimédia** qui a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="a3eae-112">**Media** object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3eae-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a3eae-113">Return value</span></span>

<span data-ttu-id="a3eae-114">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a3eae-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3eae-115">Notes</span><span class="sxs-lookup"><span data-stu-id="a3eae-115">Remarks</span></span>

<span data-ttu-id="a3eae-116">Cet événement se produit uniquement pour la bibliothèque locale.</span><span class="sxs-lookup"><span data-stu-id="a3eae-116">This event only occurs for the local library.</span></span>

<span data-ttu-id="a3eae-117">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a3eae-117">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3eae-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3eae-118">Requirements</span></span>



| <span data-ttu-id="a3eae-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3eae-119">Requirement</span></span> | <span data-ttu-id="a3eae-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3eae-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a3eae-121">Version</span><span class="sxs-lookup"><span data-stu-id="a3eae-121">Version</span></span><br/> | <span data-ttu-id="a3eae-122">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="a3eae-122">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="a3eae-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a3eae-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="a3eae-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3eae-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3eae-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3eae-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3eae-126">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="a3eae-126">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="a3eae-127">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="a3eae-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="a3eae-128">**Player. mediaCollection**</span><span class="sxs-lookup"><span data-stu-id="a3eae-128">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





