---
title: Message LVM_GETNUMBEROFWORKAREAS (commctrl. h)
description: Récupère le nombre de zones de travail dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetNumberOfWorkAreas.
ms.assetid: ce0bcccd-62a2-45a4-959e-9959c9ca0c46
keywords:
- LVM_GETNUMBEROFWORKAREAS les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETNUMBEROFWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73c62b7184ba60b979356a98a93d2579c8f74a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942647"
---
# <a name="lvm_getnumberofworkareas-message"></a><span data-ttu-id="263ae-105">\_Message GETNUMBEROFWORKAREAS LVM</span><span class="sxs-lookup"><span data-stu-id="263ae-105">LVM\_GETNUMBEROFWORKAREAS message</span></span>

<span data-ttu-id="263ae-106">Récupère le nombre de zones de travail dans un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="263ae-106">Retrieves the number of working areas in a list-view control.</span></span> <span data-ttu-id="263ae-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetNumberOfWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) .</span><span class="sxs-lookup"><span data-stu-id="263ae-107">You can send this message explicitly or use the [**ListView\_GetNumberOfWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="263ae-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="263ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="263ae-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="263ae-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="263ae-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="263ae-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="263ae-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="263ae-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="263ae-112">Pointeur vers une valeur UINT qui reçoit le nombre de zones de travail dans le contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="263ae-112">Pointer to a UINT value that receives the number of working areas in the list-view control.</span></span> <span data-ttu-id="263ae-113">Si la valeur zéro est placée dans cette variable, aucune zone de travail n’est actuellement définie.</span><span class="sxs-lookup"><span data-stu-id="263ae-113">If zero is placed in this variable, then no working areas are currently set.</span></span> <span data-ttu-id="263ae-114">Cette valeur ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="263ae-114">This value cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="263ae-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="263ae-115">Return value</span></span>

<span data-ttu-id="263ae-116">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="263ae-116">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="263ae-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="263ae-117">Requirements</span></span>



| <span data-ttu-id="263ae-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="263ae-118">Requirement</span></span> | <span data-ttu-id="263ae-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="263ae-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="263ae-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="263ae-120">Minimum supported client</span></span><br/> | <span data-ttu-id="263ae-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="263ae-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="263ae-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="263ae-122">Minimum supported server</span></span><br/> | <span data-ttu-id="263ae-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="263ae-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="263ae-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="263ae-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="263ae-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="263ae-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="263ae-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="263ae-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="263ae-127">Utilisation de contrôles List-View</span><span class="sxs-lookup"><span data-stu-id="263ae-127">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 





