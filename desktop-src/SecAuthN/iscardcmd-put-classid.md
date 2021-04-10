---
description: Définit un nouvel identificateur de classe dans l’unité de données du protocole d’application (APDU).
ms.assetid: 7e7d42f2-2858-4b37-a7d5-a919e3e005da
title: ISCardCmd ::p ut_ClassId, méthode (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ed4b1f273ebe9ea0a5e105ec3d88fc8446f7a831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951420"
---
# <a name="iscardcmdput_classid-method"></a><span data-ttu-id="0cfb3-103">ISCardCmd ::p ut \_ ClassID, méthode</span><span class="sxs-lookup"><span data-stu-id="0cfb3-103">ISCardCmd::put\_ClassId method</span></span>

<span data-ttu-id="0cfb3-104">\[La méthode **put \_ ClassID** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="0cfb3-104">\[The **put\_ClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0cfb3-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0cfb3-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0cfb3-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="0cfb3-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="0cfb3-107">La méthode **put \_ ClassID** définit un nouvel identificateur de classe dans l' [*unité de données du protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="0cfb3-107">The **put\_ClassId** method sets a new class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="0cfb3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0cfb3-108">Syntax</span></span>


```C++
HRESULT put_ClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a><span data-ttu-id="0cfb3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0cfb3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cfb3-110">*byClass* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0cfb3-110">*byClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfb3-111">Octet qui représente l’identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="0cfb3-111">The byte that represents the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cfb3-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0cfb3-112">Return value</span></span>

<span data-ttu-id="0cfb3-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="0cfb3-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="0cfb3-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0cfb3-114">Return code</span></span>                                                                                   | <span data-ttu-id="0cfb3-115">Description</span><span class="sxs-lookup"><span data-stu-id="0cfb3-115">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0cfb3-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0cfb3-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0cfb3-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="0cfb3-117">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="0cfb3-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0cfb3-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0cfb3-119">*ByClass* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0cfb3-119">The *byClass* is not valid.</span></span><br/>       |
| <dl> <span data-ttu-id="0cfb3-120"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="0cfb3-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0cfb3-121">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="0cfb3-121">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="0cfb3-122">Notes</span><span class="sxs-lookup"><span data-stu-id="0cfb3-122">Remarks</span></span>

<span data-ttu-id="0cfb3-123">Pour récupérer l’identificateur de classe actuel, appelez [**obtenir \_ ClassID**](iscardcmd-get-classid.md).</span><span class="sxs-lookup"><span data-stu-id="0cfb3-123">To retrieve the current class identifier, call [**get\_ClassId**](iscardcmd-get-classid.md).</span></span>

<span data-ttu-id="0cfb3-124">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="0cfb3-124">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="0cfb3-125">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="0cfb3-125">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="0cfb3-126">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="0cfb3-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0cfb3-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="0cfb3-127">Examples</span></span>

<span data-ttu-id="0cfb3-128">L’exemple suivant montre comment définir un nouvel identificateur de classe dans l' [*unité de données du protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="0cfb3-128">The following example shows how to set a new class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="0cfb3-129">L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="0cfb3-129">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the class ID.
hr = pISCardCmd->put_ClassId(0xC0);
if (FAILED(hr))
{
  printf("Failed put_ClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="0cfb3-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0cfb3-130">Requirements</span></span>



| <span data-ttu-id="0cfb3-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0cfb3-131">Requirement</span></span> | <span data-ttu-id="0cfb3-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cfb3-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cfb3-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cfb3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0cfb3-134">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0cfb3-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0cfb3-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cfb3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0cfb3-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0cfb3-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0cfb3-137">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="0cfb3-137">End of client support</span></span><br/>    | <span data-ttu-id="0cfb3-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0cfb3-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="0cfb3-139">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="0cfb3-139">End of server support</span></span><br/>    | <span data-ttu-id="0cfb3-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0cfb3-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="0cfb3-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="0cfb3-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cfb3-142"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cfb3-142"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="0cfb3-143">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0cfb3-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="0cfb3-144"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0cfb3-144"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0cfb3-145">DLL</span><span class="sxs-lookup"><span data-stu-id="0cfb3-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cfb3-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cfb3-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0cfb3-147">IID</span><span class="sxs-lookup"><span data-stu-id="0cfb3-147">IID</span></span><br/>                      | <span data-ttu-id="0cfb3-148">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="0cfb3-148">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="0cfb3-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0cfb3-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cfb3-150">**Obtient \_ ClassID**</span><span class="sxs-lookup"><span data-stu-id="0cfb3-150">**get\_ClassId**</span></span>](iscardcmd-get-classid.md)
</dt> <dt>

[<span data-ttu-id="0cfb3-151">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="0cfb3-151">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
