---
title: Message TDM_SET_PROGRESS_BAR_STATE (commctrl. h)
description: Définit l’état de la barre de progression dans une boîte de dialogue de tâche.
ms.assetid: 8b0f2ee9-e6ca-4a5b-8687-6e2682eda7d0
keywords:
- TDM_SET_PROGRESS_BAR_STATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f0ae4ec104c8472d3640aa804650640d77cc63
ms.sourcegitcommit: e584514ced7396dde55e58501c8c8a872229acc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2021
ms.locfileid: "104321790"
---
# <a name="tdm_set_progress_bar_state-message"></a><span data-ttu-id="3064d-104">Message d’état de la barre de progression de l' \_ ensemble TDM \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="3064d-104">TDM\_SET\_PROGRESS\_BAR\_STATE message</span></span>

<span data-ttu-id="3064d-105">Définit l’état de la barre de progression dans une boîte de dialogue de tâche.</span><span class="sxs-lookup"><span data-stu-id="3064d-105">Sets the state of the progress bar in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="3064d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3064d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3064d-107">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3064d-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3064d-108">**Entier** qui spécifie l’état de la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="3064d-108">An **int** that specifies the state of the progress bar.</span></span> <span data-ttu-id="3064d-109">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="3064d-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="3064d-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="3064d-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="3064d-111">Signification</span><span class="sxs-lookup"><span data-stu-id="3064d-111">Meaning</span></span>                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <span data-ttu-id="3064d-112"><dt>**PBST \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="3064d-112"><dt>**PBST\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="3064d-113">Définit la barre de progression à l’état normal.</span><span class="sxs-lookup"><span data-stu-id="3064d-113">Sets the progress bar to the normal state.</span></span><br/> |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <span data-ttu-id="3064d-114"><dt>**PBST \_ suspendu**</dt></span><span class="sxs-lookup"><span data-stu-id="3064d-114"><dt>**PBST\_PAUSED**</dt></span></span> </dl>    | <span data-ttu-id="3064d-115">Définit la barre de progression à l’état suspendu.</span><span class="sxs-lookup"><span data-stu-id="3064d-115">Sets the progress bar to the paused state.</span></span><br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <span data-ttu-id="3064d-116"><dt>**\_erreur PBST**</dt></span><span class="sxs-lookup"><span data-stu-id="3064d-116"><dt>**PBST\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="3064d-117">Définissez la barre de progression sur l’état d’erreur.</span><span class="sxs-lookup"><span data-stu-id="3064d-117">Set the progress bar to the error state.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="3064d-118">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3064d-118">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3064d-119">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="3064d-119">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3064d-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3064d-120">Return value</span></span>

<span data-ttu-id="3064d-121">Si la fonction est réussie, la valeur de retour est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="3064d-121">If the function succeeds, the return value is non zero.</span></span>

<span data-ttu-id="3064d-122">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="3064d-122">If the function fails, the return value is zero.</span></span> <span data-ttu-id="3064d-123">Pour recevoir l’appel d’informations d’erreur étendues GetLastError.</span><span class="sxs-lookup"><span data-stu-id="3064d-123">To get extended error information call GetLastError.</span></span>

## <a name="requirements"></a><span data-ttu-id="3064d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3064d-124">Requirements</span></span>



| <span data-ttu-id="3064d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3064d-125">Requirement</span></span> | <span data-ttu-id="3064d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3064d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3064d-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3064d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3064d-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3064d-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3064d-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3064d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3064d-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3064d-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3064d-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="3064d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3064d-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3064d-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





