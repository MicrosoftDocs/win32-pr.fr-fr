---
title: Code de notification EN_LOWFIRTF (RichEdit. h)
description: Notifie la fenêtre parente d’un contrôle Rich Edit Microsoft qu’un mot clé RTF (Rich Text Format) non pris en charge a été reçu. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: 3b18320b-ebc3-44f2-a93c-e967a028c522
keywords:
- Contrôles Windows de code de notification EN_LOWFIRTF
topic_type:
- apiref
api_name:
- EN_LOWFIRTF
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e74a6e5dada471fdd8364b34bf2ed1b4da7f2314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509165"
---
# <a name="en_lowfirtf-notification-code"></a><span data-ttu-id="b45ac-105">\_Code de notification en LOWFIRTF</span><span class="sxs-lookup"><span data-stu-id="b45ac-105">EN\_LOWFIRTF notification code</span></span>

<span data-ttu-id="b45ac-106">Notifie la fenêtre parente d’un contrôle Rich Edit Microsoft qu’un mot clé RTF (Rich Text Format) non pris en charge a été reçu.</span><span class="sxs-lookup"><span data-stu-id="b45ac-106">Notifies the parent window of a Microsoft Rich Edit control that an unsupported Rich Text Format (RTF) keyword was received.</span></span> <span data-ttu-id="b45ac-107">Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b45ac-107">A Rich Edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_LOWFIRTF

    penLowfiRTF = (ENLOWFIRTF *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b45ac-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b45ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b45ac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b45ac-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b45ac-110">Structure [**ENLOWFIRTF**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf) .</span><span class="sxs-lookup"><span data-stu-id="b45ac-110">The [**ENLOWFIRTF**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b45ac-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b45ac-111">Return value</span></span>

<span data-ttu-id="b45ac-112">Ce code de notification ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b45ac-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b45ac-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b45ac-113">Remarks</span></span>

<span data-ttu-id="b45ac-114">Pour recevoir une \_ notification en LOWFIRTF, spécifiez l' \_ indicateur ENM LOWFIRTF dans le masque envoyé avec le message [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="b45ac-114">To receive an EN\_LOWFIRTF notification, specify the ENM\_LOWFIRTF flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b45ac-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b45ac-115">Requirements</span></span>



| <span data-ttu-id="b45ac-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b45ac-116">Requirement</span></span> | <span data-ttu-id="b45ac-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b45ac-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b45ac-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b45ac-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b45ac-119">Windows XP avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b45ac-119">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b45ac-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b45ac-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b45ac-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b45ac-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b45ac-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b45ac-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b45ac-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b45ac-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b45ac-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b45ac-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="b45ac-125">**Référence**</span><span class="sxs-lookup"><span data-stu-id="b45ac-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b45ac-126">**ENLOWFIRTF**</span><span class="sxs-lookup"><span data-stu-id="b45ac-126">**ENLOWFIRTF**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)
</dt> <dt>

[<span data-ttu-id="b45ac-127">**\_notification WM**</span><span class="sxs-lookup"><span data-stu-id="b45ac-127">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





