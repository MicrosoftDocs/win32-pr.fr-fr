---
title: Message TBM_SETTOOLTIPS (commctrl. h)
description: Assigne un contrôle ToolTip à un contrôle TrackBar.
ms.assetid: 9bba1084-d04e-4631-a5cc-408849a14eb1
keywords:
- TBM_SETTOOLTIPS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d60c7e108db926b85e7d9e1167f33c1ed807a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464770"
---
# <a name="tbm_settooltips-message"></a><span data-ttu-id="dc4f2-104">\_Message TBM SETTOOLTIPS</span><span class="sxs-lookup"><span data-stu-id="dc4f2-104">TBM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="dc4f2-105">Assigne un contrôle ToolTip à un contrôle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-105">Assigns a tooltip control to a trackbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="dc4f2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc4f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc4f2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc4f2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc4f2-108">Handle vers un contrôle ToolTip existant.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-108">Handle to an existing tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="dc4f2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc4f2-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dc4f2-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc4f2-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dc4f2-111">Return value</span></span>

<span data-ttu-id="dc4f2-112">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-112">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc4f2-113">Notes</span><span class="sxs-lookup"><span data-stu-id="dc4f2-113">Remarks</span></span>

<span data-ttu-id="dc4f2-114">Lorsqu’un contrôle TrackBar est créé avec le style des [**\_ info-bulles tbs**](trackbar-control-styles.md) , il crée un contrôle ToolTip par défaut qui apparaît à côté du curseur, en affichant la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-114">When a trackbar control is created with the [**TBS\_TOOLTIPS**](trackbar-control-styles.md) style, it creates a default tooltip control that appears next to the slider, displaying the slider's current position.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc4f2-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc4f2-115">Requirements</span></span>



| <span data-ttu-id="dc4f2-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc4f2-116">Requirement</span></span> | <span data-ttu-id="dc4f2-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc4f2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc4f2-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc4f2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dc4f2-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc4f2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dc4f2-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc4f2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dc4f2-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc4f2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dc4f2-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc4f2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc4f2-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc4f2-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





