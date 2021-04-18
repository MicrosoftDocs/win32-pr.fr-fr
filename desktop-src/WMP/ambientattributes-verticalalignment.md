---
title: AmbientAttributes. verticalAlignment
description: L’attribut verticalAlignment spécifie ou récupère une valeur indiquant le positionnement vertical du contrôle lorsque la vue ou la sous-vue parente est étirée.
ms.assetid: 08ef483a-58ee-4a35-9973-2567076d07f7
keywords:
- Lecteur Windows Media AmbientAttributes. verticalAlignment
topic_type:
- apiref
api_name:
- AmbientAttributes.verticalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88de2f5f54b95b14827fabb2bafb89ff6974966b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540652"
---
# <a name="ambientattributesverticalalignment"></a><span data-ttu-id="ce6f6-104">AmbientAttributes. verticalAlignment</span><span class="sxs-lookup"><span data-stu-id="ce6f6-104">AmbientAttributes.verticalAlignment</span></span>

<span data-ttu-id="ce6f6-105">L’attribut **VerticalAlignment** spécifie ou récupère une valeur indiquant le positionnement vertical du contrôle lorsque la **vue** ou la sous- **vue** parente est étirée.</span><span class="sxs-lookup"><span data-stu-id="ce6f6-105">The **verticalAlignment** attribute specifies or retrieves a value indicating the vertical placement of the control when the **VIEW** or parent **SUBVIEW** is stretched.</span></span>

``` syntax
        elementID.verticalAlignment
```

## <a name="possible-values"></a><span data-ttu-id="ce6f6-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="ce6f6-106">Possible Values</span></span>

<span data-ttu-id="ce6f6-107">Cet attribut est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ce6f6-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="ce6f6-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce6f6-108">Value</span></span>   | <span data-ttu-id="ce6f6-109">Description</span><span class="sxs-lookup"><span data-stu-id="ce6f6-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce6f6-110">top</span><span class="sxs-lookup"><span data-stu-id="ce6f6-110">top</span></span>     | <span data-ttu-id="ce6f6-111">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="ce6f6-111">Default.</span></span> <span data-ttu-id="ce6f6-112">Maintient le positionnement du contrôle par rapport au haut de la **vue** ou de la sous- **vue** parente lorsque la vue est redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="ce6f6-112">Maintains the placement of the control relative to the top of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="ce6f6-113">bottom</span><span class="sxs-lookup"><span data-stu-id="ce6f6-113">bottom</span></span>  | <span data-ttu-id="ce6f6-114">Maintient le positionnement du contrôle par rapport au bas de la **vue** ou de la sous- **vue** parente lorsque la vue est redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="ce6f6-114">Maintains the placement of the control relative to the bottom of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="ce6f6-115">centre</span><span class="sxs-lookup"><span data-stu-id="ce6f6-115">center</span></span>  | <span data-ttu-id="ce6f6-116">Maintient le positionnement du contrôle par rapport au centre vertical de la **vue** ou de la sous- **vue** parente lorsque la vue est redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="ce6f6-116">Maintains the placement of the control relative to the vertical center of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="ce6f6-117">étirement</span><span class="sxs-lookup"><span data-stu-id="ce6f6-117">stretch</span></span> | <span data-ttu-id="ce6f6-118">Maintient la position du contrôle par rapport aux marges supérieure et inférieure de la vue lors du redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="ce6f6-118">Maintains the placement of the control relative to both the top and bottom margins of the View when resized.</span></span> <span data-ttu-id="ce6f6-119">Le contrôle s’étire pour s’ajuster lorsque la **vue** ou la sous- **vue** parente est étirée.</span><span class="sxs-lookup"><span data-stu-id="ce6f6-119">The control stretches to fit when the **VIEW** or parent **SUBVIEW** is stretched.</span></span> <span data-ttu-id="ce6f6-120">L’image réelle n’est pas agrandie ou réduite, à moins qu’elle ne soit redimensionnable, mais la zone cliquable augmente ou diminue si elle n’est pas limitée par un **clippingImage**.</span><span class="sxs-lookup"><span data-stu-id="ce6f6-120">The actual image does not grow or shrink unless it is resizable, but the clickable area grows or shrinks if not bounded by a **clippingImage**.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ce6f6-121">Notes</span><span class="sxs-lookup"><span data-stu-id="ce6f6-121">Remarks</span></span>

<span data-ttu-id="ce6f6-122">À moins que **VerticalAlignment** ne soit défini sur « Center », le contrôle conserve sa distance d’origine à partir du bord spécifié, ou à partir des deux bords si « Stretch » est spécifié et que le contrôle est redimensionnable.</span><span class="sxs-lookup"><span data-stu-id="ce6f6-122">Unless **verticalAlignment** is set to "center", the control retains its original distance from the specified edge, or from both edges if "stretch" is specified and the control is resizable.</span></span> <span data-ttu-id="ce6f6-123">Si le contrôle n’est pas redimensionnable et que « Stretch » est spécifié, la zone cliquable est étirée à la place.</span><span class="sxs-lookup"><span data-stu-id="ce6f6-123">If the control is not resizable and "stretch" is specified, the clickable region is stretched instead.</span></span>

<span data-ttu-id="ce6f6-124">Vous pouvez définir n’importe quelle combinaison d’attributs **HorizontalAlignment** et **VerticalAlignment** .</span><span class="sxs-lookup"><span data-stu-id="ce6f6-124">You can set any combination of the **horizontalAlignment** and **verticalAlignment** attributes.</span></span> <span data-ttu-id="ce6f6-125">Par exemple, si vous souhaitez qu’un contrôle soit centré à la fois horizontalement et verticalement, définissez **HorizontalAlignment** sur « Center » et **VerticalAlignment** sur « Center ».</span><span class="sxs-lookup"><span data-stu-id="ce6f6-125">For example, if you want a control to be centered both horizontally and vertically, set **horizontalAlignment** to "center" and **verticalAlignment** to "center".</span></span>

## <a name="requirements"></a><span data-ttu-id="ce6f6-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce6f6-126">Requirements</span></span>



| <span data-ttu-id="ce6f6-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce6f6-127">Requirement</span></span> | <span data-ttu-id="ce6f6-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce6f6-128">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ce6f6-129">Version</span><span class="sxs-lookup"><span data-stu-id="ce6f6-129">Version</span></span><br/> | <span data-ttu-id="ce6f6-130">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="ce6f6-130">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ce6f6-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce6f6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce6f6-132">**Attributs ambiants**</span><span class="sxs-lookup"><span data-stu-id="ce6f6-132">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="ce6f6-133">**AmbientAttributes. horizontalAlignment**</span><span class="sxs-lookup"><span data-stu-id="ce6f6-133">**AmbientAttributes.horizontalAlignment**</span></span>](ambientattributes-horizontalalignment.md)
</dt> </dl>

 

 





