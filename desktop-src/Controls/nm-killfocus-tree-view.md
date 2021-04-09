---
title: Code de notification NM_KILLFOCUS (arborescence) (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View que le contrôle a perdu le focus d’entrée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: f6646a39-6480-4417-9c1c-ffd2417ca7dd
keywords:
- Contrôles Windows de code de notification NM_KILLFOCUS (arborescence)
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7123f47469a02fcec92805a27d81e173c5e1d10a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941663"
---
# <a name="nm_killfocus-tree-view-notification-code"></a><span data-ttu-id="012f0-105">\_Code de notification KILLFOCUS nm (arborescence)</span><span class="sxs-lookup"><span data-stu-id="012f0-105">NM\_KILLFOCUS (tree view) notification code</span></span>

<span data-ttu-id="012f0-106">Avertit une fenêtre parente d’un contrôle Tree-View que le contrôle a perdu le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="012f0-106">Notifies a tree-view control's parent window that the control has lost the input focus.</span></span> <span data-ttu-id="012f0-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="012f0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="012f0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="012f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="012f0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="012f0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="012f0-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="012f0-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="012f0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="012f0-111">Return value</span></span>

<span data-ttu-id="012f0-112">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="012f0-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="012f0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="012f0-113">Requirements</span></span>



| <span data-ttu-id="012f0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="012f0-114">Requirement</span></span> | <span data-ttu-id="012f0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="012f0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="012f0-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="012f0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="012f0-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="012f0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="012f0-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="012f0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="012f0-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="012f0-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="012f0-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="012f0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="012f0-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="012f0-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





