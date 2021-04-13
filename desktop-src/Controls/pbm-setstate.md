---
title: Message PBM_SETSTATE (commctrl. h)
description: Définit l’état de la barre de progression.
ms.assetid: 4626f334-db74-4618-8fc7-e6f21c88ca19
keywords:
- PBM_SETSTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PBM_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c91e94bcc909957264eff776e56d3580b2c36ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466102"
---
# <a name="pbm_setstate-message"></a><span data-ttu-id="128de-104">\_Message PBM SETSTATE</span><span class="sxs-lookup"><span data-stu-id="128de-104">PBM\_SETSTATE message</span></span>

<span data-ttu-id="128de-105">Définit l’état de la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="128de-105">Sets the state of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="128de-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="128de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="128de-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="128de-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="128de-108">État de la barre de progression qui est définie.</span><span class="sxs-lookup"><span data-stu-id="128de-108">State of the progress bar that is being set.</span></span> <span data-ttu-id="128de-109">Une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="128de-109">One of the following values.</span></span>



| <span data-ttu-id="128de-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="128de-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="128de-111">Signification</span><span class="sxs-lookup"><span data-stu-id="128de-111">Meaning</span></span>                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <span data-ttu-id="128de-112"><dt>**PBST \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="128de-112"><dt>**PBST\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="128de-113">En cours.</span><span class="sxs-lookup"><span data-stu-id="128de-113">In progress.</span></span><br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <span data-ttu-id="128de-114"><dt>**\_erreur PBST**</dt></span><span class="sxs-lookup"><span data-stu-id="128de-114"><dt>**PBST\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="128de-115">Erreur.</span><span class="sxs-lookup"><span data-stu-id="128de-115">Error.</span></span><br/>       |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <span data-ttu-id="128de-116"><dt>**PBST \_ suspendu**</dt></span><span class="sxs-lookup"><span data-stu-id="128de-116"><dt>**PBST\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="128de-117">Suspendu.</span><span class="sxs-lookup"><span data-stu-id="128de-117">Paused.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="128de-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="128de-118">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="128de-119">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="128de-119">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="128de-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="128de-120">Return value</span></span>

<span data-ttu-id="128de-121">Retourne l’état précédent.</span><span class="sxs-lookup"><span data-stu-id="128de-121">Returns the previous state.</span></span>

## <a name="requirements"></a><span data-ttu-id="128de-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="128de-122">Requirements</span></span>



| <span data-ttu-id="128de-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="128de-123">Requirement</span></span> | <span data-ttu-id="128de-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="128de-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="128de-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="128de-125">Minimum supported client</span></span><br/> | <span data-ttu-id="128de-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="128de-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="128de-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="128de-127">Minimum supported server</span></span><br/> | <span data-ttu-id="128de-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="128de-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="128de-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="128de-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="128de-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="128de-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





