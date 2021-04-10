---
title: Message LVM_HITTEST (commctrl. h)
description: Détermine l’élément de la vue de liste, le cas échéant, à une position spécifiée. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView HitTest.
ms.assetid: 81df4ed1-30bd-4b63-9cb9-5163cb7cf52c
keywords:
- LVM_HITTEST les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb770c8f5a47f1dcbbf23a11443afa581aea2e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942643"
---
# <a name="lvm_hittest-message"></a><span data-ttu-id="e74a9-105">Message LVM LVM \_</span><span class="sxs-lookup"><span data-stu-id="e74a9-105">LVM\_HITTEST message</span></span>

<span data-ttu-id="e74a9-106">Détermine l’élément de la vue de liste, le cas échéant, à une position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e74a9-106">Determines which list-view item, if any, is at a specified position.</span></span> <span data-ttu-id="e74a9-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) .</span><span class="sxs-lookup"><span data-stu-id="e74a9-107">You can send this message explicitly or by using the [**ListView\_HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e74a9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e74a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e74a9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e74a9-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e74a9-110">Doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="e74a9-110">Must be 0.</span></span> <span data-ttu-id="e74a9-111">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="e74a9-111">**Windows Vista.**</span></span> <span data-ttu-id="e74a9-112">Doit avoir la valeur-1 si les membres **iGroup** et **iSubItem** de la structure *lParam* doivent être récupérés.</span><span class="sxs-lookup"><span data-stu-id="e74a9-112">Should be -1 if the **iGroup** and **iSubItem** members of the *lParam* structure are to be retrieved.</span></span></dd> <dt>

<span data-ttu-id="e74a9-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e74a9-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e74a9-114">Pointeur vers une structure [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) qui contient la position à laquelle effectuer un test de positionnement et reçoit des informations sur les résultats du test de positionnement.</span><span class="sxs-lookup"><span data-stu-id="e74a9-114">Pointer to an [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure that contains the position to hit test and receives information about the results of the hit test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e74a9-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e74a9-115">Return value</span></span>

<span data-ttu-id="e74a9-116">Retourne l’index de l’élément à la position spécifiée, le cas échéant, ou-1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e74a9-116">Returns the index of the item at the specified position, if any, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e74a9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e74a9-117">Requirements</span></span>



| <span data-ttu-id="e74a9-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e74a9-118">Requirement</span></span> | <span data-ttu-id="e74a9-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e74a9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e74a9-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e74a9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e74a9-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e74a9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e74a9-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e74a9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e74a9-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e74a9-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e74a9-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e74a9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e74a9-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e74a9-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





