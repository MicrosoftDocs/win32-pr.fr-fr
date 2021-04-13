---
title: Message WM_GETHOTKEY (winuser. h)
description: Envoyé pour déterminer la touche d’accès rapide associée à une fenêtre.
ms.assetid: 6f527758-e713-47a8-a571-3bf3270f0b33
keywords:
- WM_GETHOTKEY l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_GETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f045ceefaf33c8d8edba0cb69e062ad589cfd833
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464935"
---
# <a name="wm_gethotkey-message"></a><span data-ttu-id="e258d-104">\_Message WM GETHOTKEY</span><span class="sxs-lookup"><span data-stu-id="e258d-104">WM\_GETHOTKEY message</span></span>

<span data-ttu-id="e258d-105">Envoyé pour déterminer la touche d’accès rapide associée à une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e258d-105">Sent to determine the hot key associated with a window.</span></span>


```C++
#define WM_GETHOTKEY                    0x0033
```



## <a name="parameters"></a><span data-ttu-id="e258d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e258d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e258d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e258d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e258d-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e258d-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e258d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e258d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e258d-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e258d-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e258d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e258d-111">Return value</span></span>

<span data-ttu-id="e258d-112">La valeur de retour est le code de touche virtuelle et les modificateurs de la touche d’accès rapide, ou **null** si aucune touche d’accès rapide n’est associée à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e258d-112">The return value is the virtual-key code and modifiers for the hot key, or **NULL** if no hot key is associated with the window.</span></span> <span data-ttu-id="e258d-113">Le code de la touche virtuelle se trouve dans l’octet de poids faible de la valeur de retour et les modificateurs se trouvent dans l’octet de poids fort.</span><span class="sxs-lookup"><span data-stu-id="e258d-113">The virtual-key code is in the low byte of the return value and the modifiers are in the high byte.</span></span> <span data-ttu-id="e258d-114">Les modificateurs peuvent être une combinaison des indicateurs suivants à partir de CommCtrl. h.</span><span class="sxs-lookup"><span data-stu-id="e258d-114">The modifiers can be a combination of the following flags from CommCtrl.h.</span></span>



| <span data-ttu-id="e258d-115">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e258d-115">Return code/value</span></span>                                                                                                                                         | <span data-ttu-id="e258d-116">Description</span><span class="sxs-lookup"><span data-stu-id="e258d-116">Description</span></span>             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <dl> <span data-ttu-id="e258d-117"><dt>**HOTKEYF \_ ALT**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="e258d-117"><dt>**HOTKEYF\_ALT**</dt> <dt>0x04</dt></span></span> </dl>     | <span data-ttu-id="e258d-118">touche ALT</span><span class="sxs-lookup"><span data-stu-id="e258d-118">ALT key</span></span><br/>      |
| <dl> <span data-ttu-id="e258d-119"><dt>**HOTKEYF \_ CONTRÔLE**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="e258d-119"><dt>**HOTKEYF\_CONTROL**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="e258d-120">Touche CTRL</span><span class="sxs-lookup"><span data-stu-id="e258d-120">CTRL key</span></span><br/>     |
| <dl> <span data-ttu-id="e258d-121"><dt>**HOTKEYF \_**</dt> <dt>0x08</dt> de l’ext.</span><span class="sxs-lookup"><span data-stu-id="e258d-121"><dt>**HOTKEYF\_EXT**</dt> <dt>0x08</dt></span></span> </dl>     | <span data-ttu-id="e258d-122">Clé étendue</span><span class="sxs-lookup"><span data-stu-id="e258d-122">Extended key</span></span><br/> |
| <dl> <span data-ttu-id="e258d-123"><dt>**HOTKEYF \_ DÉCALAGE**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="e258d-123"><dt>**HOTKEYF\_SHIFT**</dt> <dt>0x01</dt></span></span> </dl>   | <span data-ttu-id="e258d-124">Touche Maj</span><span class="sxs-lookup"><span data-stu-id="e258d-124">SHIFT key</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="e258d-125">Notes</span><span class="sxs-lookup"><span data-stu-id="e258d-125">Remarks</span></span>

<span data-ttu-id="e258d-126">Ces touches d’accès rapide ne sont pas liées aux touches d’accès rapide définies par la fonction [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) .</span><span class="sxs-lookup"><span data-stu-id="e258d-126">These hot keys are unrelated to the hot keys set by the [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e258d-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e258d-127">Requirements</span></span>



| <span data-ttu-id="e258d-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e258d-128">Requirement</span></span> | <span data-ttu-id="e258d-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="e258d-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e258d-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e258d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e258d-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e258d-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e258d-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e258d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e258d-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e258d-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e258d-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="e258d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e258d-135"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e258d-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e258d-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e258d-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="e258d-137">**Référence**</span><span class="sxs-lookup"><span data-stu-id="e258d-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e258d-138">**RegisterHotKey**</span><span class="sxs-lookup"><span data-stu-id="e258d-138">**RegisterHotKey**</span></span>](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[<span data-ttu-id="e258d-139">**\_SETHOTKEY WM**</span><span class="sxs-lookup"><span data-stu-id="e258d-139">**WM\_SETHOTKEY**</span></span>](wm-sethotkey.md)
</dt> <dt>

<span data-ttu-id="e258d-140">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="e258d-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e258d-141">Entrée au clavier</span><span class="sxs-lookup"><span data-stu-id="e258d-141">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

