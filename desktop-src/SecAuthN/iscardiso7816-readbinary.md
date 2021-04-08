---
description: La méthode ReadBinary construit une commande APDU (Application Protocol Data Unit) qui acquiert un message de réponse qui donne cette partie du contenu d’un fichier élémentaire structuré de manière transparente.
ms.assetid: 15394c21-1e07-4ea1-8f11-817e07b31f9b
title: 'ISCardISO7816 :: ReadBinary, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a29093d8725a3390df9837f4e2f395cfcf2eef29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867846"
---
# <a name="iscardiso7816readbinary-method"></a><span data-ttu-id="69271-103">ISCardISO7816 :: ReadBinary, méthode</span><span class="sxs-lookup"><span data-stu-id="69271-103">ISCardISO7816::ReadBinary method</span></span>

<span data-ttu-id="69271-104">\[La méthode **readBinary** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="69271-104">\[The **ReadBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="69271-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="69271-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="69271-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="69271-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="69271-107">La méthode **readBinary** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui acquiert un message de réponse qui donne cette partie du contenu d’un fichier élémentaire structuré de manière transparente.</span><span class="sxs-lookup"><span data-stu-id="69271-107">The **ReadBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that acquires a response message that gives that part of the contents of a transparent-structured elementary file.</span></span>

## <a name="syntax"></a><span data-ttu-id="69271-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69271-108">Syntax</span></span>


```C++
HRESULT ReadBinary(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="69271-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69271-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69271-110">*byP1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69271-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69271-111">Le champ P1-P2, décalé vers le premier octet à lire à partir du début du fichier.</span><span class="sxs-lookup"><span data-stu-id="69271-111">The P1-P2 field, offset to the first byte to be read from the beginning of the file.</span></span> <span data-ttu-id="69271-112">Si B8 = 1 dans P1, alors B7 et B6 de P1 ont la valeur zéro (RFU bits), B5 à B1 pour P1 est un identificateur EF bref et P2 est le décalage du premier octet à lire dans les unités de données à partir du début du fichier.</span><span class="sxs-lookup"><span data-stu-id="69271-112">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span> <span data-ttu-id="69271-113">Si B8 = 0 dans P1, P1 \| \| P2 est le décalage du premier octet à lire dans les unités de données à partir du début du fichier.</span><span class="sxs-lookup"><span data-stu-id="69271-113">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="69271-114">*byP2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69271-114">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69271-115">Le champ P1-P2, décalé vers le premier octet à lire à partir du début du fichier.</span><span class="sxs-lookup"><span data-stu-id="69271-115">The P1-P2 field, offset to the first byte to be read from the beginning of the file.</span></span> <span data-ttu-id="69271-116">Si B8 = 1 dans P1, alors B7 et B6 de P1 ont la valeur zéro (RFU bits), B5 à B1 pour P1 est un identificateur EF bref et P2 est le décalage du premier octet à lire dans les unités de données à partir du début du fichier.</span><span class="sxs-lookup"><span data-stu-id="69271-116">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span> <span data-ttu-id="69271-117">Si B8 = 0 dans P1, P1 \| \| P2 est le décalage du premier octet à lire dans les unités de données à partir du début du fichier.</span><span class="sxs-lookup"><span data-stu-id="69271-117">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="69271-118">*lBytesToRead* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69271-118">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69271-119">Nombre d’octets à lire à partir du EF transparent.</span><span class="sxs-lookup"><span data-stu-id="69271-119">Number of bytes to read from the transparent EF.</span></span>

<span data-ttu-id="69271-120">Si le champ le contient uniquement des zéros, alors dans la limite de 256 pour la longueur brève ou 65536 pour la longueur étendue, tous les octets jusqu’à la fin du fichier doivent être lus.</span><span class="sxs-lookup"><span data-stu-id="69271-120">If the Le field contains only zeros, then within the limit of 256 for short length or 65536 for extended length, all the bytes until the end of the file should be read.</span></span>

</dd> <dt>

<span data-ttu-id="69271-121">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="69271-121">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="69271-122">En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.</span><span class="sxs-lookup"><span data-stu-id="69271-122">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="69271-123">Au retour, elle est remplie avec la commande APDU construite par cette opération.</span><span class="sxs-lookup"><span data-stu-id="69271-123">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="69271-124">Si *ppCmd* a été défini **sur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé en interne et retourné à l’aide du pointeur *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="69271-124">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69271-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="69271-125">Return value</span></span>

<span data-ttu-id="69271-126">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="69271-126">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="69271-127">Code de retour</span><span class="sxs-lookup"><span data-stu-id="69271-127">Return code</span></span>                                                                                   | <span data-ttu-id="69271-128">Description</span><span class="sxs-lookup"><span data-stu-id="69271-128">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="69271-129"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="69271-129"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="69271-130">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="69271-130">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="69271-131"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="69271-131"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="69271-132">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="69271-132">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="69271-133"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="69271-133"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="69271-134">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="69271-134">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="69271-135"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="69271-135"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="69271-136">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="69271-136">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="69271-137">Notes</span><span class="sxs-lookup"><span data-stu-id="69271-137">Remarks</span></span>

<span data-ttu-id="69271-138">La commande encapsulée ne peut être exécutée que si l’état de sécurité de la [*carte à puce*](../secgloss/s-gly.md) répond aux attributs de sécurité du fichier élémentaire en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="69271-138">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="69271-139">Lorsque la commande contient un identificateur élémentaire Short valide, elle définit le fichier en tant que fichier élémentaire actuel.</span><span class="sxs-lookup"><span data-stu-id="69271-139">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="69271-140">Les fichiers élémentaires sans structure transparente ne peuvent pas être effacés.</span><span class="sxs-lookup"><span data-stu-id="69271-140">Elementary files without a transparent structure cannot be erased.</span></span> <span data-ttu-id="69271-141">La commande encapsulée est abandonnée si elle est appliquée à un fichier élémentaire sans structure transparente.</span><span class="sxs-lookup"><span data-stu-id="69271-141">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="69271-142">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="69271-142">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="69271-143">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="69271-143">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="69271-144">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="69271-144">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="69271-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69271-145">Requirements</span></span>



| <span data-ttu-id="69271-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69271-146">Requirement</span></span> | <span data-ttu-id="69271-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="69271-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69271-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69271-148">Minimum supported client</span></span><br/> | <span data-ttu-id="69271-149">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69271-149">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="69271-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69271-150">Minimum supported server</span></span><br/> | <span data-ttu-id="69271-151">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69271-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="69271-152">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="69271-152">End of client support</span></span><br/>    | <span data-ttu-id="69271-153">Windows XP</span><span class="sxs-lookup"><span data-stu-id="69271-153">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="69271-154">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="69271-154">End of server support</span></span><br/>    | <span data-ttu-id="69271-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="69271-155">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="69271-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="69271-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="69271-157"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="69271-157"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="69271-158">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="69271-158">Type library</span></span><br/>             | <dl> <span data-ttu-id="69271-159"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="69271-159"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="69271-160">DLL</span><span class="sxs-lookup"><span data-stu-id="69271-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69271-161"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69271-161"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="69271-162">IID</span><span class="sxs-lookup"><span data-stu-id="69271-162">IID</span></span><br/>                      | <span data-ttu-id="69271-163">IID \_ ISCardISO7816 est défini en tant que 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="69271-163">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="69271-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69271-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69271-165">**EraseBinary**</span><span class="sxs-lookup"><span data-stu-id="69271-165">**EraseBinary**</span></span>](iscardiso7816-erasebinary.md)
</dt> <dt>

[<span data-ttu-id="69271-166">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="69271-166">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="69271-167">**UpdateBinary**</span><span class="sxs-lookup"><span data-stu-id="69271-167">**UpdateBinary**</span></span>](iscardiso7816-updatebinary.md)
</dt> <dt>

[<span data-ttu-id="69271-168">**WriteBinary**</span><span class="sxs-lookup"><span data-stu-id="69271-168">**WriteBinary**</span></span>](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
