---
title: Message TBM_SETLINESIZE (commctrl. h)
description: Définit le nombre de positions logiques du curseur de la barre de défilement en réponse à une entrée au clavier à partir des touches de direction, telles que les touches ou. Les positions logiques sont les incréments de l’entier dans la plage de la plage de la barre de défilement minimale à la position maximale du curseur.
ms.assetid: 7fe3f9b8-2ddf-4460-882f-6be439f83daa
keywords:
- TBM_SETLINESIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_SETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec898ed09b20f15023ef04a399f5644df746e495
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941795"
---
# <a name="tbm_setlinesize-message"></a><span data-ttu-id="97219-105">\_Message TBM SETLINESIZE</span><span class="sxs-lookup"><span data-stu-id="97219-105">TBM\_SETLINESIZE message</span></span>

<span data-ttu-id="97219-106">Définit le nombre de positions logiques du curseur de la barre de défilement en réponse à une entrée au clavier à partir des touches de direction, telles que les touches ou.</span><span class="sxs-lookup"><span data-stu-id="97219-106">Sets the number of logical positions the trackbar's slider moves in response to keyboard input from the arrow keys, such as the or keys.</span></span> <span data-ttu-id="97219-107">Les positions logiques sont les incréments de l’entier dans la plage de la plage de la barre de défilement minimale à la position maximale du curseur.</span><span class="sxs-lookup"><span data-stu-id="97219-107">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="97219-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97219-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97219-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="97219-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="97219-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="97219-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="97219-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97219-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97219-112">Nouvelle taille de ligne.</span><span class="sxs-lookup"><span data-stu-id="97219-112">New line size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97219-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97219-113">Return value</span></span>

<span data-ttu-id="97219-114">Retourne une valeur 32 bits qui spécifie la taille de ligne précédente.</span><span class="sxs-lookup"><span data-stu-id="97219-114">Returns a 32-bit value that specifies the previous line size.</span></span>

## <a name="remarks"></a><span data-ttu-id="97219-115">Notes</span><span class="sxs-lookup"><span data-stu-id="97219-115">Remarks</span></span>

<span data-ttu-id="97219-116">La valeur par défaut de la taille de ligne est 1.</span><span class="sxs-lookup"><span data-stu-id="97219-116">The default setting for the line size is 1.</span></span>

<span data-ttu-id="97219-117">Le TrackBar envoie également un message [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) avec les \_ codes de notification de la programmation to et de to \_ LINEDOWN à sa fenêtre parente quand l’utilisateur appuie sur les touches de direction.</span><span class="sxs-lookup"><span data-stu-id="97219-117">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_LINEUP and TB\_LINEDOWN notification codes to its parent window when the user presses the arrow keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="97219-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97219-118">Requirements</span></span>



| <span data-ttu-id="97219-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97219-119">Requirement</span></span> | <span data-ttu-id="97219-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="97219-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97219-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97219-121">Minimum supported client</span></span><br/> | <span data-ttu-id="97219-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97219-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="97219-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97219-123">Minimum supported server</span></span><br/> | <span data-ttu-id="97219-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97219-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97219-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="97219-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="97219-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="97219-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97219-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97219-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97219-128">**TBM \_ GETLINESIZE**</span><span class="sxs-lookup"><span data-stu-id="97219-128">**TBM\_GETLINESIZE**</span></span>](tbm-getlinesize.md)
</dt> </dl>

 

 





