---
title: Code de notification EN_MSGFILTER (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle d’édition enrichi d’un événement de clavier ou de souris dans le contrôle. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: 96cf0047-baae-46cd-82e8-ab6f3f353260
keywords:
- Contrôles Windows de code de notification EN_MSGFILTER
topic_type:
- apiref
api_name:
- EN_MSGFILTER
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40ddb3e9b1d5314e2e981b00f0e0ef8e22974242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103930"
---
# <a name="en_msgfilter-notification-code"></a><span data-ttu-id="7c9ec-105">\_Code de notification en msgfilter</span><span class="sxs-lookup"><span data-stu-id="7c9ec-105">EN\_MSGFILTER notification code</span></span>

<span data-ttu-id="7c9ec-106">Avertit une fenêtre parente d’un contrôle d’édition enrichi d’un événement de clavier ou de souris dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="7c9ec-106">Notifies a rich edit control's parent window of a keyboard or mouse event in the control.</span></span> <span data-ttu-id="7c9ec-107">Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7c9ec-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_MSGFILTER

    pMsgFilter = (MSGFILTER *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="7c9ec-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c9ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c9ec-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c9ec-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c9ec-110">Structure [**msgfilter**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) contenant des informations sur le clavier ou le message de la souris.</span><span class="sxs-lookup"><span data-stu-id="7c9ec-110">A [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) structure containing information about the keyboard or mouse message.</span></span> <span data-ttu-id="7c9ec-111">Si la fenêtre parente modifie cette structure et retourne une valeur différente de zéro, le message modifié est traité à la place de celui d’origine.</span><span class="sxs-lookup"><span data-stu-id="7c9ec-111">If the parent window modifies this structure and returns a nonzero value, the modified message is processed instead of the original one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c9ec-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7c9ec-112">Return value</span></span>

<span data-ttu-id="7c9ec-113">Retourne zéro si le contrôle doit traiter l’événement de clavier ou de souris.</span><span class="sxs-lookup"><span data-stu-id="7c9ec-113">Return zero if the control should process the keyboard or mouse event.</span></span>

<span data-ttu-id="7c9ec-114">Retourne une valeur différente de zéro si le contrôle doit ignorer l’événement du clavier ou de la souris.</span><span class="sxs-lookup"><span data-stu-id="7c9ec-114">Return nonzero if the control should ignore the keyboard or mouse event.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c9ec-115">Notes</span><span class="sxs-lookup"><span data-stu-id="7c9ec-115">Remarks</span></span>

<span data-ttu-id="7c9ec-116">Pour recevoir les \_ codes de notification en msgfilter pour les événements, spécifiez un ou plusieurs des indicateurs suivants dans le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="7c9ec-116">To receive EN\_MSGFILTER notification codes for events, specify one or more of the following flags in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>



| <span data-ttu-id="7c9ec-117">Indicateur</span><span class="sxs-lookup"><span data-stu-id="7c9ec-117">Flag</span></span>                                                                             | <span data-ttu-id="7c9ec-118">Signification</span><span class="sxs-lookup"><span data-stu-id="7c9ec-118">Meaning</span></span>                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="7c9ec-119">**\_événements ENM**</span><span class="sxs-lookup"><span data-stu-id="7c9ec-119">**ENM\_KEYEVENTS**</span></span>](rich-edit-control-event-mask-flags.md)       | <span data-ttu-id="7c9ec-120">Pour recevoir des codes de notification pour les événements de clavier.</span><span class="sxs-lookup"><span data-stu-id="7c9ec-120">To receive notification codes for keyboard events.</span></span>     |
| [<span data-ttu-id="7c9ec-121">**ENM \_ MOUSEEVENTS**</span><span class="sxs-lookup"><span data-stu-id="7c9ec-121">**ENM\_MOUSEEVENTS**</span></span>](rich-edit-control-event-mask-flags.md)   | <span data-ttu-id="7c9ec-122">Pour recevoir des codes de notification pour les événements de souris.</span><span class="sxs-lookup"><span data-stu-id="7c9ec-122">To receive notification codes for mouse events.</span></span>        |
| [<span data-ttu-id="7c9ec-123">**ENM \_ SCROLLEVENTS**</span><span class="sxs-lookup"><span data-stu-id="7c9ec-123">**ENM\_SCROLLEVENTS**</span></span>](rich-edit-control-event-mask-flags.md) | <span data-ttu-id="7c9ec-124">Pour recevoir des codes de notification pour un événement de roulette de la souris.</span><span class="sxs-lookup"><span data-stu-id="7c9ec-124">To receive notification codes for a mouse wheel event.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="7c9ec-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c9ec-125">Requirements</span></span>



| <span data-ttu-id="7c9ec-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c9ec-126">Requirement</span></span> | <span data-ttu-id="7c9ec-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c9ec-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c9ec-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c9ec-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7c9ec-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c9ec-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7c9ec-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c9ec-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7c9ec-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c9ec-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c9ec-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c9ec-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c9ec-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c9ec-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c9ec-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c9ec-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="7c9ec-135">**Référence**</span><span class="sxs-lookup"><span data-stu-id="7c9ec-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7c9ec-136">**MSGFILTER**</span><span class="sxs-lookup"><span data-stu-id="7c9ec-136">**MSGFILTER**</span></span>](/windows/desktop/api/Richedit/ns-richedit-msgfilter)
</dt> <dt>

[<span data-ttu-id="7c9ec-137">**\_notification WM**</span><span class="sxs-lookup"><span data-stu-id="7c9ec-137">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





