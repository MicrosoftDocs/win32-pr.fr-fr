---
description: Récupère l’état actuel de la carte à puce.
ms.assetid: 0e6e4a8f-ecad-4a82-8804-aaf58f13f7ca
title: 'ISCard :: get_Status, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Status
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f0daa47653779b3aa4b5e7cb65c0c56410b19ab9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210760"
---
# <a name="iscardget_status-method"></a><span data-ttu-id="88f73-103">ISCard :: obtient l' \_ État, méthode</span><span class="sxs-lookup"><span data-stu-id="88f73-103">ISCard::get\_Status method</span></span>

<span data-ttu-id="88f73-104">\[La méthode **obtenir l' \_ État** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="88f73-104">\[The **get\_Status** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="88f73-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="88f73-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="88f73-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="88f73-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="88f73-107">La méthode **obtenir l' \_ État** récupère l' [*État*](../secgloss/s-gly.md) actuel de la [*carte à puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="88f73-107">The **get\_Status** method retrieves the current [*state*](../secgloss/s-gly.md) of the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="88f73-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88f73-108">Syntax</span></span>


```C++
HRESULT get_Status(
  [out] SCARD_STATES *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="88f73-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88f73-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88f73-110">*pStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="88f73-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88f73-111">Pointeur vers la variable d’État.</span><span class="sxs-lookup"><span data-stu-id="88f73-111">Pointer to the state variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88f73-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="88f73-112">Return value</span></span>

<span data-ttu-id="88f73-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="88f73-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="88f73-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="88f73-114">Return code</span></span>                                                                                  | <span data-ttu-id="88f73-115">Description</span><span class="sxs-lookup"><span data-stu-id="88f73-115">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="88f73-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="88f73-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="88f73-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="88f73-117">Operation completed successfully.</span></span><br/>      |
| <dl> <span data-ttu-id="88f73-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="88f73-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="88f73-119">Le paramètre *pStatus* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="88f73-119">The *pStatus* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="88f73-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="88f73-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="88f73-121">Un pointeur incorrect a été passé dans *pStatus*.</span><span class="sxs-lookup"><span data-stu-id="88f73-121">A bad pointer was passed in *pStatus*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="88f73-122">Notes</span><span class="sxs-lookup"><span data-stu-id="88f73-122">Remarks</span></span>

<span data-ttu-id="88f73-123">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="88f73-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="88f73-124">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="88f73-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="88f73-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="88f73-125">Examples</span></span>

<span data-ttu-id="88f73-126">L’exemple suivant montre l’extraction de l’état actuel de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="88f73-126">The following example shows retrieving the current state of the smart card.</span></span>


```C++
SCARD_STATES    scState;
HRESULT         hr;

// Determine the current state of the smart card.
hr = pISCard->get_Status(&scState);
if (FAILED(hr))
{
   printf("Failed get_Status\n");
   exit(1);  // Or other error handling action.
}
// Use the retrieved value. (This example merely displays it.)
switch (scState)
{
    case ABSENT:
        printf("Absent state\n");
        break;
    case PRESENT:
        printf("Present state\n");
        break;
    case SWALLOWED:
        printf("Swallowed state\n");
        break;
    case POWERED:
        printf("Powered state\n");
        break;
    case NEGOTIABLEMODE:
        printf("Negotiable mode state\n");
        break;
    case SPECIFICMODE:
        printf("Specific mode state\n");
        break;
    default:
        printf("Unexpected state\n");
        break;
}
```



## <a name="requirements"></a><span data-ttu-id="88f73-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88f73-127">Requirements</span></span>



| <span data-ttu-id="88f73-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88f73-128">Requirement</span></span> | <span data-ttu-id="88f73-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="88f73-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88f73-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88f73-130">Minimum supported client</span></span><br/> | <span data-ttu-id="88f73-131">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88f73-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="88f73-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88f73-132">Minimum supported server</span></span><br/> | <span data-ttu-id="88f73-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88f73-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="88f73-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="88f73-134">End of client support</span></span><br/>    | <span data-ttu-id="88f73-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="88f73-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="88f73-136">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="88f73-136">End of server support</span></span><br/>    | <span data-ttu-id="88f73-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="88f73-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="88f73-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="88f73-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="88f73-139"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="88f73-139"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="88f73-140">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="88f73-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="88f73-141"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="88f73-141"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="88f73-142">DLL</span><span class="sxs-lookup"><span data-stu-id="88f73-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88f73-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88f73-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="88f73-144">IID</span><span class="sxs-lookup"><span data-stu-id="88f73-144">IID</span></span><br/>                      | <span data-ttu-id="88f73-145">IID \_ ISCard est défini en tant que 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="88f73-145">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="88f73-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88f73-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88f73-147">**Obtient \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="88f73-147">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="88f73-148">**Obtient \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="88f73-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="88f73-149">**recevoir le \_ contexte**</span><span class="sxs-lookup"><span data-stu-id="88f73-149">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="88f73-150">**Obtient le \_ protocole**</span><span class="sxs-lookup"><span data-stu-id="88f73-150">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="88f73-151">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="88f73-151">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
