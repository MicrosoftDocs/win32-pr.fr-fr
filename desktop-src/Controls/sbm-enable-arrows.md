---
title: Message SBM_ENABLE_ARROWS (winuser. h)
description: Une application envoie un \_ message de flèches d’activation SBM \_ pour activer ou désactiver une ou deux flèches d’un contrôle de barre de défilement.
ms.assetid: 9646826a-3a7c-490b-822d-7511e4ef2262
keywords:
- SBM_ENABLE_ARROWS les contrôles de message Windows
topic_type:
- apiref
api_name:
- SBM_ENABLE_ARROWS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78895b43ec7908172a6164917b33ac8549088db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942543"
---
# <a name="sbm_enable_arrows-message"></a><span data-ttu-id="f9ae6-104">\_Message d’activation des \_ flèches SBM</span><span class="sxs-lookup"><span data-stu-id="f9ae6-104">SBM\_ENABLE\_ARROWS message</span></span>

<span data-ttu-id="f9ae6-105">Une application envoie un message de **\_ \_ flèches d’activation SBM** pour activer ou désactiver une ou deux flèches d’un contrôle de barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="f9ae6-105">An application sends the **SBM\_ENABLE\_ARROWS** message to enable or disable one or both arrows of a scroll bar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f9ae6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9ae6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9ae6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f9ae6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9ae6-108">Spécifie si les flèches de barre de défilement sont activées ou désactivées, et indique quelles flèches sont activées ou désactivées.</span><span class="sxs-lookup"><span data-stu-id="f9ae6-108">Specifies whether the scroll bar arrows are enabled or disabled and indicates which arrows are enabled or disabled.</span></span> <span data-ttu-id="f9ae6-109">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f9ae6-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="f9ae6-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9ae6-110">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="f9ae6-111">Signification</span><span class="sxs-lookup"><span data-stu-id="f9ae6-111">Meaning</span></span>                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="ESB_DISABLE_BOTH"></span><span id="esb_disable_both"></span><dl> <span data-ttu-id="f9ae6-112"><dt>**ESB \_ désactiver \_ les deux**</dt></span><span class="sxs-lookup"><span data-stu-id="f9ae6-112"><dt>**ESB\_DISABLE\_BOTH**</dt></span></span> </dl> | <span data-ttu-id="f9ae6-113">Désactive les deux flèches sur une barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="f9ae6-113">Disables both arrows on a scroll bar.</span></span><br/>                                                           |
| <span id="ESB_DISABLE_DOWN"></span><span id="esb_disable_down"></span><dl> <span data-ttu-id="f9ae6-114"><dt>**désactivation de ESB \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f9ae6-114"><dt>**ESB\_DISABLE\_DOWN**</dt></span></span> </dl> | <span data-ttu-id="f9ae6-115">Désactive la flèche vers le bas sur une barre de défilement verticale.</span><span class="sxs-lookup"><span data-stu-id="f9ae6-115">Disables the down arrow on a vertical scroll bar.</span></span><br/>                                               |
| <span id="ESB_DISABLE_LTUP"></span><span id="esb_disable_ltup"></span><dl> <span data-ttu-id="f9ae6-116"><dt>**ESB \_ désactiver \_ LTUP**</dt></span><span class="sxs-lookup"><span data-stu-id="f9ae6-116"><dt>**ESB\_DISABLE\_LTUP**</dt></span></span> </dl> | <span data-ttu-id="f9ae6-117">Désactive la flèche gauche sur une barre de défilement horizontale ou la flèche vers le haut sur une barre de défilement verticale.</span><span class="sxs-lookup"><span data-stu-id="f9ae6-117">Disables the left arrow on a horizontal scroll bar or the up arrow on a vertical scroll bar.</span></span><br/>    |
| <span id="ESB_DISABLE_LEFT"></span><span id="esb_disable_left"></span><dl> <span data-ttu-id="f9ae6-118"><dt>**ESB- \_ désactiver la \_ gauche**</dt></span><span class="sxs-lookup"><span data-stu-id="f9ae6-118"><dt>**ESB\_DISABLE\_LEFT**</dt></span></span> </dl> | <span data-ttu-id="f9ae6-119">Désactive la flèche gauche sur une barre de défilement horizontale.</span><span class="sxs-lookup"><span data-stu-id="f9ae6-119">Disables the left arrow on a horizontal scroll bar.</span></span><br/>                                             |
| <span id="ESB_DISABLE_RTDN"></span><span id="esb_disable_rtdn"></span><dl> <span data-ttu-id="f9ae6-120"><dt>**ESB \_ désactiver \_ RTDN**</dt></span><span class="sxs-lookup"><span data-stu-id="f9ae6-120"><dt>**ESB\_DISABLE\_RTDN**</dt></span></span> </dl> | <span data-ttu-id="f9ae6-121">Désactive la flèche droite sur une barre de défilement horizontale ou la flèche vers le bas sur une barre de défilement verticale.</span><span class="sxs-lookup"><span data-stu-id="f9ae6-121">Disables the right arrow on a horizontal scroll bar or the down arrow on a vertical scroll bar.</span></span><br/> |
| <span id="ESB_DISABLE_UP"></span><span id="esb_disable_up"></span><dl> <span data-ttu-id="f9ae6-122"><dt>**désactivation d’ESB \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f9ae6-122"><dt>**ESB\_DISABLE\_UP**</dt></span></span> </dl>       | <span data-ttu-id="f9ae6-123">Désactive la flèche vers le haut sur une barre de défilement verticale.</span><span class="sxs-lookup"><span data-stu-id="f9ae6-123">Disables the up arrow on a vertical scroll bar.</span></span><br/>                                                 |
| <span id="ESB_ENABLE_BOTH"></span><span id="esb_enable_both"></span><dl> <span data-ttu-id="f9ae6-124"><dt>**ESB \_ activer \_ les deux**</dt></span><span class="sxs-lookup"><span data-stu-id="f9ae6-124"><dt>**ESB\_ENABLE\_BOTH**</dt></span></span> </dl>    | <span data-ttu-id="f9ae6-125">Active les deux flèches sur une barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="f9ae6-125">Enables both arrows on a scroll bar.</span></span><br/>                                                            |



 

</dd> <dt>

<span data-ttu-id="f9ae6-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9ae6-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9ae6-127">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="f9ae6-127">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9ae6-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f9ae6-128">Return value</span></span>

<span data-ttu-id="f9ae6-129">Si le message est correctement exécuté, la valeur de retour est **true**; Sinon, la **valeur est false**.</span><span class="sxs-lookup"><span data-stu-id="f9ae6-129">If the message succeeds, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9ae6-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9ae6-130">Requirements</span></span>



| <span data-ttu-id="f9ae6-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9ae6-131">Requirement</span></span> | <span data-ttu-id="f9ae6-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9ae6-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9ae6-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9ae6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f9ae6-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9ae6-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f9ae6-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9ae6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f9ae6-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9ae6-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f9ae6-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9ae6-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9ae6-138"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9ae6-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





