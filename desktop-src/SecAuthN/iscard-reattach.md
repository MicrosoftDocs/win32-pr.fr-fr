---
description: La méthode de réassociation réinitialise, ou réinitialise, la carte à puce.
ms.assetid: c9cd9cd7-5ee6-48dc-8460-deb9c827fcc4
title: 'ISCard :: Attach, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.ReAttach
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 3f5ff4cd46b2b523b0031e1389b96d9c2c3973a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201949"
---
# <a name="iscardreattach-method"></a><span data-ttu-id="6e398-103">ISCard :: Attach, méthode</span><span class="sxs-lookup"><span data-stu-id="6e398-103">ISCard::ReAttach method</span></span>

<span data-ttu-id="6e398-104">\[La méthode de **reconnexion** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="6e398-104">\[The **ReAttach** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6e398-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6e398-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6e398-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="6e398-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6e398-107">La méthode de **réassociation** réinitialise, ou réinitialise, la [*carte à puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="6e398-107">The **ReAttach** method resets, or reinitializes, the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6e398-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e398-108">Syntax</span></span>


```C++
HRESULT ReAttach(
  [in] SCARD_SHARE_MODES  ShareMode,
  [in] SCARD_DISPOSITIONS InitState
);
```



## <a name="parameters"></a><span data-ttu-id="6e398-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e398-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e398-110">*ShareMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6e398-110">*ShareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e398-111">Mode dans lequel partager ou posséder exclusivement la connexion à la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="6e398-111">Mode in which to share or exclusively own the connection to the smart card.</span></span>



| <span data-ttu-id="6e398-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e398-112">Value</span></span>                                                                                                                                            | <span data-ttu-id="6e398-113">Signification</span><span class="sxs-lookup"><span data-stu-id="6e398-113">Meaning</span></span>                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <span data-ttu-id="6e398-114"><dt>**Or**</dt></span><span class="sxs-lookup"><span data-stu-id="6e398-114"><dt>**EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="6e398-115">Personne d’autre n’utilise cette connexion à la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="6e398-115">No one else use this connection to the smart card.</span></span><br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <span data-ttu-id="6e398-116"><dt>**PARTAGÉ**</dt></span><span class="sxs-lookup"><span data-stu-id="6e398-116"><dt>**SHARED**</dt></span></span> </dl>          | <span data-ttu-id="6e398-117">D’autres applications peuvent utiliser cette connexion.</span><span class="sxs-lookup"><span data-stu-id="6e398-117">Other applications can use this connection.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="6e398-118">*InitState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6e398-118">*InitState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e398-119">Indique ce qu’il faut faire avec la carte.</span><span class="sxs-lookup"><span data-stu-id="6e398-119">Indicates what to do with the card.</span></span>



| <span data-ttu-id="6e398-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e398-120">Value</span></span>                                                                                                                                      | <span data-ttu-id="6e398-121">Signification</span><span class="sxs-lookup"><span data-stu-id="6e398-121">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <span data-ttu-id="6e398-122"><dt>**CONGÉ**</dt></span><span class="sxs-lookup"><span data-stu-id="6e398-122"><dt>**LEAVE**</dt></span></span> </dl>       | <span data-ttu-id="6e398-123">Laisse la carte à puce dans l' [*État*](../secgloss/s-gly.md)actuel.</span><span class="sxs-lookup"><span data-stu-id="6e398-123">Leaves the smart card in the current [*state*](../secgloss/s-gly.md).</span></span><br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <span data-ttu-id="6e398-124"><dt>**INITIALISATION**</dt></span><span class="sxs-lookup"><span data-stu-id="6e398-124"><dt>**RESET**</dt></span></span> </dl>       | <span data-ttu-id="6e398-125">Réinitialise la carte à puce à un état connu.</span><span class="sxs-lookup"><span data-stu-id="6e398-125">Resets the smart card to some known state.</span></span><br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <span data-ttu-id="6e398-126"><dt>**Hors tension**</dt></span><span class="sxs-lookup"><span data-stu-id="6e398-126"><dt>**UNPOWER**</dt></span></span> </dl> | <span data-ttu-id="6e398-127">Supprime l’alimentation de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="6e398-127">Removes power from the smart card.</span></span><br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <span data-ttu-id="6e398-128"><dt>**ÉMISSION**</dt></span><span class="sxs-lookup"><span data-stu-id="6e398-128"><dt>**EJECT**</dt></span></span> </dl>       | <span data-ttu-id="6e398-129">Éjecte la carte à puce si le lecteur possède des fonctionnalités d’éjection.</span><span class="sxs-lookup"><span data-stu-id="6e398-129">Ejects the smart card if the reader has eject capabilities.</span></span><br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e398-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6e398-130">Return value</span></span>

<span data-ttu-id="6e398-131">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="6e398-131">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6e398-132">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6e398-132">Return code</span></span>                                                                                  | <span data-ttu-id="6e398-133">Description</span><span class="sxs-lookup"><span data-stu-id="6e398-133">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6e398-134"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6e398-134"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6e398-135">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="6e398-135">Operation completed successfully.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="6e398-136"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6e398-136"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="6e398-137">Il y a un problème avec un ou plusieurs des paramètres transmis à la fonction.</span><span class="sxs-lookup"><span data-stu-id="6e398-137">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6e398-138">Notes</span><span class="sxs-lookup"><span data-stu-id="6e398-138">Remarks</span></span>

<span data-ttu-id="6e398-139">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="6e398-139">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6e398-140">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6e398-140">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6e398-141">Exemples</span><span class="sxs-lookup"><span data-stu-id="6e398-141">Examples</span></span>

<span data-ttu-id="6e398-142">L’exemple suivant illustre la réinitialisation de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="6e398-142">The following example shows reinitializing the smart card.</span></span>


```C++
HRESULT    hr;

// Reattach the smart card.
hr = pISCard->ReAttach(SHARED, LEAVE);
if (FAILED(hr))
{
   printf("Failed ReAttach\n");
   // Take error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="6e398-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e398-143">Requirements</span></span>



| <span data-ttu-id="6e398-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e398-144">Requirement</span></span> | <span data-ttu-id="6e398-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e398-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e398-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e398-146">Minimum supported client</span></span><br/> | <span data-ttu-id="6e398-147">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e398-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6e398-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e398-148">Minimum supported server</span></span><br/> | <span data-ttu-id="6e398-149">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e398-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6e398-150">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="6e398-150">End of client support</span></span><br/>    | <span data-ttu-id="6e398-151">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6e398-151">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6e398-152">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="6e398-152">End of server support</span></span><br/>    | <span data-ttu-id="6e398-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6e398-153">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6e398-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e398-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e398-155"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e398-155"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="6e398-156">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6e398-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="6e398-157"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6e398-157"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6e398-158">DLL</span><span class="sxs-lookup"><span data-stu-id="6e398-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e398-159"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e398-159"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6e398-160">IID</span><span class="sxs-lookup"><span data-stu-id="6e398-160">IID</span></span><br/>                      | <span data-ttu-id="6e398-161">IID \_ ISCard est défini en tant que 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="6e398-161">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="6e398-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e398-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e398-163">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="6e398-163">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="6e398-164">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="6e398-164">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="6e398-165">**Dissocié**</span><span class="sxs-lookup"><span data-stu-id="6e398-165">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="6e398-166">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="6e398-166">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
