---
title: Indicateurs de stylet
description: Valeurs qui peuvent apparaître dans le champ penFlags de la structure POINTER_PEN_INFO.
ms.assetid: BC3CE568-4090-4451-B780-18530C988305
topic_type:
- apiref
api_name:
- PEN_FLAG_NONE
- PEN_FLAG_BARREL
- PEN_FLAG_INVERTED
- PEN_FLAG_ERASER
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: d7c28beaf58b6fa96bb8dd82b2dd650b2a7d6950
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466130"
---
# <a name="pen-flags"></a><span data-ttu-id="135ca-103">Indicateurs de stylet</span><span class="sxs-lookup"><span data-stu-id="135ca-103">Pen Flags</span></span>

<span data-ttu-id="135ca-104">Valeurs qui peuvent apparaître dans le champ **penFlags** de la structure [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="135ca-104">Values that can appear in the **penFlags** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="135ca-105"><span id="PEN_FLAG_NONE"></span><span id="pen_flag_none"></span>**PEN_FLAG_NONE**</span><span class="sxs-lookup"><span data-stu-id="135ca-105"><span id="PEN_FLAG_NONE"></span><span id="pen_flag_none"></span>**PEN_FLAG_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ca-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="135ca-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="135ca-107">Il n’y a pas d’indicateur de stylet.</span><span class="sxs-lookup"><span data-stu-id="135ca-107">There is no pen flag.</span></span> <span data-ttu-id="135ca-108">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="135ca-108">This is the default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="135ca-109"><span id="PEN_FLAG_BARREL"></span><span id="pen_flag_barrel"></span>**PEN_FLAG_BARREL**</span><span class="sxs-lookup"><span data-stu-id="135ca-109"><span id="PEN_FLAG_BARREL"></span><span id="pen_flag_barrel"></span>**PEN_FLAG_BARREL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ca-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="135ca-110">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="135ca-111">Le bouton en barillet est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="135ca-111">The barrel button is pressed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="135ca-112"><span id="PEN_FLAG_INVERTED"></span><span id="pen_flag_inverted"></span>**PEN_FLAG_INVERTED**</span><span class="sxs-lookup"><span data-stu-id="135ca-112"><span id="PEN_FLAG_INVERTED"></span><span id="pen_flag_inverted"></span>**PEN_FLAG_INVERTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ca-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="135ca-113">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="135ca-114">Le stylet est inversé.</span><span class="sxs-lookup"><span data-stu-id="135ca-114">The pen is inverted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="135ca-115"><span id="PEN_FLAG_ERASER"></span><span id="pen_flag_eraser"></span>**PEN_FLAG_ERASER**</span><span class="sxs-lookup"><span data-stu-id="135ca-115"><span id="PEN_FLAG_ERASER"></span><span id="pen_flag_eraser"></span>**PEN_FLAG_ERASER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ca-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="135ca-116">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="135ca-117">Le bouton gomme est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="135ca-117">The eraser button is pressed.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="135ca-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="135ca-118">Requirements</span></span>



| <span data-ttu-id="135ca-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="135ca-119">Requirement</span></span> | <span data-ttu-id="135ca-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="135ca-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="135ca-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="135ca-121">Minimum supported client</span></span><br/> | <span data-ttu-id="135ca-122">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="135ca-122">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="135ca-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="135ca-123">Minimum supported server</span></span><br/> | <span data-ttu-id="135ca-124">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="135ca-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="135ca-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="135ca-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="135ca-126"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="135ca-126"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="135ca-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="135ca-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="135ca-128">Constantes</span><span class="sxs-lookup"><span data-stu-id="135ca-128">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="135ca-129">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="135ca-129">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





