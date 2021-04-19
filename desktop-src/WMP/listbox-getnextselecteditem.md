---
title: LISTBOX. getNextSelectedItem
description: La méthode getNextSelectedItem récupère l’élément sélectionné suivant dans le contrôle de zone de liste à partir de l’élément après celui avec l’index spécifié.
ms.assetid: 060d196d-2b14-4386-ba01-34256c137db5
keywords:
- LISTBOX. getNextSelectedItem Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afb3df1f1b6a6adc528e02dd6531ac4fc1a9a3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541100"
---
# <a name="listboxgetnextselecteditem"></a><span data-ttu-id="df28d-104">LISTBOX. getNextSelectedItem</span><span class="sxs-lookup"><span data-stu-id="df28d-104">LISTBOX.getNextSelectedItem</span></span>

<span data-ttu-id="df28d-105">La méthode **getNextSelectedItem** récupère l’élément sélectionné suivant dans le contrôle de zone de liste à partir de l’élément après celui avec l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="df28d-105">The **getNextSelectedItem** method retrieves the next selected item in the list box control starting at the item after the one with the specified index.</span></span>

``` syntax
        elementID.getNextSelectedItem(startIndex)
```

## <a name="parameters"></a><span data-ttu-id="df28d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df28d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df28d-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span><span class="sxs-lookup"><span data-stu-id="df28d-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span></span>
</dt> <dd>

<span data-ttu-id="df28d-108">**Nombre** (**long**) contenant l’index de l’élément qui précède l’élément en cours de récupération.</span><span class="sxs-lookup"><span data-stu-id="df28d-108">**Number** (**long**) containing the index of the item that precedes the item being retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df28d-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="df28d-109">Return Value</span></span>

<span data-ttu-id="df28d-110">Cette méthode retourne un **nombre** (**long**) contenant l’index de l’élément sélectionné suivant.</span><span class="sxs-lookup"><span data-stu-id="df28d-110">This method returns a **Number** (**long**) containing the index of the next selected item.</span></span>

## <a name="remarks"></a><span data-ttu-id="df28d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="df28d-111">Remarks</span></span>

<span data-ttu-id="df28d-112">Pour démarrer la recherche à partir du début, utilisez 1 pour l’index de début.</span><span class="sxs-lookup"><span data-stu-id="df28d-112">To start search from the beginning, use  1 for the start index.</span></span>

## <a name="requirements"></a><span data-ttu-id="df28d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df28d-113">Requirements</span></span>



| <span data-ttu-id="df28d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df28d-114">Requirement</span></span> | <span data-ttu-id="df28d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="df28d-115">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="df28d-116">Version</span><span class="sxs-lookup"><span data-stu-id="df28d-116">Version</span></span><br/> | <span data-ttu-id="df28d-117">Lecteur Windows Media pour Windows XP ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="df28d-117">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="df28d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df28d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df28d-119">**Élément LISTBOX**</span><span class="sxs-lookup"><span data-stu-id="df28d-119">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> </dl>

 

 





