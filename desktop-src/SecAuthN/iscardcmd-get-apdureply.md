---
description: Récupère les APDU de réponse, en les plaçant dans une mémoire tampon d’octets spécifique.
ms.assetid: ab349e7a-350f-4e72-98b4-4c6431b6e380
title: 'ISCardCmd :: get_ApduReply, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduReply
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2ce11ec2d3d8202574ab23074531c393c9fecb98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042812"
---
# <a name="iscardcmdget_apdureply-method"></a><span data-ttu-id="c7d44-103">ISCardCmd :: \_ ApduReply, méthode</span><span class="sxs-lookup"><span data-stu-id="c7d44-103">ISCardCmd::get\_ApduReply method</span></span>

<span data-ttu-id="c7d44-104">\[La méthode **obtenir \_ ApduReply** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="c7d44-104">\[The **get\_ApduReply** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c7d44-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="c7d44-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c7d44-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="c7d44-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c7d44-107">La méthode **obtenir \_ ApduReply** récupère les [*APDU de réponse*](../secgloss/r-gly.md), en les plaçant dans une mémoire tampon d’octets spécifique.</span><span class="sxs-lookup"><span data-stu-id="c7d44-107">The **get\_ApduReply** method retrieves the [*reply APDU*](../secgloss/r-gly.md), placing it in a specific byte buffer.</span></span> <span data-ttu-id="c7d44-108">La réponse peut être **null** si aucune [*transaction*](../secgloss/t-gly.md) n’a été effectuée sur la commande APDU.</span><span class="sxs-lookup"><span data-stu-id="c7d44-108">The reply may be **NULL** if no [*transaction*](../secgloss/t-gly.md) has been performed on the command APDU.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7d44-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7d44-109">Syntax</span></span>


```C++
HRESULT get_ApduReply(
  [out] LPBYTEBUFFER *ppReplyApdu
);
```



## <a name="parameters"></a><span data-ttu-id="c7d44-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7d44-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7d44-111">*ppReplyApdu* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c7d44-111">*ppReplyApdu* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7d44-112">Pointeur vers la mémoire tampon d’octets (mappée via un objet **IStream** ) qui contient le message de réponse APDU au retour.</span><span class="sxs-lookup"><span data-stu-id="c7d44-112">Pointer to the byte buffer (mapped through an **IStream** object) that contains the APDU reply message on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7d44-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c7d44-113">Return value</span></span>

<span data-ttu-id="c7d44-114">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="c7d44-114">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="c7d44-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c7d44-115">Return code</span></span>                                                                                   | <span data-ttu-id="c7d44-116">Description</span><span class="sxs-lookup"><span data-stu-id="c7d44-116">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="c7d44-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c7d44-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c7d44-118">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="c7d44-118">Operation completed successfully.</span></span><br/>          |
| <dl> <span data-ttu-id="c7d44-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c7d44-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c7d44-120">Le paramètre *ppReplyApdu* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c7d44-120">The *ppReplyApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="c7d44-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="c7d44-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c7d44-122">Un pointeur incorrect a été passé dans *ppReplyApdu*.</span><span class="sxs-lookup"><span data-stu-id="c7d44-122">A bad pointer was passed in *ppReplyApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="c7d44-123"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="c7d44-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c7d44-124">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="c7d44-124">Out of memory.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="c7d44-125">Notes</span><span class="sxs-lookup"><span data-stu-id="c7d44-125">Remarks</span></span>

<span data-ttu-id="c7d44-126">Pour déterminer la longueur de la réponse APDU, appelez [**obtenir \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md).</span><span class="sxs-lookup"><span data-stu-id="c7d44-126">To determine the length of the APDU reply, call [**get\_ApduReplyLength**](iscardcmd-get-apdureplylength.md).</span></span>

<span data-ttu-id="c7d44-127">Pour définir une nouvelle valeur APDU de réponse, appelez [**put \_ ApduReply**](iscardcmd-put-apdureply.md).</span><span class="sxs-lookup"><span data-stu-id="c7d44-127">To set a new reply APDU, call [**put\_ApduReply**](iscardcmd-put-apdureply.md).</span></span>

<span data-ttu-id="c7d44-128">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="c7d44-128">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="c7d44-129">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="c7d44-129">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="c7d44-130">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="c7d44-130">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c7d44-131">Exemples</span><span class="sxs-lookup"><span data-stu-id="c7d44-131">Examples</span></span>

<span data-ttu-id="c7d44-132">L’exemple suivant montre comment récupérer des données de réponse.</span><span class="sxs-lookup"><span data-stu-id="c7d44-132">The following example shows how to retrieve reply data.</span></span> <span data-ttu-id="c7d44-133">L’exemple suppose que lLe est une variable de type **long** dont la valeur a été définie par un appel précédent à la méthode [**ISCardCmd :: obtenir \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md) , que pIByteReply est un pointeur valide vers une instance de l’interface [**IByteBuffer**](ibytebuffer.md) et que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="c7d44-133">The example assumes that lLe is a variable of type **LONG** whose value was set by a previous call to the [**ISCardCmd::get\_ApduReplyLength**](iscardcmd-get-apdureplylength.md) method, that pIByteReply is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface, and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT      hr;

if (lLe > 0)
{
    // Get reply data if available.
    hr = pISCardCmd->get_ApduReply(&pIByteReply);
    if (FAILED(hr)) 
    {
        printf("Failed ISCardCmd::get_ApduReply.\n");
        // Take other error handling action as needed.
    }
    else
    {
        BYTE byReplyBytes[256];
        LONG lBytesRead;

        hr = pIByteReply->Read(byReplyBytes, lLe, &lBytesRead);
        if (FAILED(hr))
        {
            printf("Failed IByteBuffer::Read.\n");
            // Take other error handling action as needed.
        }
        // Use the bytes in byReplyBytes as needed.
    }
}
```



## <a name="requirements"></a><span data-ttu-id="c7d44-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7d44-134">Requirements</span></span>



| <span data-ttu-id="c7d44-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7d44-135">Requirement</span></span> | <span data-ttu-id="c7d44-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7d44-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7d44-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7d44-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c7d44-138">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7d44-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c7d44-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7d44-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c7d44-140">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7d44-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c7d44-141">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="c7d44-141">End of client support</span></span><br/>    | <span data-ttu-id="c7d44-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c7d44-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="c7d44-143">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="c7d44-143">End of server support</span></span><br/>    | <span data-ttu-id="c7d44-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c7d44-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="c7d44-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7d44-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7d44-146"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7d44-146"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7d44-147">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c7d44-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="c7d44-148"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c7d44-148"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c7d44-149">DLL</span><span class="sxs-lookup"><span data-stu-id="c7d44-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7d44-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7d44-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c7d44-151">IID</span><span class="sxs-lookup"><span data-stu-id="c7d44-151">IID</span></span><br/>                      | <span data-ttu-id="c7d44-152">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="c7d44-152">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="c7d44-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7d44-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7d44-154">**Obtient \_ ApduReplyLength**</span><span class="sxs-lookup"><span data-stu-id="c7d44-154">**get\_ApduReplyLength**</span></span>](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[<span data-ttu-id="c7d44-155">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="c7d44-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="c7d44-156">**put \_ ApduReply**</span><span class="sxs-lookup"><span data-stu-id="c7d44-156">**put\_ApduReply**</span></span>](iscardcmd-put-apdureply.md)
</dt> </dl>

 

 
