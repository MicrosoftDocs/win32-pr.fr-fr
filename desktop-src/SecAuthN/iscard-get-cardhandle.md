---
description: Récupère le handle d’une carte à puce connectée. Cette méthode retourne ( \* pHandle) = = NULL si elle n’est pas connectée.
ms.assetid: f03f8f25-b2e4-4fae-b7d2-bb0f1a7cd987
title: 'ISCard :: get_CardHandle, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_CardHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d7e945f0f4a300dfed444c7e8f5921b806d96b1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950951"
---
# <a name="iscardget_cardhandle-method"></a><span data-ttu-id="f01b4-104">ISCard :: \_ CardHandle, méthode</span><span class="sxs-lookup"><span data-stu-id="f01b4-104">ISCard::get\_CardHandle method</span></span>

<span data-ttu-id="f01b4-105">\[La méthode **obtenir \_ CardHandle** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="f01b4-105">\[The **get\_CardHandle** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f01b4-106">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f01b4-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f01b4-107">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="f01b4-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f01b4-108">La méthode **obtenir \_ CardHandle** récupère le handle d’une [*carte à puce*](../secgloss/s-gly.md)connectée.</span><span class="sxs-lookup"><span data-stu-id="f01b4-108">The **get\_CardHandle** method retrieves the handle for a connected [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="f01b4-109">Cette méthode retourne ( \* pHandle) = = **null** si elle n’est pas connectée.</span><span class="sxs-lookup"><span data-stu-id="f01b4-109">This method returns (\*pHandle) == **NULL** if not connected.</span></span>

## <a name="syntax"></a><span data-ttu-id="f01b4-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f01b4-110">Syntax</span></span>


```C++
HRESULT get_CardHandle(
  [out] HSCARD *pHandle
);
```



## <a name="parameters"></a><span data-ttu-id="f01b4-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f01b4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f01b4-112">*pHandle* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f01b4-112">*pHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f01b4-113">Pointeur vers le handle de carte au retour.</span><span class="sxs-lookup"><span data-stu-id="f01b4-113">Pointer to the card handle on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f01b4-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f01b4-114">Return value</span></span>

<span data-ttu-id="f01b4-115">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="f01b4-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="f01b4-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f01b4-116">Return code</span></span>                                                                                  | <span data-ttu-id="f01b4-117">Description</span><span class="sxs-lookup"><span data-stu-id="f01b4-117">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="f01b4-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f01b4-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="f01b4-119">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="f01b4-119">Operation completed successfully.</span></span><br/>      |
| <dl> <span data-ttu-id="f01b4-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f01b4-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="f01b4-121">Le paramètre *pHandle* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f01b4-121">The *pHandle* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="f01b4-122"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="f01b4-122"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="f01b4-123">Un pointeur incorrect a été passé dans *pHandle*.</span><span class="sxs-lookup"><span data-stu-id="f01b4-123">A bad pointer was passed in *pHandle*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f01b4-124">Notes</span><span class="sxs-lookup"><span data-stu-id="f01b4-124">Remarks</span></span>

<span data-ttu-id="f01b4-125">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="f01b4-125">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="f01b4-126">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="f01b4-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f01b4-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="f01b4-127">Examples</span></span>

<span data-ttu-id="f01b4-128">L’exemple suivant montre la récupération du descripteur de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="f01b4-128">The following example shows retrieving the smart card handle.</span></span>


```C++
HSCARD   hSC;
HRESULT  hr;

// Retrieve the card handle.
hr = pISCard->get_CardHandle(&hSC);
if (FAILED(hr))
{
   printf("Failed get_CardHandle\n");
   // Take other error handling action as needed.
}
// Use card handle as needed.
```



## <a name="requirements"></a><span data-ttu-id="f01b4-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f01b4-129">Requirements</span></span>



| <span data-ttu-id="f01b4-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f01b4-130">Requirement</span></span> | <span data-ttu-id="f01b4-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f01b4-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f01b4-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f01b4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f01b4-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f01b4-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f01b4-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f01b4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f01b4-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f01b4-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f01b4-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f01b4-136">End of client support</span></span><br/>    | <span data-ttu-id="f01b4-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f01b4-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f01b4-138">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="f01b4-138">End of server support</span></span><br/>    | <span data-ttu-id="f01b4-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f01b4-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f01b4-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="f01b4-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f01b4-141"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="f01b4-141"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="f01b4-142">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f01b4-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="f01b4-143"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f01b4-143"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f01b4-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f01b4-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f01b4-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f01b4-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f01b4-146">IID</span><span class="sxs-lookup"><span data-stu-id="f01b4-146">IID</span></span><br/>                      | <span data-ttu-id="f01b4-147">IID \_ ISCard est défini en tant que 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="f01b4-147">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="f01b4-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f01b4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f01b4-149">**Obtient \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="f01b4-149">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="f01b4-150">**recevoir le \_ contexte**</span><span class="sxs-lookup"><span data-stu-id="f01b4-150">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="f01b4-151">**Obtient le \_ protocole**</span><span class="sxs-lookup"><span data-stu-id="f01b4-151">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="f01b4-152">**afficher l' \_ État**</span><span class="sxs-lookup"><span data-stu-id="f01b4-152">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="f01b4-153">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="f01b4-153">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
