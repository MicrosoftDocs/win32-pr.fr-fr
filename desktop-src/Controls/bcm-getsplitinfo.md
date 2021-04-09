---
title: Message BCM_GETSPLITINFO (commctrl. h)
description: Obtient des informations pour un contrôle bouton partagé. Envoyez ce message explicitement ou à l’aide de la \_ macro Button GetSplitInfo.
ms.assetid: d608440d-b8d8-4e32-9128-08b7566b185c
keywords:
- BCM_GETSPLITINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- BCM_GETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 162c5522fcb432e3d512f688ae24aa12d4d0d8e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942204"
---
# <a name="bcm_getsplitinfo-message"></a><span data-ttu-id="b5201-105">\_Message GETSPLITINFO BCM</span><span class="sxs-lookup"><span data-stu-id="b5201-105">BCM\_GETSPLITINFO message</span></span>

<span data-ttu-id="b5201-106">Obtient des informations pour un contrôle bouton partagé.</span><span class="sxs-lookup"><span data-stu-id="b5201-106">Gets information for a split button control.</span></span> <span data-ttu-id="b5201-107">Envoyez ce message explicitement ou à l’aide de la macro [**Button \_ GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) .</span><span class="sxs-lookup"><span data-stu-id="b5201-107">Send this message explicitly or by using the [**Button\_GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b5201-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5201-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5201-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b5201-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5201-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b5201-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b5201-111">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b5201-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5201-112">Pointeur vers une structure [**\_ SPLITINFO de bouton**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) pour recevoir des informations sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="b5201-112">A pointer to a [**BUTTON\_SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) structure to receive information on the button.</span></span> <span data-ttu-id="b5201-113">L’appelant est chargé d’allouer la mémoire pour la structure.</span><span class="sxs-lookup"><span data-stu-id="b5201-113">The caller is responsible for allocating the memory for the structure.</span></span> <span data-ttu-id="b5201-114">Définissez le membre de **masque** de cette structure pour déterminer les informations à recevoir.</span><span class="sxs-lookup"><span data-stu-id="b5201-114">Set the **mask** member of this structure to determine what information to receive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5201-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b5201-115">Return value</span></span>

<span data-ttu-id="b5201-116">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b5201-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5201-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b5201-117">Remarks</span></span>

<span data-ttu-id="b5201-118">Utilisez ce message uniquement avec les styles de boutons [**BS \_ SPLITBUTTON**](button-styles.md) et [**BS \_ DEFSPLITBUTTON**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b5201-118">Use this message only with the [**BS\_SPLITBUTTON**](button-styles.md) and [**BS\_DEFSPLITBUTTON**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5201-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5201-119">Requirements</span></span>



| <span data-ttu-id="b5201-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5201-120">Requirement</span></span> | <span data-ttu-id="b5201-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5201-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5201-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5201-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b5201-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5201-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b5201-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5201-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b5201-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5201-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b5201-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5201-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5201-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5201-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5201-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5201-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="b5201-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="b5201-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b5201-130">Styles de bouton</span><span class="sxs-lookup"><span data-stu-id="b5201-130">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="b5201-131">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="b5201-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b5201-132">Types de bouton</span><span class="sxs-lookup"><span data-stu-id="b5201-132">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





