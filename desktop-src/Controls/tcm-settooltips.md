---
title: Message TCM_SETTOOLTIPS (commctrl. h)
description: Assigne un contrôle ToolTip à un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetToolTips.
ms.assetid: c1b173b1-9da6-441a-a2b6-3875e2c343f8
keywords:
- TCM_SETTOOLTIPS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e00166fb97c49c33b22811d28b79165bed4e9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739869"
---
# <a name="tcm_settooltips-message"></a><span data-ttu-id="3ea5f-105">\_Message SETTOOLTIPS TCM</span><span class="sxs-lookup"><span data-stu-id="3ea5f-105">TCM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="3ea5f-106">Assigne un contrôle ToolTip à un contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="3ea5f-106">Assigns a tooltip control to a tab control.</span></span> <span data-ttu-id="3ea5f-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips) .</span><span class="sxs-lookup"><span data-stu-id="3ea5f-107">You can send this message explicitly or by using the [**TabCtrl\_SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3ea5f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ea5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ea5f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3ea5f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3ea5f-110">Handle du contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="3ea5f-110">Handle to the tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="3ea5f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3ea5f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3ea5f-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="3ea5f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ea5f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3ea5f-113">Return value</span></span>

<span data-ttu-id="3ea5f-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="3ea5f-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ea5f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3ea5f-115">Remarks</span></span>

<span data-ttu-id="3ea5f-116">Vous pouvez récupérer le contrôle ToolTip associé à un contrôle onglet à l’aide du message [**\_ GETTOOLTIPS TCM**](tcm-gettooltips.md) .</span><span class="sxs-lookup"><span data-stu-id="3ea5f-116">You can retrieve the tooltip control associated with a tab control by using the [**TCM\_GETTOOLTIPS**](tcm-gettooltips.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ea5f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ea5f-117">Requirements</span></span>



| <span data-ttu-id="3ea5f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ea5f-118">Requirement</span></span> | <span data-ttu-id="3ea5f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ea5f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ea5f-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ea5f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3ea5f-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ea5f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3ea5f-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ea5f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3ea5f-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ea5f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3ea5f-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="3ea5f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ea5f-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ea5f-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





