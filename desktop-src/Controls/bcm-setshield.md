---
title: Message BCM_SETSHIELD (commctrl. h)
description: Définit l’état d’élévation requis pour un bouton ou un lien de commande spécifié pour afficher une icône avec élévation de privilèges. Envoyez ce message explicitement ou à l’aide de la \_ macro Button SetElevationRequiredState.
ms.assetid: 2ce2a006-7136-415b-824b-46b282b100f4
keywords:
- BCM_SETSHIELD les contrôles de message Windows
topic_type:
- apiref
api_name:
- BCM_SETSHIELD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2149e2945f2876309459c287961b7b0a4a1f9acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103489"
---
# <a name="bcm_setshield-message"></a><span data-ttu-id="8444e-105">\_Message SETSHIELD BCM</span><span class="sxs-lookup"><span data-stu-id="8444e-105">BCM\_SETSHIELD message</span></span>

<span data-ttu-id="8444e-106">Définit l’état d’élévation requis pour un bouton ou un lien de commande spécifié pour afficher une icône avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="8444e-106">Sets the elevation required state for a specified button or command link to display an elevated icon.</span></span> <span data-ttu-id="8444e-107">Envoyez ce message explicitement ou à l’aide de la macro [**Button \_ SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) .</span><span class="sxs-lookup"><span data-stu-id="8444e-107">Send this message explicitly or by using the [**Button\_SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8444e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8444e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8444e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8444e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8444e-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8444e-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8444e-111">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8444e-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8444e-112">Valeur **booléenne** qui est **true** pour dessiner une icône avec élévation de privilèges, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8444e-112">A **BOOL** that is **TRUE** to draw an elevated icon, or **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8444e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8444e-113">Return value</span></span>

<span data-ttu-id="8444e-114">Retourne 1 en cas de réussite, ou un code d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8444e-114">Returns 1 if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8444e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8444e-115">Remarks</span></span>

<span data-ttu-id="8444e-116">Une application doit être manifestée pour utiliser comctl32.dll version 6 pour obtenir cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="8444e-116">An application must be manifested to use comctl32.dll version 6 to gain this functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="8444e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8444e-117">Requirements</span></span>



| <span data-ttu-id="8444e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8444e-118">Requirement</span></span> | <span data-ttu-id="8444e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8444e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8444e-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8444e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8444e-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8444e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8444e-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8444e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8444e-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8444e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8444e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8444e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8444e-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8444e-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





