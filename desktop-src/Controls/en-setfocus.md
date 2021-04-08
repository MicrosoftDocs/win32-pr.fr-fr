---
title: EN_SETFOCUS le code de notification (winuser. h)
description: Envoyé lorsqu’un contrôle d’édition reçoit le focus clavier. La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un \_ message de commande WM.
ms.assetid: 482d2afa-4e21-4f3f-bdf4-6966b34cc3c4
keywords:
- Contrôles Windows de code de notification EN_SETFOCUS
topic_type:
- apiref
api_name:
- EN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cb96482f0e42669658dde3a39637e3c2311619
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743036"
---
# <a name="en_setfocus-notification-code"></a><span data-ttu-id="7507d-105">\_Code de notification en SetFocus</span><span class="sxs-lookup"><span data-stu-id="7507d-105">EN\_SETFOCUS notification code</span></span>

<span data-ttu-id="7507d-106">Envoyé lorsqu’un contrôle d’édition reçoit le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="7507d-106">Sent when an edit control receives the keyboard focus.</span></span> <span data-ttu-id="7507d-107">La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="7507d-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="7507d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7507d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7507d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7507d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7507d-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="7507d-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="7507d-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="7507d-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="7507d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7507d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7507d-113">Handle du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="7507d-113">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7507d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7507d-114">Remarks</span></span>

<span data-ttu-id="7507d-115">La fenêtre parente reçoit toujours un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) pour cet événement, elle ne nécessite pas de masque de notification envoyé avec [**em \_ SETEVENTMASK**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="7507d-115">The parent window always receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

<span data-ttu-id="7507d-116">**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7507d-116">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="7507d-117">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="7507d-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7507d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7507d-118">Requirements</span></span>



| <span data-ttu-id="7507d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7507d-119">Requirement</span></span> | <span data-ttu-id="7507d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="7507d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7507d-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7507d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7507d-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7507d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7507d-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7507d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7507d-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7507d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7507d-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="7507d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7507d-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7507d-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7507d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7507d-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="7507d-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="7507d-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7507d-129">en \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="7507d-129">EN\_KILLFOCUS</span></span>](en-killfocus.md)
</dt> <dt>

<span data-ttu-id="7507d-130">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="7507d-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="7507d-131">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="7507d-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

