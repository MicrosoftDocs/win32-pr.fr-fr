---
description: Construit une commande APDU (Application Protocol Data Unit) qui initie la comparaison (dans la carte) des données de vérification envoyées à partir de l’appareil d’interface avec les données de référence stockées dans la carte (par exemple, le mot de passe).
ms.assetid: a0837c39-d741-42eb-88b2-87c4e043e64f
title: 'ISCardISO7816 :: Verify, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.Verify
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: c44bf65bfcebe6e76ce1ee955205b9c9163efcee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533945"
---
# <a name="iscardiso7816verify-method"></a><span data-ttu-id="cb2ae-103">ISCardISO7816 :: Verify, méthode</span><span class="sxs-lookup"><span data-stu-id="cb2ae-103">ISCardISO7816::Verify method</span></span>

<span data-ttu-id="cb2ae-104">\[La méthode **verify** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cb2ae-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cb2ae-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="cb2ae-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="cb2ae-107">La méthode **verify** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui initie la comparaison (dans la carte) des données de vérification envoyées à partir de l’appareil d’interface avec les données de référence stockées dans la carte (par exemple, le mot de passe).</span><span class="sxs-lookup"><span data-stu-id="cb2ae-107">The **Verify** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that initiates the comparison (in the card) of the verification data sent from the interface device with the reference data stored in the card (for example, password).</span></span>

## <a name="syntax"></a><span data-ttu-id="cb2ae-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb2ae-108">Syntax</span></span>


```C++
HRESULT Verify(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="cb2ae-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb2ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb2ae-110">*byRefCtrl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cb2ae-110">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb2ae-111">Quantificateur des données de référence.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-111">A quantifier of the reference data.</span></span> <span data-ttu-id="cb2ae-112">Le codage du contrôle de référence P2 suit.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-112">Coding of the reference control P2 follows.</span></span>

<span data-ttu-id="cb2ae-113">Lorsque le corps est vide, la commande peut être utilisée pour récupérer le nombre « X » de nouvelles tentatives autorisées (SW1-SW2 = 63CX) ou pour vérifier si la vérification n’est pas requise (SW1-SW2 = 9000).</span><span class="sxs-lookup"><span data-stu-id="cb2ae-113">When the body is empty, the command may be used either to retrieve the number 'X' of further allowed retries (SW1-SW2=63CX) or to check whether the verification is not required (SW1-SW2=9000).</span></span>



| <span data-ttu-id="cb2ae-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb2ae-114">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="cb2ae-115">Signification</span><span class="sxs-lookup"><span data-stu-id="cb2ae-115">Meaning</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <span data-ttu-id="cb2ae-116"><dt>**Aucune information**</dt></span><span class="sxs-lookup"><span data-stu-id="cb2ae-116"><dt>**No Info**</dt></span></span> </dl>                     | <span data-ttu-id="cb2ae-117">Position du bit : 00000000</span><span class="sxs-lookup"><span data-stu-id="cb2ae-117">Bit position: 00000000</span></span><br/> <span data-ttu-id="cb2ae-118">P2 = 00 est réservé pour indiquer qu’aucun qualificateur particulier n’est utilisé dans ces cartes où la commande Verify référence les données secrètes sans ambiguïté.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-118">P2=00 is reserved to indicate that no particular qualifier is used in those cards where the verify command references the secret data unambiguously.</span></span><br/> |
| <span id="Global_Ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <span data-ttu-id="cb2ae-119"><dt>**Référence globale**</dt></span><span class="sxs-lookup"><span data-stu-id="cb2ae-119"><dt>**Global Ref**</dt></span></span> </dl>         | <span data-ttu-id="cb2ae-120">Position du bit : 0-------</span><span class="sxs-lookup"><span data-stu-id="cb2ae-120">Bit position: 0-------</span></span><br/> <span data-ttu-id="cb2ae-121">Un mot de passe est un exemple de référence globale.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-121">An example of Global Ref would be a password.</span></span><br/>                                                                                                        |
| <span id="Specific_Ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <span data-ttu-id="cb2ae-122"><dt>**Réf. spécifique**</dt></span><span class="sxs-lookup"><span data-stu-id="cb2ae-122"><dt>**Specific Ref**</dt></span></span> </dl> | <span data-ttu-id="cb2ae-123">Position du bit : 1-------</span><span class="sxs-lookup"><span data-stu-id="cb2ae-123">Bit position: 1-------</span></span><br/> <span data-ttu-id="cb2ae-124">Un mot de passe spécifique à DF est un exemple de référence spécifique.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-124">An example of Specific Ref is DF specific password.</span></span><br/>                                                                                                  |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="cb2ae-125"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="cb2ae-125"><dt>**RFU**</dt></span></span> </dl>                                                           | <span data-ttu-id="cb2ae-126">Position du bit :-XX-----</span><span class="sxs-lookup"><span data-stu-id="cb2ae-126">Bit position: -xx-----</span></span><br/>                                                                                                                                                                 |
| <span id="Ref_Data__"></span><span id="ref_data__"></span><span id="REF_DATA__"></span><dl> <span data-ttu-id="cb2ae-127"><dt>**Données de référence \#**</dt></span><span class="sxs-lookup"><span data-stu-id="cb2ae-127"><dt>**Ref Data \#**</dt></span></span> </dl>        | <span data-ttu-id="cb2ae-128">Position du bit :---xxxxx</span><span class="sxs-lookup"><span data-stu-id="cb2ae-128">Bit position: ---xxxxx</span></span><br/> <span data-ttu-id="cb2ae-129">Le numéro de données de référence peut être, par exemple, un numéro de mot de passe ou un identificateur EF bref.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-129">The reference data number may be, for example, a password number or a short EF identifier.</span></span><br/>                                                           |



 

</dd> <dt>

<span data-ttu-id="cb2ae-130">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cb2ae-130">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb2ae-131">Pointeur vers les données de vérification.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-131">A pointer to the verification data.</span></span> <span data-ttu-id="cb2ae-132">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-132">This parameter can be **NULL**.</span></span> <span data-ttu-id="cb2ae-133">La valeur par défaut est **NULL**.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-133">The default value is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cb2ae-134">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cb2ae-134">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb2ae-135">En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-135">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="cb2ae-136">Au retour, elle est remplie avec la commande APDU construite par cette opération.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-136">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="cb2ae-137">Si *ppCmd* a été défini **sur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé et retourné en interne à l’aide du pointeur *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="cb2ae-137">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb2ae-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cb2ae-138">Return value</span></span>

<span data-ttu-id="cb2ae-139">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-139">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="cb2ae-140">Code de retour</span><span class="sxs-lookup"><span data-stu-id="cb2ae-140">Return code</span></span>                                                                                   | <span data-ttu-id="cb2ae-141">Description</span><span class="sxs-lookup"><span data-stu-id="cb2ae-141">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="cb2ae-142"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cb2ae-142"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cb2ae-143">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-143">The operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="cb2ae-144"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cb2ae-144"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="cb2ae-145">Un paramètre non valide a été utilisé.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-145">A parameter that is not valid was used.</span></span><br/> |
| <dl> <span data-ttu-id="cb2ae-146"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="cb2ae-146"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="cb2ae-147">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-147">A bad pointer was passed in.</span></span><br/>            |
| <dl> <span data-ttu-id="cb2ae-148"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="cb2ae-148"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cb2ae-149">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-149">Out of memory.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="cb2ae-150">Notes</span><span class="sxs-lookup"><span data-stu-id="cb2ae-150">Remarks</span></span>

<span data-ttu-id="cb2ae-151">L’état de sécurité peut être modifié à la suite d’une comparaison.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-151">The security status may be modified as a result of a comparison.</span></span> <span data-ttu-id="cb2ae-152">Les comparaisons ayant échoué peuvent être enregistrées dans la carte (par exemple, pour limiter le nombre de tentatives supplémentaires d’utilisation des données de référence).</span><span class="sxs-lookup"><span data-stu-id="cb2ae-152">Unsuccessful comparisons may be recorded in the card (for example, to limit the number of further attempts of the use of the reference data).</span></span>

<span data-ttu-id="cb2ae-153">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="cb2ae-153">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="cb2ae-154">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="cb2ae-154">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="cb2ae-155">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="cb2ae-155">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb2ae-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb2ae-156">Requirements</span></span>



| <span data-ttu-id="cb2ae-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb2ae-157">Requirement</span></span> | <span data-ttu-id="cb2ae-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb2ae-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb2ae-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb2ae-159">Minimum supported client</span></span><br/> | <span data-ttu-id="cb2ae-160">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb2ae-160">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cb2ae-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb2ae-161">Minimum supported server</span></span><br/> | <span data-ttu-id="cb2ae-162">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb2ae-162">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cb2ae-163">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="cb2ae-163">End of client support</span></span><br/>    | <span data-ttu-id="cb2ae-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cb2ae-164">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="cb2ae-165">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="cb2ae-165">End of server support</span></span><br/>    | <span data-ttu-id="cb2ae-166">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cb2ae-166">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="cb2ae-167">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb2ae-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb2ae-168"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb2ae-168"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cb2ae-169">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="cb2ae-169">Type library</span></span><br/>             | <dl> <span data-ttu-id="cb2ae-170"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cb2ae-170"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cb2ae-171">DLL</span><span class="sxs-lookup"><span data-stu-id="cb2ae-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb2ae-172"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb2ae-172"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cb2ae-173">IID</span><span class="sxs-lookup"><span data-stu-id="cb2ae-173">IID</span></span><br/>                      | <span data-ttu-id="cb2ae-174">IID \_ ISCardISO7816 est défini en tant que 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="cb2ae-174">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="cb2ae-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb2ae-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb2ae-176">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="cb2ae-176">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
