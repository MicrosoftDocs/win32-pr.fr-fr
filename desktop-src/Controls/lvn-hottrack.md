---
title: LVN_HOTTRACK le code de notification (commctrl. h)
description: Envoyé par un contrôle List-View lorsque l’utilisateur déplace la souris sur un élément. Ce code de notification est uniquement envoyé par les contrôles List-View qui ont \_ le \_ style LVS ex TRACKSELECT Extended List-View. Il est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 6bbfe6b8-9b67-49e4-9481-65abe98608bb
keywords:
- Contrôles Windows de code de notification LVN_HOTTRACK
topic_type:
- apiref
api_name:
- LVN_HOTTRACK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c677b69fa21cdbe3680442304f6745cfb3a907de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844474"
---
# <a name="lvn_hottrack-notification-code"></a><span data-ttu-id="bc174-106">\_Code de notification LVN HOTTRACK</span><span class="sxs-lookup"><span data-stu-id="bc174-106">LVN\_HOTTRACK notification code</span></span>

<span data-ttu-id="bc174-107">Envoyé par un contrôle List-View lorsque l’utilisateur déplace la souris sur un élément.</span><span class="sxs-lookup"><span data-stu-id="bc174-107">Sent by a list-view control when the user moves the mouse over an item.</span></span> <span data-ttu-id="bc174-108">Ce code de notification est uniquement envoyé par les contrôles List-View qui ont le style [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) Extended List-View.</span><span class="sxs-lookup"><span data-stu-id="bc174-108">This notification code is only sent by list-view controls that have the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md) extended list-view style.</span></span> <span data-ttu-id="bc174-109">Il est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bc174-109">It is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_HOTTRACK

    lpnmlv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="bc174-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc174-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc174-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bc174-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc174-112">Pointeur vers une structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) qui contient des informations sur ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="bc174-112">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that contains information about this notification code.</span></span> <span data-ttu-id="bc174-113">Les membres **iItem**, **iSubItem** et **ptAction** de cette structure contiennent des informations sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="bc174-113">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span> <span data-ttu-id="bc174-114">L’application réceptrice peut modifier le membre **iItem** pour spécifier l’élément qui sera sélectionné.</span><span class="sxs-lookup"><span data-stu-id="bc174-114">The receiving application can modify the **iItem** member to specify the item that will be selected.</span></span> <span data-ttu-id="bc174-115">Si **iItem** a la valeur-1, aucun élément n’est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="bc174-115">If **iItem** is set to -1, no item will be selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc174-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bc174-116">Return value</span></span>

<span data-ttu-id="bc174-117">Retourne zéro pour permettre à la vue de liste d’effectuer son traitement de sélection normal.</span><span class="sxs-lookup"><span data-stu-id="bc174-117">Return zero to allow the list view to perform its normal track select processing.</span></span> <span data-ttu-id="bc174-118">Si l’application retourne une valeur différente de zéro, l’élément n’est pas sélectionné.</span><span class="sxs-lookup"><span data-stu-id="bc174-118">If the application returns nonzero, the item will not be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc174-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc174-119">Requirements</span></span>



| <span data-ttu-id="bc174-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc174-120">Requirement</span></span> | <span data-ttu-id="bc174-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc174-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc174-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc174-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bc174-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc174-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bc174-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc174-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bc174-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc174-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bc174-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="bc174-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc174-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc174-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





