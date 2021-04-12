---
title: Message PBM_GETBARCOLOR (commctrl. h)
description: Obtient la couleur de la barre de progression.
ms.assetid: d046f7e4-e21e-4dd9-a7be-2bf820c3c492
keywords:
- PBM_GETBARCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- PBM_GETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35586d3483d1d487f740a1a3d991c884c814f452
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104800"
---
# <a name="pbm_getbarcolor-message"></a><span data-ttu-id="eda30-104">\_Message PBM GETBARCOLOR</span><span class="sxs-lookup"><span data-stu-id="eda30-104">PBM\_GETBARCOLOR message</span></span>

<span data-ttu-id="eda30-105">Obtient la couleur de la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="eda30-105">Gets the color of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="eda30-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eda30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eda30-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eda30-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eda30-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="eda30-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eda30-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eda30-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="eda30-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="eda30-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eda30-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eda30-111">Return value</span></span>

<span data-ttu-id="eda30-112">Retourne la couleur de la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="eda30-112">Returns the color of the progress bar.</span></span>

## <a name="remarks"></a><span data-ttu-id="eda30-113">Notes</span><span class="sxs-lookup"><span data-stu-id="eda30-113">Remarks</span></span>

<span data-ttu-id="eda30-114">Il s’agit de la couleur définie par le message [**PBM \_ SETBARCOLOR**](pbm-setbarcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="eda30-114">This is the color set by the [**PBM\_SETBARCOLOR**](pbm-setbarcolor.md) message.</span></span> <span data-ttu-id="eda30-115">La valeur par défaut est CLR \_ par défaut, qui est définie dans commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="eda30-115">The default value is CLR\_DEFAULT, which is defined in commctrl.h.</span></span>

<span data-ttu-id="eda30-116">Cette fonction affecte uniquement le mode classique, et non aucun style visuel.</span><span class="sxs-lookup"><span data-stu-id="eda30-116">This function only affects the classic mode, not any visual style.</span></span>

## <a name="requirements"></a><span data-ttu-id="eda30-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eda30-117">Requirements</span></span>



| <span data-ttu-id="eda30-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eda30-118">Requirement</span></span> | <span data-ttu-id="eda30-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="eda30-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eda30-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eda30-120">Minimum supported client</span></span><br/> | <span data-ttu-id="eda30-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eda30-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eda30-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eda30-122">Minimum supported server</span></span><br/> | <span data-ttu-id="eda30-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eda30-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eda30-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="eda30-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="eda30-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eda30-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





