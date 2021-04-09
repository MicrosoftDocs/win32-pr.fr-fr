---
title: Message HDM_SETHOTDIVIDER (commctrl. h)
description: Modifie la couleur d’un séparateur entre des éléments d’en-tête pour indiquer la destination d’une opération de glisser-déplacer externe. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ SetHotDivider.
ms.assetid: 56f6e5c6-1df3-4b4d-9ad8-97fb168c5462
keywords:
- HDM_SETHOTDIVIDER les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_SETHOTDIVIDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb894100878e9b3ee85e8e8367a4b81a022a0a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103552"
---
# <a name="hdm_sethotdivider-message"></a><span data-ttu-id="13ea8-105">\_Message HDM SETHOTDIVIDER</span><span class="sxs-lookup"><span data-stu-id="13ea8-105">HDM\_SETHOTDIVIDER message</span></span>

<span data-ttu-id="13ea8-106">Modifie la couleur d’un séparateur entre des éléments d’en-tête pour indiquer la destination d’une opération de glisser-déplacer externe.</span><span class="sxs-lookup"><span data-stu-id="13ea8-106">Changes the color of a divider between header items to indicate the destination of an external drag-and-drop operation.</span></span> <span data-ttu-id="13ea8-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ SetHotDivider**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider) .</span><span class="sxs-lookup"><span data-stu-id="13ea8-107">You can send this message explicitly or use the [**Header\_SetHotDivider**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="13ea8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13ea8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13ea8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="13ea8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13ea8-110">Type de valeur représenté par *lParam*.</span><span class="sxs-lookup"><span data-stu-id="13ea8-110">The type of value represented by *lParam*.</span></span> <span data-ttu-id="13ea8-111">Cette valeur peut être l'une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="13ea8-111">This value can be one of the following:</span></span>



| <span data-ttu-id="13ea8-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="13ea8-112">Value</span></span>                                                                                                                                    | <span data-ttu-id="13ea8-113">Signification</span><span class="sxs-lookup"><span data-stu-id="13ea8-113">Meaning</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="13ea8-114"><dt>VRAI \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="13ea8-114"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="13ea8-115">Indique que *lParam* contient les coordonnées clientes du pointeur.</span><span class="sxs-lookup"><span data-stu-id="13ea8-115">Indicates that *lParam* holds the client coordinates of the pointer.</span></span><br/> |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="13ea8-116"><dt>FALSe \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="13ea8-116"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="13ea8-117">Indique que *lParam* contient une valeur d’index de séparateur.</span><span class="sxs-lookup"><span data-stu-id="13ea8-117">Indicates that *lParam* holds a divider index value.</span></span><br/>                 |



 

</dd> <dt>

<span data-ttu-id="13ea8-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="13ea8-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13ea8-119">Une valeur contenue dans *lParam* est interprétée en fonction de la valeur de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="13ea8-119">A value held in *lParam* is interpreted depending on the value of *wParam*.</span></span>

<span data-ttu-id="13ea8-120">Si *wParam* a la **valeur true**, *lParam* représente les coordonnées x et y du pointeur.</span><span class="sxs-lookup"><span data-stu-id="13ea8-120">If *wParam* is **TRUE**, *lParam* represents the x- and y-coordinates of the pointer.</span></span> <span data-ttu-id="13ea8-121">La coordonnée x se trouve dans le mot de poids faible et la coordonnée y est dans le mot haut.</span><span class="sxs-lookup"><span data-stu-id="13ea8-121">The x-coordinate is in the low word, and the y-coordinate is in the high word.</span></span> <span data-ttu-id="13ea8-122">Lorsque le contrôle header reçoit le message, il met en surbrillance le séparateur approprié en fonction des coordonnées *lParam* .</span><span class="sxs-lookup"><span data-stu-id="13ea8-122">When the header control receives the message, it highlights the appropriate divider based on the *lParam* coordinates.</span></span>

<span data-ttu-id="13ea8-123">Si *wParam* a la **valeur false**, *lParam* représente l’index entier du séparateur à mettre en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="13ea8-123">If *wParam* is **FALSE**, *lParam* represents the integer index of the divider to be highlighted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13ea8-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="13ea8-124">Return value</span></span>

<span data-ttu-id="13ea8-125">Retourne une valeur égale à l’index du séparateur mis en surbrillance par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="13ea8-125">Returns a value equal to the index of the divider that the control highlighted.</span></span>

## <a name="remarks"></a><span data-ttu-id="13ea8-126">Notes</span><span class="sxs-lookup"><span data-stu-id="13ea8-126">Remarks</span></span>

<span data-ttu-id="13ea8-127">Ce message crée un effet qu’un contrôle header génère automatiquement lorsqu’il a le style [**HDS \_ DRAGDROP**](header-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="13ea8-127">This message creates an effect that a header control automatically produces when it has the [**HDS\_DRAGDROP**](header-control-styles.md) style.</span></span> <span data-ttu-id="13ea8-128">Le message **HDM \_ SETHOTDIVIDER** est destiné à être utilisé lorsque le propriétaire du contrôle gère manuellement les opérations de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="13ea8-128">The **HDM\_SETHOTDIVIDER** message is intended to be used when the owner of the control handles drag-and-drop operations manually.</span></span>

## <a name="requirements"></a><span data-ttu-id="13ea8-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13ea8-129">Requirements</span></span>



| <span data-ttu-id="13ea8-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13ea8-130">Requirement</span></span> | <span data-ttu-id="13ea8-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="13ea8-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="13ea8-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13ea8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="13ea8-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="13ea8-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="13ea8-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13ea8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="13ea8-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="13ea8-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="13ea8-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="13ea8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="13ea8-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="13ea8-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





