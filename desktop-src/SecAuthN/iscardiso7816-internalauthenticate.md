---
description: Construit une commande APDU (Application Protocol Data Unit) qui lance le calcul des données d’authentification par la carte à l’aide des données de stimulation envoyées par l’appareil d’interface et d’une clé secrète pertinente (par exemple, une clé) stockée dans la carte.
ms.assetid: cb0b2535-6e5b-4fb2-b540-cd037259baab
title: 'ISCardISO7816 :: InternalAuthenticate, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.InternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1e30dbb06373907c5cea07e45d4f7a390b773349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034319"
---
# <a name="iscardiso7816internalauthenticate-method"></a><span data-ttu-id="e1ae7-103">ISCardISO7816 :: InternalAuthenticate, méthode</span><span class="sxs-lookup"><span data-stu-id="e1ae7-103">ISCardISO7816::InternalAuthenticate method</span></span>

<span data-ttu-id="e1ae7-104">\[La méthode **InternalAuthenticate** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-104">\[The **InternalAuthenticate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e1ae7-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e1ae7-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="e1ae7-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="e1ae7-107">La méthode **InternalAuthenticate** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui lance le calcul des données d’authentification par la carte à l’aide des données de stimulation envoyées par l’appareil d’interface et d’une clé secrète pertinente (par exemple, une clé) stockée dans la carte.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-107">The **InternalAuthenticate** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that initiates the computation of the authentication data by the card using the challenge data sent from the interface device and a relevant secret (for example, a key) stored in the card.</span></span>

<span data-ttu-id="e1ae7-108">Lorsque le secret pertinent est attaché à MF, la commande peut être utilisée pour authentifier la carte dans son ensemble.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-108">When the relevant secret is attached to the MF, the command may be used to authenticate the card as a whole.</span></span>

<span data-ttu-id="e1ae7-109">Lorsque le secret pertinent est attaché à un autre DF, la commande peut être utilisée pour authentifier ce DF.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-109">When the relevant secret is attached to another DF, the command may be used to authenticate that DF.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1ae7-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1ae7-110">Syntax</span></span>


```C++
HRESULT InternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in]      LONG         lReplyBytes,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="e1ae7-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1ae7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1ae7-112">*byAlgorithmRef* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1ae7-112">*byAlgorithmRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1ae7-113">Référence de l’algorithme dans la carte.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-113">Reference of the algorithm in the card.</span></span>

<span data-ttu-id="e1ae7-114">Si cette valeur est égale à zéro, cela indique qu’aucune information n’est fournie.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-114">If this value is zero, this indicates that no information is given.</span></span> <span data-ttu-id="e1ae7-115">La référence de l’algorithme est connue avant l’émission de la commande ou est fournie dans le champ de données.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-115">The reference of the algorithm is known either before issuing the command or is provided in the data field.</span></span>

</dd> <dt>

<span data-ttu-id="e1ae7-116">*bySecretRef* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1ae7-116">*bySecretRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1ae7-117">Référence du secret.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-117">Reference of the secret.</span></span>



| <span data-ttu-id="e1ae7-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1ae7-118">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="e1ae7-119">Signification</span><span class="sxs-lookup"><span data-stu-id="e1ae7-119">Meaning</span></span>                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <span data-ttu-id="e1ae7-120"><dt>**Aucune information**</dt></span><span class="sxs-lookup"><span data-stu-id="e1ae7-120"><dt>**No Info**</dt></span></span> </dl>                     | <span data-ttu-id="e1ae7-121">Position du bit : 00000000</span><span class="sxs-lookup"><span data-stu-id="e1ae7-121">Bit position: 00000000</span></span> <br/> <span data-ttu-id="e1ae7-122">Aucune information n’est fournie.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-122">No information is given.</span></span> <span data-ttu-id="e1ae7-123">La référence du secret est connue avant l’émission de la commande ou est fournie dans le champ de données.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-123">The reference of the secret is known either before issuing the command or is provided in the data field.</span></span><br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <span data-ttu-id="e1ae7-124"><dt>**Référence globale**</dt></span><span class="sxs-lookup"><span data-stu-id="e1ae7-124"><dt>**Global ref**</dt></span></span> </dl>         | <span data-ttu-id="e1ae7-125">Position du bit : 0-------</span><span class="sxs-lookup"><span data-stu-id="e1ae7-125">Bit position: 0-------</span></span> <br/> <span data-ttu-id="e1ae7-126">Données de référence globales (une clé spécifique à MF).</span><span class="sxs-lookup"><span data-stu-id="e1ae7-126">Global reference data (an MF specific key).</span></span><br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <span data-ttu-id="e1ae7-127"><dt>**Réf. spécifique**</dt></span><span class="sxs-lookup"><span data-stu-id="e1ae7-127"><dt>**Specific ref**</dt></span></span> </dl> | <span data-ttu-id="e1ae7-128">Position du bit : 1-------</span><span class="sxs-lookup"><span data-stu-id="e1ae7-128">Bit position: 1-------</span></span><br/> <span data-ttu-id="e1ae7-129">Données de référence spécifiques (clé spécifique à DF).</span><span class="sxs-lookup"><span data-stu-id="e1ae7-129">Specific reference data (a DF specific key).</span></span><br/>                                                                                       |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="e1ae7-130"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="e1ae7-130"><dt>**RFU**</dt></span></span> </dl>                                                           | <span data-ttu-id="e1ae7-131">Position du bit :-XX-----</span><span class="sxs-lookup"><span data-stu-id="e1ae7-131">Bit position: -xx-----</span></span><br/> <span data-ttu-id="e1ae7-132">00 (les autres valeurs sont RFU).</span><span class="sxs-lookup"><span data-stu-id="e1ae7-132">00 (other values are RFU).</span></span><br/>                                                                                                         |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <span data-ttu-id="e1ae7-133"><dt>**Secret**</dt></span><span class="sxs-lookup"><span data-stu-id="e1ae7-133"><dt>**Secret**</dt></span></span> </dl>                         | <span data-ttu-id="e1ae7-134">Position du bit :---xxxxx</span><span class="sxs-lookup"><span data-stu-id="e1ae7-134">Bit position: ---xxxxx</span></span><br/> <span data-ttu-id="e1ae7-135">Numéro du secret.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-135">Number of the secret.</span></span><br/>                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="e1ae7-136">*pChallenge* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1ae7-136">*pChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1ae7-137">Pointeur vers les données liées à l’authentification (par exemple, Challenge).</span><span class="sxs-lookup"><span data-stu-id="e1ae7-137">Pointer to the authentication-related data (for example, challenge).</span></span>

</dd> <dt>

<span data-ttu-id="e1ae7-138">*lReplyBytes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1ae7-138">*lReplyBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1ae7-139">Nombre maximal d’octets attendus dans la réponse.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-139">Maximum number of bytes expected in response.</span></span>

</dd> <dt>

<span data-ttu-id="e1ae7-140">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e1ae7-140">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1ae7-141">En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-141">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="e1ae7-142">Au retour, elle est remplie avec la commande APDU construite par cette opération.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-142">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="e1ae7-143">Si *ppCmd* a été défini **sur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé en interne et retourné à l’aide du pointeur *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="e1ae7-143">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1ae7-144">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1ae7-144">Return value</span></span>

<span data-ttu-id="e1ae7-145">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-145">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="e1ae7-146">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e1ae7-146">Return code</span></span>                                                                                   | <span data-ttu-id="e1ae7-147">Description</span><span class="sxs-lookup"><span data-stu-id="e1ae7-147">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e1ae7-148"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e1ae7-148"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e1ae7-149">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-149">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="e1ae7-150"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e1ae7-150"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e1ae7-151">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-151">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="e1ae7-152"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="e1ae7-152"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e1ae7-153">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-153">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="e1ae7-154"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="e1ae7-154"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e1ae7-155">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-155">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="e1ae7-156">Notes</span><span class="sxs-lookup"><span data-stu-id="e1ae7-156">Remarks</span></span>

<span data-ttu-id="e1ae7-157">La réussite de l’exécution de la commande peut être soumise à la réussite des commandes précédentes (par exemple, vérifier ou sélectionner un fichier) ou à des sélections (par exemple, la clé secrète pertinente).</span><span class="sxs-lookup"><span data-stu-id="e1ae7-157">The successful execution of the command may be subject to successful completion of prior commands (for example, VERIFY or SELECT FILE) or selections (for example, the relevant secret).</span></span>

<span data-ttu-id="e1ae7-158">Si une clé et un algorithme sont actuellement sélectionnés lors de l’émission de la commande, la commande peut utiliser la clé et l’algorithme de manière implicite.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-158">If a key and an algorithm are currently selected when issuing the command, then the command may implicitly use the key and the algorithm.</span></span>

<span data-ttu-id="e1ae7-159">Le nombre de fois où la commande est émise peut être enregistré dans la carte pour limiter le nombre de tentatives supplémentaires d’utilisation de la clé secrète ou de l’algorithme approprié.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-159">The number of times the command is issued may be recorded in the card to limit the number of further attempts of using the relevant secret or the algorithm.</span></span>

<span data-ttu-id="e1ae7-160">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="e1ae7-160">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="e1ae7-161">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="e1ae7-161">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="e1ae7-162">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="e1ae7-162">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1ae7-163">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1ae7-163">Requirements</span></span>



| <span data-ttu-id="e1ae7-164">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1ae7-164">Requirement</span></span> | <span data-ttu-id="e1ae7-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1ae7-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ae7-166">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1ae7-166">Minimum supported client</span></span><br/> | <span data-ttu-id="e1ae7-167">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1ae7-167">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e1ae7-168">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1ae7-168">Minimum supported server</span></span><br/> | <span data-ttu-id="e1ae7-169">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1ae7-169">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e1ae7-170">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e1ae7-170">End of client support</span></span><br/>    | <span data-ttu-id="e1ae7-171">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e1ae7-171">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="e1ae7-172">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="e1ae7-172">End of server support</span></span><br/>    | <span data-ttu-id="e1ae7-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e1ae7-173">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="e1ae7-174">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1ae7-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1ae7-175"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1ae7-175"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e1ae7-176">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e1ae7-176">Type library</span></span><br/>             | <dl> <span data-ttu-id="e1ae7-177"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e1ae7-177"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e1ae7-178">DLL</span><span class="sxs-lookup"><span data-stu-id="e1ae7-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1ae7-179"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1ae7-179"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e1ae7-180">IID</span><span class="sxs-lookup"><span data-stu-id="e1ae7-180">IID</span></span><br/>                      | <span data-ttu-id="e1ae7-181">IID \_ ISCardISO7816 est défini en tant que 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="e1ae7-181">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="e1ae7-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1ae7-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1ae7-183">**ExternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="e1ae7-183">**ExternalAuthenticate**</span></span>](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="e1ae7-184">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="e1ae7-184">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
