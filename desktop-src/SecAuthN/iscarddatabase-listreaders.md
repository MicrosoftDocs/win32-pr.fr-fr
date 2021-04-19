---
description: La méthode ListReaders récupère les noms des lecteurs de carte à puce inscrits dans la base de données de la carte à puce.
ms.assetid: e1ca85a1-9206-4c09-ba0f-10b60e472dfb
title: 'ISCardDatabase :: ListReaders, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListReaders
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dcd78066a95c69b75d5089ba1683e5c937cb7414
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514186"
---
# <a name="iscarddatabaselistreaders-method"></a><span data-ttu-id="5f62e-103">ISCardDatabase :: ListReaders, méthode</span><span class="sxs-lookup"><span data-stu-id="5f62e-103">ISCardDatabase::ListReaders method</span></span>

<span data-ttu-id="5f62e-104">\[La méthode **ListReaders** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="5f62e-104">\[The **ListReaders** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5f62e-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="5f62e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5f62e-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="5f62e-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="5f62e-107">La méthode **ListReaders** récupère les noms des [*lecteurs*](../secgloss/r-gly.md) de carte à puce inscrits dans la [*base de données de la carte à puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5f62e-107">The **ListReaders** method retrieves the names of the smart card [*readers*](../secgloss/r-gly.md) registered in the [*smart card database*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5f62e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f62e-108">Syntax</span></span>


```C++
HRESULT ListReaders(
  [in]  LONG        localeId,
  [out] LPSAFEARRAY *ppReaders
);
```



## <a name="parameters"></a><span data-ttu-id="5f62e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f62e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f62e-110">*LocaleID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f62e-110">*localeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f62e-111">ID de localisation de la langue.</span><span class="sxs-lookup"><span data-stu-id="5f62e-111">Language localization ID.</span></span>

</dd> <dt>

<span data-ttu-id="5f62e-112">*ppReaders* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5f62e-112">*ppReaders* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f62e-113">Pointeur vers un SAFEARRAY de BSTR qui contient les noms des lecteurs de carte à puce en cas de réussite ; **Null** si l’opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="5f62e-113">Pointer to a SAFEARRAY of BSTRs that contains the names of the smart card readers if successful; **NULL** if the operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f62e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5f62e-114">Return value</span></span>

<span data-ttu-id="5f62e-115">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="5f62e-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="5f62e-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5f62e-116">Return code</span></span>                                                                                   | <span data-ttu-id="5f62e-117">Description</span><span class="sxs-lookup"><span data-stu-id="5f62e-117">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="5f62e-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5f62e-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5f62e-119">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="5f62e-119">Operation completed successfully.</span></span><br/>        |
| <dl> <span data-ttu-id="5f62e-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5f62e-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="5f62e-121">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="5f62e-121">Invalid parameter.</span></span><br/>                       |
| <dl> <span data-ttu-id="5f62e-122"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="5f62e-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="5f62e-123">Un pointeur incorrect a été passé dans *ppReaders*.</span><span class="sxs-lookup"><span data-stu-id="5f62e-123">A bad pointer was passed in *ppReaders*.</span></span><br/> |
| <dl> <span data-ttu-id="5f62e-124"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="5f62e-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5f62e-125">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="5f62e-125">Out of memory.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="5f62e-126">Notes</span><span class="sxs-lookup"><span data-stu-id="5f62e-126">Remarks</span></span>

<span data-ttu-id="5f62e-127">Pour récupérer toutes les [*cartes à puce*](../secgloss/s-gly.md) ou les [*groupes de lecteurs*](../secgloss/r-gly.md)connus, appelez [**ListCards**](iscarddatabase-listcards.md) ou [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectivement.</span><span class="sxs-lookup"><span data-stu-id="5f62e-127">To retrieve all known [*smart cards*](../secgloss/s-gly.md) or [*reader groups*](../secgloss/r-gly.md), call [**ListCards**](iscarddatabase-listcards.md) or [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="5f62e-128">Pour récupérer le [*fournisseur de services principal*](../secgloss/p-gly.md) ou les interfaces d’une carte spécifique [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) ou [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="5f62e-128">To retrieve the [*primary service provider*](../secgloss/p-gly.md) or the interfaces of a specific card [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) or [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) respectively.</span></span>

<span data-ttu-id="5f62e-129">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardDatabase**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="5f62e-129">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="5f62e-130">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="5f62e-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="5f62e-131">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="5f62e-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5f62e-132">Exemples</span><span class="sxs-lookup"><span data-stu-id="5f62e-132">Examples</span></span>

<span data-ttu-id="5f62e-133">L’exemple suivant montre comment récupérer les noms des lecteurs de carte à puce inscrits dans la base de données de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="5f62e-133">The following example shows retrieving the names of the smart card readers registered in the smart card database.</span></span>


```C++
LPSAFEARRAY pReaders = NULL;
HRESULT     hr;

// Determine the reader groups.
hr = pISCDataBase->ListReaders(0x0409,  // English (US)
                               &pReaders);
if (FAILED(hr))
{
   printf("Failed ListReaders\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
}
```



## <a name="requirements"></a><span data-ttu-id="5f62e-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f62e-134">Requirements</span></span>



| <span data-ttu-id="5f62e-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f62e-135">Requirement</span></span> | <span data-ttu-id="5f62e-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f62e-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f62e-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f62e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5f62e-138">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f62e-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5f62e-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f62e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5f62e-140">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f62e-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5f62e-141">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="5f62e-141">End of client support</span></span><br/>    | <span data-ttu-id="5f62e-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5f62e-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="5f62e-143">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="5f62e-143">End of server support</span></span><br/>    | <span data-ttu-id="5f62e-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5f62e-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="5f62e-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f62e-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f62e-146"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f62e-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="5f62e-147">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="5f62e-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="5f62e-148"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5f62e-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5f62e-149">DLL</span><span class="sxs-lookup"><span data-stu-id="5f62e-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f62e-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f62e-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5f62e-151">IID</span><span class="sxs-lookup"><span data-stu-id="5f62e-151">IID</span></span><br/>                      | <span data-ttu-id="5f62e-152">IID \_ ISCardDatabase est défini en tant que 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="5f62e-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="5f62e-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f62e-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f62e-154">**GetProviderCardId**</span><span class="sxs-lookup"><span data-stu-id="5f62e-154">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[<span data-ttu-id="5f62e-155">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="5f62e-155">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="5f62e-156">**ListCardInterfaces**</span><span class="sxs-lookup"><span data-stu-id="5f62e-156">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[<span data-ttu-id="5f62e-157">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="5f62e-157">**ListCards**</span></span>](iscarddatabase-listcards.md)
</dt> <dt>

[<span data-ttu-id="5f62e-158">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="5f62e-158">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> </dl>

 

 
