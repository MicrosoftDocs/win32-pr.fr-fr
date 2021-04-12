---
description: La méthode SelectFile construit une commande APDU (Application Protocol Data Unit) qui définit un fichier élémentaire actuel au sein d’un canal logique. Les commandes suivantes peuvent faire référence implicitement au fichier actif par le biais du canal logique.
ms.assetid: cb6231b3-fb1c-4350-8797-9efaa663c21b
title: 'ISCardISO7816 :: SelectFile, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SelectFile
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9bab499d32a65a2e6b4348458ec42328029760ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203049"
---
# <a name="iscardiso7816selectfile-method"></a><span data-ttu-id="dea26-104">ISCardISO7816 :: SelectFile, méthode</span><span class="sxs-lookup"><span data-stu-id="dea26-104">ISCardISO7816::SelectFile method</span></span>

<span data-ttu-id="dea26-105">\[La méthode **SelectFile** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="dea26-105">\[The **SelectFile** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dea26-106">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="dea26-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dea26-107">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="dea26-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="dea26-108">La méthode **SelectFile** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui définit un fichier élémentaire actuel au sein d’un canal logique.</span><span class="sxs-lookup"><span data-stu-id="dea26-108">The **SelectFile** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that sets a current elementary file within a logical channel.</span></span> <span data-ttu-id="dea26-109">Les commandes suivantes peuvent faire référence implicitement au fichier actif par le biais du canal logique.</span><span class="sxs-lookup"><span data-stu-id="dea26-109">Subsequent commands may implicitly refer to the current file through the logical channel.</span></span>

<span data-ttu-id="dea26-110">La sélection d’un répertoire (DF) dans le magasin de contenu de la carte, qui peut être la racine (MF) du cache de l’utilisateur, en fait le DF actuel.</span><span class="sxs-lookup"><span data-stu-id="dea26-110">Selecting a directory (DF) within the card filestore — which may be the root (MF) of the filestore — makes it the current DF.</span></span> <span data-ttu-id="dea26-111">Après une telle sélection, un fichier élémentaire en cours implicite peut être référencé par ce canal logique.</span><span class="sxs-lookup"><span data-stu-id="dea26-111">After such a selection, an implicit current elementary file may be referred to through that logical channel.</span></span>

<span data-ttu-id="dea26-112">La sélection d’un fichier élémentaire définit le fichier sélectionné et son parent en tant que fichiers actifs.</span><span class="sxs-lookup"><span data-stu-id="dea26-112">Selecting an elementary file sets the selected file and its parent as current files.</span></span>

<span data-ttu-id="dea26-113">Après la réponse à la réinitialisation, le MF est implicitement sélectionné par le biais du canal logique de base, sauf s’il est spécifié différemment dans les octets historiques ou dans la chaîne de données initiale.</span><span class="sxs-lookup"><span data-stu-id="dea26-113">After the answer to reset, the MF is implicitly selected through the basic logical channel, unless specified differently in the historical bytes or in the initial data string.</span></span>

## <a name="syntax"></a><span data-ttu-id="dea26-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea26-114">Syntax</span></span>


```C++
HRESULT SelectFile(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in]      LONG         lBytesToRead,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="dea26-115">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dea26-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dea26-116">*byP1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dea26-116">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dea26-117">Contrôle de sélection.</span><span class="sxs-lookup"><span data-stu-id="dea26-117">Selection control.</span></span>



| <span data-ttu-id="dea26-118">P1 (octet supérieur dans Word) : 8 7 6 5 4 3 2 1</span><span class="sxs-lookup"><span data-stu-id="dea26-118">P1 (upper byte in word): 8 7 6 5 4 3 2 1</span></span>                                                                                                                                                            | <span data-ttu-id="dea26-119">Signification</span><span class="sxs-lookup"><span data-stu-id="dea26-119">Meaning</span></span>                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span id="000000xx"></span><span id="000000XX"></span><dl> <span data-ttu-id="dea26-120"><dt>**000000xx**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="dea26-120"><dt>**000000xx**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="dea26-121">Sélectionner l’ID de fichier</span><span class="sxs-lookup"><span data-stu-id="dea26-121">Select File ID</span></span><br/>          |
| <span id="00000000"></span><dl> <span data-ttu-id="dea26-122"><dt>**00000000**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="dea26-122"><dt>**00000000**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="dea26-123">EF, DF ou MF</span><span class="sxs-lookup"><span data-stu-id="dea26-123">EF, DF, or MF</span></span><br/>           |
| <span id="00000001"></span><dl> <span data-ttu-id="dea26-124"><dt>**00000001**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="dea26-124"><dt>**00000001**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="dea26-125">DF enfant</span><span class="sxs-lookup"><span data-stu-id="dea26-125">Child DF</span></span><br/>                |
| <span id="00000010"></span><dl> <span data-ttu-id="dea26-126"><dt>**00000010**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="dea26-126"><dt>**00000010**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="dea26-127">EF sous DF</span><span class="sxs-lookup"><span data-stu-id="dea26-127">EF under DF</span></span><br/>             |
| <span id="00000011"></span><dl> <span data-ttu-id="dea26-128"><dt>**00000011**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="dea26-128"><dt>**00000011**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="dea26-129">DF parent du DF actuel</span><span class="sxs-lookup"><span data-stu-id="dea26-129">Parent DF of current DF</span></span><br/> |



 

<span data-ttu-id="dea26-130">Lorsque P1 = 00, la carte connaît soit en raison d’un codage spécifique de l’ID de fichier, soit en raison du contexte d’exécution de la commande si le fichier à sélectionner est MF, DF ou EF.</span><span class="sxs-lookup"><span data-stu-id="dea26-130">When P1=00, the card knows either because of a specific coding of the file ID or because of the context of execution of the command if the file to select is the MF, a DF, or an EF.</span></span>

<span data-ttu-id="dea26-131">Lorsque P1-P2 = 0000, si un ID de fichier est fourni, il doit être unique dans les environnements suivants :</span><span class="sxs-lookup"><span data-stu-id="dea26-131">When P1-P2=0000, if a file ID is provided, then it shall be unique in the following environments:</span></span>

-   <span data-ttu-id="dea26-132">Enfants immédiats du DF actuel</span><span class="sxs-lookup"><span data-stu-id="dea26-132">Immediate children of the current DF</span></span>
-   <span data-ttu-id="dea26-133">DF parent</span><span class="sxs-lookup"><span data-stu-id="dea26-133">Parent DF</span></span>
-   <span data-ttu-id="dea26-134">Enfants immédiats du DF parent</span><span class="sxs-lookup"><span data-stu-id="dea26-134">Immediate children of the parent DF</span></span>

<span data-ttu-id="dea26-135">Si P1-P2 = 0000 et que le champ de données est vide ou égal à 3F00, sélectionnez le MF.</span><span class="sxs-lookup"><span data-stu-id="dea26-135">If P1-P2=0000 and if the data field is empty or equal to 3F00, then select the MF.</span></span>

<span data-ttu-id="dea26-136">Lorsque P1 = 04, le champ de données est un nom DF, éventuellement tronqué à droite.</span><span class="sxs-lookup"><span data-stu-id="dea26-136">When P1=04, the data field is a DF name, possibly right truncated.</span></span>

<span data-ttu-id="dea26-137">En cas de prise en charge, ces commandes successives avec le même champ de données doivent sélectionner DFs dont les noms correspondent à ceux du champ de données (autrement dit, commencez par le champ de données de la commande).</span><span class="sxs-lookup"><span data-stu-id="dea26-137">When supported, successive such commands with the same data field shall select DFs whose names match with the data field (that is, start with the command data field).</span></span> <span data-ttu-id="dea26-138">Si la carte accepte la commande avec un champ de données vide, l’ensemble ou un sous-ensemble du DFs peut être sélectionné successivement.</span><span class="sxs-lookup"><span data-stu-id="dea26-138">If the card accepts the command with an empty data field, then all or a subset of the DFs can be successively selected.</span></span>

</dd> <dt>

<span data-ttu-id="dea26-139">*byP2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dea26-139">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dea26-140">Contrôle de sélection.</span><span class="sxs-lookup"><span data-stu-id="dea26-140">Selection control.</span></span>

</dd> <dt>

<span data-ttu-id="dea26-141">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dea26-141">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dea26-142">Données pour l’opération si nécessaire ; Sinon, **null**.</span><span class="sxs-lookup"><span data-stu-id="dea26-142">Data for operation if needed; else, **NULL**.</span></span> <span data-ttu-id="dea26-143">Les types de données passés dans ce paramètre sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="dea26-143">Types of data that are passed in this parameter include:</span></span>

-   <span data-ttu-id="dea26-144">ID de fichier</span><span class="sxs-lookup"><span data-stu-id="dea26-144">file ID</span></span>
-   <span data-ttu-id="dea26-145">chemin d’accès à partir du MF</span><span class="sxs-lookup"><span data-stu-id="dea26-145">path from the MF</span></span>
-   <span data-ttu-id="dea26-146">chemin du DF actuel</span><span class="sxs-lookup"><span data-stu-id="dea26-146">path from the current DF</span></span>
-   <span data-ttu-id="dea26-147">Nom du DF</span><span class="sxs-lookup"><span data-stu-id="dea26-147">DF name</span></span>

</dd> <dt>

<span data-ttu-id="dea26-148">*lBytesToRead* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dea26-148">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dea26-149">Vide (autrement dit, 0) ou longueur maximale des données attendues dans la réponse.</span><span class="sxs-lookup"><span data-stu-id="dea26-149">Empty (that is, 0) or maximum length of data expected in response.</span></span>

</dd> <dt>

<span data-ttu-id="dea26-150">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="dea26-150">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dea26-151">En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.</span><span class="sxs-lookup"><span data-stu-id="dea26-151">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="dea26-152">Au retour, elle est remplie avec la commande APDU construite par cette opération.</span><span class="sxs-lookup"><span data-stu-id="dea26-152">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="dea26-153">Si *ppCmd* a été défini avec la **valeur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé et retourné en interne par le biais du pointeur *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="dea26-153">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dea26-154">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dea26-154">Return value</span></span>

<span data-ttu-id="dea26-155">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="dea26-155">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="dea26-156">Code de retour</span><span class="sxs-lookup"><span data-stu-id="dea26-156">Return code</span></span>                                                                                   | <span data-ttu-id="dea26-157">Description</span><span class="sxs-lookup"><span data-stu-id="dea26-157">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="dea26-158"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dea26-158"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="dea26-159">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="dea26-159">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="dea26-160"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="dea26-160"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="dea26-161">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="dea26-161">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="dea26-162"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="dea26-162"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="dea26-163">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="dea26-163">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="dea26-164"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="dea26-164"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="dea26-165">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="dea26-165">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="dea26-166">Notes</span><span class="sxs-lookup"><span data-stu-id="dea26-166">Remarks</span></span>

<span data-ttu-id="dea26-167">Sauf indication contraire, l’exécution correcte de la commande encapsulée modifie l’état de sécurité conformément aux règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="dea26-167">Unless otherwise specified, the correct execution of the encapsulated command modifies the security status according to the following rules:</span></span>

-   <span data-ttu-id="dea26-168">Lorsque le fichier élémentaire actuel est modifié ou qu’il n’existe aucun fichier élémentaire en cours, l’état de sécurité spécifique à un ancien fichier élémentaire actuel est perdu.</span><span class="sxs-lookup"><span data-stu-id="dea26-168">When the current elementary file is changed, or when there is no current elementary file, the security status specific to a former current elementary file is lost.</span></span>
-   <span data-ttu-id="dea26-169">Lorsque le répertoire de cache actuel (DF) est un descendant de ou identique à l’ancien DF actuel, l’état de sécurité spécifique à l’ancien DF actuel est perdu.</span><span class="sxs-lookup"><span data-stu-id="dea26-169">When the current filestore directory (DF) is descendant of, or identical to the former current DF, the security status specific to the former current DF is lost.</span></span> <span data-ttu-id="dea26-170">L’état de sécurité commun à tous les ancêtres communs du DF précédent et du nouveau DF actuel est conservé.</span><span class="sxs-lookup"><span data-stu-id="dea26-170">The security status common to all common ancestors of the previous and new current DF is maintained.</span></span>

<span data-ttu-id="dea26-171">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="dea26-171">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="dea26-172">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="dea26-172">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="dea26-173">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="dea26-173">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dea26-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dea26-174">Requirements</span></span>



| <span data-ttu-id="dea26-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dea26-175">Requirement</span></span> | <span data-ttu-id="dea26-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="dea26-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dea26-177">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dea26-177">Minimum supported client</span></span><br/> | <span data-ttu-id="dea26-178">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dea26-178">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dea26-179">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dea26-179">Minimum supported server</span></span><br/> | <span data-ttu-id="dea26-180">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dea26-180">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dea26-181">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="dea26-181">End of client support</span></span><br/>    | <span data-ttu-id="dea26-182">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dea26-182">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="dea26-183">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="dea26-183">End of server support</span></span><br/>    | <span data-ttu-id="dea26-184">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dea26-184">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="dea26-185">En-tête</span><span class="sxs-lookup"><span data-stu-id="dea26-185">Header</span></span><br/>                   | <dl> <span data-ttu-id="dea26-186"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dea26-186"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dea26-187">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="dea26-187">Type library</span></span><br/>             | <dl> <span data-ttu-id="dea26-188"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dea26-188"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dea26-189">DLL</span><span class="sxs-lookup"><span data-stu-id="dea26-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dea26-190"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dea26-190"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dea26-191">IID</span><span class="sxs-lookup"><span data-stu-id="dea26-191">IID</span></span><br/>                      | <span data-ttu-id="dea26-192">IID \_ ISCardISO7816 est défini en tant que 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="dea26-192">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="dea26-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dea26-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dea26-194">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="dea26-194">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
