---
title: Message IPM_SETRANGE (commctrl. h)
description: Définit la plage valide pour le champ spécifié dans le contrôle d’adresse IP.
ms.assetid: 03068c5d-822f-459d-8f79-e7f0430a27bf
keywords:
- IPM_SETRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- IPM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e70df7b2b8f76f514d9a0cc6101aba2ee7cf4ec6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033108"
---
# <a name="ipm_setrange-message"></a><span data-ttu-id="dd43a-104">\_Message IPM SEtrange</span><span class="sxs-lookup"><span data-stu-id="dd43a-104">IPM\_SETRANGE message</span></span>

<span data-ttu-id="dd43a-105">Définit la plage valide pour le champ spécifié dans le contrôle d’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="dd43a-105">Sets the valid range for the specified field in the IP address control.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd43a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd43a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd43a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dd43a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd43a-108">Index de champ de base zéro auquel la plage sera appliquée.</span><span class="sxs-lookup"><span data-stu-id="dd43a-108">A zero-based field index to which the range will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="dd43a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd43a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd43a-110">Valeur de **mot** qui contient la limite inférieure de la plage dans l’octet de poids faible et la limite supérieure dans l’octet de poids fort.</span><span class="sxs-lookup"><span data-stu-id="dd43a-110">A **WORD** value that contains the lower limit of the range in the low-order byte and the upper limit in the high-order byte.</span></span> <span data-ttu-id="dd43a-111">Ces deux valeurs sont inclusives.</span><span class="sxs-lookup"><span data-stu-id="dd43a-111">Both of these values are inclusive.</span></span> <span data-ttu-id="dd43a-112">La macro [**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange) peut également être utilisée pour créer la plage.</span><span class="sxs-lookup"><span data-stu-id="dd43a-112">The [**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange) macro can also be used to create the range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd43a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dd43a-113">Return value</span></span>

<span data-ttu-id="dd43a-114">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="dd43a-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd43a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="dd43a-115">Remarks</span></span>

<span data-ttu-id="dd43a-116">Si l’utilisateur entre une valeur dans le champ qui est en dehors de cette plage, le contrôle envoie la notification [IPN \_ FIELDCHANGED](ipn-fieldchanged.md) avec la valeur entrée.</span><span class="sxs-lookup"><span data-stu-id="dd43a-116">If the user enters a value in the field that is outside of this range, the control will send the [IPN\_FIELDCHANGED](ipn-fieldchanged.md) notification with the entered value.</span></span> <span data-ttu-id="dd43a-117">Si la valeur est toujours en dehors de la plage après l’envoi de la notification, le contrôle tente de modifier la valeur entrée à la limite de plage la plus proche.</span><span class="sxs-lookup"><span data-stu-id="dd43a-117">If the value is still outside of the range after sending the notification, the control will attempt to change the entered value to the closest range limit.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd43a-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd43a-118">Requirements</span></span>



| <span data-ttu-id="dd43a-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd43a-119">Requirement</span></span> | <span data-ttu-id="dd43a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd43a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd43a-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd43a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dd43a-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd43a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dd43a-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd43a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dd43a-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd43a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd43a-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd43a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd43a-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd43a-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





