---
title: Message PBM_GETSTEP (commctrl. h)
description: Récupère l’incrément d’étape d’une barre de progression. L’incrément d’étape correspond à la quantité d’augmentation de la position actuelle de la barre de progression à chaque fois qu’elle reçoit un \_ message PBM STEPIT. Par défaut, l’incrément de l’étape est défini sur 10.
ms.assetid: 0cf3052a-cf86-4c0e-ad59-ddab7c6e3602
keywords:
- PBM_GETSTEP les contrôles de message Windows
topic_type:
- apiref
api_name:
- PBM_GETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dcc4adb18d2b60d2936c2cdc7ab79d00389b3ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942472"
---
# <a name="pbm_getstep-message"></a><span data-ttu-id="61029-106">\_Message PBM GETSTEP</span><span class="sxs-lookup"><span data-stu-id="61029-106">PBM\_GETSTEP message</span></span>

<span data-ttu-id="61029-107">Récupère l’incrément d’étape d’une barre de progression.</span><span class="sxs-lookup"><span data-stu-id="61029-107">Retrieves the step increment from a progress bar.</span></span> <span data-ttu-id="61029-108">L’incrément d’étape correspond à la quantité d’augmentation de la position actuelle de la barre de progression à chaque fois qu’elle reçoit un message [**PBM \_ STEPIT**](pbm-stepit.md) .</span><span class="sxs-lookup"><span data-stu-id="61029-108">The step increment is the amount by which the progress bar increases its current position whenever it receives a [**PBM\_STEPIT**](pbm-stepit.md) message.</span></span> <span data-ttu-id="61029-109">Par défaut, l’incrément de l’étape est défini sur 10.</span><span class="sxs-lookup"><span data-stu-id="61029-109">By default, the step increment is set to 10.</span></span>

## <a name="parameters"></a><span data-ttu-id="61029-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61029-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61029-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="61029-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="61029-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="61029-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="61029-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="61029-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="61029-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="61029-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61029-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="61029-115">Return value</span></span>

<span data-ttu-id="61029-116">Retourne l’incrément de l’étape actuelle.</span><span class="sxs-lookup"><span data-stu-id="61029-116">Returns the current step increment.</span></span>

## <a name="requirements"></a><span data-ttu-id="61029-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61029-117">Requirements</span></span>



| <span data-ttu-id="61029-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61029-118">Requirement</span></span> | <span data-ttu-id="61029-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="61029-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61029-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61029-120">Minimum supported client</span></span><br/> | <span data-ttu-id="61029-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61029-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61029-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61029-122">Minimum supported server</span></span><br/> | <span data-ttu-id="61029-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61029-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61029-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="61029-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="61029-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="61029-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





