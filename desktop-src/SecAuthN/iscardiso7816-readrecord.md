---
description: La méthode ReadRecord construit une commande APDU (Application Protocol Data Unit) qui lit soit le contenu des enregistrements spécifiés, soit la partie de début d’un enregistrement d’un fichier élémentaire.
ms.assetid: b00a3242-93bc-4779-8c62-89157fbcb5d1
title: 'ISCardISO7816 :: ReadRecord, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0cb9697315a6f9dd2436cd7a64d54fa6b44e00f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034476"
---
# <a name="iscardiso7816readrecord-method"></a><span data-ttu-id="bf7ae-103">ISCardISO7816 :: ReadRecord, méthode</span><span class="sxs-lookup"><span data-stu-id="bf7ae-103">ISCardISO7816::ReadRecord method</span></span>

<span data-ttu-id="bf7ae-104">\[La méthode **ReadRecord** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-104">\[The **ReadRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bf7ae-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bf7ae-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="bf7ae-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="bf7ae-107">La méthode **ReadRecord** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui lit soit le contenu des enregistrements spécifiés, soit la partie de début d’un enregistrement d’un fichier élémentaire.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-107">The **ReadRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that reads either the contents of the specified records or the beginning part of one record of an elementary file.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf7ae-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf7ae-108">Syntax</span></span>


```C++
HRESULT ReadRecord(
  [in]      BYTE       byRecordId,
  [in]      BYTE       byRefCtrl,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="bf7ae-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf7ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf7ae-110">*byRecordId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf7ae-110">*byRecordId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf7ae-111">Numéro d’enregistrement ou ID du premier enregistrement à lire (00 indique l’enregistrement en cours).</span><span class="sxs-lookup"><span data-stu-id="bf7ae-111">Record number or ID of the first record to be read (00 indicates the current record).</span></span>

</dd> <dt>

<span data-ttu-id="bf7ae-112">*byRefCtrl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf7ae-112">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf7ae-113">Codage du contrôle de référence.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-113">Coding of the reference control.</span></span>



| <span data-ttu-id="bf7ae-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf7ae-114">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="bf7ae-115">Signification</span><span class="sxs-lookup"><span data-stu-id="bf7ae-115">Meaning</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="bf7ae-116"><dt>**EF actuel**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7ae-116"><dt>**Current EF**</dt></span></span> </dl>     | <span data-ttu-id="bf7ae-117">Position du bit : 00000---</span><span class="sxs-lookup"><span data-stu-id="bf7ae-117">Bit position: 00000---</span></span><br/> <span data-ttu-id="bf7ae-118">EF actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-118">Currently selected EF.</span></span><br/>                    |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="bf7ae-119"><dt>**ID EF Short**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7ae-119"><dt>**Short EF ID**</dt></span></span> </dl> | <span data-ttu-id="bf7ae-120">Position du bit : xxxxx---</span><span class="sxs-lookup"><span data-stu-id="bf7ae-120">Bit position: xxxxx---</span></span><br/> <span data-ttu-id="bf7ae-121">Identificateur EF bref.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-121">Short EF identifier.</span></span><br/>                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="bf7ae-122"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7ae-122"><dt>**RFU**</dt></span></span> </dl>                                                       | <span data-ttu-id="bf7ae-123">Position du bit : 11111---</span><span class="sxs-lookup"><span data-stu-id="bf7ae-123">Bit position: 11111---</span></span><br/>                                                      |
| <span id="Record__"></span><span id="record__"></span><span id="RECORD__"></span><dl> <span data-ttu-id="bf7ae-124"><dt>**Enregistrement \#**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7ae-124"><dt>**Record \#**</dt></span></span> </dl>            | <span data-ttu-id="bf7ae-125">Position du bit :-----1xx</span><span class="sxs-lookup"><span data-stu-id="bf7ae-125">Bit position: -----1xx</span></span><br/> <span data-ttu-id="bf7ae-126">Utilisation du numéro d’enregistrement dans P1.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-126">Usage of record number in P1.</span></span><br/>             |
| <span id="Read_Record"></span><span id="read_record"></span><span id="READ_RECORD"></span><dl> <span data-ttu-id="bf7ae-127"><dt>**Lire l’enregistrement**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7ae-127"><dt>**Read Record**</dt></span></span> </dl> | <span data-ttu-id="bf7ae-128">Position du bit :-----100</span><span class="sxs-lookup"><span data-stu-id="bf7ae-128">Bit position: -----100</span></span><br/> <span data-ttu-id="bf7ae-129">Lire l’enregistrement P1.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-129">Read record P1.</span></span><br/>                           |
| <span id="Up_to_Last"></span><span id="up_to_last"></span><span id="UP_TO_LAST"></span><dl> <span data-ttu-id="bf7ae-130"><dt>**Jusqu’au dernier**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7ae-130"><dt>**Up to Last**</dt></span></span> </dl>     | <span data-ttu-id="bf7ae-131">Position du bit :-----101</span><span class="sxs-lookup"><span data-stu-id="bf7ae-131">Bit position: -----101</span></span><br/> <span data-ttu-id="bf7ae-132">Lit tous les enregistrements de P1 jusqu’au dernier.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-132">Read all records from P1 up to the last.</span></span> <br/> |
| <span id="Up_to_P1"></span><span id="up_to_p1"></span><span id="UP_TO_P1"></span><dl> <span data-ttu-id="bf7ae-133"><dt>**Jusqu’à P1**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7ae-133"><dt>**Up to P1**</dt></span></span> </dl>             | <span data-ttu-id="bf7ae-134">Position du bit :-----110</span><span class="sxs-lookup"><span data-stu-id="bf7ae-134">Bit position: -----110</span></span><br/> <span data-ttu-id="bf7ae-135">Lit tous les enregistrements du dernier au plus P1.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-135">Read all records from the last up to P1.</span></span> <br/> |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="bf7ae-136"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7ae-136"><dt>**RFU**</dt></span></span> </dl>                                                       | <span data-ttu-id="bf7ae-137">Position du bit :-----111</span><span class="sxs-lookup"><span data-stu-id="bf7ae-137">Bit position: -----111</span></span><br/>                                                      |
| <span id="Record_ID"></span><span id="record_id"></span><span id="RECORD_ID"></span><dl> <span data-ttu-id="bf7ae-138"><dt>**ID d’enregistrement**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7ae-138"><dt>**Record ID**</dt></span></span> </dl>         | <span data-ttu-id="bf7ae-139">Position du bit :-----0XX</span><span class="sxs-lookup"><span data-stu-id="bf7ae-139">Bit position: -----0xx</span></span><br/> <span data-ttu-id="bf7ae-140">Utilisation du numéro d’enregistrement dans P1.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-140">Usage of record number in P1.</span></span><br/>             |
| <span id="First_Occur"></span><span id="first_occur"></span><span id="FIRST_OCCUR"></span><dl> <span data-ttu-id="bf7ae-141"><dt>**Première apparition**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7ae-141"><dt>**First Occur**</dt></span></span> </dl> | <span data-ttu-id="bf7ae-142">Position du bit :-----000</span><span class="sxs-lookup"><span data-stu-id="bf7ae-142">Bit position: -----000</span></span><br/> <span data-ttu-id="bf7ae-143">Lire la première occurrence.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-143">Read first occurrence.</span></span> <br/>                   |
| <span id="Last_Occur"></span><span id="last_occur"></span><span id="LAST_OCCUR"></span><dl> <span data-ttu-id="bf7ae-144"><dt>**Dernière exécution**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7ae-144"><dt>**Last Occur**</dt></span></span> </dl>     | <span data-ttu-id="bf7ae-145">Position du bit :-----001</span><span class="sxs-lookup"><span data-stu-id="bf7ae-145">Bit position: -----001</span></span><br/> <span data-ttu-id="bf7ae-146">Lire la dernière occurrence.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-146">Read last occurrence.</span></span> <br/>                    |
| <span id="Next_Occur"></span><span id="next_occur"></span><span id="NEXT_OCCUR"></span><dl> <span data-ttu-id="bf7ae-147"><dt>**Suivant**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7ae-147"><dt>**Next Occur**</dt></span></span> </dl>     | <span data-ttu-id="bf7ae-148">Position du bit :-----010</span><span class="sxs-lookup"><span data-stu-id="bf7ae-148">Bit position: -----010</span></span><br/> <span data-ttu-id="bf7ae-149">Lire l’occurrence suivante.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-149">Read next occurrence.</span></span> <br/>                    |
| <span id="Previous"></span><span id="previous"></span><span id="PREVIOUS"></span><dl> <span data-ttu-id="bf7ae-150"><dt>**Précédente**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7ae-150"><dt>**Previous**</dt></span></span> </dl>             | <span data-ttu-id="bf7ae-151">Position du bit :-----011</span><span class="sxs-lookup"><span data-stu-id="bf7ae-151">Bit position: -----011</span></span><br/> <span data-ttu-id="bf7ae-152">Lire l’occurrence précédente.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-152">Read previous occurrence.</span></span> <br/>                |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <span data-ttu-id="bf7ae-153"><dt>**Secret**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7ae-153"><dt>**Secret**</dt></span></span> </dl>                     | <span data-ttu-id="bf7ae-154">Position du bit :---xxxxx</span><span class="sxs-lookup"><span data-stu-id="bf7ae-154">Bit position: ---xxxxx</span></span><br/>                                                      |



 

</dd> <dt>

<span data-ttu-id="bf7ae-155">*lBytesToRead* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf7ae-155">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf7ae-156">Nombre d’octets à lire à partir du EF transparent.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-156">Number of bytes to read from the transparent EF.</span></span>

<span data-ttu-id="bf7ae-157">Si le champ le contient uniquement des zéros, en fonction de b3b2b1 de P2 et dans la limite de 256 pour la longueur abrégée ou de 65536 pour la longueur étendue, la commande doit lire complètement l’enregistrement demandé unique ou la séquence d’enregistrements demandée.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-157">If the Le field contains only zeros, then depending on b3b2b1 of P2 and within the limit of 256 for short length or 65536 for extended length, the command should read completely either the single requested record or the requested sequence of records.</span></span>

</dd> <dt>

<span data-ttu-id="bf7ae-158">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bf7ae-158">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf7ae-159">En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-159">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="bf7ae-160">Au retour, elle est remplie avec la commande APDU construite par cette opération.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-160">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="bf7ae-161">Si *ppCmd* a été défini avec la **valeur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé et retourné en interne par le biais du pointeur *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="bf7ae-161">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf7ae-162">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bf7ae-162">Return value</span></span>

<span data-ttu-id="bf7ae-163">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-163">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="bf7ae-164">Code de retour</span><span class="sxs-lookup"><span data-stu-id="bf7ae-164">Return code</span></span>                                                                                   | <span data-ttu-id="bf7ae-165">Description</span><span class="sxs-lookup"><span data-stu-id="bf7ae-165">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="bf7ae-166"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7ae-166"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bf7ae-167">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-167">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="bf7ae-168"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7ae-168"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="bf7ae-169">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-169">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="bf7ae-170"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7ae-170"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bf7ae-171">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-171">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="bf7ae-172"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7ae-172"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bf7ae-173">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-173">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="bf7ae-174">Notes</span><span class="sxs-lookup"><span data-stu-id="bf7ae-174">Remarks</span></span>

<span data-ttu-id="bf7ae-175">La commande encapsulée ne peut être exécutée que si l’état de sécurité de la [*carte à puce*](../secgloss/s-gly.md) répond aux attributs de sécurité du fichier élémentaire en cours de lecture.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-175">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being read.</span></span>

<span data-ttu-id="bf7ae-176">Si un autre fichier élémentaire est actuellement sélectionné au moment de l’émission de cette commande, il peut être traité sans identification du fichier actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-176">If another elementary file is currently selected at the time of issuing this command, it may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="bf7ae-177">Lorsque la commande contient un identificateur élémentaire Short valide, elle définit le fichier en tant que fichier élémentaire actuel.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-177">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="bf7ae-178">Impossible de lire les fichiers élémentaires sans structure d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-178">Elementary files without a record structure cannot be read.</span></span> <span data-ttu-id="bf7ae-179">La commande encapsulée est abandonnée si elle est appliquée à un fichier élémentaire sans structure d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-179">The encapsulated command aborts if applied to an elementary file without a record structure.</span></span>

<span data-ttu-id="bf7ae-180">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="bf7ae-180">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="bf7ae-181">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="bf7ae-181">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="bf7ae-182">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="bf7ae-182">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf7ae-183">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf7ae-183">Requirements</span></span>



| <span data-ttu-id="bf7ae-184">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf7ae-184">Requirement</span></span> | <span data-ttu-id="bf7ae-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf7ae-185">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf7ae-186">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf7ae-186">Minimum supported client</span></span><br/> | <span data-ttu-id="bf7ae-187">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf7ae-187">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bf7ae-188">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf7ae-188">Minimum supported server</span></span><br/> | <span data-ttu-id="bf7ae-189">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf7ae-189">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bf7ae-190">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="bf7ae-190">End of client support</span></span><br/>    | <span data-ttu-id="bf7ae-191">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bf7ae-191">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="bf7ae-192">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="bf7ae-192">End of server support</span></span><br/>    | <span data-ttu-id="bf7ae-193">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bf7ae-193">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="bf7ae-194">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf7ae-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf7ae-195"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf7ae-195"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf7ae-196">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="bf7ae-196">Type library</span></span><br/>             | <dl> <span data-ttu-id="bf7ae-197"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bf7ae-197"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bf7ae-198">DLL</span><span class="sxs-lookup"><span data-stu-id="bf7ae-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf7ae-199"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf7ae-199"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bf7ae-200">IID</span><span class="sxs-lookup"><span data-stu-id="bf7ae-200">IID</span></span><br/>                      | <span data-ttu-id="bf7ae-201">IID \_ ISCardISO7816 est défini en tant que 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="bf7ae-201">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="bf7ae-202">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf7ae-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf7ae-203">**AppendRecord**</span><span class="sxs-lookup"><span data-stu-id="bf7ae-203">**AppendRecord**</span></span>](iscardiso7816-appendrecord.md)
</dt> <dt>

[<span data-ttu-id="bf7ae-204">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="bf7ae-204">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="bf7ae-205">**UpdateRecord**</span><span class="sxs-lookup"><span data-stu-id="bf7ae-205">**UpdateRecord**</span></span>](iscardiso7816-updaterecord.md)
</dt> <dt>

[<span data-ttu-id="bf7ae-206">**WriteRecord**</span><span class="sxs-lookup"><span data-stu-id="bf7ae-206">**WriteRecord**</span></span>](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
