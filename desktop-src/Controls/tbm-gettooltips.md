---
title: Message TBM_GETTOOLTIPS (commctrl. h)
description: Récupère le handle du contrôle ToolTip assigné au TrackBar, le cas échéant.
ms.assetid: 30efef12-1aec-4635-94a7-1843db404c4f
keywords:
- TBM_GETTOOLTIPS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02b0b757b1aabfef2c9df2e80ca9f96542ba4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843601"
---
# <a name="tbm_gettooltips-message"></a><span data-ttu-id="3acbb-104">\_Message TBM GETTOOLTIPS</span><span class="sxs-lookup"><span data-stu-id="3acbb-104">TBM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="3acbb-105">Récupère le handle du contrôle ToolTip assigné au TrackBar, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="3acbb-105">Retrieves the handle to the tooltip control assigned to the trackbar, if any.</span></span>

## <a name="parameters"></a><span data-ttu-id="3acbb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3acbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3acbb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3acbb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3acbb-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="3acbb-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3acbb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3acbb-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3acbb-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="3acbb-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3acbb-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3acbb-111">Return value</span></span>

<span data-ttu-id="3acbb-112">Retourne le handle du contrôle ToolTip assigné au TrackBar, ou **null** si les info-bulles ne sont pas utilisées.</span><span class="sxs-lookup"><span data-stu-id="3acbb-112">Returns the handle to the tooltip control assigned to the trackbar, or **NULL** if tooltips are not in use.</span></span> <span data-ttu-id="3acbb-113">Si le contrôle TrackBar n’utilise pas le style des [**\_ info-bulles tbs**](trackbar-control-styles.md) , la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="3acbb-113">If the trackbar control does not use the [**TBS\_TOOLTIPS**](trackbar-control-styles.md) style, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3acbb-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3acbb-114">Requirements</span></span>



| <span data-ttu-id="3acbb-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3acbb-115">Requirement</span></span> | <span data-ttu-id="3acbb-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3acbb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3acbb-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3acbb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3acbb-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3acbb-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3acbb-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3acbb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3acbb-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3acbb-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3acbb-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="3acbb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3acbb-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3acbb-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





