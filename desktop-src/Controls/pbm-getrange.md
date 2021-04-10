---
title: Message PBM_GETRANGE (commctrl. h)
description: Récupère des informations sur les limites haute et basse actuelles d’un contrôle de barre de progression donné.
ms.assetid: 676b7a37-bdde-4307-9888-9a0cf40db2db
keywords:
- PBM_GETRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PBM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0c4ffe9365686432a5e78cb1540055f41a838fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942474"
---
# <a name="pbm_getrange-message"></a><span data-ttu-id="84eb9-104">\_Message PBM GETRANGE</span><span class="sxs-lookup"><span data-stu-id="84eb9-104">PBM\_GETRANGE message</span></span>

<span data-ttu-id="84eb9-105">Récupère des informations sur les limites haute et basse actuelles d’un contrôle de barre de progression donné.</span><span class="sxs-lookup"><span data-stu-id="84eb9-105">Retrieves information about the current high and low limits of a given progress bar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="84eb9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84eb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84eb9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="84eb9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84eb9-108">Valeur de l’indicateur spécifiant la valeur limite à utiliser comme valeur de retour du message.</span><span class="sxs-lookup"><span data-stu-id="84eb9-108">Flag value specifying which limit value is to be used as the message's return value.</span></span> <span data-ttu-id="84eb9-109">Ce paramètre peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="84eb9-109">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="84eb9-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="84eb9-110">Value</span></span>                                                                                                                                    | <span data-ttu-id="84eb9-111">Signification</span><span class="sxs-lookup"><span data-stu-id="84eb9-111">Meaning</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="84eb9-112"><dt>VRAI \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="84eb9-112"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="84eb9-113">Retourne la limite inférieure.</span><span class="sxs-lookup"><span data-stu-id="84eb9-113">Return the low limit.</span></span><br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="84eb9-114"><dt>FALSe \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="84eb9-114"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="84eb9-115">Retourne la limite supérieure.</span><span class="sxs-lookup"><span data-stu-id="84eb9-115">Return the high limit.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="84eb9-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="84eb9-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84eb9-117">Pointeur vers une structure [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) qui doit être remplie avec les limites haute et basse du contrôle de barre de progression.</span><span class="sxs-lookup"><span data-stu-id="84eb9-117">Pointer to a [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) structure that is to be filled with the high and low limits of the progress bar control.</span></span> <span data-ttu-id="84eb9-118">Si ce paramètre a la valeur **null**, le contrôle ne retourne que la limite spécifiée par *wParam*.</span><span class="sxs-lookup"><span data-stu-id="84eb9-118">If this parameter is set to **NULL**, the control will return only the limit specified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84eb9-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="84eb9-119">Return value</span></span>

<span data-ttu-id="84eb9-120">Retourne un entier qui représente la valeur limite spécifiée par *wParam*.</span><span class="sxs-lookup"><span data-stu-id="84eb9-120">Returns an INT that represents the limit value specified by *wParam*.</span></span> <span data-ttu-id="84eb9-121">Si *lParam* n’est pas **null**, *lParam* doit pointer vers une structure [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) qui doit être remplie avec les deux valeurs limites.</span><span class="sxs-lookup"><span data-stu-id="84eb9-121">If *lParam* is not **NULL**, *lParam* must point to a [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) structure that is to be filled with both limit values.</span></span>

## <a name="requirements"></a><span data-ttu-id="84eb9-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84eb9-122">Requirements</span></span>



| <span data-ttu-id="84eb9-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84eb9-123">Requirement</span></span> | <span data-ttu-id="84eb9-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="84eb9-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84eb9-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84eb9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="84eb9-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84eb9-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="84eb9-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84eb9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="84eb9-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84eb9-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="84eb9-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="84eb9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="84eb9-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="84eb9-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





