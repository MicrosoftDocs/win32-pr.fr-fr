---
title: BUTTONELEMENT. collant
description: L’attribut rémanent spécifie ou récupère une valeur indiquant si le BUTTONELEMENT est un bouton bascule, c’est-à-dire s’il s’agit d’un bouton à deux États ou un seul État.
ms.assetid: a7e74f70-9fa6-45a1-ab65-2db107e13551
keywords:
- BUTTONELEMENT. collant le lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTONELEMENT.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 713b26fdee3062fbe803d05e034bc9896cdd5563
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541343"
---
# <a name="buttonelementsticky"></a><span data-ttu-id="55cbf-104">BUTTONELEMENT. collant</span><span class="sxs-lookup"><span data-stu-id="55cbf-104">BUTTONELEMENT.sticky</span></span>

<span data-ttu-id="55cbf-105">L’attribut **rémanent** spécifie ou récupère une valeur indiquant si le **BUTTONELEMENT** est un bouton bascule, c’est-à-dire s’il s’agit d’un bouton à deux États ou un seul État.</span><span class="sxs-lookup"><span data-stu-id="55cbf-105">The **sticky** attribute specifies or retrieves a value indicating whether the **BUTTONELEMENT** is a toggle, that is, whether it is a two-state or single-state button.</span></span>

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a><span data-ttu-id="55cbf-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="55cbf-106">Possible Values</span></span>

<span data-ttu-id="55cbf-107">Cet attribut est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="55cbf-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="55cbf-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="55cbf-108">Value</span></span> | <span data-ttu-id="55cbf-109">Description</span><span class="sxs-lookup"><span data-stu-id="55cbf-109">Description</span></span>                               |
|-------|-------------------------------------------|
| <span data-ttu-id="55cbf-110">true</span><span class="sxs-lookup"><span data-stu-id="55cbf-110">true</span></span>  | <span data-ttu-id="55cbf-111">**BUTTONELEMENT** est rémanente.</span><span class="sxs-lookup"><span data-stu-id="55cbf-111">**BUTTONELEMENT** is sticky.</span></span>              |
| <span data-ttu-id="55cbf-112">false</span><span class="sxs-lookup"><span data-stu-id="55cbf-112">false</span></span> | <span data-ttu-id="55cbf-113">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="55cbf-113">Default.</span></span> <span data-ttu-id="55cbf-114">**BUTTONELEMENT** n’est pas rémanent.</span><span class="sxs-lookup"><span data-stu-id="55cbf-114">**BUTTONELEMENT** is not sticky.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="55cbf-115">Notes</span><span class="sxs-lookup"><span data-stu-id="55cbf-115">Remarks</span></span>

<span data-ttu-id="55cbf-116">Si l’attribut **rémanent** a la valeur true, l’élément Button passe à l’état inactif lorsque vous cliquez dessus et reste dans cet État jusqu’à ce que l’utilisateur clique à nouveau dessus.</span><span class="sxs-lookup"><span data-stu-id="55cbf-116">If the **sticky** attribute is set to true, the button element will change to the down state when clicked and will remain in that state until clicked again.</span></span> <span data-ttu-id="55cbf-117">Lorsque l’élément Button est dans l’état inactif, l’attribut **UpDown** a la valeur true et la partie appropriée du groupe de boutons **downImage** est affichée.</span><span class="sxs-lookup"><span data-stu-id="55cbf-117">When the button element is in the down state, the **down** attribute will be true and the appropriate portion of the button group **downImage** will be displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="55cbf-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55cbf-118">Requirements</span></span>



| <span data-ttu-id="55cbf-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55cbf-119">Requirement</span></span> | <span data-ttu-id="55cbf-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="55cbf-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="55cbf-121">Version</span><span class="sxs-lookup"><span data-stu-id="55cbf-121">Version</span></span><br/> | <span data-ttu-id="55cbf-122">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="55cbf-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55cbf-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55cbf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55cbf-124">**Élément BUTTONELEMENT**</span><span class="sxs-lookup"><span data-stu-id="55cbf-124">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> <dt>

[<span data-ttu-id="55cbf-125">**BUTTONELEMENT. suiv.**</span><span class="sxs-lookup"><span data-stu-id="55cbf-125">**BUTTONELEMENT.down**</span></span>](buttonelement-down.md)
</dt> <dt>

[<span data-ttu-id="55cbf-126">**BUTTONGROUP. downImage**</span><span class="sxs-lookup"><span data-stu-id="55cbf-126">**BUTTONGROUP.downImage**</span></span>](buttongroup-downimage.md)
</dt> </dl>

 

 





