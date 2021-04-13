---
title: Message LVM_GETHOVERTIME (commctrl. h)
description: Récupère la durée pendant laquelle le curseur de la souris doit pointer sur un élément avant d’être sélectionné. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetHoverTime.
ms.assetid: e7646024-f868-459f-88be-b232b6b4bb2a
keywords:
- LVM_GETHOVERTIME les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83e243ece42f06ffe35eb31954d9ca0dd44957be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465879"
---
# <a name="lvm_gethovertime-message"></a><span data-ttu-id="f322a-105">\_Message GETHOVERTIME LVM</span><span class="sxs-lookup"><span data-stu-id="f322a-105">LVM\_GETHOVERTIME message</span></span>

<span data-ttu-id="f322a-106">Récupère la durée pendant laquelle le curseur de la souris doit pointer sur un élément avant d’être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="f322a-106">Retrieves the amount of time that the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="f322a-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetHoverTime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime) .</span><span class="sxs-lookup"><span data-stu-id="f322a-107">You can send this message explicitly or use the [**ListView\_GetHoverTime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f322a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f322a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f322a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f322a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f322a-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="f322a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f322a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f322a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f322a-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="f322a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f322a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f322a-113">Return value</span></span>

<span data-ttu-id="f322a-114">Retourne la durée, en millisecondes, pendant laquelle le curseur de la souris doit pointer sur un élément avant d’être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="f322a-114">Returns the amount of time, in milliseconds, that the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="f322a-115">Si la valeur de retour est (**DWORD**)-1, la durée de pointage est la durée de pointage par défaut.</span><span class="sxs-lookup"><span data-stu-id="f322a-115">If the return value is (**DWORD**)-1, then the hover time is the default hover time.</span></span>

## <a name="remarks"></a><span data-ttu-id="f322a-116">Notes</span><span class="sxs-lookup"><span data-stu-id="f322a-116">Remarks</span></span>

<span data-ttu-id="f322a-117">La durée de survol affecte uniquement les contrôles d’affichage de liste qui ont le style de vue de liste étendu [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md), [**LVS \_ ex \_ ONECLICKACTIVATE**](extended-list-view-styles.md)ou [**LVS \_ ex \_ TWOCLICKACTIVATE**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f322a-117">The hover time only affects list-view controls that have the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md), [**LVS\_EX\_ONECLICKACTIVATE**](extended-list-view-styles.md), or [**LVS\_EX\_TWOCLICKACTIVATE**](extended-list-view-styles.md) extended list-view style.</span></span>

## <a name="requirements"></a><span data-ttu-id="f322a-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f322a-118">Requirements</span></span>



| <span data-ttu-id="f322a-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f322a-119">Requirement</span></span> | <span data-ttu-id="f322a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f322a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f322a-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f322a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f322a-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f322a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f322a-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f322a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f322a-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f322a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f322a-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="f322a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f322a-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f322a-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





