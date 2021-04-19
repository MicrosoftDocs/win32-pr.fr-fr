---
title: AmbientAttributes. horizontalAlignment
description: L’attribut horizontalAlignment spécifie ou récupère une valeur qui indique le positionnement horizontal du contrôle lorsque la vue ou la sous-vue parente est redimensionnée.
ms.assetid: 97ca23b9-2046-45ee-b2da-ea388e7ab8d8
keywords:
- Lecteur Windows Media AmbientAttributes. horizontalAlignment
topic_type:
- apiref
api_name:
- AmbientAttributes.horizontalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f946f0d095526c9fc0894cdf0270cbf7cc0c81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537330"
---
# <a name="ambientattributeshorizontalalignment"></a><span data-ttu-id="9ce14-104">AmbientAttributes. horizontalAlignment</span><span class="sxs-lookup"><span data-stu-id="9ce14-104">AmbientAttributes.horizontalAlignment</span></span>

<span data-ttu-id="9ce14-105">L’attribut **HorizontalAlignment** spécifie ou récupère une valeur qui indique le positionnement horizontal du contrôle lorsque la **vue** ou la sous- **vue** parente est redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="9ce14-105">The **horizontalAlignment** attribute specifies or retrieves a value that indicates the horizontal placement of the control when the **VIEW** or parent **SUBVIEW** is resized.</span></span>

``` syntax
        elementID.horizontalAlignment
```

## <a name="possible-values"></a><span data-ttu-id="9ce14-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="9ce14-106">Possible Values</span></span>

<span data-ttu-id="9ce14-107">Cet attribut est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9ce14-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="9ce14-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ce14-108">Value</span></span>   | <span data-ttu-id="9ce14-109">Description</span><span class="sxs-lookup"><span data-stu-id="9ce14-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ce14-110">gauche</span><span class="sxs-lookup"><span data-stu-id="9ce14-110">left</span></span>    | <span data-ttu-id="9ce14-111">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="9ce14-111">Default.</span></span> <span data-ttu-id="9ce14-112">Maintient le positionnement du contrôle par rapport à la gauche de la **vue** ou de la sous- **vue** parente lorsque la vue est redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="9ce14-112">Maintains the placement of the control relative to the left of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="9ce14-113">droite</span><span class="sxs-lookup"><span data-stu-id="9ce14-113">right</span></span>   | <span data-ttu-id="9ce14-114">Maintient le positionnement du contrôle par rapport à la droite de la **vue** ou de la sous- **vue** parente lorsque la vue est redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="9ce14-114">Maintains the placement of the control relative to the right of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="9ce14-115">centre</span><span class="sxs-lookup"><span data-stu-id="9ce14-115">center</span></span>  | <span data-ttu-id="9ce14-116">Maintient le positionnement du contrôle par rapport au centre horizontal de la **vue** ou de la sous- **vue** parente lorsque la vue est redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="9ce14-116">Maintains the placement of the control relative to the horizontal center of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="9ce14-117">étirement</span><span class="sxs-lookup"><span data-stu-id="9ce14-117">stretch</span></span> | <span data-ttu-id="9ce14-118">Maintient le positionnement du contrôle par rapport aux marges gauche et droite de la **vue** ou de la sous- **vue** parente lors du redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="9ce14-118">Maintains the placement of the control relative to both the left and right margins of the **VIEW** or parent **SUBVIEW** when resized.</span></span> <span data-ttu-id="9ce14-119">Le contrôle s’étire pour s’ajuster lorsque la **vue** ou la sous- **vue** est étirée.</span><span class="sxs-lookup"><span data-stu-id="9ce14-119">The control stretches to fit when the **VIEW** or **SUBVIEW** is stretched.</span></span> <span data-ttu-id="9ce14-120">L’image réelle n’est pas agrandie ou réduite, à moins qu’elle ne soit redimensionnable, mais la zone cliquable augmente ou diminue si elle n’est pas limitée par un **clippingImage**.</span><span class="sxs-lookup"><span data-stu-id="9ce14-120">The actual image does not grow or shrink unless it is resizable, but the clickable area grows or shrinks if not bounded by a **clippingImage**.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9ce14-121">Notes</span><span class="sxs-lookup"><span data-stu-id="9ce14-121">Remarks</span></span>

<span data-ttu-id="9ce14-122">Sauf si **HorizontalAlignment** est défini sur « Center », le contrôle conserve sa distance d’origine à partir du bord spécifié, ou des deux bords si « Stretch » est spécifié et que le contrôle est redimensionnable.</span><span class="sxs-lookup"><span data-stu-id="9ce14-122">Unless **horizontalAlignment** is set to "center", the control retains its original distance from the specified edge, or from both edges if "stretch" is specified and the control is resizable.</span></span> <span data-ttu-id="9ce14-123">Si le contrôle n’est pas redimensionnable et que « Stretch » est spécifié, la zone cliquable est étirée à la place.</span><span class="sxs-lookup"><span data-stu-id="9ce14-123">If the control is not resizable and "stretch" is specified, the clickable region is stretched instead.</span></span>

<span data-ttu-id="9ce14-124">Vous pouvez définir n’importe quelle combinaison de **HorizontalAlignment** et **VerticalAlignment**.</span><span class="sxs-lookup"><span data-stu-id="9ce14-124">You can set any combination of **horizontalAlignment** and **verticalAlignment**.</span></span> <span data-ttu-id="9ce14-125">Par exemple, si vous souhaitez centrer un contrôle à la fois horizontalement et verticalement, définissez horizontalAlignment = "Center" verticalAlignment = "Center".</span><span class="sxs-lookup"><span data-stu-id="9ce14-125">For example, if you want to center a control both horizontally and vertically, set horizontalAlignment="center" verticalAlignment="center".</span></span>

## <a name="requirements"></a><span data-ttu-id="9ce14-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ce14-126">Requirements</span></span>



| <span data-ttu-id="9ce14-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ce14-127">Requirement</span></span> | <span data-ttu-id="9ce14-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ce14-128">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="9ce14-129">Version</span><span class="sxs-lookup"><span data-stu-id="9ce14-129">Version</span></span><br/> | <span data-ttu-id="9ce14-130">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="9ce14-130">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9ce14-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ce14-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ce14-132">**Attributs ambiants**</span><span class="sxs-lookup"><span data-stu-id="9ce14-132">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="9ce14-133">**AmbientAttributes. verticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="9ce14-133">**AmbientAttributes.verticalAlignment**</span></span>](ambientattributes-verticalalignment.md)
</dt> <dt>

[<span data-ttu-id="9ce14-134">**AmbientAttributes.clippingImage**</span><span class="sxs-lookup"><span data-stu-id="9ce14-134">**AmbientAttributes.clippingImage**</span></span>](ambientattributes-clippingimage.md)
</dt> </dl>

 

 





