---
description: Construit une commande APDU (Application Protocol Data Unit) qui définit de façon séquentielle une partie du contenu d’un fichier élémentaire à son état effacé logique, à partir d’un offset donné.
ms.assetid: 89e2371e-e27d-475b-9427-bbf6d614c473
title: 'ISCardISO7816 :: EraseBinary, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.EraseBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a9bad21bbb35b7ac16209ac0075267ef7300fe21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534742"
---
# <a name="iscardiso7816erasebinary-method"></a><span data-ttu-id="435c5-103">ISCardISO7816 :: EraseBinary, méthode</span><span class="sxs-lookup"><span data-stu-id="435c5-103">ISCardISO7816::EraseBinary method</span></span>

<span data-ttu-id="435c5-104">\[La méthode **EraseBinary** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="435c5-104">\[The **EraseBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="435c5-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="435c5-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="435c5-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="435c5-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="435c5-107">La méthode **EraseBinary** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui définit de façon séquentielle une partie du contenu d’un fichier élémentaire à son état effacé logique, à partir d’un décalage donné.</span><span class="sxs-lookup"><span data-stu-id="435c5-107">The **EraseBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that sequentially sets part of the content of an elementary file to its logical erased state, starting from a given offset.</span></span>

## <a name="syntax"></a><span data-ttu-id="435c5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="435c5-108">Syntax</span></span>


```C++
HRESULT EraseBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="435c5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="435c5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="435c5-110">*byP1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="435c5-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="435c5-111">Position RFU.</span><span class="sxs-lookup"><span data-stu-id="435c5-111">RFU position.</span></span>

<span data-ttu-id="435c5-112">Si B8 = 1 dans P1, alors B7 et B6 de P1 ont la valeur zéro (RFU bits), B5 à B1 pour P1 est un identificateur EF bref et P2 est le décalage du premier octet à effacer (en unités de données) à partir du début du fichier.</span><span class="sxs-lookup"><span data-stu-id="435c5-112">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="435c5-113">Si B8 = 0 dans P1, P1 \| \| P2 est le décalage du premier octet à effacer (en unités de données) à partir du début du fichier.</span><span class="sxs-lookup"><span data-stu-id="435c5-113">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="435c5-114">Si le champ de données est présent, il code le décalage de la première unité de données à ne pas effacer.</span><span class="sxs-lookup"><span data-stu-id="435c5-114">If the data field is present, it codes the offset of the first data unit not to be erased.</span></span> <span data-ttu-id="435c5-115">Ce décalage doit être supérieur à celui codé dans P1-P2.</span><span class="sxs-lookup"><span data-stu-id="435c5-115">This offset shall be higher than the one coded in P1-P2.</span></span> <span data-ttu-id="435c5-116">Lorsque le champ de données est vide, la commande s’efface jusqu’à la fin du fichier.</span><span class="sxs-lookup"><span data-stu-id="435c5-116">When the data field is empty, the command erases up to the end of the file.</span></span>

</dd> <dt>

<span data-ttu-id="435c5-117">*byP2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="435c5-117">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="435c5-118">Position RFU.</span><span class="sxs-lookup"><span data-stu-id="435c5-118">RFU position.</span></span>

<span data-ttu-id="435c5-119">Si B8 = 1 dans P1, alors B7 et B6 de P1 ont la valeur zéro (RFU bits), B5 à B1 pour P1 est un identificateur EF bref et P2 est le décalage du premier octet à effacer (en unités de données) à partir du début du fichier.</span><span class="sxs-lookup"><span data-stu-id="435c5-119">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="435c5-120">Si B8 = 0 dans P1, P1 \| \| P2 est le décalage du premier octet à effacer (en unités de données) à partir du début du fichier.</span><span class="sxs-lookup"><span data-stu-id="435c5-120">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="435c5-121">Si le champ de données est présent, il code le décalage de la première unité de données à ne pas effacer.</span><span class="sxs-lookup"><span data-stu-id="435c5-121">If the data field is present, it codes the offset of the first data unit not to be erased.</span></span> <span data-ttu-id="435c5-122">Ce décalage doit être supérieur à celui codé dans P1-P2.</span><span class="sxs-lookup"><span data-stu-id="435c5-122">This offset shall be higher than the one coded in P1-P2.</span></span> <span data-ttu-id="435c5-123">Lorsque le champ de données est vide, la commande s’efface jusqu’à la fin du fichier.</span><span class="sxs-lookup"><span data-stu-id="435c5-123">When the data field is empty, the command erases up to the end of the file.</span></span>

</dd> <dt>

<span data-ttu-id="435c5-124">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="435c5-124">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="435c5-125">Pointeur vers les données qui spécifient la plage d’effacement.</span><span class="sxs-lookup"><span data-stu-id="435c5-125">A pointer to the data that specifies the erase range.</span></span> <span data-ttu-id="435c5-126">Ce paramètre peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="435c5-126">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="435c5-127">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="435c5-127">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="435c5-128">En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.</span><span class="sxs-lookup"><span data-stu-id="435c5-128">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="435c5-129">Au retour, elle est remplie avec la commande APDU construite par cette opération.</span><span class="sxs-lookup"><span data-stu-id="435c5-129">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="435c5-130">Si *ppCmd* a été défini **sur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé et retourné en interne à l’aide du pointeur *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="435c5-130">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="435c5-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="435c5-131">Return value</span></span>

<span data-ttu-id="435c5-132">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="435c5-132">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="435c5-133">Code de retour</span><span class="sxs-lookup"><span data-stu-id="435c5-133">Return code</span></span>                                                                                   | <span data-ttu-id="435c5-134">Description</span><span class="sxs-lookup"><span data-stu-id="435c5-134">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="435c5-135"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="435c5-135"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="435c5-136">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="435c5-136">The operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="435c5-137"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="435c5-137"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="435c5-138">Un paramètre non valide a été passé.</span><span class="sxs-lookup"><span data-stu-id="435c5-138">A parameter that is not valid was passed.</span></span><br/> |
| <dl> <span data-ttu-id="435c5-139"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="435c5-139"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="435c5-140">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="435c5-140">A bad pointer was passed in.</span></span><br/>              |
| <dl> <span data-ttu-id="435c5-141"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="435c5-141"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="435c5-142">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="435c5-142">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="435c5-143">Notes</span><span class="sxs-lookup"><span data-stu-id="435c5-143">Remarks</span></span>

<span data-ttu-id="435c5-144">La commande encapsulée ne peut être exécutée que si l’état de sécurité de la [*carte à puce*](../secgloss/s-gly.md) répond aux attributs de sécurité du fichier élémentaire en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="435c5-144">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="435c5-145">Lorsque la commande contient un identificateur élémentaire Short valide, elle définit le fichier en tant que fichier élémentaire actuel.</span><span class="sxs-lookup"><span data-stu-id="435c5-145">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="435c5-146">Les fichiers élémentaires sans structure transparente ne peuvent pas être effacés.</span><span class="sxs-lookup"><span data-stu-id="435c5-146">Elementary files without a transparent structure cannot be erased.</span></span> <span data-ttu-id="435c5-147">La commande encapsulée est abandonnée si elle est appliquée à un fichier élémentaire sans structure transparente.</span><span class="sxs-lookup"><span data-stu-id="435c5-147">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="435c5-148">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="435c5-148">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="435c5-149">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="435c5-149">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="435c5-150">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="435c5-150">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="435c5-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="435c5-151">Requirements</span></span>



| <span data-ttu-id="435c5-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="435c5-152">Requirement</span></span> | <span data-ttu-id="435c5-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="435c5-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="435c5-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="435c5-154">Minimum supported client</span></span><br/> | <span data-ttu-id="435c5-155">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="435c5-155">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="435c5-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="435c5-156">Minimum supported server</span></span><br/> | <span data-ttu-id="435c5-157">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="435c5-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="435c5-158">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="435c5-158">End of client support</span></span><br/>    | <span data-ttu-id="435c5-159">Windows XP</span><span class="sxs-lookup"><span data-stu-id="435c5-159">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="435c5-160">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="435c5-160">End of server support</span></span><br/>    | <span data-ttu-id="435c5-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="435c5-161">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="435c5-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="435c5-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="435c5-163"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="435c5-163"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="435c5-164">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="435c5-164">Type library</span></span><br/>             | <dl> <span data-ttu-id="435c5-165"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="435c5-165"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="435c5-166">DLL</span><span class="sxs-lookup"><span data-stu-id="435c5-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="435c5-167"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="435c5-167"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="435c5-168">IID</span><span class="sxs-lookup"><span data-stu-id="435c5-168">IID</span></span><br/>                      | <span data-ttu-id="435c5-169">IID \_ ISCardISO7816 est défini en tant que 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="435c5-169">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="435c5-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="435c5-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="435c5-171">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="435c5-171">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="435c5-172">**ReadBinary**</span><span class="sxs-lookup"><span data-stu-id="435c5-172">**ReadBinary**</span></span>](iscardiso7816-readbinary.md)
</dt> <dt>

[<span data-ttu-id="435c5-173">**UpdateBinary**</span><span class="sxs-lookup"><span data-stu-id="435c5-173">**UpdateBinary**</span></span>](iscardiso7816-updatebinary.md)
</dt> <dt>

[<span data-ttu-id="435c5-174">**WriteBinary**</span><span class="sxs-lookup"><span data-stu-id="435c5-174">**WriteBinary**</span></span>](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
