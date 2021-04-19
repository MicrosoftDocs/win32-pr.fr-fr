---
title: BUTTONGROUP. radio
description: L’attribut radio spécifie ou récupère une valeur indiquant si le BUTTONGROUP est composé de cases d’option.
ms.assetid: f84479f8-af4f-4ca8-991e-1c2ab39d7110
keywords:
- BUTTONGROUP. radio Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.radio
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1765a7756aedcebc2b7b030634d8598a5cd89e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539964"
---
# <a name="buttongroupradio"></a><span data-ttu-id="912f3-104">BUTTONGROUP. radio</span><span class="sxs-lookup"><span data-stu-id="912f3-104">BUTTONGROUP.radio</span></span>

<span data-ttu-id="912f3-105">L’attribut **radio** spécifie ou récupère une valeur indiquant si le **BUTTONGROUP** est composé de cases d’option.</span><span class="sxs-lookup"><span data-stu-id="912f3-105">The **radio** attribute specifies or retrieves a value indicating whether the **BUTTONGROUP** is composed of radio buttons.</span></span>

``` syntax
        elementID.radio
```

## <a name="possible-values"></a><span data-ttu-id="912f3-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="912f3-106">Possible Values</span></span>

<span data-ttu-id="912f3-107">Cet attribut est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="912f3-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="912f3-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="912f3-108">Value</span></span> | <span data-ttu-id="912f3-109">Description</span><span class="sxs-lookup"><span data-stu-id="912f3-109">Description</span></span>                                      |
|-------|--------------------------------------------------|
| <span data-ttu-id="912f3-110">true</span><span class="sxs-lookup"><span data-stu-id="912f3-110">true</span></span>  | <span data-ttu-id="912f3-111">Le **BUTTONGROUP** est de type radio.</span><span class="sxs-lookup"><span data-stu-id="912f3-111">The **BUTTONGROUP** is radio style.</span></span>              |
| <span data-ttu-id="912f3-112">false</span><span class="sxs-lookup"><span data-stu-id="912f3-112">false</span></span> | <span data-ttu-id="912f3-113">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="912f3-113">Default.</span></span> <span data-ttu-id="912f3-114">**BUTTONGROUP** n’est pas de type radio.</span><span class="sxs-lookup"><span data-stu-id="912f3-114">The **BUTTONGROUP** is not radio style.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="912f3-115">Notes</span><span class="sxs-lookup"><span data-stu-id="912f3-115">Remarks</span></span>

<span data-ttu-id="912f3-116">Si **radio** a la valeur true, tous les éléments **BUTTONELEMENT** dans le **BUTTONGROUP** seront rémanents, mais un seul bouton à la fois sera à l’état inactif.</span><span class="sxs-lookup"><span data-stu-id="912f3-116">If **radio** is set to true, all the **BUTTONELEMENT** elements in the **BUTTONGROUP** will be sticky, but only one button at a time will be in the down state.</span></span>

## <a name="requirements"></a><span data-ttu-id="912f3-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="912f3-117">Requirements</span></span>



| <span data-ttu-id="912f3-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="912f3-118">Requirement</span></span> | <span data-ttu-id="912f3-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="912f3-119">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="912f3-120">Version</span><span class="sxs-lookup"><span data-stu-id="912f3-120">Version</span></span><br/> | <span data-ttu-id="912f3-121">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="912f3-121">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="912f3-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="912f3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="912f3-123">**BUTTONELEMENT. collant**</span><span class="sxs-lookup"><span data-stu-id="912f3-123">**BUTTONELEMENT.sticky**</span></span>](buttonelement-sticky.md)
</dt> <dt>

[<span data-ttu-id="912f3-124">**Élément BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="912f3-124">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> </dl>

 

 





