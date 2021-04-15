---
title: LVN_LINKCLICK le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle List-View qu’un lien a été activé sur un lien. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: de8f40d6-b79e-4324-af67-9a3c0915609d
keywords:
- Contrôles Windows de code de notification LVN_LINKCLICK
topic_type:
- apiref
api_name:
- LVN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd69fb463e71523fcbd4eeb65a6a718d27847c09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467118"
---
# <a name="lvn_linkclick-notification-code"></a><span data-ttu-id="42a2b-105">\_Code de notification LVN LINKCLICK</span><span class="sxs-lookup"><span data-stu-id="42a2b-105">LVN\_LINKCLICK notification code</span></span>

<span data-ttu-id="42a2b-106">Avertit une fenêtre parente d’un contrôle List-View qu’un lien a été activé sur un lien.</span><span class="sxs-lookup"><span data-stu-id="42a2b-106">Notifies a list-view control's parent window that a link has been clicked on.</span></span> <span data-ttu-id="42a2b-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="42a2b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_LINKCLICK
        
    pLinkInfo = (NMLVLINK*) lParam;         
```



## <a name="parameters"></a><span data-ttu-id="42a2b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42a2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42a2b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42a2b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42a2b-110">Pointeur vers une structure [**NMLVLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlvlink) .</span><span class="sxs-lookup"><span data-stu-id="42a2b-110">Pointer to an [**NMLVLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlvlink) structure.</span></span> <span data-ttu-id="42a2b-111">L’identificateur du groupe contenant le lien se trouve dans le membre **iSubItem** .</span><span class="sxs-lookup"><span data-stu-id="42a2b-111">The identifier of the group containing the link is in the **iSubItem** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42a2b-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="42a2b-112">Return value</span></span>

<span data-ttu-id="42a2b-113">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="42a2b-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="42a2b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="42a2b-114">Remarks</span></span>

<span data-ttu-id="42a2b-115">L’exemple suivant montre comment une application peut répondre à ce code de notification dans son gestionnaire de messages [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="42a2b-115">The following example shows how an application might respond to this notification code in its [**WM\_NOTIFY**](wm-notify.md) message handler.</span></span> <span data-ttu-id="42a2b-116">L’exemple bascule l’État réduit du groupe et définit le texte de lien approprié.</span><span class="sxs-lookup"><span data-stu-id="42a2b-116">The example toggles the collapsed state of the group and sets the appropriate link text.</span></span>

``` syntax
case LVN_LINKCLICK:
{
    NMLVLINK* pLinkInfo = (NMLVLINK*)lParam;
    HWND hList = pLinkInfo->hdr.hwndFrom;
    LVGROUP groupInfo;
    groupInfo.cbSize = sizeof(groupInfo);
    groupInfo.mask = LVGF_TASK;
    int groupIndex = pLinkInfo->iSubItem;
    if (ListView_GetGroupState(hList, groupIndex, LVGS_COLLAPSED))
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, 0);
        groupInfo.pszTask = L"Hide";
    }
    else
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, LVGS_COLLAPSED);
        groupInfo.pszTask = L"Show";
     }
      ListView_SetGroupInfo(hList, groupIndex, &groupInfo);
      break;
}
```

## <a name="requirements"></a><span data-ttu-id="42a2b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42a2b-117">Requirements</span></span>



| <span data-ttu-id="42a2b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42a2b-118">Requirement</span></span> | <span data-ttu-id="42a2b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="42a2b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42a2b-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42a2b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="42a2b-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42a2b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="42a2b-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42a2b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="42a2b-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42a2b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="42a2b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="42a2b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="42a2b-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="42a2b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





