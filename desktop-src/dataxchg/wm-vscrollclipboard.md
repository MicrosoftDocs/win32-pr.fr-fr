---
title: Message WM_VSCROLLCLIPBOARD (winuser. h)
description: Envoyé au propriétaire du presse-papiers par une fenêtre de la visionneuse du presse-papiers lorsque le presse-papiers contient des données au \_ format CF OWNERDISPLAY et qu’un événement se produit dans la barre de défilement verticale de la visionneuse du presse-papiers.
ms.assetid: 17bd32c4-1b07-42b7-b269-f517e3ec13f3
keywords:
- WM_VSCROLLCLIPBOARD l’échange de données de message
topic_type:
- apiref
api_name:
- WM_VSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a9e80aa342065ee88c8e1d7aa44c1fd598e411
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465614"
---
# <a name="wm_vscrollclipboard-message"></a><span data-ttu-id="0f21c-104">\_Message WM VSCROLLCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="0f21c-104">WM\_VSCROLLCLIPBOARD message</span></span>

<span data-ttu-id="0f21c-105">Envoyé au propriétaire du presse-papiers par une fenêtre de la visionneuse du presse-papiers lorsque le presse-papiers contient des données au format [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) et qu’un événement se produit dans la barre de défilement verticale de la visionneuse du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="0f21c-105">Sent to the clipboard owner by a clipboard viewer window when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and an event occurs in the clipboard viewer's vertical scroll bar.</span></span> <span data-ttu-id="0f21c-106">Le propriétaire doit faire défiler l’image du presse-papiers et mettre à jour les valeurs de la barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="0f21c-106">The owner should scroll the clipboard image and update the scroll bar values.</span></span>


```C++
#define WM_VSCROLLCLIPBOARD             0x030A
```



## <a name="parameters"></a><span data-ttu-id="0f21c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f21c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f21c-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f21c-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f21c-109">Handle de la fenêtre de la visionneuse du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="0f21c-109">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="0f21c-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f21c-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f21c-111">Le mot de poids faible de *lParam* spécifie un événement de barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="0f21c-111">The low-order word of *lParam* specifies a scroll bar event.</span></span> <span data-ttu-id="0f21c-112">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0f21c-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="0f21c-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f21c-113">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="0f21c-114">Signification</span><span class="sxs-lookup"><span data-stu-id="0f21c-114">Meaning</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <span data-ttu-id="0f21c-115"><dt>**SB \_**</dt> <dt>7</dt> en bas</span><span class="sxs-lookup"><span data-stu-id="0f21c-115"><dt>**SB\_BOTTOM**</dt> <dt>7</dt></span></span> </dl>                      | <span data-ttu-id="0f21c-116">Faites défiler vers la droite.</span><span class="sxs-lookup"><span data-stu-id="0f21c-116">Scroll to lower right.</span></span><br/>                                                                 |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="0f21c-117"><dt>**SB \_ ENDSCROLL**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="0f21c-117"><dt>**SB\_ENDSCROLL**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="0f21c-118">Fin du défilement.</span><span class="sxs-lookup"><span data-stu-id="0f21c-118">End scroll.</span></span><br/>                                                                            |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <span data-ttu-id="0f21c-119"><dt>**SB \_ LINEDOWN**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0f21c-119"><dt>**SB\_LINEDOWN**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="0f21c-120">Faire défiler d’une ligne vers le dessous.</span><span class="sxs-lookup"><span data-stu-id="0f21c-120">Scroll one line down.</span></span><br/>                                                                  |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <span data-ttu-id="0f21c-121"><dt>**SB \_ GAMME**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0f21c-121"><dt>**SB\_LINEUP**</dt> <dt>0</dt></span></span> </dl>                      | <span data-ttu-id="0f21c-122">Faire défiler d’une ligne vers le haut.</span><span class="sxs-lookup"><span data-stu-id="0f21c-122">Scroll one line up.</span></span><br/>                                                                    |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <span data-ttu-id="0f21c-123"><dt>**SB \_ PG SUIV**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0f21c-123"><dt>**SB\_PAGEDOWN**</dt> <dt>3</dt></span></span> </dl>                | <span data-ttu-id="0f21c-124">Faire défiler d’une page vers le dessous.</span><span class="sxs-lookup"><span data-stu-id="0f21c-124">Scroll one page down.</span></span><br/>                                                                  |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <span data-ttu-id="0f21c-125"><dt>**SB \_ PG PRÉC**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0f21c-125"><dt>**SB\_PAGEUP**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="0f21c-126">Faire défiler d’une page vers le haut.</span><span class="sxs-lookup"><span data-stu-id="0f21c-126">Scroll one page up.</span></span><br/>                                                                    |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="0f21c-127"><dt>**SB \_ THUMBPOSITION**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="0f21c-127"><dt>**SB\_THUMBPOSITION**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="0f21c-128">Faites défiler jusqu’à position absolue.</span><span class="sxs-lookup"><span data-stu-id="0f21c-128">Scroll to absolute position.</span></span> <span data-ttu-id="0f21c-129">La position actuelle est spécifiée par le mot de poids fort.</span><span class="sxs-lookup"><span data-stu-id="0f21c-129">The current position is specified by the high-order word.</span></span><br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <span data-ttu-id="0f21c-130"><dt>**SB \_**</dt> <dt>6</dt> premiers</span><span class="sxs-lookup"><span data-stu-id="0f21c-130"><dt>**SB\_TOP**</dt> <dt>6</dt></span></span> </dl>                               | <span data-ttu-id="0f21c-131">Faites défiler vers le haut à gauche.</span><span class="sxs-lookup"><span data-stu-id="0f21c-131">Scroll to upper left.</span></span><br/>                                                                  |



 

<span data-ttu-id="0f21c-132">Le mot de poids fort de *lParam* spécifie la position actuelle de la case de défilement si le mot de poids faible de *lParam* est **SB \_ THUMBPOSITION**; dans le cas contraire, le mot de poids fort de *lParam* n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="0f21c-132">The high-order word of *lParam* specifies the current position of the scroll box if the low-order word of *lParam* is **SB\_THUMBPOSITION**; otherwise, the high-order word of *lParam* is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f21c-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f21c-133">Return value</span></span>

<span data-ttu-id="0f21c-134">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="0f21c-134">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f21c-135">Notes</span><span class="sxs-lookup"><span data-stu-id="0f21c-135">Remarks</span></span>

<span data-ttu-id="0f21c-136">Le propriétaire du presse-papiers peut utiliser la fonction [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) pour faire défiler l’image dans la fenêtre de la visionneuse du presse-papiers et invalider la région appropriée.</span><span class="sxs-lookup"><span data-stu-id="0f21c-136">The clipboard owner can use the [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) function to scroll the image in the clipboard viewer window and invalidate the appropriate region.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f21c-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f21c-137">Requirements</span></span>



| <span data-ttu-id="0f21c-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f21c-138">Requirement</span></span> | <span data-ttu-id="0f21c-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f21c-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f21c-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f21c-140">Minimum supported client</span></span><br/> | <span data-ttu-id="0f21c-141">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f21c-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0f21c-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f21c-142">Minimum supported server</span></span><br/> | <span data-ttu-id="0f21c-143">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f21c-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0f21c-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f21c-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f21c-145"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f21c-145"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f21c-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f21c-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="0f21c-147">**Référence**</span><span class="sxs-lookup"><span data-stu-id="0f21c-147">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="0f21c-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0f21c-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="0f21c-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0f21c-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="0f21c-150">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="0f21c-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0f21c-151">Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="0f21c-151">Clipboard</span></span>](clipboard.md)
</dt> <dt>

<span data-ttu-id="0f21c-152">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="0f21c-152">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="0f21c-153">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="0f21c-153">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span></span>
</dt> </dl>

 

