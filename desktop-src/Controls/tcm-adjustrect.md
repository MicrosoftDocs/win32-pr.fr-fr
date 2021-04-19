---
title: Message TCM_ADJUSTRECT (commctrl. h)
description: Calcule la zone d’affichage d’un contrôle onglet en fonction d’un rectangle de fenêtre, ou calcule le rectangle de la fenêtre qui correspondrait à une zone d’affichage spécifiée. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl AdjustRect.
ms.assetid: 2f14201a-e4a3-4ae5-b9cf-4a674c52f24a
keywords:
- TCM_ADJUSTRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c1612a4f6c2fc436f858807fca59112c376a35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518109"
---
# <a name="tcm_adjustrect-message"></a><span data-ttu-id="f7db6-105">\_Message ADJUSTRECT TCM</span><span class="sxs-lookup"><span data-stu-id="f7db6-105">TCM\_ADJUSTRECT message</span></span>

<span data-ttu-id="f7db6-106">Calcule la zone d’affichage d’un contrôle onglet en fonction d’un rectangle de fenêtre, ou calcule le rectangle de la fenêtre qui correspondrait à une zone d’affichage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f7db6-106">Calculates a tab control's display area given a window rectangle, or calculates the window rectangle that would correspond to a specified display area.</span></span> <span data-ttu-id="f7db6-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ AdjustRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) .</span><span class="sxs-lookup"><span data-stu-id="f7db6-107">You can send this message explicitly or by using the [**TabCtrl\_AdjustRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f7db6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7db6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7db6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7db6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7db6-110">Opération à effectuer.</span><span class="sxs-lookup"><span data-stu-id="f7db6-110">Operation to perform.</span></span> <span data-ttu-id="f7db6-111">Si ce paramètre a la **valeur true**, *lParam* spécifie un rectangle d’affichage et reçoit le rectangle de fenêtre correspondant.</span><span class="sxs-lookup"><span data-stu-id="f7db6-111">If this parameter is **TRUE**, *lParam* specifies a display rectangle and receives the corresponding window rectangle.</span></span> <span data-ttu-id="f7db6-112">Si ce paramètre a la **valeur false**, *lParam* spécifie un rectangle de fenêtre et reçoit la zone d’affichage correspondante.</span><span class="sxs-lookup"><span data-stu-id="f7db6-112">If this parameter is **FALSE**, *lParam* specifies a window rectangle and receives the corresponding display area.</span></span>

</dd> <dt>

<span data-ttu-id="f7db6-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7db6-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7db6-114">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui spécifie le rectangle donné et reçoit le rectangle calculé.</span><span class="sxs-lookup"><span data-stu-id="f7db6-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the given rectangle and receives the calculated rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7db6-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f7db6-115">Return value</span></span>

<span data-ttu-id="f7db6-116">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="f7db6-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7db6-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f7db6-117">Remarks</span></span>

<span data-ttu-id="f7db6-118">Ce message s’applique uniquement aux contrôles d’onglet situés en haut.</span><span class="sxs-lookup"><span data-stu-id="f7db6-118">This message applies only to tab controls that are at the top.</span></span> <span data-ttu-id="f7db6-119">Elle ne s’applique pas aux contrôles d’onglet situés sur les côtés ou en bas.</span><span class="sxs-lookup"><span data-stu-id="f7db6-119">It does not apply to tab controls that are on the sides or bottom.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7db6-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7db6-120">Requirements</span></span>



| <span data-ttu-id="f7db6-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7db6-121">Requirement</span></span> | <span data-ttu-id="f7db6-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7db6-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7db6-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7db6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f7db6-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7db6-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f7db6-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7db6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f7db6-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7db6-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f7db6-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7db6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7db6-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7db6-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

