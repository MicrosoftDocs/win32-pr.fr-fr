---
title: Query. beginNextGroup, méthode
description: La méthode beginNextGroup commence un nouveau groupe de conditions. | Query. beginNextGroup, méthode
ms.assetid: e0c59bd0-0789-413e-ade8-8d53c6f3e19b
keywords:
- méthode beginNextGroup lecteur Windows Media
- méthode beginNextGroup lecteur Windows Media, classe Query
- Classe de requête lecteur Windows Media, méthode beginNextGroup
topic_type:
- apiref
api_name:
- Query.beginNextGroup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46c043b9a0ea506e054877b4d8122304ced75e28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543878"
---
# <a name="querybeginnextgroup-method"></a><span data-ttu-id="e98a3-107">Query. beginNextGroup, méthode</span><span class="sxs-lookup"><span data-stu-id="e98a3-107">Query.beginNextGroup method</span></span>

<span data-ttu-id="e98a3-108">La méthode **beginNextGroup** commence un nouveau groupe de conditions.</span><span class="sxs-lookup"><span data-stu-id="e98a3-108">The **beginNextGroup** method begins a new condition group.</span></span>

## <a name="syntax"></a><span data-ttu-id="e98a3-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e98a3-109">Syntax</span></span>


```JScript
Query.beginNextGroup()
```



## <a name="parameters"></a><span data-ttu-id="e98a3-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e98a3-110">Parameters</span></span>

<span data-ttu-id="e98a3-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e98a3-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e98a3-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e98a3-112">Return value</span></span>

<span data-ttu-id="e98a3-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e98a3-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e98a3-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e98a3-114">Remarks</span></span>

<span data-ttu-id="e98a3-115">Le démarrage d’un nouveau groupe de conditions implique que vous avez terminé le groupe de conditions actuel.</span><span class="sxs-lookup"><span data-stu-id="e98a3-115">Beginning a new condition group implies that you have completed the current condition group.</span></span> <span data-ttu-id="e98a3-116">Le nouveau groupe de conditions est toujours concaténé au groupe de conditions précédent à l’aide de ou de la logique.</span><span class="sxs-lookup"><span data-stu-id="e98a3-116">The new condition group is always concatenated to the previous condition group using OR logic.</span></span>

## <a name="requirements"></a><span data-ttu-id="e98a3-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e98a3-117">Requirements</span></span>



| <span data-ttu-id="e98a3-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e98a3-118">Requirement</span></span> | <span data-ttu-id="e98a3-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e98a3-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e98a3-120">Version</span><span class="sxs-lookup"><span data-stu-id="e98a3-120">Version</span></span><br/> | <span data-ttu-id="e98a3-121">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="e98a3-121">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="e98a3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e98a3-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="e98a3-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e98a3-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e98a3-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e98a3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e98a3-125">**MediaCollection. createQuery**</span><span class="sxs-lookup"><span data-stu-id="e98a3-125">**MediaCollection.createQuery**</span></span>](mediacollection-createquery.md)
</dt> <dt>

[<span data-ttu-id="e98a3-126">**MediaCollection.getPlaylistByQuery**</span><span class="sxs-lookup"><span data-stu-id="e98a3-126">**MediaCollection.getPlaylistByQuery**</span></span>](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[<span data-ttu-id="e98a3-127">**MediaCollection.getStringCollectionByQuery**</span><span class="sxs-lookup"><span data-stu-id="e98a3-127">**MediaCollection.getStringCollectionByQuery**</span></span>](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[<span data-ttu-id="e98a3-128">**Objet Query**</span><span class="sxs-lookup"><span data-stu-id="e98a3-128">**Query Object**</span></span>](query-object.md)
</dt> <dt>

[<span data-ttu-id="e98a3-129">**Query. addCondition**</span><span class="sxs-lookup"><span data-stu-id="e98a3-129">**Query.addCondition**</span></span>](query-addcondition.md)
</dt> </dl>

 

 





