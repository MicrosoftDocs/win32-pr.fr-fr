---
title: Message BCM_SETDROPDOWNSTATE (commctrl. h)
description: Définit l’État déroulant d’un bouton avec la \_ liste déroulante style TBSTYLE. Envoyez ce message explicitement ou à l’aide de la \_ macro Button SetDropDownState.
ms.assetid: 725deff4-0bcb-497d-a6cf-e9c98b05f16e
keywords:
- BCM_SETDROPDOWNSTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- BCM_SETDROPDOWNSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc44ec58d40e047708591121f81c84f327ca47c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103633"
---
# <a name="bcm_setdropdownstate-message"></a><span data-ttu-id="5fc3f-105">\_Message SETDROPDOWNSTATE BCM</span><span class="sxs-lookup"><span data-stu-id="5fc3f-105">BCM\_SETDROPDOWNSTATE message</span></span>

<span data-ttu-id="5fc3f-106">Définit l’État déroulant d’un bouton avec la [**\_ liste déroulante style TBSTYLE**](toolbar-control-and-button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="5fc3f-106">Sets the drop down state for a button with style [**TBSTYLE\_DROPDOWN**](toolbar-control-and-button-styles.md).</span></span> <span data-ttu-id="5fc3f-107">Envoyez ce message explicitement ou à l’aide de la macro [**Button \_ SetDropDownState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) .</span><span class="sxs-lookup"><span data-stu-id="5fc3f-107">Send this message explicitly or by using the [**Button\_SetDropDownState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5fc3f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5fc3f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fc3f-109">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5fc3f-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fc3f-110">Valeur **booléenne** qui est **true** pour l’état de BST \_ DROPDOWNPUSHED, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5fc3f-110">A **BOOL** that is **TRUE** for state of BST\_DROPDOWNPUSHED, or **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="5fc3f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5fc3f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5fc3f-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="5fc3f-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fc3f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5fc3f-113">Return value</span></span>

<span data-ttu-id="5fc3f-114">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5fc3f-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fc3f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5fc3f-115">Requirements</span></span>



| <span data-ttu-id="5fc3f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5fc3f-116">Requirement</span></span> | <span data-ttu-id="5fc3f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fc3f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5fc3f-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fc3f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5fc3f-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fc3f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5fc3f-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fc3f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5fc3f-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fc3f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5fc3f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="5fc3f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fc3f-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fc3f-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fc3f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fc3f-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="5fc3f-125">**Référence**</span><span class="sxs-lookup"><span data-stu-id="5fc3f-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5fc3f-126">Styles de bouton</span><span class="sxs-lookup"><span data-stu-id="5fc3f-126">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="5fc3f-127">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="5fc3f-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5fc3f-128">Types de bouton</span><span class="sxs-lookup"><span data-stu-id="5fc3f-128">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





