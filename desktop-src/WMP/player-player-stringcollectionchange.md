---
title: Événement Player. StringCollectionChange
description: L’événement StringCollectionChange se produit lorsqu’une collection de chaînes change. | Événement Player. StringCollectionChange
ms.assetid: 465ec694-afd1-4baa-b559-3ab75874388f
keywords:
- Événement StringCollectionChange lecteur Windows Media
- Événement StringCollectionChange lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement StringCollectionChange
topic_type:
- apiref
api_name:
- Player.StringCollectionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29f72d7af0f73d74393d980b2506a3b7f05e578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523496"
---
# <a name="playerstringcollectionchange-event"></a><span data-ttu-id="e2523-107">Événement Player. StringCollectionChange</span><span class="sxs-lookup"><span data-stu-id="e2523-107">Player.StringCollectionChange event</span></span>

<span data-ttu-id="e2523-108">L’événement StringCollectionChange se produit lorsqu’une collection de chaînes change.</span><span class="sxs-lookup"><span data-stu-id="e2523-108">The StringCollectionChange event occurs when a string collection changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2523-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2523-109">Syntax</span></span>


```JScript
Player.StringCollectionChange(
  pdispStringCollection,
  change,
  lCollectionIndex
)
```



## <a name="parameters"></a><span data-ttu-id="e2523-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2523-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2523-111">*pdispStringCollection*</span><span class="sxs-lookup"><span data-stu-id="e2523-111">*pdispStringCollection*</span></span> 
</dt> <dd>

<span data-ttu-id="e2523-112">Objet **StringCollection** modifié.</span><span class="sxs-lookup"><span data-stu-id="e2523-112">**StringCollection** object that changed.</span></span>

</dd> <dt>

<span data-ttu-id="e2523-113">*change*</span><span class="sxs-lookup"><span data-stu-id="e2523-113">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="e2523-114">Nombre (long) indiquant le type de modification qui s’est produite dans la collection de chaînes.</span><span class="sxs-lookup"><span data-stu-id="e2523-114">Number (long)indicating the type of change that occurred to the string collection.</span></span> <span data-ttu-id="e2523-115">Contient l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e2523-115">Includes one of the following values.</span></span>



|        |                                    |
|--------|------------------------------------|
| <span data-ttu-id="e2523-116">Number</span><span class="sxs-lookup"><span data-stu-id="e2523-116">Number</span></span> | <span data-ttu-id="e2523-117">Description</span><span class="sxs-lookup"><span data-stu-id="e2523-117">Description</span></span>                        |
| <span data-ttu-id="e2523-118">0</span><span class="sxs-lookup"><span data-stu-id="e2523-118">0</span></span>      | <span data-ttu-id="e2523-119">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="e2523-119">Unknown.</span></span> <span data-ttu-id="e2523-120">(Valeur non valide)</span><span class="sxs-lookup"><span data-stu-id="e2523-120">(Not a valid value)</span></span>       |
| <span data-ttu-id="e2523-121">1</span><span class="sxs-lookup"><span data-stu-id="e2523-121">1</span></span>      | <span data-ttu-id="e2523-122">Un élément a été inséré.</span><span class="sxs-lookup"><span data-stu-id="e2523-122">An item was inserted.</span></span>              |
| <span data-ttu-id="e2523-123">2</span><span class="sxs-lookup"><span data-stu-id="e2523-123">2</span></span>      | <span data-ttu-id="e2523-124">La collection de chaînes a changé.</span><span class="sxs-lookup"><span data-stu-id="e2523-124">The string collection changed.</span></span>     |
| <span data-ttu-id="e2523-125">3</span><span class="sxs-lookup"><span data-stu-id="e2523-125">3</span></span>      | <span data-ttu-id="e2523-126">Un élément a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="e2523-126">An item was deleted.</span></span>               |
| <span data-ttu-id="e2523-127">4</span><span class="sxs-lookup"><span data-stu-id="e2523-127">4</span></span>      | <span data-ttu-id="e2523-128">La collection de chaînes a été effacée.</span><span class="sxs-lookup"><span data-stu-id="e2523-128">The string collection was cleared.</span></span> |
| <span data-ttu-id="e2523-129">5</span><span class="sxs-lookup"><span data-stu-id="e2523-129">5</span></span>      | <span data-ttu-id="e2523-130">Les mises à jour en bloc commencent.</span><span class="sxs-lookup"><span data-stu-id="e2523-130">Bulk updates are beginning.</span></span>        |
| <span data-ttu-id="e2523-131">6</span><span class="sxs-lookup"><span data-stu-id="e2523-131">6</span></span>      | <span data-ttu-id="e2523-132">Les mises à jour en bloc se sont terminées.</span><span class="sxs-lookup"><span data-stu-id="e2523-132">Bulk updates have ended.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="e2523-133">*lCollectionIndex*</span><span class="sxs-lookup"><span data-stu-id="e2523-133">*lCollectionIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="e2523-134">Nombre (long) contenant l’index de l’élément de collection de chaînes qui a changé.</span><span class="sxs-lookup"><span data-stu-id="e2523-134">Number (long) containing the index of the string collection item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2523-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e2523-135">Return value</span></span>

<span data-ttu-id="e2523-136">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e2523-136">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2523-137">Notes</span><span class="sxs-lookup"><span data-stu-id="e2523-137">Remarks</span></span>

<span data-ttu-id="e2523-138">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e2523-138">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2523-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2523-139">Requirements</span></span>



| <span data-ttu-id="e2523-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2523-140">Requirement</span></span> | <span data-ttu-id="e2523-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2523-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e2523-142">Version</span><span class="sxs-lookup"><span data-stu-id="e2523-142">Version</span></span><br/> | <span data-ttu-id="e2523-143">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="e2523-143">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="e2523-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e2523-144">DLL</span></span><br/>     | <dl> <span data-ttu-id="e2523-145"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2523-145"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2523-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2523-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2523-147">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="e2523-147">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="e2523-148">**StringCollection, objet**</span><span class="sxs-lookup"><span data-stu-id="e2523-148">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





