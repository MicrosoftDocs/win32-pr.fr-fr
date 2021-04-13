---
description: Récupère l’octet de l’État SW1 de réponse APDU.
ms.assetid: 5f74d0c9-cf82-4694-bca6-a2655e717a1f
title: 'ISCardCmd :: get_ReplyStatusSW1, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatusSW1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92bcf490a3cb1fc533bcf9a1046642d3c3e55b59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526350"
---
# <a name="iscardcmdget_replystatussw1-method"></a><span data-ttu-id="ade25-103">ISCardCmd :: \_ ReplyStatusSW1, méthode</span><span class="sxs-lookup"><span data-stu-id="ade25-103">ISCardCmd::get\_ReplyStatusSW1 method</span></span>

<span data-ttu-id="ade25-104">\[La méthode **obtenir \_ ReplyStatusSW1** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="ade25-104">\[The **get\_ReplyStatusSW1** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ade25-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ade25-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ade25-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="ade25-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ade25-107">La méthode **obtenir \_ ReplyStatusSW1** récupère l’octet d’état de la [*réponse APDU*](../secgloss/r-gly.md) SW1.</span><span class="sxs-lookup"><span data-stu-id="ade25-107">The **get\_ReplyStatusSW1** method retrieves the [*reply APDUs*](../secgloss/r-gly.md) SW1 status byte.</span></span>

## <a name="syntax"></a><span data-ttu-id="ade25-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ade25-108">Syntax</span></span>


```C++
HRESULT get_ReplyStatusSW1(
  [out] LPBYTE pbySW1
);
```



## <a name="parameters"></a><span data-ttu-id="ade25-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ade25-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ade25-110">*pbySW1* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ade25-110">*pbySW1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ade25-111">Pointeur vers l’octet qui contient la valeur de l’octet SW1 sur le retour.</span><span class="sxs-lookup"><span data-stu-id="ade25-111">Pointer to the byte that contains the value of the SW1 byte on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ade25-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ade25-112">Return value</span></span>

<span data-ttu-id="ade25-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="ade25-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ade25-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ade25-114">Return code</span></span>                                                                                   | <span data-ttu-id="ade25-115">Description</span><span class="sxs-lookup"><span data-stu-id="ade25-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="ade25-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ade25-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ade25-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="ade25-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="ade25-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ade25-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ade25-119">Le paramètre *pbySW1* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ade25-119">The *pbySW1* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="ade25-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="ade25-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ade25-121">Un pointeur incorrect a été passé dans *pbySW1*.</span><span class="sxs-lookup"><span data-stu-id="ade25-121">A bad pointer was passed in *pbySW1*.</span></span><br/> |
| <dl> <span data-ttu-id="ade25-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="ade25-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ade25-123">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="ade25-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="ade25-124">Notes</span><span class="sxs-lookup"><span data-stu-id="ade25-124">Remarks</span></span>

<span data-ttu-id="ade25-125">L’octet d’État SW1 [*de la réponse APDU*](../secgloss/r-gly.md) est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ade25-125">The [*reply APDU's*](../secgloss/r-gly.md) SW1 status byte is read-only.</span></span>

<span data-ttu-id="ade25-126">Pour récupérer l’octet d’État SW2 de la réponse APDU, appelez [**obtenir \_ ReplyStatusSW2**](iscardcmd-get-replystatussw2.md).</span><span class="sxs-lookup"><span data-stu-id="ade25-126">To retrieve the reply APDU's SW2 status byte, call [**get\_ReplyStatusSW2**](iscardcmd-get-replystatussw2.md).</span></span>

<span data-ttu-id="ade25-127">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="ade25-127">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="ade25-128">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="ade25-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ade25-129">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ade25-129">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ade25-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="ade25-130">Examples</span></span>

<span data-ttu-id="ade25-131">L’exemple suivant montre comment récupérer l’octet d’État SW1 de la [*réponse APDU*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ade25-131">The following example shows how to retrieve the SW1 status byte of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="ade25-132">L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="ade25-132">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     bySW1;
HRESULT  hr;

// Retrieve the reply status SW1 byte.
hr = pISCardCmd->get_ReplyStatusSW1(&bySW1);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatusSW1\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="ade25-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ade25-133">Requirements</span></span>



| <span data-ttu-id="ade25-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ade25-134">Requirement</span></span> | <span data-ttu-id="ade25-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="ade25-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ade25-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ade25-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ade25-137">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ade25-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ade25-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ade25-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ade25-139">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ade25-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ade25-140">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="ade25-140">End of client support</span></span><br/>    | <span data-ttu-id="ade25-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ade25-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ade25-142">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="ade25-142">End of server support</span></span><br/>    | <span data-ttu-id="ade25-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ade25-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ade25-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="ade25-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="ade25-145"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="ade25-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="ade25-146">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ade25-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="ade25-147"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ade25-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ade25-148">DLL</span><span class="sxs-lookup"><span data-stu-id="ade25-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ade25-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ade25-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ade25-150">IID</span><span class="sxs-lookup"><span data-stu-id="ade25-150">IID</span></span><br/>                      | <span data-ttu-id="ade25-151">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="ade25-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="ade25-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ade25-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ade25-153">**Obtient \_ ReplyStatusSW2**</span><span class="sxs-lookup"><span data-stu-id="ade25-153">**get\_ReplyStatusSW2**</span></span>](iscardcmd-get-replystatussw2.md)
</dt> <dt>

[<span data-ttu-id="ade25-154">**Obtient \_ ReplyStatus**</span><span class="sxs-lookup"><span data-stu-id="ade25-154">**get\_ReplyStatus**</span></span>](iscardcmd-get-replystatus.md)
</dt> <dt>

[<span data-ttu-id="ade25-155">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="ade25-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
