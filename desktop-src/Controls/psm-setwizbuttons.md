---
title: Message PSM_SETWIZBUTTONS (Prsht. h)
description: Active ou désactive les boutons précédent, suivant et terminer dans un Assistant. Vous pouvez également utiliser la \_ macro PropSheet SetWizButtons pour envoyer le message.
ms.assetid: e32abdb0-12d1-471e-a309-662389e0dba4
keywords:
- PSM_SETWIZBUTTONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_SETWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79cb7b6fbc0c91e1e94df62c2c8401839ace2d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104194"
---
# <a name="psm_setwizbuttons-message"></a><span data-ttu-id="fc1e2-105">\_Message PSM SETWIZBUTTONS</span><span class="sxs-lookup"><span data-stu-id="fc1e2-105">PSM\_SETWIZBUTTONS message</span></span>

<span data-ttu-id="fc1e2-106">Active ou désactive les boutons **précédent**, **suivant** et **Terminer** dans un Assistant.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-106">Enables or disables the **Back**, **Next**, and **Finish** buttons in a wizard.</span></span> <span data-ttu-id="fc1e2-107">Vous pouvez également utiliser la macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) pour envoyer le message.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-107">You can also use the [**PropSheet\_SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) macro to post the message.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc1e2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc1e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc1e2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc1e2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc1e2-110">Définissez ce paramètre sur PSWIZBF \_ ELEVATIONREQUIRED pour afficher l’icône avec élévation de privilèges sur les boutons spécifiés dans *lParam*.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-110">Set this parameter to PSWIZBF\_ELEVATIONREQUIRED to display the elevated icon on the buttons specified in *lParam*.</span></span> <span data-ttu-id="fc1e2-111">L’icône avec élévation de privilèges (ou icône de blindage UAC) indique que l’invite d’élévation sera utilisée pour inviter l’utilisateur à approuver ou à fournir des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-111">The elevated icon (or UAC shield icon) indicates that the elevation prompt will be used to prompt the user for approval or credentials.</span></span> <span data-ttu-id="fc1e2-112">Pour plus d’informations, consultez [conception d’applications UAC pour Windows Vista]( /previous-versions/bb756973(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="fc1e2-112">For more information, see [Designing UAC Applications for Windows Vista]( /previous-versions/bb756973(v=msdn.10)).</span></span>

> [!Note]  
> <span data-ttu-id="fc1e2-113">L’affichage de l’icône de bouclier UAC est pris en charge uniquement dans AeroWizards (PSH \_ AEROWIZARD).</span><span class="sxs-lookup"><span data-stu-id="fc1e2-113">Displaying the UAC shield icon is only supported in AeroWizards (PSH\_AEROWIZARD).</span></span>

 

</dd> <dt>

<span data-ttu-id="fc1e2-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc1e2-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc1e2-115">Valeur qui spécifie les boutons de la feuille de propriétés qui sont activés.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-115">Value that specifies which property sheet buttons are enabled.</span></span> <span data-ttu-id="fc1e2-116">Vous pouvez combiner un ou plusieurs des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-116">You can combine one or more of the following flags.</span></span>



| <span data-ttu-id="fc1e2-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc1e2-117">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="fc1e2-118">Signification</span><span class="sxs-lookup"><span data-stu-id="fc1e2-118">Meaning</span></span>                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="fc1e2-119"><dt>**PSWIZB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fc1e2-119"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="fc1e2-120">Active le bouton **précédent** .</span><span class="sxs-lookup"><span data-stu-id="fc1e2-120">Enables the **Back** button.</span></span> <span data-ttu-id="fc1e2-121">Si cet indicateur n’est pas défini, le bouton **précédent** s’affiche comme étant désactivé.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-121">If this flag is not set, the **Back** button is displayed as disabled.</span></span><br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="fc1e2-122"><dt>**PSWIZB \_ DISABLEDFINISH**</dt></span><span class="sxs-lookup"><span data-stu-id="fc1e2-122"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="fc1e2-123">Affiche un bouton **Terminer** désactivé.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-123">Displays a disabled **Finish** button.</span></span><br/>                                                              |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="fc1e2-124"><dt>**PSWIZB \_ terminer**</dt></span><span class="sxs-lookup"><span data-stu-id="fc1e2-124"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="fc1e2-125">Affiche un bouton **Terminer** activé.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-125">Displays an enabled **Finish** button.</span></span><br/>                                                              |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="fc1e2-126"><dt>**PSWIZB \_ suivant**</dt></span><span class="sxs-lookup"><span data-stu-id="fc1e2-126"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="fc1e2-127">Active le bouton **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-127">Enables the **Next** button.</span></span> <span data-ttu-id="fc1e2-128">Si cet indicateur n’est pas défini, le bouton **suivant** s’affiche comme étant désactivé.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-128">If this flag is not set, the **Next** button is displayed as disabled.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc1e2-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fc1e2-129">Return value</span></span>

<span data-ttu-id="fc1e2-130">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-130">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc1e2-131">Notes</span><span class="sxs-lookup"><span data-stu-id="fc1e2-131">Remarks</span></span>

<span data-ttu-id="fc1e2-132">Si votre gestionnaire de notifications utilise [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) pour envoyer un message **PSM \_ SETWIZBUTTONS** , ne faites rien qui affectera le focus de la fenêtre tant que le gestionnaire ne sera pas retourné.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-132">If your notification handler uses [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) to send a **PSM\_SETWIZBUTTONS** message, do nothing that will affect window focus until after the handler returns.</span></span> <span data-ttu-id="fc1e2-133">Par exemple, si vous appelez [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immédiatement après avoir utilisé **PostMessage** pour envoyer des **\_ SETWIZBUTTONS PSM**, la boîte de message reçoit le focus.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-133">For example, if you call [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immediately after using **PostMessage** to send **PSM\_SETWIZBUTTONS**, the message box will receive focus.</span></span> <span data-ttu-id="fc1e2-134">Étant donné que les messages publiés ne sont pas remis tant qu’ils n’atteignent pas le début de la file d’attente de messages, le message **\_ SETWIZBUTTONS PSM** n’est pas remis tant que l’Assistant n’a pas perdu le focus sur la boîte de message.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-134">Since posted messages are not delivered until they reach the head of the message queue, the **PSM\_SETWIZBUTTONS** message will not be delivered until after the wizard has lost focus to the message box.</span></span> <span data-ttu-id="fc1e2-135">Par conséquent, la feuille de propriétés ne sera pas en mesure de définir correctement le focus pour les boutons.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-135">As a result, the property sheet will not be able to properly set the focus for the buttons.</span></span>

<span data-ttu-id="fc1e2-136">Si vous envoyez le \_ message SETWIZBUTTONS PSM lors de la gestion de la notification [ \_ SetActive PSN](psn-setactive.md) , utilisez la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) au lieu de la fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="fc1e2-136">If you send the PSM\_SETWIZBUTTONS message during your handling of the [PSN\_SETACTIVE](psn-setactive.md) notification, use the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function rather than the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function.</span></span> <span data-ttu-id="fc1e2-137">Dans le cas contraire, le système ne met pas à jour les boutons correctement.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-137">Otherwise, the system will not update the buttons properly.</span></span> <span data-ttu-id="fc1e2-138">Si vous utilisez la macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) pour envoyer ce message, celui-ci sera publié.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-138">If you use the [**PropSheet\_SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) macro to send this message, it will be posted.</span></span> <span data-ttu-id="fc1e2-139">À tout moment, vous pouvez utiliser **SendMessage** pour envoyer des **\_ SETWIZBUTTONS PSM**.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-139">At any other time, you can use **SendMessage** to send **PSM\_SETWIZBUTTONS**.</span></span>

<span data-ttu-id="fc1e2-140">Les assistants affichent trois ou quatre boutons sous chaque page.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-140">Wizards display either three or four buttons below each page.</span></span> <span data-ttu-id="fc1e2-141">Ce message est utilisé pour spécifier les boutons qui sont activés.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-141">This message is used to specify which buttons are enabled.</span></span> <span data-ttu-id="fc1e2-142">Les assistants s' **affichent** normalement, **annulent** et un bouton **suivant** ou **Terminer** .</span><span class="sxs-lookup"><span data-stu-id="fc1e2-142">Wizards normally display **Back**, **Cancel**, and either a **Next** or **Finish** button.</span></span> <span data-ttu-id="fc1e2-143">En général, vous activez uniquement le bouton **suivant** pour la page d’accueil, **suivant** et **précédent** pour les pages intérieures, et en **arrière** et en **fin** pour la page de fin.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-143">You typically enable only the **Next** button for the welcome page, **Next** and **Back** for interior pages, and **Back** and **Finish** for the completion page.</span></span> <span data-ttu-id="fc1e2-144">Le bouton **Annuler** est toujours activé.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-144">The **Cancel** button is always enabled.</span></span> <span data-ttu-id="fc1e2-145">Normalement, la définition de PSWIZB \_ Finish ou PSWIZB \_ DISABLEDFINISH remplace le bouton **suivant** par un bouton **Terminer** .</span><span class="sxs-lookup"><span data-stu-id="fc1e2-145">Normally, setting PSWIZB\_FINISH or PSWIZB\_DISABLEDFINISH replaces the **Next** button with a **Finish** button.</span></span> <span data-ttu-id="fc1e2-146">Pour afficher les boutons **suivant** et **Terminer** simultanément, définissez l' \_ indicateur PSH WIZARDHASFINISH dans le membre **dwFlags** de la structure [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) de l’Assistant lorsque vous créez l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-146">To display **Next** and **Finish** buttons simultaneously, set the PSH\_WIZARDHASFINISH flag in the **dwFlags** member of the wizard's [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure when you create the wizard.</span></span> <span data-ttu-id="fc1e2-147">Chaque page affiche ensuite les quatre boutons.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-147">Every page will then display all four buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc1e2-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc1e2-148">Requirements</span></span>



| <span data-ttu-id="fc1e2-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc1e2-149">Requirement</span></span> | <span data-ttu-id="fc1e2-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc1e2-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fc1e2-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc1e2-151">Minimum supported client</span></span><br/> | <span data-ttu-id="fc1e2-152">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc1e2-152">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fc1e2-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc1e2-153">Minimum supported server</span></span><br/> | <span data-ttu-id="fc1e2-154">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc1e2-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fc1e2-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="fc1e2-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc1e2-156"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc1e2-156"><dt>Prsht.h</dt></span></span> </dl> |



 

