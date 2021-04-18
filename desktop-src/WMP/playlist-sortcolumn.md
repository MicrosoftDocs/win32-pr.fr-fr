---
title: PLAYLIST. sortColumn
description: La méthode sortColumn trie les données dans la colonne spécifiée.
ms.assetid: 1563fee8-044a-4cb4-a9c2-11d4533536da
keywords:
- PLAYLIST. sortColumn lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.sortColumn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f21f0032ee4db4c7af46b5dda814bb11db551330
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533271"
---
# <a name="playlistsortcolumn"></a><span data-ttu-id="774f0-104">PLAYLIST. sortColumn</span><span class="sxs-lookup"><span data-stu-id="774f0-104">PLAYLIST.sortColumn</span></span>

<span data-ttu-id="774f0-105">La méthode **SortColumn** trie les données dans la colonne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="774f0-105">The **sortColumn** method sorts the data in the specified column.</span></span>

``` syntax
        elementID.sortColumn(column)
```

## <a name="parameters"></a><span data-ttu-id="774f0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="774f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="774f0-107"><span id="column"></span><span id="COLUMN"></span>*chronique*</span><span class="sxs-lookup"><span data-stu-id="774f0-107"><span id="column"></span><span id="COLUMN"></span>*column*</span></span>
</dt> <dd>

<span data-ttu-id="774f0-108">**Nombre** (**long**) indiquant l’index de la colonne à trier.</span><span class="sxs-lookup"><span data-stu-id="774f0-108">**Number** (**long**) indicating the index of the column to sort.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="774f0-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="774f0-109">Return Value</span></span>

<span data-ttu-id="774f0-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="774f0-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="774f0-111">Notes</span><span class="sxs-lookup"><span data-stu-id="774f0-111">Remarks</span></span>

<span data-ttu-id="774f0-112">Cette méthode trie la colonne spécifiée de la même façon que les boutons d’en-tête de colonne dans l’élément **playlist** .</span><span class="sxs-lookup"><span data-stu-id="774f0-112">This method sorts the specified column in the same way as the column header buttons in the **PLAYLIST** element.</span></span> <span data-ttu-id="774f0-113">Si la colonne n’a pas encore été triée, elle est triée dans l’ordre alphanumérique.</span><span class="sxs-lookup"><span data-stu-id="774f0-113">If the column has not yet been sorted, it is sorted in alphanumeric order.</span></span> <span data-ttu-id="774f0-114">S’il a été trié, son ordre est inversé.</span><span class="sxs-lookup"><span data-stu-id="774f0-114">If it has been sorted, its order is reversed.</span></span>

<span data-ttu-id="774f0-115">Pour que cette méthode fonctionne, l’attribut **allowColumnSorting** doit avoir la valeur true.</span><span class="sxs-lookup"><span data-stu-id="774f0-115">For this method to work, the **allowColumnSorting** attribute must be set to true.</span></span>

## <a name="requirements"></a><span data-ttu-id="774f0-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="774f0-116">Requirements</span></span>



| <span data-ttu-id="774f0-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="774f0-117">Requirement</span></span> | <span data-ttu-id="774f0-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="774f0-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="774f0-119">Version</span><span class="sxs-lookup"><span data-stu-id="774f0-119">Version</span></span><br/> | <span data-ttu-id="774f0-120">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="774f0-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="774f0-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="774f0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="774f0-122">**Élément PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="774f0-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="774f0-123">**PLAYLIST. allowColumnSorting**</span><span class="sxs-lookup"><span data-stu-id="774f0-123">**PLAYLIST.allowColumnSorting**</span></span>](playlist-allowcolumnsorting.md)
</dt> </dl>

 

 





