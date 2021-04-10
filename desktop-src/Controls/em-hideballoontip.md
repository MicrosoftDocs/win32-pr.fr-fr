---
title: Message EM_HIDEBALLOONTIP (commctrl. h)
description: Masque toute info-bulle associée à un contrôle d’édition.
ms.assetid: 820b98d6-c2bd-4821-ba44-9d58e23eac81
keywords:
- EM_HIDEBALLOONTIP les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_HIDEBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8ecececff3d12ad48cfcfb6353a717e8f8875df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941741"
---
# <a name="em_hideballoontip-message"></a><span data-ttu-id="2b849-104">\_Message HIDEBALLOONTIP em</span><span class="sxs-lookup"><span data-stu-id="2b849-104">EM\_HIDEBALLOONTIP message</span></span>

<span data-ttu-id="2b849-105">Masque toute info-bulle associée à un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="2b849-105">Hides any balloon tip associated with an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2b849-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b849-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b849-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b849-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b849-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="2b849-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2b849-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b849-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b849-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="2b849-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b849-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2b849-111">Return value</span></span>

<span data-ttu-id="2b849-112">Si le message est correctement exécuté, la méthode retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="2b849-112">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="2b849-113">Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="2b849-113">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b849-114">Notes</span><span class="sxs-lookup"><span data-stu-id="2b849-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2b849-115">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="2b849-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="2b849-116">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2b849-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2b849-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b849-117">Requirements</span></span>



| <span data-ttu-id="2b849-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b849-118">Requirement</span></span> | <span data-ttu-id="2b849-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b849-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b849-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b849-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2b849-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b849-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2b849-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b849-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2b849-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b849-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2b849-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="2b849-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b849-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b849-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b849-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b849-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b849-127">**Modifier \_ HideBalloonTip**</span><span class="sxs-lookup"><span data-stu-id="2b849-127">**Edit\_HideBalloonTip**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_hideballoontip)
</dt> </dl>

 

 





