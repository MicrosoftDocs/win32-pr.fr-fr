---
title: THÈME. openViewRelative
description: La méthode openViewRelative ouvre une vue dans une nouvelle fenêtre à une position initiale spécifiée par rapport à l’angle supérieur gauche de l’apparence.
ms.assetid: fc31a1ce-e6b9-4084-b244-28fad486f485
keywords:
- THEMe. openViewRelative Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openViewRelative
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80ec93055535640b84c33dde2b61ee59cd5bfdcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545483"
---
# <a name="themeopenviewrelative"></a><span data-ttu-id="34e59-104">THÈME. openViewRelative</span><span class="sxs-lookup"><span data-stu-id="34e59-104">THEME.openViewRelative</span></span>

<span data-ttu-id="34e59-105">La méthode **openViewRelative** ouvre une **vue** dans une nouvelle fenêtre à une position initiale spécifiée par rapport à l’angle supérieur gauche de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="34e59-105">The **openViewRelative** method opens a **VIEW** in a new window at a specified initial position relative to the upper-left corner of the skin.</span></span>

``` syntax
        theme.openView(view, left, top)
```

## <a name="parameters"></a><span data-ttu-id="34e59-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34e59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34e59-107"><span id="view"></span><span id="VIEW"></span>*affichage*</span><span class="sxs-lookup"><span data-stu-id="34e59-107"><span id="view"></span><span id="VIEW"></span>*view*</span></span>
</dt> <dd>

<span data-ttu-id="34e59-108">**Chaîne** spécifiant l' **ID** de la **vue** à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="34e59-108">A **String** specifying the **id** of the **VIEW** to open.</span></span>

</dd> <dt>

<span data-ttu-id="34e59-109"><span id="left"></span><span id="LEFT"></span>*gauche*</span><span class="sxs-lookup"><span data-stu-id="34e59-109"><span id="left"></span><span id="LEFT"></span>*left*</span></span>
</dt> <dd>

<span data-ttu-id="34e59-110">**Nombre** (**long**) qui spécifie la distance initiale, en pixels, de la bordure gauche de la **vue** à partir de la bordure gauche de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="34e59-110">A **Number** (**long**) specifying the initial distance in pixels of the left border of the **VIEW** from the left border of the skin.</span></span> <span data-ttu-id="34e59-111">Une valeur négative indique une position initiale à gauche de la bordure de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="34e59-111">A negative value indicates an initial position to the left of the skin border.</span></span>

</dd> <dt>

<span data-ttu-id="34e59-112"><span id="top"></span><span id="TOP"></span>*Retour au début*</span><span class="sxs-lookup"><span data-stu-id="34e59-112"><span id="top"></span><span id="TOP"></span>*top*</span></span>
</dt> <dd>

<span data-ttu-id="34e59-113">**Nombre** (**long**) qui spécifie la position initiale de la bordure supérieure de la **vue** par rapport à la bordure supérieure de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="34e59-113">A **Number** (**long**) specifying the initial position of the top border of the **VIEW** relative to the top border of the skin.</span></span> <span data-ttu-id="34e59-114">Une valeur négative indique une position initiale au-dessus de la bordure de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="34e59-114">A negative values indicates an initial position above the skin border.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34e59-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="34e59-115">Return Value</span></span>

<span data-ttu-id="34e59-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="34e59-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="34e59-117">Notes</span><span class="sxs-lookup"><span data-stu-id="34e59-117">Remarks</span></span>

<span data-ttu-id="34e59-118">La position spécifiée pour la **vue** est utilisée la première fois que cette méthode est appelée, après laquelle l’utilisateur peut faire glisser la **vue** vers un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="34e59-118">The position specified for the **VIEW** is used the first time this method is called, after which the user can drag the **VIEW** to another location.</span></span> <span data-ttu-id="34e59-119">La nouvelle position est enregistrée et, lors des appels suivants, la position la plus récente est utilisée.</span><span class="sxs-lookup"><span data-stu-id="34e59-119">The new position is saved, and on subsequent calls, the most recent position is used.</span></span>

## <a name="examples"></a><span data-ttu-id="34e59-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="34e59-120">Examples</span></span>


```JScript
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openViewRelative('newView', 50, 50)"/>
    <TEXT top="30" value="close" 
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="34e59-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34e59-121">Requirements</span></span>



| <span data-ttu-id="34e59-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34e59-122">Requirement</span></span> | <span data-ttu-id="34e59-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="34e59-123">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="34e59-124">Version</span><span class="sxs-lookup"><span data-stu-id="34e59-124">Version</span></span><br/> | <span data-ttu-id="34e59-125">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="34e59-125">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="34e59-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34e59-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34e59-127">**Élément THEMe**</span><span class="sxs-lookup"><span data-stu-id="34e59-127">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="34e59-128">**THÈME. évènement CloseView**</span><span class="sxs-lookup"><span data-stu-id="34e59-128">**THEME.closeView**</span></span>](theme-closeview.md)
</dt> <dt>

[<span data-ttu-id="34e59-129">**THEMe. openView**</span><span class="sxs-lookup"><span data-stu-id="34e59-129">**THEME.openView**</span></span>](theme-openview.md)
</dt> </dl>

 

 





