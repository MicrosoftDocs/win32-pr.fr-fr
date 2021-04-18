---
title: Message PSM_PRESSBUTTON (Prsht. h)
description: Simule la sélection d’un bouton de feuille de propriétés. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet PressButton.
ms.assetid: 82a55a29-d916-47ee-b0a0-f685a3a386d9
keywords:
- PSM_PRESSBUTTON les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_PRESSBUTTON
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b54b04dcc7b1263019f49ff8c1de0d2c21a12a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467103"
---
# <a name="psm_pressbutton-message"></a><span data-ttu-id="47267-105">\_Message PSM PRESSBUTTON</span><span class="sxs-lookup"><span data-stu-id="47267-105">PSM\_PRESSBUTTON message</span></span>

<span data-ttu-id="47267-106">Simule la sélection d’un bouton de feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="47267-106">Simulates the selection of a property sheet button.</span></span> <span data-ttu-id="47267-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ PressButton**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) .</span><span class="sxs-lookup"><span data-stu-id="47267-107">You can send this message explicitly or by using the [**PropSheet\_PressButton**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="47267-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47267-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47267-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="47267-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="47267-110">Index du bouton à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="47267-110">Index of the button to select.</span></span> <span data-ttu-id="47267-111">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="47267-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="47267-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="47267-112">Value</span></span>                                                                                                                                                            | <span data-ttu-id="47267-113">Signification</span><span class="sxs-lookup"><span data-stu-id="47267-113">Meaning</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PSBTN_APPLYNOW"></span><span id="psbtn_applynow"></span><dl> <span data-ttu-id="47267-114"><dt>**PSBTN \_ APPLYNOW**</dt></span><span class="sxs-lookup"><span data-stu-id="47267-114"><dt>**PSBTN\_APPLYNOW**</dt></span></span> </dl> | <span data-ttu-id="47267-115">Sélectionne le bouton **appliquer** .</span><span class="sxs-lookup"><span data-stu-id="47267-115">Selects the **Apply** button.</span></span> <span data-ttu-id="47267-116">Cette valeur n’est pas valide lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="47267-116">This value is not valid when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span><br/> |
| <span id="PSBTN_BACK"></span><span id="psbtn_back"></span><dl> <span data-ttu-id="47267-117"><dt>**PSBTN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="47267-117"><dt>**PSBTN\_BACK**</dt></span></span> </dl>             | <span data-ttu-id="47267-118">Sélectionne le bouton **précédent** .</span><span class="sxs-lookup"><span data-stu-id="47267-118">Selects the **Back** button.</span></span><br/>                                                                                                         |
| <span id="PSBTN_CANCEL"></span><span id="psbtn_cancel"></span><dl> <span data-ttu-id="47267-119"><dt>**PSBTN \_ Annuler**</dt></span><span class="sxs-lookup"><span data-stu-id="47267-119"><dt>**PSBTN\_CANCEL**</dt></span></span> </dl>       | <span data-ttu-id="47267-120">Sélectionne le bouton **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="47267-120">Selects the **Cancel** button.</span></span><br/>                                                                                                       |
| <span id="PSBTN_FINISH"></span><span id="psbtn_finish"></span><dl> <span data-ttu-id="47267-121"><dt>**PSBTN \_ terminer**</dt></span><span class="sxs-lookup"><span data-stu-id="47267-121"><dt>**PSBTN\_FINISH**</dt></span></span> </dl>       | <span data-ttu-id="47267-122">Sélectionne le bouton **Terminer** .</span><span class="sxs-lookup"><span data-stu-id="47267-122">Selects the **Finish** button.</span></span><br/>                                                                                                       |
| <span id="PSBTN_HELP"></span><span id="psbtn_help"></span><dl> <span data-ttu-id="47267-123"><dt>**aide de PSBTN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="47267-123"><dt>**PSBTN\_HELP**</dt></span></span> </dl>             | <span data-ttu-id="47267-124">Sélectionne le bouton **aide** .</span><span class="sxs-lookup"><span data-stu-id="47267-124">Selects the **Help** button.</span></span> <span data-ttu-id="47267-125">Cette valeur n’est pas valide lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="47267-125">This value is not valid when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span><br/>  |
| <span id="PSBTN_NEXT"></span><span id="psbtn_next"></span><dl> <span data-ttu-id="47267-126"><dt>**PSBTN \_ suivant**</dt></span><span class="sxs-lookup"><span data-stu-id="47267-126"><dt>**PSBTN\_NEXT**</dt></span></span> </dl>             | <span data-ttu-id="47267-127">Sélectionne le bouton **suivant** .</span><span class="sxs-lookup"><span data-stu-id="47267-127">Selects the **Next** button.</span></span><br/>                                                                                                         |
| <span id="PSBTN_OK"></span><span id="psbtn_ok"></span><dl> <span data-ttu-id="47267-128"><dt>**PSBTN \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="47267-128"><dt>**PSBTN\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="47267-129">Sélectionne le bouton **OK** .</span><span class="sxs-lookup"><span data-stu-id="47267-129">Selects the **OK** button.</span></span> <span data-ttu-id="47267-130">Cette valeur n’est pas valide lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="47267-130">This value is not valid when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="47267-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="47267-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="47267-132">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="47267-132">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47267-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="47267-133">Return value</span></span>

<span data-ttu-id="47267-134">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="47267-134">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="47267-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47267-135">Requirements</span></span>



| <span data-ttu-id="47267-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47267-136">Requirement</span></span> | <span data-ttu-id="47267-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="47267-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="47267-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47267-138">Minimum supported client</span></span><br/> | <span data-ttu-id="47267-139">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47267-139">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="47267-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47267-140">Minimum supported server</span></span><br/> | <span data-ttu-id="47267-141">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47267-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="47267-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="47267-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="47267-143"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="47267-143"><dt>Prsht.h</dt></span></span> </dl> |



 

 





