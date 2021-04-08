---
title: EN_VSCROLL le code de notification (winuser. h)
description: Envoyé lorsque l’utilisateur clique sur la barre de défilement verticale d’un contrôle d’édition ou lorsque l’utilisateur fait défiler la roulette de la souris au-dessus du contrôle d’édition.
ms.assetid: 46307dee-3c5c-4020-9c2b-ec4638a0cea5
keywords:
- Contrôles Windows de code de notification EN_VSCROLL
topic_type:
- apiref
api_name:
- EN_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1f99b9ea05d037b5c00562a24bda1e434ce08d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844342"
---
# <a name="en_vscroll-notification-code"></a><span data-ttu-id="ab280-104">\_Code de notification en VSCROLL</span><span class="sxs-lookup"><span data-stu-id="ab280-104">EN\_VSCROLL notification code</span></span>

<span data-ttu-id="ab280-105">Envoyé lorsque l’utilisateur clique sur la barre de défilement verticale d’un contrôle d’édition ou lorsque l’utilisateur fait défiler la roulette de la souris au-dessus du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="ab280-105">Sent when the user clicks an edit control's vertical scroll bar or when the user scrolls the mouse wheel over the edit control.</span></span> <span data-ttu-id="ab280-106">La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="ab280-106">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="ab280-107">La fenêtre parente est avertie avant la mise à jour de l’écran.</span><span class="sxs-lookup"><span data-stu-id="ab280-107">The parent window is notified before the screen is updated.</span></span>


```C++
EN_VSCROLL

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="ab280-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab280-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab280-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ab280-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab280-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="ab280-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="ab280-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="ab280-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="ab280-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ab280-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab280-113">Handle du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="ab280-113">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab280-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ab280-114">Remarks</span></span>

<span data-ttu-id="ab280-115">Ce message est envoyé pour les événements de souris suivants sur la barre de défilement verticale : cliquez sur le bouton fléché ou cliquez entre le bouton fléché et le curseur.</span><span class="sxs-lookup"><span data-stu-id="ab280-115">This message is sent for the following mouse events on the vertical scroll bar: clicking either arrow button or clicking between the arrow button and the thumb.</span></span> <span data-ttu-id="ab280-116">Toutefois, le message n’est pas envoyé quand vous cliquez sur la souris de la barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="ab280-116">However, the message is not sent when clicking the scroll bar mouse itself.</span></span> <span data-ttu-id="ab280-117">Le message est également envoyé lorsqu’un événement de clavier provoque une modification dans la zone d’affichage du contrôle d’édition, par exemple en appuyant sur origine, fin, PAGE précédente, PAGE suivante, flèche haut ou flèche bas.</span><span class="sxs-lookup"><span data-stu-id="ab280-117">The message is also sent when a keyboard event causes a change in the view area of the edit control, for example, pressing HOME, END, PAGE UP, PAGE DOWN, UP ARROW, or DOWN ARROW.</span></span>

<span data-ttu-id="ab280-118">La roulette de la souris est une souris dotée d’une roulette centrale qui défile.</span><span class="sxs-lookup"><span data-stu-id="ab280-118">The mouse wheel is a mouse that has a center wheel that scrolls.</span></span> <span data-ttu-id="ab280-119">Pour plus d’informations, consultez « la roulette de la souris » dans [à propos de l’entrée de la souris](/windows/desktop/inputdev/about-mouse-input).</span><span class="sxs-lookup"><span data-stu-id="ab280-119">For more information, see "The Mouse Wheel" in [About Mouse Input](/windows/desktop/inputdev/about-mouse-input).</span></span>

<span data-ttu-id="ab280-120">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ab280-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="ab280-121">Pour recevoir \_ les codes de notification en VSCROLL, spécifiez [**ENM \_ faites défiler**](rich-edit-control-event-mask-flags.md) le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="ab280-121">To receive EN\_VSCROLL notification codes, specify [**ENM\_SCROLL**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="ab280-122">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="ab280-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab280-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab280-123">Requirements</span></span>



| <span data-ttu-id="ab280-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab280-124">Requirement</span></span> | <span data-ttu-id="ab280-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab280-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab280-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab280-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ab280-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab280-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ab280-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab280-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ab280-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab280-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ab280-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab280-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab280-131"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab280-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab280-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab280-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="ab280-133">**Référence**</span><span class="sxs-lookup"><span data-stu-id="ab280-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ab280-134">en \_ HSCROLL</span><span class="sxs-lookup"><span data-stu-id="ab280-134">EN\_HSCROLL</span></span>](en-hscroll.md)
</dt> <dt>

<span data-ttu-id="ab280-135">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="ab280-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ab280-136">Utilisation des contrôles d’édition</span><span class="sxs-lookup"><span data-stu-id="ab280-136">Using Edit Controls</span></span>](using-edit-controls.md)
</dt> <dt>

<span data-ttu-id="ab280-137">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="ab280-137">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="ab280-138">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="ab280-138">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

