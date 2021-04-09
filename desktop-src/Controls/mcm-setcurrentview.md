---
title: Message MCM_SETCURRENTVIEW (commctrl. h)
description: Définit la vue actuelle du calendrier. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal SetCurrentView.
ms.assetid: 26ccbb80-0dba-4241-a2eb-b79000fc3618
keywords:
- MCM_SETCURRENTVIEW les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_SETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d383c984932c19805f452cb39841c2edf36809b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942764"
---
# <a name="mcm_setcurrentview-message"></a><span data-ttu-id="08979-105">\_Message SETCURRENTVIEW MCM</span><span class="sxs-lookup"><span data-stu-id="08979-105">MCM\_SETCURRENTVIEW message</span></span>

<span data-ttu-id="08979-106">Définit la vue actuelle du calendrier.</span><span class="sxs-lookup"><span data-stu-id="08979-106">Sets the current view of the calendar.</span></span> <span data-ttu-id="08979-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ SetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview) .</span><span class="sxs-lookup"><span data-stu-id="08979-107">You can send this message explicitly or by using the [**MonthCal\_SetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="08979-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08979-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08979-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="08979-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08979-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="08979-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="08979-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08979-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08979-112">Nouvelle vue.</span><span class="sxs-lookup"><span data-stu-id="08979-112">New view.</span></span> <span data-ttu-id="08979-113">Une des constantes suivantes.</span><span class="sxs-lookup"><span data-stu-id="08979-113">One of the following constants.</span></span>



| <span data-ttu-id="08979-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="08979-114">Value</span></span>                                                                                                                                                      | <span data-ttu-id="08979-115">Signification</span><span class="sxs-lookup"><span data-stu-id="08979-115">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="MCMV_MONTH"></span><span id="mcmv_month"></span><dl> <span data-ttu-id="08979-116"><dt>**MCMV \_ mois**</dt></span><span class="sxs-lookup"><span data-stu-id="08979-116"><dt>**MCMV\_MONTH**</dt></span></span> </dl>       | <span data-ttu-id="08979-117">Affichage mensuel.</span><span class="sxs-lookup"><span data-stu-id="08979-117">Monthly view.</span></span><br/> |
| <span id="MCMV_YEAR"></span><span id="mcmv_year"></span><dl> <span data-ttu-id="08979-118"><dt>**MCMV \_ année**</dt></span><span class="sxs-lookup"><span data-stu-id="08979-118"><dt>**MCMV\_YEAR**</dt></span></span> </dl>          | <span data-ttu-id="08979-119">Vue annuelle.</span><span class="sxs-lookup"><span data-stu-id="08979-119">Annual view.</span></span><br/>  |
| <span id="MCMV_DECADE"></span><span id="mcmv_decade"></span><dl> <span data-ttu-id="08979-120"><dt>**MCMV \_ décennie**</dt></span><span class="sxs-lookup"><span data-stu-id="08979-120"><dt>**MCMV\_DECADE**</dt></span></span> </dl>    | <span data-ttu-id="08979-121">Vue décennie.</span><span class="sxs-lookup"><span data-stu-id="08979-121">Decade view.</span></span><br/>  |
| <span id="MCMV_CENTURY"></span><span id="mcmv_century"></span><dl> <span data-ttu-id="08979-122"><dt>**MCMV \_ siècle**</dt></span><span class="sxs-lookup"><span data-stu-id="08979-122"><dt>**MCMV\_CENTURY**</dt></span></span> </dl> | <span data-ttu-id="08979-123">Vue Century.</span><span class="sxs-lookup"><span data-stu-id="08979-123">Century view.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08979-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="08979-124">Return value</span></span>

<span data-ttu-id="08979-125">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="08979-125">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="08979-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08979-126">Requirements</span></span>



| <span data-ttu-id="08979-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08979-127">Requirement</span></span> | <span data-ttu-id="08979-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="08979-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08979-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08979-129">Minimum supported client</span></span><br/> | <span data-ttu-id="08979-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08979-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="08979-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08979-131">Minimum supported server</span></span><br/> | <span data-ttu-id="08979-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08979-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="08979-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="08979-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="08979-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="08979-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





