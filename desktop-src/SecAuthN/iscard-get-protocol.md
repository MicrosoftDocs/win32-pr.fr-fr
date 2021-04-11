---
description: Récupère l’identificateur du protocole en cours d’utilisation sur la carte à puce.
ms.assetid: 68c75e98-da5c-4e3e-9836-369941751fb0
title: 'ISCard :: get_Protocol, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Protocol
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fb58f890da85e3348ede6af70a006f98daac38a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320197"
---
# <a name="iscardget_protocol-method"></a><span data-ttu-id="901a7-103">ISCard :: obten, \_ méthode de protocole</span><span class="sxs-lookup"><span data-stu-id="901a7-103">ISCard::get\_Protocol method</span></span>

<span data-ttu-id="901a7-104">\[La méthode **obtenir le \_ protocole** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="901a7-104">\[The **get\_Protocol** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="901a7-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="901a7-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="901a7-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="901a7-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="901a7-107">La méthode d’extraction de **\_ protocole** récupère l’identificateur du protocole en cours d’utilisation sur la [*carte à puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="901a7-107">The **get\_Protocol** method retrieves the identifier of the protocol currently in use on the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="901a7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="901a7-108">Syntax</span></span>


```C++
HRESULT get_Protocol(
  [out] SCARD_PROTOCOLS *pProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="901a7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="901a7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="901a7-110">*pProtocol* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="901a7-110">*pProtocol* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="901a7-111">Pointeur vers l’identificateur de protocole.</span><span class="sxs-lookup"><span data-stu-id="901a7-111">Pointer to the protocol identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="901a7-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="901a7-112">Return value</span></span>

<span data-ttu-id="901a7-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="901a7-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="901a7-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="901a7-114">Return code</span></span>                                                                                  | <span data-ttu-id="901a7-115">Description</span><span class="sxs-lookup"><span data-stu-id="901a7-115">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="901a7-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="901a7-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="901a7-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="901a7-117">Operation completed successfully.</span></span><br/>        |
| <dl> <span data-ttu-id="901a7-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="901a7-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="901a7-119">Le paramètre *pProtocol* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="901a7-119">The *pProtocol* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="901a7-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="901a7-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="901a7-121">Un pointeur incorrect a été passé dans *pProtocol*.</span><span class="sxs-lookup"><span data-stu-id="901a7-121">A bad pointer was passed in *pProtocol*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="901a7-122">Notes</span><span class="sxs-lookup"><span data-stu-id="901a7-122">Remarks</span></span>

<span data-ttu-id="901a7-123">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="901a7-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="901a7-124">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="901a7-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="901a7-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="901a7-125">Examples</span></span>

<span data-ttu-id="901a7-126">L’exemple suivant montre comment récupérer l’identificateur du protocole en cours d’utilisation sur la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="901a7-126">The following example shows retrieving the identifier of the protocol currently in use on the smart card.</span></span>


```C++
SCARD_PROTOCOLS   scProtocol;
HRESULT           hr;

// Retrieve the protocol.
hr = pISCard->get_Protocol(&scProtocol);
if (FAILED(hr))
{
   printf("Failed get_Protocol\n");
   // Take other error handling action as needed.
}
// Use the retrieved protocol. (This example merely displays it.)
switch (scProtocol)
{
    case T0:
        printf("T0 protocol\n");
        break;
    case T1:
        printf("T1 protocol\n");
        break;
    default:
        printf("Other protocol\n");
        break;
}
```



## <a name="requirements"></a><span data-ttu-id="901a7-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="901a7-127">Requirements</span></span>



| <span data-ttu-id="901a7-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="901a7-128">Requirement</span></span> | <span data-ttu-id="901a7-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="901a7-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="901a7-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="901a7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="901a7-131">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="901a7-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="901a7-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="901a7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="901a7-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="901a7-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="901a7-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="901a7-134">End of client support</span></span><br/>    | <span data-ttu-id="901a7-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="901a7-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="901a7-136">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="901a7-136">End of server support</span></span><br/>    | <span data-ttu-id="901a7-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="901a7-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="901a7-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="901a7-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="901a7-139"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="901a7-139"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="901a7-140">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="901a7-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="901a7-141"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="901a7-141"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="901a7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="901a7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="901a7-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="901a7-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="901a7-144">IID</span><span class="sxs-lookup"><span data-stu-id="901a7-144">IID</span></span><br/>                      | <span data-ttu-id="901a7-145">IID \_ ISCard est défini en tant que 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="901a7-145">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="901a7-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="901a7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="901a7-147">**Obtient \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="901a7-147">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="901a7-148">**Obtient \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="901a7-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="901a7-149">**recevoir le \_ contexte**</span><span class="sxs-lookup"><span data-stu-id="901a7-149">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="901a7-150">**afficher l' \_ État**</span><span class="sxs-lookup"><span data-stu-id="901a7-150">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="901a7-151">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="901a7-151">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
