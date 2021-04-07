---
description: La méthode GetProviderCardId récupère l’identificateur (GUID) du fournisseur de services principal pour la carte à puce spécifiée.
ms.assetid: 0008bb5a-872f-4e5d-9029-a863cd3eea00
title: 'ISCardDatabase :: GetProviderCardId, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.GetProviderCardId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9f361e83431fa7c6e0a0c2c0ea363bef7e487738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758824"
---
# <a name="iscarddatabasegetprovidercardid-method"></a><span data-ttu-id="98f11-103">ISCardDatabase :: GetProviderCardId, méthode</span><span class="sxs-lookup"><span data-stu-id="98f11-103">ISCardDatabase::GetProviderCardId method</span></span>

<span data-ttu-id="98f11-104">\[La méthode **GetProviderCardId** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="98f11-104">\[The **GetProviderCardId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="98f11-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="98f11-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="98f11-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="98f11-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="98f11-107">La méthode **GetProviderCardId** récupère l’identificateur (Guid) du [*fournisseur de services principal*](../secgloss/p-gly.md) pour la [*carte à puce*](../secgloss/s-gly.md)spécifiée.</span><span class="sxs-lookup"><span data-stu-id="98f11-107">The **GetProviderCardId** method retrieves the identifier (GUID) of the [*primary service provider*](../secgloss/p-gly.md) for the specified [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="98f11-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98f11-108">Syntax</span></span>


```C++
HRESULT GetProviderCardId(
  [in]  BSTR   bstrCardName,
  [out] LPGUID *ppguidProviderId
);
```



## <a name="parameters"></a><span data-ttu-id="98f11-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98f11-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98f11-110">*bstrCardName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="98f11-110">*bstrCardName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98f11-111">Nom de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="98f11-111">Name of the smart card.</span></span>

</dd> <dt>

<span data-ttu-id="98f11-112">*ppguidProviderId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="98f11-112">*ppguidProviderId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98f11-113">Pointeur vers l’identificateur (GUID) du fournisseur de services principal en cas de réussite ; **Null** si l’opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="98f11-113">Pointer to the primary service provider's identifier (GUID) if successful; **NULL** if operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98f11-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="98f11-114">Return value</span></span>

<span data-ttu-id="98f11-115">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="98f11-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="98f11-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="98f11-116">Return code</span></span>                                                                                   | <span data-ttu-id="98f11-117">Description</span><span class="sxs-lookup"><span data-stu-id="98f11-117">Description</span></span>                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="98f11-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="98f11-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="98f11-119">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="98f11-119">Operation completed successfully.</span></span><br/>               |
| <dl> <span data-ttu-id="98f11-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="98f11-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="98f11-121">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="98f11-121">Invalid parameter.</span></span><br/>                              |
| <dl> <span data-ttu-id="98f11-122"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="98f11-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="98f11-123">Un pointeur incorrect a été passé dans *ppguidProviderId*.</span><span class="sxs-lookup"><span data-stu-id="98f11-123">A bad pointer was passed in *ppguidProviderId*.</span></span><br/> |
| <dl> <span data-ttu-id="98f11-124"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="98f11-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="98f11-125">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="98f11-125">Out of memory.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="98f11-126">Notes</span><span class="sxs-lookup"><span data-stu-id="98f11-126">Remarks</span></span>

<span data-ttu-id="98f11-127">Pour répertorier les interfaces de la carte à puce, appelez [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md).</span><span class="sxs-lookup"><span data-stu-id="98f11-127">To list the interfaces of the smart card, call [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md).</span></span>

<span data-ttu-id="98f11-128">Pour récupérer toutes les [*cartes à puce*](../secgloss/s-gly.md)connues, les lecteurs et les [*groupes*](../secgloss/r-gly.md) de [*lecteurs*](../secgloss/r-gly.md) appellent respectivement [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md)et [**ListReaderGroups**](iscarddatabase-listreadergroups.md) .</span><span class="sxs-lookup"><span data-stu-id="98f11-128">To retrieve all known [*smart cards*](../secgloss/s-gly.md), [*readers*](../secgloss/r-gly.md) and [*reader groups*](../secgloss/r-gly.md) call [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md), and [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="98f11-129">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardDatabase**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="98f11-129">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="98f11-130">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="98f11-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="98f11-131">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="98f11-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="98f11-132">Exemples</span><span class="sxs-lookup"><span data-stu-id="98f11-132">Examples</span></span>

<span data-ttu-id="98f11-133">L’exemple suivant montre comment récupérer l’identificateur du fournisseur de services principal pour la carte à puce spécifiée.</span><span class="sxs-lookup"><span data-stu-id="98f11-133">The following example shows retrieving the identifier of the primary service provider for the specified smart card.</span></span>


```C++
BSTR     bstrCard = NULL;
LPGUID   pguidProvId = NULL;
HRESULT  hr;

bstrCard = SysAllocString(L"My Card");
hr = pISCDataBase->GetProviderCardId(bstrCard,&pguidProvId);
if (FAILED(hr))
{
   printf("Failed GetProviderCardId\n");
}
else
{
    // Use pguidProvId as needed.
}

// Free BSTR when done.
if ( NULL != bstrCard )
{
    SysFreeString(bstrCard);
    bstrCard=NULL;
}
```



## <a name="requirements"></a><span data-ttu-id="98f11-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98f11-134">Requirements</span></span>



| <span data-ttu-id="98f11-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98f11-135">Requirement</span></span> | <span data-ttu-id="98f11-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="98f11-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98f11-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98f11-137">Minimum supported client</span></span><br/> | <span data-ttu-id="98f11-138">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98f11-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="98f11-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98f11-139">Minimum supported server</span></span><br/> | <span data-ttu-id="98f11-140">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98f11-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="98f11-141">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="98f11-141">End of client support</span></span><br/>    | <span data-ttu-id="98f11-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="98f11-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="98f11-143">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="98f11-143">End of server support</span></span><br/>    | <span data-ttu-id="98f11-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="98f11-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="98f11-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="98f11-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="98f11-146"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="98f11-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="98f11-147">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="98f11-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="98f11-148"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="98f11-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="98f11-149">DLL</span><span class="sxs-lookup"><span data-stu-id="98f11-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98f11-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98f11-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="98f11-151">IID</span><span class="sxs-lookup"><span data-stu-id="98f11-151">IID</span></span><br/>                      | <span data-ttu-id="98f11-152">IID \_ ISCardDatabase est défini en tant que 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="98f11-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="98f11-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98f11-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98f11-154">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="98f11-154">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="98f11-155">**ListCardInterfaces**</span><span class="sxs-lookup"><span data-stu-id="98f11-155">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[<span data-ttu-id="98f11-156">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="98f11-156">**ListCards**</span></span>](iscarddatabase-listcards.md)
</dt> <dt>

[<span data-ttu-id="98f11-157">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="98f11-157">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> <dt>

[<span data-ttu-id="98f11-158">**ListReaders**</span><span class="sxs-lookup"><span data-stu-id="98f11-158">**ListReaders**</span></span>](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
