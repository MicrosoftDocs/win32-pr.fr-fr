---
description: La méthode LockSCard réclame un accès exclusif à la carte à puce.
ms.assetid: 70af7c5a-ebe7-48ee-8a76-dfea7f73f45e
title: 'ISCard :: LockSCard, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.LockSCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d5b834afec339aa4c3a4eee42f9817409fabb917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210011"
---
# <a name="iscardlockscard-method"></a><span data-ttu-id="0c9d7-103">ISCard :: LockSCard, méthode</span><span class="sxs-lookup"><span data-stu-id="0c9d7-103">ISCard::LockSCard method</span></span>

<span data-ttu-id="0c9d7-104">\[La méthode **LockSCard** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="0c9d7-104">\[The **LockSCard** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0c9d7-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0c9d7-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0c9d7-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="0c9d7-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="0c9d7-107">La méthode **LockSCard** réclame un accès exclusif à la [*carte à puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0c9d7-107">The **LockSCard** method claims exclusive access to the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0c9d7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c9d7-108">Syntax</span></span>


```C++
HRESULT LockSCard();
```



## <a name="parameters"></a><span data-ttu-id="0c9d7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c9d7-109">Parameters</span></span>

<span data-ttu-id="0c9d7-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0c9d7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0c9d7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0c9d7-111">Return value</span></span>

<span data-ttu-id="0c9d7-112">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="0c9d7-112">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="0c9d7-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0c9d7-113">Return code</span></span>                                                                          | <span data-ttu-id="0c9d7-114">Description</span><span class="sxs-lookup"><span data-stu-id="0c9d7-114">Description</span></span>                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0c9d7-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0c9d7-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0c9d7-116">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="0c9d7-116">Operation completed successfully.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0c9d7-117">Notes</span><span class="sxs-lookup"><span data-stu-id="0c9d7-117">Remarks</span></span>

<span data-ttu-id="0c9d7-118">Outre le code d’erreur COM indiqué ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="0c9d7-118">In addition to the COM error code listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="0c9d7-119">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="0c9d7-119">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

<span data-ttu-id="0c9d7-120">Pour déverrouiller la carte à puce, appelez la méthode [**ISCard :: UnlockSCard**](iscard-unlockscard.md) .</span><span class="sxs-lookup"><span data-stu-id="0c9d7-120">To unlock the smart card, call the [**ISCard::UnlockSCard**](iscard-unlockscard.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="0c9d7-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="0c9d7-121">Examples</span></span>

<span data-ttu-id="0c9d7-122">L’exemple suivant montre l’acquisition d’un accès exclusif à la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="0c9d7-122">The following example shows acquiring exclusive access to the smart card.</span></span>


```C++
HRESULT    hr;

// Lock the smart card.
hr = pISCard->LockSCard();
if (FAILED(hr))
{
    printf("Failed LockSCard\n");
    // Take error handling action as needed.
}
// Use smart card; unlock the smart card when done.
```



## <a name="requirements"></a><span data-ttu-id="0c9d7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c9d7-123">Requirements</span></span>



| <span data-ttu-id="0c9d7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c9d7-124">Requirement</span></span> | <span data-ttu-id="0c9d7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c9d7-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c9d7-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c9d7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0c9d7-127">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c9d7-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0c9d7-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c9d7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0c9d7-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c9d7-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0c9d7-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="0c9d7-130">End of client support</span></span><br/>    | <span data-ttu-id="0c9d7-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c9d7-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="0c9d7-132">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="0c9d7-132">End of server support</span></span><br/>    | <span data-ttu-id="0c9d7-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0c9d7-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="0c9d7-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c9d7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c9d7-135"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c9d7-135"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="0c9d7-136">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0c9d7-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="0c9d7-137"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0c9d7-137"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0c9d7-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0c9d7-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c9d7-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c9d7-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0c9d7-140">IID</span><span class="sxs-lookup"><span data-stu-id="0c9d7-140">IID</span></span><br/>                      | <span data-ttu-id="0c9d7-141">IID \_ ISCard est défini en tant que 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="0c9d7-141">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="0c9d7-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c9d7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c9d7-143">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="0c9d7-143">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="0c9d7-144">**UnlockSCard**</span><span class="sxs-lookup"><span data-stu-id="0c9d7-144">**UnlockSCard**</span></span>](iscard-unlockscard.md)
</dt> </dl>

 

 
