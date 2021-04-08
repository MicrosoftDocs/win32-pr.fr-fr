---
title: Code de notification EN_OBJECTPOSITIONS (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle RichEdit quand le contrôle lit des objets. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: 1965185f-8a13-4989-8574-af8b9b30f6b0
keywords:
- Contrôles Windows de code de notification EN_OBJECTPOSITIONS
topic_type:
- apiref
api_name:
- EN_OBJECTPOSITIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35681f6734457eb6b6ebcac1bcb67227cbd3b9e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843678"
---
# <a name="en_objectpositions-notification-code"></a><span data-ttu-id="0b650-105">\_Code de notification en OBJECTPOSITIONS</span><span class="sxs-lookup"><span data-stu-id="0b650-105">EN\_OBJECTPOSITIONS notification code</span></span>

<span data-ttu-id="0b650-106">Avertit une fenêtre parente d’un contrôle RichEdit quand le contrôle lit des objets.</span><span class="sxs-lookup"><span data-stu-id="0b650-106">Notifies a rich edit control's parent window when the control reads in objects.</span></span> <span data-ttu-id="0b650-107">Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0b650-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_OBJECTPOSITIONS

    pOjectPositions = (OBJECTPOSITIONS *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="0b650-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b650-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b650-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b650-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b650-110">Structure [**OBJECTPOSITIONS**](/windows/desktop/api/Richedit/ns-richedit-objectpositions) .</span><span class="sxs-lookup"><span data-stu-id="0b650-110">An [**OBJECTPOSITIONS**](/windows/desktop/api/Richedit/ns-richedit-objectpositions) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b650-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b650-111">Return value</span></span>

<span data-ttu-id="0b650-112">Retournez zéro pour poursuivre l’opération de **lecture** .</span><span class="sxs-lookup"><span data-stu-id="0b650-112">Return zero to continue the **Read** operation.</span></span>

<span data-ttu-id="0b650-113">Retourne une valeur différente de zéro pour arrêter l’opération de **lecture** .</span><span class="sxs-lookup"><span data-stu-id="0b650-113">Return a nonzero value to stop the **Read** operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b650-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0b650-114">Remarks</span></span>

<span data-ttu-id="0b650-115">Pour recevoir un \_ Code de notification en OBJECTPOSITIONS, spécifiez l’indicateur [**ENM \_ OBJECTPOSITIONS**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="0b650-115">To receive an EN\_OBJECTPOSITIONS notification code, specify the [**ENM\_OBJECTPOSITIONS**](rich-edit-control-event-mask-flags.md) flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b650-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b650-116">Requirements</span></span>



| <span data-ttu-id="0b650-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b650-117">Requirement</span></span> | <span data-ttu-id="0b650-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b650-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b650-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b650-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0b650-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b650-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0b650-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b650-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0b650-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b650-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0b650-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b650-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b650-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b650-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b650-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b650-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="0b650-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="0b650-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0b650-127">**EM \_ SETEVENTMASK**</span><span class="sxs-lookup"><span data-stu-id="0b650-127">**EM\_SETEVENTMASK**</span></span>](em-seteventmask.md)
</dt> <dt>

[<span data-ttu-id="0b650-128">**OBJECTPOSITIONS**</span><span class="sxs-lookup"><span data-stu-id="0b650-128">**OBJECTPOSITIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-objectpositions)
</dt> <dt>

[<span data-ttu-id="0b650-129">**\_notification WM**</span><span class="sxs-lookup"><span data-stu-id="0b650-129">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> <dt>

<span data-ttu-id="0b650-130">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="0b650-130">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="0b650-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0b650-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="0b650-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0b650-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> </dl>

 

