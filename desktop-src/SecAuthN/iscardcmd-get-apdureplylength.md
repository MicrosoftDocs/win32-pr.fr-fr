---
description: Détermine la longueur (en octets) de l’unité de données du protocole d’application (APDU).
ms.assetid: 25011db1-a037-4764-b700-8ad2200419da
title: 'ISCardCmd :: get_ApduReplyLength, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduReplyLength
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b62e67154ab48f8378c96a78c8bd54765962c3fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210759"
---
# <a name="iscardcmdget_apdureplylength-method"></a><span data-ttu-id="4cf74-103">ISCardCmd :: \_ ApduReplyLength, méthode</span><span class="sxs-lookup"><span data-stu-id="4cf74-103">ISCardCmd::get\_ApduReplyLength method</span></span>

<span data-ttu-id="4cf74-104">\[La méthode **obtenir \_ ApduReplyLength** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="4cf74-104">\[The **get\_ApduReplyLength** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4cf74-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4cf74-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4cf74-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="4cf74-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4cf74-107">La méthode d' **extraction \_ ApduReplyLength** détermine la longueur (en octets) de l' [*unité de données du protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="4cf74-107">The **get\_ApduReplyLength** method determines the length (in bytes) of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="4cf74-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4cf74-108">Syntax</span></span>


```C++
HRESULT get_ApduReplyLength(
  [out] LONG *plSize
);
```



## <a name="parameters"></a><span data-ttu-id="4cf74-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4cf74-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cf74-110">*plSize* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4cf74-110">*plSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cf74-111">Pointeur vers la taille du message APDU de réponse.</span><span class="sxs-lookup"><span data-stu-id="4cf74-111">Pointer to the size of the reply APDU message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cf74-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4cf74-112">Return value</span></span>

<span data-ttu-id="4cf74-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="4cf74-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="4cf74-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4cf74-114">Return code</span></span>                                                                                   | <span data-ttu-id="4cf74-115">Description</span><span class="sxs-lookup"><span data-stu-id="4cf74-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="4cf74-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4cf74-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4cf74-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="4cf74-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="4cf74-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4cf74-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4cf74-119">Le paramètre *plSize* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4cf74-119">The *plSize* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="4cf74-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="4cf74-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4cf74-121">Un pointeur incorrect a été passé dans *plSize*.</span><span class="sxs-lookup"><span data-stu-id="4cf74-121">A bad pointer was passed in *plSize*.</span></span><br/> |
| <dl> <span data-ttu-id="4cf74-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="4cf74-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4cf74-123">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="4cf74-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="4cf74-124">Notes</span><span class="sxs-lookup"><span data-stu-id="4cf74-124">Remarks</span></span>

<span data-ttu-id="4cf74-125">Pour récupérer une valeur APDU de réponse existante, appelez la [**\_ ApduReply**](iscardcmd-get-apdureply.md).</span><span class="sxs-lookup"><span data-stu-id="4cf74-125">To get an existing reply APDU, call [**get\_ApduReply**](iscardcmd-get-apdureply.md).</span></span>

<span data-ttu-id="4cf74-126">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="4cf74-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="4cf74-127">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="4cf74-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="4cf74-128">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="4cf74-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4cf74-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="4cf74-129">Examples</span></span>

<span data-ttu-id="4cf74-130">L’exemple suivant montre comment récupérer la longueur des valeurs APDU de la [*réponse*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4cf74-130">The following example shows how to retrieve the length of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="4cf74-131">L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="4cf74-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
LONG    lLen;
HRESULT hr;

// Retrieve the APDU reply length.
hr = pISCardCmd->get_ApduReplyLength(&lLen);
if (FAILED(hr))
{
    printf("Failed get_ApduReplyLength\n");
    // Take other error handling action.
}
else
    printf("Length returned is %d\n", lLen);
```



## <a name="requirements"></a><span data-ttu-id="4cf74-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4cf74-132">Requirements</span></span>



| <span data-ttu-id="4cf74-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4cf74-133">Requirement</span></span> | <span data-ttu-id="4cf74-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cf74-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cf74-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4cf74-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4cf74-136">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4cf74-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4cf74-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4cf74-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4cf74-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4cf74-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4cf74-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="4cf74-139">End of client support</span></span><br/>    | <span data-ttu-id="4cf74-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4cf74-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4cf74-141">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="4cf74-141">End of server support</span></span><br/>    | <span data-ttu-id="4cf74-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4cf74-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4cf74-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="4cf74-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cf74-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cf74-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="4cf74-145">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4cf74-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="4cf74-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4cf74-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4cf74-147">DLL</span><span class="sxs-lookup"><span data-stu-id="4cf74-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cf74-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cf74-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4cf74-149">IID</span><span class="sxs-lookup"><span data-stu-id="4cf74-149">IID</span></span><br/>                      | <span data-ttu-id="4cf74-150">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="4cf74-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="4cf74-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cf74-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cf74-152">**Obtient \_ ApduReply**</span><span class="sxs-lookup"><span data-stu-id="4cf74-152">**get\_ApduReply**</span></span>](iscardcmd-get-apdureply.md)
</dt> <dt>

[<span data-ttu-id="4cf74-153">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="4cf74-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="4cf74-154">**put \_ ApduReply**</span><span class="sxs-lookup"><span data-stu-id="4cf74-154">**put\_ApduReply**</span></span>](iscardcmd-put-apdureply.md)
</dt> </dl>

 

 
