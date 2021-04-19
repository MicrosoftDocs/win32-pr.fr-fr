---
title: Message WM_DWMCOMPOSITIONCHANGED (winuser. h)
description: Informe toutes les fenêtres de niveau supérieur qui Gestionnaire de fenêtrage composition (DWM) ont été activées ou désactivées.
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_dwmcompositionchanged.htm
keywords:
- Message de WM_DWMCOMPOSITIONCHANGED Gestionnaire de fenêtrage
topic_type:
- apiref
api_name:
- WM_DWMCOMPOSITIONCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ec25f740e1a5d002edec2c1faeaaf068190583c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106532048"
---
# <a name="wm_dwmcompositionchanged-message"></a><span data-ttu-id="74ff2-104">\_Message WM DWMCOMPOSITIONCHANGED</span><span class="sxs-lookup"><span data-stu-id="74ff2-104">WM\_DWMCOMPOSITIONCHANGED message</span></span>

<span data-ttu-id="74ff2-105">Informe toutes les fenêtres de niveau supérieur qui Gestionnaire de fenêtrage composition (DWM) ont été activées ou désactivées.</span><span class="sxs-lookup"><span data-stu-id="74ff2-105">Informs all top-level windows that Desktop Window Manager (DWM) composition has been enabled or disabled.</span></span>

> [!Note]  
> <span data-ttu-id="74ff2-106">À compter de Windows 8, la composition DWM est toujours activée, ce qui signifie que ce message n’est pas envoyé, quelles que soient les modifications du mode vidéo.</span><span class="sxs-lookup"><span data-stu-id="74ff2-106">As of Windows 8, DWM composition is always enabled, so this message is not sent regardless of video mode changes.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="74ff2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74ff2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74ff2-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74ff2-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74ff2-109">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="74ff2-109">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="74ff2-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74ff2-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74ff2-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="74ff2-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74ff2-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="74ff2-112">Return value</span></span>

<span data-ttu-id="74ff2-113">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="74ff2-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="74ff2-114">Notes</span><span class="sxs-lookup"><span data-stu-id="74ff2-114">Remarks</span></span>

<span data-ttu-id="74ff2-115">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="74ff2-115">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

<span data-ttu-id="74ff2-116">La fonction [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled) peut être utilisée pour déterminer l’état actuel de la composition.</span><span class="sxs-lookup"><span data-stu-id="74ff2-116">The [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled) function can be used to determine the current composition state.</span></span>

## <a name="requirements"></a><span data-ttu-id="74ff2-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74ff2-117">Requirements</span></span>



| <span data-ttu-id="74ff2-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74ff2-118">Requirement</span></span> | <span data-ttu-id="74ff2-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="74ff2-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="74ff2-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74ff2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="74ff2-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74ff2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="74ff2-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74ff2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="74ff2-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74ff2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="74ff2-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="74ff2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="74ff2-125"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="74ff2-125"><dt>Winuser.h</dt></span></span> </dl> |



 

