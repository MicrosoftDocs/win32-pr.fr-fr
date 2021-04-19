---
title: VIDÉO. sans fenêtre
description: L’attribut sans fenêtre spécifie ou récupère une valeur indiquant si le contrôle vidéo sera fenêtre ou sans fenêtre ; autrement dit, si le rectangle entier du contrôle est visible à tout moment ou s’il peut être coupé.
ms.assetid: d59e6baf-374b-48f6-b99f-35a83af7feb6
keywords:
- VIDÉO. Windows Media Player sans fenêtre
topic_type:
- apiref
api_name:
- VIDEO.windowless
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a17d905d2ba8c11254476337d656890469b2b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528527"
---
# <a name="videowindowless"></a><span data-ttu-id="ac39b-104">VIDÉO. sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="ac39b-104">VIDEO.windowless</span></span>

<span data-ttu-id="ac39b-105">L’attribut **sans fenêtre** spécifie ou récupère une valeur indiquant si le contrôle vidéo sera fenêtre ou sans fenêtre ; autrement dit, si le rectangle entier du contrôle est visible à tout moment ou s’il peut être coupé.</span><span class="sxs-lookup"><span data-stu-id="ac39b-105">The **windowless** attribute specifies or retrieves a value indicating whether the Video control will be windowed or windowless; that is, whether the entire rectangle of the control will be visible at all times or can be clipped.</span></span> <span data-ttu-id="ac39b-106">Ne peut être défini qu’au moment de la conception.</span><span class="sxs-lookup"><span data-stu-id="ac39b-106">Can only be set at design time.</span></span>

``` syntax
        elementID.windowless
```

## <a name="possible-values"></a><span data-ttu-id="ac39b-107">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="ac39b-107">Possible Values</span></span>

<span data-ttu-id="ac39b-108">Cet attribut est une **valeur booléenne** spécifiée au moment de la conception et en lecture seule par la suite.</span><span class="sxs-lookup"><span data-stu-id="ac39b-108">This attribute is a **Boolean** specified at design time and read-only thereafter.</span></span>



| <span data-ttu-id="ac39b-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac39b-109">Value</span></span> | <span data-ttu-id="ac39b-110">Description</span><span class="sxs-lookup"><span data-stu-id="ac39b-110">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="ac39b-111">true</span><span class="sxs-lookup"><span data-stu-id="ac39b-111">true</span></span>  | <span data-ttu-id="ac39b-112">Le contrôle vidéo sera sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ac39b-112">Video control will be windowless.</span></span>        |
| <span data-ttu-id="ac39b-113">false</span><span class="sxs-lookup"><span data-stu-id="ac39b-113">false</span></span> | <span data-ttu-id="ac39b-114">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="ac39b-114">Default.</span></span> <span data-ttu-id="ac39b-115">Le contrôle vidéo sera fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ac39b-115">Video control will be windowed.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ac39b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="ac39b-116">Remarks</span></span>

<span data-ttu-id="ac39b-117">Si vous souhaitez une fenêtre vidéo non rectangulaire ou si vous souhaitez couvrir une partie quelconque de la fenêtre vidéo avec une image, cet attribut doit avoir la valeur true.</span><span class="sxs-lookup"><span data-stu-id="ac39b-117">If a non-rectangular video window is desired, or if you want to cover any part of the video window with an image, this attribute must be set to true.</span></span> <span data-ttu-id="ac39b-118">Cela sacrifie certaines performances pour effectuer l’écrêtage nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ac39b-118">This sacrifices some performance to do the necessary clipping.</span></span>

<span data-ttu-id="ac39b-119">La lecture vidéo est optimisée pour la lecture non découpée.</span><span class="sxs-lookup"><span data-stu-id="ac39b-119">Video playback is optimized for unclipped playback.</span></span> <span data-ttu-id="ac39b-120">Dans ce cas, l’attribut **sans fenêtre** est défini sur false et l’intégralité du rectangle vidéo est toujours affichée.</span><span class="sxs-lookup"><span data-stu-id="ac39b-120">In this case, the **windowless** attribute is set to false, and the entire video rectangle is always displayed.</span></span> <span data-ttu-id="ac39b-121">Toute image couvrant la fenêtre vidéo est ignorée et la fenêtre vidéo a l’ordre de plan de niveau le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="ac39b-121">Any image covering the video window is ignored, and the video window has the highest-level z-order.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac39b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac39b-122">Requirements</span></span>



| <span data-ttu-id="ac39b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac39b-123">Requirement</span></span> | <span data-ttu-id="ac39b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac39b-124">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ac39b-125">Version</span><span class="sxs-lookup"><span data-stu-id="ac39b-125">Version</span></span><br/> | <span data-ttu-id="ac39b-126">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="ac39b-126">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ac39b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac39b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac39b-128">**Élément VIDEO**</span><span class="sxs-lookup"><span data-stu-id="ac39b-128">**VIDEO Element**</span></span>](video-element.md)
</dt> </dl>

 

 





