---
description: La méthode WriteBinary construit une commande APDU (Application Protocol Data Unit) qui écrit des valeurs binaires dans un fichier élémentaire.
ms.assetid: e38273d5-4eb0-4c0b-829a-c78e511a38bc
title: 'ISCardISO7816 :: WriteBinary, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 330e817bc501c451026589087991fb43c0b5ac57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950949"
---
# <a name="iscardiso7816writebinary-method"></a><span data-ttu-id="06e9b-103">ISCardISO7816 :: WriteBinary, méthode</span><span class="sxs-lookup"><span data-stu-id="06e9b-103">ISCardISO7816::WriteBinary method</span></span>

<span data-ttu-id="06e9b-104">\[La méthode **writeBinary** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="06e9b-104">\[The **WriteBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="06e9b-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="06e9b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="06e9b-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="06e9b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="06e9b-107">La méthode **writeBinary** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui écrit des valeurs binaires dans un fichier élémentaire.</span><span class="sxs-lookup"><span data-stu-id="06e9b-107">The **WriteBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that writes binary values into an elementary file.</span></span>

<span data-ttu-id="06e9b-108">En fonction des attributs de fichier, la commande effectue l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="06e9b-108">Depending upon the file attributes, the command performs one of the following operations:</span></span>

-   <span data-ttu-id="06e9b-109">Le ou logique des bits déjà présents dans la carte avec les bits indiqués dans la commande APDU (l’État effacé logique des bits du fichier est 0).</span><span class="sxs-lookup"><span data-stu-id="06e9b-109">The logical OR of the bits already present in the card with the bits given in the command APDU (logical erased state of the bits of the file is 0).</span></span>
-   <span data-ttu-id="06e9b-110">Le AND logique des bits déjà présents dans la carte avec les bits indiqués dans la commande APDU (l’État effacé logique des bits du fichier est 1).</span><span class="sxs-lookup"><span data-stu-id="06e9b-110">The logical AND of the bits already present in the card with the bits given in the command APDU (logical erased state of the bits of the file is 1).</span></span>
-   <span data-ttu-id="06e9b-111">Écriture unique dans la carte des bits donnée dans la commande APDU.</span><span class="sxs-lookup"><span data-stu-id="06e9b-111">The one-time write in the card of the bits given in the command APDU.</span></span>

<span data-ttu-id="06e9b-112">Si aucune indication n’est donnée dans l’octet de codage des données, le comportement logique ou s’applique.</span><span class="sxs-lookup"><span data-stu-id="06e9b-112">When no indication is given in the data coding byte, the logical OR behavior applies.</span></span>

## <a name="syntax"></a><span data-ttu-id="06e9b-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06e9b-113">Syntax</span></span>


```C++
HRESULT WriteBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="06e9b-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06e9b-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06e9b-115">*byP1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06e9b-115">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06e9b-116">Décalage à l’emplacement d’écriture à partir du début du fichier binaire (EF).</span><span class="sxs-lookup"><span data-stu-id="06e9b-116">Offset to the write location from the beginning of the binary file (EF).</span></span> <span data-ttu-id="06e9b-117">Si B8 = 1 dans P1, alors B7 et B6 de P1 ont la valeur zéro (RFU bits), B5 à B1 pour P1 est un identificateur EF bref et P2 est le décalage du premier octet à écrire dans les unités de données à partir du début du fichier.</span><span class="sxs-lookup"><span data-stu-id="06e9b-117">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span> <span data-ttu-id="06e9b-118">Si B8 = 0 dans P1, P1 \| \| P2 est le décalage du premier octet à écrire dans les unités de données à partir du début du fichier.</span><span class="sxs-lookup"><span data-stu-id="06e9b-118">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="06e9b-119">*byP2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06e9b-119">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06e9b-120">Décalage à l’emplacement d’écriture à partir du début du fichier binaire (EF).</span><span class="sxs-lookup"><span data-stu-id="06e9b-120">Offset to the write location from the beginning of the binary file (EF).</span></span> <span data-ttu-id="06e9b-121">Si B8 = 1 dans P1, alors B7 et B6 de P1 ont la valeur zéro (RFU bits), B5 à B1 pour P1 est un identificateur EF bref et P2 est le décalage du premier octet à écrire dans les unités de données à partir du début du fichier.</span><span class="sxs-lookup"><span data-stu-id="06e9b-121">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span> <span data-ttu-id="06e9b-122">Si B8 = 0 dans P1, P1 \| \| P2 est le décalage du premier octet à écrire dans les unités de données à partir du début du fichier.</span><span class="sxs-lookup"><span data-stu-id="06e9b-122">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="06e9b-123">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06e9b-123">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06e9b-124">Pointeur vers la chaîne d’unités de données à écrire.</span><span class="sxs-lookup"><span data-stu-id="06e9b-124">Pointer to the string of data units to be written.</span></span>

</dd> <dt>

<span data-ttu-id="06e9b-125">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="06e9b-125">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="06e9b-126">En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.</span><span class="sxs-lookup"><span data-stu-id="06e9b-126">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="06e9b-127">Au retour, elle est remplie avec la commande APDU construite par cette opération.</span><span class="sxs-lookup"><span data-stu-id="06e9b-127">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="06e9b-128">Si *ppCmd* a été défini avec la **valeur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé et retourné en interne par le biais du pointeur *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="06e9b-128">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06e9b-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06e9b-129">Return value</span></span>

<span data-ttu-id="06e9b-130">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="06e9b-130">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="06e9b-131">Code de retour</span><span class="sxs-lookup"><span data-stu-id="06e9b-131">Return code</span></span>                                                                                   | <span data-ttu-id="06e9b-132">Description</span><span class="sxs-lookup"><span data-stu-id="06e9b-132">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="06e9b-133"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="06e9b-133"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="06e9b-134">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="06e9b-134">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="06e9b-135"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="06e9b-135"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="06e9b-136">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="06e9b-136">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="06e9b-137"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="06e9b-137"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="06e9b-138">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="06e9b-138">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="06e9b-139"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="06e9b-139"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="06e9b-140">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="06e9b-140">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="06e9b-141">Notes</span><span class="sxs-lookup"><span data-stu-id="06e9b-141">Remarks</span></span>

<span data-ttu-id="06e9b-142">La commande encapsulée ne peut être exécutée que si l’état de sécurité de la [*carte à puce*](../secgloss/s-gly.md) répond aux attributs de sécurité du fichier élémentaire en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="06e9b-142">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="06e9b-143">Lorsque la commande contient un identificateur élémentaire Short valide, elle définit le fichier en tant que fichier élémentaire actuel.</span><span class="sxs-lookup"><span data-stu-id="06e9b-143">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="06e9b-144">Lorsqu’une opération d’écriture binaire a été appliquée à une unité de données d’un EF d’écriture unique, toute opération d’écriture faisant référence à cette unité de données est abandonnée si le contenu de l’unité de données ou l’indicateur d’État effacé logique (le cas échéant) attaché à cette unité de données est différent de l’État effacé logique.</span><span class="sxs-lookup"><span data-stu-id="06e9b-144">When a write binary operation has been applied to a data unit of a one-time write EF, any further write operation referring to this data unit will be aborted if the content of the data unit or the logical erased state indicator (if any) attached to this data unit is different from the logical erased state.</span></span>

<span data-ttu-id="06e9b-145">Impossible d’écrire dans les fichiers élémentaires sans structure transparente.</span><span class="sxs-lookup"><span data-stu-id="06e9b-145">Elementary files without a transparent structure cannot be written to.</span></span> <span data-ttu-id="06e9b-146">La commande encapsulée est abandonnée si elle est appliquée à un fichier élémentaire sans structure transparente.</span><span class="sxs-lookup"><span data-stu-id="06e9b-146">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="06e9b-147">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="06e9b-147">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="06e9b-148">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="06e9b-148">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="06e9b-149">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="06e9b-149">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="06e9b-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06e9b-150">Requirements</span></span>



| <span data-ttu-id="06e9b-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06e9b-151">Requirement</span></span> | <span data-ttu-id="06e9b-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="06e9b-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06e9b-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06e9b-153">Minimum supported client</span></span><br/> | <span data-ttu-id="06e9b-154">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06e9b-154">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="06e9b-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06e9b-155">Minimum supported server</span></span><br/> | <span data-ttu-id="06e9b-156">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06e9b-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="06e9b-157">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="06e9b-157">End of client support</span></span><br/>    | <span data-ttu-id="06e9b-158">Windows XP</span><span class="sxs-lookup"><span data-stu-id="06e9b-158">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="06e9b-159">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="06e9b-159">End of server support</span></span><br/>    | <span data-ttu-id="06e9b-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="06e9b-160">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="06e9b-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="06e9b-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="06e9b-162"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="06e9b-162"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="06e9b-163">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="06e9b-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="06e9b-164"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="06e9b-164"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="06e9b-165">DLL</span><span class="sxs-lookup"><span data-stu-id="06e9b-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06e9b-166"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06e9b-166"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="06e9b-167">IID</span><span class="sxs-lookup"><span data-stu-id="06e9b-167">IID</span></span><br/>                      | <span data-ttu-id="06e9b-168">IID \_ ISCardISO7816 est défini en tant que 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="06e9b-168">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="06e9b-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06e9b-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06e9b-170">**EraseBinary**</span><span class="sxs-lookup"><span data-stu-id="06e9b-170">**EraseBinary**</span></span>](iscardiso7816-erasebinary.md)
</dt> <dt>

[<span data-ttu-id="06e9b-171">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="06e9b-171">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="06e9b-172">**ReadBinary**</span><span class="sxs-lookup"><span data-stu-id="06e9b-172">**ReadBinary**</span></span>](iscardiso7816-readbinary.md)
</dt> <dt>

[<span data-ttu-id="06e9b-173">**UpdateBinary**</span><span class="sxs-lookup"><span data-stu-id="06e9b-173">**UpdateBinary**</span></span>](iscardiso7816-updatebinary.md)
</dt> </dl>

 

 
