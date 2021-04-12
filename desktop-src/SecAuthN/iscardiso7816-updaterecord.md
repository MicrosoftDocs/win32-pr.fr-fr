---
description: La méthode UpdateRecord construit une commande APDU (Application Protocol Data Unit) qui met à jour un enregistrement spécifique avec les bits indiqués dans la commande APDU.
ms.assetid: 66039afd-5d73-41b3-b87b-b5d598c6f3db
title: 'ISCardISO7816 :: UpdateRecord, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.UpdateRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6bf810594e623d58944f58d3b7671664b3be175f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203050"
---
# <a name="iscardiso7816updaterecord-method"></a><span data-ttu-id="aa0eb-103">ISCardISO7816 :: UpdateRecord, méthode</span><span class="sxs-lookup"><span data-stu-id="aa0eb-103">ISCardISO7816::UpdateRecord method</span></span>

<span data-ttu-id="aa0eb-104">\[La méthode **UpdateRecord** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="aa0eb-104">\[The **UpdateRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="aa0eb-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="aa0eb-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="aa0eb-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="aa0eb-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="aa0eb-107">La méthode **UpdateRecord** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui met à jour un enregistrement spécifique avec les bits indiqués dans la commande APDU.</span><span class="sxs-lookup"><span data-stu-id="aa0eb-107">The **UpdateRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that updates a specific record with the bits given in the APDU command.</span></span>

> [!Note]  
> <span data-ttu-id="aa0eb-108">Lors de l’utilisation de l’adressage d’enregistrement actuel, la commande définit le pointeur d’enregistrement sur l’enregistrement mis à jour avec succès.</span><span class="sxs-lookup"><span data-stu-id="aa0eb-108">When using current record addressing, the command sets the record pointer on the successfully updated record.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="aa0eb-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa0eb-109">Syntax</span></span>


```C++
HRESULT UpdateRecord(
  [in]      BYTE         byRecordId,
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="aa0eb-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa0eb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa0eb-111">*byRecordId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aa0eb-111">*byRecordId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa0eb-112">Valeur P1 :</span><span class="sxs-lookup"><span data-stu-id="aa0eb-112">P1 value:</span></span>

<span data-ttu-id="aa0eb-113">P1 = 00 désigne l’enregistrement en cours</span><span class="sxs-lookup"><span data-stu-id="aa0eb-113">P1 = 00 designates the current record</span></span>

<span data-ttu-id="aa0eb-114">P1 ! = « 00 » est le numéro de l’enregistrement spécifié</span><span class="sxs-lookup"><span data-stu-id="aa0eb-114">P1 != '00' is the number of the specified record</span></span>

</dd> <dt>

<span data-ttu-id="aa0eb-115">*byRefCtrl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aa0eb-115">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa0eb-116">Codage du contrôle de référence P2 :</span><span class="sxs-lookup"><span data-stu-id="aa0eb-116">Coding of the reference control P2:</span></span>



| <span data-ttu-id="aa0eb-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa0eb-117">Value</span></span>                                                                                                                                                                                                | <span data-ttu-id="aa0eb-118">Signification</span><span class="sxs-lookup"><span data-stu-id="aa0eb-118">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="aa0eb-119"><dt>**EF actuel**</dt></span><span class="sxs-lookup"><span data-stu-id="aa0eb-119"><dt>**Current EF**</dt></span></span> </dl>                     | <span data-ttu-id="aa0eb-120">Position du bit : 00000---</span><span class="sxs-lookup"><span data-stu-id="aa0eb-120">Bit position: 00000---</span></span><br/> <span data-ttu-id="aa0eb-121">EF actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="aa0eb-121">Currently selected EF.</span></span><br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="aa0eb-122"><dt>**ID EF Short**</dt></span><span class="sxs-lookup"><span data-stu-id="aa0eb-122"><dt>**Short EF ID**</dt></span></span> </dl>                 | <span data-ttu-id="aa0eb-123">Position du bit : xxxxx---</span><span class="sxs-lookup"><span data-stu-id="aa0eb-123">Bit position: xxxxx---</span></span><br/> <span data-ttu-id="aa0eb-124">Identificateur EF bref.</span><span class="sxs-lookup"><span data-stu-id="aa0eb-124">Short EF identifier.</span></span><br/>   |
| <span id="First_Record"></span><span id="first_record"></span><span id="FIRST_RECORD"></span><dl> <span data-ttu-id="aa0eb-125"><dt>**Premier enregistrement**</dt></span><span class="sxs-lookup"><span data-stu-id="aa0eb-125"><dt>**First Record**</dt></span></span> </dl>             | <span data-ttu-id="aa0eb-126">Position du bit :-----000</span><span class="sxs-lookup"><span data-stu-id="aa0eb-126">Bit position: -----000</span></span><br/>                                   |
| <span id="Last_Record"></span><span id="last_record"></span><span id="LAST_RECORD"></span><dl> <span data-ttu-id="aa0eb-127"><dt>**Dernier enregistrement**</dt></span><span class="sxs-lookup"><span data-stu-id="aa0eb-127"><dt>**Last Record**</dt></span></span> </dl>                 | <span data-ttu-id="aa0eb-128">Position du bit :-----001</span><span class="sxs-lookup"><span data-stu-id="aa0eb-128">Bit position: -----001</span></span><br/>                                   |
| <span id="Next_Record"></span><span id="next_record"></span><span id="NEXT_RECORD"></span><dl> <span data-ttu-id="aa0eb-129"><dt>**Enregistrement suivant**</dt></span><span class="sxs-lookup"><span data-stu-id="aa0eb-129"><dt>**Next Record**</dt></span></span> </dl>                 | <span data-ttu-id="aa0eb-130">Position du bit :-----010</span><span class="sxs-lookup"><span data-stu-id="aa0eb-130">Bit position: -----010</span></span><br/>                                   |
| <span id="Previous_Record"></span><span id="previous_record"></span><span id="PREVIOUS_RECORD"></span><dl> <span data-ttu-id="aa0eb-131"><dt>**Enregistrement précédent**</dt></span><span class="sxs-lookup"><span data-stu-id="aa0eb-131"><dt>**Previous Record**</dt></span></span> </dl> | <span data-ttu-id="aa0eb-132">Position du bit :-----011</span><span class="sxs-lookup"><span data-stu-id="aa0eb-132">Bit position: -----011</span></span><br/>                                   |
| <span id="Record___in_P1"></span><span id="record___in_p1"></span><span id="RECORD___IN_P1"></span><dl> <span data-ttu-id="aa0eb-133"><dt>**Enregistrement \# dans P1**</dt></span><span class="sxs-lookup"><span data-stu-id="aa0eb-133"><dt>**Record \# in P1**</dt></span></span> </dl>    | <span data-ttu-id="aa0eb-134">Position du bit :-----100</span><span class="sxs-lookup"><span data-stu-id="aa0eb-134">Bit position: -----100</span></span><br/>                                   |



 

</dd> <dt>

<span data-ttu-id="aa0eb-135">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aa0eb-135">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa0eb-136">Pointeur vers l’enregistrement à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="aa0eb-136">Pointer to the record to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="aa0eb-137">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="aa0eb-137">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa0eb-138">En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.</span><span class="sxs-lookup"><span data-stu-id="aa0eb-138">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="aa0eb-139">Au retour, elle est remplie avec la commande APDU construite par cette opération.</span><span class="sxs-lookup"><span data-stu-id="aa0eb-139">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="aa0eb-140">Si *ppCmd* a été défini avec la **valeur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé et retourné en interne par le biais du pointeur *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="aa0eb-140">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa0eb-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aa0eb-141">Return value</span></span>

<span data-ttu-id="aa0eb-142">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="aa0eb-142">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="aa0eb-143">Code de retour</span><span class="sxs-lookup"><span data-stu-id="aa0eb-143">Return code</span></span>                                                                                   | <span data-ttu-id="aa0eb-144">Description</span><span class="sxs-lookup"><span data-stu-id="aa0eb-144">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="aa0eb-145"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="aa0eb-145"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="aa0eb-146">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="aa0eb-146">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="aa0eb-147"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="aa0eb-147"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="aa0eb-148">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="aa0eb-148">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="aa0eb-149"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="aa0eb-149"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="aa0eb-150">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="aa0eb-150">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="aa0eb-151"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="aa0eb-151"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="aa0eb-152">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="aa0eb-152">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="aa0eb-153">Notes</span><span class="sxs-lookup"><span data-stu-id="aa0eb-153">Remarks</span></span>

<span data-ttu-id="aa0eb-154">La commande encapsulée ne peut être exécutée que si l’état de sécurité de la [*carte à puce*](../secgloss/s-gly.md) répond aux attributs de sécurité du fichier élémentaire en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="aa0eb-154">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="aa0eb-155">Lorsque la commande contient un identificateur élémentaire Short valide, elle définit le fichier en tant que fichier élémentaire actuel.</span><span class="sxs-lookup"><span data-stu-id="aa0eb-155">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span> <span data-ttu-id="aa0eb-156">Si un autre fichier élémentaire est actuellement sélectionné au moment de l’émission de cette commande, cette commande peut être traitée sans identification du fichier actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="aa0eb-156">If another elementary file is currently selected at the time of issuing this command, this command may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="aa0eb-157">Si la commande construite s’applique à un fichier élémentaire linéaire ou à structure cyclique, elle s’arrête si la longueur de l’enregistrement est différente de la longueur de l’enregistrement existant.</span><span class="sxs-lookup"><span data-stu-id="aa0eb-157">If the constructed command applies to a linear-fixed or cyclic-structured elementary file, it will abort if the record length is different from the length of the existing record.</span></span>

<span data-ttu-id="aa0eb-158">Si la commande s’applique à un fichier élémentaire structuré à variables linéaires, elle peut être exécutée lorsque la longueur de l’enregistrement est différente de la longueur de l’enregistrement existant.</span><span class="sxs-lookup"><span data-stu-id="aa0eb-158">If the command applies to a linear-variable structured elementary file, it may be carried out when the record length is different from the length of the existing record.</span></span>

<span data-ttu-id="aa0eb-159">L’option « Previous » de la commande (P2 = xxxxx011), appliquée à un fichier cyclique, a le même comportement qu’une commande construite par [**AppendRecord**](iscardiso7816-appendrecord.md).</span><span class="sxs-lookup"><span data-stu-id="aa0eb-159">The "previous" option of the command (P2=xxxxx011), applied to a cyclic file, has the same behavior as a command constructed by [**AppendRecord**](iscardiso7816-appendrecord.md).</span></span>

<span data-ttu-id="aa0eb-160">Impossible de lire les fichiers élémentaires sans structure d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="aa0eb-160">Elementary files without a record structure cannot be read.</span></span> <span data-ttu-id="aa0eb-161">La commande construite s’arrête si elle est appliquée à un fichier élémentaire sans structure d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="aa0eb-161">The constructed command aborts if applied to an elementary file without record structure.</span></span>

<span data-ttu-id="aa0eb-162">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="aa0eb-162">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="aa0eb-163">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="aa0eb-163">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="aa0eb-164">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="aa0eb-164">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa0eb-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa0eb-165">Requirements</span></span>



| <span data-ttu-id="aa0eb-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa0eb-166">Requirement</span></span> | <span data-ttu-id="aa0eb-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa0eb-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0eb-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa0eb-168">Minimum supported client</span></span><br/> | <span data-ttu-id="aa0eb-169">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa0eb-169">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="aa0eb-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa0eb-170">Minimum supported server</span></span><br/> | <span data-ttu-id="aa0eb-171">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa0eb-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aa0eb-172">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="aa0eb-172">End of client support</span></span><br/>    | <span data-ttu-id="aa0eb-173">Windows XP</span><span class="sxs-lookup"><span data-stu-id="aa0eb-173">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="aa0eb-174">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="aa0eb-174">End of server support</span></span><br/>    | <span data-ttu-id="aa0eb-175">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aa0eb-175">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="aa0eb-176">En-tête</span><span class="sxs-lookup"><span data-stu-id="aa0eb-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa0eb-177"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa0eb-177"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="aa0eb-178">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="aa0eb-178">Type library</span></span><br/>             | <dl> <span data-ttu-id="aa0eb-179"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="aa0eb-179"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="aa0eb-180">DLL</span><span class="sxs-lookup"><span data-stu-id="aa0eb-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa0eb-181"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa0eb-181"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="aa0eb-182">IID</span><span class="sxs-lookup"><span data-stu-id="aa0eb-182">IID</span></span><br/>                      | <span data-ttu-id="aa0eb-183">IID \_ ISCardISO7816 est défini en tant que 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="aa0eb-183">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="aa0eb-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa0eb-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa0eb-185">**AppendRecord**</span><span class="sxs-lookup"><span data-stu-id="aa0eb-185">**AppendRecord**</span></span>](iscardiso7816-appendrecord.md)
</dt> <dt>

[<span data-ttu-id="aa0eb-186">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="aa0eb-186">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="aa0eb-187">**ReadRecord**</span><span class="sxs-lookup"><span data-stu-id="aa0eb-187">**ReadRecord**</span></span>](iscardiso7816-readrecord.md)
</dt> <dt>

[<span data-ttu-id="aa0eb-188">**WriteRecord**</span><span class="sxs-lookup"><span data-stu-id="aa0eb-188">**WriteRecord**</span></span>](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
