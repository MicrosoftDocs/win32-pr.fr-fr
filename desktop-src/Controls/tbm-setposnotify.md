---
title: Message TBM_SETPOSNOTIFY (commctrl. h)
description: Définit la position logique actuelle du curseur dans un TrackBar.
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- TBM_SETPOSNOTIFY les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_SETPOSNOTIFY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 636a2add9f13470a89b312450f1a3dcbc185be2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464771"
---
# <a name="tbm_setposnotify-message"></a><span data-ttu-id="6acc5-104">\_Message TBM SETPOSNOTIFY</span><span class="sxs-lookup"><span data-stu-id="6acc5-104">TBM\_SETPOSNOTIFY message</span></span>

<span data-ttu-id="6acc5-105">Définit la position logique actuelle du curseur dans un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="6acc5-105">Sets the current logical position of the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="6acc5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6acc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6acc5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6acc5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6acc5-108">wParam n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="6acc5-108">wParam is unused.</span></span>

</dd> <dt>

<span data-ttu-id="6acc5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6acc5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6acc5-110">Nouvelle position logique du curseur.</span><span class="sxs-lookup"><span data-stu-id="6acc5-110">New logical position of the slider.</span></span> <span data-ttu-id="6acc5-111">Les positions logiques valides sont les valeurs entières de la plage de la plage de la barre de défilement minimale à la position maximale du curseur.</span><span class="sxs-lookup"><span data-stu-id="6acc5-111">Valid logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span> <span data-ttu-id="6acc5-112">Si cette valeur est en dehors de la plage maximale et minimale du contrôle, la position est définie sur la valeur maximale ou minimale.</span><span class="sxs-lookup"><span data-stu-id="6acc5-112">If this value is outside the control's maximum and minimum range, the position is set to the maximum or minimum value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6acc5-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6acc5-113">Return value</span></span>

<span data-ttu-id="6acc5-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="6acc5-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6acc5-115">Notes</span><span class="sxs-lookup"><span data-stu-id="6acc5-115">Remarks</span></span>

<span data-ttu-id="6acc5-116">L’appel de **TBM \_ SETPOSNOTIFY** définit l’emplacement du curseur de la barre de défilement de la barre de défilement, comme [**TBM \_ SetPos**](tbm-setpos.md) , mais il fait également en sorte que le TrackBar informe son parent d’un déplacement via un message [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="6acc5-116">Calling **TBM\_SETPOSNOTIFY** will set the trackbar slider location like [**TBM\_SETPOS**](tbm-setpos.md) would, but it will also cause the trackbar to notify its parent of a move via a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6acc5-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6acc5-117">Requirements</span></span>



| <span data-ttu-id="6acc5-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6acc5-118">Requirement</span></span> | <span data-ttu-id="6acc5-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="6acc5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6acc5-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6acc5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6acc5-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6acc5-121">Windows 7 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6acc5-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6acc5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6acc5-123">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6acc5-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6acc5-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="6acc5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6acc5-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6acc5-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





