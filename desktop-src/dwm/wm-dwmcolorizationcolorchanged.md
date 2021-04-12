---
title: Message WM_DWMCOLORIZATIONCOLORCHANGED (winuser. h)
description: Informe toutes les fenêtres de niveau supérieur que la couleur de colorisation a changé.
ms.assetid: 6118d41b-f0b4-4034-aa98-d8757f18ca0d
keywords:
- Message de WM_DWMCOLORIZATIONCOLORCHANGED Gestionnaire de fenêtrage
topic_type:
- apiref
api_name:
- WM_DWMCOLORIZATIONCOLORCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc99d42fe2d4af77fa4534945a3396dda9c02b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103942"
---
# <a name="wm_dwmcolorizationcolorchanged-message"></a><span data-ttu-id="13ee4-104">\_Message WM DWMCOLORIZATIONCOLORCHANGED</span><span class="sxs-lookup"><span data-stu-id="13ee4-104">WM\_DWMCOLORIZATIONCOLORCHANGED message</span></span>

<span data-ttu-id="13ee4-105">Informe toutes les fenêtres de niveau supérieur que la couleur de colorisation a changé.</span><span class="sxs-lookup"><span data-stu-id="13ee4-105">Informs all top-level windows that the colorization color has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="13ee4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13ee4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13ee4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="13ee4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13ee4-108">Spécifie la nouvelle couleur de colorisation.</span><span class="sxs-lookup"><span data-stu-id="13ee4-108">Specifies the new colorization color.</span></span> <span data-ttu-id="13ee4-109">Le format de couleur est 0xAARRGGBB.</span><span class="sxs-lookup"><span data-stu-id="13ee4-109">The color format is 0xAARRGGBB.</span></span>

</dd> <dt>

<span data-ttu-id="13ee4-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="13ee4-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13ee4-111">Spécifie si la nouvelle couleur est mélangée avec l’opacité.</span><span class="sxs-lookup"><span data-stu-id="13ee4-111">Specifies whether the new color is blended with opacity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13ee4-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="13ee4-112">Return value</span></span>

<span data-ttu-id="13ee4-113">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="13ee4-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="13ee4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="13ee4-114">Remarks</span></span>

<span data-ttu-id="13ee4-115">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="13ee4-115">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

<span data-ttu-id="13ee4-116">[**DwmGetColorizationColor**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) est utilisé pour déterminer la valeur de couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="13ee4-116">[**DwmGetColorizationColor**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) is used to determine the current color value.</span></span>

## <a name="requirements"></a><span data-ttu-id="13ee4-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13ee4-117">Requirements</span></span>



| <span data-ttu-id="13ee4-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13ee4-118">Requirement</span></span> | <span data-ttu-id="13ee4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="13ee4-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="13ee4-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13ee4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="13ee4-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="13ee4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="13ee4-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13ee4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="13ee4-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="13ee4-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="13ee4-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="13ee4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="13ee4-125"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="13ee4-125"><dt>Winuser.h</dt></span></span> </dl> |



 

