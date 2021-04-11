---
description: Récupère l’octet d’état de la réponse APDU SW2.
ms.assetid: 24ad0164-84fc-4a99-b9dd-0f7d789dff92
title: 'ISCardCmd :: get_ReplyStatusSW2, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatusSW2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7ff503758a50437b4b7ff974fe4455d4b92ce978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113215"
---
# <a name="iscardcmdget_replystatussw2-method"></a><span data-ttu-id="df407-103">ISCardCmd :: \_ ReplyStatusSW2, méthode</span><span class="sxs-lookup"><span data-stu-id="df407-103">ISCardCmd::get\_ReplyStatusSW2 method</span></span>

<span data-ttu-id="df407-104">\[La méthode **obtenir \_ ReplyStatusSW2** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="df407-104">\[The **get\_ReplyStatusSW2** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="df407-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="df407-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="df407-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="df407-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="df407-107">La méthode **obtenir \_ ReplyStatusSW2** récupère l’octet d’état de la [*réponse APDU*](../secgloss/r-gly.md) SW2.</span><span class="sxs-lookup"><span data-stu-id="df407-107">The **get\_ReplyStatusSW2** method retrieves the [*reply APDU*](../secgloss/r-gly.md) SW2 status byte.</span></span>

## <a name="syntax"></a><span data-ttu-id="df407-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df407-108">Syntax</span></span>


```C++
HRESULT get_ReplyStatusSW2(
  [out] LPBYTE pbySW2
);
```



## <a name="parameters"></a><span data-ttu-id="df407-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df407-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df407-110">*pbySW2* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="df407-110">*pbySW2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df407-111">Pointeur vers l’octet qui contient la valeur de l’octet SW2 sur le retour.</span><span class="sxs-lookup"><span data-stu-id="df407-111">Pointer to the byte that contains the value of the SW2 byte on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df407-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="df407-112">Return value</span></span>

<span data-ttu-id="df407-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="df407-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="df407-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="df407-114">Return code</span></span>                                                                                   | <span data-ttu-id="df407-115">Description</span><span class="sxs-lookup"><span data-stu-id="df407-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="df407-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="df407-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="df407-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="df407-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="df407-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="df407-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="df407-119">*PbySW2* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="df407-119">The *pbySW2* is not valid.</span></span><br/>            |
| <dl> <span data-ttu-id="df407-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="df407-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="df407-121">Un pointeur incorrect a été passé dans *pbySW2*.</span><span class="sxs-lookup"><span data-stu-id="df407-121">A bad pointer was passed in *pbySW2*.</span></span><br/> |
| <dl> <span data-ttu-id="df407-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="df407-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="df407-123">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="df407-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="df407-124">Notes</span><span class="sxs-lookup"><span data-stu-id="df407-124">Remarks</span></span>

<span data-ttu-id="df407-125">L’octet d’État SW2 de la réponse APDU est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="df407-125">The reply APDU's SW2 status byte is read-only.</span></span>

<span data-ttu-id="df407-126">Pour récupérer l’octet d’État SW1 de la réponse APDU, appelez [**obtenir \_ ReplyStatusSW1**](iscardcmd-get-replystatussw1.md).</span><span class="sxs-lookup"><span data-stu-id="df407-126">To retrieve the reply APDU's SW1 status byte, call [**get\_ReplyStatusSW1**](iscardcmd-get-replystatussw1.md).</span></span>

<span data-ttu-id="df407-127">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="df407-127">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="df407-128">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="df407-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="df407-129">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="df407-129">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="df407-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="df407-130">Examples</span></span>

<span data-ttu-id="df407-131">L’exemple suivant montre comment récupérer l’octet d’État SW2 de la [*réponse APDU*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="df407-131">The following example shows how to retrieve the SW2 status byte of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="df407-132">L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="df407-132">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     bySW2;
HRESULT  hr;

// Retrieve the reply status SW2 byte.
hr = pISCardCmd->get_ReplyStatusSW2(&bySW2);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatusSW2\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="df407-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df407-133">Requirements</span></span>



| <span data-ttu-id="df407-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df407-134">Requirement</span></span> | <span data-ttu-id="df407-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="df407-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df407-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df407-136">Minimum supported client</span></span><br/> | <span data-ttu-id="df407-137">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df407-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="df407-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df407-138">Minimum supported server</span></span><br/> | <span data-ttu-id="df407-139">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df407-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="df407-140">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="df407-140">End of client support</span></span><br/>    | <span data-ttu-id="df407-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="df407-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="df407-142">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="df407-142">End of server support</span></span><br/>    | <span data-ttu-id="df407-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="df407-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="df407-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="df407-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="df407-145"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="df407-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="df407-146">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="df407-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="df407-147"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="df407-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="df407-148">DLL</span><span class="sxs-lookup"><span data-stu-id="df407-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df407-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df407-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="df407-150">IID</span><span class="sxs-lookup"><span data-stu-id="df407-150">IID</span></span><br/>                      | <span data-ttu-id="df407-151">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="df407-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="df407-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df407-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df407-153">**Obtient \_ ReplyStatusSW1**</span><span class="sxs-lookup"><span data-stu-id="df407-153">**get\_ReplyStatusSW1**</span></span>](iscardcmd-get-replystatussw1.md)
</dt> <dt>

[<span data-ttu-id="df407-154">**Obtient \_ ReplyStatus**</span><span class="sxs-lookup"><span data-stu-id="df407-154">**get\_ReplyStatus**</span></span>](iscardcmd-get-replystatus.md)
</dt> <dt>

[<span data-ttu-id="df407-155">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="df407-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
