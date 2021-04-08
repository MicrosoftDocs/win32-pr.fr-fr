---
title: Message TBM_GETNUMTICS (commctrl. h)
description: Récupère le nombre de graduations dans un TrackBar.
ms.assetid: 3c3f7ebb-a544-474c-ba14-68eae543ee38
keywords:
- TBM_GETNUMTICS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_GETNUMTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 712e1a0190334ec279f28a68959f3e3d5d5ffd1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941841"
---
# <a name="tbm_getnumtics-message"></a><span data-ttu-id="bcf28-104">\_Message TBM GETNUMTICS</span><span class="sxs-lookup"><span data-stu-id="bcf28-104">TBM\_GETNUMTICS message</span></span>

<span data-ttu-id="bcf28-105">Récupère le nombre de graduations dans un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="bcf28-105">Retrieves the number of tick marks in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="bcf28-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bcf28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcf28-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bcf28-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bcf28-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="bcf28-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bcf28-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bcf28-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bcf28-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="bcf28-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcf28-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bcf28-111">Return value</span></span>

<span data-ttu-id="bcf28-112">Si aucun [indicateur de graduation](trackbar-control-styles.md) n’est défini, la valeur 2 est retournée pour les graduations de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="bcf28-112">If no [tick flag](trackbar-control-styles.md) is set, it returns 2 for the beginning and ending ticks.</span></span> <span data-ttu-id="bcf28-113">Si la valeur de [**tbs \_ notiques**](trackbar-control-styles.md) est définie, elle retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="bcf28-113">If [**TBS\_NOTICKS**](trackbar-control-styles.md) is set, it returns zero.</span></span> <span data-ttu-id="bcf28-114">Sinon, elle prend la différence entre les valeurs minimale et maximale de la plage, se divise par la fréquence de graduation et ajoute 2.</span><span class="sxs-lookup"><span data-stu-id="bcf28-114">Otherwise, it takes the difference between the range minimum and maximum, divides by the tick frequency, and adds 2.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcf28-115">Notes</span><span class="sxs-lookup"><span data-stu-id="bcf28-115">Remarks</span></span>

<span data-ttu-id="bcf28-116">Le message **TBM \_ GETNUMTICS** compte toutes les graduations, y compris les première et dernière graduations créées par le TrackBar.</span><span class="sxs-lookup"><span data-stu-id="bcf28-116">The **TBM\_GETNUMTICS** message counts all of the tick marks, including the first and last tick marks created by the trackbar.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcf28-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcf28-117">Requirements</span></span>



| <span data-ttu-id="bcf28-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bcf28-118">Requirement</span></span> | <span data-ttu-id="bcf28-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="bcf28-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf28-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcf28-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bcf28-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bcf28-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bcf28-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcf28-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bcf28-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bcf28-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bcf28-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="bcf28-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcf28-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcf28-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





