---
title: Message HDM_GETITEMDROPDOWNRECT (commctrl. h)
description: Obtient le rectangle englobant du bouton partagé pour un élément d’en-tête avec style HDF \_ SPLITBUTTON. Envoyez ce message de manière explicite ou à l’aide de la macro GetItemDropDownRect d’en-tête \_ .
ms.assetid: d7188dfb-4ffa-4641-b210-2c2ec480ca13
keywords:
- HDM_GETITEMDROPDOWNRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86f3df8de5224e79ca4e15ea18409e13972ca5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032892"
---
# <a name="hdm_getitemdropdownrect-message"></a><span data-ttu-id="4a1a4-105">\_Message HDM GETITEMDROPDOWNRECT</span><span class="sxs-lookup"><span data-stu-id="4a1a4-105">HDM\_GETITEMDROPDOWNRECT message</span></span>

<span data-ttu-id="4a1a4-106">Obtient le rectangle englobant du bouton partagé pour un élément d’en-tête avec style **HDF \_ SPLITBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="4a1a4-106">Gets the bounding rectangle of the split button for a header item with style **HDF\_SPLITBUTTON**.</span></span> <span data-ttu-id="4a1a4-107">Envoyez ce message de manière explicite ou à l’aide de la macro [**\_ GetItemDropDownRect d’en-tête**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect) .</span><span class="sxs-lookup"><span data-stu-id="4a1a4-107">Send this message explicitly or by using the [**Header\_GetItemDropDownRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4a1a4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a1a4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a1a4-109">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4a1a4-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a1a4-110">Index de base zéro de l’élément de contrôle d’en-tête pour lequel récupérer le rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="4a1a4-110">The zero-based index of the header control item for which to retrieve the bounding rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="4a1a4-111">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4a1a4-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a1a4-112">Pointeur vers une structure [**Rect**](/windows/win32/api/windef/ns-windef-rect) qui reçoit les informations de rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="4a1a4-112">A pointer to a [**RECT**](/windows/win32/api/windef/ns-windef-rect) structure that receives the bounding rectangle information.</span></span> <span data-ttu-id="4a1a4-113">L’expéditeur du message est chargé d’allouer cette structure.</span><span class="sxs-lookup"><span data-stu-id="4a1a4-113">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="4a1a4-114">Les coordonnées retournées dans la structure RECT sont exprimées par rapport au parent du contrôle header.</span><span class="sxs-lookup"><span data-stu-id="4a1a4-114">The coordinates returned in the RECT structure are expressed relative to the header control parent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a1a4-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4a1a4-115">Return value</span></span>

<span data-ttu-id="4a1a4-116">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4a1a4-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a1a4-117">Notes</span><span class="sxs-lookup"><span data-stu-id="4a1a4-117">Remarks</span></span>

<span data-ttu-id="4a1a4-118">L’élément d’en-tête doit être de style **HDF \_ SPLITBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="4a1a4-118">The header item must have style **HDF\_SPLITBUTTON**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a1a4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a1a4-119">Requirements</span></span>



| <span data-ttu-id="4a1a4-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a1a4-120">Requirement</span></span> | <span data-ttu-id="4a1a4-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a1a4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a1a4-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a1a4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4a1a4-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a1a4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4a1a4-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a1a4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4a1a4-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a1a4-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4a1a4-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a1a4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a1a4-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a1a4-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a1a4-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a1a4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a1a4-129">À propos des contrôles Header</span><span class="sxs-lookup"><span data-stu-id="4a1a4-129">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

 





