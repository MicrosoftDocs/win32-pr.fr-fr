---
description: Construit une commande APDU qui initie l’une des opérations listées.
ms.assetid: 2ce313b9-ccd7-4be0-a91f-d0747e35fab8
title: 'ISCardISO7816 :: WriteRecord, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 30bfdb9ff8779633d81da89bbf7ac8e69a617d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112175"
---
# <a name="iscardiso7816writerecord-method"></a><span data-ttu-id="deccb-103">ISCardISO7816 :: WriteRecord, méthode</span><span class="sxs-lookup"><span data-stu-id="deccb-103">ISCardISO7816::WriteRecord method</span></span>

<span data-ttu-id="deccb-104">\[La méthode **WriteRecord** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="deccb-104">\[The **WriteRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="deccb-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="deccb-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="deccb-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="deccb-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="deccb-107">La méthode **WriteRecord** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui initie l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="deccb-107">The **WriteRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that initiates one of the following operations:</span></span>

-   <span data-ttu-id="deccb-108">Écriture unique d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="deccb-108">The write once of a record.</span></span>
-   <span data-ttu-id="deccb-109">**Or** logique des octets de données d’un enregistrement déjà présent dans la carte avec les octets de données de l’enregistrement donné dans la commande APDU.</span><span class="sxs-lookup"><span data-stu-id="deccb-109">The logical **OR** of the data bytes of a record already present in the card with the data bytes of the record given in the command APDU.</span></span>
-   <span data-ttu-id="deccb-110">Le AND logique des octets de données d’un enregistrement déjà présent dans la carte avec les octets de données de l’enregistrement donné dans la commande APDU.</span><span class="sxs-lookup"><span data-stu-id="deccb-110">The logical AND of the data bytes of a record already present in the card with the data bytes of the record given in the command APDU.</span></span>

<span data-ttu-id="deccb-111">Si aucune indication n’est donnée dans l’octet de codage des données, le comportement logique ou s’applique.</span><span class="sxs-lookup"><span data-stu-id="deccb-111">When no indication is given in the data coding byte, the logical OR behavior applies.</span></span>

> [!Note]  
> <span data-ttu-id="deccb-112">Lors de l’utilisation de l’adressage d’enregistrement actuel, la commande définit le pointeur d’enregistrement sur l’enregistrement mis à jour avec succès.</span><span class="sxs-lookup"><span data-stu-id="deccb-112">When using current record addressing, the command sets the record pointer on the successfully updated record.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="deccb-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="deccb-113">Syntax</span></span>


```C++
HRESULT WriteRecord(
  [in]      BYTE         byRecordId,
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="deccb-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="deccb-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deccb-115">*byRecordId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="deccb-115">*byRecordId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deccb-116">Identification de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="deccb-116">Record identification.</span></span> <span data-ttu-id="deccb-117">Il s’agit de la valeur P1 :</span><span class="sxs-lookup"><span data-stu-id="deccb-117">This is the P1 value:</span></span>

<span data-ttu-id="deccb-118">P1 = « 00 » désigne l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="deccb-118">P1 = '00' designates the current record.</span></span>

<span data-ttu-id="deccb-119">P1 ! = « 00 » est le numéro de l’enregistrement spécifié.</span><span class="sxs-lookup"><span data-stu-id="deccb-119">P1 != '00' is the number of the specified record.</span></span>

</dd> <dt>

<span data-ttu-id="deccb-120">*byRefCtrl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="deccb-120">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deccb-121">Codage du contrôle de référence P2.</span><span class="sxs-lookup"><span data-stu-id="deccb-121">Coding of the reference control P2.</span></span>



| <span data-ttu-id="deccb-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="deccb-122">Value</span></span>                                                                                                                                                                                                | <span data-ttu-id="deccb-123">Signification</span><span class="sxs-lookup"><span data-stu-id="deccb-123">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="deccb-124"><dt>**EF actuel**</dt></span><span class="sxs-lookup"><span data-stu-id="deccb-124"><dt>**Current EF**</dt></span></span> </dl>                     | <span data-ttu-id="deccb-125">Position du bit : 00000---</span><span class="sxs-lookup"><span data-stu-id="deccb-125">Bit position: 00000---</span></span><br/> <span data-ttu-id="deccb-126">EF actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="deccb-126">Currently selected EF.</span></span><br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="deccb-127"><dt>**ID EF Short**</dt></span><span class="sxs-lookup"><span data-stu-id="deccb-127"><dt>**Short EF ID**</dt></span></span> </dl>                 | <span data-ttu-id="deccb-128">Position du bit : xxxxx---</span><span class="sxs-lookup"><span data-stu-id="deccb-128">Bit position: xxxxx---</span></span><br/> <span data-ttu-id="deccb-129">Identificateur EF bref.</span><span class="sxs-lookup"><span data-stu-id="deccb-129">Short EF identifier.</span></span><br/>   |
| <span id="First_Record"></span><span id="first_record"></span><span id="FIRST_RECORD"></span><dl> <span data-ttu-id="deccb-130"><dt>**Premier enregistrement**</dt></span><span class="sxs-lookup"><span data-stu-id="deccb-130"><dt>**First Record**</dt></span></span> </dl>             | <span data-ttu-id="deccb-131">Position du bit :-----000</span><span class="sxs-lookup"><span data-stu-id="deccb-131">Bit position: -----000</span></span><br/>                                   |
| <span id="Last_Record"></span><span id="last_record"></span><span id="LAST_RECORD"></span><dl> <span data-ttu-id="deccb-132"><dt>**Dernier enregistrement**</dt></span><span class="sxs-lookup"><span data-stu-id="deccb-132"><dt>**Last Record**</dt></span></span> </dl>                 | <span data-ttu-id="deccb-133">Position du bit :-----001</span><span class="sxs-lookup"><span data-stu-id="deccb-133">Bit position: -----001</span></span><br/>                                   |
| <span id="Next_Record"></span><span id="next_record"></span><span id="NEXT_RECORD"></span><dl> <span data-ttu-id="deccb-134"><dt>**Enregistrement suivant**</dt></span><span class="sxs-lookup"><span data-stu-id="deccb-134"><dt>**Next Record**</dt></span></span> </dl>                 | <span data-ttu-id="deccb-135">Position du bit :-----010</span><span class="sxs-lookup"><span data-stu-id="deccb-135">Bit position: -----010</span></span><br/>                                   |
| <span id="Previous_Record"></span><span id="previous_record"></span><span id="PREVIOUS_RECORD"></span><dl> <span data-ttu-id="deccb-136"><dt>**Enregistrement précédent**</dt></span><span class="sxs-lookup"><span data-stu-id="deccb-136"><dt>**Previous Record**</dt></span></span> </dl> | <span data-ttu-id="deccb-137">Position du bit :-----011</span><span class="sxs-lookup"><span data-stu-id="deccb-137">Bit position: -----011</span></span><br/>                                   |
| <span id="Record___in_P1"></span><span id="record___in_p1"></span><span id="RECORD___IN_P1"></span><dl> <span data-ttu-id="deccb-138"><dt>**Enregistrement \# dans P1**</dt></span><span class="sxs-lookup"><span data-stu-id="deccb-138"><dt>**Record \# in P1**</dt></span></span> </dl>    | <span data-ttu-id="deccb-139">Position du bit :-----100</span><span class="sxs-lookup"><span data-stu-id="deccb-139">Bit position: -----100</span></span><br/>                                   |



 

</dd> <dt>

<span data-ttu-id="deccb-140">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="deccb-140">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deccb-141">Pointeur vers l’enregistrement à écrire.</span><span class="sxs-lookup"><span data-stu-id="deccb-141">Pointer to the record to be written.</span></span>

</dd> <dt>

<span data-ttu-id="deccb-142">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="deccb-142">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="deccb-143">En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.</span><span class="sxs-lookup"><span data-stu-id="deccb-143">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="deccb-144">Au retour, elle est remplie avec la commande APDU construite par cette opération.</span><span class="sxs-lookup"><span data-stu-id="deccb-144">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="deccb-145">Si *ppCmd* a été défini avec la **valeur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé et retourné en interne par le biais du pointeur *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="deccb-145">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deccb-146">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="deccb-146">Return value</span></span>

<span data-ttu-id="deccb-147">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="deccb-147">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="deccb-148">Code de retour</span><span class="sxs-lookup"><span data-stu-id="deccb-148">Return code</span></span>                                                                                   | <span data-ttu-id="deccb-149">Description</span><span class="sxs-lookup"><span data-stu-id="deccb-149">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="deccb-150"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="deccb-150"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="deccb-151">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="deccb-151">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="deccb-152"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="deccb-152"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="deccb-153">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="deccb-153">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="deccb-154"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="deccb-154"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="deccb-155">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="deccb-155">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="deccb-156"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="deccb-156"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="deccb-157">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="deccb-157">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="deccb-158">Notes</span><span class="sxs-lookup"><span data-stu-id="deccb-158">Remarks</span></span>

<span data-ttu-id="deccb-159">La commande encapsulée ne peut être exécutée que si l’état de sécurité de la [*carte à puce*](../secgloss/s-gly.md) répond aux attributs de sécurité du fichier élémentaire en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="deccb-159">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="deccb-160">Lorsque la commande contient un identificateur élémentaire Short valide, elle définit le fichier en tant que fichier élémentaire actuel.</span><span class="sxs-lookup"><span data-stu-id="deccb-160">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span> <span data-ttu-id="deccb-161">Si un autre fichier élémentaire est actuellement sélectionné au moment de l’émission de cette commande, cette commande peut être traitée sans identification du fichier actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="deccb-161">If another elementary file is currently selected at the time of issuing this command, this command may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="deccb-162">Si la commande encapsulée s’applique à un fichier élémentaire linéaire ou à structure cyclique, elle est abandonnée si la longueur de l’enregistrement est différente de la longueur de l’enregistrement existant.</span><span class="sxs-lookup"><span data-stu-id="deccb-162">If the encapsulated command applies to a linear-fixed or cyclic-structured elementary file, it will abort if the record length is different from the length of the existing record.</span></span> <span data-ttu-id="deccb-163">Si elle s’applique à un fichier élémentaire structuré à variables linéaires, elle peut être exécutée lorsque la longueur de l’enregistrement est différente de la longueur de l’enregistrement existant.</span><span class="sxs-lookup"><span data-stu-id="deccb-163">If it applies to a linear-variable structured elementary file, it may be carried out when the record length is different from the length of the existing record.</span></span>

<span data-ttu-id="deccb-164">Si P2 = xxxxx011 et que le fichier élémentaire est un fichier cyclique, cette commande a le même comportement qu’une commande construite à l’aide de [**AppendRecord**](iscardiso7816-appendrecord.md).</span><span class="sxs-lookup"><span data-stu-id="deccb-164">If P2=xxxxx011 and the elementary file is cyclic file, this command has the same behavior a command constructed using [**AppendRecord**](iscardiso7816-appendrecord.md).</span></span>

<span data-ttu-id="deccb-165">Impossible d’écrire dans les fichiers élémentaires sans structure d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="deccb-165">Elementary files without a record structure cannot be written to.</span></span> <span data-ttu-id="deccb-166">La commande construite s’arrête si elle est appliquée à un fichier élémentaire sans structure d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="deccb-166">The constructed command aborts if applied to an elementary file without a record structure.</span></span>

<span data-ttu-id="deccb-167">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="deccb-167">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="deccb-168">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="deccb-168">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="deccb-169">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="deccb-169">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="deccb-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="deccb-170">Requirements</span></span>



| <span data-ttu-id="deccb-171">Condition requise</span><span class="sxs-lookup"><span data-stu-id="deccb-171">Requirement</span></span> | <span data-ttu-id="deccb-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="deccb-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="deccb-173">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="deccb-173">Minimum supported client</span></span><br/> | <span data-ttu-id="deccb-174">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="deccb-174">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="deccb-175">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="deccb-175">Minimum supported server</span></span><br/> | <span data-ttu-id="deccb-176">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="deccb-176">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="deccb-177">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="deccb-177">End of client support</span></span><br/>    | <span data-ttu-id="deccb-178">Windows XP</span><span class="sxs-lookup"><span data-stu-id="deccb-178">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="deccb-179">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="deccb-179">End of server support</span></span><br/>    | <span data-ttu-id="deccb-180">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="deccb-180">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="deccb-181">En-tête</span><span class="sxs-lookup"><span data-stu-id="deccb-181">Header</span></span><br/>                   | <dl> <span data-ttu-id="deccb-182"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="deccb-182"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="deccb-183">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="deccb-183">Type library</span></span><br/>             | <dl> <span data-ttu-id="deccb-184"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="deccb-184"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="deccb-185">DLL</span><span class="sxs-lookup"><span data-stu-id="deccb-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="deccb-186"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="deccb-186"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="deccb-187">IID</span><span class="sxs-lookup"><span data-stu-id="deccb-187">IID</span></span><br/>                      | <span data-ttu-id="deccb-188">IID \_ ISCardISO7816 est défini en tant que 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="deccb-188">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="deccb-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="deccb-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deccb-190">**AppendRecord**</span><span class="sxs-lookup"><span data-stu-id="deccb-190">**AppendRecord**</span></span>](iscardiso7816-appendrecord.md)
</dt> <dt>

[<span data-ttu-id="deccb-191">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="deccb-191">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="deccb-192">**ReadRecord**</span><span class="sxs-lookup"><span data-stu-id="deccb-192">**ReadRecord**</span></span>](iscardiso7816-readrecord.md)
</dt> <dt>

[<span data-ttu-id="deccb-193">**UpdateRecord**</span><span class="sxs-lookup"><span data-stu-id="deccb-193">**UpdateRecord**</span></span>](iscardiso7816-updaterecord.md)
</dt> </dl>

 

 
