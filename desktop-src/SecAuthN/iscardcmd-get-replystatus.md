---
description: Récupère le mot d’État du message de la réponse APDU.
ms.assetid: c8a4b713-4ae9-49f2-a623-6ee305123638
title: 'ISCardCmd :: get_ReplyStatus, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatus
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 021c5395dbca6275161a53cb7e8a0c2247ab9410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113218"
---
# <a name="iscardcmdget_replystatus-method"></a><span data-ttu-id="30b71-103">ISCardCmd :: \_ ReplyStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="30b71-103">ISCardCmd::get\_ReplyStatus method</span></span>

<span data-ttu-id="30b71-104">\[La méthode **obtenir \_ ReplyStatus** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="30b71-104">\[The **get\_ReplyStatus** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="30b71-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="30b71-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="30b71-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="30b71-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="30b71-107">La méthode **obtenir \_ ReplyStatus** récupère le mot [*d’État du message de la réponse APDU*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="30b71-107">The **get\_ReplyStatus** method retrieves the [*reply APDU's*](../secgloss/r-gly.md) message status word.</span></span>

## <a name="syntax"></a><span data-ttu-id="30b71-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30b71-108">Syntax</span></span>


```C++
HRESULT get_ReplyStatus(
  [out] LPWORD pwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="30b71-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30b71-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30b71-110">*pwStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="30b71-110">*pwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30b71-111">Pointeur vers le mot qui correspond à l’état de retour.</span><span class="sxs-lookup"><span data-stu-id="30b71-111">Pointer to the word that is the status on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30b71-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30b71-112">Return value</span></span>

<span data-ttu-id="30b71-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="30b71-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="30b71-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="30b71-114">Return code</span></span>                                                                                   | <span data-ttu-id="30b71-115">Description</span><span class="sxs-lookup"><span data-stu-id="30b71-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="30b71-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="30b71-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="30b71-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="30b71-117">Operation completed successfully.</span></span><br/>       |
| <dl> <span data-ttu-id="30b71-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="30b71-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="30b71-119">Le paramètre *pwStatus* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="30b71-119">The *pwStatus* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="30b71-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="30b71-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="30b71-121">Un pointeur incorrect a été passé dans *pwStatus*.</span><span class="sxs-lookup"><span data-stu-id="30b71-121">A bad pointer was passed in *pwStatus*.</span></span><br/> |
| <dl> <span data-ttu-id="30b71-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="30b71-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="30b71-123">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="30b71-123">Out of memory.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="30b71-124">Notes</span><span class="sxs-lookup"><span data-stu-id="30b71-124">Remarks</span></span>

<span data-ttu-id="30b71-125">Pour définir le mot d’État du message de la réponse APDU, appelez [**put \_ ReplyStatus**](iscardcmd-put-replystatus.md).</span><span class="sxs-lookup"><span data-stu-id="30b71-125">To set the reply APDU's message status word, call [**put\_ReplyStatus**](iscardcmd-put-replystatus.md).</span></span>

<span data-ttu-id="30b71-126">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="30b71-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="30b71-127">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="30b71-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="30b71-128">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="30b71-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="30b71-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="30b71-129">Examples</span></span>

<span data-ttu-id="30b71-130">L’exemple suivant montre comment récupérer le mot d’État du message de la [*réponse APDU*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="30b71-130">The following example shows how to retrieve the message status word of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="30b71-131">L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="30b71-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
WORD    wReplyStatus;
HRESULT hr;

// Get reply status.
hr = pISCardCmd->get_ReplyStatus(&wReplyStatus);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatus\n");
  // Take other error handling action as needed.
}
else
{
  if (wReplyStatus != 0x9000)
  {
    printf("APDU failed - Error [0x%x]\n", wReplyStatus);
    // Take other error handling action as needed.
  }
}
```



## <a name="requirements"></a><span data-ttu-id="30b71-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30b71-132">Requirements</span></span>



| <span data-ttu-id="30b71-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30b71-133">Requirement</span></span> | <span data-ttu-id="30b71-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="30b71-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30b71-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30b71-135">Minimum supported client</span></span><br/> | <span data-ttu-id="30b71-136">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30b71-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="30b71-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30b71-137">Minimum supported server</span></span><br/> | <span data-ttu-id="30b71-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30b71-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="30b71-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="30b71-139">End of client support</span></span><br/>    | <span data-ttu-id="30b71-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="30b71-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="30b71-141">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="30b71-141">End of server support</span></span><br/>    | <span data-ttu-id="30b71-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="30b71-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="30b71-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="30b71-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="30b71-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="30b71-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="30b71-145">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="30b71-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="30b71-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="30b71-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="30b71-147">DLL</span><span class="sxs-lookup"><span data-stu-id="30b71-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30b71-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30b71-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="30b71-149">IID</span><span class="sxs-lookup"><span data-stu-id="30b71-149">IID</span></span><br/>                      | <span data-ttu-id="30b71-150">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="30b71-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="30b71-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30b71-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30b71-152">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="30b71-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="30b71-153">**put \_ ReplyStatus**</span><span class="sxs-lookup"><span data-stu-id="30b71-153">**put\_ReplyStatus**</span></span>](iscardcmd-put-replystatus.md)
</dt> </dl>

 

 
