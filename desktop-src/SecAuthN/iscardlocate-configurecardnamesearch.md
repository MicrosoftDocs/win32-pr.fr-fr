---
description: La méthode ConfigureCardNameSearch spécifie les noms de carte à utiliser dans la recherche de la carte à puce.
ms.assetid: fb406696-0cf0-4d67-8125-8888ee1b8213
title: 'ISCardLocate :: ConfigureCardNameSearch, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.ConfigureCardNameSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4af451bea1f08df2af0a673b26e84c9df2a0954b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203372"
---
# <a name="iscardlocateconfigurecardnamesearch-method"></a><span data-ttu-id="cd681-103">ISCardLocate :: ConfigureCardNameSearch, méthode</span><span class="sxs-lookup"><span data-stu-id="cd681-103">ISCardLocate::ConfigureCardNameSearch method</span></span>

<span data-ttu-id="cd681-104">\[La méthode **ConfigureCardNameSearch** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="cd681-104">\[The **ConfigureCardNameSearch** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cd681-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="cd681-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cd681-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="cd681-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="cd681-107">La méthode **ConfigureCardNameSearch** spécifie les noms de carte à utiliser dans la recherche de la [*carte à puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="cd681-107">The **ConfigureCardNameSearch** method specifies the card names to be used in the search for the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cd681-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd681-108">Syntax</span></span>


```C++
HRESULT ConfigureCardNameSearch(
  [in] LPSAFEARRAY pCardNames,
  [in] LPSAFEARRAY pGroupNames,
  [in] BSTR        bstrTitle,
  [in] LONG        lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="cd681-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd681-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd681-110">*pCardNames* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd681-110">*pCardNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd681-111">Pointeur vers un tableau sécurisé Automation de noms de carte sous forme BSTR.</span><span class="sxs-lookup"><span data-stu-id="cd681-111">A pointer to an Automation safe array of card names in BSTR form.</span></span>

</dd> <dt>

<span data-ttu-id="cd681-112">*pGroupNames* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd681-112">*pGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd681-113">Pointeur vers un tableau sécurisé Automation des noms des groupes de cartes/lecteurs dans le formulaire BSTR à ajouter à la recherche.</span><span class="sxs-lookup"><span data-stu-id="cd681-113">A pointer to an Automation safe array of names of card/reader groups in BSTR form to add to the search.</span></span>

</dd> <dt>

<span data-ttu-id="cd681-114">*bstrTitle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd681-114">*bstrTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd681-115">Titre de la boîte de dialogue pour le contrôle commun de recherche.</span><span class="sxs-lookup"><span data-stu-id="cd681-115">Dialog box title for the search common control.</span></span>

</dd> <dt>

<span data-ttu-id="cd681-116">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd681-116">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd681-117">Spécifie quand l' [*interface utilisateur*](../secgloss/u-gly.md) est affichée.</span><span class="sxs-lookup"><span data-stu-id="cd681-117">Specifies when [*user interface*](../secgloss/u-gly.md) is displayed.</span></span>



| <span data-ttu-id="cd681-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd681-118">Value</span></span>                                                                                                                                                                       | <span data-ttu-id="cd681-119">Signification</span><span class="sxs-lookup"><span data-stu-id="cd681-119">Meaning</span></span>                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <span data-ttu-id="cd681-120"><dt>**\_ \_ interface utilisateur minimale SC DLG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cd681-120"><dt>**SC\_DLG\_MINIMAL\_UI**</dt></span></span> </dl> | <span data-ttu-id="cd681-121">Affiche la boîte de dialogue uniquement si la carte recherchée par l’application appelante n’est pas localisée et peut être utilisée dans un lecteur.</span><span class="sxs-lookup"><span data-stu-id="cd681-121">Displays the dialog box only if the card being searched for by the calling application is not located and available for use in a reader.</span></span> <span data-ttu-id="cd681-122">Cela permet de trouver la carte connectée (via un mécanisme de boîte de dialogue interne ou à l’aide des fonctions de rappel de l’utilisateur) et retournée à l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="cd681-122">This allows the card to be found, connected (either through an internal dialog box mechanism or by using the user callback functions), and returned to the calling application.</span></span><br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <span data-ttu-id="cd681-123"><dt>**SC \_ DLG \_ non \_ UI**</dt></span><span class="sxs-lookup"><span data-stu-id="cd681-123"><dt>**SC\_DLG\_NO\_UI**</dt></span></span> </dl>                | <span data-ttu-id="cd681-124">N’affiche aucune interface utilisateur, quel que soit le résultat de la recherche.</span><span class="sxs-lookup"><span data-stu-id="cd681-124">Causes no UI display, regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <span data-ttu-id="cd681-125"><dt>**\_ \_ interface utilisateur force SC DLG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cd681-125"><dt>**SC\_DLG\_FORCE\_UI**</dt></span></span> </dl>       | <span data-ttu-id="cd681-126">Provoque l’affichage de l’interface utilisateur, quel que soit le résultat de la recherche.</span><span class="sxs-lookup"><span data-stu-id="cd681-126">Causes UI display regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd681-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cd681-127">Return value</span></span>

<span data-ttu-id="cd681-128">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="cd681-128">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="cd681-129">Code de retour</span><span class="sxs-lookup"><span data-stu-id="cd681-129">Return code</span></span>                                                                                   | <span data-ttu-id="cd681-130">Description</span><span class="sxs-lookup"><span data-stu-id="cd681-130">Description</span></span>                                                           |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="cd681-131"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cd681-131"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cd681-132">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="cd681-132">Operation completed successfully.</span></span><br/>                          |
| <dl> <span data-ttu-id="cd681-133"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cd681-133"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="cd681-134">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="cd681-134">Invalid parameter.</span></span><br/>                                         |
| <dl> <span data-ttu-id="cd681-135"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="cd681-135"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="cd681-136">Un pointeur incorrect a été passé dans *pCardNames* ou *pGroupNames*.</span><span class="sxs-lookup"><span data-stu-id="cd681-136">A bad pointer was passed in *pCardNames* or *pGroupNames*.</span></span><br/> |
| <dl> <span data-ttu-id="cd681-137"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="cd681-137"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cd681-138">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="cd681-138">Out of memory.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="cd681-139">Notes</span><span class="sxs-lookup"><span data-stu-id="cd681-139">Remarks</span></span>

<span data-ttu-id="cd681-140">Pour localiser la [*carte à puce*](../secgloss/s-gly.md), appelez [**FindCard**](iscardlocate-findcard.md).</span><span class="sxs-lookup"><span data-stu-id="cd681-140">To locate the [*smart card*](../secgloss/s-gly.md), call [**FindCard**](iscardlocate-findcard.md).</span></span>

<span data-ttu-id="cd681-141">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardLocate**](iscardlocate.md).</span><span class="sxs-lookup"><span data-stu-id="cd681-141">For a list of all the methods provided by this interface, see [**ISCardLocate**](iscardlocate.md).</span></span>

<span data-ttu-id="cd681-142">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="cd681-142">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="cd681-143">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="cd681-143">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd681-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd681-144">Requirements</span></span>



| <span data-ttu-id="cd681-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd681-145">Requirement</span></span> | <span data-ttu-id="cd681-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd681-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd681-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd681-147">Minimum supported client</span></span><br/> | <span data-ttu-id="cd681-148">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd681-148">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cd681-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd681-149">Minimum supported server</span></span><br/> | <span data-ttu-id="cd681-150">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd681-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cd681-151">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="cd681-151">End of client support</span></span><br/>    | <span data-ttu-id="cd681-152">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cd681-152">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="cd681-153">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="cd681-153">End of server support</span></span><br/>    | <span data-ttu-id="cd681-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cd681-154">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="cd681-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="cd681-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd681-156"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd681-156"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="cd681-157">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="cd681-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="cd681-158"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cd681-158"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cd681-159">DLL</span><span class="sxs-lookup"><span data-stu-id="cd681-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd681-160"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd681-160"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cd681-161">IID</span><span class="sxs-lookup"><span data-stu-id="cd681-161">IID</span></span><br/>                      | <span data-ttu-id="cd681-162">IID \_ ISCardLocate est défini en tant que 1461AACD-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="cd681-162">IID\_ISCardLocate is defined as 1461AACD-6810-11D0-918F-00AA00C18068</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="cd681-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd681-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd681-164">**FindCard**</span><span class="sxs-lookup"><span data-stu-id="cd681-164">**FindCard**</span></span>](iscardlocate-findcard.md)
</dt> <dt>

[<span data-ttu-id="cd681-165">**ISCardLocate**</span><span class="sxs-lookup"><span data-stu-id="cd681-165">**ISCardLocate**</span></span>](iscardlocate.md)
</dt> </dl>

 

 
