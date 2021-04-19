---
title: Message SBM_SETSCROLLINFO (winuser. h)
description: Le \_ message SBM SETSCROLLINFO est envoyé pour définir les paramètres d’une barre de défilement.
ms.assetid: e0e42a81-67be-4d40-88c8-77398b068617
keywords:
- SBM_SETSCROLLINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- SBM_SETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e98abbca2d53d4b104caea22954472a17dfd5c1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518096"
---
# <a name="sbm_setscrollinfo-message"></a><span data-ttu-id="5ac7a-104">\_Message SBM SETSCROLLINFO</span><span class="sxs-lookup"><span data-stu-id="5ac7a-104">SBM\_SETSCROLLINFO message</span></span>

<span data-ttu-id="5ac7a-105">Le message **SBM \_ SETSCROLLINFO** est envoyé pour définir les paramètres d’une barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="5ac7a-105">The **SBM\_SETSCROLLINFO** message is sent to set the parameters of a scroll bar.</span></span>

<span data-ttu-id="5ac7a-106">Les applications ne doivent pas envoyer ce message directement.</span><span class="sxs-lookup"><span data-stu-id="5ac7a-106">Applications should not send this message directly.</span></span> <span data-ttu-id="5ac7a-107">Au lieu de cela, ils doivent utiliser la fonction [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="5ac7a-107">Instead, they should use the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) function.</span></span> <span data-ttu-id="5ac7a-108">Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5ac7a-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="5ac7a-109">Les applications qui implémentent un contrôle de barre de défilement personnalisé doivent répondre à ces messages pour que la fonction **SetScrollInfo** fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="5ac7a-109">Applications which implement a custom scroll bar control must respond to these messages for the **SetScrollInfo** function to function properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="5ac7a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ac7a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ac7a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5ac7a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ac7a-112">Spécifie si la barre de défilement est redessinée pour refléter la nouvelle position de la case de défilement.</span><span class="sxs-lookup"><span data-stu-id="5ac7a-112">Specifies whether the scroll bar is redrawn to reflect the new scroll box position.</span></span> <span data-ttu-id="5ac7a-113">Si ce paramètre a la **valeur true**, la barre de défilement est redessinée.</span><span class="sxs-lookup"><span data-stu-id="5ac7a-113">If this parameter is **TRUE**, the scroll bar is redrawn.</span></span> <span data-ttu-id="5ac7a-114">Si la **valeur est false**, la barre de défilement n’est pas redessinée.</span><span class="sxs-lookup"><span data-stu-id="5ac7a-114">If it is **FALSE**, the scroll bar is not redrawn.</span></span>

</dd> <dt>

<span data-ttu-id="5ac7a-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5ac7a-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ac7a-116">Pointeur vers une structure [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="5ac7a-116">Pointer to a [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure.</span></span> <span data-ttu-id="5ac7a-117">Avant d’appeler [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), définissez le membre **cbSize** de la structure sur **sizeof**(**SCROLLINFO**), définissez le membre **fmask** pour indiquer les paramètres à définir et spécifiez les nouvelles valeurs de paramètre dans les membres appropriés.</span><span class="sxs-lookup"><span data-stu-id="5ac7a-117">Before calling [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), set the **cbSize** member of the structure to **sizeof**(**SCROLLINFO**), set the **fMask** member to indicate the parameters to set, and specify the new parameter values in the appropriate members.</span></span>

<span data-ttu-id="5ac7a-118">Le membre **fmask** peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="5ac7a-118">The **fMask** member can be one or more of the following values.</span></span>



| <span data-ttu-id="5ac7a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ac7a-119">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="5ac7a-120">Signification</span><span class="sxs-lookup"><span data-stu-id="5ac7a-120">Meaning</span></span>                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIF_DISABLENOSCROLL"></span><span id="sif_disablenoscroll"></span><dl> <span data-ttu-id="5ac7a-121"><dt>**\_DISABLENOSCROLL SIF**</dt></span><span class="sxs-lookup"><span data-stu-id="5ac7a-121"><dt>**SIF\_DISABLENOSCROLL**</dt></span></span> </dl> | <span data-ttu-id="5ac7a-122">Désactive la barre de défilement au lieu de la supprimer, si les nouveaux paramètres de la barre de défilement rendent la barre de défilement inutile.</span><span class="sxs-lookup"><span data-stu-id="5ac7a-122">Disables the scroll bar instead of removing it, if the scroll bar's new parameters make the scroll bar unnecessary.</span></span><br/> |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <span data-ttu-id="5ac7a-123"><dt>**\_page SIF**</dt></span><span class="sxs-lookup"><span data-stu-id="5ac7a-123"><dt>**SIF\_PAGE**</dt></span></span> </dl>                                  | <span data-ttu-id="5ac7a-124">Définit la page de défilement sur la valeur spécifiée dans le membre **nPage** .</span><span class="sxs-lookup"><span data-stu-id="5ac7a-124">Sets the scroll page to the value specified in the **nPage** member.</span></span><br/>                                                |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <span data-ttu-id="5ac7a-125"><dt>**\_pos SIF**</dt></span><span class="sxs-lookup"><span data-stu-id="5ac7a-125"><dt>**SIF\_POS**</dt></span></span> </dl>                                     | <span data-ttu-id="5ac7a-126">Définit la position de défilement sur la valeur spécifiée dans le membre **nPos** .</span><span class="sxs-lookup"><span data-stu-id="5ac7a-126">Sets the scroll position to the value specified in the **nPos** member.</span></span> <br/>                                            |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <span data-ttu-id="5ac7a-127"><dt>**\_plage SIF**</dt></span><span class="sxs-lookup"><span data-stu-id="5ac7a-127"><dt>**SIF\_RANGE**</dt></span></span> </dl>                               | <span data-ttu-id="5ac7a-128">Affecte à la plage de défilement la valeur spécifiée dans les membres **nMin** et **nmax** .</span><span class="sxs-lookup"><span data-stu-id="5ac7a-128">Sets the scroll range to the value specified in the **nMin** and **nMax** members.</span></span> <br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ac7a-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5ac7a-129">Return value</span></span>

<span data-ttu-id="5ac7a-130">La valeur de retour correspond à la position actuelle de la case de défilement.</span><span class="sxs-lookup"><span data-stu-id="5ac7a-130">The return value is the current position of the scroll box.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ac7a-131">Notes</span><span class="sxs-lookup"><span data-stu-id="5ac7a-131">Remarks</span></span>

<span data-ttu-id="5ac7a-132">Les messages qui indiquent la position de la barre de défilement, [**WM \_ HSCROLL**](wm-hscroll.md) et [**WM \_ VSCROLL**](wm-vscroll.md), fournissent uniquement 16 bits de données de position.</span><span class="sxs-lookup"><span data-stu-id="5ac7a-132">The messages that indicate scroll bar position, [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md), provide only 16 bits of position data.</span></span> <span data-ttu-id="5ac7a-133">Toutefois, la structure [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) utilisée par [**SBM \_ GETSCROLLINFO**](sbm-getscrollinfo.md), **SBM \_ SETSCROLLINFO**, [**GETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)et [**SETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) fournit 32 bits de données de position de la barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="5ac7a-133">However, the [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure used by [**SBM\_GETSCROLLINFO**](sbm-getscrollinfo.md), **SBM\_SETSCROLLINFO**, [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), and [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) provides 32 bits of scroll bar position data.</span></span> <span data-ttu-id="5ac7a-134">Vous pouvez utiliser ces messages et ces fonctions lors du traitement des messages **WM \_ HSCROLL** ou **WM \_ VSCROLL** pour obtenir les données de position de la barre de défilement 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5ac7a-134">You can use these messages and functions while processing either the **WM\_HSCROLL** or **WM\_VSCROLL** messages to obtain 32-bit scroll bar position data.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ac7a-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ac7a-135">Requirements</span></span>



| <span data-ttu-id="5ac7a-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ac7a-136">Requirement</span></span> | <span data-ttu-id="5ac7a-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ac7a-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac7a-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ac7a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5ac7a-139">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5ac7a-139">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5ac7a-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ac7a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5ac7a-141">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5ac7a-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5ac7a-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ac7a-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ac7a-143"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ac7a-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ac7a-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ac7a-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="5ac7a-145">**Référence**</span><span class="sxs-lookup"><span data-stu-id="5ac7a-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5ac7a-146">**GetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="5ac7a-146">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="5ac7a-147">**\_GETSCROLLINFO SBM**</span><span class="sxs-lookup"><span data-stu-id="5ac7a-147">**SBM\_GETSCROLLINFO**</span></span>](sbm-getscrollinfo.md)
</dt> <dt>

[<span data-ttu-id="5ac7a-148">**SCROLLINFO**</span><span class="sxs-lookup"><span data-stu-id="5ac7a-148">**SCROLLINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[<span data-ttu-id="5ac7a-149">**SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="5ac7a-149">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

