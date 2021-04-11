---
title: Message PSM_SETBUTTONTEXT (Prsht. h)
description: Définit le texte d’un bouton dans un Assistant Aero. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet SetButtonText.
ms.assetid: 30b7afd1-5094-430f-9c48-d87832d96050
keywords:
- PSM_SETBUTTONTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_SETBUTTONTEXT
- PSM_SETBUTTONTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41a0b55f73fc7084e89f54c1e741d12000b0f949
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032752"
---
# <a name="psm_setbuttontext-message"></a><span data-ttu-id="a3eb5-105">\_Message PSM SETBUTTONTEXT</span><span class="sxs-lookup"><span data-stu-id="a3eb5-105">PSM\_SETBUTTONTEXT message</span></span>

<span data-ttu-id="a3eb5-106">Définit le texte d’un bouton dans un Assistant Aero.</span><span class="sxs-lookup"><span data-stu-id="a3eb5-106">Sets the text on a button in an Aero wizard.</span></span> <span data-ttu-id="a3eb5-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) .</span><span class="sxs-lookup"><span data-stu-id="a3eb5-107">You can send this message explicitly or by using the [**PropSheet\_SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a3eb5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3eb5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3eb5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a3eb5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3eb5-110">L’une des valeurs suivantes spécifiant le bouton dont le texte est défini.</span><span class="sxs-lookup"><span data-stu-id="a3eb5-110">One of the following values specifying the button whose text is set.</span></span>



| <span data-ttu-id="a3eb5-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3eb5-111">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="a3eb5-112">Signification</span><span class="sxs-lookup"><span data-stu-id="a3eb5-112">Meaning</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="a3eb5-113"><dt>**PSWIZB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a3eb5-113"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="a3eb5-114">Bouton **précédent** .</span><span class="sxs-lookup"><span data-stu-id="a3eb5-114">The **Back** button.</span></span><br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <span data-ttu-id="a3eb5-115"><dt>**PSWIZB \_ Annuler**</dt></span><span class="sxs-lookup"><span data-stu-id="a3eb5-115"><dt>**PSWIZB\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="a3eb5-116">Bouton **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="a3eb5-116">The **Cancel** button.</span></span><br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="a3eb5-117"><dt>**PSWIZB \_ DISABLEDFINISH**</dt></span><span class="sxs-lookup"><span data-stu-id="a3eb5-117"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="a3eb5-118">Bouton **Terminer** .</span><span class="sxs-lookup"><span data-stu-id="a3eb5-118">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="a3eb5-119"><dt>**PSWIZB \_ terminer**</dt></span><span class="sxs-lookup"><span data-stu-id="a3eb5-119"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="a3eb5-120">Bouton **Terminer** .</span><span class="sxs-lookup"><span data-stu-id="a3eb5-120">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="a3eb5-121"><dt>**PSWIZB \_ suivant**</dt></span><span class="sxs-lookup"><span data-stu-id="a3eb5-121"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="a3eb5-122">Bouton **suivant** .</span><span class="sxs-lookup"><span data-stu-id="a3eb5-122">The **Next** button.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="a3eb5-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3eb5-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3eb5-124">Texte à définir.</span><span class="sxs-lookup"><span data-stu-id="a3eb5-124">The text to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3eb5-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a3eb5-125">Return value</span></span>

<span data-ttu-id="a3eb5-126">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="a3eb5-126">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3eb5-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3eb5-127">Requirements</span></span>



| <span data-ttu-id="a3eb5-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3eb5-128">Requirement</span></span> | <span data-ttu-id="a3eb5-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3eb5-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a3eb5-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3eb5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a3eb5-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a3eb5-131">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a3eb5-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3eb5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a3eb5-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a3eb5-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a3eb5-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3eb5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3eb5-135"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3eb5-135"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="a3eb5-136">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="a3eb5-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a3eb5-137">**PSM \_ SETBUTTONTEXTW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="a3eb5-137">**PSM\_SETBUTTONTEXTW** (Unicode)</span></span><br/>                                       |



 

 





