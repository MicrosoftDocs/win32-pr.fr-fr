---
description: Ferme la connexion ouverte à la carte à puce.
ms.assetid: 7d768945-8d5d-4d29-b5bc-1b2ac5b0e114
title: ISCard ::D méthode Etach (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Detach
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f9fd2b2a6d9ea2df8e886c6ff9851706c2030a1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545066"
---
# <a name="iscarddetach-method"></a><span data-ttu-id="7695c-103">ISCard ::D méthode Etach</span><span class="sxs-lookup"><span data-stu-id="7695c-103">ISCard::Detach method</span></span>

<span data-ttu-id="7695c-104">\[La méthode de **détachement** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="7695c-104">\[The **Detach** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7695c-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7695c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7695c-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="7695c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7695c-107">La méthode **Detach** ferme la connexion ouverte à la [*carte à puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7695c-107">The **Detach** method closes the open connection to the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7695c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7695c-108">Syntax</span></span>


```C++
HRESULT Detach(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a><span data-ttu-id="7695c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7695c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7695c-110">*Disposition* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7695c-110">*Disposition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7695c-111">Indique ce qui doit être fait avec la carte dans le [*lecteur*](../secgloss/r-gly.md)connecté.</span><span class="sxs-lookup"><span data-stu-id="7695c-111">Indicates what should be done with the card in the connected [*reader*](../secgloss/r-gly.md).</span></span>



| <span data-ttu-id="7695c-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="7695c-112">Value</span></span>                                                                                                                                      | <span data-ttu-id="7695c-113">Signification</span><span class="sxs-lookup"><span data-stu-id="7695c-113">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <span data-ttu-id="7695c-114"><dt>**CONGÉ**</dt></span><span class="sxs-lookup"><span data-stu-id="7695c-114"><dt>**LEAVE**</dt></span></span> </dl>       | <span data-ttu-id="7695c-115">Laisse la carte à puce dans l' [*État*](../secgloss/s-gly.md)actuel.</span><span class="sxs-lookup"><span data-stu-id="7695c-115">Leaves the smart card in the current [*state*](../secgloss/s-gly.md).</span></span><br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <span data-ttu-id="7695c-116"><dt>**INITIALISATION**</dt></span><span class="sxs-lookup"><span data-stu-id="7695c-116"><dt>**RESET**</dt></span></span> </dl>       | <span data-ttu-id="7695c-117">Réinitialise la carte à puce à un état connu.</span><span class="sxs-lookup"><span data-stu-id="7695c-117">Resets the smart card to some known state.</span></span><br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <span data-ttu-id="7695c-118"><dt>**Hors tension**</dt></span><span class="sxs-lookup"><span data-stu-id="7695c-118"><dt>**UNPOWER**</dt></span></span> </dl> | <span data-ttu-id="7695c-119">Supprime l’alimentation de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="7695c-119">Removes power from the smart card.</span></span><br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <span data-ttu-id="7695c-120"><dt>**ÉMISSION**</dt></span><span class="sxs-lookup"><span data-stu-id="7695c-120"><dt>**EJECT**</dt></span></span> </dl>       | <span data-ttu-id="7695c-121">Éjecte la carte à puce si le lecteur possède des fonctionnalités d’éjection.</span><span class="sxs-lookup"><span data-stu-id="7695c-121">Ejects the smart card if the reader has eject capabilities.</span></span><br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7695c-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7695c-122">Return value</span></span>

<span data-ttu-id="7695c-123">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="7695c-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7695c-124">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7695c-124">Return code</span></span>                                                                                  | <span data-ttu-id="7695c-125">Description</span><span class="sxs-lookup"><span data-stu-id="7695c-125">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="7695c-126"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7695c-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="7695c-127">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="7695c-127">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="7695c-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7695c-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="7695c-129">La *disposition* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7695c-129">*Disposition* is not valid.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="7695c-130">Notes</span><span class="sxs-lookup"><span data-stu-id="7695c-130">Remarks</span></span>

<span data-ttu-id="7695c-131">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="7695c-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7695c-132">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7695c-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7695c-133">Exemples</span><span class="sxs-lookup"><span data-stu-id="7695c-133">Examples</span></span>

<span data-ttu-id="7695c-134">L’exemple suivant illustre la fermeture de la connexion à la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="7695c-134">The following example shows closing the connection to the smart card.</span></span>


```C++
HRESULT    hr;

// Detach the smart card.
hr = pISCard->Detach(LEAVE);
if (FAILED(hr))
{
   printf("Failed Detach\n");
   // Take error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="7695c-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7695c-135">Requirements</span></span>



| <span data-ttu-id="7695c-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7695c-136">Requirement</span></span> | <span data-ttu-id="7695c-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="7695c-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7695c-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7695c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7695c-139">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7695c-139">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7695c-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7695c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7695c-141">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7695c-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7695c-142">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7695c-142">End of client support</span></span><br/>    | <span data-ttu-id="7695c-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7695c-143">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7695c-144">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="7695c-144">End of server support</span></span><br/>    | <span data-ttu-id="7695c-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7695c-145">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7695c-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="7695c-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="7695c-147"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="7695c-147"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="7695c-148">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="7695c-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="7695c-149"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7695c-149"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7695c-150">DLL</span><span class="sxs-lookup"><span data-stu-id="7695c-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7695c-151"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7695c-151"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7695c-152">IID</span><span class="sxs-lookup"><span data-stu-id="7695c-152">IID</span></span><br/>                      | <span data-ttu-id="7695c-153">IID \_ ISCard est défini en tant que 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="7695c-153">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="7695c-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7695c-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7695c-155">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="7695c-155">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="7695c-156">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="7695c-156">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="7695c-157">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="7695c-157">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="7695c-158">**Rattacher**</span><span class="sxs-lookup"><span data-stu-id="7695c-158">**ReAttach**</span></span>](iscard-reattach.md)
</dt> </dl>

 

 
