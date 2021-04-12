---
title: EN_UPDATE le code de notification (winuser. h)
description: Envoyé lorsqu’un contrôle d’édition va se redessiner lui-même.
ms.assetid: 59138736-6cc9-4a3f-95f3-ada9cbf253cb
keywords:
- Contrôles Windows de code de notification EN_UPDATE
topic_type:
- apiref
api_name:
- EN_UPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0b045efcfb5d50cb2a85c9ae230e215263aa2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105550"
---
# <a name="en_update-notification-code"></a><span data-ttu-id="f8998-104">Code de notification en cours de \_ mise à jour</span><span class="sxs-lookup"><span data-stu-id="f8998-104">EN\_UPDATE notification code</span></span>

<span data-ttu-id="f8998-105">Envoyé lorsqu’un contrôle d’édition va se redessiner lui-même.</span><span class="sxs-lookup"><span data-stu-id="f8998-105">Sent when an edit control is about to redraw itself.</span></span> <span data-ttu-id="f8998-106">Ce code de notification est envoyé une fois que le contrôle a mis en forme le texte, mais avant d’afficher le texte.</span><span class="sxs-lookup"><span data-stu-id="f8998-106">This notification code is sent after the control has formatted the text, but before it displays the text.</span></span> <span data-ttu-id="f8998-107">Vous pouvez ainsi redimensionner la fenêtre de contrôle d’édition, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f8998-107">This makes it possible to resize the edit control window, if necessary.</span></span> <span data-ttu-id="f8998-108">La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="f8998-108">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_UPDATE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="f8998-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8998-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8998-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8998-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8998-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="f8998-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="f8998-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="f8998-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="f8998-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8998-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8998-114">Handle du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="f8998-114">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8998-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f8998-115">Remarks</span></span>

<span data-ttu-id="f8998-116">**Édition enrichie 1,0 :** Pour recevoir des \_ codes de notification en mise à jour, spécifiez la [**\_ mise à jour ENM**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="f8998-116">**Rich Edit 1.0:** To receive EN\_UPDATE notification codes, specify [**ENM\_UPDATE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="f8998-117">**Édition enrichie 2,0 et versions ultérieures :** L’indicateur de [**\_ mise à jour ENM**](rich-edit-control-event-mask-flags.md) est ignoré.</span><span class="sxs-lookup"><span data-stu-id="f8998-117">**Rich Edit 2.0 and later:** The [**ENM\_UPDATE**](rich-edit-control-event-mask-flags.md) flag is ignored.</span></span> <span data-ttu-id="f8998-118">Le \_ Code de notification en mise à jour est toujours reçu.</span><span class="sxs-lookup"><span data-stu-id="f8998-118">The EN\_UPDATE notification code is always received.</span></span> <span data-ttu-id="f8998-119">Toutefois, lorsque Microsoft Rich Edit 3,0 émule Microsoft Rich Edit 1,0, pour recevoir \_ les codes de notification de mise à jour, vous devez spécifier **ENM \_ Update** dans le masque envoyé avec le message [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="f8998-119">However, when Microsoft Rich Edit 3.0 emulates Microsoft Rich Edit 1.0, to receive EN\_UPDATE notification codes you must specify **ENM\_UPDATE** in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="f8998-120">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="f8998-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8998-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8998-121">Requirements</span></span>



| <span data-ttu-id="f8998-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8998-122">Requirement</span></span> | <span data-ttu-id="f8998-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8998-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8998-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8998-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f8998-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8998-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f8998-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8998-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f8998-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8998-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f8998-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8998-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8998-129"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8998-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8998-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8998-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="f8998-131">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f8998-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f8998-132">en \_ modification</span><span class="sxs-lookup"><span data-stu-id="f8998-132">EN\_CHANGE</span></span>](en-change.md)
</dt> <dt>

<span data-ttu-id="f8998-133">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="f8998-133">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f8998-134">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="f8998-134">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

