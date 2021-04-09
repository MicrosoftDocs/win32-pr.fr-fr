---
title: PGN_SCROLL le code de notification (commctrl. h)
description: Notifie la fenêtre parente d’un contrôle de pagineur que la fenêtre contenue est sur le défilant. Cette notification est envoyée sous la forme d’un \_ message WM Notify.
ms.assetid: 3d40e75e-c445-4885-b807-8cfcb92cb2d9
keywords:
- Contrôles Windows de code de notification PGN_SCROLL
topic_type:
- apiref
api_name:
- PGN_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62bc964b1a820fb0d5cd341e8909f36d5f6312ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103472"
---
# <a name="pgn_scroll-notification-code"></a><span data-ttu-id="43578-105">\_Code de notification de défilement PGN</span><span class="sxs-lookup"><span data-stu-id="43578-105">PGN\_SCROLL notification code</span></span>

<span data-ttu-id="43578-106">Notifie la fenêtre parente d’un contrôle de pagineur que la fenêtre contenue est sur le défilant.</span><span class="sxs-lookup"><span data-stu-id="43578-106">Notifies a pager control's parent window that the contained window is about to be scrolled.</span></span> <span data-ttu-id="43578-107">Cette notification est envoyée sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="43578-107">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PGN_SCROLL

    lpnms = (LPNMPGSCROLL) lParam;
```



## <a name="parameters"></a><span data-ttu-id="43578-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43578-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43578-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43578-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43578-110">Pointeur vers une structure [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll) qui contient et reçoit des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="43578-110">Pointer to an [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll) structure that contains and receives information about the notification code.</span></span> <span data-ttu-id="43578-111">Le membre **iDir** de cette structure indique la direction du défilement.</span><span class="sxs-lookup"><span data-stu-id="43578-111">The **iDir** member of this structure indicates the direction of the scroll.</span></span> <span data-ttu-id="43578-112">Les membres **iXpos** et **iYpos** contiennent la position horizontale et verticale de la fenêtre contenue avant le défilement.</span><span class="sxs-lookup"><span data-stu-id="43578-112">The **iXpos** and **iYpos** members contain the horizontal and vertical position of the contained window prior to the scroll.</span></span> <span data-ttu-id="43578-113">Le membre **iScroll** contient le montant Delta de défilement par défaut.</span><span class="sxs-lookup"><span data-stu-id="43578-113">The **iScroll** member contains the default scroll delta amount.</span></span> <span data-ttu-id="43578-114">Vous pouvez modifier ce membre en fonction d’un autre montant de défilement, si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="43578-114">You can modify this member to a different scroll amount if desired.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43578-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="43578-115">Return value</span></span>

<span data-ttu-id="43578-116">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="43578-116">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="43578-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43578-117">Requirements</span></span>



| <span data-ttu-id="43578-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43578-118">Requirement</span></span> | <span data-ttu-id="43578-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="43578-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43578-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43578-120">Minimum supported client</span></span><br/> | <span data-ttu-id="43578-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43578-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43578-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43578-122">Minimum supported server</span></span><br/> | <span data-ttu-id="43578-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43578-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43578-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="43578-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="43578-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="43578-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





