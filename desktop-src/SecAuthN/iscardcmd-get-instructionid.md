---
description: Récupère l’octet d’identificateur d’instruction à partir de l’unité de données de protocole d’application (APDU).
ms.assetid: 294f51cd-0a13-4dfb-bf02-9edd11a7085e
title: 'ISCardCmd :: get_InstructionId, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_InstructionId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4b0125237ef94a5d6173f517483b9ae8781d5607
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953069"
---
# <a name="iscardcmdget_instructionid-method"></a><span data-ttu-id="f496a-103">ISCardCmd :: \_ InstructionId, méthode</span><span class="sxs-lookup"><span data-stu-id="f496a-103">ISCardCmd::get\_InstructionId method</span></span>

<span data-ttu-id="f496a-104">\[La méthode **obtenir \_ InstructionId** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="f496a-104">\[The **get\_InstructionId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f496a-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f496a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f496a-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="f496a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f496a-107">La méthode **obtenir \_ InstructionId** récupère l’octet d’identificateur d’instruction à partir de l' [*unité de données de protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="f496a-107">The **get\_InstructionId** method retrieves the instruction identifier byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="f496a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f496a-108">Syntax</span></span>


```C++
HRESULT get_InstructionId(
  [out] BYTE *pbyIns
);
```



## <a name="parameters"></a><span data-ttu-id="f496a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f496a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f496a-110">*pbyIns* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f496a-110">*pbyIns* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f496a-111">Pointeur vers l’octet qui est l’ID d’instruction de l’APDU au retour.</span><span class="sxs-lookup"><span data-stu-id="f496a-111">Pointer to the byte that is the instruction ID from the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f496a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f496a-112">Return value</span></span>

<span data-ttu-id="f496a-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="f496a-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="f496a-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f496a-114">Return code</span></span>                                                                                   | <span data-ttu-id="f496a-115">Description</span><span class="sxs-lookup"><span data-stu-id="f496a-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="f496a-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f496a-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f496a-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="f496a-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="f496a-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f496a-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f496a-119">Le paramètre *pbyIns* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f496a-119">The *pbyIns* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="f496a-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="f496a-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f496a-121">Un pointeur incorrect a été passé dans *pbyIns*.</span><span class="sxs-lookup"><span data-stu-id="f496a-121">A bad pointer was passed in *pbyIns*.</span></span><br/> |
| <dl> <span data-ttu-id="f496a-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="f496a-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f496a-123">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="f496a-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="f496a-124">Notes</span><span class="sxs-lookup"><span data-stu-id="f496a-124">Remarks</span></span>

<span data-ttu-id="f496a-125">Pour définir l’identificateur d’instruction sur une nouvelle valeur, appelez [**put \_ InstructionId**](iscardcmd-put-instructionid.md).</span><span class="sxs-lookup"><span data-stu-id="f496a-125">To set the instructional identifier to a new value, call [**put\_InstructionId**](iscardcmd-put-instructionid.md).</span></span>

<span data-ttu-id="f496a-126">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="f496a-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="f496a-127">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="f496a-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="f496a-128">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="f496a-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f496a-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="f496a-129">Examples</span></span>

<span data-ttu-id="f496a-130">L’exemple suivant montre comment récupérer l’octet d’identificateur d’instruction à partir de l' [*unité de données de protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="f496a-130">The following example shows how to retrieve the instruction identifier byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="f496a-131">L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="f496a-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byInstructID;
HRESULT hr;

// Retrieve the instruction ID.
hr = pISCardCmd->get_InstructionId(&byInstructID);
if (FAILED(hr))
{
  printf("Failed get_InstructionId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="f496a-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f496a-132">Requirements</span></span>



| <span data-ttu-id="f496a-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f496a-133">Requirement</span></span> | <span data-ttu-id="f496a-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="f496a-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f496a-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f496a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f496a-136">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f496a-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f496a-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f496a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f496a-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f496a-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f496a-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f496a-139">End of client support</span></span><br/>    | <span data-ttu-id="f496a-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f496a-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f496a-141">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="f496a-141">End of server support</span></span><br/>    | <span data-ttu-id="f496a-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f496a-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f496a-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="f496a-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="f496a-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="f496a-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="f496a-145">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f496a-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="f496a-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f496a-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f496a-147">DLL</span><span class="sxs-lookup"><span data-stu-id="f496a-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f496a-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f496a-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f496a-149">IID</span><span class="sxs-lookup"><span data-stu-id="f496a-149">IID</span></span><br/>                      | <span data-ttu-id="f496a-150">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="f496a-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="f496a-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f496a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f496a-152">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="f496a-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="f496a-153">**put \_ InstructionId**</span><span class="sxs-lookup"><span data-stu-id="f496a-153">**put\_InstructionId**</span></span>](iscardcmd-put-instructionid.md)
</dt> </dl>

 

 
