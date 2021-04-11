---
title: Message LVM_SETHOVERTIME (commctrl. h)
description: Définit la durée pendant laquelle le curseur de la souris doit pointer sur un élément avant d’être sélectionné. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView SetHoverTime.
ms.assetid: 454fbc38-f7fd-4dea-b223-56003b88528f
keywords:
- LVM_SETHOVERTIME les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3aecd3c0d48cddc2cbaae49e7e888f91a985575
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102885"
---
# <a name="lvm_sethovertime-message"></a><span data-ttu-id="bdfcb-105">\_Message SETHOVERTIME LVM</span><span class="sxs-lookup"><span data-stu-id="bdfcb-105">LVM\_SETHOVERTIME message</span></span>

<span data-ttu-id="bdfcb-106">Définit la durée pendant laquelle le curseur de la souris doit pointer sur un élément avant d’être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="bdfcb-106">Sets the amount of time which the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="bdfcb-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ SetHoverTime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime) .</span><span class="sxs-lookup"><span data-stu-id="bdfcb-107">You can send this message explicitly or use the [**ListView\_SetHoverTime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bdfcb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdfcb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdfcb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bdfcb-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bdfcb-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="bdfcb-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bdfcb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bdfcb-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdfcb-112">Nouvelle durée, en millisecondes, pendant laquelle le curseur de la souris doit pointer sur un élément avant d’être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="bdfcb-112">The new amount of time, in milliseconds, that the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="bdfcb-113">Si cette valeur est (**DWORD**)-1, la durée de survol est définie sur la durée de pointage par défaut.</span><span class="sxs-lookup"><span data-stu-id="bdfcb-113">If this value is (**DWORD**)-1, then the hover time is set to the default hover time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdfcb-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bdfcb-114">Return value</span></span>

<span data-ttu-id="bdfcb-115">Retourne la durée de pointage précédente.</span><span class="sxs-lookup"><span data-stu-id="bdfcb-115">Returns the previous hover time.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdfcb-116">Notes</span><span class="sxs-lookup"><span data-stu-id="bdfcb-116">Remarks</span></span>

<span data-ttu-id="bdfcb-117">La durée de survol affecte uniquement les contrôles d’affichage de liste qui ont le style de vue de liste étendu [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md), [**LVS \_ ex \_ ONECLICKACTIVATE**](extended-list-view-styles.md)ou [**LVS \_ ex \_ TWOCLICKACTIVATE**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="bdfcb-117">The hover time only affects list-view controls that have the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md), [**LVS\_EX\_ONECLICKACTIVATE**](extended-list-view-styles.md), or [**LVS\_EX\_TWOCLICKACTIVATE**](extended-list-view-styles.md) extended list-view style.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdfcb-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bdfcb-118">Requirements</span></span>



| <span data-ttu-id="bdfcb-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bdfcb-119">Requirement</span></span> | <span data-ttu-id="bdfcb-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdfcb-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bdfcb-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bdfcb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bdfcb-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bdfcb-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bdfcb-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bdfcb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bdfcb-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bdfcb-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bdfcb-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="bdfcb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdfcb-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdfcb-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





