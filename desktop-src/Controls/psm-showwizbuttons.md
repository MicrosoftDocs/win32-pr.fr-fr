---
title: Message PSM_SHOWWIZBUTTONS (Prsht. h)
description: Affiche ou masque les boutons dans un Assistant. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet ShowWizButtons.
ms.assetid: 669c4e51-cac1-40e1-8f23-afae0e41fc9b
keywords:
- PSM_SHOWWIZBUTTONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_SHOWWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22e8d1fc54d556240ef3fa6d6b6185a669978b84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106538807"
---
# <a name="psm_showwizbuttons-message"></a><span data-ttu-id="f010f-105">\_Message PSM SHOWWIZBUTTONS</span><span class="sxs-lookup"><span data-stu-id="f010f-105">PSM\_SHOWWIZBUTTONS message</span></span>

<span data-ttu-id="f010f-106">Affiche ou masque les boutons dans un Assistant.</span><span class="sxs-lookup"><span data-stu-id="f010f-106">Shows or hides buttons in a wizard.</span></span> <span data-ttu-id="f010f-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) .</span><span class="sxs-lookup"><span data-stu-id="f010f-107">You can send this message explicitly or by using the [**PropSheet\_ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f010f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f010f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f010f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f010f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f010f-110">Une ou plusieurs des valeurs suivantes qui spécifient les boutons de la feuille de propriétés à afficher.</span><span class="sxs-lookup"><span data-stu-id="f010f-110">One or more of the following values that specify which property sheet buttons are to be shown.</span></span> <span data-ttu-id="f010f-111">Si une valeur de bouton est incluse à la fois dans ce paramètre et dans *lParam*, elle est affichée.</span><span class="sxs-lookup"><span data-stu-id="f010f-111">If a button value is included in both this parameter and *lParam*, it is shown.</span></span>



| <span data-ttu-id="f010f-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="f010f-112">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="f010f-113">Signification</span><span class="sxs-lookup"><span data-stu-id="f010f-113">Meaning</span></span>                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="f010f-114"><dt>**PSWIZB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f010f-114"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="f010f-115">Bouton **précédent** .</span><span class="sxs-lookup"><span data-stu-id="f010f-115">The **Back** button.</span></span><br/>                                                            |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <span data-ttu-id="f010f-116"><dt>**PSWIZB \_ Annuler**</dt></span><span class="sxs-lookup"><span data-stu-id="f010f-116"><dt>**PSWIZB\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="f010f-117">Bouton **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="f010f-117">The **Cancel** button.</span></span><br/>                                                          |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="f010f-118"><dt>**PSWIZB \_ DISABLEDFINISH**</dt></span><span class="sxs-lookup"><span data-stu-id="f010f-118"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="f010f-119">Bouton **Terminer** .</span><span class="sxs-lookup"><span data-stu-id="f010f-119">The **Finish** button.</span></span><br/>                                                          |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="f010f-120"><dt>**PSWIZB \_ terminer**</dt></span><span class="sxs-lookup"><span data-stu-id="f010f-120"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="f010f-121">Bouton **Terminer** .</span><span class="sxs-lookup"><span data-stu-id="f010f-121">The **Finish** button.</span></span><br/>                                                          |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="f010f-122"><dt>**PSWIZB \_ suivant**</dt></span><span class="sxs-lookup"><span data-stu-id="f010f-122"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="f010f-123">Bouton **suivant** .</span><span class="sxs-lookup"><span data-stu-id="f010f-123">The **Next** button.</span></span><br/>                                                            |
| <span id="PSWIZB_SHOW"></span><span id="pswizb_show"></span><dl> <span data-ttu-id="f010f-124"><dt>**PSWIZB \_ afficher**</dt></span><span class="sxs-lookup"><span data-stu-id="f010f-124"><dt>**PSWIZB\_SHOW**</dt></span></span> </dl>                               | <span data-ttu-id="f010f-125">Définit uniquement cet indicateur (défini comme zéro) pour masquer tous les boutons spécifiés dans *lParam*.</span><span class="sxs-lookup"><span data-stu-id="f010f-125">Set only this flag (defined as zero) to hide all buttons specified in *lParam*.</span></span><br/> |
| <span id="PSWIZB_RESTORE"></span><span id="pswizb_restore"></span><dl> <span data-ttu-id="f010f-126"><dt>**\_restauration PSWIZB**</dt></span><span class="sxs-lookup"><span data-stu-id="f010f-126"><dt>**PSWIZB\_RESTORE**</dt></span></span> </dl>                      | <span data-ttu-id="f010f-127">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="f010f-127">Not implemented.</span></span><br/>                                                                |



 

</dd> <dt>

<span data-ttu-id="f010f-128">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f010f-128">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f010f-129">Une ou plusieurs des valeurs utilisées dans *wParam*, en spécifiant les boutons affectés par cet appel.</span><span class="sxs-lookup"><span data-stu-id="f010f-129">One or more of the same values used in *wParam*, specifying which buttons are affected by this call.</span></span> <span data-ttu-id="f010f-130">Si une valeur de bouton apparaît dans ce paramètre mais pas dans *wParam*, le bouton est masqué.</span><span class="sxs-lookup"><span data-stu-id="f010f-130">If a button value appears in this parameter but not in *wParam*, the button is hidden.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f010f-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f010f-131">Return value</span></span>

<span data-ttu-id="f010f-132">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="f010f-132">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f010f-133">Notes</span><span class="sxs-lookup"><span data-stu-id="f010f-133">Remarks</span></span>

<span data-ttu-id="f010f-134">Les assistants affichent trois ou quatre boutons sous chaque page.</span><span class="sxs-lookup"><span data-stu-id="f010f-134">Wizards display either three or four buttons below each page.</span></span> <span data-ttu-id="f010f-135">Ce message est utilisé pour spécifier les boutons à afficher.</span><span class="sxs-lookup"><span data-stu-id="f010f-135">This message is used to specify which buttons are visible.</span></span> <span data-ttu-id="f010f-136">Les assistants s' **affichent** normalement, **annulent** et un bouton **suivant** ou **Terminer** .</span><span class="sxs-lookup"><span data-stu-id="f010f-136">Wizards normally display **Back**, **Cancel**, and either a **Next** or **Finish** button.</span></span> <span data-ttu-id="f010f-137">Le bouton **Annuler** est toujours visible.</span><span class="sxs-lookup"><span data-stu-id="f010f-137">The **Cancel** button is always visible.</span></span>

<span data-ttu-id="f010f-138">En règle générale, définissez **PSWIZB \_ Finish** ou **PSWIZB \_ DISABLEDFINISH** pour remplacer le bouton **Next** par un bouton **Finish** .</span><span class="sxs-lookup"><span data-stu-id="f010f-138">Typically, set **PSWIZB\_FINISH** or **PSWIZB\_DISABLEDFINISH** to replace the **Next** button with a **Finish** button.</span></span> <span data-ttu-id="f010f-139">Pour afficher les boutons **suivant** et **Terminer** simultanément, définissez l’indicateur **PSH \_ WIZARDHASFINISH** dans le membre **dwFlags** de la structure [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) lorsque vous créez l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="f010f-139">To display **Next** and **Finish** buttons simultaneously, set the **PSH\_WIZARDHASFINISH** flag in the **dwFlags** member of the [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure when you create the wizard.</span></span> <span data-ttu-id="f010f-140">Chaque page affiche ensuite les quatre boutons suivants : **précédent**, **suivant**, **Annuler** et **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="f010f-140">Every page will then display all four buttons: **Back**, **Next**, **Cancel**, and **Finish**.</span></span>

<span data-ttu-id="f010f-141">Si vous utilisez la macro [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) pour envoyer ce message, celui-ci sera publié.</span><span class="sxs-lookup"><span data-stu-id="f010f-141">If you use the [**PropSheet\_ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) macro to send this message, it will be posted.</span></span> <span data-ttu-id="f010f-142">À tout moment, vous pouvez utiliser [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) pour envoyer des **\_ SHOWWIZBUTTONS PSM**.</span><span class="sxs-lookup"><span data-stu-id="f010f-142">At any other time, you can use [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) to send **PSM\_SHOWWIZBUTTONS**.</span></span>

<span data-ttu-id="f010f-143">Si votre gestionnaire de notifications utilise [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) pour envoyer un message **PSM \_ SHOWWIZBUTTONS** , ne faites rien qui affectera le focus de la fenêtre tant que le gestionnaire ne sera pas retourné.</span><span class="sxs-lookup"><span data-stu-id="f010f-143">If your notification handler uses [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) to send a **PSM\_SHOWWIZBUTTONS** message, do nothing that will affect window focus until after the handler returns.</span></span> <span data-ttu-id="f010f-144">Par exemple, si vous appelez [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immédiatement après avoir utilisé **PostMessage** pour envoyer des **\_ SHOWWIZBUTTONS PSM**, la boîte de message reçoit le focus.</span><span class="sxs-lookup"><span data-stu-id="f010f-144">For example, if you call [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immediately after using **PostMessage** to send **PSM\_SHOWWIZBUTTONS**, the message box will receive focus.</span></span> <span data-ttu-id="f010f-145">Étant donné que les messages publiés ne sont pas remis tant qu’ils n’atteignent pas le début de la file d’attente de messages, le message **\_ SHOWWIZBUTTONS PSM** n’est pas remis tant que l’Assistant n’a pas perdu le focus sur la boîte de message.</span><span class="sxs-lookup"><span data-stu-id="f010f-145">Since posted messages are not delivered until they reach the head of the message queue, the **PSM\_SHOWWIZBUTTONS** message will not be delivered until after the wizard has lost focus to the message box.</span></span> <span data-ttu-id="f010f-146">Par conséquent, la feuille de propriétés ne sera pas en mesure de définir correctement le focus pour les boutons.</span><span class="sxs-lookup"><span data-stu-id="f010f-146">As a result, the property sheet will not be able to properly set the focus for the buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="f010f-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f010f-147">Requirements</span></span>



| <span data-ttu-id="f010f-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f010f-148">Requirement</span></span> | <span data-ttu-id="f010f-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="f010f-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f010f-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f010f-150">Minimum supported client</span></span><br/> | <span data-ttu-id="f010f-151">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f010f-151">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f010f-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f010f-152">Minimum supported server</span></span><br/> | <span data-ttu-id="f010f-153">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f010f-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f010f-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="f010f-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="f010f-155"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="f010f-155"><dt>Prsht.h</dt></span></span> </dl> |



 

