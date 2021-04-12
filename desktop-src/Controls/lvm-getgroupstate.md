---
title: Message LVM_GETGROUPSTATE (commctrl. h)
description: Obtient l’état d’un groupe spécifié. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView GetGroupState.
ms.assetid: f087d17f-9066-44fb-b21b-ac7ceb56eb45
keywords:
- LVM_GETGROUPSTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17b5bb25fd517816afd04bb700211222e6985f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464414"
---
# <a name="lvm_getgroupstate-message"></a><span data-ttu-id="14087-105">\_Message GETGROUPSTATE LVM</span><span class="sxs-lookup"><span data-stu-id="14087-105">LVM\_GETGROUPSTATE message</span></span>

<span data-ttu-id="14087-106">Obtient l’état d’un groupe spécifié.</span><span class="sxs-lookup"><span data-stu-id="14087-106">Gets the state for a specified group.</span></span> <span data-ttu-id="14087-107">Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ GetGroupState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate) .</span><span class="sxs-lookup"><span data-stu-id="14087-107">Send this message explicitly or by using the [**ListView\_GetGroupState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="14087-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14087-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14087-109">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14087-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14087-110">Spécifie le groupe par **iGroupId** (voir structure [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ).</span><span class="sxs-lookup"><span data-stu-id="14087-110">Specifies the group by **iGroupId** (see [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure).</span></span>

</dd> <dt>

<span data-ttu-id="14087-111">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14087-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14087-112">Spécifie les valeurs d’État à récupérer.</span><span class="sxs-lookup"><span data-stu-id="14087-112">Specifies the state values to retrieve.</span></span> <span data-ttu-id="14087-113">Il s’agit d’une combinaison des indicateurs listés pour le membre d' **État** de [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup).</span><span class="sxs-lookup"><span data-stu-id="14087-113">This is a combination of the flags listed for the **state** member of [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14087-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="14087-114">Return value</span></span>

<span data-ttu-id="14087-115">Retourne la combinaison des valeurs d’état définies.</span><span class="sxs-lookup"><span data-stu-id="14087-115">Returns the combination of state values that are set.</span></span> <span data-ttu-id="14087-116">Par exemple, si *lParam* est LVGS \_ réduit et que la valeur retournée est zéro, l' \_ État réduit LVGS n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="14087-116">For example, if *lParam* is LVGS\_COLLAPSED and the value returned is zero, the LVGS\_COLLAPSED state is not set.</span></span> <span data-ttu-id="14087-117">La valeur zéro est retournée si le groupe est introuvable.</span><span class="sxs-lookup"><span data-stu-id="14087-117">Zero is returned if the group is not found.</span></span>

## <a name="requirements"></a><span data-ttu-id="14087-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14087-118">Requirements</span></span>



| <span data-ttu-id="14087-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14087-119">Requirement</span></span> | <span data-ttu-id="14087-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="14087-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14087-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14087-121">Minimum supported client</span></span><br/> | <span data-ttu-id="14087-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14087-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="14087-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14087-123">Minimum supported server</span></span><br/> | <span data-ttu-id="14087-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14087-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="14087-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="14087-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="14087-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="14087-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





