---
description: La méthode GetData construit une commande APDU (Application Protocol Data Unit) qui récupère soit un objet de données primitif unique, soit un ensemble d’objets de données (contenu dans un objet de données construit), en fonction du type de fichier sélectionné.
ms.assetid: d764a765-f451-4bf7-9d06-f5901062dcac
title: 'ISCardISO7816 :: GetData, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 93dca04daa50e068a68dc62cf11a580eb8e3b1c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758097"
---
# <a name="iscardiso7816getdata-method"></a><span data-ttu-id="65c75-103">ISCardISO7816 :: GetData, méthode</span><span class="sxs-lookup"><span data-stu-id="65c75-103">ISCardISO7816::GetData method</span></span>

<span data-ttu-id="65c75-104">\[La méthode **GetData** est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="65c75-104">\[The **GetData** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="65c75-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="65c75-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="65c75-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="65c75-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="65c75-107">La méthode **GetData** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui récupère soit un objet de données primitif unique, soit un ensemble d’objets de données (contenu dans un objet de données construit), en fonction du type de fichier sélectionné.</span><span class="sxs-lookup"><span data-stu-id="65c75-107">The **GetData** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that retrieves either a single primitive data object or a set of data objects (contained in a constructed data object), depending on the type of file selected.</span></span>

## <a name="syntax"></a><span data-ttu-id="65c75-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65c75-108">Syntax</span></span>


```C++
HRESULT GetData(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToGet,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="65c75-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65c75-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65c75-110">*byP1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65c75-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65c75-111">Paramètres.</span><span class="sxs-lookup"><span data-stu-id="65c75-111">Parameters.</span></span>



| <span data-ttu-id="65c75-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="65c75-112">Value</span></span>                                                                                  | <span data-ttu-id="65c75-113">Signification</span><span class="sxs-lookup"><span data-stu-id="65c75-113">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="65c75-114"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="65c75-114"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="65c75-115">RFU</span><span class="sxs-lookup"><span data-stu-id="65c75-115">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="65c75-116"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="65c75-116"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="65c75-117">La balise BER-TLV (1 octet) dans P2</span><span class="sxs-lookup"><span data-stu-id="65c75-117">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="65c75-118"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="65c75-118"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="65c75-119">Données d’application (codage propriétaire)</span><span class="sxs-lookup"><span data-stu-id="65c75-119">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="65c75-120"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="65c75-120"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="65c75-121">Balise SIMPLE-TLV dans P2</span><span class="sxs-lookup"><span data-stu-id="65c75-121">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="65c75-122"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="65c75-122"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="65c75-123">RFU</span><span class="sxs-lookup"><span data-stu-id="65c75-123">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="65c75-124"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="65c75-124"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="65c75-125">La balise BER-TLV (2 octets) dans P1-P2</span><span class="sxs-lookup"><span data-stu-id="65c75-125">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="65c75-126">*byP2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65c75-126">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65c75-127">Paramètres.</span><span class="sxs-lookup"><span data-stu-id="65c75-127">Parameters.</span></span>



| <span data-ttu-id="65c75-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="65c75-128">Value</span></span>                                                                                  | <span data-ttu-id="65c75-129">Signification</span><span class="sxs-lookup"><span data-stu-id="65c75-129">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="65c75-130"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="65c75-130"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="65c75-131">RFU</span><span class="sxs-lookup"><span data-stu-id="65c75-131">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="65c75-132"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="65c75-132"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="65c75-133">La balise BER-TLV (1 octet) dans P2</span><span class="sxs-lookup"><span data-stu-id="65c75-133">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="65c75-134"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="65c75-134"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="65c75-135">Données d’application (codage propriétaire)</span><span class="sxs-lookup"><span data-stu-id="65c75-135">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="65c75-136"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="65c75-136"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="65c75-137">Balise SIMPLE-TLV dans P2</span><span class="sxs-lookup"><span data-stu-id="65c75-137">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="65c75-138"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="65c75-138"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="65c75-139">RFU</span><span class="sxs-lookup"><span data-stu-id="65c75-139">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="65c75-140"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="65c75-140"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="65c75-141">La balise BER-TLV (2 octets) dans P1-P2</span><span class="sxs-lookup"><span data-stu-id="65c75-141">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="65c75-142">*lBytesToGet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65c75-142">*lBytesToGet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65c75-143">Nombre d’octets attendus dans la réponse.</span><span class="sxs-lookup"><span data-stu-id="65c75-143">Number of bytes expected in the response.</span></span>

</dd> <dt>

<span data-ttu-id="65c75-144">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="65c75-144">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="65c75-145">En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.</span><span class="sxs-lookup"><span data-stu-id="65c75-145">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="65c75-146">Au retour, elle est remplie avec la commande APDU construite par cette opération.</span><span class="sxs-lookup"><span data-stu-id="65c75-146">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="65c75-147">Si *ppCmd* a été défini **sur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé en interne et retourné à l’aide du pointeur *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="65c75-147">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65c75-148">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65c75-148">Return value</span></span>

<span data-ttu-id="65c75-149">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="65c75-149">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="65c75-150">Code de retour</span><span class="sxs-lookup"><span data-stu-id="65c75-150">Return code</span></span>                                                                                   | <span data-ttu-id="65c75-151">Description</span><span class="sxs-lookup"><span data-stu-id="65c75-151">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="65c75-152"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="65c75-152"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="65c75-153">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="65c75-153">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="65c75-154"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="65c75-154"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="65c75-155">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="65c75-155">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="65c75-156"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="65c75-156"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="65c75-157">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="65c75-157">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="65c75-158"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="65c75-158"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="65c75-159">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="65c75-159">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="65c75-160">Notes</span><span class="sxs-lookup"><span data-stu-id="65c75-160">Remarks</span></span>

<span data-ttu-id="65c75-161">La commande encapsulée ne peut être exécutée que si l’état de sécurité de la [*carte à puce*](../secgloss/s-gly.md) répond aux attributs de sécurité du fichier élémentaire en cours de lecture.</span><span class="sxs-lookup"><span data-stu-id="65c75-161">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being read.</span></span> <span data-ttu-id="65c75-162">Les conditions de sécurité dépendent de la stratégie de la carte et peuvent être manipulées par le biais de [**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md), [**InternalAuthenticate**](iscardiso7816-internalauthenticate.md), [**ISCardAuth**](iscardauth.md), etc.</span><span class="sxs-lookup"><span data-stu-id="65c75-162">Security conditions are dependent on the policy of the card, and may be manipulated through [**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md), [**InternalAuthenticate**](iscardiso7816-internalauthenticate.md), [**ISCardAuth**](iscardauth.md), and so on.</span></span>

<span data-ttu-id="65c75-163">Pour sélectionner un fichier, appelez [**SelectFile**](iscardiso7816-selectfile.md).</span><span class="sxs-lookup"><span data-stu-id="65c75-163">To select a file, call [**SelectFile**](iscardiso7816-selectfile.md).</span></span>

<span data-ttu-id="65c75-164">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="65c75-164">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="65c75-165">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="65c75-165">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="65c75-166">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="65c75-166">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="65c75-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65c75-167">Requirements</span></span>



| <span data-ttu-id="65c75-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65c75-168">Requirement</span></span> | <span data-ttu-id="65c75-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="65c75-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65c75-170">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65c75-170">Minimum supported client</span></span><br/> | <span data-ttu-id="65c75-171">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65c75-171">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="65c75-172">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65c75-172">Minimum supported server</span></span><br/> | <span data-ttu-id="65c75-173">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65c75-173">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="65c75-174">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="65c75-174">End of client support</span></span><br/>    | <span data-ttu-id="65c75-175">Windows XP</span><span class="sxs-lookup"><span data-stu-id="65c75-175">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="65c75-176">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="65c75-176">End of server support</span></span><br/>    | <span data-ttu-id="65c75-177">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="65c75-177">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="65c75-178">En-tête</span><span class="sxs-lookup"><span data-stu-id="65c75-178">Header</span></span><br/>                   | <dl> <span data-ttu-id="65c75-179"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="65c75-179"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="65c75-180">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="65c75-180">Type library</span></span><br/>             | <dl> <span data-ttu-id="65c75-181"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="65c75-181"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="65c75-182">DLL</span><span class="sxs-lookup"><span data-stu-id="65c75-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65c75-183"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65c75-183"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="65c75-184">IID</span><span class="sxs-lookup"><span data-stu-id="65c75-184">IID</span></span><br/>                      | <span data-ttu-id="65c75-185">IID \_ ISCardISO7816 est défini en tant que 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="65c75-185">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="65c75-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65c75-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65c75-187">**ExternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="65c75-187">**ExternalAuthenticate**</span></span>](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="65c75-188">**InternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="65c75-188">**InternalAuthenticate**</span></span>](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="65c75-189">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="65c75-189">**ISCardAuth**</span></span>](iscardauth.md)
</dt> <dt>

[<span data-ttu-id="65c75-190">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="65c75-190">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="65c75-191">**PutData**</span><span class="sxs-lookup"><span data-stu-id="65c75-191">**PutData**</span></span>](iscardiso7816-putdata.md)
</dt> <dt>

[<span data-ttu-id="65c75-192">**SelectFile**</span><span class="sxs-lookup"><span data-stu-id="65c75-192">**SelectFile**</span></span>](iscardiso7816-selectfile.md)
</dt> </dl>

 

 
