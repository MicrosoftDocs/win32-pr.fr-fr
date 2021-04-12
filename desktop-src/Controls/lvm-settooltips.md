---
title: Message LVM_SETTOOLTIPS (commctrl. h)
description: Définit le contrôle ToolTip que le contrôle List-View utilisera pour afficher des info-bulles. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView SetToolTips.
ms.assetid: 5b4335a4-e9f0-4b13-b00b-516af3b60bf1
keywords:
- LVM_SETTOOLTIPS les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff749c24a35cf73de2d75b8a3b516197b57aac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464879"
---
# <a name="lvm_settooltips-message"></a><span data-ttu-id="e75ac-105">\_Message SETTOOLTIPS LVM</span><span class="sxs-lookup"><span data-stu-id="e75ac-105">LVM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="e75ac-106">Définit le contrôle ToolTip que le contrôle List-View utilisera pour afficher des info-bulles.</span><span class="sxs-lookup"><span data-stu-id="e75ac-106">Sets the tooltip control that the list-view control will use to display tooltips.</span></span> <span data-ttu-id="e75ac-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips) .</span><span class="sxs-lookup"><span data-stu-id="e75ac-107">You can send this message explicitly or use the [**ListView\_SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e75ac-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e75ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e75ac-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e75ac-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e75ac-110">Handle du contrôle ToolTip à définir.</span><span class="sxs-lookup"><span data-stu-id="e75ac-110">Handle to the tooltip control to be set.</span></span></dd> <dt>

<span data-ttu-id="e75ac-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e75ac-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e75ac-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="e75ac-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e75ac-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e75ac-113">Return value</span></span>

<span data-ttu-id="e75ac-114">Retourne le handle du contrôle ToolTip précédent.</span><span class="sxs-lookup"><span data-stu-id="e75ac-114">Returns the handle to the previous tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="e75ac-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e75ac-115">Requirements</span></span>



| <span data-ttu-id="e75ac-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e75ac-116">Requirement</span></span> | <span data-ttu-id="e75ac-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e75ac-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e75ac-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e75ac-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e75ac-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e75ac-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e75ac-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e75ac-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e75ac-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e75ac-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e75ac-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e75ac-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e75ac-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e75ac-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e75ac-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e75ac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e75ac-125">**\_GETTOOLTIPS LVM**</span><span class="sxs-lookup"><span data-stu-id="e75ac-125">**LVM\_GETTOOLTIPS**</span></span>](lvm-gettooltips.md)
</dt> </dl>

 

 





