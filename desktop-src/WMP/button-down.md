---
title: BUTTON. suiv.
description: L’attribut UpDown spécifie ou récupère une valeur indiquant si le bouton se trouve à la position haut ou inférieure.
ms.assetid: 75398e8c-b13e-4836-b487-ed880da753ea
keywords:
- BUTTON. vers le lecteur Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a0e2c7f97f782b51c145f3974f1490d0286fbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539699"
---
# <a name="buttondown"></a><span data-ttu-id="29aef-104">BUTTON. suiv.</span><span class="sxs-lookup"><span data-stu-id="29aef-104">BUTTON.down</span></span>

<span data-ttu-id="29aef-105">L’attribut **UpDown** spécifie ou récupère une valeur indiquant si le **bouton** se trouve à la position haut ou inférieure.</span><span class="sxs-lookup"><span data-stu-id="29aef-105">The **down** attribute specifies or retrieves a value indicating whether the **BUTTON** is in the up or down position.</span></span>

``` syntax
        elementID.down
```

## <a name="possible-values"></a><span data-ttu-id="29aef-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="29aef-106">Possible Values</span></span>

<span data-ttu-id="29aef-107">Cet attribut est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="29aef-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="29aef-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="29aef-108">Value</span></span> | <span data-ttu-id="29aef-109">Description</span><span class="sxs-lookup"><span data-stu-id="29aef-109">Description</span></span>                                                   |
|-------|---------------------------------------------------------------|
| <span data-ttu-id="29aef-110">true</span><span class="sxs-lookup"><span data-stu-id="29aef-110">true</span></span>  | <span data-ttu-id="29aef-111">Indique que le **bouton** est en position inférieure.</span><span class="sxs-lookup"><span data-stu-id="29aef-111">Indicates that the **BUTTON** is in the down position.</span></span>        |
| <span data-ttu-id="29aef-112">false</span><span class="sxs-lookup"><span data-stu-id="29aef-112">false</span></span> | <span data-ttu-id="29aef-113">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="29aef-113">Default.</span></span> <span data-ttu-id="29aef-114">Indique que le **bouton** se trouve à la position de haut.</span><span class="sxs-lookup"><span data-stu-id="29aef-114">Indicates that the **BUTTON** is in the up position.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="29aef-115">Notes</span><span class="sxs-lookup"><span data-stu-id="29aef-115">Remarks</span></span>

<span data-ttu-id="29aef-116">Pour qu’un **bouton** reste à la position inférieure, l’option **rémanent** doit avoir la valeur true.</span><span class="sxs-lookup"><span data-stu-id="29aef-116">For a **BUTTON** to remain in the down position, **sticky** must be set to true.</span></span> <span data-ttu-id="29aef-117">Par défaut, l’option **rémanent** a la valeur false et toute tentative de définition de **la** valeur true sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="29aef-117">By default, **sticky** is false, and any attempt to set **down** to true will be ignored.</span></span>

<span data-ttu-id="29aef-118">Si une valeur non valide est spécifiée, l’état précédent est conservé.</span><span class="sxs-lookup"><span data-stu-id="29aef-118">If an invalid value is specified, the previous state is maintained.</span></span>

## <a name="requirements"></a><span data-ttu-id="29aef-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29aef-119">Requirements</span></span>



| <span data-ttu-id="29aef-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29aef-120">Requirement</span></span> | <span data-ttu-id="29aef-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="29aef-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="29aef-122">Version</span><span class="sxs-lookup"><span data-stu-id="29aef-122">Version</span></span><br/> | <span data-ttu-id="29aef-123">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="29aef-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="29aef-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29aef-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29aef-125">**BUTTON, élément**</span><span class="sxs-lookup"><span data-stu-id="29aef-125">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="29aef-126">**BUTTON. downImage**</span><span class="sxs-lookup"><span data-stu-id="29aef-126">**BUTTON.downImage**</span></span>](button-downimage.md)
</dt> <dt>

[<span data-ttu-id="29aef-127">**BUTTON. downToolTip**</span><span class="sxs-lookup"><span data-stu-id="29aef-127">**BUTTON.downToolTip**</span></span>](button-downtooltip.md)
</dt> </dl>

 

 





