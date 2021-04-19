---
title: VIEW. Size
description: La méthode size redimensionne la vue sur un bord spécifié.
ms.assetid: c15a33b2-3618-41a7-bff1-9d48a566ed4f
keywords:
- AFFICHER. taille du lecteur Windows Media
topic_type:
- apiref
api_name:
- VIEW.size
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: def9b416dfe5eda052ef430b587fa1c6017b4e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545393"
---
# <a name="viewsize"></a><span data-ttu-id="1e412-104">VIEW. Size</span><span class="sxs-lookup"><span data-stu-id="1e412-104">VIEW.size</span></span>

<span data-ttu-id="1e412-105">La méthode **Size** redimensionne la **vue** sur un bord spécifié.</span><span class="sxs-lookup"><span data-stu-id="1e412-105">The **size** method resizes the **VIEW** on a specified edge.</span></span>

``` syntax
        elementID.size(handle)
```

## <a name="parameters"></a><span data-ttu-id="1e412-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e412-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e412-107"><span id="handle"></span><span id="HANDLE"></span>*traitée*</span><span class="sxs-lookup"><span data-stu-id="1e412-107"><span id="handle"></span><span id="HANDLE"></span>*handle*</span></span>
</dt> <dd>

<span data-ttu-id="1e412-108">Chaîne spécifiant le bord ou le coin à déplacer lors du dimensionnement.</span><span class="sxs-lookup"><span data-stu-id="1e412-108">String specifying the edge or corner to move when sizing.</span></span> <span data-ttu-id="1e412-109">Cette chaîne doit avoir l’une des huit valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1e412-109">This string must have one of the following eight values.</span></span>



| <span data-ttu-id="1e412-110">Edge</span><span class="sxs-lookup"><span data-stu-id="1e412-110">Edge</span></span>   | <span data-ttu-id="1e412-111">Virage</span><span class="sxs-lookup"><span data-stu-id="1e412-111">Corner</span></span>      |
|--------|-------------|
| <span data-ttu-id="1e412-112">top</span><span class="sxs-lookup"><span data-stu-id="1e412-112">top</span></span>    | <span data-ttu-id="1e412-113">angle supérieur</span><span class="sxs-lookup"><span data-stu-id="1e412-113">topright</span></span>    |
| <span data-ttu-id="1e412-114">droite</span><span class="sxs-lookup"><span data-stu-id="1e412-114">right</span></span>  | <span data-ttu-id="1e412-115">telle</span><span class="sxs-lookup"><span data-stu-id="1e412-115">bottomright</span></span> |
| <span data-ttu-id="1e412-116">bottom</span><span class="sxs-lookup"><span data-stu-id="1e412-116">bottom</span></span> | <span data-ttu-id="1e412-117">bottomleft</span><span class="sxs-lookup"><span data-stu-id="1e412-117">bottomleft</span></span>  |
| <span data-ttu-id="1e412-118">gauche</span><span class="sxs-lookup"><span data-stu-id="1e412-118">left</span></span>   | <span data-ttu-id="1e412-119">côté gauche</span><span class="sxs-lookup"><span data-stu-id="1e412-119">topleft</span></span>     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e412-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1e412-120">Return Value</span></span>

<span data-ttu-id="1e412-121">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1e412-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e412-122">Notes</span><span class="sxs-lookup"><span data-stu-id="1e412-122">Remarks</span></span>

<span data-ttu-id="1e412-123">Cette méthode est généralement appelée à partir d’un gestionnaire **OnMouseDown** .</span><span class="sxs-lookup"><span data-stu-id="1e412-123">This method is typically called from within an **onmousedown** handler.</span></span> <span data-ttu-id="1e412-124">Le redimensionnement s’effectue pendant le déplacement de la souris et arrête le redimensionnement lorsque le bouton de la souris est relâché.</span><span class="sxs-lookup"><span data-stu-id="1e412-124">It takes care of resizing while the mouse is dragged and stops resizing when the mouse button is released.</span></span> <span data-ttu-id="1e412-125">Si la taille de la **vue** est restreinte, vous ne pouvez pas faire glisser la souris pour redimensionner la **vue** au-delà des limites restreintes.</span><span class="sxs-lookup"><span data-stu-id="1e412-125">If the size of the **VIEW** is restricted, you cannot drag the mouse to resize the **View** beyond the restricted bounds.</span></span>

## <a name="examples"></a><span data-ttu-id="1e412-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="1e412-126">Examples</span></span>


```JScript
<THEME>
  <VIEW id="View1" backgroundImage="greenstone.bmp">
    <BUTTON id="sizer" horizontalAlignment="right" 
        verticalAlignment="bottom" image="Open.png" 
        onmousedown="jscript:View1.size('bottomright')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="1e412-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e412-127">Requirements</span></span>



| <span data-ttu-id="1e412-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e412-128">Requirement</span></span> | <span data-ttu-id="1e412-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e412-129">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1e412-130">Version</span><span class="sxs-lookup"><span data-stu-id="1e412-130">Version</span></span><br/> | <span data-ttu-id="1e412-131">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="1e412-131">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1e412-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e412-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e412-133">**Élément VIEW**</span><span class="sxs-lookup"><span data-stu-id="1e412-133">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





