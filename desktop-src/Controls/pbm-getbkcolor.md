---
title: Message PBM_GETBKCOLOR (commctrl. h)
description: Obtient la couleur d’arrière-plan de la barre de progression.
ms.assetid: 9526ed78-08d9-468f-831b-72bb7c8c92d1
keywords:
- PBM_GETBKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- PBM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2240025629bbcc242ea7ed47be2e3db42ae73b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843933"
---
# <a name="pbm_getbkcolor-message"></a><span data-ttu-id="0f421-104">\_Message PBM GETBKCOLOR</span><span class="sxs-lookup"><span data-stu-id="0f421-104">PBM\_GETBKCOLOR message</span></span>

<span data-ttu-id="0f421-105">Obtient la couleur d’arrière-plan de la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="0f421-105">Gets the background color of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="0f421-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f421-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f421-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f421-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0f421-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="0f421-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0f421-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f421-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0f421-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="0f421-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f421-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f421-111">Return value</span></span>

<span data-ttu-id="0f421-112">Retourne la couleur d’arrière-plan de la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="0f421-112">Returns the background color of the progress bar.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f421-113">Notes</span><span class="sxs-lookup"><span data-stu-id="0f421-113">Remarks</span></span>

<span data-ttu-id="0f421-114">Il s’agit de la couleur définie par le message [**PBM \_ SETBKCOLOR**](pbm-setbkcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="0f421-114">This is the color set by the [**PBM\_SETBKCOLOR**](pbm-setbkcolor.md) message.</span></span> <span data-ttu-id="0f421-115">La valeur par défaut est CLR \_ par défaut, qui est définie dans commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="0f421-115">The default value is CLR\_DEFAULT, which is defined in commctrl.h.</span></span>

<span data-ttu-id="0f421-116">Cette fonction affecte uniquement le mode classique, et non aucun style visuel.</span><span class="sxs-lookup"><span data-stu-id="0f421-116">This function only affects the classic mode, not any visual style.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f421-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f421-117">Requirements</span></span>



| <span data-ttu-id="0f421-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f421-118">Requirement</span></span> | <span data-ttu-id="0f421-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f421-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f421-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f421-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0f421-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f421-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0f421-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f421-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0f421-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f421-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0f421-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f421-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f421-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f421-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





