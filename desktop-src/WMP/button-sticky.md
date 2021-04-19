---
title: BUTTON. rémanent
description: L’attribut rémanent spécifie ou récupère une valeur indiquant si le bouton est un bouton bascule, c’est-à-dire s’il s’agit d’un bouton à deux États ou un seul État.
ms.assetid: aa0b48b4-29ce-440c-aeb9-dce31ab3cb63
keywords:
- BUTTON. collant le lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTON.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8de9b4e1a8e4bab04e5729cb45662164e2dfa2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528017"
---
# <a name="buttonsticky"></a><span data-ttu-id="083f3-104">BUTTON. rémanent</span><span class="sxs-lookup"><span data-stu-id="083f3-104">BUTTON.sticky</span></span>

<span data-ttu-id="083f3-105">L’attribut **rémanent** spécifie ou récupère une valeur indiquant si le **bouton** est un bouton bascule, c’est-à-dire s’il s’agit d’un **bouton** à deux États ou un seul État.</span><span class="sxs-lookup"><span data-stu-id="083f3-105">The **sticky** attribute specifies or retrieves a value indicating whether the **BUTTON** is a toggle, that is, whether it is a two-state or single-state **BUTTON**.</span></span>

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a><span data-ttu-id="083f3-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="083f3-106">Possible Values</span></span>

<span data-ttu-id="083f3-107">Cet attribut est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="083f3-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="083f3-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="083f3-108">Value</span></span> | <span data-ttu-id="083f3-109">Description</span><span class="sxs-lookup"><span data-stu-id="083f3-109">Description</span></span>                        |
|-------|------------------------------------|
| <span data-ttu-id="083f3-110">true</span><span class="sxs-lookup"><span data-stu-id="083f3-110">true</span></span>  | <span data-ttu-id="083f3-111">Le **bouton** est rémanent.</span><span class="sxs-lookup"><span data-stu-id="083f3-111">**BUTTON** is sticky.</span></span>              |
| <span data-ttu-id="083f3-112">false</span><span class="sxs-lookup"><span data-stu-id="083f3-112">false</span></span> | <span data-ttu-id="083f3-113">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="083f3-113">Default.</span></span> <span data-ttu-id="083f3-114">Le **bouton** n’est pas rémanent.</span><span class="sxs-lookup"><span data-stu-id="083f3-114">**BUTTON** is not sticky.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="083f3-115">Notes</span><span class="sxs-lookup"><span data-stu-id="083f3-115">Remarks</span></span>

<span data-ttu-id="083f3-116">Si le **pense-bête** est défini sur true, le **bouton** passe à l’état inactif lorsque vous cliquez dessus et reste dans cet État jusqu’à ce que l’utilisateur clique à nouveau dessus.</span><span class="sxs-lookup"><span data-stu-id="083f3-116">If **sticky** is set to true, the **BUTTON** will change to the down state when clicked and will remain in that state until clicked again.</span></span> <span data-ttu-id="083f3-117">Quand le **bouton** est à l’état inactif, l’attribut **enfoncé** a la valeur true et le **downImage** est affiché.</span><span class="sxs-lookup"><span data-stu-id="083f3-117">When the **BUTTON** is in the down state, the **down** attribute will be true and the **downImage** will be displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="083f3-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="083f3-118">Requirements</span></span>



| <span data-ttu-id="083f3-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="083f3-119">Requirement</span></span> | <span data-ttu-id="083f3-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="083f3-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="083f3-121">Version</span><span class="sxs-lookup"><span data-stu-id="083f3-121">Version</span></span><br/> | <span data-ttu-id="083f3-122">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="083f3-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="083f3-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="083f3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="083f3-124">**BUTTON, élément**</span><span class="sxs-lookup"><span data-stu-id="083f3-124">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="083f3-125">**BUTTON. suiv.**</span><span class="sxs-lookup"><span data-stu-id="083f3-125">**BUTTON.down**</span></span>](button-down.md)
</dt> <dt>

[<span data-ttu-id="083f3-126">**BUTTON. downImage**</span><span class="sxs-lookup"><span data-stu-id="083f3-126">**BUTTON.downImage**</span></span>](button-downimage.md)
</dt> </dl>

 

 





