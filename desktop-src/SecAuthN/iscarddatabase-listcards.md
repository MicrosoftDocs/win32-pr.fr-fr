---
description: La méthode ListCards récupère tous les noms de carte à puce qui correspondent aux identificateurs d’interface (GUID) spécifiés, à la chaîne ATR spécifiée, ou aux deux.
ms.assetid: a1cf8186-0746-4c4d-917d-40d6c3542036
title: 'ISCardDatabase :: ListCards, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCards
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e8a5bf56aa27a044d29e2e0153698bfefe69e1d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751684"
---
# <a name="iscarddatabaselistcards-method"></a><span data-ttu-id="35eae-103">ISCardDatabase :: ListCards, méthode</span><span class="sxs-lookup"><span data-stu-id="35eae-103">ISCardDatabase::ListCards method</span></span>

<span data-ttu-id="35eae-104">\[La méthode **ListCards** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="35eae-104">\[The **ListCards** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="35eae-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="35eae-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="35eae-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="35eae-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="35eae-107">La méthode **ListCards** récupère tous les noms de carte à puce qui correspondent aux identificateurs d’interface (Guid) spécifiés, à la [*chaîne ATR*](../secgloss/a-gly.md)spécifiée, ou aux deux.</span><span class="sxs-lookup"><span data-stu-id="35eae-107">The **ListCards** method retrieves all of the smart card names that match the specified interface identifiers (GUIDs), the specified [*ATR string*](../secgloss/a-gly.md), or both.</span></span>

## <a name="syntax"></a><span data-ttu-id="35eae-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35eae-108">Syntax</span></span>


```C++
HRESULT ListCards(
  [in]  LPBYTEBUFFER pAtr,
  [in]  LPSAFEARRAY  pInterfaceGuids,
  [in]  LONG         localeId,
  [out] LPSAFEARRAY  *ppCardNames
);
```



## <a name="parameters"></a><span data-ttu-id="35eae-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35eae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35eae-110">*pAtr* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="35eae-110">*pAtr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35eae-111">Pointeur désignant une chaîne rar de [*carte à puce*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="35eae-111">Pointer to a [*smart card*](../secgloss/s-gly.md) ATR string.</span></span> <span data-ttu-id="35eae-112">La chaîne ATR doit être empaquetée dans un [**IByteBuffer**](ibytebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="35eae-112">The ATR string must be packaged into an [**IByteBuffer**](ibytebuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="35eae-113">*pInterfaceGuids* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="35eae-113">*pInterfaceGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35eae-114">Pointeur vers un SAFEARRAY d’identificateurs d’interface COM (GUID) au format BSTR.</span><span class="sxs-lookup"><span data-stu-id="35eae-114">Pointer to a SAFEARRAY of COM interface identifiers (GUIDs) in BSTR format.</span></span>

</dd> <dt>

<span data-ttu-id="35eae-115">*LocaleID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="35eae-115">*localeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35eae-116">Identificateur de localisation de langue.</span><span class="sxs-lookup"><span data-stu-id="35eae-116">Language localization identifier.</span></span>

</dd> <dt>

<span data-ttu-id="35eae-117">*ppCardNames* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="35eae-117">*ppCardNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35eae-118">Pointeur vers un SAFEARRAY de BSTR qui contient les noms des cartes à puce qui ont respecté les paramètres de recherche en cas de réussite ; **Null** si l’opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="35eae-118">Pointer to a SAFEARRAY of BSTRs that contains the names of the smart cards that satisfied the search parameters if successful; **NULL** if the operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35eae-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35eae-119">Return value</span></span>

<span data-ttu-id="35eae-120">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="35eae-120">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="35eae-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="35eae-121">Return code</span></span>                                                                                   | <span data-ttu-id="35eae-122">Description</span><span class="sxs-lookup"><span data-stu-id="35eae-122">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="35eae-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="35eae-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="35eae-124">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="35eae-124">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="35eae-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="35eae-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="35eae-126">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="35eae-126">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="35eae-127"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="35eae-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="35eae-128">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="35eae-128">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="35eae-129"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="35eae-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="35eae-130">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="35eae-130">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="35eae-131">Notes</span><span class="sxs-lookup"><span data-stu-id="35eae-131">Remarks</span></span>

<span data-ttu-id="35eae-132">Pour récupérer tous les [*lecteurs ou lecteurs*](../secgloss/r-gly.md) [*connus, appelez*](../secgloss/r-gly.md) [**ListReaders**](iscarddatabase-listreaders.md) ou [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectivement.</span><span class="sxs-lookup"><span data-stu-id="35eae-132">To retrieve all known [*readers*](../secgloss/r-gly.md) or [*reader*](../secgloss/r-gly.md), call [**ListReaders**](iscarddatabase-listreaders.md) or [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="35eae-133">Pour récupérer le [*service principal*](../secgloss/p-gly.md) ou les interfaces d’une carte spécifique [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) ou [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="35eae-133">To retrieve the [*primary service*](../secgloss/p-gly.md) or the interfaces of a specific card [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) or [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) respectively.</span></span>

<span data-ttu-id="35eae-134">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardDatabase**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="35eae-134">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="35eae-135">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="35eae-135">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="35eae-136">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="35eae-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="35eae-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="35eae-137">Examples</span></span>

<span data-ttu-id="35eae-138">L’exemple suivant montre l’extraction des noms de carte à puce qui correspondent à la chaîne ATR spécifiée.</span><span class="sxs-lookup"><span data-stu-id="35eae-138">The following example shows retrieving the smart card names that match the specified ATR string.</span></span>


```C++
// Define or determine byAtr as needed for your ATR use.
BYTE byAtr[] = {0x3b,0x27,0x00,0x80,0x65,0xa2,0x0c,0x01,0x01,0x37};
LPSAFEARRAY pSafeArray = NULL;
HRESULT          hr;

// pIByteBuff is a pointer to an instance of IByteBuffer.
hr = pIByteBuff->Initialize(sizeof(byAtr), byAtr);

// Call the function for the specified ATR.
hr = pISCDataBase->ListCards(pIByteBuff,
                             NULL,
                             0,
                             &pSafeArray);
if (FAILED(hr))
{
   printf("Failed ListCards\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="35eae-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35eae-139">Requirements</span></span>



| <span data-ttu-id="35eae-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35eae-140">Requirement</span></span> | <span data-ttu-id="35eae-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="35eae-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35eae-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35eae-142">Minimum supported client</span></span><br/> | <span data-ttu-id="35eae-143">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35eae-143">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="35eae-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35eae-144">Minimum supported server</span></span><br/> | <span data-ttu-id="35eae-145">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35eae-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="35eae-146">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="35eae-146">End of client support</span></span><br/>    | <span data-ttu-id="35eae-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="35eae-147">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="35eae-148">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="35eae-148">End of server support</span></span><br/>    | <span data-ttu-id="35eae-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="35eae-149">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="35eae-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="35eae-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="35eae-151"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="35eae-151"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="35eae-152">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="35eae-152">Type library</span></span><br/>             | <dl> <span data-ttu-id="35eae-153"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="35eae-153"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="35eae-154">DLL</span><span class="sxs-lookup"><span data-stu-id="35eae-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35eae-155"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35eae-155"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="35eae-156">IID</span><span class="sxs-lookup"><span data-stu-id="35eae-156">IID</span></span><br/>                      | <span data-ttu-id="35eae-157">IID \_ ISCardDatabase est défini en tant que 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="35eae-157">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="35eae-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35eae-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35eae-159">**GetProviderCardId**</span><span class="sxs-lookup"><span data-stu-id="35eae-159">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[<span data-ttu-id="35eae-160">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="35eae-160">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="35eae-161">**ListCardInterfaces**</span><span class="sxs-lookup"><span data-stu-id="35eae-161">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[<span data-ttu-id="35eae-162">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="35eae-162">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> <dt>

[<span data-ttu-id="35eae-163">**ListReaders**</span><span class="sxs-lookup"><span data-stu-id="35eae-163">**ListReaders**</span></span>](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
