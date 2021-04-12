---
title: Message UDM_GETACCEL (commctrl. h)
description: Récupère les informations d’accélération pour un contrôle up-up.
ms.assetid: 794538d6-ca01-4f05-82d1-ce7bc0f76f64
keywords:
- UDM_GETACCEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- UDM_GETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86a9740e59631b737453763a10ccb9820056d95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464654"
---
# <a name="udm_getaccel-message"></a><span data-ttu-id="c9fdc-104">\_Message GETACCEL UDM</span><span class="sxs-lookup"><span data-stu-id="c9fdc-104">UDM\_GETACCEL message</span></span>

<span data-ttu-id="c9fdc-105">Récupère les informations d’accélération pour un contrôle up-up.</span><span class="sxs-lookup"><span data-stu-id="c9fdc-105">Retrieves acceleration information for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c9fdc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9fdc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9fdc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c9fdc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9fdc-108">Nombre d’éléments dans le tableau spécifié par *lParam*.</span><span class="sxs-lookup"><span data-stu-id="c9fdc-108">Number of elements in the array specified by *lParam*.</span></span>

</dd> <dt>

<span data-ttu-id="c9fdc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9fdc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9fdc-110">Pointeur vers un tableau de structures [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) qui reçoivent des informations d’accélération.</span><span class="sxs-lookup"><span data-stu-id="c9fdc-110">Pointer to an array of [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) structures that receive acceleration information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9fdc-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9fdc-111">Return value</span></span>

<span data-ttu-id="c9fdc-112">La valeur de retour est le nombre d’accélérateurs actuellement définis pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="c9fdc-112">The return value is the number of accelerators currently set for the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9fdc-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9fdc-113">Requirements</span></span>



| <span data-ttu-id="c9fdc-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9fdc-114">Requirement</span></span> | <span data-ttu-id="c9fdc-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9fdc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9fdc-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9fdc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c9fdc-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9fdc-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c9fdc-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9fdc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c9fdc-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9fdc-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9fdc-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9fdc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9fdc-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9fdc-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9fdc-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9fdc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9fdc-123">**\_SETACCEL UDM**</span><span class="sxs-lookup"><span data-stu-id="c9fdc-123">**UDM\_SETACCEL**</span></span>](udm-setaccel.md)
</dt> </dl>

 

 





