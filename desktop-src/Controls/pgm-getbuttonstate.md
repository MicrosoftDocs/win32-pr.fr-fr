---
title: Message PGM_GETBUTTONSTATE (commctrl. h)
description: Récupère l’état du bouton spécifié dans un contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ GetButtonState.
ms.assetid: 58f99b67-fef7-4695-86e2-0579a2f6de2f
keywords:
- PGM_GETBUTTONSTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d8c9eebbc0aa91651a01de1fe193544f0c8afcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942467"
---
# <a name="pgm_getbuttonstate-message"></a><span data-ttu-id="90dfd-105">\_Message GETBUTTONSTATE PGM</span><span class="sxs-lookup"><span data-stu-id="90dfd-105">PGM\_GETBUTTONSTATE message</span></span>

<span data-ttu-id="90dfd-106">Récupère l’état du bouton spécifié dans un contrôle de pagineur.</span><span class="sxs-lookup"><span data-stu-id="90dfd-106">Retrieves the state of the specified button in a pager control.</span></span> <span data-ttu-id="90dfd-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) .</span><span class="sxs-lookup"><span data-stu-id="90dfd-107">You can send this message explicitly or use the [**Pager\_GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="90dfd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90dfd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90dfd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="90dfd-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="90dfd-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="90dfd-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="90dfd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90dfd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90dfd-112">Indique le bouton pour lequel l’État doit être récupéré.</span><span class="sxs-lookup"><span data-stu-id="90dfd-112">Indicates which button to retrieve the state for.</span></span> <span data-ttu-id="90dfd-113">Il peut s’agir de l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="90dfd-113">This can be one of the following values:</span></span>



| <span data-ttu-id="90dfd-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="90dfd-114">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="90dfd-115">Signification</span><span class="sxs-lookup"><span data-stu-id="90dfd-115">Meaning</span></span>                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PGB_TOPORLEFT"></span><span id="pgb_toporleft"></span><dl> <span data-ttu-id="90dfd-116"><dt>**PGB \_ TOPORLEFT**</dt></span><span class="sxs-lookup"><span data-stu-id="90dfd-116"><dt>**PGB\_TOPORLEFT**</dt></span></span> </dl>             | <span data-ttu-id="90dfd-117">Indique le bouton supérieur dans un contrôle de pagineur [**PG \_ vert**](pager-control-styles.md) ou le bouton gauche dans un contrôle de pagineur [**\_ Hori PG**](pager-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="90dfd-117">Indicates the top button in a [**PGS\_VERT**](pager-control-styles.md) pager control or the left button in a [**PGS\_HORZ**](pager-control-styles.md) pager control.</span></span> <br/>     |
| <span id="PGB_BOTTOMORRIGHT"></span><span id="pgb_bottomorright"></span><dl> <span data-ttu-id="90dfd-118"><dt>**PGB \_ BOTTOMORRIGHT**</dt></span><span class="sxs-lookup"><span data-stu-id="90dfd-118"><dt>**PGB\_BOTTOMORRIGHT**</dt></span></span> </dl> | <span data-ttu-id="90dfd-119">Indique le bouton inférieur dans un contrôle de pagineur [**PG \_ vert**](pager-control-styles.md) ou le bouton droit dans un contrôle de pagineur [**\_ Hori PG**](pager-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="90dfd-119">Indicates the bottom button in a [**PGS\_VERT**](pager-control-styles.md) pager control or the right button in a [**PGS\_HORZ**](pager-control-styles.md) pager control.</span></span> <br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90dfd-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="90dfd-120">Return value</span></span>

<span data-ttu-id="90dfd-121">Retourne l’état du bouton spécifié dans *lParam*.</span><span class="sxs-lookup"><span data-stu-id="90dfd-121">Returns the state of the button specified in *lParam*.</span></span> <span data-ttu-id="90dfd-122">Il s’agit d’une ou plusieurs des valeurs suivantes (si plus une valeur est retournée, elles sont combinées à l’aide d’une opération or au niveau du bit) :</span><span class="sxs-lookup"><span data-stu-id="90dfd-122">This will be one or more of the following values (if more then one value is returned they will be combined using a bitwise OR):</span></span>



| <span data-ttu-id="90dfd-123">Code de retour</span><span class="sxs-lookup"><span data-stu-id="90dfd-123">Return code</span></span>                                                                                   | <span data-ttu-id="90dfd-124">Description</span><span class="sxs-lookup"><span data-stu-id="90dfd-124">Description</span></span>                                 |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="90dfd-125"><dt>**PGF \_ invisible**</dt></span><span class="sxs-lookup"><span data-stu-id="90dfd-125"><dt>**PGF\_INVISIBLE**</dt></span></span> </dl> | <span data-ttu-id="90dfd-126">Le bouton n’est pas visible.</span><span class="sxs-lookup"><span data-stu-id="90dfd-126">The button is not visible.</span></span> <br/>      |
| <dl> <span data-ttu-id="90dfd-127"><dt>**PGF \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="90dfd-127"><dt>**PGF\_NORMAL**</dt></span></span> </dl>    | <span data-ttu-id="90dfd-128">Le bouton est dans un état normal.</span><span class="sxs-lookup"><span data-stu-id="90dfd-128">The button is in normal state.</span></span> <br/>  |
| <dl> <span data-ttu-id="90dfd-129"><dt>**PGF \_ grisé**</dt></span><span class="sxs-lookup"><span data-stu-id="90dfd-129"><dt>**PGF\_GRAYED**</dt></span></span> </dl>    | <span data-ttu-id="90dfd-130">Le bouton est grisé.</span><span class="sxs-lookup"><span data-stu-id="90dfd-130">The button is in grayed state.</span></span> <br/>  |
| <dl> <span data-ttu-id="90dfd-131"><dt>**PGF \_ enfoncé**</dt></span><span class="sxs-lookup"><span data-stu-id="90dfd-131"><dt>**PGF\_DEPRESSED**</dt></span></span> </dl> | <span data-ttu-id="90dfd-132">Le bouton est à l’état enfoncé.</span><span class="sxs-lookup"><span data-stu-id="90dfd-132">The button is in pressed state.</span></span> <br/> |
| <dl> <span data-ttu-id="90dfd-133"><dt>**PGF \_ chaud**</dt></span><span class="sxs-lookup"><span data-stu-id="90dfd-133"><dt>**PGF\_HOT**</dt></span></span> </dl>       | <span data-ttu-id="90dfd-134">Le bouton est à l’état actif.</span><span class="sxs-lookup"><span data-stu-id="90dfd-134">The button is in hot state.</span></span> <br/>     |



 

## <a name="requirements"></a><span data-ttu-id="90dfd-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90dfd-135">Requirements</span></span>



| <span data-ttu-id="90dfd-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="90dfd-136">Requirement</span></span> | <span data-ttu-id="90dfd-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="90dfd-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90dfd-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90dfd-138">Minimum supported client</span></span><br/> | <span data-ttu-id="90dfd-139">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="90dfd-139">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="90dfd-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90dfd-140">Minimum supported server</span></span><br/> | <span data-ttu-id="90dfd-141">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="90dfd-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="90dfd-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="90dfd-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="90dfd-143"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="90dfd-143"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





