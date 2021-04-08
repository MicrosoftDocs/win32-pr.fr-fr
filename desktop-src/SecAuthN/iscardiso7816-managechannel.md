---
description: La méthode ManageChannel construit une commande APDU (Application Protocol Data Unit) qui ouvre et ferme des canaux logiques.
ms.assetid: a55b5b3f-0404-45bd-afeb-e96173319a50
title: 'ISCardISO7816 :: ManageChannel, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ManageChannel
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f0b9af92e280781405c2cb570c93e8873a279765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034318"
---
# <a name="iscardiso7816managechannel-method"></a><span data-ttu-id="26c00-103">ISCardISO7816 :: ManageChannel, méthode</span><span class="sxs-lookup"><span data-stu-id="26c00-103">ISCardISO7816::ManageChannel method</span></span>

<span data-ttu-id="26c00-104">\[La méthode **ManageChannel** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="26c00-104">\[The **ManageChannel** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="26c00-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="26c00-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="26c00-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="26c00-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="26c00-107">La méthode **ManageChannel** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui ouvre et ferme des canaux logiques.</span><span class="sxs-lookup"><span data-stu-id="26c00-107">The **ManageChannel** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that opens and closes logical channels.</span></span>

<span data-ttu-id="26c00-108">La fonction Open ouvre un nouveau canal logique autre que celui de base.</span><span class="sxs-lookup"><span data-stu-id="26c00-108">The open function opens a new logical channel other than the basic one.</span></span> <span data-ttu-id="26c00-109">Des options sont fournies pour que la carte affecte un numéro de canal logique, ou pour que le numéro de canal logique soit fourni à la carte.</span><span class="sxs-lookup"><span data-stu-id="26c00-109">Options are provided for the card to assign a logical channel number, or for the logical channel number to be supplied to the card.</span></span>

<span data-ttu-id="26c00-110">La fonction Close ferme explicitement un canal logique autre que le canal de base.</span><span class="sxs-lookup"><span data-stu-id="26c00-110">The close function explicitly closes a logical channel other than the basic one.</span></span> <span data-ttu-id="26c00-111">Une fois la fermeture terminée, le canal logique sera disponible pour une réutilisation.</span><span class="sxs-lookup"><span data-stu-id="26c00-111">After the successful closing, the logical channel shall be available for re-use.</span></span>

## <a name="syntax"></a><span data-ttu-id="26c00-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26c00-112">Syntax</span></span>


```C++
HRESULT ManageChannel(
  [in]      BYTE       byChannelState,
  [in]      BYTE       byChannel,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="26c00-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26c00-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26c00-114">*byChannelState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26c00-114">*byChannelState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26c00-115">Le bit B8 de P1 est utilisé pour indiquer la fonction Open ou la fonction Close ; Si B8 est égal à 0, MANAGE CHANNEL ouvrira un canal logique et, si B8 a la valeur 1, le canal MANAGE doit fermer un canal logique :</span><span class="sxs-lookup"><span data-stu-id="26c00-115">Bit b8 of P1 is used to indicate the open function or the close function; if b8 is 0, then MANAGE CHANNEL shall open a logical channel and if b8 is 1, then MANAGE CHANNEL shall close a logical channel:</span></span>

<span data-ttu-id="26c00-116">P1 = « 00 » pour l’ouvrir</span><span class="sxs-lookup"><span data-stu-id="26c00-116">P1 = '00' to open</span></span>

<span data-ttu-id="26c00-117">P1 = ' 80 'pour fermer</span><span class="sxs-lookup"><span data-stu-id="26c00-117">P1 = '80' to close</span></span>

<span data-ttu-id="26c00-118">Les autres valeurs sont RFU</span><span class="sxs-lookup"><span data-stu-id="26c00-118">Other values are RFU</span></span>

</dd> <dt>

<span data-ttu-id="26c00-119">*byChannel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26c00-119">*byChannel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26c00-120">Pour la fonction Open (P1 = « 00 »), les bits B1 et B2 de P2 sont utilisés pour coder le numéro de canal logique de la même manière que dans l’octet de classe, les autres bits de P2 sont RFU.</span><span class="sxs-lookup"><span data-stu-id="26c00-120">For the open function (P1 = '00'), the bits b1 and b2 of P2 are used to code the logical channel number in the same manner as in the class byte, the other bits of P2 are RFU.</span></span>

<span data-ttu-id="26c00-121">Lorsque B1 et B2 de P2 ont la **valeur null**, la carte affecte un numéro de canal logique qui est retourné dans les bits B1 et B2 du champ de données.</span><span class="sxs-lookup"><span data-stu-id="26c00-121">When b1 and b2 of P2 are **NULL**, then the card will assign a logical channel number that will be returned in bits b1 and b2 of the data field.</span></span>

<span data-ttu-id="26c00-122">Lorsque B1 et/ou B2 de P2 ne sont pas **null**, ils codent un numéro de canal logique autre que celui de base ; Ensuite, la carte ouvre le numéro de canal logique attribué en externe.</span><span class="sxs-lookup"><span data-stu-id="26c00-122">When b1 and/or b2 of P2 are not **NULL**, they code a logical channel number other than the basic one; then the card will open the externally assigned logical channel number.</span></span>

</dd> <dt>

<span data-ttu-id="26c00-123">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="26c00-123">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="26c00-124">En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.</span><span class="sxs-lookup"><span data-stu-id="26c00-124">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="26c00-125">Au retour, elle est remplie avec la commande APDU construite par cette opération.</span><span class="sxs-lookup"><span data-stu-id="26c00-125">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="26c00-126">Si *ppCmd* a été défini **sur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé en interne et retourné à l’aide du pointeur *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="26c00-126">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26c00-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26c00-127">Return value</span></span>

<span data-ttu-id="26c00-128">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="26c00-128">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="26c00-129">Code de retour</span><span class="sxs-lookup"><span data-stu-id="26c00-129">Return code</span></span>                                                                                   | <span data-ttu-id="26c00-130">Description</span><span class="sxs-lookup"><span data-stu-id="26c00-130">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="26c00-131"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="26c00-131"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="26c00-132">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="26c00-132">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="26c00-133"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="26c00-133"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="26c00-134">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="26c00-134">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="26c00-135"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="26c00-135"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="26c00-136">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="26c00-136">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="26c00-137"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="26c00-137"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="26c00-138">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="26c00-138">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="26c00-139">Notes</span><span class="sxs-lookup"><span data-stu-id="26c00-139">Remarks</span></span>

<span data-ttu-id="26c00-140">Lorsque la fonction Open est correctement exécutée à partir du canal logique de base, le MF est implicitement sélectionné comme DF actuel et l’état de sécurité du nouveau canal logique doit être identique au canal logique de base après ATR.</span><span class="sxs-lookup"><span data-stu-id="26c00-140">When the open function is successfully performed from the basic logical channel, the MF shall be implicitly selected as the current DF and the security status of the new logical channel should be the same as the basic logical channel after ATR.</span></span> <span data-ttu-id="26c00-141">L’état de sécurité du nouveau canal logique doit être distinct de celui de tout autre canal logique.</span><span class="sxs-lookup"><span data-stu-id="26c00-141">The security status of the new logical channel should be separate from that of any other logical channel.</span></span>

<span data-ttu-id="26c00-142">Lorsque la fonction Open est exécutée avec succès à partir d’un canal logique, qui n’est pas le canal de base, le DF actuel du canal logique qui a émis la commande est sélectionné en tant que DF actuel.</span><span class="sxs-lookup"><span data-stu-id="26c00-142">When the open function is successfully performed from a logical channel, which is not the basic one, the current DF of the logical channel that issued the command will be selected as the current DF.</span></span> <span data-ttu-id="26c00-143">En outre, l’état de sécurité du nouveau canal logique doit être identique à l’état de sécurité du canal logique à partir duquel la fonction d’ouverture a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="26c00-143">In addition, the security status for the new logical channel should be the same as the security status of the logical channel from which the open function was performed.</span></span>

<span data-ttu-id="26c00-144">Après une fonction de fermeture réussie, l’état de sécurité associé à ce canal logique est perdu.</span><span class="sxs-lookup"><span data-stu-id="26c00-144">After a successful close function, the security status related to this logical channel is lost.</span></span>

<span data-ttu-id="26c00-145">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="26c00-145">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="26c00-146">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="26c00-146">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="26c00-147">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="26c00-147">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="26c00-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26c00-148">Requirements</span></span>



| <span data-ttu-id="26c00-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26c00-149">Requirement</span></span> | <span data-ttu-id="26c00-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="26c00-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26c00-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26c00-151">Minimum supported client</span></span><br/> | <span data-ttu-id="26c00-152">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26c00-152">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="26c00-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26c00-153">Minimum supported server</span></span><br/> | <span data-ttu-id="26c00-154">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26c00-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="26c00-155">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="26c00-155">End of client support</span></span><br/>    | <span data-ttu-id="26c00-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="26c00-156">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="26c00-157">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="26c00-157">End of server support</span></span><br/>    | <span data-ttu-id="26c00-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="26c00-158">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="26c00-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="26c00-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="26c00-160"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="26c00-160"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="26c00-161">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="26c00-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="26c00-162"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="26c00-162"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="26c00-163">DLL</span><span class="sxs-lookup"><span data-stu-id="26c00-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26c00-164"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26c00-164"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="26c00-165">IID</span><span class="sxs-lookup"><span data-stu-id="26c00-165">IID</span></span><br/>                      | <span data-ttu-id="26c00-166">IID \_ ISCardISO7816 est défini en tant que 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="26c00-166">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="26c00-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26c00-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26c00-168">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="26c00-168">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
