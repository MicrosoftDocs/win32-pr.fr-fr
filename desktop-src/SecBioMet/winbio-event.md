---
title: Structure WINBIO_EVENT ( \_ types WINBIO. h)
description: Contient les informations d’État envoyées à la routine de rappel lorsqu’une notification d’événement est déclenchée.
ms.assetid: f46df7ff-8197-49cb-b1f8-4e7e3288e3df
keywords:
- API de Windows Biometric Framework de structure de WINBIO_EVENT
- API du pointeur de structure PWINBIO_EVENT Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_EVENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75b6a8301ea5dab7d860e5bd7fb32c69277bad63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511388"
---
# <a name="winbio_event-structure"></a><span data-ttu-id="7450f-105">\_Structure d’événement WINBIO</span><span class="sxs-lookup"><span data-stu-id="7450f-105">WINBIO\_EVENT structure</span></span>

<span data-ttu-id="7450f-106">La structure d' **\_ événement WINBIO** contient les informations d’État envoyées à la routine de rappel lorsqu’une notification d’événement est déclenchée.</span><span class="sxs-lookup"><span data-stu-id="7450f-106">The **WINBIO\_EVENT** structure contains status information sent to the callback routine when an event notice is raised.</span></span>

## <a name="syntax"></a><span data-ttu-id="7450f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7450f-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EVENT {
  WINBIO_EVENT_TYPE Type;
  union {
    struct {
      WINBIO_UNIT_ID       UnitId;
      WINBIO_REJECT_DETAIL RejectDetail;
    } Unclaimed;
    struct {
      WINBIO_UNIT_ID           UnitId;
      WINBIO_IDENTITY          Identity;
      WINBIO_BIOMETRIC_SUBTYPE SubFactor;
      WINBIO_REJECT_DETAIL     RejectDetail;
    } UnclaimedIdentify;
    struct {
      HRESULT ErrorCode;
    } Error;
  } Parameters;
} WINBIO_EVENT, *PWINBIO_EVENT;
```



## <a name="members"></a><span data-ttu-id="7450f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7450f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7450f-109">**Type**</span><span class="sxs-lookup"><span data-stu-id="7450f-109">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="7450f-110">Valeur qui spécifie le type d’avis d’événement du fournisseur de services déclenché.</span><span class="sxs-lookup"><span data-stu-id="7450f-110">A value that specifies the type of service provider event notice raised.</span></span> <span data-ttu-id="7450f-111">Le seul fournisseur actuellement pris en charge est le capteur d’empreintes digitales.</span><span class="sxs-lookup"><span data-stu-id="7450f-111">The only provider currently supported is the fingerprint sensor.</span></span> <span data-ttu-id="7450f-112">Ce capteur prend en charge les indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="7450f-112">This sensor supports the following flags.</span></span>

<dl> <dt>

<span data-ttu-id="7450f-113"><span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**WINBIO \_ ÉVÉNEMENT \_ FP non \_ réclamé** (le capteur a détecté un glissement Finger qui n’a pas été demandé par l’application ou par la fenêtre qui a actuellement le focus.</span><span class="sxs-lookup"><span data-stu-id="7450f-113"><span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**WINBIO\_EVENT\_FP\_UNCLAIMED** (The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="7450f-114">Le Windows Biometric Framework appelle la fonction de rappel pour indiquer qu’un glissement Finger s’est produit, mais n’essaie pas d’identifier l’empreinte digitale.</span><span class="sxs-lookup"><span data-stu-id="7450f-114">The Windows Biometric Framework calls into your callback function to indicate that a finger swipe has occurred but does not try to identify the fingerprint.)</span></span>
</dt> <dt>

<span data-ttu-id="7450f-115"><span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**WINBIO \_ \_ \_ \_ Identification non revendiquée du FP d’événement** (le capteur a détecté un glissement Finger qui n’a pas été demandé par l’application ou par la fenêtre qui a actuellement le focus.</span><span class="sxs-lookup"><span data-stu-id="7450f-115"><span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**WINBIO\_EVENT\_FP\_UNCLAIMED\_IDENTIFY** (The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="7450f-116">Le Windows Biometric Framework tente d’identifier l’empreinte digitale et transmet le résultat de ce processus à votre fonction de rappel.)</span><span class="sxs-lookup"><span data-stu-id="7450f-116">The Windows Biometric Framework attempts to identify the fingerprint and passes the result of that process to your callback function.)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="7450f-117">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="7450f-117">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7450f-118">**Revendication**</span><span class="sxs-lookup"><span data-stu-id="7450f-118">**Unclaimed**</span></span>
</dt> <dd>

<span data-ttu-id="7450f-119">Structure retournée pour l’exemple de capture biométrique.</span><span class="sxs-lookup"><span data-stu-id="7450f-119">Structure returned for biometric sample capture.</span></span>

<dl> <dt>

<span data-ttu-id="7450f-120">**UnitId**</span><span class="sxs-lookup"><span data-stu-id="7450f-120">**UnitId**</span></span>
</dt> <dd>

<span data-ttu-id="7450f-121">Unité biométrique qui a généré l’exemple.</span><span class="sxs-lookup"><span data-stu-id="7450f-121">The biometric unit that generated the sample.</span></span>

</dd> <dt>

<span data-ttu-id="7450f-122">**RejectDetail**</span><span class="sxs-lookup"><span data-stu-id="7450f-122">**RejectDetail**</span></span>
</dt> <dd>

<span data-ttu-id="7450f-123">Valeur **ULong** qui contient des informations supplémentaires sur l’échec de la capture d’un échantillon biométrique.</span><span class="sxs-lookup"><span data-stu-id="7450f-123">A **ULONG** value that contains additional information regarding failure to capture a biometric sample.</span></span> <span data-ttu-id="7450f-124">Si une capture a réussi, ce paramètre a la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="7450f-124">If a capture succeeded, this parameter is set to zero.</span></span> <span data-ttu-id="7450f-125">Les valeurs suivantes sont définies pour la capture d’empreinte digitale :</span><span class="sxs-lookup"><span data-stu-id="7450f-125">The following values are defined for fingerprint capture:</span></span>

-   <span data-ttu-id="7450f-126">WINBIO \_ FP \_ trop \_ élevé</span><span class="sxs-lookup"><span data-stu-id="7450f-126">WINBIO\_FP\_TOO\_HIGH</span></span>
-   <span data-ttu-id="7450f-127">WINBIO \_ FP \_ trop \_ faible</span><span class="sxs-lookup"><span data-stu-id="7450f-127">WINBIO\_FP\_TOO\_LOW</span></span>
-   <span data-ttu-id="7450f-128">WINBIO \_ FP \_ trop à \_ gauche</span><span class="sxs-lookup"><span data-stu-id="7450f-128">WINBIO\_FP\_TOO\_LEFT</span></span>
-   <span data-ttu-id="7450f-129">WINBIO \_ FP \_ trop à \_ droite</span><span class="sxs-lookup"><span data-stu-id="7450f-129">WINBIO\_FP\_TOO\_RIGHT</span></span>
-   <span data-ttu-id="7450f-130">WINBIO \_ FP \_ trop \_ rapide</span><span class="sxs-lookup"><span data-stu-id="7450f-130">WINBIO\_FP\_TOO\_FAST</span></span>
-   <span data-ttu-id="7450f-131">WINBIO \_ FP \_ trop \_ lent</span><span class="sxs-lookup"><span data-stu-id="7450f-131">WINBIO\_FP\_TOO\_SLOW</span></span>
-   <span data-ttu-id="7450f-132">\_ \_ qualité médiocre de WINBIO FP \_</span><span class="sxs-lookup"><span data-stu-id="7450f-132">WINBIO\_FP\_POOR\_QUALITY</span></span>
-   <span data-ttu-id="7450f-133">WINBIO \_ FP \_ trop \_ incliné</span><span class="sxs-lookup"><span data-stu-id="7450f-133">WINBIO\_FP\_TOO\_SKEWED</span></span>
-   <span data-ttu-id="7450f-134">WINBIO \_ FP \_ trop \_ petit</span><span class="sxs-lookup"><span data-stu-id="7450f-134">WINBIO\_FP\_TOO\_SHORT</span></span>
-   <span data-ttu-id="7450f-135">échec de la \_ fusion WINBIO FP \_ \_</span><span class="sxs-lookup"><span data-stu-id="7450f-135">WINBIO\_FP\_MERGE\_FAILURE</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7450f-136">**UnclaimedIdentify**</span><span class="sxs-lookup"><span data-stu-id="7450f-136">**UnclaimedIdentify**</span></span>
</dt> <dd>

<span data-ttu-id="7450f-137">Structure retournée pour la capture et l’identification biométriques.</span><span class="sxs-lookup"><span data-stu-id="7450f-137">Structure returned for biometric capture and identification.</span></span> <span data-ttu-id="7450f-138">L’identification détermine si un exemple peut être associé à un modèle biométrique existant.</span><span class="sxs-lookup"><span data-stu-id="7450f-138">Identification determines whether a sample can be associated with an existing biometric template.</span></span>

<dl> <dt>

<span data-ttu-id="7450f-139">**UnitId**</span><span class="sxs-lookup"><span data-stu-id="7450f-139">**UnitId**</span></span>
</dt> <dd>

<span data-ttu-id="7450f-140">Unité biométrique qui a généré l’exemple.</span><span class="sxs-lookup"><span data-stu-id="7450f-140">The biometric unit that generated the sample.</span></span>

</dd> <dt>

<span data-ttu-id="7450f-141">**Identité**</span><span class="sxs-lookup"><span data-stu-id="7450f-141">**Identity**</span></span>
</dt> <dd>

<span data-ttu-id="7450f-142">Structure [**d' \_ identité WINBIO**](winbio-identity.md) qui contient le GUID ou le SID de l’utilisateur qui fournit l’exemple biométrique.</span><span class="sxs-lookup"><span data-stu-id="7450f-142">A [**WINBIO\_IDENTITY**](winbio-identity.md) structure that contains the GUID or SID of the user providing the biometric sample.</span></span>

</dd> <dt>

<span data-ttu-id="7450f-143">**Sous-fait**</span><span class="sxs-lookup"><span data-stu-id="7450f-143">**SubFactor**</span></span>
</dt> <dd>

<span data-ttu-id="7450f-144">Valeur de sous- [**\_ \_ type biométrique WINBIO**](winbio-biometric-subtype-constants.md) qui spécifie le sous-facteur associé à un échantillon biométrique.</span><span class="sxs-lookup"><span data-stu-id="7450f-144">A [**WINBIO\_BIOMETRIC\_SUBTYPE**](winbio-biometric-subtype-constants.md) value that specifies the sub-factor associated with a biometric sample.</span></span> <span data-ttu-id="7450f-145">Le Windows Biometric Framework (WBF) prend actuellement en charge uniquement la capture d’empreintes digitales et utilise les constantes suivantes pour représenter les informations de sous-type.</span><span class="sxs-lookup"><span data-stu-id="7450f-145">The Windows Biometric Framework (WBF) currently supports only fingerprint capture and uses the following constants to represent sub-type information.</span></span>

-   <span data-ttu-id="7450f-146">WINBIO \_ ANSI \_ 381 \_ pos \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="7450f-146">WINBIO\_ANSI\_381\_POS\_UNKNOWN</span></span>
-   <span data-ttu-id="7450f-147">WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_</span><span class="sxs-lookup"><span data-stu-id="7450f-147">WINBIO\_ANSI\_381\_POS\_RH\_THUMB</span></span>
-   <span data-ttu-id="7450f-148">WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ index \_ Finger</span><span class="sxs-lookup"><span data-stu-id="7450f-148">WINBIO\_ANSI\_381\_POS\_RH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="7450f-149">WINBIO \_ ANSI \_ 381 \_ pos \_ hr \_ \_ Finger Middle</span><span class="sxs-lookup"><span data-stu-id="7450f-149">WINBIO\_ANSI\_381\_POS\_RH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="7450f-150">WINBIO de l' \_ \_ \_ \_ anneau RH \_ du PDV ANSI 381 \_</span><span class="sxs-lookup"><span data-stu-id="7450f-150">WINBIO\_ANSI\_381\_POS\_RH\_RING\_FINGER</span></span>
-   <span data-ttu-id="7450f-151">WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ petit \_ Finger</span><span class="sxs-lookup"><span data-stu-id="7450f-151">WINBIO\_ANSI\_381\_POS\_RH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="7450f-152">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_</span><span class="sxs-lookup"><span data-stu-id="7450f-152">WINBIO\_ANSI\_381\_POS\_LH\_THUMB</span></span>
-   <span data-ttu-id="7450f-153">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ index \_ Finger</span><span class="sxs-lookup"><span data-stu-id="7450f-153">WINBIO\_ANSI\_381\_POS\_LH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="7450f-154">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ - \_ Finger</span><span class="sxs-lookup"><span data-stu-id="7450f-154">WINBIO\_ANSI\_381\_POS\_LH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="7450f-155">\_ \_ Doigt Ring WINBIO ANSI 381 \_ pos \_ LH \_ \_</span><span class="sxs-lookup"><span data-stu-id="7450f-155">WINBIO\_ANSI\_381\_POS\_LH\_RING\_FINGER</span></span>
-   <span data-ttu-id="7450f-156">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ petit \_ doigt</span><span class="sxs-lookup"><span data-stu-id="7450f-156">WINBIO\_ANSI\_381\_POS\_LH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="7450f-157">WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ quatre \_ doigts</span><span class="sxs-lookup"><span data-stu-id="7450f-157">WINBIO\_ANSI\_381\_POS\_RH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="7450f-158">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ quatre \_ doigts</span><span class="sxs-lookup"><span data-stu-id="7450f-158">WINBIO\_ANSI\_381\_POS\_LH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="7450f-159">WINBIO \_ ANSI \_ 381 \_ pos \_ deux \_ pouces</span><span class="sxs-lookup"><span data-stu-id="7450f-159">WINBIO\_ANSI\_381\_POS\_TWO\_THUMBS</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="7450f-160">N’essayez pas de valider la valeur fournie pour la valeur de sous- *fait* .</span><span class="sxs-lookup"><span data-stu-id="7450f-160">Do not attempt to validate the value supplied for the *SubFactor* value.</span></span> <span data-ttu-id="7450f-161">Le service de biométrie Windows validera la valeur fournie avant de la passer à votre implémentation.</span><span class="sxs-lookup"><span data-stu-id="7450f-161">The Windows Biometrics Service will validate the supplied value before passing it through to your implementation.</span></span> <span data-ttu-id="7450f-162">Si la valeur est **WINBIO \_ sous-type \_ aucune \_ information** ou **WINBIO sous- \_ type \_ any**, validez le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="7450f-162">If the value is **WINBIO\_SUBTYPE\_NO\_INFORMATION** or **WINBIO\_SUBTYPE\_ANY**, then validate where appropriate.</span></span>

 

</dd> <dt>

<span data-ttu-id="7450f-163">**RejectDetail**</span><span class="sxs-lookup"><span data-stu-id="7450f-163">**RejectDetail**</span></span>
</dt> <dd>

<span data-ttu-id="7450f-164">Valeur **ULong** qui contient des informations supplémentaires sur l’échec de capture d’un échantillon biométrique.</span><span class="sxs-lookup"><span data-stu-id="7450f-164">A **ULONG** value that contains additional information about the failure to capture a biometric sample.</span></span> <span data-ttu-id="7450f-165">Si la capture a réussi, ce paramètre a la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="7450f-165">If the capture succeeded, this parameter is set to zero.</span></span> <span data-ttu-id="7450f-166">Les valeurs suivantes sont définies pour la capture d’empreinte digitale :</span><span class="sxs-lookup"><span data-stu-id="7450f-166">The following values are defined for fingerprint capture:</span></span>

-   <span data-ttu-id="7450f-167">WINBIO \_ FP \_ trop \_ élevé</span><span class="sxs-lookup"><span data-stu-id="7450f-167">WINBIO\_FP\_TOO\_HIGH</span></span>
-   <span data-ttu-id="7450f-168">WINBIO \_ FP \_ trop \_ faible</span><span class="sxs-lookup"><span data-stu-id="7450f-168">WINBIO\_FP\_TOO\_LOW</span></span>
-   <span data-ttu-id="7450f-169">WINBIO \_ FP \_ trop à \_ gauche</span><span class="sxs-lookup"><span data-stu-id="7450f-169">WINBIO\_FP\_TOO\_LEFT</span></span>
-   <span data-ttu-id="7450f-170">WINBIO \_ FP \_ trop à \_ droite</span><span class="sxs-lookup"><span data-stu-id="7450f-170">WINBIO\_FP\_TOO\_RIGHT</span></span>
-   <span data-ttu-id="7450f-171">WINBIO \_ FP \_ trop \_ rapide</span><span class="sxs-lookup"><span data-stu-id="7450f-171">WINBIO\_FP\_TOO\_FAST</span></span>
-   <span data-ttu-id="7450f-172">WINBIO \_ FP \_ trop \_ lent</span><span class="sxs-lookup"><span data-stu-id="7450f-172">WINBIO\_FP\_TOO\_SLOW</span></span>
-   <span data-ttu-id="7450f-173">\_ \_ qualité médiocre de WINBIO FP \_</span><span class="sxs-lookup"><span data-stu-id="7450f-173">WINBIO\_FP\_POOR\_QUALITY</span></span>
-   <span data-ttu-id="7450f-174">WINBIO \_ FP \_ trop \_ incliné</span><span class="sxs-lookup"><span data-stu-id="7450f-174">WINBIO\_FP\_TOO\_SKEWED</span></span>
-   <span data-ttu-id="7450f-175">WINBIO \_ FP \_ trop \_ petit</span><span class="sxs-lookup"><span data-stu-id="7450f-175">WINBIO\_FP\_TOO\_SHORT</span></span>
-   <span data-ttu-id="7450f-176">échec de la \_ fusion WINBIO FP \_ \_</span><span class="sxs-lookup"><span data-stu-id="7450f-176">WINBIO\_FP\_MERGE\_FAILURE</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7450f-177">**Error**</span><span class="sxs-lookup"><span data-stu-id="7450f-177">**Error**</span></span>
</dt> <dd>

<span data-ttu-id="7450f-178">Structure qui identifie la réussite ou l’échec de l’opération surveillée.</span><span class="sxs-lookup"><span data-stu-id="7450f-178">Structure that identifies the success or failure of the operation being monitored.</span></span>

<dl> <dt>

<span data-ttu-id="7450f-179">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7450f-179">**ErrorCode**</span></span>
</dt> <dd>

<span data-ttu-id="7450f-180">Valeur **HRESULT** qui contient \_ un ou un code d’erreur qui résulte des calculs effectués par le Windows Biometric Framework.</span><span class="sxs-lookup"><span data-stu-id="7450f-180">**HRESULT** value that contains S\_OK or an error code that resulted from computations performed by the Windows Biometric Framework.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7450f-181">Notes</span><span class="sxs-lookup"><span data-stu-id="7450f-181">Remarks</span></span>

<span data-ttu-id="7450f-182">Appelez la fonction [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) pour inscrire une routine de rappel afin de recevoir des notifications d’événements de la Windows Biometric Framework.</span><span class="sxs-lookup"><span data-stu-id="7450f-182">Call the [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) function to register a callback routine to receive event notifications from the Windows Biometric Framework.</span></span> <span data-ttu-id="7450f-183">Le rappel est une fonction personnalisée que vous devez définir pour votre application.</span><span class="sxs-lookup"><span data-stu-id="7450f-183">The callback is a custom function that you must define for your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="7450f-184">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7450f-184">Requirements</span></span>



| <span data-ttu-id="7450f-185">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7450f-185">Requirement</span></span> | <span data-ttu-id="7450f-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="7450f-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7450f-187">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7450f-187">Minimum supported client</span></span><br/> | <span data-ttu-id="7450f-188">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7450f-188">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="7450f-189">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7450f-189">Minimum supported server</span></span><br/> | <span data-ttu-id="7450f-190">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7450f-190">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7450f-191">En-tête</span><span class="sxs-lookup"><span data-stu-id="7450f-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="7450f-192"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7450f-192"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7450f-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7450f-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7450f-194">Structures d’application cliente</span><span class="sxs-lookup"><span data-stu-id="7450f-194">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="7450f-195">**WinBioRegisterEventMonitor**</span><span class="sxs-lookup"><span data-stu-id="7450f-195">**WinBioRegisterEventMonitor**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor)
</dt> </dl>

 

 





