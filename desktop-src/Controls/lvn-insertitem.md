---
title: LVN_INSERTITEM le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle List-View qu’un nouvel élément a été inséré. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 8d368fb2-e4fc-4dc4-a89e-872ba1278b75
keywords:
- Contrôles Windows de code de notification LVN_INSERTITEM
topic_type:
- apiref
api_name:
- LVN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba70ba806dea2725385badee4b5c57e927a9d42b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479437"
---
# <a name="lvn_insertitem-notification-code"></a><span data-ttu-id="84dc3-105">\_Code de notification LVN INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="84dc3-105">LVN\_INSERTITEM notification code</span></span>

<span data-ttu-id="84dc3-106">Avertit la fenêtre parente d’un contrôle List-View qu’un nouvel élément a été inséré.</span><span class="sxs-lookup"><span data-stu-id="84dc3-106">Notifies a list-view control's parent window that a new item was inserted.</span></span> <span data-ttu-id="84dc3-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="84dc3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_INSERTITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="84dc3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84dc3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84dc3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="84dc3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84dc3-110">Pointeur vers une structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="84dc3-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="84dc3-111">Le membre **iItem** identifie le nouvel élément, et les autres membres sont nuls.</span><span class="sxs-lookup"><span data-stu-id="84dc3-111">The **iItem** member identifies the new item, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84dc3-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="84dc3-112">Return value</span></span>

<span data-ttu-id="84dc3-113">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="84dc3-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="84dc3-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84dc3-114">Requirements</span></span>



| <span data-ttu-id="84dc3-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84dc3-115">Requirement</span></span> | <span data-ttu-id="84dc3-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="84dc3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84dc3-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84dc3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="84dc3-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84dc3-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="84dc3-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84dc3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="84dc3-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84dc3-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="84dc3-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="84dc3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="84dc3-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="84dc3-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





