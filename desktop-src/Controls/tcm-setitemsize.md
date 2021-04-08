---
title: Message TCM_SETITEMSIZE (commctrl. h)
description: Définit la largeur et la hauteur des onglets dans un contrôle onglet à largeur fixe ou owner-drawn. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetItemSize.
ms.assetid: 3935d686-f8bc-41fb-b025-04120cf03f02
keywords:
- TCM_SETITEMSIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_SETITEMSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e306af3f6462507a181de91104169c5ac7d6ce14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843049"
---
# <a name="tcm_setitemsize-message"></a><span data-ttu-id="6fc3c-105">\_Message SETITEMSIZE TCM</span><span class="sxs-lookup"><span data-stu-id="6fc3c-105">TCM\_SETITEMSIZE message</span></span>

<span data-ttu-id="6fc3c-106">Définit la largeur et la hauteur des onglets dans un contrôle onglet à largeur fixe ou owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="6fc3c-106">Sets the width and height of tabs in a fixed-width or owner-drawn tab control.</span></span> <span data-ttu-id="6fc3c-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ SetItemSize**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize) .</span><span class="sxs-lookup"><span data-stu-id="6fc3c-107">You can send this message explicitly or by using the [**TabCtrl\_SetItemSize**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6fc3c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6fc3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fc3c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6fc3c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6fc3c-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="6fc3c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6fc3c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6fc3c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6fc3c-112">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est une valeur **int** qui spécifie la nouvelle largeur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="6fc3c-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is an **INT** value that specifies the new width, in pixels.</span></span> <span data-ttu-id="6fc3c-113">Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) est une valeur **int** qui spécifie la nouvelle hauteur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="6fc3c-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is an **INT** value that specifies the new height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fc3c-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6fc3c-114">Return value</span></span>

<span data-ttu-id="6fc3c-115">Retourne l’ancienne largeur et la hauteur.</span><span class="sxs-lookup"><span data-stu-id="6fc3c-115">Returns the old width and height.</span></span> <span data-ttu-id="6fc3c-116">La largeur est dans le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) de la valeur de retour et la hauteur est dans le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6fc3c-116">The width is in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of the return value, and the height is in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span>

## <a name="remarks"></a><span data-ttu-id="6fc3c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6fc3c-117">Remarks</span></span>

<span data-ttu-id="6fc3c-118">Si la largeur est définie sur une valeur inférieure à la largeur d’image définie par [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create), la largeur de l’onglet est définie sur la valeur la plus faible qui est supérieure à la largeur de l’image.</span><span class="sxs-lookup"><span data-stu-id="6fc3c-118">If the width is set to a value less than the image width set by [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create), the width of the tab is set to the lowest value that is greater than the image width.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fc3c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fc3c-119">Requirements</span></span>



| <span data-ttu-id="6fc3c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fc3c-120">Requirement</span></span> | <span data-ttu-id="6fc3c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fc3c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6fc3c-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fc3c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6fc3c-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fc3c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6fc3c-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fc3c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6fc3c-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fc3c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6fc3c-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="6fc3c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fc3c-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fc3c-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

