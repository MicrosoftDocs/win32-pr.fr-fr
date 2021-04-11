---
description: La méthode AppendRecord construit une commande APDU (Application Protocol Data Unit) qui ajoute un enregistrement à la fin d’un fichier élémentaire structuré linéairement (EF) ou écrit un enregistrement Numéro 1 dans un fichier élémentaire à structure cyclique.
ms.assetid: 4dd88661-41c4-4238-88c9-279b39afb206
title: 'ISCardISO7816 :: AppendRecord, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.AppendRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 28d1b6762e0a350bb87b673f21fa063ae2478e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201946"
---
# <a name="iscardiso7816appendrecord-method"></a><span data-ttu-id="64066-103">ISCardISO7816 :: AppendRecord, méthode</span><span class="sxs-lookup"><span data-stu-id="64066-103">ISCardISO7816::AppendRecord method</span></span>

<span data-ttu-id="64066-104">\[La méthode **AppendRecord** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="64066-104">\[The **AppendRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="64066-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="64066-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="64066-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="64066-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="64066-107">La méthode **AppendRecord** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui ajoute un enregistrement à la fin d’un fichier élémentaire structuré linéairement (EF) ou écrit un enregistrement Numéro 1 dans un fichier élémentaire à structure cyclique.</span><span class="sxs-lookup"><span data-stu-id="64066-107">The **AppendRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that either appends a record to the end of a linear-structured elementary file (EF) or writes record number 1 in a cyclic-structured elementary file.</span></span>

## <a name="syntax"></a><span data-ttu-id="64066-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64066-108">Syntax</span></span>


```C++
HRESULT AppendRecord(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="64066-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64066-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64066-110">*byRefCtrl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64066-110">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64066-111">Identifie le fichier élémentaire à ajouter.</span><span class="sxs-lookup"><span data-stu-id="64066-111">Identifies the elementary file to be appended.</span></span>



| <span data-ttu-id="64066-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="64066-112">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="64066-113">Signification</span><span class="sxs-lookup"><span data-stu-id="64066-113">Meaning</span></span>                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="64066-114"><dt>**EF actuel**</dt></span><span class="sxs-lookup"><span data-stu-id="64066-114"><dt>**Current EF**</dt></span></span> </dl>     | <span data-ttu-id="64066-115">Position du bit : 00000000</span><span class="sxs-lookup"><span data-stu-id="64066-115">Bit position: 00000000</span></span><br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="64066-116"><dt>**ID EF Short**</dt></span><span class="sxs-lookup"><span data-stu-id="64066-116"><dt>**Short EF ID**</dt></span></span> </dl> | <span data-ttu-id="64066-117">Position du bit : XXXXX000</span><span class="sxs-lookup"><span data-stu-id="64066-117">Bit position: xxxxx000</span></span><br/> |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <span data-ttu-id="64066-118"><dt>**Réservé**</dt></span><span class="sxs-lookup"><span data-stu-id="64066-118"><dt>**Reserved**</dt></span></span> </dl>             | <span data-ttu-id="64066-119">Position du bit : xxxxxxxx</span><span class="sxs-lookup"><span data-stu-id="64066-119">Bit position: xxxxxxxx</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="64066-120">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64066-120">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64066-121">Pointeur vers les données à ajouter au fichier.</span><span class="sxs-lookup"><span data-stu-id="64066-121">A pointer to the data to be appended to the file.</span></span>



| <span data-ttu-id="64066-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="64066-122">Value</span></span>                                                                                                                                                | <span data-ttu-id="64066-123">Signification</span><span class="sxs-lookup"><span data-stu-id="64066-123">Meaning</span></span>                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="Tn"></span><span id="tn"></span><span id="TN"></span><dl> <span data-ttu-id="64066-124"><dt>**TN**</dt></span><span class="sxs-lookup"><span data-stu-id="64066-124"><dt>**Tn**</dt></span></span> </dl>     | <span data-ttu-id="64066-125">1 octet</span><span class="sxs-lookup"><span data-stu-id="64066-125">1 byte</span></span><br/>       |
| <span id="Ln_"></span><span id="ln_"></span><span id="LN_"></span><dl> <span data-ttu-id="64066-126"><dt>**LN**</dt></span><span class="sxs-lookup"><span data-stu-id="64066-126"><dt>**Ln** </dt></span></span> </dl> | <span data-ttu-id="64066-127">1 ou 3 octets</span><span class="sxs-lookup"><span data-stu-id="64066-127">1 or 3 bytes</span></span><br/> |
| <span id="data"></span><span id="DATA"></span><dl> <span data-ttu-id="64066-128"><dt>**métadonnée**</dt></span><span class="sxs-lookup"><span data-stu-id="64066-128"><dt>**data**</dt></span></span> </dl>                    | <span data-ttu-id="64066-129">Octets de ln</span><span class="sxs-lookup"><span data-stu-id="64066-129">Ln bytes</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="64066-130">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="64066-130">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="64066-131">En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.</span><span class="sxs-lookup"><span data-stu-id="64066-131">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="64066-132">Au retour, elle est remplie avec la commande APDU construite par cette opération.</span><span class="sxs-lookup"><span data-stu-id="64066-132">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="64066-133">Si *ppCmd* a été défini **sur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé et retourné en interne à l’aide du pointeur *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="64066-133">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64066-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="64066-134">Return value</span></span>

<span data-ttu-id="64066-135">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="64066-135">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="64066-136">Code de retour</span><span class="sxs-lookup"><span data-stu-id="64066-136">Return code</span></span>                                                                                   | <span data-ttu-id="64066-137">Description</span><span class="sxs-lookup"><span data-stu-id="64066-137">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="64066-138"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="64066-138"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="64066-139">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="64066-139">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="64066-140"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="64066-140"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="64066-141">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="64066-141">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="64066-142"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="64066-142"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="64066-143">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="64066-143">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="64066-144"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="64066-144"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="64066-145">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="64066-145">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="64066-146">Notes</span><span class="sxs-lookup"><span data-stu-id="64066-146">Remarks</span></span>

<span data-ttu-id="64066-147">La commande encapsulée ne peut être exécutée que si l’état de sécurité de la [*carte à puce*](../secgloss/s-gly.md) répond aux attributs de sécurité de la lecture de fichier élémentaire.</span><span class="sxs-lookup"><span data-stu-id="64066-147">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file read.</span></span>

<span data-ttu-id="64066-148">Si un autre fichier élémentaire est sélectionné au moment de l’émission de cette commande, il peut être traité sans identification du fichier actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="64066-148">If another elementary file is selected at the time of issuing this command, it may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="64066-149">Impossible de lire les fichiers élémentaires sans structure d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="64066-149">Elementary files without a record structure cannot be read.</span></span> <span data-ttu-id="64066-150">La commande encapsulée est abandonnée si elle est appliquée à un fichier élémentaire sans structure d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="64066-150">The encapsulated command aborts if applied to an elementary file without a record structure.</span></span>

<span data-ttu-id="64066-151">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="64066-151">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="64066-152">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="64066-152">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="64066-153">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="64066-153">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="64066-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64066-154">Requirements</span></span>



| <span data-ttu-id="64066-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64066-155">Requirement</span></span> | <span data-ttu-id="64066-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="64066-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64066-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64066-157">Minimum supported client</span></span><br/> | <span data-ttu-id="64066-158">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64066-158">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="64066-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64066-159">Minimum supported server</span></span><br/> | <span data-ttu-id="64066-160">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64066-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="64066-161">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="64066-161">End of client support</span></span><br/>    | <span data-ttu-id="64066-162">Windows XP</span><span class="sxs-lookup"><span data-stu-id="64066-162">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="64066-163">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="64066-163">End of server support</span></span><br/>    | <span data-ttu-id="64066-164">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="64066-164">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="64066-165">En-tête</span><span class="sxs-lookup"><span data-stu-id="64066-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="64066-166"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="64066-166"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="64066-167">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="64066-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="64066-168"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="64066-168"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="64066-169">DLL</span><span class="sxs-lookup"><span data-stu-id="64066-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64066-170"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64066-170"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="64066-171">IID</span><span class="sxs-lookup"><span data-stu-id="64066-171">IID</span></span><br/>                      | <span data-ttu-id="64066-172">IID \_ ISCardISO7816 est défini en tant que 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="64066-172">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="64066-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64066-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64066-174">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="64066-174">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="64066-175">**ReadRecord**</span><span class="sxs-lookup"><span data-stu-id="64066-175">**ReadRecord**</span></span>](iscardiso7816-readrecord.md)
</dt> <dt>

[<span data-ttu-id="64066-176">**UpdateRecord**</span><span class="sxs-lookup"><span data-stu-id="64066-176">**UpdateRecord**</span></span>](iscardiso7816-updaterecord.md)
</dt> <dt>

[<span data-ttu-id="64066-177">**WriteRecord**</span><span class="sxs-lookup"><span data-stu-id="64066-177">**WriteRecord**</span></span>](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
