---
title: Message BCM_SETSPLITINFO (commctrl. h)
description: Définit des informations pour un contrôle bouton partagé. Envoyez ce message explicitement ou à l’aide de la \_ macro Button SetSplitInfo.
ms.assetid: 609b8972-9616-4850-a72c-2f87ce19f563
keywords:
- BCM_SETSPLITINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- BCM_SETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac40f2d1ef016ee76ab21ccf2dc4733d0ff427f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512579"
---
# <a name="bcm_setsplitinfo-message"></a><span data-ttu-id="5eae1-105">\_Message SETSPLITINFO BCM</span><span class="sxs-lookup"><span data-stu-id="5eae1-105">BCM\_SETSPLITINFO message</span></span>

<span data-ttu-id="5eae1-106">Définit des informations pour un contrôle bouton partagé.</span><span class="sxs-lookup"><span data-stu-id="5eae1-106">Sets information for a split button control.</span></span> <span data-ttu-id="5eae1-107">Envoyez ce message explicitement ou à l’aide de la macro [**Button \_ SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) .</span><span class="sxs-lookup"><span data-stu-id="5eae1-107">Send this message explicitly or by using the [**Button\_SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5eae1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5eae1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5eae1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5eae1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5eae1-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="5eae1-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5eae1-111">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5eae1-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eae1-112">Pointeur vers une structure [**\_ SPLITINFO de bouton**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) contenant des informations sur le bouton partagé.</span><span class="sxs-lookup"><span data-stu-id="5eae1-112">A pointer to a [**BUTTON\_SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) structure containing information about the split button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5eae1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5eae1-113">Return value</span></span>

<span data-ttu-id="5eae1-114">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5eae1-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5eae1-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5eae1-115">Remarks</span></span>

<span data-ttu-id="5eae1-116">Utilisez ce message uniquement avec les styles de boutons [**BS \_ SPLITBUTTON**](button-styles.md) et [**BS \_ DEFSPLITBUTTON**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5eae1-116">Use this message only with the [**BS\_SPLITBUTTON**](button-styles.md) and [**BS\_DEFSPLITBUTTON**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="5eae1-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5eae1-117">Requirements</span></span>



| <span data-ttu-id="5eae1-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5eae1-118">Requirement</span></span> | <span data-ttu-id="5eae1-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5eae1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5eae1-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5eae1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5eae1-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5eae1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5eae1-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5eae1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5eae1-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5eae1-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5eae1-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="5eae1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5eae1-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5eae1-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5eae1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5eae1-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="5eae1-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="5eae1-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5eae1-128">Styles de bouton</span><span class="sxs-lookup"><span data-stu-id="5eae1-128">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="5eae1-129">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="5eae1-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5eae1-130">Types de bouton</span><span class="sxs-lookup"><span data-stu-id="5eae1-130">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





