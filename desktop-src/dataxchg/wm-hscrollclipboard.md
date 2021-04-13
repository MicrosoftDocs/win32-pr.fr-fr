---
title: Message WM_HSCROLLCLIPBOARD (winuser. h)
description: Envoyé au propriétaire du presse-papiers par une fenêtre de la visionneuse du presse-papiers.
ms.assetid: 73558de6-a822-40f7-9eb2-47ea5afd4e6e
keywords:
- WM_HSCROLLCLIPBOARD l’échange de données de message
topic_type:
- apiref
api_name:
- WM_HSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34ee33709601b483258ae0aec4873c47fa69a00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466366"
---
# <a name="wm_hscrollclipboard-message"></a><span data-ttu-id="ea709-104">\_Message WM HSCROLLCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="ea709-104">WM\_HSCROLLCLIPBOARD message</span></span>

<span data-ttu-id="ea709-105">Envoyé au propriétaire du presse-papiers par une fenêtre de la visionneuse du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="ea709-105">Sent to the clipboard owner by a clipboard viewer window.</span></span> <span data-ttu-id="ea709-106">Cela se produit lorsque le presse-papiers contient des données au format [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) et qu’un événement se produit dans la barre de défilement horizontale de la visionneuse du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="ea709-106">This occurs when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and an event occurs in the clipboard viewer's horizontal scroll bar.</span></span> <span data-ttu-id="ea709-107">Le propriétaire doit faire défiler l’image du presse-papiers et mettre à jour les valeurs de la barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="ea709-107">The owner should scroll the clipboard image and update the scroll bar values.</span></span>


```C++
#define WM_HSCROLLCLIPBOARD             0x030E
```



## <a name="parameters"></a><span data-ttu-id="ea709-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea709-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea709-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea709-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea709-110">Handle de la fenêtre de la visionneuse du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="ea709-110">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="ea709-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea709-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea709-112">Le mot de poids faible de *lParam* spécifie un événement de barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="ea709-112">The low-order word of *lParam* specifies a scroll bar event.</span></span> <span data-ttu-id="ea709-113">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ea709-113">This parameter can be one of the following values.</span></span> <span data-ttu-id="ea709-114">Le mot de poids fort de *lParam* spécifie la position actuelle de la case de défilement si le mot de poids faible de *lParam* est **SB \_ THUMBPOSITION**; sinon, le mot de poids fort n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="ea709-114">The high-order word of *lParam* specifies the current position of the scroll box if the low-order word of *lParam* is **SB\_THUMBPOSITION**; otherwise, the high-order word is not used.</span></span>



| <span data-ttu-id="ea709-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea709-115">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="ea709-116">Signification</span><span class="sxs-lookup"><span data-stu-id="ea709-116">Meaning</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="ea709-117"><dt>**SB \_ ENDSCROLL**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="ea709-117"><dt>**SB\_ENDSCROLL**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="ea709-118">Fin du défilement.</span><span class="sxs-lookup"><span data-stu-id="ea709-118">End scroll.</span></span><br/>                                                                            |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <span data-ttu-id="ea709-119"><dt>**SB \_**</dt> <dt>6</dt> à gauche</span><span class="sxs-lookup"><span data-stu-id="ea709-119"><dt>**SB\_LEFT**</dt> <dt>6</dt></span></span> </dl>                            | <span data-ttu-id="ea709-120">Faites défiler vers le haut à gauche.</span><span class="sxs-lookup"><span data-stu-id="ea709-120">Scroll to upper left.</span></span><br/>                                                                  |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <span data-ttu-id="ea709-121"><dt>**SB \_**</dt> <dt>7</dt> droits</span><span class="sxs-lookup"><span data-stu-id="ea709-121"><dt>**SB\_RIGHT**</dt> <dt>7</dt></span></span> </dl>                         | <span data-ttu-id="ea709-122">Faites défiler vers la droite.</span><span class="sxs-lookup"><span data-stu-id="ea709-122">Scroll to lower right.</span></span><br/>                                                                 |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <span data-ttu-id="ea709-123"><dt>**SB \_ LINELEFT**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ea709-123"><dt>**SB\_LINELEFT**</dt> <dt>0</dt></span></span> </dl>                | <span data-ttu-id="ea709-124">Fait défiler d’une unité vers la gauche.</span><span class="sxs-lookup"><span data-stu-id="ea709-124">Scrolls left by one unit.</span></span><br/>                                                              |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <span data-ttu-id="ea709-125"><dt>**SB \_ LINERIGHT**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ea709-125"><dt>**SB\_LINERIGHT**</dt> <dt>1</dt></span></span> </dl>             | <span data-ttu-id="ea709-126">Fait défiler vers la droite d’une unité.</span><span class="sxs-lookup"><span data-stu-id="ea709-126">Scrolls right by one unit.</span></span><br/>                                                             |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <span data-ttu-id="ea709-127"><dt>**SB \_ PAGELEFT**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ea709-127"><dt>**SB\_PAGELEFT**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="ea709-128">Fait défiler vers la gauche de la largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ea709-128">Scrolls left by the width of the window.</span></span><br/>                                               |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <span data-ttu-id="ea709-129"><dt>**SB \_ ÉPINGLÉE**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ea709-129"><dt>**SB\_PAGERIGHT**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="ea709-130">Fait défiler la largeur de la fenêtre vers la droite.</span><span class="sxs-lookup"><span data-stu-id="ea709-130">Scrolls right by the width of the window.</span></span><br/>                                              |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="ea709-131"><dt>**SB \_ THUMBPOSITION**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ea709-131"><dt>**SB\_THUMBPOSITION**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="ea709-132">Faites défiler jusqu’à position absolue.</span><span class="sxs-lookup"><span data-stu-id="ea709-132">Scroll to absolute position.</span></span> <span data-ttu-id="ea709-133">La position actuelle est spécifiée par le mot de poids fort.</span><span class="sxs-lookup"><span data-stu-id="ea709-133">The current position is specified by the high-order word.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea709-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea709-134">Return value</span></span>

<span data-ttu-id="ea709-135">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="ea709-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea709-136">Notes</span><span class="sxs-lookup"><span data-stu-id="ea709-136">Remarks</span></span>

<span data-ttu-id="ea709-137">Le propriétaire du presse-papiers peut utiliser la fonction [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) pour faire défiler l’image dans la fenêtre de la visionneuse du presse-papiers et invalider la région appropriée.</span><span class="sxs-lookup"><span data-stu-id="ea709-137">The clipboard owner can use the [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) function to scroll the image in the clipboard viewer window and invalidate the appropriate region.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea709-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea709-138">Requirements</span></span>



| <span data-ttu-id="ea709-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea709-139">Requirement</span></span> | <span data-ttu-id="ea709-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea709-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea709-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea709-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ea709-142">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea709-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ea709-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea709-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ea709-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea709-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ea709-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea709-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea709-146"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea709-146"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea709-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea709-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="ea709-148">**Référence**</span><span class="sxs-lookup"><span data-stu-id="ea709-148">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="ea709-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ea709-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="ea709-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ea709-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="ea709-151">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="ea709-151">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ea709-152">Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="ea709-152">Clipboard</span></span>](clipboard.md)
</dt> <dt>

<span data-ttu-id="ea709-153">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="ea709-153">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="ea709-154">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="ea709-154">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span></span>
</dt> </dl>

 

