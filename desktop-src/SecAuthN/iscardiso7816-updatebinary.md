---
description: La méthode UpdateBinary construit une commande APDU (Application Protocol Data Unit) qui met à jour les bits présents dans un fichier élémentaire avec les bits fournis dans la commande APDU.
ms.assetid: 14ac6ad9-efcf-48ea-8712-19caeee47521
title: 'ISCardISO7816 :: UpdateBinary, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.UpdateBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d9651189cab228eaa5dacc9c2f5963201bbc65c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519949"
---
# <a name="iscardiso7816updatebinary-method"></a><span data-ttu-id="6f39a-103">ISCardISO7816 :: UpdateBinary, méthode</span><span class="sxs-lookup"><span data-stu-id="6f39a-103">ISCardISO7816::UpdateBinary method</span></span>

<span data-ttu-id="6f39a-104">\[La méthode **UpdateBinary** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="6f39a-104">\[The **UpdateBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6f39a-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6f39a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6f39a-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="6f39a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6f39a-107">La méthode **UpdateBinary** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui met à jour les bits présents dans un fichier élémentaire avec les bits fournis dans la commande APDU.</span><span class="sxs-lookup"><span data-stu-id="6f39a-107">The **UpdateBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that updates the bits present in an elementary file with the bits given in the APDU command.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f39a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f39a-108">Syntax</span></span>


```C++
HRESULT UpdateBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="6f39a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f39a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f39a-110">*byP1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f39a-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f39a-111">Offset à l’emplacement d’écriture (mise à jour) dans le binaire à partir du début du binaire.</span><span class="sxs-lookup"><span data-stu-id="6f39a-111">Offset to the write (update) location into the binary from the start of the binary.</span></span> <span data-ttu-id="6f39a-112">Si B8 = 1 dans P1, alors B7 et B6 de P1 ont la valeur zéro (RFU bits), B5 à B1 pour P1 est un identificateur EF bref et P2 est le décalage du premier octet à mettre à jour dans les unités de données à partir du début du fichier.</span><span class="sxs-lookup"><span data-stu-id="6f39a-112">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span> <span data-ttu-id="6f39a-113">Si B8 = 0 dans P1, P1 \| \| P2 est le décalage du premier octet à mettre à jour dans les unités de données à partir du début du fichier.</span><span class="sxs-lookup"><span data-stu-id="6f39a-113">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="6f39a-114">*byP2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f39a-114">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f39a-115">Offset à l’emplacement d’écriture (mise à jour) dans le binaire à partir du début du binaire.</span><span class="sxs-lookup"><span data-stu-id="6f39a-115">Offset to the write (update) location into the binary from the start of the binary.</span></span> <span data-ttu-id="6f39a-116">Si B8 = 1 dans P1, alors B7 et B6 de P1 ont la valeur zéro (RFU bits), B5 à B1 pour P1 est un identificateur EF bref et P2 est le décalage du premier octet à mettre à jour dans les unités de données à partir du début du fichier.</span><span class="sxs-lookup"><span data-stu-id="6f39a-116">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span> <span data-ttu-id="6f39a-117">Si B8 = 0 dans P1, P1 \| \| P2 est le décalage du premier octet à mettre à jour dans les unités de données à partir du début du fichier.</span><span class="sxs-lookup"><span data-stu-id="6f39a-117">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="6f39a-118">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f39a-118">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f39a-119">Pointeur vers la chaîne d’unités de données à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="6f39a-119">Pointer to the string of data units to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="6f39a-120">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6f39a-120">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f39a-121">En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.</span><span class="sxs-lookup"><span data-stu-id="6f39a-121">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="6f39a-122">Au retour, elle est remplie avec la commande APDU construite par cette opération.</span><span class="sxs-lookup"><span data-stu-id="6f39a-122">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="6f39a-123">Si *ppCmd* a été défini **sur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé en interne et retourné à l’aide du pointeur *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="6f39a-123">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f39a-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6f39a-124">Return value</span></span>

<span data-ttu-id="6f39a-125">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="6f39a-125">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6f39a-126">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6f39a-126">Return code</span></span>                                                                                   | <span data-ttu-id="6f39a-127">Description</span><span class="sxs-lookup"><span data-stu-id="6f39a-127">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6f39a-128"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6f39a-128"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6f39a-129">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="6f39a-129">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="6f39a-130"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6f39a-130"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6f39a-131">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="6f39a-131">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="6f39a-132"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="6f39a-132"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6f39a-133">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="6f39a-133">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="6f39a-134"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="6f39a-134"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6f39a-135">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="6f39a-135">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="6f39a-136">Notes</span><span class="sxs-lookup"><span data-stu-id="6f39a-136">Remarks</span></span>

<span data-ttu-id="6f39a-137">La commande encapsulée ne peut être exécutée que si l’état de sécurité de la carte à puce répond aux attributs de sécurité du fichier élémentaire en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="6f39a-137">The encapsulated command can only be performed if the security status of the smart card satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="6f39a-138">Lorsque la commande contient un identificateur élémentaire Short valide, elle définit le fichier en tant que fichier élémentaire actuel.</span><span class="sxs-lookup"><span data-stu-id="6f39a-138">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="6f39a-139">Les fichiers élémentaires sans structure transparente ne peuvent pas être effacés.</span><span class="sxs-lookup"><span data-stu-id="6f39a-139">Elementary files without a transparent structure cannot be erased.</span></span> <span data-ttu-id="6f39a-140">La commande encapsulée est abandonnée si elle est appliquée à un fichier élémentaire sans structure transparente.</span><span class="sxs-lookup"><span data-stu-id="6f39a-140">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="6f39a-141">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="6f39a-141">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="6f39a-142">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="6f39a-142">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6f39a-143">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6f39a-143">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f39a-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f39a-144">Requirements</span></span>



| <span data-ttu-id="6f39a-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f39a-145">Requirement</span></span> | <span data-ttu-id="6f39a-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f39a-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f39a-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f39a-147">Minimum supported client</span></span><br/> | <span data-ttu-id="6f39a-148">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f39a-148">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6f39a-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f39a-149">Minimum supported server</span></span><br/> | <span data-ttu-id="6f39a-150">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f39a-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6f39a-151">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="6f39a-151">End of client support</span></span><br/>    | <span data-ttu-id="6f39a-152">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6f39a-152">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6f39a-153">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="6f39a-153">End of server support</span></span><br/>    | <span data-ttu-id="6f39a-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6f39a-154">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6f39a-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="6f39a-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f39a-156"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f39a-156"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f39a-157">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6f39a-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="6f39a-158"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6f39a-158"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6f39a-159">DLL</span><span class="sxs-lookup"><span data-stu-id="6f39a-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f39a-160"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f39a-160"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6f39a-161">IID</span><span class="sxs-lookup"><span data-stu-id="6f39a-161">IID</span></span><br/>                      | <span data-ttu-id="6f39a-162">IID \_ ISCardISO7816 est défini en tant que 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="6f39a-162">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="6f39a-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f39a-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f39a-164">**EraseBinary**</span><span class="sxs-lookup"><span data-stu-id="6f39a-164">**EraseBinary**</span></span>](iscardiso7816-erasebinary.md)
</dt> <dt>

[<span data-ttu-id="6f39a-165">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="6f39a-165">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="6f39a-166">**ReadBinary**</span><span class="sxs-lookup"><span data-stu-id="6f39a-166">**ReadBinary**</span></span>](iscardiso7816-readbinary.md)
</dt> <dt>

[<span data-ttu-id="6f39a-167">**WriteBinary**</span><span class="sxs-lookup"><span data-stu-id="6f39a-167">**WriteBinary**</span></span>](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
