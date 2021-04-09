---
description: Libère l’accès exclusif à la carte à puce.
ms.assetid: 12256c91-faf2-4a06-9501-f00d0115a069
title: 'ISCard :: UnlockSCard, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.UnlockSCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 68907e157e60518d1df3855fbca69709f2c21437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754188"
---
# <a name="iscardunlockscard-method"></a><span data-ttu-id="8e50c-103">ISCard :: UnlockSCard, méthode</span><span class="sxs-lookup"><span data-stu-id="8e50c-103">ISCard::UnlockSCard method</span></span>

<span data-ttu-id="8e50c-104">\[La méthode **UnlockScard** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="8e50c-104">\[The **UnlockScard** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8e50c-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8e50c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8e50c-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="8e50c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="8e50c-107">La méthode **UnlockScard** libère un accès exclusif à la [*carte à puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8e50c-107">The **UnlockScard** method releases exclusive access to the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8e50c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e50c-108">Syntax</span></span>


```C++
HRESULT UnlockSCard(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a><span data-ttu-id="8e50c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e50c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e50c-110">*Disposition* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8e50c-110">*Disposition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e50c-111">Indique ce qui doit être fait avec la carte dans le [*lecteur*](../secgloss/r-gly.md)connecté.</span><span class="sxs-lookup"><span data-stu-id="8e50c-111">Indicates what should be done with the card in the connected [*reader*](../secgloss/r-gly.md).</span></span>



| <span data-ttu-id="8e50c-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e50c-112">Value</span></span>                                                                                                                                      | <span data-ttu-id="8e50c-113">Signification</span><span class="sxs-lookup"><span data-stu-id="8e50c-113">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <span data-ttu-id="8e50c-114"><dt>**CONGÉ**</dt></span><span class="sxs-lookup"><span data-stu-id="8e50c-114"><dt>**LEAVE**</dt></span></span> </dl>       | <span data-ttu-id="8e50c-115">Laisse la carte à puce dans l' [*État*](../secgloss/s-gly.md)actuel.</span><span class="sxs-lookup"><span data-stu-id="8e50c-115">Leaves the smart card in the current [*state*](../secgloss/s-gly.md).</span></span><br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <span data-ttu-id="8e50c-116"><dt>**INITIALISATION**</dt></span><span class="sxs-lookup"><span data-stu-id="8e50c-116"><dt>**RESET**</dt></span></span> </dl>       | <span data-ttu-id="8e50c-117">Réinitialise la carte à puce à un état connu.</span><span class="sxs-lookup"><span data-stu-id="8e50c-117">Resets the smart card to some known state.</span></span><br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <span data-ttu-id="8e50c-118"><dt>**Hors tension**</dt></span><span class="sxs-lookup"><span data-stu-id="8e50c-118"><dt>**UNPOWER**</dt></span></span> </dl> | <span data-ttu-id="8e50c-119">Supprime l’alimentation de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="8e50c-119">Removes power from the smart card.</span></span><br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <span data-ttu-id="8e50c-120"><dt>**ÉMISSION**</dt></span><span class="sxs-lookup"><span data-stu-id="8e50c-120"><dt>**EJECT**</dt></span></span> </dl>       | <span data-ttu-id="8e50c-121">Éjecte la carte à puce si le lecteur possède des fonctionnalités d’éjection.</span><span class="sxs-lookup"><span data-stu-id="8e50c-121">Ejects the smart card if the reader has eject capabilities.</span></span><br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e50c-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8e50c-122">Return value</span></span>

<span data-ttu-id="8e50c-123">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="8e50c-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="8e50c-124">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8e50c-124">Return code</span></span>                                                                                  | <span data-ttu-id="8e50c-125">Description</span><span class="sxs-lookup"><span data-stu-id="8e50c-125">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="8e50c-126"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8e50c-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="8e50c-127">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="8e50c-127">Operation completed successfully.</span></span><br/>        |
| <dl> <span data-ttu-id="8e50c-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8e50c-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="8e50c-129">Le paramètre *disposition* n’est pas valide</span><span class="sxs-lookup"><span data-stu-id="8e50c-129">The *Disposition* parameter is not valid</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8e50c-130">Notes</span><span class="sxs-lookup"><span data-stu-id="8e50c-130">Remarks</span></span>

<span data-ttu-id="8e50c-131">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="8e50c-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="8e50c-132">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="8e50c-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8e50c-133">Exemples</span><span class="sxs-lookup"><span data-stu-id="8e50c-133">Examples</span></span>

<span data-ttu-id="8e50c-134">L’exemple suivant montre comment libérer un accès exclusif à la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="8e50c-134">The following example shows releasing exclusive access to the smart card.</span></span>


```C++
HRESULT    hr;

// Unlock the smart card.
hr = pISCard->UnlockSCard(LEAVE);
if (FAILED(hr))
{
   printf("Failed UnlockSCard\n");
   // Take error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="8e50c-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e50c-135">Requirements</span></span>



| <span data-ttu-id="8e50c-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e50c-136">Requirement</span></span> | <span data-ttu-id="8e50c-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e50c-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e50c-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e50c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8e50c-139">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e50c-139">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8e50c-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e50c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8e50c-141">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e50c-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8e50c-142">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8e50c-142">End of client support</span></span><br/>    | <span data-ttu-id="8e50c-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8e50c-143">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="8e50c-144">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="8e50c-144">End of server support</span></span><br/>    | <span data-ttu-id="8e50c-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8e50c-145">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="8e50c-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e50c-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e50c-147"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e50c-147"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="8e50c-148">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="8e50c-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="8e50c-149"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8e50c-149"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8e50c-150">DLL</span><span class="sxs-lookup"><span data-stu-id="8e50c-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e50c-151"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e50c-151"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8e50c-152">IID</span><span class="sxs-lookup"><span data-stu-id="8e50c-152">IID</span></span><br/>                      | <span data-ttu-id="8e50c-153">IID \_ ISCard est défini en tant que 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="8e50c-153">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="8e50c-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e50c-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e50c-155">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="8e50c-155">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="8e50c-156">**LockSCard**</span><span class="sxs-lookup"><span data-stu-id="8e50c-156">**LockSCard**</span></span>](iscard-lockscard.md)
</dt> </dl>

 

 
