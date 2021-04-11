---
title: Message PSM_ENABLEWIZBUTTONS (Prsht. h)
description: Active ou désactive tous les boutons standard dans un Assistant Aero. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro PropSheet EnableWizButtons.
ms.assetid: 9e8ff2dc-c0e7-4754-8be2-2c7b65a524f4
keywords:
- PSM_ENABLEWIZBUTTONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_ENABLEWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01fb30fa3337aed369c2cd24a1296785bd6b3a79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942378"
---
# <a name="psm_enablewizbuttons-message"></a><span data-ttu-id="a635a-105">\_Message PSM ENABLEWIZBUTTONS</span><span class="sxs-lookup"><span data-stu-id="a635a-105">PSM\_ENABLEWIZBUTTONS message</span></span>

<span data-ttu-id="a635a-106">Active ou désactive tous les boutons standard dans un Assistant Aero.</span><span class="sxs-lookup"><span data-stu-id="a635a-106">Enables or disables any of the standard buttons in an Aero wizard.</span></span> <span data-ttu-id="a635a-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ EnableWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) .</span><span class="sxs-lookup"><span data-stu-id="a635a-107">You can send this message explicitly or use the [**PropSheet\_EnableWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a635a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a635a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a635a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a635a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a635a-110">Une ou plusieurs des valeurs suivantes qui spécifient les boutons de la feuille de propriétés qui doivent être activés.</span><span class="sxs-lookup"><span data-stu-id="a635a-110">One or more of the following values that specify which property sheet buttons are to be enabled.</span></span> <span data-ttu-id="a635a-111">Si une valeur de bouton est incluse à la fois dans ce paramètre et dans *lParam*, elle est activée.</span><span class="sxs-lookup"><span data-stu-id="a635a-111">If a button value is included in both this parameter and *lParam*, it is enabled.</span></span>



| <span data-ttu-id="a635a-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="a635a-112">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="a635a-113">Signification</span><span class="sxs-lookup"><span data-stu-id="a635a-113">Meaning</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="a635a-114"><dt>**PSWIZB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a635a-114"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="a635a-115">Bouton **précédent** .</span><span class="sxs-lookup"><span data-stu-id="a635a-115">The **Back** button.</span></span><br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <span data-ttu-id="a635a-116"><dt>**PSWIZB \_ Annuler**</dt></span><span class="sxs-lookup"><span data-stu-id="a635a-116"><dt>**PSWIZB\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="a635a-117">Bouton **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="a635a-117">The **Cancel** button.</span></span><br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="a635a-118"><dt>**PSWIZB \_ DISABLEDFINISH**</dt></span><span class="sxs-lookup"><span data-stu-id="a635a-118"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="a635a-119">Bouton **Terminer** .</span><span class="sxs-lookup"><span data-stu-id="a635a-119">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="a635a-120"><dt>**PSWIZB \_ terminer**</dt></span><span class="sxs-lookup"><span data-stu-id="a635a-120"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="a635a-121">Bouton **Terminer** .</span><span class="sxs-lookup"><span data-stu-id="a635a-121">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="a635a-122"><dt>**PSWIZB \_ suivant**</dt></span><span class="sxs-lookup"><span data-stu-id="a635a-122"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="a635a-123">Bouton **suivant** .</span><span class="sxs-lookup"><span data-stu-id="a635a-123">The **Next** button.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="a635a-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a635a-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a635a-125">Une ou plusieurs des valeurs utilisées dans *wParam*, en spécifiant les boutons affectés par cet appel.</span><span class="sxs-lookup"><span data-stu-id="a635a-125">One or more of the same values used in *wParam*, specifying which buttons are affected by this call.</span></span> <span data-ttu-id="a635a-126">Si une valeur de bouton apparaît dans ce paramètre mais pas dans *wParam*, elle indique que le bouton doit être désactivé.</span><span class="sxs-lookup"><span data-stu-id="a635a-126">If a button value appears in this parameter but not in *wParam*, it indicates that the button should be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a635a-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a635a-127">Return value</span></span>

<span data-ttu-id="a635a-128">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="a635a-128">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a635a-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a635a-129">Requirements</span></span>



| <span data-ttu-id="a635a-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a635a-130">Requirement</span></span> | <span data-ttu-id="a635a-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="a635a-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a635a-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a635a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a635a-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a635a-133">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a635a-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a635a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a635a-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a635a-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a635a-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="a635a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a635a-137"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="a635a-137"><dt>Prsht.h</dt></span></span> </dl> |



 

 





