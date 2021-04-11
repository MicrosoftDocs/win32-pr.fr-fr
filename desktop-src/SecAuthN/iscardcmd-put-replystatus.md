---
description: Définit un nouveau mot d’état de message APDU de réponse.
ms.assetid: 17b498eb-2268-451a-9f5c-c53cb7e42019
title: ISCardCmd ::p ut_ReplyStatus, méthode (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ReplyStatus
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 55e6de81cd7e2c98b527d0852ea31a25f8256c68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112182"
---
# <a name="iscardcmdput_replystatus-method"></a><span data-ttu-id="6dc85-103">ISCardCmd ::p ut \_ ReplyStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="6dc85-103">ISCardCmd::put\_ReplyStatus method</span></span>

<span data-ttu-id="6dc85-104">\[La méthode **put \_ ReplyStatus** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="6dc85-104">\[The **put\_ReplyStatus** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6dc85-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6dc85-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6dc85-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="6dc85-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6dc85-107">La méthode **put \_ ReplyStatus** définit un nouveau mot d’état de message [*APDU de réponse*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="6dc85-107">The **put\_ReplyStatus** method sets a new [*reply APDU*](../secgloss/r-gly.md) message status word.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dc85-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6dc85-108">Syntax</span></span>


```C++
HRESULT put_ReplyStatus(
  [in] WORD wStatus
);
```



## <a name="parameters"></a><span data-ttu-id="6dc85-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6dc85-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dc85-110">*wStatus* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6dc85-110">*wStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dc85-111">Mot qui est l’État.</span><span class="sxs-lookup"><span data-stu-id="6dc85-111">Word that is the status.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dc85-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6dc85-112">Return value</span></span>

<span data-ttu-id="6dc85-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="6dc85-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6dc85-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6dc85-114">Return code</span></span>                                                                                   | <span data-ttu-id="6dc85-115">Description</span><span class="sxs-lookup"><span data-stu-id="6dc85-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="6dc85-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6dc85-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6dc85-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="6dc85-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="6dc85-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6dc85-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6dc85-119">Le paramètre *wStatus* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6dc85-119">The *wStatus* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="6dc85-120"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="6dc85-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6dc85-121">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="6dc85-121">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="6dc85-122">Notes</span><span class="sxs-lookup"><span data-stu-id="6dc85-122">Remarks</span></span>

<span data-ttu-id="6dc85-123">Pour récupérer le mot d’État du message de la réponse APDU, appelez la [**\_ ReplyStatus**](iscardcmd-get-replystatus.md).</span><span class="sxs-lookup"><span data-stu-id="6dc85-123">To get the reply APDU's message status word, call [**get\_ReplyStatus**](iscardcmd-get-replystatus.md).</span></span>

<span data-ttu-id="6dc85-124">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="6dc85-124">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="6dc85-125">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="6dc85-125">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6dc85-126">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6dc85-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6dc85-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="6dc85-127">Examples</span></span>

<span data-ttu-id="6dc85-128">L’exemple suivant montre comment définir un nouveau mot d’état de message [*APDU de réponse*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="6dc85-128">The following example shows how to set a new [*reply APDU*](../secgloss/r-gly.md) message status word.</span></span> <span data-ttu-id="6dc85-129">L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="6dc85-129">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
WORD     wNewStatus = 0x0000;
HRESULT  hr;

// Set reply status.
hr = pISCardCmd->put_ReplyStatus(wNewStatus);
if (FAILED(hr))
{
  printf("Failed put_ReplyStatus\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="6dc85-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6dc85-130">Requirements</span></span>



| <span data-ttu-id="6dc85-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6dc85-131">Requirement</span></span> | <span data-ttu-id="6dc85-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="6dc85-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6dc85-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6dc85-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6dc85-134">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6dc85-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6dc85-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6dc85-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6dc85-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6dc85-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6dc85-137">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="6dc85-137">End of client support</span></span><br/>    | <span data-ttu-id="6dc85-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6dc85-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6dc85-139">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="6dc85-139">End of server support</span></span><br/>    | <span data-ttu-id="6dc85-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6dc85-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6dc85-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="6dc85-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="6dc85-142"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="6dc85-142"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="6dc85-143">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6dc85-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="6dc85-144"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6dc85-144"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6dc85-145">DLL</span><span class="sxs-lookup"><span data-stu-id="6dc85-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dc85-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6dc85-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6dc85-147">IID</span><span class="sxs-lookup"><span data-stu-id="6dc85-147">IID</span></span><br/>                      | <span data-ttu-id="6dc85-148">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="6dc85-148">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="6dc85-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6dc85-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dc85-150">**Obtient \_ ReplyStatus**</span><span class="sxs-lookup"><span data-stu-id="6dc85-150">**get\_ReplyStatus**</span></span>](iscardcmd-get-replystatus.md)
</dt> <dt>

[<span data-ttu-id="6dc85-151">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="6dc85-151">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
