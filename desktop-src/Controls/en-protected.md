---
title: Code de notification EN_PROTECTED (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle RichEdit que l’utilisateur effectue une action qui modifie une plage de texte protégée. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: 29c0cb51-675c-44b1-ad45-5f7140ca5675
keywords:
- Contrôles Windows de code de notification EN_PROTECTED
topic_type:
- apiref
api_name:
- EN_PROTECTED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1475053366a06f46b0c99514ade961f1a2998b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465482"
---
# <a name="en_protected-notification-code"></a><span data-ttu-id="e283b-105">\_Code de notification en code protégé</span><span class="sxs-lookup"><span data-stu-id="e283b-105">EN\_PROTECTED notification code</span></span>

<span data-ttu-id="e283b-106">Avertit une fenêtre parente d’un contrôle RichEdit que l’utilisateur effectue une action qui modifie une plage de texte protégée.</span><span class="sxs-lookup"><span data-stu-id="e283b-106">Notifies a rich edit control's parent window that the user is taking an action that would change a protected range of text.</span></span> <span data-ttu-id="e283b-107">Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e283b-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_PROTECTED

    penProtected = (ENPROTECTED *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e283b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e283b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e283b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e283b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e283b-110">Structure [**protégée**](/windows/desktop/api/Richedit/ns-richedit-enprotected) contenant des informations sur le message qui a déclenché le code de notification.</span><span class="sxs-lookup"><span data-stu-id="e283b-110">An [**ENPROTECTED**](/windows/desktop/api/Richedit/ns-richedit-enprotected) structure containing information about the message that triggered the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e283b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e283b-111">Return value</span></span>

<span data-ttu-id="e283b-112">Retournez zéro pour permettre l’opération.</span><span class="sxs-lookup"><span data-stu-id="e283b-112">Return zero to allow the operation.</span></span>

<span data-ttu-id="e283b-113">Retournez une valeur différente de zéro pour empêcher l’opération.</span><span class="sxs-lookup"><span data-stu-id="e283b-113">Return a nonzero value to prevent the operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="e283b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e283b-114">Remarks</span></span>

<span data-ttu-id="e283b-115">Si la valeur zéro est retournée et que les membres **MSG**, **wParam** et **lParam** de la structure [**protégée**](/windows/desktop/api/Richedit/ns-richedit-enprotected) sont modifiés, le contrôle traite le message révisé à la place du message d’origine.</span><span class="sxs-lookup"><span data-stu-id="e283b-115">If zero is returned and the **msg**, **wParam**, and **lParam** members of the [**ENPROTECTED**](/windows/desktop/api/Richedit/ns-richedit-enprotected) structure are changed, the control processes the revised message instead of the original message.</span></span>

<span data-ttu-id="e283b-116">Pour recevoir des \_ codes de notification en protection, spécifiez [**ENM \_ protected**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="e283b-116">To receive EN\_PROTECTED notification codes, specify [**ENM\_PROTECTED**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e283b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e283b-117">Requirements</span></span>



| <span data-ttu-id="e283b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e283b-118">Requirement</span></span> | <span data-ttu-id="e283b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e283b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e283b-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e283b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e283b-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e283b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e283b-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e283b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e283b-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e283b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e283b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e283b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e283b-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e283b-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e283b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e283b-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="e283b-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="e283b-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e283b-128">**PROTÉGÉ**</span><span class="sxs-lookup"><span data-stu-id="e283b-128">**ENPROTECTED**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enprotected)
</dt> <dt>

[<span data-ttu-id="e283b-129">**\_notification WM**</span><span class="sxs-lookup"><span data-stu-id="e283b-129">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





