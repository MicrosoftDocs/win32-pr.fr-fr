---
title: Code de notification EN_STOPNOUNDO (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle RichEdit qu’une action s’est produite pour laquelle le contrôle ne peut pas allouer suffisamment de mémoire pour maintenir l’état d’annulation. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: 5608f6dd-83dc-4712-b485-dd9bc17dea24
keywords:
- Contrôles Windows de code de notification EN_STOPNOUNDO
topic_type:
- apiref
api_name:
- EN_STOPNOUNDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab71e6e1a78c468e6349fc1f42d03e9b68fb043
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105547"
---
# <a name="en_stopnoundo-notification-code"></a><span data-ttu-id="ddd1f-105">\_Code de notification en STOPNOUNDO</span><span class="sxs-lookup"><span data-stu-id="ddd1f-105">EN\_STOPNOUNDO notification code</span></span>

<span data-ttu-id="ddd1f-106">Avertit une fenêtre parente d’un contrôle RichEdit qu’une action s’est produite pour laquelle le contrôle ne peut pas allouer suffisamment de mémoire pour maintenir l’état d’annulation.</span><span class="sxs-lookup"><span data-stu-id="ddd1f-106">Notifies a rich edit control's parent window that an action occurred for which the control cannot allocate enough memory to maintain the undo state.</span></span> <span data-ttu-id="ddd1f-107">Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ddd1f-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_STOPNOUNDO

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ddd1f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ddd1f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddd1f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ddd1f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ddd1f-110">Structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="ddd1f-110">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddd1f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ddd1f-111">Return value</span></span>

<span data-ttu-id="ddd1f-112">Retournez zéro pour poursuivre l’opération d' **annulation** .</span><span class="sxs-lookup"><span data-stu-id="ddd1f-112">Return zero to continue the **Undo** operation.</span></span>

<span data-ttu-id="ddd1f-113">Retourne une valeur différente de zéro pour arrêter l’opération d' **annulation** .</span><span class="sxs-lookup"><span data-stu-id="ddd1f-113">Return a nonzero value to stop the **Undo** operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddd1f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ddd1f-114">Remarks</span></span>

<span data-ttu-id="ddd1f-115">La fenêtre parente reçoit toujours un [**message \_ de notification WM**](wm-notify.md) pour cet événement, elle ne nécessite pas de masque de notification envoyé avec [**em \_ SETEVENTMASK**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="ddd1f-115">The parent window will always get a [**WM\_NOTIFY**](wm-notify.md) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ddd1f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ddd1f-116">Requirements</span></span>



| <span data-ttu-id="ddd1f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ddd1f-117">Requirement</span></span> | <span data-ttu-id="ddd1f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddd1f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ddd1f-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddd1f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ddd1f-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ddd1f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ddd1f-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddd1f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ddd1f-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ddd1f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ddd1f-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="ddd1f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddd1f-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddd1f-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddd1f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddd1f-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="ddd1f-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="ddd1f-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ddd1f-127">**NMHDR**</span><span class="sxs-lookup"><span data-stu-id="ddd1f-127">**NMHDR**</span></span>](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> <dt>

[<span data-ttu-id="ddd1f-128">**\_notification WM**</span><span class="sxs-lookup"><span data-stu-id="ddd1f-128">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





