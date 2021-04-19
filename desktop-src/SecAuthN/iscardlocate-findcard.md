---
description: La méthode FindCard recherche la carte à puce et ouvre une connexion valide à celle-ci.
ms.assetid: ab97eff2-0f41-4a6f-98b3-d5ad5883fa07
title: 'ISCardLocate :: FindCard, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.FindCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bf3cf05ff6e6040d5cac2bde161fa2eea07d5297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518463"
---
# <a name="iscardlocatefindcard-method"></a><span data-ttu-id="4bc41-103">ISCardLocate :: FindCard, méthode</span><span class="sxs-lookup"><span data-stu-id="4bc41-103">ISCardLocate::FindCard method</span></span>

<span data-ttu-id="4bc41-104">\[La méthode **FindCard** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="4bc41-104">\[The **FindCard** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4bc41-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4bc41-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4bc41-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="4bc41-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4bc41-107">La méthode **FindCard** recherche la [*carte à puce*](../secgloss/s-gly.md) et ouvre une connexion valide à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="4bc41-107">The **FindCard** method searches for the [*smart card*](../secgloss/s-gly.md) and opens a valid connection to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bc41-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4bc41-108">Syntax</span></span>


```C++
HRESULT FindCard(
  [in]  SCARD_SHARE_MODES ShareMode,
  [in]  SCARD_PROTOCOLS   Protocols,
  [in]  LONG              lFlags,
  [out] LPSCARDINFO       *ppCardInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4bc41-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4bc41-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bc41-110">*ShareMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4bc41-110">*ShareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bc41-111">Mode dans lequel partager ou ne pas partager la carte à puce lorsqu’une connexion est ouverte.</span><span class="sxs-lookup"><span data-stu-id="4bc41-111">Mode in which to share or not share the smart card when a connection is opened to it.</span></span>



| <span data-ttu-id="4bc41-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bc41-112">Value</span></span>                                                                                                                                            | <span data-ttu-id="4bc41-113">Signification</span><span class="sxs-lookup"><span data-stu-id="4bc41-113">Meaning</span></span>                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <span data-ttu-id="4bc41-114"><dt>**Or**</dt></span><span class="sxs-lookup"><span data-stu-id="4bc41-114"><dt>**EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="4bc41-115">Personne d’autre n’utilise cette connexion à la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="4bc41-115">No one else use this connection to the smart card.</span></span><br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <span data-ttu-id="4bc41-116"><dt>**PARTAGÉ**</dt></span><span class="sxs-lookup"><span data-stu-id="4bc41-116"><dt>**SHARED**</dt></span></span> </dl>          | <span data-ttu-id="4bc41-117">D’autres applications peuvent utiliser cette connexion.</span><span class="sxs-lookup"><span data-stu-id="4bc41-117">Other applications can use this connection.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="4bc41-118">*Protocoles* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4bc41-118">*Protocols* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bc41-119">Protocole à utiliser lors de la connexion à la carte.</span><span class="sxs-lookup"><span data-stu-id="4bc41-119">Protocol to use when connecting to the card.</span></span>

<span data-ttu-id="4bc41-120">T0</span><span class="sxs-lookup"><span data-stu-id="4bc41-120">T0</span></span>

<span data-ttu-id="4bc41-121">T1</span><span class="sxs-lookup"><span data-stu-id="4bc41-121">T1</span></span>

<span data-ttu-id="4bc41-122">RAW</span><span class="sxs-lookup"><span data-stu-id="4bc41-122">RAW</span></span>

<span data-ttu-id="4bc41-123">T0 \| T1</span><span class="sxs-lookup"><span data-stu-id="4bc41-123">T0\|T1</span></span>

</dd> <dt>

<span data-ttu-id="4bc41-124">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4bc41-124">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bc41-125">Spécifie quand l' [*interface utilisateur*](../secgloss/u-gly.md) s’affiche :</span><span class="sxs-lookup"><span data-stu-id="4bc41-125">Specifies when [*user interface*](../secgloss/u-gly.md) is displayed:</span></span>



| <span data-ttu-id="4bc41-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bc41-126">Value</span></span>                                                                                                                                                                       | <span data-ttu-id="4bc41-127">Signification</span><span class="sxs-lookup"><span data-stu-id="4bc41-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <span data-ttu-id="4bc41-128"><dt>**\_ \_ interface utilisateur minimale SC DLG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4bc41-128"><dt>**SC\_DLG\_MINIMAL\_UI**</dt></span></span> </dl> | <span data-ttu-id="4bc41-129">Affiche la boîte de dialogue uniquement si la carte recherchée par l’application appelante n’est pas localisée et peut être utilisée dans un lecteur.</span><span class="sxs-lookup"><span data-stu-id="4bc41-129">Displays the dialog box only if the card being searched for by the calling application is not located and available for use in a reader.</span></span> <span data-ttu-id="4bc41-130">Cela permet de trouver la carte connectée (via un mécanisme de boîte de dialogue interne ou à l’aide des fonctions de rappel de l’utilisateur) et retournée à l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="4bc41-130">This allows the card to be found, connected (either through an internal dialog box mechanism or by using the user callback functions), and returned to the calling application.</span></span><br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <span data-ttu-id="4bc41-131"><dt>**SC \_ DLG \_ non \_ UI**</dt></span><span class="sxs-lookup"><span data-stu-id="4bc41-131"><dt>**SC\_DLG\_NO\_UI**</dt></span></span> </dl>                | <span data-ttu-id="4bc41-132">N’affiche aucune interface utilisateur, quel que soit le résultat de la recherche.</span><span class="sxs-lookup"><span data-stu-id="4bc41-132">Causes no UI display, regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <span data-ttu-id="4bc41-133"><dt>**\_ \_ interface utilisateur force SC DLG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4bc41-133"><dt>**SC\_DLG\_FORCE\_UI**</dt></span></span> </dl>       | <span data-ttu-id="4bc41-134">Provoque l’affichage de l’interface utilisateur, quel que soit le résultat de la recherche.</span><span class="sxs-lookup"><span data-stu-id="4bc41-134">Causes UI display regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="4bc41-135">*ppCardInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4bc41-135">*ppCardInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bc41-136">Pointeur vers un pointeur vers une structure de données qui contient ou retourne des informations sur la [*carte à puce*](../secgloss/s-gly.md)ouverte, en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="4bc41-136">Pointer to a pointer to a data structure that contains or returns information about the opened [*smart card*](../secgloss/s-gly.md), if successful.</span></span> <span data-ttu-id="4bc41-137">Aura la **valeur null** si l’opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="4bc41-137">Will be **NULL** if operation has failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bc41-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4bc41-138">Return value</span></span>

<span data-ttu-id="4bc41-139">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="4bc41-139">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="4bc41-140">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4bc41-140">Return code</span></span>                                                                                   | <span data-ttu-id="4bc41-141">Description</span><span class="sxs-lookup"><span data-stu-id="4bc41-141">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="4bc41-142"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4bc41-142"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4bc41-143">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="4bc41-143">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="4bc41-144"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4bc41-144"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4bc41-145">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="4bc41-145">Invalid parameter.</span></span><br/>                        |
| <dl> <span data-ttu-id="4bc41-146"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="4bc41-146"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4bc41-147">Un pointeur incorrect a été passé dans *ppCardInfo*.</span><span class="sxs-lookup"><span data-stu-id="4bc41-147">A bad pointer was passed in *ppCardInfo*.</span></span><br/> |
| <dl> <span data-ttu-id="4bc41-148"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="4bc41-148"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4bc41-149">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="4bc41-149">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="4bc41-150">Notes</span><span class="sxs-lookup"><span data-stu-id="4bc41-150">Remarks</span></span>

<span data-ttu-id="4bc41-151">Pour définir les critères de recherche de la recherche, appelez [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) pour spécifier les noms des cartes de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="4bc41-151">To set the search criteria of the search, call [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) to specify a smart card's card names.</span></span>

<span data-ttu-id="4bc41-152">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardLocate**](iscardlocate.md).</span><span class="sxs-lookup"><span data-stu-id="4bc41-152">For a list of all the methods provided by this interface, see [**ISCardLocate**](iscardlocate.md).</span></span>

<span data-ttu-id="4bc41-153">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="4bc41-153">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="4bc41-154">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="4bc41-154">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4bc41-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4bc41-155">Requirements</span></span>



| <span data-ttu-id="4bc41-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4bc41-156">Requirement</span></span> | <span data-ttu-id="4bc41-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bc41-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bc41-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bc41-158">Minimum supported client</span></span><br/> | <span data-ttu-id="4bc41-159">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4bc41-159">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4bc41-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bc41-160">Minimum supported server</span></span><br/> | <span data-ttu-id="4bc41-161">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4bc41-161">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4bc41-162">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="4bc41-162">End of client support</span></span><br/>    | <span data-ttu-id="4bc41-163">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4bc41-163">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4bc41-164">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="4bc41-164">End of server support</span></span><br/>    | <span data-ttu-id="4bc41-165">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4bc41-165">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4bc41-166">En-tête</span><span class="sxs-lookup"><span data-stu-id="4bc41-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bc41-167"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bc41-167"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="4bc41-168">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4bc41-168">Type library</span></span><br/>             | <dl> <span data-ttu-id="4bc41-169"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4bc41-169"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4bc41-170">DLL</span><span class="sxs-lookup"><span data-stu-id="4bc41-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bc41-171"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bc41-171"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4bc41-172">IID</span><span class="sxs-lookup"><span data-stu-id="4bc41-172">IID</span></span><br/>                      | <span data-ttu-id="4bc41-173">IID \_ ISCardLocate est défini en tant que 1461AACD-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="4bc41-173">IID\_ISCardLocate is defined as 1461AACD-6810-11D0-918F-00AA00C18068</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="4bc41-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bc41-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bc41-175">**ConfigureCardNameSearch**</span><span class="sxs-lookup"><span data-stu-id="4bc41-175">**ConfigureCardNameSearch**</span></span>](iscardlocate-configurecardnamesearch.md)
</dt> <dt>

[<span data-ttu-id="4bc41-176">**ISCardLocate**</span><span class="sxs-lookup"><span data-stu-id="4bc41-176">**ISCardLocate**</span></span>](iscardlocate.md)
</dt> </dl>

 

 
