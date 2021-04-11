---
title: Message LVN_ODFINDITEM (commctrl. h)
description: Envoyé par un contrôle List-View virtuel lorsqu’il a besoin du propriétaire pour rechercher un élément de rappel particulier.
ms.assetid: 5a3f9fed-0c57-46bf-b986-ea8b54290b5e
keywords:
- LVN_ODFINDITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVN_ODFINDITEM
- LVN_ODFINDITEMA
- LVN_ODFINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a610f3de00e204bcdfbac51545553cebffe4c61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104812"
---
# <a name="lvn_odfinditem-message"></a><span data-ttu-id="11644-104">\_Message LVN ODFINDITEM</span><span class="sxs-lookup"><span data-stu-id="11644-104">LVN\_ODFINDITEM message</span></span>

<span data-ttu-id="11644-105">Envoyé par un contrôle [List-View virtuel](list-view-controls-overview.md) lorsqu’il a besoin du propriétaire pour rechercher un élément de rappel particulier.</span><span class="sxs-lookup"><span data-stu-id="11644-105">Sent by a [virtual list-view](list-view-controls-overview.md) control when it needs the owner to find a particular callback item.</span></span> <span data-ttu-id="11644-106">Par exemple, le contrôle enverra ce code de notification lorsqu’il reçoit une entrée au clavier du raccourci ou lorsqu’il reçoit un message [**\_ FINDITEM LVM**](lvm-finditem.md) .</span><span class="sxs-lookup"><span data-stu-id="11644-106">For example, the control will send this notification code when it receives shortcut keyboard input or when it receives an [**LVM\_FINDITEM**](lvm-finditem.md) message.</span></span> <span data-ttu-id="11644-107">Le \_ Code de notification LVN ODFINDITEM est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="11644-107">The LVN\_ODFINDITEM notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ODFINDITEM

    pFindInfo = (PNMLVFINDITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="11644-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11644-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11644-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="11644-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11644-110">Pointeur vers une structure [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) qui contient des informations à utiliser pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="11644-110">Pointer to an [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure that includes information to be used for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11644-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="11644-111">Return value</span></span>

<span data-ttu-id="11644-112">Retourne l’index de l’élément trouvé, ou-1 si aucun élément n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="11644-112">Return the index of the item found, or -1 if no item is found.</span></span>

## <a name="remarks"></a><span data-ttu-id="11644-113">Notes</span><span class="sxs-lookup"><span data-stu-id="11644-113">Remarks</span></span>

<span data-ttu-id="11644-114">Les informations de recherche sont envoyées sous la forme d’une structure [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) , qui est membre de la structure [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) .</span><span class="sxs-lookup"><span data-stu-id="11644-114">Search information is sent in the form of an [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structure, which is a member of the [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="11644-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11644-115">Requirements</span></span>



| <span data-ttu-id="11644-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11644-116">Requirement</span></span> | <span data-ttu-id="11644-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="11644-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11644-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11644-118">Minimum supported client</span></span><br/> | <span data-ttu-id="11644-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11644-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="11644-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11644-120">Minimum supported server</span></span><br/> | <span data-ttu-id="11644-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11644-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="11644-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="11644-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="11644-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="11644-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="11644-124">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="11644-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="11644-125">**LVN \_ ODFINDITEMW** (Unicode) et **LVN \_ ODFINDITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="11644-125">**LVN\_ODFINDITEMW** (Unicode) and **LVN\_ODFINDITEMA** (ANSI)</span></span><br/>             |



 

 





