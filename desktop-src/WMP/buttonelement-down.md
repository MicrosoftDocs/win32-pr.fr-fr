---
title: BUTTONELEMENT. suiv.
description: L’attribut UpDown spécifie ou récupère une valeur indiquant si l’élément Button est à la position haut ou inférieure.
ms.assetid: 6b3633c5-84c1-48a0-bd2f-94660890d9a6
keywords:
- BUTTONELEMENT. baisse du lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTONELEMENT.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23f48b0e2ac0f4bf02f87d90bb0bd504478beb52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545522"
---
# <a name="buttonelementdown"></a><span data-ttu-id="d9925-104">BUTTONELEMENT. suiv.</span><span class="sxs-lookup"><span data-stu-id="d9925-104">BUTTONELEMENT.down</span></span>

<span data-ttu-id="d9925-105">L’attribut **UpDown** spécifie ou récupère une valeur indiquant si l’élément Button est à la position haut ou inférieure.</span><span class="sxs-lookup"><span data-stu-id="d9925-105">The **down** attribute specifies or retrieves a value indicating whether the button element is in the up or down position.</span></span>

``` syntax
        elementID.down
```

## <a name="possible-values"></a><span data-ttu-id="d9925-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="d9925-106">Possible Values</span></span>

<span data-ttu-id="d9925-107">Cet attribut est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d9925-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="d9925-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9925-108">Value</span></span> | <span data-ttu-id="d9925-109">Description</span><span class="sxs-lookup"><span data-stu-id="d9925-109">Description</span></span>                                                     |
|-------|-----------------------------------------------------------------|
| <span data-ttu-id="d9925-110">true</span><span class="sxs-lookup"><span data-stu-id="d9925-110">true</span></span>  | <span data-ttu-id="d9925-111">Indique que le **BUTTONELEMENT** est en position inférieure.</span><span class="sxs-lookup"><span data-stu-id="d9925-111">Indicates the **BUTTONELEMENT** is in the down position.</span></span>        |
| <span data-ttu-id="d9925-112">false</span><span class="sxs-lookup"><span data-stu-id="d9925-112">false</span></span> | <span data-ttu-id="d9925-113">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="d9925-113">Default.</span></span> <span data-ttu-id="d9925-114">Indique que le **BUTTONELEMENT** est en position de haut.</span><span class="sxs-lookup"><span data-stu-id="d9925-114">Indicates the **BUTTONELEMENT** is in the up position.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d9925-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d9925-115">Remarks</span></span>

<span data-ttu-id="d9925-116">Pour qu’un élément Button reste à la position inférieure, la fonction **rémanente** doit avoir la valeur true.</span><span class="sxs-lookup"><span data-stu-id="d9925-116">For a button element to remain in the down position, **sticky** must be set to true.</span></span> <span data-ttu-id="d9925-117">Par défaut, l’option **rémanent** a la valeur false et toute tentative de définition de **la** valeur true sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="d9925-117">By default, **sticky** is false, and any attempt to set **down** to true will be ignored.</span></span>

<span data-ttu-id="d9925-118">Si une valeur non valide est spécifiée, l’état précédent est conservé.</span><span class="sxs-lookup"><span data-stu-id="d9925-118">If an invalid value is specified, the previous state is maintained.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9925-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9925-119">Requirements</span></span>



| <span data-ttu-id="d9925-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9925-120">Requirement</span></span> | <span data-ttu-id="d9925-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9925-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d9925-122">Version</span><span class="sxs-lookup"><span data-stu-id="d9925-122">Version</span></span><br/> | <span data-ttu-id="d9925-123">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="d9925-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d9925-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9925-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9925-125">**Élément BUTTONELEMENT**</span><span class="sxs-lookup"><span data-stu-id="d9925-125">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> <dt>

[<span data-ttu-id="d9925-126">**BUTTONELEMENT. downToolTip**</span><span class="sxs-lookup"><span data-stu-id="d9925-126">**BUTTONELEMENT.downToolTip**</span></span>](buttonelement-downtooltip.md)
</dt> </dl>

 

 





