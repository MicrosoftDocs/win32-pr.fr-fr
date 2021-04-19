---
description: Exécute une opération d’écriture et de lecture sur l’objet de commande de carte à puce (unité de données de protocole d’application).
ms.assetid: 4dc8ed56-97e0-4c05-a70a-ea2ffd976d47
title: 'ISCard :: transaction, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Transaction
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2abe9d4acd4d59019fe0c8ce122baa12fde06f2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534413"
---
# <a name="iscardtransaction-method"></a><span data-ttu-id="883ac-103">ISCard :: transaction, méthode</span><span class="sxs-lookup"><span data-stu-id="883ac-103">ISCard::Transaction method</span></span>

<span data-ttu-id="883ac-104">\[La méthode de **transaction** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="883ac-104">\[The **Transaction** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="883ac-105">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="883ac-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="883ac-106">La méthode de **transaction** exécute une opération d’écriture et de lecture sur l’objet de commande de [*carte à puce*](../secgloss/s-gly.md) ([*unité de données de protocole d’application*](../secgloss/a-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="883ac-106">The **Transaction** method executes a write and read operation on the [*smart card*](../secgloss/s-gly.md) command ([*application protocol data unit*](../secgloss/a-gly.md)) object.</span></span> <span data-ttu-id="883ac-107">La chaîne de réponse de la carte à puce pour la chaîne de commande définie dans la carte qui a été envoyée à la carte à puce est accessible après le retour de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="883ac-107">The reply string from the smart card for the command string defined in the card that was sent to the smart card will be accessible after this function returns.</span></span>

## <a name="syntax"></a><span data-ttu-id="883ac-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="883ac-108">Syntax</span></span>


```C++
HRESULT Transaction(
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="883ac-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="883ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="883ac-110">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="883ac-110">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="883ac-111">Pointeur vers l’objet de commande de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="883ac-111">A pointer to the smart card command object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="883ac-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="883ac-112">Return value</span></span>

<span data-ttu-id="883ac-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="883ac-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="883ac-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="883ac-114">Return code</span></span>                                                                                   | <span data-ttu-id="883ac-115">Description</span><span class="sxs-lookup"><span data-stu-id="883ac-115">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="883ac-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="883ac-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="883ac-117">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="883ac-117">The operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="883ac-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="883ac-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="883ac-119">Le paramètre *ppCmd* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="883ac-119">The *ppCmd* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="883ac-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="883ac-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="883ac-121">Un pointeur incorrect a été passé dans *ppCmd*.</span><span class="sxs-lookup"><span data-stu-id="883ac-121">A bad pointer was passed in *ppCmd*.</span></span><br/>          |
| <dl> <span data-ttu-id="883ac-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="883ac-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="883ac-123">La mémoire pour satisfaire la demande n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="883ac-123">Memory to satisfy the request is unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="883ac-124">Notes</span><span class="sxs-lookup"><span data-stu-id="883ac-124">Remarks</span></span>

<span data-ttu-id="883ac-125">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="883ac-125">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="883ac-126">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="883ac-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="883ac-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="883ac-127">Examples</span></span>

<span data-ttu-id="883ac-128">L’exemple suivant illustre l’exécution d’une opération d’écriture et de lecture sur l’objet de commande de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="883ac-128">The following example shows executing a write and read operation on the smart card command object.</span></span>


```C++
HRESULT    hr;

// pISCard is a pointer to an instance of ISCard.
// pISCardCmd is a pointer to an instance of ISCardCmd,
// and ISCardCmd::BuildCmd has already been called.
hr = pISCard->Transaction(&pISCardCmd);
if (FAILED(hr))
{
    printf("Failed ISCard::Transaction\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="883ac-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="883ac-129">Requirements</span></span>



| <span data-ttu-id="883ac-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="883ac-130">Requirement</span></span> | <span data-ttu-id="883ac-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="883ac-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="883ac-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="883ac-132">Minimum supported client</span></span><br/> | <span data-ttu-id="883ac-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="883ac-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="883ac-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="883ac-134">Minimum supported server</span></span><br/> | <span data-ttu-id="883ac-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="883ac-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="883ac-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="883ac-136">End of client support</span></span><br/>    | <span data-ttu-id="883ac-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="883ac-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="883ac-138">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="883ac-138">End of server support</span></span><br/>    | <span data-ttu-id="883ac-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="883ac-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="883ac-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="883ac-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="883ac-141"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="883ac-141"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="883ac-142">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="883ac-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="883ac-143"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="883ac-143"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="883ac-144">DLL</span><span class="sxs-lookup"><span data-stu-id="883ac-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="883ac-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="883ac-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="883ac-146">IID</span><span class="sxs-lookup"><span data-stu-id="883ac-146">IID</span></span><br/>                      | <span data-ttu-id="883ac-147">IID \_ ISCard est défini en tant que 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="883ac-147">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="883ac-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="883ac-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="883ac-149">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="883ac-149">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="883ac-150">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="883ac-150">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="883ac-151">**Dissocié**</span><span class="sxs-lookup"><span data-stu-id="883ac-151">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="883ac-152">**Obtient \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="883ac-152">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="883ac-153">**Obtient \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="883ac-153">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="883ac-154">**recevoir le \_ contexte**</span><span class="sxs-lookup"><span data-stu-id="883ac-154">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="883ac-155">**Obtient le \_ protocole**</span><span class="sxs-lookup"><span data-stu-id="883ac-155">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="883ac-156">**afficher l' \_ État**</span><span class="sxs-lookup"><span data-stu-id="883ac-156">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="883ac-157">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="883ac-157">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="883ac-158">**LockSCard**</span><span class="sxs-lookup"><span data-stu-id="883ac-158">**LockSCard**</span></span>](iscard-lockscard.md)
</dt> <dt>

[<span data-ttu-id="883ac-159">**Rattacher**</span><span class="sxs-lookup"><span data-stu-id="883ac-159">**ReAttach**</span></span>](iscard-reattach.md)
</dt> <dt>

[<span data-ttu-id="883ac-160">**UnlockSCard**</span><span class="sxs-lookup"><span data-stu-id="883ac-160">**UnlockSCard**</span></span>](iscard-unlockscard.md)
</dt> </dl>

 

 
