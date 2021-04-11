---
title: Code de notification EN_REQUESTRESIZE (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle RichEdit que le contenu du contrôle est plus petit ou plus grand que la taille de la fenêtre du contrôle. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: 708c23b1-7b81-46f1-9595-46230693855d
keywords:
- Contrôles Windows de code de notification EN_REQUESTRESIZE
topic_type:
- apiref
api_name:
- EN_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60214d8902297eb7cd77ded481b0604929e7adb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104497"
---
# <a name="en_requestresize-notification-code"></a><span data-ttu-id="c15cd-105">\_Code de notification en REQUESTRESIZE</span><span class="sxs-lookup"><span data-stu-id="c15cd-105">EN\_REQUESTRESIZE notification code</span></span>

<span data-ttu-id="c15cd-106">Avertit une fenêtre parente d’un contrôle RichEdit que le contenu du contrôle est plus petit ou plus grand que la taille de la fenêtre du contrôle.</span><span class="sxs-lookup"><span data-stu-id="c15cd-106">Notifies a rich edit control's parent window that the control's contents are either smaller or larger than the control's window size.</span></span> <span data-ttu-id="c15cd-107">Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c15cd-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_REQUESTRESIZE

    pReqResize = (REQRESIZE *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c15cd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c15cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c15cd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c15cd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c15cd-110">Structure [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) qui reçoit la taille demandée.</span><span class="sxs-lookup"><span data-stu-id="c15cd-110">A [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) structure that receives the requested size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c15cd-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c15cd-111">Return value</span></span>

<span data-ttu-id="c15cd-112">Ce code de notification ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c15cd-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c15cd-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c15cd-113">Remarks</span></span>

<span data-ttu-id="c15cd-114">Pour prendre en charge le comportement sans fin d’un contrôle RichEdit, la fenêtre parente doit redimensionner le contrôle lorsqu’il reçoit ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="c15cd-114">To support the bottomless behavior of a rich edit control, the parent window must resize the control when it receives this notification code.</span></span>

<span data-ttu-id="c15cd-115">Pour recevoir les \_ codes de notification en REQUESTRESIZE, spécifiez [**ENM \_ REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="c15cd-115">To receive EN\_REQUESTRESIZE notification codes, specify [**ENM\_REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c15cd-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c15cd-116">Requirements</span></span>



| <span data-ttu-id="c15cd-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c15cd-117">Requirement</span></span> | <span data-ttu-id="c15cd-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c15cd-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c15cd-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c15cd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c15cd-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c15cd-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c15cd-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c15cd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c15cd-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c15cd-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c15cd-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c15cd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c15cd-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c15cd-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c15cd-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c15cd-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="c15cd-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="c15cd-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c15cd-127">**REQRESIZE**</span><span class="sxs-lookup"><span data-stu-id="c15cd-127">**REQRESIZE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-reqresize)
</dt> <dt>

[<span data-ttu-id="c15cd-128">**\_notification WM**</span><span class="sxs-lookup"><span data-stu-id="c15cd-128">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





