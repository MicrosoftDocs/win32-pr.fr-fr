---
title: Code de notification NM_SETFOCUS (mode liste) (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle List-View que le contrôle a reçu le focus d’entrée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 43d3b09a-f095-4f30-87a8-2f2e782d6720
keywords:
- Contrôles Windows de code de notification NM_SETFOCUS (mode liste)
topic_type:
- apiref
api_name:
- NM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99cc84e76c0203a6e2930d3d9f50bc61a1e31395
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032689"
---
# <a name="nm_setfocus-list-view-notification-code"></a><span data-ttu-id="fa908-105">NM \_ SetFocus (mode liste) Code de notification</span><span class="sxs-lookup"><span data-stu-id="fa908-105">NM\_SETFOCUS (list view) notification code</span></span>

<span data-ttu-id="fa908-106">Avertit une fenêtre parente d’un contrôle List-View que le contrôle a reçu le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="fa908-106">Notifies a list-view control's parent window that the control has received the input focus.</span></span> <span data-ttu-id="fa908-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fa908-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="fa908-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa908-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa908-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa908-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa908-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="fa908-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa908-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fa908-111">Return value</span></span>

<span data-ttu-id="fa908-112">La valeur de retour de cette notification n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="fa908-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa908-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa908-113">Requirements</span></span>



| <span data-ttu-id="fa908-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa908-114">Requirement</span></span> | <span data-ttu-id="fa908-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa908-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa908-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa908-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fa908-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa908-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fa908-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa908-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fa908-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa908-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fa908-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="fa908-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa908-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa908-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





