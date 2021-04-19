---
description: La méthode GetResponse construit une commande APDU (Application Protocol Data Unit) qui transmet les commandes APDU (ou une partie d’une commande APDU) qui n’ont pas pu être transmises par les protocoles disponibles.
ms.assetid: 1aa83d38-d46d-4d3b-8f57-0256e5875e35
title: 'ISCardISO7816 :: GetResponse, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetResponse
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0b74fe9620aefc390957b88f9cf286f7871c1d18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541222"
---
# <a name="iscardiso7816getresponse-method"></a><span data-ttu-id="f0c07-103">ISCardISO7816 :: GetResponse, méthode</span><span class="sxs-lookup"><span data-stu-id="f0c07-103">ISCardISO7816::GetResponse method</span></span>

<span data-ttu-id="f0c07-104">\[La méthode **GetResponse** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="f0c07-104">\[The **GetResponse** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f0c07-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f0c07-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f0c07-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="f0c07-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f0c07-107">La méthode **GetResponse** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui transmet les commandes APDU (ou une partie d’une commande APDU) qui n’ont pas pu être transmises par les protocoles disponibles.</span><span class="sxs-lookup"><span data-stu-id="f0c07-107">The **GetResponse** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that transmits APDU commands (or part of an APDU command) which otherwise could not be transmitted by the available protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0c07-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0c07-108">Syntax</span></span>


```C++
HRESULT GetResponse(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lDataLength,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="f0c07-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0c07-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0c07-110">*byP1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0c07-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c07-111">Conformément à la norme ISO 7816-4, P1 doit être égal à zéro (RFU).</span><span class="sxs-lookup"><span data-stu-id="f0c07-111">Per the ISO 7816-4, P1 should be zero (RFU).</span></span>

</dd> <dt>

<span data-ttu-id="f0c07-112">*byP2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0c07-112">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c07-113">Conformément à la norme ISO 7816-4, P2 doit être égal à zéro (RFU).</span><span class="sxs-lookup"><span data-stu-id="f0c07-113">Per the ISO 7816-4, P2 should be zero (RFU).</span></span>

</dd> <dt>

<span data-ttu-id="f0c07-114">*lDataLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0c07-114">*lDataLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c07-115">Longueur des données transmises.</span><span class="sxs-lookup"><span data-stu-id="f0c07-115">Length of data transmitted.</span></span>

</dd> <dt>

<span data-ttu-id="f0c07-116">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f0c07-116">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c07-117">En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.</span><span class="sxs-lookup"><span data-stu-id="f0c07-117">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="f0c07-118">Au retour, elle est remplie avec la commande APDU construite par cette opération.</span><span class="sxs-lookup"><span data-stu-id="f0c07-118">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="f0c07-119">Si *ppCmd* a été défini avec la **valeur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé et retourné en interne par le biais du pointeur *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="f0c07-119">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0c07-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f0c07-120">Return value</span></span>

<span data-ttu-id="f0c07-121">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="f0c07-121">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="f0c07-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f0c07-122">Return code</span></span>                                                                                   | <span data-ttu-id="f0c07-123">Description</span><span class="sxs-lookup"><span data-stu-id="f0c07-123">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f0c07-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f0c07-124"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f0c07-125">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="f0c07-125">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="f0c07-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f0c07-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f0c07-127">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="f0c07-127">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="f0c07-128"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="f0c07-128"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f0c07-129">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="f0c07-129">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="f0c07-130"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="f0c07-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f0c07-131">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="f0c07-131">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="f0c07-132">Notes</span><span class="sxs-lookup"><span data-stu-id="f0c07-132">Remarks</span></span>

<span data-ttu-id="f0c07-133">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="f0c07-133">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="f0c07-134">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="f0c07-134">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="f0c07-135">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="f0c07-135">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0c07-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0c07-136">Requirements</span></span>



| <span data-ttu-id="f0c07-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0c07-137">Requirement</span></span> | <span data-ttu-id="f0c07-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0c07-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c07-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0c07-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f0c07-140">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0c07-140">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f0c07-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0c07-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f0c07-142">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0c07-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f0c07-143">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f0c07-143">End of client support</span></span><br/>    | <span data-ttu-id="f0c07-144">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f0c07-144">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f0c07-145">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="f0c07-145">End of server support</span></span><br/>    | <span data-ttu-id="f0c07-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f0c07-146">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f0c07-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0c07-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0c07-148"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0c07-148"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f0c07-149">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f0c07-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="f0c07-150"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f0c07-150"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f0c07-151">DLL</span><span class="sxs-lookup"><span data-stu-id="f0c07-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0c07-152"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0c07-152"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f0c07-153">IID</span><span class="sxs-lookup"><span data-stu-id="f0c07-153">IID</span></span><br/>                      | <span data-ttu-id="f0c07-154">IID \_ ISCardISO7816 est défini en tant que 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="f0c07-154">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="f0c07-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0c07-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0c07-156">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="f0c07-156">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
