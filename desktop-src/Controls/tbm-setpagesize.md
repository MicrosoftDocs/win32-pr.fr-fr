---
title: Message TBM_SETPAGESIZE (commctrl. h)
description: Définit le nombre de positions logiques du curseur de la barre de défilement en réponse à l’entrée au clavier, comme les touches ou, ou l’entrée de la souris, comme les clics dans le canal de la barre de défilement.
ms.assetid: 34edb868-4b6b-4b3f-b315-3ce39346b134
keywords:
- TBM_SETPAGESIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_SETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5d8a396bb605b4276346e84e7b46bfbefe0657
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033090"
---
# <a name="tbm_setpagesize-message"></a><span data-ttu-id="4077c-104">\_Message TBM SETPAGESIZE</span><span class="sxs-lookup"><span data-stu-id="4077c-104">TBM\_SETPAGESIZE message</span></span>

<span data-ttu-id="4077c-105">Définit le nombre de positions logiques du curseur de la barre de défilement en réponse à l’entrée au clavier, comme les touches ou, ou l’entrée de la souris, comme les clics dans le canal de la barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="4077c-105">Sets the number of logical positions the trackbar's slider moves in response to keyboard input, such as the or keys, or mouse input, such as clicks in the trackbar's channel.</span></span> <span data-ttu-id="4077c-106">Les positions logiques sont les incréments de l’entier dans la plage de la plage de la barre de défilement minimale à la position maximale du curseur.</span><span class="sxs-lookup"><span data-stu-id="4077c-106">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="4077c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4077c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4077c-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4077c-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4077c-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="4077c-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4077c-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4077c-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4077c-111">Nouvelle taille de page.</span><span class="sxs-lookup"><span data-stu-id="4077c-111">New page size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4077c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4077c-112">Return value</span></span>

<span data-ttu-id="4077c-113">Retourne une valeur 32 bits qui spécifie la taille de page précédente.</span><span class="sxs-lookup"><span data-stu-id="4077c-113">Returns a 32-bit value that specifies the previous page size.</span></span>

## <a name="remarks"></a><span data-ttu-id="4077c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="4077c-114">Remarks</span></span>

<span data-ttu-id="4077c-115">La barre de défilement envoie également un message [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) avec les \_ codes de \_ notification PG. préc et to PageDown à sa fenêtre parente lorsqu’elle reçoit une entrée de clavier ou de souris qui fait défiler la page.</span><span class="sxs-lookup"><span data-stu-id="4077c-115">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_PAGEUP and TB\_PAGEDOWN notification codes to its parent window when it receives keyboard or mouse input that scrolls the page.</span></span>

## <a name="requirements"></a><span data-ttu-id="4077c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4077c-116">Requirements</span></span>



| <span data-ttu-id="4077c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4077c-117">Requirement</span></span> | <span data-ttu-id="4077c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4077c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4077c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4077c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4077c-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4077c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4077c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4077c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4077c-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4077c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4077c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="4077c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4077c-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4077c-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4077c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4077c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4077c-126">**TBM \_ GETPAGESIZE**</span><span class="sxs-lookup"><span data-stu-id="4077c-126">**TBM\_GETPAGESIZE**</span></span>](tbm-getpagesize.md)
</dt> </dl>

 

 





