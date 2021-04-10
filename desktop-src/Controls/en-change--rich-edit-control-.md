---
title: Code de notification EN_CHANGE (Rich Edit) (winuser. h)
description: Avertit la fenêtre hôte d’un contrôle Rich Edit sans fenêtre qu’une modification s’est produite. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: 97C0D9F1-7D4E-409D-A4F6-E645475A8EEF
keywords:
- Contrôles Windows de code de notification EN_CHANGE (modification enrichie)
topic_type:
- apiref
api_name:
- EN_CHANGE (rich edit control)
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea615234aba881b2a8938b8e502b36acfa565fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941957"
---
# <a name="en_change-rich-edit-notification-code"></a><span data-ttu-id="e91f8-105">\_Code de notification en modification (RichEdit)</span><span class="sxs-lookup"><span data-stu-id="e91f8-105">EN\_CHANGE (rich edit) notification code</span></span>

<span data-ttu-id="e91f8-106">Avertit la fenêtre hôte d’un contrôle Rich Edit sans fenêtre qu’une modification s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e91f8-106">Notifies a windowless rich edit control's host window that a change has occurred.</span></span> <span data-ttu-id="e91f8-107">Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e91f8-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_CHANGE

    penChangeNotify = (CHANGENOTIFY *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e91f8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e91f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e91f8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e91f8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e91f8-110">Structure [**CHANGENOTIFY**](/windows/desktop/api/Textserv/ns-textserv-changenotify) spécifiant la modification apportée.</span><span class="sxs-lookup"><span data-stu-id="e91f8-110">A [**CHANGENOTIFY**](/windows/desktop/api/Textserv/ns-textserv-changenotify) structure specifying the change that was made.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e91f8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e91f8-111">Return value</span></span>

<span data-ttu-id="e91f8-112">Ce code de notification ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e91f8-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e91f8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e91f8-113">Remarks</span></span>

<span data-ttu-id="e91f8-114">Pour recevoir les \_ codes de notification de modification, spécifiez [**ENM \_ change**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="e91f8-114">To receive EN\_CHANGE notification codes, specify [**ENM\_CHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e91f8-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e91f8-115">Requirements</span></span>



| <span data-ttu-id="e91f8-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e91f8-116">Requirement</span></span> | <span data-ttu-id="e91f8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e91f8-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e91f8-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e91f8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e91f8-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e91f8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e91f8-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e91f8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e91f8-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e91f8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e91f8-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e91f8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e91f8-123"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="e91f8-123"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e91f8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e91f8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e91f8-125">**TxNotify**</span><span class="sxs-lookup"><span data-stu-id="e91f8-125">**TxNotify**</span></span>](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify)
</dt> </dl>

 

 





