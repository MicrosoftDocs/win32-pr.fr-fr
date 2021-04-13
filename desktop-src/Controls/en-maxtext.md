---
title: EN_MAXTEXT le code de notification (winuser. h)
description: Envoyé lorsque l’insertion de texte actuelle a dépassé le nombre spécifié de caractères pour le contrôle d’édition.
ms.assetid: b03835d6-d06f-415a-97f2-d2b62b17e175
keywords:
- Contrôles Windows de code de notification EN_MAXTEXT
topic_type:
- apiref
api_name:
- EN_MAXTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 454b48fb232f2225696efacc44d54660d3a83185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509162"
---
# <a name="en_maxtext-notification-code"></a><span data-ttu-id="ddfc4-104">\_Code de notification en MAXTEXT</span><span class="sxs-lookup"><span data-stu-id="ddfc4-104">EN\_MAXTEXT notification code</span></span>

<span data-ttu-id="ddfc4-105">Envoyé lorsque l’insertion de texte actuelle a dépassé le nombre spécifié de caractères pour le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="ddfc4-105">Sent when the current text insertion has exceeded the specified number of characters for the edit control.</span></span> <span data-ttu-id="ddfc4-106">L’insertion de texte a été tronquée.</span><span class="sxs-lookup"><span data-stu-id="ddfc4-106">The text insertion has been truncated.</span></span>

<span data-ttu-id="ddfc4-107">Ce code de notification est également envoyé lorsqu’un contrôle d’édition n’a pas le style [**es \_ AUTOHSCROLL**](edit-control-styles.md) et que le nombre de caractères à insérer dépasse la largeur du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="ddfc4-107">This notification code is also sent when an edit control does not have the [**ES\_AUTOHSCROLL**](edit-control-styles.md) style and the number of characters to be inserted would exceed the width of the edit control.</span></span>

<span data-ttu-id="ddfc4-108">Ce code de notification est également envoyé lorsqu’un contrôle d’édition n’a pas le style [**es \_ AUTOVSCROLL**](edit-control-styles.md) et que le nombre total de lignes résultant d’une insertion de texte dépasse la hauteur du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="ddfc4-108">This notification code is also sent when an edit control does not have the [**ES\_AUTOVSCROLL**](edit-control-styles.md) style and the total number of lines resulting from a text insertion would exceed the height of the edit control.</span></span>

<span data-ttu-id="ddfc4-109">La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="ddfc4-109">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_MAXTEXT

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="ddfc4-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ddfc4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddfc4-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ddfc4-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ddfc4-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="ddfc4-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="ddfc4-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="ddfc4-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="ddfc4-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ddfc4-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ddfc4-115">Handle du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="ddfc4-115">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ddfc4-116">Notes</span><span class="sxs-lookup"><span data-stu-id="ddfc4-116">Remarks</span></span>

<span data-ttu-id="ddfc4-117">La fenêtre parente reçoit toujours un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) pour cet événement, elle ne nécessite pas de masque de notification envoyé avec [**em \_ SETEVENTMASK**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="ddfc4-117">The parent window always receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

<span data-ttu-id="ddfc4-118">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ddfc4-118">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="ddfc4-119">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="ddfc4-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ddfc4-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ddfc4-120">Requirements</span></span>



| <span data-ttu-id="ddfc4-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ddfc4-121">Requirement</span></span> | <span data-ttu-id="ddfc4-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddfc4-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddfc4-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddfc4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ddfc4-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ddfc4-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ddfc4-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddfc4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ddfc4-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ddfc4-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ddfc4-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="ddfc4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddfc4-128"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ddfc4-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddfc4-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddfc4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddfc4-130">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="ddfc4-130">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

