---
title: Code de notification NM_CLICK (mode liste) (commctrl. h)
description: Envoyé par un contrôle List-View lorsque l’utilisateur clique sur un élément avec le bouton gauche de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 7921bc27-54ca-4bb2-ac88-8267776661ab
keywords:
- Contrôles Windows de code de notification NM_CLICK (mode liste)
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d766767bfb742e5d7ea7c22a1266540a40d65b9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106648"
---
# <a name="nm_click-list-view-notification-code"></a><span data-ttu-id="811ab-105">NM- \_ cliquer (mode liste) Code de notification</span><span class="sxs-lookup"><span data-stu-id="811ab-105">NM\_CLICK (list view) notification code</span></span>

<span data-ttu-id="811ab-106">Envoyé par un contrôle List-View lorsque l’utilisateur clique sur un élément avec le bouton gauche de la souris.</span><span class="sxs-lookup"><span data-stu-id="811ab-106">Sent by a list-view control when the user clicks an item with the left mouse button.</span></span> <span data-ttu-id="811ab-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="811ab-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="811ab-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="811ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="811ab-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="811ab-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="811ab-110">[Version 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="811ab-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="811ab-111">Pointeur vers une structure [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="811ab-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains additional information about this notification.</span></span> <span data-ttu-id="811ab-112">Les membres **iItem**, **iSubItem** et **ptAction** de cette structure contiennent des informations sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="811ab-112">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="811ab-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="811ab-113">Return value</span></span>

<span data-ttu-id="811ab-114">La valeur de retour de cette notification n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="811ab-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="811ab-115">Notes</span><span class="sxs-lookup"><span data-stu-id="811ab-115">Remarks</span></span>

<span data-ttu-id="811ab-116">Le membre **iItem** de *lParam* est uniquement valide si l’utilisateur clique sur l’étiquette de la première colonne ou sur l’icône.</span><span class="sxs-lookup"><span data-stu-id="811ab-116">The **iItem** member of *lParam* is only valid if the icon or first-column label has been clicked.</span></span> <span data-ttu-id="811ab-117">Pour déterminer l’élément sélectionné lorsqu’un clic est effectué ailleurs dans une ligne, envoyez un message [**\_ SUBITEMHITTEST LVM**](lvm-subitemhittest.md) .</span><span class="sxs-lookup"><span data-stu-id="811ab-117">To determine which item is selected when a click takes place elsewhere in a row, send an [**LVM\_SUBITEMHITTEST**](lvm-subitemhittest.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="811ab-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="811ab-118">Requirements</span></span>



| <span data-ttu-id="811ab-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="811ab-119">Requirement</span></span> | <span data-ttu-id="811ab-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="811ab-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="811ab-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="811ab-121">Minimum supported client</span></span><br/> | <span data-ttu-id="811ab-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="811ab-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="811ab-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="811ab-123">Minimum supported server</span></span><br/> | <span data-ttu-id="811ab-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="811ab-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="811ab-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="811ab-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="811ab-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="811ab-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





