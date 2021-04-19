---
title: Message SBM_GETSCROLLINFO (winuser. h)
description: Le \_ message SBM GETSCROLLINFO est envoyé pour récupérer les paramètres d’une barre de défilement.
ms.assetid: 3b43430f-b55f-43ec-8558-baf5c953064f
keywords:
- SBM_GETSCROLLINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- SBM_GETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4cb05b05ba2686d755c5fa34adcff0016433346
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510786"
---
# <a name="sbm_getscrollinfo-message"></a><span data-ttu-id="1ba75-104">\_Message SBM GETSCROLLINFO</span><span class="sxs-lookup"><span data-stu-id="1ba75-104">SBM\_GETSCROLLINFO message</span></span>

<span data-ttu-id="1ba75-105">Le message **SBM \_ GETSCROLLINFO** est envoyé pour récupérer les paramètres d’une barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="1ba75-105">The **SBM\_GETSCROLLINFO** message is sent to retrieve the parameters of a scroll bar.</span></span>

<span data-ttu-id="1ba75-106">Les applications ne doivent pas envoyer ce message directement.</span><span class="sxs-lookup"><span data-stu-id="1ba75-106">Applications should not send this message directly.</span></span> <span data-ttu-id="1ba75-107">Au lieu de cela, ils doivent utiliser la fonction [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="1ba75-107">Instead, they should use the [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) function.</span></span> <span data-ttu-id="1ba75-108">Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1ba75-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="1ba75-109">Les applications qui implémentent un contrôle de barre de défilement personnalisé doivent répondre à ces messages pour que la fonction **GetScrollInfo** fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="1ba75-109">Applications which implement a custom scroll bar control must respond to these messages for the **GetScrollInfo** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ba75-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ba75-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ba75-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ba75-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ba75-112">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="1ba75-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ba75-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ba75-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ba75-114">Pointeur vers une structure [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="1ba75-114">Pointer to a [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure.</span></span> <span data-ttu-id="1ba75-115">Avant d’appeler [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), définissez le membre **cbSize** de la structure sur **sizeof**(**SCROLLINFO**) et définissez le membre **fmask** pour spécifier les paramètres de barre de défilement à récupérer.</span><span class="sxs-lookup"><span data-stu-id="1ba75-115">Before calling [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), set the **cbSize** member of the structure to **sizeof**(**SCROLLINFO**), and set the **fMask** member to specify the scroll bar parameters to retrieve.</span></span> <span data-ttu-id="1ba75-116">Avant de retourner, le message copie les paramètres spécifiés dans les membres appropriés de la structure.</span><span class="sxs-lookup"><span data-stu-id="1ba75-116">Before returning, the message copies the specified parameters to the appropriate members of the structure.</span></span>

<span data-ttu-id="1ba75-117">Le membre **fmask** peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1ba75-117">The **fMask** member can be one or more of the following values.</span></span>



| <span data-ttu-id="1ba75-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ba75-118">Value</span></span>                                                                                                                                                      | <span data-ttu-id="1ba75-119">Signification</span><span class="sxs-lookup"><span data-stu-id="1ba75-119">Meaning</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="SIF_ALL"></span><span id="sif_all"></span><dl> <span data-ttu-id="1ba75-120"><dt>**SIF \_ tout**</dt></span><span class="sxs-lookup"><span data-stu-id="1ba75-120"><dt>**SIF\_ALL**</dt></span></span> </dl>                | <span data-ttu-id="1ba75-121">Combinaison de la \_ page SIF, de SIF \_ pos, de la \_ plage SIF et de SIF \_ TRACKPOS.</span><span class="sxs-lookup"><span data-stu-id="1ba75-121">Combination of SIF\_PAGE, SIF\_POS, SIF\_RANGE, and SIF\_TRACKPOS.</span></span><br/>       |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <span data-ttu-id="1ba75-122"><dt>**\_page SIF**</dt></span><span class="sxs-lookup"><span data-stu-id="1ba75-122"><dt>**SIF\_PAGE**</dt></span></span> </dl>             | <span data-ttu-id="1ba75-123">Copie la page de défilement dans le membre nPage.</span><span class="sxs-lookup"><span data-stu-id="1ba75-123">Copies the scroll page to the nPage member.</span></span><br/>                              |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <span data-ttu-id="1ba75-124"><dt>**\_pos SIF**</dt></span><span class="sxs-lookup"><span data-stu-id="1ba75-124"><dt>**SIF\_POS**</dt></span></span> </dl>                | <span data-ttu-id="1ba75-125">Copie la position de défilement dans le membre nPos.</span><span class="sxs-lookup"><span data-stu-id="1ba75-125">Copies the scroll position to the nPos member.</span></span> <br/>                          |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <span data-ttu-id="1ba75-126"><dt>**\_plage SIF**</dt></span><span class="sxs-lookup"><span data-stu-id="1ba75-126"><dt>**SIF\_RANGE**</dt></span></span> </dl>          | <span data-ttu-id="1ba75-127">Copie la plage de défilement vers les membres nMin et nMax.</span><span class="sxs-lookup"><span data-stu-id="1ba75-127">Copies the scroll range to the nMin and nMax members.</span></span> <br/>                   |
| <span id="SIF_TRACKPOS"></span><span id="sif_trackpos"></span><dl> <span data-ttu-id="1ba75-128"><dt>**\_TRACKPOS SIF**</dt></span><span class="sxs-lookup"><span data-stu-id="1ba75-128"><dt>**SIF\_TRACKPOS**</dt></span></span> </dl> | <span data-ttu-id="1ba75-129">Copie la position actuelle du suivi de la case de défilement dans le membre nTrackPos.</span><span class="sxs-lookup"><span data-stu-id="1ba75-129">Copies the current scroll box tracking position to the nTrackPos member.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ba75-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1ba75-130">Return value</span></span>

<span data-ttu-id="1ba75-131">Si le message a récupéré des valeurs, la valeur de retour est **true**. Sinon, la **valeur est false**.</span><span class="sxs-lookup"><span data-stu-id="1ba75-131">If the message retrieved any values, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ba75-132">Notes</span><span class="sxs-lookup"><span data-stu-id="1ba75-132">Remarks</span></span>

<span data-ttu-id="1ba75-133">Les messages qui indiquent la position de la barre de défilement, [**WM \_ HSCROLL**](wm-hscroll.md) et [**WM \_ VSCROLL**](wm-vscroll.md), fournissent uniquement 16 bits de données de position.</span><span class="sxs-lookup"><span data-stu-id="1ba75-133">The messages that indicate scroll bar position, [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md), provide only 16 bits of position data.</span></span> <span data-ttu-id="1ba75-134">Toutefois, la structure [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) utilisée par **SBM \_ GETSCROLLINFO**, [**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md), [**GETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)et [**SETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) fournit 32 bits de données de position de la barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="1ba75-134">However, the [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure used by **SBM\_GETSCROLLINFO**, [**SBM\_SETSCROLLINFO**](sbm-setscrollinfo.md), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), and [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) provides 32 bits of scroll bar position data.</span></span> <span data-ttu-id="1ba75-135">Vous pouvez utiliser ces messages et ces fonctions lors du traitement des messages **WM \_ HSCROLL** ou **WM \_ VSCROLL** pour obtenir les données de position de la barre de défilement 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1ba75-135">You can use these messages and functions while processing either the **WM\_HSCROLL** or **WM\_VSCROLL** messages to obtain 32-bit scroll bar position data.</span></span>

<span data-ttu-id="1ba75-136">Pour obtenir la position 32 bits de la case de défilement (Thumb) au cours d’un \_ Code de demande SB THUMBTRACK dans un message [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) , envoyez **\_ GETSCROLLINFO SBM** avec la \_ valeur d’TRACKPOS SIF dans le membre **fmask** de la structure [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="1ba75-136">To get the 32-bit position of the scroll box (thumb) during a SB\_THUMBTRACK request code in a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message, send **SBM\_GETSCROLLINFO** with the SIF\_TRACKPOS value in the **fMask** member of the [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure.</span></span> <span data-ttu-id="1ba75-137">Le message retourne la position de suivi de la case de défilement dans le membre **nTrackPos** de la structure **SCROLLINFO** .</span><span class="sxs-lookup"><span data-stu-id="1ba75-137">The message returns the tracking position of the scroll box in the **nTrackPos** member of the **SCROLLINFO** structure.</span></span> <span data-ttu-id="1ba75-138">Cela vous permet d’afficher la position de la case de défilement lorsque l’utilisateur la déplace.</span><span class="sxs-lookup"><span data-stu-id="1ba75-138">This allows you to get the position of the scroll box as the user moves it.</span></span> <span data-ttu-id="1ba75-139">Vous pouvez également utiliser la fonction [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) pour récupérer les mêmes informations.</span><span class="sxs-lookup"><span data-stu-id="1ba75-139">Alternatively, you can use the [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) function to get the same information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ba75-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ba75-140">Requirements</span></span>



| <span data-ttu-id="1ba75-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ba75-141">Requirement</span></span> | <span data-ttu-id="1ba75-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ba75-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ba75-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ba75-143">Minimum supported client</span></span><br/> | <span data-ttu-id="1ba75-144">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ba75-144">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1ba75-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ba75-145">Minimum supported server</span></span><br/> | <span data-ttu-id="1ba75-146">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ba75-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1ba75-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ba75-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ba75-148"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ba75-148"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ba75-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ba75-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="1ba75-150">**Référence**</span><span class="sxs-lookup"><span data-stu-id="1ba75-150">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1ba75-151">**GetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="1ba75-151">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="1ba75-152">**\_SETSCROLLINFO SBM**</span><span class="sxs-lookup"><span data-stu-id="1ba75-152">**SBM\_SETSCROLLINFO**</span></span>](sbm-setscrollinfo.md)
</dt> <dt>

[<span data-ttu-id="1ba75-153">**SCROLLINFO**</span><span class="sxs-lookup"><span data-stu-id="1ba75-153">**SCROLLINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[<span data-ttu-id="1ba75-154">**SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="1ba75-154">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

