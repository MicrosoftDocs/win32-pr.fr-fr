---
title: Message UDM_GETPOS32 (commctrl. h)
description: Retourne la position 32 bits d’un contrôle up-up.
ms.assetid: 90feffbd-a472-446f-8a67-5da408cde002
keywords:
- UDM_GETPOS32 les contrôles de message Windows
topic_type:
- apiref
api_name:
- UDM_GETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15f316b6833c67cd01d4e01910399a8730691f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464647"
---
# <a name="udm_getpos32-message"></a><span data-ttu-id="b8d28-104">\_Message GETPOS32 UDM</span><span class="sxs-lookup"><span data-stu-id="b8d28-104">UDM\_GETPOS32 message</span></span>

<span data-ttu-id="b8d28-105">Retourne la position 32 bits d’un contrôle up-up.</span><span class="sxs-lookup"><span data-stu-id="b8d28-105">Returns the 32-bit position of an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8d28-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8d28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8d28-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8d28-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8d28-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b8d28-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b8d28-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8d28-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8d28-110">Pointeur vers une valeur **bool** qui a la valeur zéro si la valeur est récupérée avec succès ou différente de zéro si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="b8d28-110">Pointer to a **BOOL** value that is set to zero if the value is successfully retrieved or nonzero if an error occurs.</span></span> <span data-ttu-id="b8d28-111">Si ce paramètre a la valeur **null**, les erreurs ne sont pas signalées.</span><span class="sxs-lookup"><span data-stu-id="b8d28-111">If this parameter is set to **NULL**, errors are not reported.</span></span>

<span data-ttu-id="b8d28-112">Si **UDM \_ GETPOS32** est utilisé dans une situation inter-processus, ce paramètre doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b8d28-112">If **UDM\_GETPOS32** is used in a cross-process situation, this parameter must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8d28-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b8d28-113">Return value</span></span>

<span data-ttu-id="b8d28-114">Retourne la position d’un contrôle up-up avec une précision de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b8d28-114">Returns the position of an up-down control with 32-bit precision.</span></span> <span data-ttu-id="b8d28-115">Les applications doivent vérifier la valeur *lParam* pour déterminer si la valeur de retour est valide.</span><span class="sxs-lookup"><span data-stu-id="b8d28-115">Applications must check the *lParam* value to determine whether the return value is valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8d28-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b8d28-116">Remarks</span></span>

<span data-ttu-id="b8d28-117">Lors du traitement de ce message, le contrôle up-out met à jour sa position actuelle en fonction de la légende de la fenêtre associée.</span><span class="sxs-lookup"><span data-stu-id="b8d28-117">When it processes this message, the up-down control updates its current position based on the caption of the buddy window.</span></span> <span data-ttu-id="b8d28-118">Elle retourne une erreur s’il n’existe aucune fenêtre associée ou si la légende spécifie une valeur non valide ou hors limites.</span><span class="sxs-lookup"><span data-stu-id="b8d28-118">It returns an error if there is no buddy window or if the caption specifies an invalid or out-of-range value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8d28-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8d28-119">Requirements</span></span>



| <span data-ttu-id="b8d28-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8d28-120">Requirement</span></span> | <span data-ttu-id="b8d28-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8d28-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8d28-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8d28-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b8d28-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8d28-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8d28-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8d28-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b8d28-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8d28-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8d28-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8d28-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8d28-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8d28-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8d28-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8d28-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="b8d28-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="b8d28-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b8d28-130">**\_GETPOS UDM**</span><span class="sxs-lookup"><span data-stu-id="b8d28-130">**UDM\_GETPOS**</span></span>](udm-getpos.md)
</dt> <dt>

[<span data-ttu-id="b8d28-131">**\_SetPos UDM**</span><span class="sxs-lookup"><span data-stu-id="b8d28-131">**UDM\_SETPOS**</span></span>](udm-setpos.md)
</dt> <dt>

[<span data-ttu-id="b8d28-132">**\_SETPOS32 UDM**</span><span class="sxs-lookup"><span data-stu-id="b8d28-132">**UDM\_SETPOS32**</span></span>](udm-setpos32.md)
</dt> </dl>

 

 





