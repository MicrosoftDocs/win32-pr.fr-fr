---
title: Message LVM_GETTOOLTIPS (commctrl. h)
description: Récupère le contrôle ToolTip que le contrôle List-View utilise pour afficher des info-bulles. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetToolTips.
ms.assetid: a3522c64-9498-40b8-9062-c112b7c8cacc
keywords:
- LVM_GETTOOLTIPS les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f409c85ed6157e8cfc837e5efa3a68488aec504
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466503"
---
# <a name="lvm_gettooltips-message"></a><span data-ttu-id="c13d5-105">\_Message GETTOOLTIPS LVM</span><span class="sxs-lookup"><span data-stu-id="c13d5-105">LVM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="c13d5-106">Récupère le contrôle ToolTip que le contrôle List-View utilise pour afficher des info-bulles.</span><span class="sxs-lookup"><span data-stu-id="c13d5-106">Retrieves the tooltip control that the list-view control uses to display tooltips.</span></span> <span data-ttu-id="c13d5-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) .</span><span class="sxs-lookup"><span data-stu-id="c13d5-107">You can send this message explicitly or use the [**ListView\_GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c13d5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c13d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c13d5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c13d5-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c13d5-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c13d5-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c13d5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c13d5-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c13d5-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c13d5-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c13d5-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c13d5-113">Return value</span></span>

<span data-ttu-id="c13d5-114">Retourne le handle du contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="c13d5-114">Returns the handle of the tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="c13d5-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c13d5-115">Requirements</span></span>



| <span data-ttu-id="c13d5-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c13d5-116">Requirement</span></span> | <span data-ttu-id="c13d5-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c13d5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c13d5-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c13d5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c13d5-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c13d5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c13d5-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c13d5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c13d5-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c13d5-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c13d5-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c13d5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c13d5-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c13d5-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c13d5-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c13d5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c13d5-125">**\_SETTOOLTIPS LVM**</span><span class="sxs-lookup"><span data-stu-id="c13d5-125">**LVM\_SETTOOLTIPS**</span></span>](lvm-settooltips.md)
</dt> </dl>

 

 





