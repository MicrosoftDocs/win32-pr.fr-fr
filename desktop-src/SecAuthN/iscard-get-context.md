---
description: Récupère le handle de contexte du gestionnaire de ressources actuel. Cette méthode retourne ( \* pContext) = = NULL si aucun contexte n’a été établi.
ms.assetid: c031f53d-4670-4d48-934c-a1550f21c23a
title: 'ISCard :: get_Context, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Context
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8b5aba075d755b644a78cca23a827a70966f4ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867850"
---
# <a name="iscardget_context-method"></a><span data-ttu-id="1f05e-104">ISCard :: obtient le \_ contexte, méthode</span><span class="sxs-lookup"><span data-stu-id="1f05e-104">ISCard::get\_Context method</span></span>

<span data-ttu-id="1f05e-105">\[La méthode **obtenir le \_ contexte** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="1f05e-105">\[The **get\_Context** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1f05e-106">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1f05e-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1f05e-107">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="1f05e-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="1f05e-108">La méthode d’extraction de **\_ contexte** récupère le handle de [*contexte du gestionnaire de ressources*](../secgloss/r-gly.md) actuel.</span><span class="sxs-lookup"><span data-stu-id="1f05e-108">The **get\_Context** method retrieves the current [*resource manager context*](../secgloss/r-gly.md) handle.</span></span> <span data-ttu-id="1f05e-109">Cette méthode retourne ( \* *pContext*) = = **null** si aucun contexte n’a été établi.</span><span class="sxs-lookup"><span data-stu-id="1f05e-109">This method returns (\**pContext*) == **NULL** if no context has been established.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f05e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f05e-110">Syntax</span></span>


```C++
HRESULT get_Context(
  [out] HSCARDCONTEXT *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="1f05e-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f05e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f05e-112">*pContext* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1f05e-112">*pContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f05e-113">Pointeur vers le handle de contexte lors du retour.</span><span class="sxs-lookup"><span data-stu-id="1f05e-113">Pointer to the context handle on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f05e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1f05e-114">Return value</span></span>

<span data-ttu-id="1f05e-115">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="1f05e-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="1f05e-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1f05e-116">Return code</span></span>                                                                                  | <span data-ttu-id="1f05e-117">Description</span><span class="sxs-lookup"><span data-stu-id="1f05e-117">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="1f05e-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1f05e-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="1f05e-119">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="1f05e-119">Operation completed successfully.</span></span><br/>       |
| <dl> <span data-ttu-id="1f05e-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1f05e-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="1f05e-121">Le paramètre *pContext* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1f05e-121">The *pContext* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="1f05e-122"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="1f05e-122"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="1f05e-123">Un pointeur incorrect a été passé dans *pContext*.</span><span class="sxs-lookup"><span data-stu-id="1f05e-123">A bad pointer was passed in *pContext*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1f05e-124">Notes</span><span class="sxs-lookup"><span data-stu-id="1f05e-124">Remarks</span></span>

<span data-ttu-id="1f05e-125">Le contexte du gestionnaire de ressources est défini en appelant la fonction de [*carte à puce*](../secgloss/s-gly.md) [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext).</span><span class="sxs-lookup"><span data-stu-id="1f05e-125">The resource manager context is set by calling the [*smart card*](../secgloss/s-gly.md) function [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext).</span></span>

<span data-ttu-id="1f05e-126">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="1f05e-126">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="1f05e-127">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="1f05e-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1f05e-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="1f05e-128">Examples</span></span>

<span data-ttu-id="1f05e-129">L’exemple suivant montre comment récupérer le handle de [*contexte du gestionnaire de ressources*](../secgloss/r-gly.md) actuel.</span><span class="sxs-lookup"><span data-stu-id="1f05e-129">The following example shows retrieving the current [*resource manager context*](../secgloss/r-gly.md) handle.</span></span>


```C++
HSCARDCONTEXT  hCtx;
HRESULT        hr;

// Retrieve the smart card context.
hr = pISCard->get_Context(&hCtx);
if (FAILED(hr))
{
   printf("Failed get_Context\n");
   // Take other error handling action as needed.
}
// Use smart card context as needed.
```



## <a name="requirements"></a><span data-ttu-id="1f05e-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f05e-130">Requirements</span></span>



| <span data-ttu-id="1f05e-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f05e-131">Requirement</span></span> | <span data-ttu-id="1f05e-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f05e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f05e-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f05e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1f05e-134">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f05e-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1f05e-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f05e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1f05e-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f05e-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1f05e-137">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="1f05e-137">End of client support</span></span><br/>    | <span data-ttu-id="1f05e-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1f05e-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="1f05e-139">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="1f05e-139">End of server support</span></span><br/>    | <span data-ttu-id="1f05e-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1f05e-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="1f05e-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f05e-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f05e-142"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f05e-142"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="1f05e-143">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="1f05e-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="1f05e-144"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1f05e-144"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1f05e-145">DLL</span><span class="sxs-lookup"><span data-stu-id="1f05e-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f05e-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f05e-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1f05e-147">IID</span><span class="sxs-lookup"><span data-stu-id="1f05e-147">IID</span></span><br/>                      | <span data-ttu-id="1f05e-148">IID \_ ISCard est défini en tant que 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="1f05e-148">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="1f05e-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f05e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f05e-150">**Obtient \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="1f05e-150">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="1f05e-151">**Obtient \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="1f05e-151">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="1f05e-152">**Obtient le \_ protocole**</span><span class="sxs-lookup"><span data-stu-id="1f05e-152">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="1f05e-153">**afficher l' \_ État**</span><span class="sxs-lookup"><span data-stu-id="1f05e-153">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="1f05e-154">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="1f05e-154">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="1f05e-155">**SCardEstablishContext**</span><span class="sxs-lookup"><span data-stu-id="1f05e-155">**SCardEstablishContext**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext)
</dt> </dl>

 

 
