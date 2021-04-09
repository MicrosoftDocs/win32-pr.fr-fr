---
title: Message TTM_TRACKPOSITION (commctrl. h)
description: Définit la position d’une info-bulle de suivi.
ms.assetid: 9eb7c86c-78e6-442a-ad77-5fb919cab591
keywords:
- TTM_TRACKPOSITION les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_TRACKPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6eab8184049d8bf876a7e782b9adc2091d5fac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033011"
---
# <a name="ttm_trackposition-message"></a><span data-ttu-id="a0794-104">\_Message atténuation TRACKPOSITION</span><span class="sxs-lookup"><span data-stu-id="a0794-104">TTM\_TRACKPOSITION message</span></span>

<span data-ttu-id="a0794-105">Définit la position d’une info-bulle de suivi.</span><span class="sxs-lookup"><span data-stu-id="a0794-105">Sets the position of a tracking tooltip.</span></span>

## <a name="parameters"></a><span data-ttu-id="a0794-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0794-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0794-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a0794-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0794-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="a0794-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a0794-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0794-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0794-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la coordonnée x du point auquel l’info-bulle de suivi sera affichée, en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="a0794-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the x-coordinate of the point at which the tracking tooltip will be displayed, in screen coordinates.</span></span> <span data-ttu-id="a0794-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la coordonnée y du point auquel l’info-bulle de suivi sera affichée, en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="a0794-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the y-coordinate of the point at which the tracking tooltip will be displayed, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0794-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a0794-112">Return value</span></span>

<span data-ttu-id="a0794-113">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="a0794-113">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0794-114">Notes</span><span class="sxs-lookup"><span data-stu-id="a0794-114">Remarks</span></span>

<span data-ttu-id="a0794-115">Le contrôle ToolTip choisit où afficher la fenêtre d’info-bulle en fonction des coordonnées que vous fournissez avec ce message.</span><span class="sxs-lookup"><span data-stu-id="a0794-115">The tooltip control chooses where to display the tooltip window based on the coordinates you provide with this message.</span></span> <span data-ttu-id="a0794-116">La fenêtre d’info-bulle s’affiche alors à côté de l’outil auquel elle correspond.</span><span class="sxs-lookup"><span data-stu-id="a0794-116">This causes the tooltip window to appear beside the tool to which it corresponds.</span></span> <span data-ttu-id="a0794-117">Pour que les fenêtres d’info-bulle s’affichent à des coordonnées spécifiques, incluez l' \_ indicateur de l’Absolute dans le membre **uFlags** de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) lors de l’ajout de l’outil.</span><span class="sxs-lookup"><span data-stu-id="a0794-117">To have tooltip windows displayed at specific coordinates, include the TTF\_ABSOLUTE flag in the **uFlags** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure when adding the tool.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0794-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0794-118">Requirements</span></span>



| <span data-ttu-id="a0794-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0794-119">Requirement</span></span> | <span data-ttu-id="a0794-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0794-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0794-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0794-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a0794-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0794-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a0794-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0794-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a0794-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0794-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a0794-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="a0794-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0794-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0794-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0794-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0794-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="a0794-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="a0794-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a0794-129">**ATTÉNUATION \_ TRACKACTIVATE**</span><span class="sxs-lookup"><span data-stu-id="a0794-129">**TTM\_TRACKACTIVATE**</span></span>](ttm-trackactivate.md)
</dt> <dt>

<span data-ttu-id="a0794-130">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="a0794-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a0794-131">Utilisation des contrôles ToolTip</span><span class="sxs-lookup"><span data-stu-id="a0794-131">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

