---
title: EN_HSCROLL le code de notification (winuser. h)
description: Envoyé lorsque l’utilisateur clique sur la barre de défilement horizontale d’un contrôle d’édition. La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un \_ message de commande WM. La fenêtre parente est avertie avant la mise à jour de l’écran.
ms.assetid: beaaa80c-4108-4a8e-aed8-04c9a3a08f3e
keywords:
- Contrôles Windows de code de notification EN_HSCROLL
topic_type:
- apiref
api_name:
- EN_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f90f6e781409419e39390e64251506b4cc915a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843798"
---
# <a name="en_hscroll-notification-code"></a><span data-ttu-id="e22ba-106">\_Code de notification en HSCROLL</span><span class="sxs-lookup"><span data-stu-id="e22ba-106">EN\_HSCROLL notification code</span></span>

<span data-ttu-id="e22ba-107">Envoyé lorsque l’utilisateur clique sur la barre de défilement horizontale d’un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="e22ba-107">Sent when the user clicks an edit control's horizontal scroll bar.</span></span> <span data-ttu-id="e22ba-108">La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="e22ba-108">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="e22ba-109">La fenêtre parente est avertie avant la mise à jour de l’écran.</span><span class="sxs-lookup"><span data-stu-id="e22ba-109">The parent window is notified before the screen is updated.</span></span>


```C++
EN_HSCROLL

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="e22ba-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e22ba-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e22ba-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e22ba-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e22ba-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="e22ba-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="e22ba-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="e22ba-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="e22ba-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e22ba-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e22ba-115">Handle du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="e22ba-115">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e22ba-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e22ba-116">Remarks</span></span>

<span data-ttu-id="e22ba-117">Ce code de notification est envoyé pour les événements de souris suivants sur la barre de défilement horizontale : cliquez sur le bouton fléché ou cliquez entre le bouton fléché et le curseur.</span><span class="sxs-lookup"><span data-stu-id="e22ba-117">This notification code is sent for the following mouse events on the horizontal scroll bar: clicking either arrow button or clicking between the arrow button and the thumb.</span></span> <span data-ttu-id="e22ba-118">Toutefois, le code de notification n’est pas envoyé quand vous cliquez sur le curseur de la barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="e22ba-118">However, the notification code is not sent when clicking the scroll bar thumb itself.</span></span> <span data-ttu-id="e22ba-119">Le code de notification est également envoyé lorsqu’un événement de clavier provoque une modification dans la zone d’affichage du contrôle d’édition, par exemple en appuyant sur origine, fin, flèche gauche ou flèche droite.</span><span class="sxs-lookup"><span data-stu-id="e22ba-119">The notification code is also sent when a keyboard event causes a change in the view area of the edit control, for example, pressing HOME, END, LEFT ARROW, or RIGHT ARROW.</span></span>

<span data-ttu-id="e22ba-120">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e22ba-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="e22ba-121">Pour recevoir les codes de notification en **\_ HSCROLL** , spécifiez [**ENM \_ faites défiler**](rich-edit-control-event-mask-flags.md) le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="e22ba-121">To receive **EN\_HSCROLL** notification codes, specify [**ENM\_SCROLL**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="e22ba-122">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="e22ba-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e22ba-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e22ba-123">Requirements</span></span>



| <span data-ttu-id="e22ba-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e22ba-124">Requirement</span></span> | <span data-ttu-id="e22ba-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e22ba-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e22ba-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e22ba-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e22ba-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e22ba-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e22ba-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e22ba-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e22ba-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e22ba-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e22ba-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="e22ba-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e22ba-131"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e22ba-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e22ba-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e22ba-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="e22ba-133">**Référence**</span><span class="sxs-lookup"><span data-stu-id="e22ba-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e22ba-134">en \_ VSCROLL</span><span class="sxs-lookup"><span data-stu-id="e22ba-134">EN\_VSCROLL</span></span>](en-vscroll.md)
</dt> <dt>

<span data-ttu-id="e22ba-135">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="e22ba-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e22ba-136">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="e22ba-136">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

