---
title: VIEW. redimensionnable
description: L’attribut redimensionnable récupère une valeur indiquant si la vue peut être redimensionnée.
ms.assetid: 4f0e4f31-cf16-498f-823f-da43566043b1
keywords:
- AFFICHAGE. lecteur Windows Media redimensionnable
topic_type:
- apiref
api_name:
- VIEW.resizable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4d61973e34891d336ea5729ea40478c6c32808
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545325"
---
# <a name="viewresizable"></a><span data-ttu-id="c1616-104">VIEW. redimensionnable</span><span class="sxs-lookup"><span data-stu-id="c1616-104">VIEW.resizable</span></span>

<span data-ttu-id="c1616-105">L’attribut **redimensionnable** récupère une valeur indiquant si la **vue** peut être redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="c1616-105">The **resizable** attribute retrieves a value indicating whether the **VIEW** can be resized.</span></span>

``` syntax
        elementID.resizable
```

## <a name="possible-values"></a><span data-ttu-id="c1616-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="c1616-106">Possible Values</span></span>

<span data-ttu-id="c1616-107">Cet attribut est une valeur **booléenne** en lecture seule avec une valeur par défaut égale à l’attribut **TitleBar** .</span><span class="sxs-lookup"><span data-stu-id="c1616-107">This attribute is a read-only **Boolean** with a default value equal to the **titlebar** attribute.</span></span>



| <span data-ttu-id="c1616-108">Valeurs</span><span class="sxs-lookup"><span data-stu-id="c1616-108">Values</span></span> | <span data-ttu-id="c1616-109">Description</span><span class="sxs-lookup"><span data-stu-id="c1616-109">Description</span></span>             |
|--------|-------------------------|
| <span data-ttu-id="c1616-110">true</span><span class="sxs-lookup"><span data-stu-id="c1616-110">true</span></span>   | <span data-ttu-id="c1616-111">La vue peut être redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="c1616-111">View can be resized.</span></span>    |
| <span data-ttu-id="c1616-112">false</span><span class="sxs-lookup"><span data-stu-id="c1616-112">false</span></span>  | <span data-ttu-id="c1616-113">Impossible de redimensionner la vue.</span><span class="sxs-lookup"><span data-stu-id="c1616-113">View cannot be resized.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c1616-114">Notes</span><span class="sxs-lookup"><span data-stu-id="c1616-114">Remarks</span></span>

<span data-ttu-id="c1616-115">S’il n’y a pas de **TitleBar** et, par conséquent, aucune fenêtre ou bordure, vous devez utiliser la méthode **Size** pour redimensionner l’élément **View** .</span><span class="sxs-lookup"><span data-stu-id="c1616-115">If there is no **titlebar**, and therefore no window or border, you must use the **size** method to resize the **VIEW** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1616-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1616-116">Requirements</span></span>



| <span data-ttu-id="c1616-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1616-117">Requirement</span></span> | <span data-ttu-id="c1616-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1616-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c1616-119">Version</span><span class="sxs-lookup"><span data-stu-id="c1616-119">Version</span></span><br/> | <span data-ttu-id="c1616-120">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="c1616-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1616-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1616-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1616-122">**Élément VIEW**</span><span class="sxs-lookup"><span data-stu-id="c1616-122">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





