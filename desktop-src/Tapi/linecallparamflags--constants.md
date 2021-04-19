---
description: Les \_ constantes LINECALLPARAMFLAGS décrivent différents indicateurs d’État sur un appel.
ms.assetid: f323ec9f-5bab-4b5d-93ef-8a552ee0d591
title: Constantes LINECALLPARAMFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e70fe2721e6fce0ac509b50290b1ec3788f3c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539193"
---
# <a name="linecallparamflags_-constants"></a><span data-ttu-id="0c1dd-103">\_Constantes LINECALLPARAMFLAGS</span><span class="sxs-lookup"><span data-stu-id="0c1dd-103">LINECALLPARAMFLAGS\_ Constants</span></span>

<span data-ttu-id="0c1dd-104">Les constantes **LINECALLPARAMFLAGS \_** décrivent différents indicateurs d’État sur un appel.</span><span class="sxs-lookup"><span data-stu-id="0c1dd-104">The **LINECALLPARAMFLAGS\_** constants describe various status flags about a call.</span></span>

<dl> <dt>

<span data-ttu-id="0c1dd-105"><span id="LINECALLPARAMFLAGS_BLOCKID"></span><span id="linecallparamflags_blockid"></span>**LINECALLPARAMFLAGS \_ BLOCKID**</span><span class="sxs-lookup"><span data-stu-id="0c1dd-105"><span id="LINECALLPARAMFLAGS_BLOCKID"></span><span id="linecallparamflags_blockid"></span>**LINECALLPARAMFLAGS\_BLOCKID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c1dd-106">L’identité de l’expéditeur doit être masquée (ID de l’appelant du bloc).</span><span class="sxs-lookup"><span data-stu-id="0c1dd-106">The originator identity should be concealed (block caller ID).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c1dd-107"><span id="LINECALLPARAMFLAGS_DESTOFFHOOK"></span><span id="linecallparamflags_destoffhook"></span>**LINECALLPARAMFLAGS \_ DESTOFFHOOK**</span><span class="sxs-lookup"><span data-stu-id="0c1dd-107"><span id="LINECALLPARAMFLAGS_DESTOFFHOOK"></span><span id="linecallparamflags_destoffhook"></span>**LINECALLPARAMFLAGS\_DESTOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c1dd-108">Le téléphone du tiers appelé doit être automatiquement pris offhook.</span><span class="sxs-lookup"><span data-stu-id="0c1dd-108">The called party's phone should be automatically taken offhook.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c1dd-109"><span id="LINECALLPARAMFLAGS_IDLE"></span><span id="linecallparamflags_idle"></span>**LINECALLPARAMFLAGS \_ inactif**</span><span class="sxs-lookup"><span data-stu-id="0c1dd-109"><span id="LINECALLPARAMFLAGS_IDLE"></span><span id="linecallparamflags_idle"></span>**LINECALLPARAMFLAGS\_IDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c1dd-110">L’appel doit être issu de l’apparence d’un appel inactif et ne pas joindre un appel en cours.</span><span class="sxs-lookup"><span data-stu-id="0c1dd-110">The call should be originated on an idle call appearance and not join a call in progress.</span></span> <span data-ttu-id="0c1dd-111">Lors de l’utilisation de la fonction [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) , si la \_ valeur d’inactivité LINECALLPARAMFLAGS n’est pas définie et qu’il existe un appel sur la ligne, la fonction s’arrête dans l’appel existant si nécessaire pour effectuer le nouvel appel.</span><span class="sxs-lookup"><span data-stu-id="0c1dd-111">When using the [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) function, if the LINECALLPARAMFLAGS\_IDLE value is not set and there is an existing call on the line, the function breaks into the existing call if necessary to make the new call.</span></span> <span data-ttu-id="0c1dd-112">S’il n’existe aucun appel, la fonction effectue le nouvel appel comme spécifié.</span><span class="sxs-lookup"><span data-stu-id="0c1dd-112">If there is no existing call, the function makes the new call as specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c1dd-113"><span id="LINECALLPARAMFLAGS_NOHOLDCONFERENCE"></span><span id="linecallparamflags_noholdconference"></span>**LINECALLPARAMFLAGS \_ NOHOLDCONFERENCE**</span><span class="sxs-lookup"><span data-stu-id="0c1dd-113"><span id="LINECALLPARAMFLAGS_NOHOLDCONFERENCE"></span><span id="linecallparamflags_noholdconference"></span>**LINECALLPARAMFLAGS\_NOHOLDCONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c1dd-114">Ce bit est utilisé uniquement conjointement avec [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) et [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference).</span><span class="sxs-lookup"><span data-stu-id="0c1dd-114">This bit is used only in conjunction with [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) and [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference).</span></span> <span data-ttu-id="0c1dd-115">L’adresse à conférence avec l’appel en cours est spécifiée dans le membre **TargetAddress** dans [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span><span class="sxs-lookup"><span data-stu-id="0c1dd-115">The address to be conferenced with the current call is specified in the **TargetAddress** member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span></span> <span data-ttu-id="0c1dd-116">L’appel de consultation ne dessine pas physiquement la tonalité à partir du commutateur, mais il progresse à travers différents États d’établissement d’appels (par exemple, la numérotation, la procédure).</span><span class="sxs-lookup"><span data-stu-id="0c1dd-116">The consultation call does not physically draw dial tone from the switch, but will progress through various call establishment states (for example, dialing, proceeding).</span></span> <span data-ttu-id="0c1dd-117">Lorsque l’appel de consultation atteint l’état connecté, la Conférence est automatiquement établie. l’appel d’origine, qui était resté à l’état connecté, passe à l’État Conférence ; l’appel de consultation passe à l’État Conférence ; le hConfCall passe à l’état connecté.</span><span class="sxs-lookup"><span data-stu-id="0c1dd-117">When the consultation call reaches the connected state, the conference is automatically established; the original call, which had remained in the connected state, enters the conferenced state; the consultation call enters the conferenced state; the hConfCall enters the connected state.</span></span> <span data-ttu-id="0c1dd-118">Si l’appel de consultation échoue (passe à l’état déconnecté suivi de Idle), le hConfCall passe également à l’état inactif, et l’appel d’origine (qui peut être une conférence existante, dans le cas de **linePrepareAddToConference**) reste dans l’état connecté.</span><span class="sxs-lookup"><span data-stu-id="0c1dd-118">If the consultation call fails (enters the disconnected state followed by idle), the hConfCall also enters the idle state, and the original call (which may have been an existing conference, in the case of **linePrepareAddToConference**) remains in the connected state.</span></span> <span data-ttu-id="0c1dd-119">Le tiers ou les tiers d’origine ne perçoivent jamais l’appel onHold.</span><span class="sxs-lookup"><span data-stu-id="0c1dd-119">The original party (or parties) never perceive the call has having gone onhold.</span></span> <span data-ttu-id="0c1dd-120">Cette fonctionnalité est souvent utilisée pour ajouter un superviseur à un appel de l’agent ACD lorsque cela est nécessaire pour surveiller les interactions avec un appelant irate.</span><span class="sxs-lookup"><span data-stu-id="0c1dd-120">This feature is often used to add a supervisor to an ACD agent call when necessary to monitor interactions with an irate caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c1dd-121"><span id="LINECALLPARAMFLAGS_ONESTEPTRANSFER"></span><span id="linecallparamflags_onesteptransfer"></span>**LINECALLPARAMFLAGS \_ ONESTEPTRANSFER**</span><span class="sxs-lookup"><span data-stu-id="0c1dd-121"><span id="LINECALLPARAMFLAGS_ONESTEPTRANSFER"></span><span id="linecallparamflags_onesteptransfer"></span>**LINECALLPARAMFLAGS\_ONESTEPTRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c1dd-122">Ce bit est utilisé uniquement conjointement avec [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer).</span><span class="sxs-lookup"><span data-stu-id="0c1dd-122">This bit is used only in conjunction with [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer).</span></span> <span data-ttu-id="0c1dd-123">Elle combine le fonctionnement de **lineSetupTransfer** suivi de [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) sur l’appel de consultation en une seule étape.</span><span class="sxs-lookup"><span data-stu-id="0c1dd-123">It combines the operation of **lineSetupTransfer** followed by [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) on the consultation call into a single step.</span></span> <span data-ttu-id="0c1dd-124">L’adresse à composer est spécifiée dans le membre **TargetAddress** dans [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span><span class="sxs-lookup"><span data-stu-id="0c1dd-124">The address to be dialed is specified in the **TargetAddress** member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span></span> <span data-ttu-id="0c1dd-125">L’appel d’origine est placé dans l’état *onholdpendingtransfer* , tout comme si **lineSetupTransfer** était appelé normalement, et l’appel de consultation est établi normalement.</span><span class="sxs-lookup"><span data-stu-id="0c1dd-125">The original call is placed in *onholdpendingtransfer* state, just as if **lineSetupTransfer** were called normally, and the consultation call is established normally.</span></span> <span data-ttu-id="0c1dd-126">L’application doit toujours appeler [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) pour appliquer le transfert.</span><span class="sxs-lookup"><span data-stu-id="0c1dd-126">The application must still call [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) to effect the transfer.</span></span> <span data-ttu-id="0c1dd-127">Cette fonctionnalité est souvent utilisée lors de l’appel d’un transfert à partir d’un serveur via un lien de contrôle d’appel tiers, car ces liens ne prennent pas en charge le processus normal en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="0c1dd-127">This feature is often used when invoking a transfer from a server over a third-party call control link, because such links frequently do not support the normal two-step process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c1dd-128"><span id="LINECALLPARAMFLAGS_ORIGOFFHOOK"></span><span id="linecallparamflags_origoffhook"></span>**LINECALLPARAMFLAGS \_ ORIGOFFHOOK**</span><span class="sxs-lookup"><span data-stu-id="0c1dd-128"><span id="LINECALLPARAMFLAGS_ORIGOFFHOOK"></span><span id="linecallparamflags_origoffhook"></span>**LINECALLPARAMFLAGS\_ORIGOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c1dd-129">Le téléphone de l’expéditeur doit être automatiquement pris offhook.</span><span class="sxs-lookup"><span data-stu-id="0c1dd-129">The originator's phone should be automatically taken offhook.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c1dd-130"><span id="LINECALLPARAMFLAGS_PREDICTIVEDIAL"></span><span id="linecallparamflags_predictivedial"></span>**LINECALLPARAMFLAGS \_ PREDICTIVEDIAL**</span><span class="sxs-lookup"><span data-stu-id="0c1dd-130"><span id="LINECALLPARAMFLAGS_PREDICTIVEDIAL"></span><span id="linecallparamflags_predictivedial"></span>**LINECALLPARAMFLAGS\_PREDICTIVEDIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c1dd-131">Ce bit est utilisé uniquement lors du placement d’un appel sur une adresse avec la fonctionnalité de numérotation prédictive (LINEADDRCAPFLAGS \_ PREDICTIVEDIALER est activé dans le membre **DwAddrCapFlags** de [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)).</span><span class="sxs-lookup"><span data-stu-id="0c1dd-131">This bit is used only when placing a call on an address with predictive dialing capability (LINEADDRCAPFLAGS\_PREDICTIVEDIALER is on in the **dwAddrCapFlags** member in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)).</span></span> <span data-ttu-id="0c1dd-132">Le bit doit être activé pour activer la progression des appels et/ou les fonctionnalités d’analyse des appareils multimédias de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0c1dd-132">The bit must be on to enable the enhanced call progress and/or media device monitoring capabilities of the device.</span></span> <span data-ttu-id="0c1dd-133">Si ce bit n’est pas activé, l’appel est placé sans la progression de l’appel ou la surveillance du type de média, et aucun transfert automatique n’est initié en fonction de l’état de l’appel.</span><span class="sxs-lookup"><span data-stu-id="0c1dd-133">If this bit is not on, the call will be placed without enhanced call progress or media type monitoring, and no automatic transfer will be initiated based on call state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c1dd-134"><span id="LINECALLPARAMFLAGS_SECURE"></span><span id="linecallparamflags_secure"></span>**LINECALLPARAMFLAGS \_ sécurisé**</span><span class="sxs-lookup"><span data-stu-id="0c1dd-134"><span id="LINECALLPARAMFLAGS_SECURE"></span><span id="linecallparamflags_secure"></span>**LINECALLPARAMFLAGS\_SECURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c1dd-135">L’appel doit être configuré comme sécurisé.</span><span class="sxs-lookup"><span data-stu-id="0c1dd-135">The call should be set up as secure.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c1dd-136">Notes</span><span class="sxs-lookup"><span data-stu-id="0c1dd-136">Remarks</span></span>

<span data-ttu-id="0c1dd-137">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="0c1dd-137">No extensibility.</span></span> <span data-ttu-id="0c1dd-138">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="0c1dd-138">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c1dd-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c1dd-139">Requirements</span></span>



| <span data-ttu-id="0c1dd-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c1dd-140">Requirement</span></span> | <span data-ttu-id="0c1dd-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c1dd-141">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0c1dd-142">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="0c1dd-142">TAPI version</span></span><br/> | <span data-ttu-id="0c1dd-143">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="0c1dd-143">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="0c1dd-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c1dd-144">Header</span></span><br/>       | <dl> <span data-ttu-id="0c1dd-145"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c1dd-145"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c1dd-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c1dd-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c1dd-147">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="0c1dd-147">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="0c1dd-148">**LINECALLPARAMS**</span><span class="sxs-lookup"><span data-stu-id="0c1dd-148">**LINECALLPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[<span data-ttu-id="0c1dd-149">**lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="0c1dd-149">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[<span data-ttu-id="0c1dd-150">**lineDial**</span><span class="sxs-lookup"><span data-stu-id="0c1dd-150">**lineDial**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[<span data-ttu-id="0c1dd-151">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="0c1dd-151">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="0c1dd-152">**linePrepareAddToConference**</span><span class="sxs-lookup"><span data-stu-id="0c1dd-152">**linePrepareAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[<span data-ttu-id="0c1dd-153">**lineSetupConference**</span><span class="sxs-lookup"><span data-stu-id="0c1dd-153">**lineSetupConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[<span data-ttu-id="0c1dd-154">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="0c1dd-154">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




