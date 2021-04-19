---
title: BUTTONGROUP. showBackground
description: L’attribut showBackground spécifie ou récupère une valeur indiquant si le BUTTONGROUP affiche uniquement les boutons, ou affiche la bitmap complète spécifiée dans l’attribut image.
ms.assetid: 5c3fc873-937c-4dad-ac18-e7a37004ee1e
keywords:
- Lecteur Windows Media BUTTONGROUP. showBackground
topic_type:
- apiref
api_name:
- BUTTONGROUP.showBackground
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31cc87260d4b0fca74d6063c757e6c3dae0db850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523952"
---
# <a name="buttongroupshowbackground"></a><span data-ttu-id="28d04-104">BUTTONGROUP. showBackground</span><span class="sxs-lookup"><span data-stu-id="28d04-104">BUTTONGROUP.showBackground</span></span>

<span data-ttu-id="28d04-105">L’attribut **showBackground** spécifie ou récupère une valeur indiquant si le **BUTTONGROUP** affiche uniquement les boutons, ou affiche la bitmap complète spécifiée dans l’attribut **image** .</span><span class="sxs-lookup"><span data-stu-id="28d04-105">The **showBackground** attribute specifies or retrieves a value indicating whether the **BUTTONGROUP** displays only the buttons, or displays the full bitmap specified in the **image** attribute.</span></span>

``` syntax
        elementID.showBackground
```

## <a name="possible-values"></a><span data-ttu-id="28d04-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="28d04-106">Possible Values</span></span>

<span data-ttu-id="28d04-107">Cet attribut est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="28d04-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="28d04-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="28d04-108">Value</span></span> | <span data-ttu-id="28d04-109">Description</span><span class="sxs-lookup"><span data-stu-id="28d04-109">Description</span></span>                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="28d04-110">true</span><span class="sxs-lookup"><span data-stu-id="28d04-110">true</span></span>  | <span data-ttu-id="28d04-111">Les boutons s’affichent et la zone non occupée par les boutons est dessinée à partir de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="28d04-111">Buttons are displayed and the area not occupied by buttons is drawn from the Image bitmap.</span></span> |
| <span data-ttu-id="28d04-112">false</span><span class="sxs-lookup"><span data-stu-id="28d04-112">false</span></span> | <span data-ttu-id="28d04-113">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="28d04-113">Default.</span></span> <span data-ttu-id="28d04-114">Seuls les boutons s’affichent.</span><span class="sxs-lookup"><span data-stu-id="28d04-114">Only the buttons are displayed.</span></span>                                                   |



 

## <a name="remarks"></a><span data-ttu-id="28d04-115">Notes</span><span class="sxs-lookup"><span data-stu-id="28d04-115">Remarks</span></span>

<span data-ttu-id="28d04-116">Quand **showBackground** a la valeur true, la totalité de l' **image** principale est visible.</span><span class="sxs-lookup"><span data-stu-id="28d04-116">When **showBackground** is true, the entire main **image** will be visible.</span></span>

<span data-ttu-id="28d04-117">Quand **showBackground** a la valeur false, seules les zones correspondant aux couleurs **mappingImage** affectées seront rendues.</span><span class="sxs-lookup"><span data-stu-id="28d04-117">When **showBackground** is false, only the areas corresponding to assigned **mappingImage** colors will be rendered.</span></span> <span data-ttu-id="28d04-118">En d’autres termes, seuls les **BUTTONELEMENTs** avec le **mappingColor** affecté sont visibles.</span><span class="sxs-lookup"><span data-stu-id="28d04-118">In other words, only **BUTTONELEMENTs** with their **mappingColor** assigned will be visible.</span></span>

<span data-ttu-id="28d04-119">Si une valeur non valide est spécifiée, l’état précédent est conservé.</span><span class="sxs-lookup"><span data-stu-id="28d04-119">If an invalid value is specified, the previous state is maintained.</span></span>

## <a name="requirements"></a><span data-ttu-id="28d04-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28d04-120">Requirements</span></span>



| <span data-ttu-id="28d04-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28d04-121">Requirement</span></span> | <span data-ttu-id="28d04-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="28d04-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="28d04-123">Version</span><span class="sxs-lookup"><span data-stu-id="28d04-123">Version</span></span><br/> | <span data-ttu-id="28d04-124">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="28d04-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="28d04-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28d04-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28d04-126">**Élément BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="28d04-126">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="28d04-127">**BUTTONELEMENT. mappingColor**</span><span class="sxs-lookup"><span data-stu-id="28d04-127">**BUTTONELEMENT.mappingColor**</span></span>](buttonelement-mappingcolor.md)
</dt> <dt>

[<span data-ttu-id="28d04-128">**BUTTONGROUP. image**</span><span class="sxs-lookup"><span data-stu-id="28d04-128">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="28d04-129">**BUTTONGROUP. mappingImage**</span><span class="sxs-lookup"><span data-stu-id="28d04-129">**BUTTONGROUP.mappingImage**</span></span>](buttongroup-mappingimage.md)
</dt> </dl>

 

 





