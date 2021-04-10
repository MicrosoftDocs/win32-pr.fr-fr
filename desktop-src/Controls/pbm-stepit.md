---
title: Message PBM_STEPIT (commctrl. h)
description: Avance la position actuelle d’une barre de progression à l’aide de l’incrément de l’étape et redessine la barre pour refléter la nouvelle position. Une application définit l’incrément d’étape en envoyant le \_ message PBM SETSTEP.
ms.assetid: fd9947f6-7a48-4207-b691-b7db78eb8a85
keywords:
- PBM_STEPIT les contrôles de message Windows
topic_type:
- apiref
api_name:
- PBM_STEPIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0d4aee387e8f929aaaaf19d947422b95ca9528
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942468"
---
# <a name="pbm_stepit-message"></a><span data-ttu-id="d57fe-105">\_Message PBM STEPIT</span><span class="sxs-lookup"><span data-stu-id="d57fe-105">PBM\_STEPIT message</span></span>

<span data-ttu-id="d57fe-106">Avance la position actuelle d’une barre de progression à l’aide de l’incrément de l’étape et redessine la barre pour refléter la nouvelle position.</span><span class="sxs-lookup"><span data-stu-id="d57fe-106">Advances the current position for a progress bar by the step increment and redraws the bar to reflect the new position.</span></span> <span data-ttu-id="d57fe-107">Une application définit l’incrément d’étape en envoyant le message [**PBM \_ SETSTEP**](pbm-setstep.md) .</span><span class="sxs-lookup"><span data-stu-id="d57fe-107">An application sets the step increment by sending the [**PBM\_SETSTEP**](pbm-setstep.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="d57fe-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d57fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d57fe-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d57fe-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d57fe-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="d57fe-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d57fe-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d57fe-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d57fe-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="d57fe-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d57fe-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d57fe-113">Return value</span></span>

<span data-ttu-id="d57fe-114">Retourne la position précédente.</span><span class="sxs-lookup"><span data-stu-id="d57fe-114">Returns the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="d57fe-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d57fe-115">Remarks</span></span>

<span data-ttu-id="d57fe-116">Lorsque la position dépasse la valeur de plage maximale, ce message réinitialise la position actuelle afin que l’indicateur de progression recommence à partir du début.</span><span class="sxs-lookup"><span data-stu-id="d57fe-116">When the position exceeds the maximum range value, this message resets the current position so that the progress indicator starts over again from the beginning.</span></span>

## <a name="requirements"></a><span data-ttu-id="d57fe-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d57fe-117">Requirements</span></span>



| <span data-ttu-id="d57fe-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d57fe-118">Requirement</span></span> | <span data-ttu-id="d57fe-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d57fe-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d57fe-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d57fe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d57fe-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d57fe-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d57fe-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d57fe-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d57fe-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d57fe-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d57fe-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d57fe-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d57fe-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d57fe-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





