---
title: Message HDM_GETOVERFLOWRECT (commctrl. h)
description: Obtient le rectangle englobant du bouton de dépassement de capacité lorsque le \_ style de dépassement de capacité HDS est défini sur le contrôle d’en-tête et que le bouton de dépassement de capacité est visible. Envoyez ce message de manière explicite ou à l’aide de la macro GetOverflowRect d’en-tête \_ .
ms.assetid: 52fb3dc3-ce22-40da-8222-20fd75c005ae
keywords:
- HDM_GETOVERFLOWRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_GETOVERFLOWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58f521bb6b188a10bb7af52ead46423e7ae0cf58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508802"
---
# <a name="hdm_getoverflowrect-message"></a><span data-ttu-id="9db66-105">\_Message HDM GETOVERFLOWRECT</span><span class="sxs-lookup"><span data-stu-id="9db66-105">HDM\_GETOVERFLOWRECT message</span></span>

<span data-ttu-id="9db66-106">Obtient le rectangle englobant du bouton de dépassement de capacité lorsque le style de [**\_ dépassement de capacité HDS**](header-control-styles.md) est défini sur le contrôle d’en-tête et que le bouton de dépassement de capacité est visible.</span><span class="sxs-lookup"><span data-stu-id="9db66-106">Gets the bounding rectangle of the overflow button when the [**HDS\_OVERFLOW**](header-control-styles.md) style is set on the header control and the overflow button is visible.</span></span> <span data-ttu-id="9db66-107">Envoyez ce message de manière explicite ou à l’aide de la macro [**\_ GetOverflowRect d’en-tête**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect) .</span><span class="sxs-lookup"><span data-stu-id="9db66-107">Send this message explicitly or by using the [**Header\_GetOverflowRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9db66-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9db66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9db66-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9db66-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9db66-110">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="9db66-110">Not used.</span></span> <span data-ttu-id="9db66-111">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="9db66-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9db66-112">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9db66-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9db66-113">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) pour recevoir les informations de rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="9db66-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the bounding rectangle information.</span></span> <span data-ttu-id="9db66-114">L’expéditeur du message est chargé d’allouer cette structure.</span><span class="sxs-lookup"><span data-stu-id="9db66-114">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="9db66-115">Les coordonnées retournées dans la structure **Rect** sont exprimées en tant que coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="9db66-115">The coordinates returned in the **RECT** structure are expressed as screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9db66-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9db66-116">Return value</span></span>

<span data-ttu-id="9db66-117">Retourne la **valeur true** en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="9db66-117">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9db66-118">Notes</span><span class="sxs-lookup"><span data-stu-id="9db66-118">Remarks</span></span>

<span data-ttu-id="9db66-119">Le contrôle header doit avoir le style **HDF \_ SPLITBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="9db66-119">The header control must have style **HDF\_SPLITBUTTON**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9db66-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9db66-120">Requirements</span></span>



| <span data-ttu-id="9db66-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9db66-121">Requirement</span></span> | <span data-ttu-id="9db66-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="9db66-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9db66-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9db66-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9db66-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9db66-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9db66-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9db66-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9db66-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9db66-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9db66-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="9db66-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9db66-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9db66-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9db66-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9db66-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9db66-130">À propos des contrôles Header</span><span class="sxs-lookup"><span data-stu-id="9db66-130">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

