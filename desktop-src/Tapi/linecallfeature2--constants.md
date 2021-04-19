---
description: Les \_ constantes LINECALLFEATURE2 répertorient les fonctionnalités supplémentaires disponibles pour la Conférence, le transfert et les appels de parking.
ms.assetid: 67a3b587-dd5b-4ccf-ab69-2137604706b8
title: Constantes LINECALLFEATURE2_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 977e71f722fba34da6b2ecbd6a3e914c34a0aae5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541103"
---
# <a name="linecallfeature2_-constants"></a><span data-ttu-id="81d5c-103">\_Constantes LINECALLFEATURE2</span><span class="sxs-lookup"><span data-stu-id="81d5c-103">LINECALLFEATURE2\_ Constants</span></span>

<span data-ttu-id="81d5c-104">Les constantes **LINECALLFEATURE2 \_** répertorient les fonctionnalités supplémentaires disponibles pour la Conférence, le transfert et les appels de parking.</span><span class="sxs-lookup"><span data-stu-id="81d5c-104">The **LINECALLFEATURE2\_** constants list the supplemental features available for conferencing, transferring, and parking calls.</span></span>

<dl> <dt>

<span data-ttu-id="81d5c-105"><span id="LINECALLFEATURE2_COMPLCALLBACK"></span><span id="linecallfeature2_complcallback"></span>**LINECALLFEATURE2 \_ COMPLCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="81d5c-105"><span id="LINECALLFEATURE2_COMPLCALLBACK"></span><span id="linecallfeature2_complcallback"></span>**LINECALLFEATURE2\_COMPLCALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="81d5c-106">Si ce bit est activé, la fonctionnalité de « rappel » peut être appelée à l’aide de l' \_ option de rappel LINECOMPLMODE avec [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span><span class="sxs-lookup"><span data-stu-id="81d5c-106">If this bit is on, the "callback" feature can be invoked by using the LINECOMPLMODE\_CALLBACK option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="81d5c-107">Le \_ bit LINECALLFEATURE COMPLETECALL est également activé dans le membre **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="81d5c-107">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81d5c-108"><span id="LINECALLFEATURE2_COMPLCAMPON"></span><span id="linecallfeature2_complcampon"></span>**LINECALLFEATURE2 \_ COMPLCAMPON**</span><span class="sxs-lookup"><span data-stu-id="81d5c-108"><span id="LINECALLFEATURE2_COMPLCAMPON"></span><span id="linecallfeature2_complcampon"></span>**LINECALLFEATURE2\_COMPLCAMPON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="81d5c-109">Si ce bit est activé, la fonctionnalité « camp on » peut être appelée à l’aide de l' \_ option LINECOMPLMODE CAMPON avec [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span><span class="sxs-lookup"><span data-stu-id="81d5c-109">If this bit is on, the "camp on" feature can be invoked by using the LINECOMPLMODE\_CAMPON option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="81d5c-110">Le \_ bit LINECALLFEATURE COMPLETECALL est également activé dans le membre **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="81d5c-110">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81d5c-111"><span id="LINECALLFEATURE2_COMPLINTRUDE"></span><span id="linecallfeature2_complintrude"></span>**LINECALLFEATURE2 \_ COMPLINTRUDE**</span><span class="sxs-lookup"><span data-stu-id="81d5c-111"><span id="LINECALLFEATURE2_COMPLINTRUDE"></span><span id="linecallfeature2_complintrude"></span>**LINECALLFEATURE2\_COMPLINTRUDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="81d5c-112">Si ce bit est activé, la fonctionnalité « intrus » peut être appelée à l’aide de l' \_ option LINECOMPLMODE intrusion avec [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span><span class="sxs-lookup"><span data-stu-id="81d5c-112">If this bit is on, the "intrude" feature can be invoked by using the LINECOMPLMODE\_INTRUDE option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="81d5c-113">Le \_ bit LINECALLFEATURE COMPLETECALL est également activé dans le membre **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="81d5c-113">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81d5c-114"><span id="LINECALLFEATURE2_COMPLMESSAGE"></span><span id="linecallfeature2_complmessage"></span>**LINECALLFEATURE2 \_ COMPLMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="81d5c-114"><span id="LINECALLFEATURE2_COMPLMESSAGE"></span><span id="linecallfeature2_complmessage"></span>**LINECALLFEATURE2\_COMPLMESSAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="81d5c-115">Si ce bit est activé, la fonctionnalité « conserver le message » peut être appelée à l’aide de l' \_ option de message LINECOMPLMODE avec [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span><span class="sxs-lookup"><span data-stu-id="81d5c-115">If this bit is on, the "leave message" feature can be invoked by using the LINECOMPLMODE\_MESSAGE option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="81d5c-116">Le \_ bit LINECALLFEATURE COMPLETECALL est également activé dans le membre **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="81d5c-116">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81d5c-117"><span id="LINECALLFEATURE2_NOHOLDCONFERENCE"></span><span id="linecallfeature2_noholdconference"></span>**LINECALLFEATURE2 \_ NOHOLDCONFERENCE**</span><span class="sxs-lookup"><span data-stu-id="81d5c-117"><span id="LINECALLFEATURE2_NOHOLDCONFERENCE"></span><span id="linecallfeature2_noholdconference"></span>**LINECALLFEATURE2\_NOHOLDCONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="81d5c-118">Si ce bit est activé, une « aucune conférence débloquée » peut être créée à l’aide de l' \_ option LINECALLPARAMFLAGS NOHOLDCONFERENCE avec [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference).</span><span class="sxs-lookup"><span data-stu-id="81d5c-118">If this bit is on, a "no hold conference" can be created by using the LINECALLPARAMFLAGS\_NOHOLDCONFERENCE option with [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference).</span></span> <span data-ttu-id="81d5c-119">Le \_ bit LINECALLFEATURE SETUPCONF est également activé dans le membre **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="81d5c-119">The LINECALLFEATURE\_SETUPCONF bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81d5c-120"><span id="LINECALLFEATURE2_ONESTEPTRANSFER"></span><span id="linecallfeature2_onesteptransfer"></span>**LINECALLFEATURE2 \_ ONESTEPTRANSFER**</span><span class="sxs-lookup"><span data-stu-id="81d5c-120"><span id="LINECALLFEATURE2_ONESTEPTRANSFER"></span><span id="linecallfeature2_onesteptransfer"></span>**LINECALLFEATURE2\_ONESTEPTRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="81d5c-121">Si ce bit est activé, vous pouvez créer un transfert en une étape à l’aide de l' \_ option LINECALLPARAMFLAGS ONESTEPTRANSFER avec [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer).</span><span class="sxs-lookup"><span data-stu-id="81d5c-121">If this bit is on, "one step transfer" can be created by using the LINECALLPARAMFLAGS\_ONESTEPTRANSFER option with [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer).</span></span> <span data-ttu-id="81d5c-122">Le \_ bit LINECALLFEATURE SETUPTRANSFER est également activé dans le membre **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="81d5c-122">The LINECALLFEATURE\_SETUPTRANSFER bit will also be on in the **dwCallFeatures** member.</span></span>

> [!Note]  
> <span data-ttu-id="81d5c-123">Si aucun des bits « compl ( » n’est spécifié dans le membre **dwCallFeatures2** dans [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) mais \_ que LINECALLFEATURE COMPLETECALL est spécifié, il est possible que l’un d’eux fonctionne, alors que le fournisseur de services n’a pas spécifié quoi.</span><span class="sxs-lookup"><span data-stu-id="81d5c-123">If none of the "COMPL" bits is specified in the **dwCallFeatures2** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) but LINECALLFEATURE\_COMPLETECALL is specified, then it is possible that any of them will work, but the service provider has not specified which.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="81d5c-124"><span id="LINECALLFEATURE2_TRANSFERCONF"></span><span id="linecallfeature2_transferconf"></span>**LINECALLFEATURE2 \_ TRANSFERCONF**</span><span class="sxs-lookup"><span data-stu-id="81d5c-124"><span id="LINECALLFEATURE2_TRANSFERCONF"></span><span id="linecallfeature2_transferconf"></span>**LINECALLFEATURE2\_TRANSFERCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="81d5c-125">Si ce bit est activé, la fonction [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) peut être utilisée pour résoudre le transfert comme une conférence triple.</span><span class="sxs-lookup"><span data-stu-id="81d5c-125">If this bit is on, the [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) function can be used to resolve the transfer as a three-way conference.</span></span> <span data-ttu-id="81d5c-126">Le \_ bit LINECALLFEATURE COMPLETETRANSF est également activé dans le membre **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="81d5c-126">The LINECALLFEATURE\_COMPLETETRANSF bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81d5c-127"><span id="LINECALLFEATURE2_TRANSFERNORM"></span><span id="linecallfeature2_transfernorm"></span>**LINECALLFEATURE2 \_ TRANSFERNORM**</span><span class="sxs-lookup"><span data-stu-id="81d5c-127"><span id="LINECALLFEATURE2_TRANSFERNORM"></span><span id="linecallfeature2_transfernorm"></span>**LINECALLFEATURE2\_TRANSFERNORM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="81d5c-128">Si ce bit est activé, la fonction [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) peut être utilisée pour résoudre le transfert comme un transfert normal.</span><span class="sxs-lookup"><span data-stu-id="81d5c-128">If this bit is on, the [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) function can be used to resolve the transfer as a normal transfer.</span></span> <span data-ttu-id="81d5c-129">Le \_ bit LINECALLFEATURE COMPLETETRANSF est également activé dans le membre **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="81d5c-129">The LINECALLFEATURE\_COMPLETETRANSF bit will also be on in the **dwCallFeatures** member.</span></span>

> [!Note]  
> <span data-ttu-id="81d5c-130">Si ni TRANSFERNORM ni TRANSFERCONF n’est spécifié dans le membre **dwCallFeatures2** dans [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) mais que LINECALLFEATURE \_ COMPLETETRANSF est spécifié, il est possible que soit fonctionne, mais que le fournisseur de services n’ait pas spécifié ce qui a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="81d5c-130">If neither TRANSFERNORM nor TRANSFERCONF is specified in the **dwCallFeatures2** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) but LINECALLFEATURE\_COMPLETETRANSF is specified, then it is possible that either will work, but the service provider has not specified which.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="81d5c-131"><span id="LINECALLFEATURE2_PARKDIRECT"></span><span id="linecallfeature2_parkdirect"></span>**LINECALLFEATURE2 \_ PARKDIRECT**</span><span class="sxs-lookup"><span data-stu-id="81d5c-131"><span id="LINECALLFEATURE2_PARKDIRECT"></span><span id="linecallfeature2_parkdirect"></span>**LINECALLFEATURE2\_PARKDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="81d5c-132">Si ce bit est activé, la fonctionnalité de « stationnement dirigé » peut être appelée à l’aide de l' \_ option LINEPARKMODE dirigée avec [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark).</span><span class="sxs-lookup"><span data-stu-id="81d5c-132">If this bit is on, the "directed park" feature can be invoked by using the LINEPARKMODE\_DIRECTED option with [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark).</span></span> <span data-ttu-id="81d5c-133">Le \_ bit de parc LINECALLFEATURE sera également activé dans le membre **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="81d5c-133">The LINECALLFEATURE\_PARK bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81d5c-134"><span id="LINECALLFEATURE2_PARKNONDIRECT"></span><span id="linecallfeature2_parknondirect"></span>**LINECALLFEATURE2 \_ PARKNONDIRECT**</span><span class="sxs-lookup"><span data-stu-id="81d5c-134"><span id="LINECALLFEATURE2_PARKNONDIRECT"></span><span id="linecallfeature2_parknondirect"></span>**LINECALLFEATURE2\_PARKNONDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="81d5c-135">Si ce bit est activé, la fonctionnalité « parc non dirigé » peut être appelée à l’aide de l' \_ option non directe LINEPARKMODE avec [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark).</span><span class="sxs-lookup"><span data-stu-id="81d5c-135">If this bit is on, the "non-directed park" feature can be invoked by using the LINEPARKMODE\_NONDIRECTED option with [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark).</span></span> <span data-ttu-id="81d5c-136">Le \_ bit de parc LINECALLFEATURE sera également activé dans le membre **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="81d5c-136">The LINECALLFEATURE\_PARK bit will also be on in the **dwCallFeatures** member.</span></span>

> [!Note]  
> <span data-ttu-id="81d5c-137">Si ni PARKDIRECT ni PARKNONDIRECT n’est spécifié dans le membre **dwCallFeatures2** dans [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) mais \_ que LINECALLFEATURE Park est spécifié, il est possible que soit fonctionne, mais que le fournisseur de services n’ait pas spécifié ce qui a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="81d5c-137">If neither PARKDIRECT nor PARKNONDIRECT is specified in the **dwCallFeatures2** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) but LINECALLFEATURE\_PARK is specified, then it is possible that either will work, but the service provider has not specified which.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81d5c-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81d5c-138">Requirements</span></span>



| <span data-ttu-id="81d5c-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81d5c-139">Requirement</span></span> | <span data-ttu-id="81d5c-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="81d5c-140">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="81d5c-141">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="81d5c-141">TAPI version</span></span><br/> | <span data-ttu-id="81d5c-142">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="81d5c-142">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="81d5c-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="81d5c-143">Header</span></span><br/>       | <dl> <span data-ttu-id="81d5c-144"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="81d5c-144"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81d5c-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81d5c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81d5c-146">**LINECALLSTATUS**</span><span class="sxs-lookup"><span data-stu-id="81d5c-146">**LINECALLSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[<span data-ttu-id="81d5c-147">**lineCompleteCall**</span><span class="sxs-lookup"><span data-stu-id="81d5c-147">**lineCompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[<span data-ttu-id="81d5c-148">**lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="81d5c-148">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[<span data-ttu-id="81d5c-149">**linePark**</span><span class="sxs-lookup"><span data-stu-id="81d5c-149">**linePark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepark)
</dt> <dt>

[<span data-ttu-id="81d5c-150">**lineSetupConference**</span><span class="sxs-lookup"><span data-stu-id="81d5c-150">**lineSetupConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[<span data-ttu-id="81d5c-151">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="81d5c-151">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




