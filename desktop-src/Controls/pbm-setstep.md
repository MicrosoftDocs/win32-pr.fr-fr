---
title: Message PBM_SETSTEP (commctrl. h)
description: Spécifie l’incrément de l’étape d’une barre de progression. L’incrément d’étape correspond à la quantité d’augmentation de la position actuelle de la barre de progression à chaque fois qu’elle reçoit un \_ message PBM STEPIT. Par défaut, l’incrément de l’étape est défini sur 10.
ms.assetid: 75c1085b-6c7a-4c44-9a12-f9bf21f7d945
keywords:
- PBM_SETSTEP les contrôles de message Windows
topic_type:
- apiref
api_name:
- PBM_SETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1240d09aeadcd7994187704d0b5a4630ab1b7afb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510762"
---
# <a name="pbm_setstep-message"></a><span data-ttu-id="c3599-106">\_Message PBM SETSTEP</span><span class="sxs-lookup"><span data-stu-id="c3599-106">PBM\_SETSTEP message</span></span>

<span data-ttu-id="c3599-107">Spécifie l’incrément de l’étape d’une barre de progression.</span><span class="sxs-lookup"><span data-stu-id="c3599-107">Specifies the step increment for a progress bar.</span></span> <span data-ttu-id="c3599-108">L’incrément d’étape correspond à la quantité d’augmentation de la position actuelle de la barre de progression à chaque fois qu’elle reçoit un message [**PBM \_ STEPIT**](pbm-stepit.md) .</span><span class="sxs-lookup"><span data-stu-id="c3599-108">The step increment is the amount by which the progress bar increases its current position whenever it receives a [**PBM\_STEPIT**](pbm-stepit.md) message.</span></span> <span data-ttu-id="c3599-109">Par défaut, l’incrément de l’étape est défini sur 10.</span><span class="sxs-lookup"><span data-stu-id="c3599-109">By default, the step increment is set to 10.</span></span>

## <a name="parameters"></a><span data-ttu-id="c3599-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3599-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3599-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3599-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3599-112">Nouvel incrément de l’étape.</span><span class="sxs-lookup"><span data-stu-id="c3599-112">New step increment.</span></span>

</dd> <dt>

<span data-ttu-id="c3599-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3599-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c3599-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c3599-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3599-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3599-115">Return value</span></span>

<span data-ttu-id="c3599-116">Retourne l’incrément de l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="c3599-116">Returns the previous step increment.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3599-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3599-117">Requirements</span></span>



| <span data-ttu-id="c3599-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3599-118">Requirement</span></span> | <span data-ttu-id="c3599-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3599-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3599-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3599-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c3599-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3599-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3599-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3599-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c3599-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3599-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c3599-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3599-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3599-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3599-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





