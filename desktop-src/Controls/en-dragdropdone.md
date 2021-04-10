---
title: Code de notification EN_DRAGDROPDONE (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle RichEdit que l’opération de glisser-déplacer est terminée. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: 3c8b95cc-86ef-4aec-b551-11dca50ea5c5
keywords:
- Contrôles Windows de code de notification EN_DRAGDROPDONE
topic_type:
- apiref
api_name:
- EN_DRAGDROPDONE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a10b6718122791bcc862866fbaf17ed43e8bfd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941715"
---
# <a name="en_dragdropdone-notification-code"></a><span data-ttu-id="beb26-105">\_Code de notification en DRAGDROPDONE</span><span class="sxs-lookup"><span data-stu-id="beb26-105">EN\_DRAGDROPDONE notification code</span></span>

<span data-ttu-id="beb26-106">Avertit une fenêtre parente d’un contrôle RichEdit que l’opération de glisser-déplacer est terminée.</span><span class="sxs-lookup"><span data-stu-id="beb26-106">Notifies a rich edit control's parent window that the drag-and-drop operation has completed.</span></span> <span data-ttu-id="beb26-107">Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="beb26-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_DRAGDROPDONE

    pnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="beb26-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="beb26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beb26-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="beb26-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="beb26-110">Structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="beb26-110">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beb26-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="beb26-111">Return value</span></span>

<span data-ttu-id="beb26-112">Ce code de notification ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="beb26-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="beb26-113">Notes</span><span class="sxs-lookup"><span data-stu-id="beb26-113">Remarks</span></span>

<span data-ttu-id="beb26-114">Pour recevoir un \_ Code de notification en DRAGDROPDONE, spécifiez l’indicateur [**ENM \_ DRAGDROPDONE**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="beb26-114">To receive an EN\_DRAGDROPDONE notification code, specify the [**ENM\_DRAGDROPDONE**](rich-edit-control-event-mask-flags.md) flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="beb26-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="beb26-115">Requirements</span></span>



| <span data-ttu-id="beb26-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="beb26-116">Requirement</span></span> | <span data-ttu-id="beb26-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="beb26-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="beb26-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="beb26-118">Minimum supported client</span></span><br/> | <span data-ttu-id="beb26-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="beb26-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="beb26-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="beb26-120">Minimum supported server</span></span><br/> | <span data-ttu-id="beb26-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="beb26-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="beb26-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="beb26-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="beb26-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="beb26-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beb26-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="beb26-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="beb26-125">**Référence**</span><span class="sxs-lookup"><span data-stu-id="beb26-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="beb26-126">**EM \_ SETEVENTMASK**</span><span class="sxs-lookup"><span data-stu-id="beb26-126">**EM\_SETEVENTMASK**</span></span>](em-seteventmask.md)
</dt> </dl>

 

 





