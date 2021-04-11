---
description: Récupère l’identificateur de classe à partir de l’unité de données de protocole d’application (APDU).
ms.assetid: 03ea997d-7698-43c7-aa9a-dfc1bac6fcdd
title: 'ISCardCmd :: get_ClassId, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6b78dfc9f3adf200a614b129ff1e86a16c88438f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113230"
---
# <a name="iscardcmdget_classid-method"></a><span data-ttu-id="a1c49-103">ISCardCmd :: \_ noclassid, méthode</span><span class="sxs-lookup"><span data-stu-id="a1c49-103">ISCardCmd::get\_ClassId method</span></span>

<span data-ttu-id="a1c49-104">\[La méthode **obtenir \_ ClassID** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="a1c49-104">\[The **get\_ClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a1c49-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a1c49-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a1c49-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="a1c49-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a1c49-107">La méthode **obtenir \_ ClassID** récupère l’identificateur de classe à partir de l' [*unité de données de protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="a1c49-107">The **get\_ClassId** method retrieves the class identifier from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="a1c49-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1c49-108">Syntax</span></span>


```C++
HRESULT get_ClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a><span data-ttu-id="a1c49-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1c49-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1c49-110">*pbyClass* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a1c49-110">*pbyClass* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1c49-111">Pointeur vers l’octet qui représente l’identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="a1c49-111">Pointer to the byte that represents the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1c49-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a1c49-112">Return value</span></span>

<span data-ttu-id="a1c49-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="a1c49-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a1c49-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a1c49-114">Return code</span></span>                                                                                   | <span data-ttu-id="a1c49-115">Description</span><span class="sxs-lookup"><span data-stu-id="a1c49-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="a1c49-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a1c49-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a1c49-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="a1c49-117">Operation completed successfully.</span></span><br/>       |
| <dl> <span data-ttu-id="a1c49-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a1c49-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a1c49-119">Le paramètre *pbyClass* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a1c49-119">The *pbyClass* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="a1c49-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="a1c49-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a1c49-121">Un pointeur incorrect a été passé dans *pbyClass*.</span><span class="sxs-lookup"><span data-stu-id="a1c49-121">A bad pointer was passed in *pbyClass*.</span></span><br/> |
| <dl> <span data-ttu-id="a1c49-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="a1c49-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a1c49-123">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="a1c49-123">Out of memory.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="a1c49-124">Notes</span><span class="sxs-lookup"><span data-stu-id="a1c49-124">Remarks</span></span>

<span data-ttu-id="a1c49-125">Pour définir l’identificateur de classe sur une nouvelle valeur, appelez [**put \_ ClassID**](iscardcmd-put-classid.md).</span><span class="sxs-lookup"><span data-stu-id="a1c49-125">To set the class identifier to a new value, call [**put\_ClassId**](iscardcmd-put-classid.md).</span></span>

<span data-ttu-id="a1c49-126">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="a1c49-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="a1c49-127">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="a1c49-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a1c49-128">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a1c49-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a1c49-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="a1c49-129">Examples</span></span>

<span data-ttu-id="a1c49-130">L’exemple suivant montre comment récupérer l’ID de classe.</span><span class="sxs-lookup"><span data-stu-id="a1c49-130">The following example shows how to retrieve the class ID.</span></span> <span data-ttu-id="a1c49-131">L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="a1c49-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     byClassID;
HRESULT  hr;

// Retrieve the class ID.
hr = pISCardCmd->get_ClassId(&byClassID);
if (FAILED(hr))
{
  printf("Failed get_ClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="a1c49-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1c49-132">Requirements</span></span>



| <span data-ttu-id="a1c49-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1c49-133">Requirement</span></span> | <span data-ttu-id="a1c49-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1c49-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1c49-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1c49-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a1c49-136">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1c49-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a1c49-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1c49-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a1c49-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1c49-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a1c49-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a1c49-139">End of client support</span></span><br/>    | <span data-ttu-id="a1c49-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a1c49-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a1c49-141">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="a1c49-141">End of server support</span></span><br/>    | <span data-ttu-id="a1c49-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a1c49-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a1c49-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="a1c49-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1c49-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1c49-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="a1c49-145">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a1c49-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="a1c49-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a1c49-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a1c49-147">DLL</span><span class="sxs-lookup"><span data-stu-id="a1c49-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1c49-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1c49-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a1c49-149">IID</span><span class="sxs-lookup"><span data-stu-id="a1c49-149">IID</span></span><br/>                      | <span data-ttu-id="a1c49-150">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="a1c49-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="a1c49-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1c49-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1c49-152">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="a1c49-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="a1c49-153">**put \_ ClassID**</span><span class="sxs-lookup"><span data-stu-id="a1c49-153">**put\_ClassId**</span></span>](iscardcmd-put-classid.md)
</dt> </dl>

 

 
