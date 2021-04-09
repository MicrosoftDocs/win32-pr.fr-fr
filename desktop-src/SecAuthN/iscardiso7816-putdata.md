---
description: La méthode PutData construit une commande APDU (Application Protocol Data Unit) qui stocke un objet de données primitif unique ou le jeu d’objets de données contenu dans un objet de données construit, en fonction du fichier sélectionné.
ms.assetid: 6bad45fb-b202-4eb0-b2f4-fe0a6af64330
title: ISCardISO7816 ::P méthode utData (scardssp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.PutData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 3c15239943a92067011011b6cedca191fa78c3a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866997"
---
# <a name="iscardiso7816putdata-method"></a><span data-ttu-id="e158b-103">ISCardISO7816 ::P méthode utData</span><span class="sxs-lookup"><span data-stu-id="e158b-103">ISCardISO7816::PutData method</span></span>

<span data-ttu-id="e158b-104">\[La méthode **PutData** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="e158b-104">\[The **PutData** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e158b-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e158b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e158b-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="e158b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="e158b-107">La méthode **PutData** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui stocke un objet de données primitif unique ou le jeu d’objets de données contenu dans un objet de données construit, en fonction du fichier sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e158b-107">The **PutData** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that stores a single primitive data object or the set of data objects contained in a constructed data object, depending on the file selected.</span></span>

<span data-ttu-id="e158b-108">La façon dont les objets sont stockés (écriture unique et/ou mise à jour et/ou ajout) dépend de la définition ou de la nature des objets de données.</span><span class="sxs-lookup"><span data-stu-id="e158b-108">How the objects are stored (writing once and/or updating and/or appending) depends on the definition or the nature of the data objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="e158b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e158b-109">Syntax</span></span>


```C++
HRESULT PutData(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="e158b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e158b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e158b-111">*byP1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e158b-111">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e158b-112">Codage de P1-P2.</span><span class="sxs-lookup"><span data-stu-id="e158b-112">Coding of P1-P2.</span></span>



| <span data-ttu-id="e158b-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="e158b-113">Value</span></span>                                                                                  | <span data-ttu-id="e158b-114">Signification</span><span class="sxs-lookup"><span data-stu-id="e158b-114">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="e158b-115"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-115"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="e158b-116">RFU</span><span class="sxs-lookup"><span data-stu-id="e158b-116">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="e158b-117"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-117"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="e158b-118">La balise BER-TLV (1 octet) dans P2</span><span class="sxs-lookup"><span data-stu-id="e158b-118">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="e158b-119"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-119"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="e158b-120">Données d’application (codage propriétaire)</span><span class="sxs-lookup"><span data-stu-id="e158b-120">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="e158b-121"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-121"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="e158b-122">Balise SIMPLE-TLV dans P2</span><span class="sxs-lookup"><span data-stu-id="e158b-122">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="e158b-123"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-123"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="e158b-124">RFU</span><span class="sxs-lookup"><span data-stu-id="e158b-124">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="e158b-125"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-125"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="e158b-126">La balise BER-TLV (2 octets) dans P1-P2</span><span class="sxs-lookup"><span data-stu-id="e158b-126">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="e158b-127">*byP2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e158b-127">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e158b-128">Codage de P1-P2.</span><span class="sxs-lookup"><span data-stu-id="e158b-128">Coding of P1-P2.</span></span>



| <span data-ttu-id="e158b-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="e158b-129">Value</span></span>                                                                                  | <span data-ttu-id="e158b-130">Signification</span><span class="sxs-lookup"><span data-stu-id="e158b-130">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="e158b-131"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-131"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="e158b-132">RFU</span><span class="sxs-lookup"><span data-stu-id="e158b-132">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="e158b-133"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-133"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="e158b-134">La balise BER-TLV (1 octet) dans P2</span><span class="sxs-lookup"><span data-stu-id="e158b-134">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="e158b-135"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-135"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="e158b-136">Données d’application (codage propriétaire)</span><span class="sxs-lookup"><span data-stu-id="e158b-136">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="e158b-137"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-137"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="e158b-138">Balise SIMPLE-TLV dans P2</span><span class="sxs-lookup"><span data-stu-id="e158b-138">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="e158b-139"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-139"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="e158b-140">RFU</span><span class="sxs-lookup"><span data-stu-id="e158b-140">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="e158b-141"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-141"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="e158b-142">La balise BER-TLV (2 octets) dans P1-P2</span><span class="sxs-lookup"><span data-stu-id="e158b-142">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="e158b-143">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e158b-143">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e158b-144">Pointeur vers une mémoire tampon d’octets qui contient les paramètres et les données à écrire.</span><span class="sxs-lookup"><span data-stu-id="e158b-144">Pointer to a byte buffer that contains the parameters and data to be written.</span></span>

</dd> <dt>

<span data-ttu-id="e158b-145">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e158b-145">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e158b-146">En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.</span><span class="sxs-lookup"><span data-stu-id="e158b-146">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="e158b-147">Au retour, elle est remplie avec la commande APDU construite par cette opération.</span><span class="sxs-lookup"><span data-stu-id="e158b-147">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="e158b-148">Si *ppCmd* a été défini **sur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé en interne et retourné à l’aide du pointeur *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="e158b-148">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e158b-149">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e158b-149">Return value</span></span>

<span data-ttu-id="e158b-150">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="e158b-150">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="e158b-151">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e158b-151">Return code</span></span>                                                                                   | <span data-ttu-id="e158b-152">Description</span><span class="sxs-lookup"><span data-stu-id="e158b-152">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e158b-153"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-153"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e158b-154">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="e158b-154">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="e158b-155"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-155"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e158b-156">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="e158b-156">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="e158b-157"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-157"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e158b-158">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="e158b-158">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="e158b-159"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-159"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e158b-160">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="e158b-160">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="e158b-161">Notes</span><span class="sxs-lookup"><span data-stu-id="e158b-161">Remarks</span></span>

<span data-ttu-id="e158b-162">La commande ne peut être exécutée que si l’état de sécurité répond aux conditions de sécurité définies par l’application dans le [*contexte*](../secgloss/c-gly.md) de la fonction.</span><span class="sxs-lookup"><span data-stu-id="e158b-162">The command can be performed only if the security status satisfies the security conditions defined by the application within the [*context*](../secgloss/c-gly.md) for the function.</span></span>

<dl> <dt>

<span data-ttu-id="e158b-163"><span id="Store_Application_Data"></span><span id="store_application_data"></span><span id="STORE_APPLICATION_DATA"></span>Stocker les données d’application</span><span class="sxs-lookup"><span data-stu-id="e158b-163"><span id="Store_Application_Data"></span><span id="store_application_data"></span><span id="STORE_APPLICATION_DATA"></span>Store Application Data</span></span>
</dt> <dd>

<span data-ttu-id="e158b-164">Lorsque la valeur de P1-P2 se situe dans la plage comprise entre 0100 et 01FF, la valeur P1-P2 est un identificateur réservé aux tests internes de carte et aux services propriétaires explicites dans un contexte d’application donné.</span><span class="sxs-lookup"><span data-stu-id="e158b-164">When the value of P1-P2 lies in the range from 0100 to 01FF, the value of P1-P2 shall be an identifier reserved for card internal tests and for proprietary services meaningful within a given application context.</span></span>

</dd> <dt>

<span data-ttu-id="e158b-165"><span id="Store_Data_Objects"></span><span id="store_data_objects"></span><span id="STORE_DATA_OBJECTS"></span>Stocker des objets de données</span><span class="sxs-lookup"><span data-stu-id="e158b-165"><span id="Store_Data_Objects"></span><span id="store_data_objects"></span><span id="STORE_DATA_OBJECTS"></span>Store Data Objects</span></span>
</dt> <dd>

<span data-ttu-id="e158b-166">Lorsque la valeur P1-P2 se trouve dans la plage comprise entre 0040 et 00FF, la valeur de P2 doit être une balise BER-TLV sur un octet unique.</span><span class="sxs-lookup"><span data-stu-id="e158b-166">When the value P1-P2 lies in the range from 0040 to 00FF, the value of P2 shall be a BER-TLV tag on a single byte.</span></span> <span data-ttu-id="e158b-167">La valeur de 00FF est réservée pour indiquer que le champ de données contient des objets de données BER-TLV.</span><span class="sxs-lookup"><span data-stu-id="e158b-167">The value of 00FF is reserved for indicating that the data field carries BER-TLV data objects.</span></span>

<span data-ttu-id="e158b-168">Lorsque la valeur de P1-P2 se situe dans la plage 0200 à 02FF, la valeur de P2 doit être une balise SIMPLE-TLV.</span><span class="sxs-lookup"><span data-stu-id="e158b-168">When the value of P1-P2 lies in the range 0200 to 02FF, the value of P2 shall be a SIMPLE-TLV tag.</span></span> <span data-ttu-id="e158b-169">La valeur 0200 est RFU.</span><span class="sxs-lookup"><span data-stu-id="e158b-169">The value 0200 is RFU.</span></span> <span data-ttu-id="e158b-170">La valeur 02FF est réservée pour indiquer que le champ de données contient des objets de données simples-TLV.</span><span class="sxs-lookup"><span data-stu-id="e158b-170">The value 02FF is reserved for indicating that the data field carries SIMPLE-TLV data objects.</span></span>

<span data-ttu-id="e158b-171">Lorsque la valeur de P1-P2 se situe dans la plage comprise entre 4000 et FFFF, la valeur P1-P2 doit être une balise BER-TLV sur deux octets.</span><span class="sxs-lookup"><span data-stu-id="e158b-171">When the value of P1-P2 lies in the range from 4000 to FFFF, the value of P1-P2 shall be a BER-TLV tag on two bytes.</span></span> <span data-ttu-id="e158b-172">Les valeurs 4000 à FFFF sont RFU.</span><span class="sxs-lookup"><span data-stu-id="e158b-172">The values 4000 to FFFF are RFU.</span></span>

<span data-ttu-id="e158b-173">Lorsqu’un objet de données primitif est fourni, le champ de données du message de commande doit contenir la valeur de l’objet de données primitif correspondant.</span><span class="sxs-lookup"><span data-stu-id="e158b-173">When a primitive data object is provided, the data field of the command message shall contain the value of the corresponding primitive data object.</span></span>

<span data-ttu-id="e158b-174">Lorsqu’un objet de données construit est fourni, le champ de données du message de commande doit contenir la valeur de l’objet de données construit (autrement dit, les objets de données, y compris leur balise, leur longueur et leur valeur).</span><span class="sxs-lookup"><span data-stu-id="e158b-174">When a constructed data object is provided, the data field of the command message shall contain the value of the constructed data object (that is, data objects including their tag, length, and value).</span></span>

</dd> </dl>

<span data-ttu-id="e158b-175">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="e158b-175">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="e158b-176">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="e158b-176">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="e158b-177">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="e158b-177">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e158b-178">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e158b-178">Requirements</span></span>



| <span data-ttu-id="e158b-179">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e158b-179">Requirement</span></span> | <span data-ttu-id="e158b-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="e158b-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e158b-181">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e158b-181">Minimum supported client</span></span><br/> | <span data-ttu-id="e158b-182">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e158b-182">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e158b-183">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e158b-183">Minimum supported server</span></span><br/> | <span data-ttu-id="e158b-184">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e158b-184">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e158b-185">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e158b-185">End of client support</span></span><br/>    | <span data-ttu-id="e158b-186">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e158b-186">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="e158b-187">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="e158b-187">End of server support</span></span><br/>    | <span data-ttu-id="e158b-188">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e158b-188">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="e158b-189">En-tête</span><span class="sxs-lookup"><span data-stu-id="e158b-189">Header</span></span><br/>                   | <dl> <span data-ttu-id="e158b-190"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-190"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e158b-191">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e158b-191">Type library</span></span><br/>             | <dl> <span data-ttu-id="e158b-192"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-192"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e158b-193">DLL</span><span class="sxs-lookup"><span data-stu-id="e158b-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e158b-194"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-194"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e158b-195">IID</span><span class="sxs-lookup"><span data-stu-id="e158b-195">IID</span></span><br/>                      | <span data-ttu-id="e158b-196">IID \_ ISCardISO7816 est défini en tant que 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="e158b-196">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="e158b-197">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e158b-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e158b-198">**GetData**</span><span class="sxs-lookup"><span data-stu-id="e158b-198">**GetData**</span></span>](iscardiso7816-getdata.md)
</dt> <dt>

[<span data-ttu-id="e158b-199">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="e158b-199">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
