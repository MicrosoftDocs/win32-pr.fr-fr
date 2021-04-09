---
description: Définit une nouvelle réponse APDU.
ms.assetid: 1d058c89-0de9-4809-b008-ae24c62acc5b
title: ISCardCmd ::p ut_ApduReply, méthode (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ApduReply
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0292f3ebd4e5f18638ad496cdf15cd9f5c4320f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862634"
---
# <a name="iscardcmdput_apdureply-method"></a><span data-ttu-id="e219c-103">ISCardCmd ::p ut \_ ApduReply, méthode</span><span class="sxs-lookup"><span data-stu-id="e219c-103">ISCardCmd::put\_ApduReply method</span></span>

<span data-ttu-id="e219c-104">\[La méthode **put \_ ApduReply** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="e219c-104">\[The **put\_ApduReply** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e219c-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e219c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e219c-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="e219c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="e219c-107">La méthode **put \_ ApduReply** définit un nouveau [*APDU de réponse*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e219c-107">The **put\_ApduReply** method sets a new [*reply APDU*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e219c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e219c-108">Syntax</span></span>


```C++
HRESULT put_ApduReply(
  [in] LPBYTEBUFFER pReplyApdu
);
```



## <a name="parameters"></a><span data-ttu-id="e219c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e219c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e219c-110">*pReplyApdu* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e219c-110">*pReplyApdu* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e219c-111">Pointeur vers la mémoire tampon d’octets (mappée via un objet **IStream** ) qui contient le message APDU de relecture au retour.</span><span class="sxs-lookup"><span data-stu-id="e219c-111">Pointer to the byte buffer (mapped through an **IStream** object) that contains the replay APDU message on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e219c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e219c-112">Return value</span></span>

<span data-ttu-id="e219c-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="e219c-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="e219c-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e219c-114">Return code</span></span>                                                                                   | <span data-ttu-id="e219c-115">Description</span><span class="sxs-lookup"><span data-stu-id="e219c-115">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="e219c-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e219c-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e219c-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="e219c-117">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="e219c-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e219c-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e219c-119">Le paramètre *pReplyApdu* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e219c-119">The *pReplyApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="e219c-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="e219c-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e219c-121">Un pointeur incorrect a été passé dans *pReplyApdu*.</span><span class="sxs-lookup"><span data-stu-id="e219c-121">A bad pointer was passed in *pReplyApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="e219c-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="e219c-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e219c-123">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="e219c-123">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="e219c-124">Notes</span><span class="sxs-lookup"><span data-stu-id="e219c-124">Remarks</span></span>

<span data-ttu-id="e219c-125">Pour récupérer une valeur APDU de réponse existante, appelez la [**\_ ApduReply**](iscardcmd-get-apdureply.md).</span><span class="sxs-lookup"><span data-stu-id="e219c-125">To get an existing reply APDU, call [**get\_ApduReply**](iscardcmd-get-apdureply.md).</span></span>

<span data-ttu-id="e219c-126">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="e219c-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="e219c-127">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="e219c-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="e219c-128">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="e219c-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e219c-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="e219c-129">Examples</span></span>

<span data-ttu-id="e219c-130">L’exemple suivant montre comment définir une nouvelle valeur [*APDU de réponse*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e219c-130">The following example shows how to set a new [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="e219c-131">L’exemple suppose que pIByteReply est un pointeur valide vers une instance de [**IByteBuffer**](ibytebuffer.md)et que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="e219c-131">The example assumes that pIByteReply is a valid pointer to an instance of [**IByteBuffer**](ibytebuffer.md), and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;

// Set the reply data.
hr = pISCardCmd->put_ApduReply(pIByteReply);
if (FAILED(hr)) 
{
    printf("Failed put_ApduReply.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="e219c-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e219c-132">Requirements</span></span>



| <span data-ttu-id="e219c-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e219c-133">Requirement</span></span> | <span data-ttu-id="e219c-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="e219c-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e219c-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e219c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e219c-136">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e219c-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e219c-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e219c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e219c-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e219c-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e219c-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e219c-139">End of client support</span></span><br/>    | <span data-ttu-id="e219c-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e219c-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="e219c-141">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="e219c-141">End of server support</span></span><br/>    | <span data-ttu-id="e219c-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e219c-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="e219c-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="e219c-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="e219c-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="e219c-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="e219c-145">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e219c-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="e219c-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e219c-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e219c-147">DLL</span><span class="sxs-lookup"><span data-stu-id="e219c-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e219c-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e219c-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e219c-149">IID</span><span class="sxs-lookup"><span data-stu-id="e219c-149">IID</span></span><br/>                      | <span data-ttu-id="e219c-150">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="e219c-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="e219c-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e219c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e219c-152">**Obtient \_ ApduReply**</span><span class="sxs-lookup"><span data-stu-id="e219c-152">**get\_ApduReply**</span></span>](iscardcmd-get-apdureply.md)
</dt> <dt>

[<span data-ttu-id="e219c-153">**Obtient \_ ApduReplyLength**</span><span class="sxs-lookup"><span data-stu-id="e219c-153">**get\_ApduReplyLength**</span></span>](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[<span data-ttu-id="e219c-154">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="e219c-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
