---
description: Les \_ constantes d’indicateur de bit LINETRANSLATERESULT décrivent différents résultats d’une traduction d’adresse.
ms.assetid: 7b834c57-d862-4fe6-828c-9e8fa20f3ec7
title: Constantes LINETRANSLATERESULT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad10c3da2b4250ded5706e4aaa10b9b61f8739b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530036"
---
# <a name="linetranslateresult_-constants"></a><span data-ttu-id="c4381-103">\_Constantes LINETRANSLATERESULT</span><span class="sxs-lookup"><span data-stu-id="c4381-103">LINETRANSLATERESULT\_ Constants</span></span>

<span data-ttu-id="c4381-104">Les constantes d’indicateur de bit **LINETRANSLATERESULT \_** décrivent différents résultats d’une traduction d’adresse.</span><span class="sxs-lookup"><span data-stu-id="c4381-104">The **LINETRANSLATERESULT\_** bit-flag constants describe various results of an address translation.</span></span>

<dl> <dt>

<span data-ttu-id="c4381-105"><span id="LINETRANSLATERESULT_CANONICAL"></span><span id="linetranslateresult_canonical"></span>**LINETRANSLATERESULT \_ canonique**</span><span class="sxs-lookup"><span data-stu-id="c4381-105"><span id="LINETRANSLATERESULT_CANONICAL"></span><span id="linetranslateresult_canonical"></span>**LINETRANSLATERESULT\_CANONICAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4381-106">Indique que la chaîne d’entrée était au format canonique valide.</span><span class="sxs-lookup"><span data-stu-id="c4381-106">Indicates that the input string was in valid canonical format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4381-107"><span id="LINETRANSLATERESULT_DIALBILLING"></span><span id="linetranslateresult_dialbilling"></span>**LINETRANSLATERESULT \_ DIALBILLING**</span><span class="sxs-lookup"><span data-stu-id="c4381-107"><span id="LINETRANSLATERESULT_DIALBILLING"></span><span id="linetranslateresult_dialbilling"></span>**LINETRANSLATERESULT\_DIALBILLING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4381-108">Indique que l’adresse retournée contient un « $ ».</span><span class="sxs-lookup"><span data-stu-id="c4381-108">Indicates that the returned address contains a "$".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4381-109"><span id="LINETRANSLATERESULT_DIALDIALTONE"></span><span id="linetranslateresult_dialdialtone"></span>**LINETRANSLATERESULT \_ DIALDIALTONE**</span><span class="sxs-lookup"><span data-stu-id="c4381-109"><span id="LINETRANSLATERESULT_DIALDIALTONE"></span><span id="linetranslateresult_dialdialtone"></span>**LINETRANSLATERESULT\_DIALDIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4381-110">Indique que l’adresse retournée contient un « W ».</span><span class="sxs-lookup"><span data-stu-id="c4381-110">Indicates that the returned address contains a "W".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4381-111"><span id="LINETRANSLATERESULT_DIALPROMPT"></span><span id="linetranslateresult_dialprompt"></span>**LINETRANSLATERESULT \_ DIALPROMPT**</span><span class="sxs-lookup"><span data-stu-id="c4381-111"><span id="LINETRANSLATERESULT_DIALPROMPT"></span><span id="linetranslateresult_dialprompt"></span>**LINETRANSLATERESULT\_DIALPROMPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4381-112">Indique que l’adresse retournée contient un «  ? ».</span><span class="sxs-lookup"><span data-stu-id="c4381-112">Indicates that the returned address contains a "?".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4381-113"><span id="LINETRANSLATERESULT_DIALQUIET"></span><span id="linetranslateresult_dialquiet"></span>**LINETRANSLATERESULT \_ DIALQUIET**</span><span class="sxs-lookup"><span data-stu-id="c4381-113"><span id="LINETRANSLATERESULT_DIALQUIET"></span><span id="linetranslateresult_dialquiet"></span>**LINETRANSLATERESULT\_DIALQUIET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4381-114">Indique que l’adresse retournée contient un « @ ».</span><span class="sxs-lookup"><span data-stu-id="c4381-114">Indicates that the returned address contain a "@".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4381-115"><span id="LINETRANSLATERESULT_INTERNATIONAL"></span><span id="linetranslateresult_international"></span>**LINETRANSLATERESULT \_ international**</span><span class="sxs-lookup"><span data-stu-id="c4381-115"><span id="LINETRANSLATERESULT_INTERNATIONAL"></span><span id="linetranslateresult_international"></span>**LINETRANSLATERESULT\_INTERNATIONAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4381-116">Indique que l’appel est traité comme un appel international (le code du pays ou de la région spécifié dans l’adresse de destination est différent du code du pays ou de la région spécifié pour le **CurrentLocation**).</span><span class="sxs-lookup"><span data-stu-id="c4381-116">Indicates that the call is being treated as an international call (country or region code specified in the destination address is different from the country or region code specified for the **CurrentLocation**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4381-117"><span id="LINETRANSLATERESULT_INTOLLLIST"></span><span id="linetranslateresult_intolllist"></span>**LINETRANSLATERESULT \_ INTOLLLIST**</span><span class="sxs-lookup"><span data-stu-id="c4381-117"><span id="LINETRANSLATERESULT_INTOLLLIST"></span><span id="linetranslateresult_intolllist"></span>**LINETRANSLATERESULT\_INTOLLLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4381-118">Indique que l’appel local est composé en tant que longue distance, car le pays ou la région a un appel payant et le préfixe apparaît dans le **TollPrefixList** du **CurrentLocation**.</span><span class="sxs-lookup"><span data-stu-id="c4381-118">Indicates that the local call is being dialed as long distance because the country or region has toll calling and the prefix appears in the **TollPrefixList** of the **CurrentLocation**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4381-119"><span id="LINETRANSLATERESULT_LOCAL"></span><span id="linetranslateresult_local"></span>**LINETRANSLATERESULT \_ local**</span><span class="sxs-lookup"><span data-stu-id="c4381-119"><span id="LINETRANSLATERESULT_LOCAL"></span><span id="linetranslateresult_local"></span>**LINETRANSLATERESULT\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4381-120">Indique que l’appel est traité comme un appel local (le code du pays ou de la région et le code de zone spécifiés dans l’adresse de destination sont les mêmes que ceux spécifiés pour le **CurrentLocation**).</span><span class="sxs-lookup"><span data-stu-id="c4381-120">Indicates that the call is being treated as a local call (country or region code and area code specified in the destination address are the same as those specified for the **CurrentLocation**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4381-121"><span id="LINETRANSLATERESULT_LONGDISTANCE"></span><span id="linetranslateresult_longdistance"></span>**LINETRANSLATERESULT \_ LONGDISTANCE**</span><span class="sxs-lookup"><span data-stu-id="c4381-121"><span id="LINETRANSLATERESULT_LONGDISTANCE"></span><span id="linetranslateresult_longdistance"></span>**LINETRANSLATERESULT\_LONGDISTANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4381-122">Indique que l’appel est traité comme un appel longue distance (le code du pays ou de la région spécifié dans l’adresse de destination est le même, mais le code de la zone est différent de ceux spécifiés pour le **CurrentLocation**).</span><span class="sxs-lookup"><span data-stu-id="c4381-122">Indicates that the call is being treated as a long distance call (country or region code specified in the destination address is the same but area code is different from those specified for the **CurrentLocation**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4381-123"><span id="LINETRANSLATERESULT_NOTINTOLLLIST"></span><span id="linetranslateresult_notintolllist"></span>**LINETRANSLATERESULT \_ NOTINTOLLLIST**</span><span class="sxs-lookup"><span data-stu-id="c4381-123"><span id="LINETRANSLATERESULT_NOTINTOLLLIST"></span><span id="linetranslateresult_notintolllist"></span>**LINETRANSLATERESULT\_NOTINTOLLLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4381-124">Indique que le pays ou la région prend en charge l’appel payant, mais que le préfixe n’apparaît pas dans le **TollPrefixList**, l’appel est donc composé en tant qu’appel local.</span><span class="sxs-lookup"><span data-stu-id="c4381-124">Indicates that the country or region supports toll calling but the prefix does not appear in the **TollPrefixList**, so the call is dialed as a local call.</span></span> <span data-ttu-id="c4381-125">Notez que si les deux inpéages et NOTINTOLLIST sont désactivés, le pays ou la région actuel ne prend pas en charge les préfixes de péage et les éléments d’interface utilisateur liés aux préfixes de péage ne doivent pas être présentés à l’utilisateur. Si un tel bit est activé, le pays ou la région ne prend pas en charge les listes de péages, et les éléments d’interface utilisateur associés doivent être activés.</span><span class="sxs-lookup"><span data-stu-id="c4381-125">Note that if both INTOLLIST and NOTINTOLLIST are off, the current country or region does not support toll prefixes, and user-interface elements related to toll prefixes should not be presented to the user; if either such bit is on, the country or region does support toll lists, and the related user-interface elements should be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4381-126"><span id="LINETRANSLATERESULT_NOTRANSLATION"></span><span id="linetranslateresult_notranslation"></span>**LINETRANSLATERESULT \_ NOtranslation**</span><span class="sxs-lookup"><span data-stu-id="c4381-126"><span id="LINETRANSLATERESULT_NOTRANSLATION"></span><span id="linetranslateresult_notranslation"></span>**LINETRANSLATERESULT\_NOTRANSLATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4381-127">Indique que la traduction d’adresses n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c4381-127">Indicates that address translation is not available.</span></span> <span data-ttu-id="c4381-128">Cet élément est exposé uniquement aux applications qui négocient une version TAPI 3,0 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="c4381-128">This element is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4381-129"><span id="LINETRANSLATERESULT_VOICEDETECT"></span><span id="linetranslateresult_voicedetect"></span>**LINETRANSLATERESULT \_ VOICEDETECT**</span><span class="sxs-lookup"><span data-stu-id="c4381-129"><span id="LINETRANSLATERESULT_VOICEDETECT"></span><span id="linetranslateresult_voicedetect"></span>**LINETRANSLATERESULT\_VOICEDETECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4381-130">Indique que l’adresse de numérotation retournée contient un «  : ».</span><span class="sxs-lookup"><span data-stu-id="c4381-130">Indicates that the returned dialable address contains a ":".</span></span> <span data-ttu-id="c4381-131">Cet élément est exposé uniquement aux applications qui négocient une version TAPI 2,0 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="c4381-131">This element is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>

> [!Note]  
> <span data-ttu-id="c4381-132">Le caractère «  : » (deux-points) est ajouté à la liste des caractères qui peuvent être incorporés dans une chaîne de numérotation et passés dans les adresses de destination.</span><span class="sxs-lookup"><span data-stu-id="c4381-132">The ":" (colon) character will be added to the list of characters that can be embedded in a dialable string and passed into destination addresses.</span></span> <span data-ttu-id="c4381-133">Si vous tentez de la passer d’une application à un périphérique de ligne qui prend en charge une version d’API antérieure à 2,0, vous obtiendrez très probablement LINEERR \_ INVALADDRESS ou éventuellement dans le caractère ignoré.</span><span class="sxs-lookup"><span data-stu-id="c4381-133">Attempting to pass it from an application to a line device that supports an API version earlier than 2.0 will most likely result in LINEERR\_INVALADDRESS, or possibly in the character being ignored entirely.</span></span> <span data-ttu-id="c4381-134">La signification de ce caractère est « suspendre jusqu’à ce qu’une invite vocale soit détectée, puis continuer la numérotation »; Il est destiné à être utilisé lors de la numérotation automatique des systèmes qui fournissent des invites vocales, telles que les processeurs de cartes d’appel longues distances.</span><span class="sxs-lookup"><span data-stu-id="c4381-134">The meaning of this character is "Pause until a voice prompt is detected, then continue dialing"; it is intended for use when automatically dialing into systems that give voice prompts, such as long distance calling card processors.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4381-135">Notes</span><span class="sxs-lookup"><span data-stu-id="c4381-135">Remarks</span></span>

<span data-ttu-id="c4381-136">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="c4381-136">No extensibility.</span></span> <span data-ttu-id="c4381-137">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="c4381-137">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4381-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4381-138">Requirements</span></span>



| <span data-ttu-id="c4381-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4381-139">Requirement</span></span> | <span data-ttu-id="c4381-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4381-140">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c4381-141">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="c4381-141">TAPI version</span></span><br/> | <span data-ttu-id="c4381-142">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c4381-142">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c4381-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4381-143">Header</span></span><br/>       | <dl> <span data-ttu-id="c4381-144"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4381-144"><dt>Tapi.h</dt></span></span> </dl> |



 

 




