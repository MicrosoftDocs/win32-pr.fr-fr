---
description: Définit la police qu’un contrôle doit utiliser pour dessiner du texte.
ms.assetid: 7db6b8af-dbec-4c29-8bf7-d7e95d9813c3
title: Message WM_SETFONT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fc334e6b8c937759555c471f00ec56254a629c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952058"
---
# <a name="wm_setfont-message"></a><span data-ttu-id="9c5ae-103">\_Message WM SetFont</span><span class="sxs-lookup"><span data-stu-id="9c5ae-103">WM\_SETFONT message</span></span>

<span data-ttu-id="9c5ae-104">Définit la police qu’un contrôle doit utiliser pour dessiner du texte.</span><span class="sxs-lookup"><span data-stu-id="9c5ae-104">Sets the font that a control is to use when drawing text.</span></span>


```C++
#define WM_SETFONT                      0x0030
```



## <a name="parameters"></a><span data-ttu-id="9c5ae-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c5ae-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c5ae-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c5ae-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c5ae-107">Handle de la police (**Hfont**).</span><span class="sxs-lookup"><span data-stu-id="9c5ae-107">A handle to the font (**HFONT**).</span></span> <span data-ttu-id="9c5ae-108">Si ce paramètre a la **valeur null**, le contrôle utilise la police système par défaut pour dessiner du texte.</span><span class="sxs-lookup"><span data-stu-id="9c5ae-108">If this parameter is **NULL**, the control uses the default system font to draw text.</span></span>

</dd> <dt>

<span data-ttu-id="9c5ae-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c5ae-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c5ae-110">Le mot de poids faible de *lParam* spécifie si le contrôle doit être redessiné immédiatement lors de la définition de la police.</span><span class="sxs-lookup"><span data-stu-id="9c5ae-110">The low-order word of *lParam* specifies whether the control should be redrawn immediately upon setting the font.</span></span> <span data-ttu-id="9c5ae-111">Si ce paramètre a la **valeur true**, le contrôle se redessine lui-même.</span><span class="sxs-lookup"><span data-stu-id="9c5ae-111">If this parameter is **TRUE**, the control redraws itself.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c5ae-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9c5ae-112">Return value</span></span>

<span data-ttu-id="9c5ae-113">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="9c5ae-113">Type: **LRESULT**</span></span>

<span data-ttu-id="9c5ae-114">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9c5ae-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c5ae-115">Notes</span><span class="sxs-lookup"><span data-stu-id="9c5ae-115">Remarks</span></span>

<span data-ttu-id="9c5ae-116">Le message **WM \_ SetFont** s’applique à tous les contrôles, pas seulement à ceux des boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="9c5ae-116">The **WM\_SETFONT** message applies to all controls, not just those in dialog boxes.</span></span>

<span data-ttu-id="9c5ae-117">Le meilleur moment pour le propriétaire d’un contrôle de boîte de dialogue de définir la police du contrôle est lorsqu’il reçoit le message [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="9c5ae-117">The best time for the owner of a dialog box control to set the font of the control is when it receives the [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md) message.</span></span> <span data-ttu-id="9c5ae-118">L’application doit appeler la fonction [**SupprimerObjet**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) pour supprimer la police lorsqu’elle n’est plus nécessaire. par exemple, après avoir détruit le contrôle.</span><span class="sxs-lookup"><span data-stu-id="9c5ae-118">The application should call the [**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) function to delete the font when it is no longer needed; for example, after it destroys the control.</span></span>

<span data-ttu-id="9c5ae-119">La taille du contrôle ne change pas suite à la réception de ce message.</span><span class="sxs-lookup"><span data-stu-id="9c5ae-119">The size of the control does not change as a result of receiving this message.</span></span> <span data-ttu-id="9c5ae-120">Pour éviter le découpage du texte qui ne tient pas dans les limites du contrôle, l’application doit corriger la taille de la fenêtre de contrôle avant de définir la police.</span><span class="sxs-lookup"><span data-stu-id="9c5ae-120">To avoid clipping text that does not fit within the boundaries of the control, the application should correct the size of the control window before it sets the font.</span></span>

<span data-ttu-id="9c5ae-121">Quand une boîte de dialogue utilise le style [DS \_ SetFont](../dlgbox/about-dialog-boxes.md) pour définir le texte dans ses contrôles, le système envoie le message **WM \_ SetFont** à la procédure de boîte de dialogue avant de créer les contrôles.</span><span class="sxs-lookup"><span data-stu-id="9c5ae-121">When a dialog box uses the [DS\_SETFONT](../dlgbox/about-dialog-boxes.md) style to set the text in its controls, the system sends the **WM\_SETFONT** message to the dialog box procedure before it creates the controls.</span></span> <span data-ttu-id="9c5ae-122">Une application peut créer une boîte de dialogue qui contient le \_ style DS SetFont en appelant l’une des fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="9c5ae-122">An application can create a dialog box that contains the DS\_SETFONT style by calling any of the following functions:</span></span>

-   [<span data-ttu-id="9c5ae-123">**CreateDialogIndirect**</span><span class="sxs-lookup"><span data-stu-id="9c5ae-123">**CreateDialogIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
-   [<span data-ttu-id="9c5ae-124">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="9c5ae-124">**CreateDialogIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
-   [<span data-ttu-id="9c5ae-125">**DialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="9c5ae-125">**DialogBoxIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
-   [<span data-ttu-id="9c5ae-126">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="9c5ae-126">**DialogBoxIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)

## <a name="requirements"></a><span data-ttu-id="9c5ae-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c5ae-127">Requirements</span></span>



| <span data-ttu-id="9c5ae-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c5ae-128">Requirement</span></span> | <span data-ttu-id="9c5ae-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c5ae-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c5ae-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c5ae-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9c5ae-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c5ae-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9c5ae-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c5ae-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9c5ae-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c5ae-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9c5ae-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="9c5ae-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c5ae-135"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c5ae-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c5ae-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c5ae-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="9c5ae-137">**Référence**</span><span class="sxs-lookup"><span data-stu-id="9c5ae-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9c5ae-138">**CreateDialogIndirect**</span><span class="sxs-lookup"><span data-stu-id="9c5ae-138">**CreateDialogIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[<span data-ttu-id="9c5ae-139">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="9c5ae-139">**CreateDialogIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="9c5ae-140">**DialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="9c5ae-140">**DialogBoxIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[<span data-ttu-id="9c5ae-141">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="9c5ae-141">**DialogBoxIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="9c5ae-142">**DLGTEMPLATE**</span><span class="sxs-lookup"><span data-stu-id="9c5ae-142">**DLGTEMPLATE**</span></span>](/windows/win32/api/winuser/ns-winuser-dlgtemplate)
</dt> <dt>

[<span data-ttu-id="9c5ae-143">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="9c5ae-143">**MAKELPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[<span data-ttu-id="9c5ae-144">**WM \_ GETFONT**</span><span class="sxs-lookup"><span data-stu-id="9c5ae-144">**WM\_GETFONT**</span></span>](wm-getfont.md)
</dt> <dt>

[<span data-ttu-id="9c5ae-145">**\_INITDIALOG WM**</span><span class="sxs-lookup"><span data-stu-id="9c5ae-145">**WM\_INITDIALOG**</span></span>](../dlgbox/wm-initdialog.md)
</dt> <dt>

<span data-ttu-id="9c5ae-146">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="9c5ae-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9c5ae-147">Windows</span><span class="sxs-lookup"><span data-stu-id="9c5ae-147">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="9c5ae-148">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="9c5ae-148">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="9c5ae-149">**DeleteObject**</span><span class="sxs-lookup"><span data-stu-id="9c5ae-149">**DeleteObject**</span></span>](/windows/win32/api/wingdi/nf-wingdi-deleteobject)
</dt> </dl>

 

 
