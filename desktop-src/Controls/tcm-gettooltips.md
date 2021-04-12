---
title: Message TCM_GETTOOLTIPS (commctrl. h)
description: Récupère le handle du contrôle ToolTip associé à un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl GetToolTips.
ms.assetid: d7dcca4f-8629-4eeb-844f-b3171438f528
keywords:
- TCM_GETTOOLTIPS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e49334a1fa7124dd6e7a0f0b739cd1ebd24b51b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105736"
---
# <a name="tcm_gettooltips-message"></a><span data-ttu-id="eaa9d-105">\_Message GETTOOLTIPS TCM</span><span class="sxs-lookup"><span data-stu-id="eaa9d-105">TCM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="eaa9d-106">Récupère le handle du contrôle ToolTip associé à un contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="eaa9d-106">Retrieves the handle to the tooltip control associated with a tab control.</span></span> <span data-ttu-id="eaa9d-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips) .</span><span class="sxs-lookup"><span data-stu-id="eaa9d-107">You can send this message explicitly or by using the [**TabCtrl\_GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="eaa9d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eaa9d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaa9d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eaa9d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eaa9d-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="eaa9d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eaa9d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eaa9d-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="eaa9d-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="eaa9d-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaa9d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eaa9d-113">Return value</span></span>

<span data-ttu-id="eaa9d-114">Retourne le handle du contrôle ToolTip en cas de réussite, ou **null** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="eaa9d-114">Returns the handle to the tooltip control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaa9d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="eaa9d-115">Remarks</span></span>

<span data-ttu-id="eaa9d-116">Un contrôle onglet crée un contrôle ToolTip s’il a le [**style \_ info-bulles TCS**](tab-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="eaa9d-116">A tab control creates a tooltip control if it has the [**TCS\_TOOLTIPS**](tab-control-styles.md) style.</span></span> <span data-ttu-id="eaa9d-117">Vous pouvez également assigner un contrôle ToolTip à un contrôle onglet à l’aide du message [**\_ SETTOOLTIPS TCM**](tcm-settooltips.md) .</span><span class="sxs-lookup"><span data-stu-id="eaa9d-117">You can also assign a tooltip control to a tab control by using the [**TCM\_SETTOOLTIPS**](tcm-settooltips.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaa9d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eaa9d-118">Requirements</span></span>



| <span data-ttu-id="eaa9d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eaa9d-119">Requirement</span></span> | <span data-ttu-id="eaa9d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="eaa9d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eaa9d-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eaa9d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="eaa9d-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eaa9d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eaa9d-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eaa9d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="eaa9d-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eaa9d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eaa9d-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="eaa9d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaa9d-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eaa9d-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





