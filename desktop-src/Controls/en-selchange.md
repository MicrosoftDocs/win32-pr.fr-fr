---
title: Code de notification EN_SELCHANGE (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle RichEdit que la sélection actuelle a été modifiée. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: 53d47b53-a73c-4652-889c-2374f8e99382
keywords:
- Contrôles Windows de code de notification EN_SELCHANGE
topic_type:
- apiref
api_name:
- EN_SELCHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79dfcf951f88fa1e10f4723bd9843421f0e20ae5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743029"
---
# <a name="en_selchange-notification-code"></a><span data-ttu-id="7c233-105">\_Code de notification en selChange</span><span class="sxs-lookup"><span data-stu-id="7c233-105">EN\_SELCHANGE notification code</span></span>

<span data-ttu-id="7c233-106">Avertit une fenêtre parente d’un contrôle RichEdit que la sélection actuelle a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="7c233-106">Notifies a rich edit control's parent window that the current selection has changed.</span></span> <span data-ttu-id="7c233-107">Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7c233-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_SELCHANGE

    pSelChange = (SELCHANGE *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="7c233-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c233-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c233-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c233-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c233-110">Structure [**selChange**](/windows/desktop/api/Richedit/ns-richedit-selchange) qui reçoit des informations sur la sélection.</span><span class="sxs-lookup"><span data-stu-id="7c233-110">A [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c233-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7c233-111">Return value</span></span>

<span data-ttu-id="7c233-112">Ce code de notification ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7c233-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c233-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7c233-113">Remarks</span></span>

<span data-ttu-id="7c233-114">Pour recevoir les \_ codes de notification en selChange, spécifiez [**ENM \_ selChange**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="7c233-114">To receive EN\_SELCHANGE notification codes, specify [**ENM\_SELCHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="7c233-115">Ce code de notification est envoyé lorsque l’emplacement du signe insertion change et qu’aucun texte n’est sélectionné (la sélection est vide).</span><span class="sxs-lookup"><span data-stu-id="7c233-115">This notification code is sent when the caret position changes and no text is selected (the selection is empty).</span></span> <span data-ttu-id="7c233-116">La position du signe insertion peut changer lorsque l’utilisateur clique sur la souris, tape ou appuie sur une touche de direction.</span><span class="sxs-lookup"><span data-stu-id="7c233-116">The caret position can change when the user clicks the mouse, types, or presses an arrow key.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c233-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c233-117">Requirements</span></span>



| <span data-ttu-id="7c233-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c233-118">Requirement</span></span> | <span data-ttu-id="7c233-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c233-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c233-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c233-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7c233-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c233-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7c233-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c233-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7c233-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c233-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c233-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c233-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c233-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c233-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c233-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c233-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="7c233-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="7c233-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7c233-128">**SELCHANGE**</span><span class="sxs-lookup"><span data-stu-id="7c233-128">**SELCHANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-selchange)
</dt> <dt>

[<span data-ttu-id="7c233-129">**\_notification WM**</span><span class="sxs-lookup"><span data-stu-id="7c233-129">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





