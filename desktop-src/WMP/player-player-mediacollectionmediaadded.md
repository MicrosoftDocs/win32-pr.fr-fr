---
title: Événement Player. MediaCollectionMediaAdded
description: L’événement MediaCollectionMediaAdded se produit lorsqu’un élément multimédia est ajouté à la bibliothèque locale. | Événement Player. MediaCollectionMediaAdded
ms.assetid: 01696d28-e83b-4fd2-8e88-2871831b61e7
keywords:
- Événement MediaCollectionMediaAdded lecteur Windows Media
- Événement MediaCollectionMediaAdded lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement MediaCollectionMediaAdded
topic_type:
- apiref
api_name:
- Player.MediaCollectionMediaAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d18dd0536f508090c46f9fc5a9059c809f50091d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545621"
---
# <a name="playermediacollectionmediaadded-event"></a><span data-ttu-id="c63f4-107">Événement Player. MediaCollectionMediaAdded</span><span class="sxs-lookup"><span data-stu-id="c63f4-107">Player.MediaCollectionMediaAdded event</span></span>

<span data-ttu-id="c63f4-108">L’événement MediaCollectionMediaAdded se produit lorsqu’un élément multimédia est ajouté à la bibliothèque locale.</span><span class="sxs-lookup"><span data-stu-id="c63f4-108">The MediaCollectionMediaAdded event occurs when a media item is added to the local library.</span></span>

## <a name="syntax"></a><span data-ttu-id="c63f4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c63f4-109">Syntax</span></span>


```JScript
Player.MediaCollectionMediaAdded(
  pdispMedia
)
```



## <a name="parameters"></a><span data-ttu-id="c63f4-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c63f4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c63f4-111">*pdispMedia*</span><span class="sxs-lookup"><span data-stu-id="c63f4-111">*pdispMedia*</span></span> 
</dt> <dd>

<span data-ttu-id="c63f4-112">Objet **multimédia** qui a été ajouté.</span><span class="sxs-lookup"><span data-stu-id="c63f4-112">**Media** object that was added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c63f4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c63f4-113">Return value</span></span>

<span data-ttu-id="c63f4-114">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c63f4-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c63f4-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c63f4-115">Remarks</span></span>

<span data-ttu-id="c63f4-116">Cet événement se produit uniquement pour la bibliothèque locale.</span><span class="sxs-lookup"><span data-stu-id="c63f4-116">This event only occurs for the local library.</span></span>

<span data-ttu-id="c63f4-117">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c63f4-117">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="c63f4-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c63f4-118">Requirements</span></span>



| <span data-ttu-id="c63f4-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c63f4-119">Requirement</span></span> | <span data-ttu-id="c63f4-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c63f4-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c63f4-121">Version</span><span class="sxs-lookup"><span data-stu-id="c63f4-121">Version</span></span><br/> | <span data-ttu-id="c63f4-122">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="c63f4-122">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="c63f4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c63f4-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="c63f4-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c63f4-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c63f4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c63f4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c63f4-126">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="c63f4-126">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="c63f4-127">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="c63f4-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="c63f4-128">**Player. mediaCollection**</span><span class="sxs-lookup"><span data-stu-id="c63f4-128">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





