---
description: Construit une commande APDU (Application Protocol Data Unit) qui met à jour l’état de la sécurité de manière conditionnelle, en vérifiant l’identité de l’ordinateur lorsque la carte à puce ne l’approuve pas.
ms.assetid: 6db063d5-48a7-4c8b-ae84-cbcf34edc79d
title: 'ISCardISO7816 :: ExternalAuthenticate, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ExternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1c8d56b6f2210974bd86dbecea06f16b68548659
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393551"
---
# <a name="iscardiso7816externalauthenticate-method"></a><span data-ttu-id="de21d-103">ISCardISO7816 :: ExternalAuthenticate, méthode</span><span class="sxs-lookup"><span data-stu-id="de21d-103">ISCardISO7816::ExternalAuthenticate method</span></span>

<span data-ttu-id="de21d-104">\[La méthode **ExternalAuthenticate** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="de21d-104">\[The **ExternalAuthenticate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="de21d-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="de21d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="de21d-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="de21d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="de21d-107">La méthode **ExternalAuthenticate** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui met à jour l’état de la sécurité de manière conditionnelle, en vérifiant l’identité de l’ordinateur lorsque la [*carte à puce*](../secgloss/s-gly.md) ne l’approuve pas.</span><span class="sxs-lookup"><span data-stu-id="de21d-107">The **ExternalAuthenticate** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that conditionally updates security status, verifying the identity of the computer when the [*smart card*](../secgloss/s-gly.md) does not trust it.</span></span>

<span data-ttu-id="de21d-108">La commande utilise le résultat (oui ou non) du calcul par la carte (en fonction d’une demande précédemment émise par la carte, par exemple par la \_ commande ins obtenir un \_ Challenge), d’une clé (éventuellement secrète) stockée dans la carte et des données d’authentification transmises par l’appareil de l’interface.</span><span class="sxs-lookup"><span data-stu-id="de21d-108">The command uses the result (yes or no) of the computation by the card (based on a challenge previously issued by the card, for example, by the INS\_GET\_CHALLENGE command), a key (possibly secret) stored in the card, and authentication data transmitted by the interface device.</span></span>

## <a name="syntax"></a><span data-ttu-id="de21d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de21d-109">Syntax</span></span>


```C++
HRESULT ExternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="de21d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de21d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de21d-111">*byAlgorithmRef* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="de21d-111">*byAlgorithmRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de21d-112">Référence de l’algorithme dans la carte.</span><span class="sxs-lookup"><span data-stu-id="de21d-112">The reference of the algorithm in the card.</span></span>

<span data-ttu-id="de21d-113">Si cette valeur est égale à zéro, cela indique qu’aucune information n’est fournie.</span><span class="sxs-lookup"><span data-stu-id="de21d-113">If this value is zero, this indicates that no information is given.</span></span> <span data-ttu-id="de21d-114">La référence de l’algorithme est connue avant l’émission de la commande ou est fournie dans le champ de données.</span><span class="sxs-lookup"><span data-stu-id="de21d-114">The reference of the algorithm is known either before issuing the command or is provided in the data field.</span></span>

</dd> <dt>

<span data-ttu-id="de21d-115">*bySecretRef* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="de21d-115">*bySecretRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de21d-116">Référence du secret.</span><span class="sxs-lookup"><span data-stu-id="de21d-116">The reference of the secret.</span></span>



| <span data-ttu-id="de21d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="de21d-117">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="de21d-118">Signification</span><span class="sxs-lookup"><span data-stu-id="de21d-118">Meaning</span></span>                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <span data-ttu-id="de21d-119"><dt>**Aucune information**</dt></span><span class="sxs-lookup"><span data-stu-id="de21d-119"><dt>**No Info**</dt></span></span> </dl>                     | <span data-ttu-id="de21d-120">Position du bit : 00000000</span><span class="sxs-lookup"><span data-stu-id="de21d-120">Bit position: 00000000</span></span><br/> <span data-ttu-id="de21d-121">Aucune information n’est fournie.</span><span class="sxs-lookup"><span data-stu-id="de21d-121">No information is given.</span></span> <span data-ttu-id="de21d-122">La référence du secret est connue avant l’émission de la commande ou est fournie dans le champ de données.</span><span class="sxs-lookup"><span data-stu-id="de21d-122">The reference of the secret is known either before issuing the command or is provided in the data field.</span></span><br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <span data-ttu-id="de21d-123"><dt>**Référence globale**</dt></span><span class="sxs-lookup"><span data-stu-id="de21d-123"><dt>**Global ref**</dt></span></span> </dl>         | <span data-ttu-id="de21d-124">Position du bit : 0-------</span><span class="sxs-lookup"><span data-stu-id="de21d-124">Bit position: 0-------</span></span><br/> <span data-ttu-id="de21d-125">Données de référence globales (une clé spécifique à MF).</span><span class="sxs-lookup"><span data-stu-id="de21d-125">Global reference data (an MF specific key).</span></span><br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <span data-ttu-id="de21d-126"><dt>**Réf. spécifique**</dt></span><span class="sxs-lookup"><span data-stu-id="de21d-126"><dt>**Specific ref**</dt></span></span> </dl> | <span data-ttu-id="de21d-127">Position du bit : 1-------</span><span class="sxs-lookup"><span data-stu-id="de21d-127">Bit position: 1-------</span></span><br/> <span data-ttu-id="de21d-128">Données de référence spécifiques (clé spécifique à DF).</span><span class="sxs-lookup"><span data-stu-id="de21d-128">Specific reference data (a DF specific key).</span></span><br/>                                                                                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="de21d-129"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="de21d-129"><dt>**RFU**</dt></span></span> </dl>                                                           | <span data-ttu-id="de21d-130">Position du bit :-XX-----</span><span class="sxs-lookup"><span data-stu-id="de21d-130">Bit position: -xx-----</span></span><br/> <span data-ttu-id="de21d-131">00 (les autres valeurs sont RFU).</span><span class="sxs-lookup"><span data-stu-id="de21d-131">00 (other values are RFU).</span></span><br/>                                                                                                        |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <span data-ttu-id="de21d-132"><dt>**Secret**</dt></span><span class="sxs-lookup"><span data-stu-id="de21d-132"><dt>**Secret**</dt></span></span> </dl>                         | <span data-ttu-id="de21d-133">Position du bit :---xxxxx</span><span class="sxs-lookup"><span data-stu-id="de21d-133">Bit position: ---xxxxx</span></span><br/> <span data-ttu-id="de21d-134">Numéro du secret.</span><span class="sxs-lookup"><span data-stu-id="de21d-134">Number of the secret.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="de21d-135">*pChallenge* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="de21d-135">*pChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de21d-136">Pointeur vers les données liées à l’authentification.</span><span class="sxs-lookup"><span data-stu-id="de21d-136">A pointer to the authentication-related data.</span></span> <span data-ttu-id="de21d-137">Ce paramètre peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="de21d-137">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="de21d-138">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="de21d-138">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="de21d-139">En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.</span><span class="sxs-lookup"><span data-stu-id="de21d-139">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="de21d-140">Au retour, elle est remplie avec la commande APDU construite par cette opération.</span><span class="sxs-lookup"><span data-stu-id="de21d-140">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="de21d-141">Si *ppCmd* a été défini **sur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé et retourné en interne à l’aide du pointeur *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="de21d-141">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de21d-142">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="de21d-142">Return value</span></span>

<span data-ttu-id="de21d-143">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="de21d-143">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="de21d-144">Code de retour</span><span class="sxs-lookup"><span data-stu-id="de21d-144">Return code</span></span>                                                                                   | <span data-ttu-id="de21d-145">Description</span><span class="sxs-lookup"><span data-stu-id="de21d-145">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="de21d-146"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="de21d-146"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="de21d-147">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="de21d-147">The operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="de21d-148"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="de21d-148"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="de21d-149">Un paramètre non valide a été passé.</span><span class="sxs-lookup"><span data-stu-id="de21d-149">A parameter that is not valid was passed.</span></span><br/> |
| <dl> <span data-ttu-id="de21d-150"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="de21d-150"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="de21d-151">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="de21d-151">A bad pointer was passed in.</span></span><br/>              |
| <dl> <span data-ttu-id="de21d-152"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="de21d-152"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="de21d-153">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="de21d-153">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="de21d-154">Notes</span><span class="sxs-lookup"><span data-stu-id="de21d-154">Remarks</span></span>

<span data-ttu-id="de21d-155">Pour que la commande encapsulée réussisse, la dernière demande d’obtention de la carte doit être valide.</span><span class="sxs-lookup"><span data-stu-id="de21d-155">For the encapsulated command to be successful, the last challenge obtained from the card must be valid.</span></span>

<span data-ttu-id="de21d-156">Les comparaisons ayant échoué peuvent être enregistrées dans la carte (par exemple, pour limiter le nombre de tentatives supplémentaires d’utilisation des données de référence).</span><span class="sxs-lookup"><span data-stu-id="de21d-156">Unsuccessful comparisons may be recorded in the card (for example, to limit the number of further attempts of the use of the reference data).</span></span>

<span data-ttu-id="de21d-157">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="de21d-157">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="de21d-158">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="de21d-158">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="de21d-159">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="de21d-159">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="de21d-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de21d-160">Requirements</span></span>



| <span data-ttu-id="de21d-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de21d-161">Requirement</span></span> | <span data-ttu-id="de21d-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="de21d-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de21d-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de21d-163">Minimum supported client</span></span><br/> | <span data-ttu-id="de21d-164">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de21d-164">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="de21d-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de21d-165">Minimum supported server</span></span><br/> | <span data-ttu-id="de21d-166">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de21d-166">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="de21d-167">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="de21d-167">End of client support</span></span><br/>    | <span data-ttu-id="de21d-168">Windows XP</span><span class="sxs-lookup"><span data-stu-id="de21d-168">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="de21d-169">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="de21d-169">End of server support</span></span><br/>    | <span data-ttu-id="de21d-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="de21d-170">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="de21d-171">En-tête</span><span class="sxs-lookup"><span data-stu-id="de21d-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="de21d-172"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="de21d-172"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="de21d-173">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="de21d-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="de21d-174"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="de21d-174"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="de21d-175">DLL</span><span class="sxs-lookup"><span data-stu-id="de21d-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de21d-176"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de21d-176"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="de21d-177">IID</span><span class="sxs-lookup"><span data-stu-id="de21d-177">IID</span></span><br/>                      | <span data-ttu-id="de21d-178">IID \_ ISCardISO7816 est défini en tant que 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="de21d-178">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="de21d-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de21d-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de21d-180">**InternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="de21d-180">**InternalAuthenticate**</span></span>](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="de21d-181">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="de21d-181">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
