---
title: Message MCM_GETCURRENTVIEW (commctrl. h)
description: Obtient la vue actuelle du calendrier. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetCurrentView.
ms.assetid: 9c42ebf6-611e-4e50-9dcc-cf7fd63b32eb
keywords:
- MCM_GETCURRENTVIEW les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eebbd6a2b33043294b64b8b65308520b52dbe449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466491"
---
# <a name="mcm_getcurrentview-message"></a><span data-ttu-id="8354f-105">\_Message GETCURRENTVIEW MCM</span><span class="sxs-lookup"><span data-stu-id="8354f-105">MCM\_GETCURRENTVIEW message</span></span>

<span data-ttu-id="8354f-106">Obtient la vue actuelle du calendrier.</span><span class="sxs-lookup"><span data-stu-id="8354f-106">Gets the current view of the calendar.</span></span> <span data-ttu-id="8354f-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) .</span><span class="sxs-lookup"><span data-stu-id="8354f-107">You can send this message explicitly or by using the [**MonthCal\_GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8354f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8354f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8354f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8354f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8354f-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8354f-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8354f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8354f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8354f-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8354f-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8354f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8354f-113">Return value</span></span>

<span data-ttu-id="8354f-114">Affichage actuel.</span><span class="sxs-lookup"><span data-stu-id="8354f-114">Current view.</span></span> <span data-ttu-id="8354f-115">Une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="8354f-115">One of the following values.</span></span>



| <span data-ttu-id="8354f-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8354f-116">Return code</span></span>                                                                                  | <span data-ttu-id="8354f-117">Description</span><span class="sxs-lookup"><span data-stu-id="8354f-117">Description</span></span>              |
|----------------------------------------------------------------------------------------------|--------------------------|
| <dl> <span data-ttu-id="8354f-118"><dt>**MCMV \_ mois**</dt></span><span class="sxs-lookup"><span data-stu-id="8354f-118"><dt>**MCMV\_MONTH**</dt></span></span> </dl>   | <span data-ttu-id="8354f-119">Affichage mensuel.</span><span class="sxs-lookup"><span data-stu-id="8354f-119">Monthly view.</span></span><br/> |
| <dl> <span data-ttu-id="8354f-120"><dt>**MCMV \_ année**</dt></span><span class="sxs-lookup"><span data-stu-id="8354f-120"><dt>**MCMV\_YEAR**</dt></span></span> </dl>    | <span data-ttu-id="8354f-121">Vue annuelle.</span><span class="sxs-lookup"><span data-stu-id="8354f-121">Annual view.</span></span><br/>  |
| <dl> <span data-ttu-id="8354f-122"><dt>**MCMV \_ décennie**</dt></span><span class="sxs-lookup"><span data-stu-id="8354f-122"><dt>**MCMV\_DECADE**</dt></span></span> </dl>  | <span data-ttu-id="8354f-123">Vue décennie.</span><span class="sxs-lookup"><span data-stu-id="8354f-123">Decade view.</span></span><br/>  |
| <dl> <span data-ttu-id="8354f-124"><dt>**MCMV \_ siècle**</dt></span><span class="sxs-lookup"><span data-stu-id="8354f-124"><dt>**MCMV\_CENTURY**</dt></span></span> </dl> | <span data-ttu-id="8354f-125">Vue Century.</span><span class="sxs-lookup"><span data-stu-id="8354f-125">Century view.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8354f-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8354f-126">Requirements</span></span>



| <span data-ttu-id="8354f-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8354f-127">Requirement</span></span> | <span data-ttu-id="8354f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="8354f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8354f-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8354f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8354f-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8354f-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8354f-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8354f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8354f-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8354f-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8354f-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="8354f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8354f-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8354f-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





