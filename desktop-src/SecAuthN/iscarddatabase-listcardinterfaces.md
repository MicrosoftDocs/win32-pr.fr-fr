---
description: La méthode ListCardInterfaces récupère les identificateurs (GUID) de toutes les interfaces prises en charge pour la carte à puce spécifiée.
ms.assetid: c9dfd17e-f4a9-47d3-974e-66e78bc4b06a
title: 'ISCardDatabase :: ListCardInterfaces, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCardInterfaces
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d52324edd4a502388ac6064de07a6ab58a68074d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201244"
---
# <a name="iscarddatabaselistcardinterfaces-method"></a><span data-ttu-id="f67c2-103">ISCardDatabase :: ListCardInterfaces, méthode</span><span class="sxs-lookup"><span data-stu-id="f67c2-103">ISCardDatabase::ListCardInterfaces method</span></span>

<span data-ttu-id="f67c2-104">\[La méthode **ListCardInterfaces** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="f67c2-104">\[The **ListCardInterfaces** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f67c2-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f67c2-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f67c2-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="f67c2-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f67c2-107">La méthode **ListCardInterfaces** récupère les identificateurs (Guid) de toutes les interfaces prises en charge pour la [*carte à puce*](../secgloss/s-gly.md)spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f67c2-107">The **ListCardInterfaces** method retrieves the identifiers (GUIDs) of all the interfaces supported for the specified [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f67c2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f67c2-108">Syntax</span></span>


```C++
HRESULT ListCardInterfaces(
  [in]  BSTR        bstrCardName,
  [out] LPSAFEARRAY *ppInterfaceGuids
);
```



## <a name="parameters"></a><span data-ttu-id="f67c2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f67c2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f67c2-110">*bstrCardName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f67c2-110">*bstrCardName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f67c2-111">Nom de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="f67c2-111">Name of the smart card.</span></span>

</dd> <dt>

<span data-ttu-id="f67c2-112">*ppInterfaceGuids* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f67c2-112">*ppInterfaceGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f67c2-113">Pointeur vers les GUID d’interface en cas de réussite ; **Null** si l’opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="f67c2-113">Pointer to the interface GUIDs if successful; **NULL** if operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f67c2-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f67c2-114">Return value</span></span>

<span data-ttu-id="f67c2-115">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="f67c2-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="f67c2-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f67c2-116">Return code</span></span>                                                                                   | <span data-ttu-id="f67c2-117">Description</span><span class="sxs-lookup"><span data-stu-id="f67c2-117">Description</span></span>                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="f67c2-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f67c2-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f67c2-119">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="f67c2-119">Operation completed successfully.</span></span><br/>               |
| <dl> <span data-ttu-id="f67c2-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f67c2-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f67c2-121">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="f67c2-121">Invalid parameter.</span></span><br/>                              |
| <dl> <span data-ttu-id="f67c2-122"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="f67c2-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f67c2-123">Un pointeur incorrect a été passé dans *ppInterfaceGuids*.</span><span class="sxs-lookup"><span data-stu-id="f67c2-123">A bad pointer was passed in *ppInterfaceGuids*.</span></span><br/> |
| <dl> <span data-ttu-id="f67c2-124"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="f67c2-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f67c2-125">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="f67c2-125">Out of memory.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="f67c2-126">Notes</span><span class="sxs-lookup"><span data-stu-id="f67c2-126">Remarks</span></span>

<span data-ttu-id="f67c2-127">Pour récupérer le [*fournisseur de services principal*](../secgloss/p-gly.md) de la carte à puce, appelez [**GetProviderCardId**](iscarddatabase-getprovidercardid.md).</span><span class="sxs-lookup"><span data-stu-id="f67c2-127">To retrieve the [*primary service provider*](../secgloss/p-gly.md) of the smart card, call [**GetProviderCardId**](iscarddatabase-getprovidercardid.md).</span></span>

<span data-ttu-id="f67c2-128">Pour récupérer toutes les [*cartes à puce*](../secgloss/s-gly.md)connues, les [*lecteurs*](../secgloss/r-gly.md)et les [*groupes*](../secgloss/r-gly.md) de lecteurs appellent respectivement [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md)et [**ListReaderGroups**](iscarddatabase-listreadergroups.md) .</span><span class="sxs-lookup"><span data-stu-id="f67c2-128">To retrieve all known [*smart cards*](../secgloss/s-gly.md), [*readers*](../secgloss/r-gly.md), and [*reader groups*](../secgloss/r-gly.md) call [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md), and [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="f67c2-129">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardDatabase**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="f67c2-129">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="f67c2-130">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="f67c2-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="f67c2-131">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="f67c2-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f67c2-132">Exemples</span><span class="sxs-lookup"><span data-stu-id="f67c2-132">Examples</span></span>

<span data-ttu-id="f67c2-133">L’exemple suivant montre l’extraction des identificateurs des interfaces prises en charge pour la carte à puce spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f67c2-133">The following example shows retrieving the identifiers of the interfaces supported for the specified smart card.</span></span>


```C++
BSTR         bstrCard = NULL;
LPSAFEARRAY  pGuids = NULL;
HRESULT      hr;

bstrCard = SysAllocString(L"GemSAFE");
// Call the function for the specified card.
hr = pISCDataBase->ListCardInterfaces(bstrCard,
                                      &pGuids);
if (FAILED(hr))
{
   printf("Failed ListCardInterfaces\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
   // Free BSTR when done.
   if (bstrCard)
       SysFreeString(bstrCard);
}
```



## <a name="requirements"></a><span data-ttu-id="f67c2-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f67c2-134">Requirements</span></span>



| <span data-ttu-id="f67c2-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f67c2-135">Requirement</span></span> | <span data-ttu-id="f67c2-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="f67c2-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f67c2-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f67c2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f67c2-138">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f67c2-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f67c2-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f67c2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f67c2-140">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f67c2-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f67c2-141">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f67c2-141">End of client support</span></span><br/>    | <span data-ttu-id="f67c2-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f67c2-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f67c2-143">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="f67c2-143">End of server support</span></span><br/>    | <span data-ttu-id="f67c2-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f67c2-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f67c2-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="f67c2-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="f67c2-146"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="f67c2-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="f67c2-147">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f67c2-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="f67c2-148"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f67c2-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f67c2-149">DLL</span><span class="sxs-lookup"><span data-stu-id="f67c2-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f67c2-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f67c2-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f67c2-151">IID</span><span class="sxs-lookup"><span data-stu-id="f67c2-151">IID</span></span><br/>                      | <span data-ttu-id="f67c2-152">IID \_ ISCardDatabase est défini en tant que 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="f67c2-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f67c2-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f67c2-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f67c2-154">**GetProviderCardId**</span><span class="sxs-lookup"><span data-stu-id="f67c2-154">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[<span data-ttu-id="f67c2-155">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="f67c2-155">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="f67c2-156">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="f67c2-156">**ListCards**</span></span>](iscarddatabase-listcards.md)
</dt> <dt>

[<span data-ttu-id="f67c2-157">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="f67c2-157">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> <dt>

[<span data-ttu-id="f67c2-158">**ListReaders**</span><span class="sxs-lookup"><span data-stu-id="f67c2-158">**ListReaders**</span></span>](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
