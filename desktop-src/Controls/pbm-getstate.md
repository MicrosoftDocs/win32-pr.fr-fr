---
title: Message PBM_GETSTATE (commctrl. h)
description: Obtient l’état de la barre de progression.
ms.assetid: ff240160-7db6-4711-8d4e-25a77dfba118
keywords:
- PBM_GETSTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PBM_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07d4f7029fca46a046545efd1cea8e0eab99c757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942473"
---
# <a name="pbm_getstate-message"></a><span data-ttu-id="abcee-104">\_Message PBM GETSTATE</span><span class="sxs-lookup"><span data-stu-id="abcee-104">PBM\_GETSTATE message</span></span>

<span data-ttu-id="abcee-105">Obtient l’état de la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="abcee-105">Gets the state of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="abcee-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="abcee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abcee-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="abcee-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="abcee-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="abcee-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="abcee-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="abcee-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="abcee-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="abcee-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abcee-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="abcee-111">Return value</span></span>

<span data-ttu-id="abcee-112">Retourne l’état actuel de la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="abcee-112">Returns the current state of the progress bar.</span></span> <span data-ttu-id="abcee-113">Une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="abcee-113">One of the following values.</span></span>



| <span data-ttu-id="abcee-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="abcee-114">Return code</span></span>                                                                                 | <span data-ttu-id="abcee-115">Description</span><span class="sxs-lookup"><span data-stu-id="abcee-115">Description</span></span>             |
|---------------------------------------------------------------------------------------------|-------------------------|
| <dl> <span data-ttu-id="abcee-116"><dt>**PBST \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="abcee-116"><dt>**PBST\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="abcee-117">En cours.</span><span class="sxs-lookup"><span data-stu-id="abcee-117">In progress.</span></span><br/> |
| <dl> <span data-ttu-id="abcee-118"><dt>**\_erreur PBST**</dt></span><span class="sxs-lookup"><span data-stu-id="abcee-118"><dt>**PBST\_ERROR**</dt></span></span> </dl>  | <span data-ttu-id="abcee-119">Erreur.</span><span class="sxs-lookup"><span data-stu-id="abcee-119">Error.</span></span><br/>       |
| <dl> <span data-ttu-id="abcee-120"><dt>**PBST \_ suspendu**</dt></span><span class="sxs-lookup"><span data-stu-id="abcee-120"><dt>**PBST\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="abcee-121">Suspendu.</span><span class="sxs-lookup"><span data-stu-id="abcee-121">Paused.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="abcee-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="abcee-122">Requirements</span></span>



| <span data-ttu-id="abcee-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="abcee-123">Requirement</span></span> | <span data-ttu-id="abcee-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="abcee-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="abcee-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abcee-125">Minimum supported client</span></span><br/> | <span data-ttu-id="abcee-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="abcee-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="abcee-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abcee-127">Minimum supported server</span></span><br/> | <span data-ttu-id="abcee-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="abcee-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="abcee-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="abcee-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="abcee-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="abcee-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





