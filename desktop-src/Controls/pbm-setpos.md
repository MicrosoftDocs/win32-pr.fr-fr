---
title: Message PBM_SETPOS (commctrl. h)
description: Définit la position actuelle d’une barre de progression et redessine la barre pour refléter la nouvelle position.
ms.assetid: 9ebeaa19-0f42-4af7-85d8-aae22498fd6f
keywords:
- PBM_SETPOS les contrôles de message Windows
topic_type:
- apiref
api_name:
- PBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a157f6a220f4932d39d13f08df79afa99d7348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513619"
---
# <a name="pbm_setpos-message"></a><span data-ttu-id="b3ac4-104">\_Message PBM SetPos</span><span class="sxs-lookup"><span data-stu-id="b3ac4-104">PBM\_SETPOS message</span></span>

<span data-ttu-id="b3ac4-105">Définit la position actuelle d’une barre de progression et redessine la barre pour refléter la nouvelle position.</span><span class="sxs-lookup"><span data-stu-id="b3ac4-105">Sets the current position for a progress bar and redraws the bar to reflect the new position.</span></span>

## <a name="parameters"></a><span data-ttu-id="b3ac4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3ac4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3ac4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b3ac4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b3ac4-108">Entier signé qui devient la nouvelle position.</span><span class="sxs-lookup"><span data-stu-id="b3ac4-108">Signed integer that becomes the new position.</span></span>

</dd> <dt>

<span data-ttu-id="b3ac4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b3ac4-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b3ac4-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b3ac4-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3ac4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3ac4-111">Return value</span></span>

<span data-ttu-id="b3ac4-112">Retourne la position précédente.</span><span class="sxs-lookup"><span data-stu-id="b3ac4-112">Returns the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3ac4-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b3ac4-113">Remarks</span></span>

<span data-ttu-id="b3ac4-114">Si *wParam* est en dehors de la plage du contrôle, la position est définie sur la limite la plus proche.</span><span class="sxs-lookup"><span data-stu-id="b3ac4-114">If *wParam* is outside the range of the control, the position is set to the closest boundary.</span></span>

<span data-ttu-id="b3ac4-115">N’envoyez pas ce message à un contrôle dont le style [**PBS est \_ défilant**](progress-bar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b3ac4-115">Do not send this message to a control that has the [**PBS\_MARQUEE**](progress-bar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3ac4-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3ac4-116">Requirements</span></span>



| <span data-ttu-id="b3ac4-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3ac4-117">Requirement</span></span> | <span data-ttu-id="b3ac4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3ac4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3ac4-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3ac4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b3ac4-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3ac4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b3ac4-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3ac4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b3ac4-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3ac4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b3ac4-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3ac4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3ac4-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3ac4-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





