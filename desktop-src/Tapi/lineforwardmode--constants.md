---
description: Les \_ constantes d’indicateur de bit LINEFORWARDMODE décrivent les conditions dans lesquelles les appels à une adresse peuvent être transférés.
ms.assetid: 8cc053bd-1056-42be-b48a-d2312c456893
title: Constantes LINEFORWARDMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33702be12afaef5d1194ca5c0d288bd967a93e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521770"
---
# <a name="lineforwardmode_-constants"></a><span data-ttu-id="a8056-103">\_Constantes LINEFORWARDMODE</span><span class="sxs-lookup"><span data-stu-id="a8056-103">LINEFORWARDMODE\_ Constants</span></span>

<span data-ttu-id="a8056-104">Les constantes d’indicateur de bit **LINEFORWARDMODE \_** décrivent les conditions dans lesquelles les appels à une adresse peuvent être transférés.</span><span class="sxs-lookup"><span data-stu-id="a8056-104">The **LINEFORWARDMODE\_** bit-flag constants describe the conditions under which calls to an address can be forwarded.</span></span>

<dl> <dt>

<span data-ttu-id="a8056-105"><span id="LINEFORWARDMODE_BUSY"></span><span id="lineforwardmode_busy"></span>**LINEFORWARDMODE \_ occupé**</span><span class="sxs-lookup"><span data-stu-id="a8056-105"><span id="LINEFORWARDMODE_BUSY"></span><span id="lineforwardmode_busy"></span>**LINEFORWARDMODE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8056-106">Transférer tous les appels sur occupé, quelle que soit leur origine.</span><span class="sxs-lookup"><span data-stu-id="a8056-106">Forward all calls on busy, irrespective of their origin.</span></span> <span data-ttu-id="a8056-107">Utilisez cette valeur lorsque le transfert pour des appels internes et externes sur occupé et sans réponse ne peut pas être contrôlé séparément.</span><span class="sxs-lookup"><span data-stu-id="a8056-107">Use this value when forwarding for internal and external calls on busy and on no answer cannot be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8056-108"><span id="LINEFORWARDMODE_BUSYEXTERNAL"></span><span id="lineforwardmode_busyexternal"></span>**LINEFORWARDMODE \_ BUSYEXTERNAL**</span><span class="sxs-lookup"><span data-stu-id="a8056-108"><span id="LINEFORWARDMODE_BUSYEXTERNAL"></span><span id="lineforwardmode_busyexternal"></span>**LINEFORWARDMODE\_BUSYEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8056-109">Transférer tous les appels externes sur occupé.</span><span class="sxs-lookup"><span data-stu-id="a8056-109">Forward all external calls on busy.</span></span> <span data-ttu-id="a8056-110">Utilisez cette valeur lorsque le transfert pour des appels internes et externes sur occupé et sur aucune réponse peut être contrôlé séparément.</span><span class="sxs-lookup"><span data-stu-id="a8056-110">Use this value when forwarding for internal and external calls on busy and on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8056-111"><span id="LINEFORWARDMODE_BUSYINTERNAL"></span><span id="lineforwardmode_busyinternal"></span>**LINEFORWARDMODE \_ BUSYINTERNAL**</span><span class="sxs-lookup"><span data-stu-id="a8056-111"><span id="LINEFORWARDMODE_BUSYINTERNAL"></span><span id="lineforwardmode_busyinternal"></span>**LINEFORWARDMODE\_BUSYINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8056-112">Transférer tous les appels internes sur occupé.</span><span class="sxs-lookup"><span data-stu-id="a8056-112">Forward all internal calls on busy.</span></span> <span data-ttu-id="a8056-113">Utilisez cette valeur lorsque le transfert pour des appels internes et externes sur occupé et sur aucune réponse peut être contrôlé séparément.</span><span class="sxs-lookup"><span data-stu-id="a8056-113">Use this value when forwarding for internal and external calls on busy and on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8056-114"><span id="LINEFORWARDMODE_BUSYNA"></span><span id="lineforwardmode_busyna"></span>**LINEFORWARDMODE \_ BUSYNA**</span><span class="sxs-lookup"><span data-stu-id="a8056-114"><span id="LINEFORWARDMODE_BUSYNA"></span><span id="lineforwardmode_busyna"></span>**LINEFORWARDMODE\_BUSYNA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8056-115">Transférez tous les appels en cas de non-réponse, quelle que soit leur origine.</span><span class="sxs-lookup"><span data-stu-id="a8056-115">Forward all calls on busy/no answer, irrespective of their origin.</span></span> <span data-ttu-id="a8056-116">Utilisez cette valeur lorsque le transfert pour des appels internes et externes sur occupé et sans réponse ne peut pas être contrôlé séparément.</span><span class="sxs-lookup"><span data-stu-id="a8056-116">Use this value when forwarding for internal and external calls on busy and on no answer cannot be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8056-117"><span id="LINEFORWARDMODE_BUSYNAEXTERNAL"></span><span id="lineforwardmode_busynaexternal"></span>**LINEFORWARDMODE \_ BUSYNAEXTERNAL**</span><span class="sxs-lookup"><span data-stu-id="a8056-117"><span id="LINEFORWARDMODE_BUSYNAEXTERNAL"></span><span id="lineforwardmode_busynaexternal"></span>**LINEFORWARDMODE\_BUSYNAEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8056-118">Transférez tous les appels externes sur occupé/aucune réponse.</span><span class="sxs-lookup"><span data-stu-id="a8056-118">Forward all external calls on busy/no answer.</span></span> <span data-ttu-id="a8056-119">Utilisez cette valeur lorsque le transfert d’appels sur occupé et sur aucune réponse ne peut pas être contrôlé séparément pour les appels internes.</span><span class="sxs-lookup"><span data-stu-id="a8056-119">Use this value when call forwarding on busy and on no answer cannot be controlled separately for internal calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8056-120"><span id="LINEFORWARDMODE_BUSYNAINTERNAL"></span><span id="lineforwardmode_busynainternal"></span>**LINEFORWARDMODE \_ BUSYNAINTERNAL**</span><span class="sxs-lookup"><span data-stu-id="a8056-120"><span id="LINEFORWARDMODE_BUSYNAINTERNAL"></span><span id="lineforwardmode_busynainternal"></span>**LINEFORWARDMODE\_BUSYNAINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8056-121">Transférez tous les appels internes sur les appels occupés/sans réponse.</span><span class="sxs-lookup"><span data-stu-id="a8056-121">Forward all internal calls on busy/no answer.</span></span> <span data-ttu-id="a8056-122">Utilisez cette valeur lorsque le transfert d’appels sur occupé et sur aucune réponse ne peut pas être contrôlé séparément pour les appels internes.</span><span class="sxs-lookup"><span data-stu-id="a8056-122">Use this value when call forwarding on busy and on no answer cannot be controlled separately for internal calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8056-123"><span id="LINEFORWARDMODE_BUSYNASPECIFIC"></span><span id="lineforwardmode_busynaspecific"></span>**LINEFORWARDMODE \_ BUSYNASPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="a8056-123"><span id="LINEFORWARDMODE_BUSYNASPECIFIC"></span><span id="lineforwardmode_busynaspecific"></span>**LINEFORWARDMODE\_BUSYNASPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8056-124">Transférer sur occupé/non répondez à tous les appels provenant d’une adresse spécifiée (transfert sélectif de l’appel).</span><span class="sxs-lookup"><span data-stu-id="a8056-124">Forward on busy/no answer all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8056-125"><span id="LINEFORWARDMODE_BUSYSPECIFIC"></span><span id="lineforwardmode_busyspecific"></span>**LINEFORWARDMODE \_ BUSYSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="a8056-125"><span id="LINEFORWARDMODE_BUSYSPECIFIC"></span><span id="lineforwardmode_busyspecific"></span>**LINEFORWARDMODE\_BUSYSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8056-126">Transférer sur les appels occupés qui proviennent d’une adresse spécifiée (transfert d’appel sélectif).</span><span class="sxs-lookup"><span data-stu-id="a8056-126">Forward on busy all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8056-127"><span id="LINEFORWARDMODE_NOANSW"></span><span id="lineforwardmode_noansw"></span>**LINEFORWARDMODE \_ NOANSW**</span><span class="sxs-lookup"><span data-stu-id="a8056-127"><span id="LINEFORWARDMODE_NOANSW"></span><span id="lineforwardmode_noansw"></span>**LINEFORWARDMODE\_NOANSW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8056-128">Transférer tous les appels sans réponse, quelle que soit leur origine.</span><span class="sxs-lookup"><span data-stu-id="a8056-128">Forward all calls on no answer, irrespective of their origin.</span></span> <span data-ttu-id="a8056-129">Utilisez cette valeur lorsque le transfert d’appels pour les appels internes et externes sur aucune réponse ne peut pas être contrôlé séparément.</span><span class="sxs-lookup"><span data-stu-id="a8056-129">Use this value when call forwarding for internal and external calls on no answer cannot be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8056-130"><span id="LINEFORWARDMODE_NOANSWEXTERNAL"></span><span id="lineforwardmode_noanswexternal"></span>**LINEFORWARDMODE \_ NOANSWEXTERNAL**</span><span class="sxs-lookup"><span data-stu-id="a8056-130"><span id="LINEFORWARDMODE_NOANSWEXTERNAL"></span><span id="lineforwardmode_noanswexternal"></span>**LINEFORWARDMODE\_NOANSWEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8056-131">Transférez tous les appels externes sans réponse.</span><span class="sxs-lookup"><span data-stu-id="a8056-131">Forward all external calls on no answer.</span></span> <span data-ttu-id="a8056-132">Utilisez cette valeur lorsque le transfert pour des appels internes et externes sur aucune réponse peut être contrôlé séparément.</span><span class="sxs-lookup"><span data-stu-id="a8056-132">Use this value when forwarding for internal and external calls on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8056-133"><span id="LINEFORWARDMODE_NOANSWINTERNAL"></span><span id="lineforwardmode_noanswinternal"></span>**LINEFORWARDMODE \_ NOANSWINTERNAL**</span><span class="sxs-lookup"><span data-stu-id="a8056-133"><span id="LINEFORWARDMODE_NOANSWINTERNAL"></span><span id="lineforwardmode_noanswinternal"></span>**LINEFORWARDMODE\_NOANSWINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8056-134">Transférez tous les appels internes sans réponse.</span><span class="sxs-lookup"><span data-stu-id="a8056-134">Forward all internal calls on no answer.</span></span> <span data-ttu-id="a8056-135">Utilisez cette valeur lorsque le transfert pour des appels internes et externes sur aucune réponse peut être contrôlé séparément.</span><span class="sxs-lookup"><span data-stu-id="a8056-135">Use this value when forwarding for internal and external calls on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8056-136"><span id="LINEFORWARDMODE_NOANSWSPECIFIC"></span><span id="lineforwardmode_noanswspecific"></span>**LINEFORWARDMODE \_ NOANSWSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="a8056-136"><span id="LINEFORWARDMODE_NOANSWSPECIFIC"></span><span id="lineforwardmode_noanswspecific"></span>**LINEFORWARDMODE\_NOANSWSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8056-137">Transférer en l’absence de réponse tous les appels provenant d’une adresse spécifiée (transfert sélectif de l’appel).</span><span class="sxs-lookup"><span data-stu-id="a8056-137">Forward on no answer all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8056-138"><span id="LINEFORWARDMODE_UNAVAIL"></span><span id="lineforwardmode_unavail"></span>**LINEFORWARDMODE \_ INdispo**</span><span class="sxs-lookup"><span data-stu-id="a8056-138"><span id="LINEFORWARDMODE_UNAVAIL"></span><span id="lineforwardmode_unavail"></span>**LINEFORWARDMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8056-139">Les appels sont transférés, mais les conditions dans lesquelles le transfert se produit ne sont pas connues, et ne sont jamais connues du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="a8056-139">Calls are forwarded, but the conditions under which forwarding will occur are not known, and will never be known by the service provider.</span></span> <span data-ttu-id="a8056-140">(TAPI versions 1,4 et ultérieures)</span><span class="sxs-lookup"><span data-stu-id="a8056-140">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8056-141"><span id="LINEFORWARDMODE_UNCOND"></span><span id="lineforwardmode_uncond"></span>**LINEFORWARDMODE \_**</span><span class="sxs-lookup"><span data-stu-id="a8056-141"><span id="LINEFORWARDMODE_UNCOND"></span><span id="lineforwardmode_uncond"></span>**LINEFORWARDMODE\_UNCOND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8056-142">Transférez tous les appels de manière inconditionnelle, quelle que soit leur origine.</span><span class="sxs-lookup"><span data-stu-id="a8056-142">Forward all calls unconditionally, irrespective of their origin.</span></span> <span data-ttu-id="a8056-143">Utilisez cette valeur lorsque le transfert non conditionnel pour des appels internes et externes ne peut pas être contrôlé séparément.</span><span class="sxs-lookup"><span data-stu-id="a8056-143">Use this value when unconditional forwarding for internal and external calls cannot be controlled separately.</span></span> <span data-ttu-id="a8056-144">Le transfert non conditionnel remplace le transfert sur des conditions de réponse occupées et/ou aucune.</span><span class="sxs-lookup"><span data-stu-id="a8056-144">Unconditional forwarding overrides forwarding on busy and/or no answer conditions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8056-145"><span id="LINEFORWARDMODE_UNCONDEXTERNAL"></span><span id="lineforwardmode_uncondexternal"></span>**LINEFORWARDMODE \_ UNCONDEXTERNAL**</span><span class="sxs-lookup"><span data-stu-id="a8056-145"><span id="LINEFORWARDMODE_UNCONDEXTERNAL"></span><span id="lineforwardmode_uncondexternal"></span>**LINEFORWARDMODE\_UNCONDEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8056-146">Transférer tous les appels externes sans condition.</span><span class="sxs-lookup"><span data-stu-id="a8056-146">Forward all external calls unconditionally.</span></span> <span data-ttu-id="a8056-147">Utilisez cette valeur lorsque le transfert non conditionnel pour des appels internes et externes peut être contrôlé séparément.</span><span class="sxs-lookup"><span data-stu-id="a8056-147">Use this value when unconditional forwarding for internal and external calls can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8056-148"><span id="LINEFORWARDMODE_UNCONDINTERNAL"></span><span id="lineforwardmode_uncondinternal"></span>**LINEFORWARDMODE \_ UNCONDINTERNAL**</span><span class="sxs-lookup"><span data-stu-id="a8056-148"><span id="LINEFORWARDMODE_UNCONDINTERNAL"></span><span id="lineforwardmode_uncondinternal"></span>**LINEFORWARDMODE\_UNCONDINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8056-149">Transférer tous les appels internes de manière inconditionnelle.</span><span class="sxs-lookup"><span data-stu-id="a8056-149">Forward all internal calls unconditionally.</span></span> <span data-ttu-id="a8056-150">Utilisez cette valeur lorsque le transfert non conditionnel pour des appels internes et externes peut être contrôlé séparément.</span><span class="sxs-lookup"><span data-stu-id="a8056-150">Use this value when unconditional forwarding for internal and external calls can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8056-151"><span id="LINEFORWARDMODE_UNCONDSPECIFIC"></span><span id="lineforwardmode_uncondspecific"></span>**LINEFORWARDMODE \_ UNCONDSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="a8056-151"><span id="LINEFORWARDMODE_UNCONDSPECIFIC"></span><span id="lineforwardmode_uncondspecific"></span>**LINEFORWARDMODE\_UNCONDSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8056-152">Transférer de manière inconditionnelle tous les appels provenant d’une adresse spécifiée (transfert sélectif de l’appel).</span><span class="sxs-lookup"><span data-stu-id="a8056-152">Unconditionally forward all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8056-153"><span id="LINEFORWARDMODE_UNKNOWN"></span><span id="lineforwardmode_unknown"></span>**LINEFORWARDMODE \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="a8056-153"><span id="LINEFORWARDMODE_UNKNOWN"></span><span id="lineforwardmode_unknown"></span>**LINEFORWARDMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8056-154">Les appels sont transférés, mais les conditions dans lesquelles le transfert se produit ne sont pas connues pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="a8056-154">Calls are forwarded, but the conditions under which forwarding will occur are not known at this time.</span></span> <span data-ttu-id="a8056-155">Il est possible que les conditions soient connues à un moment ultérieur.</span><span class="sxs-lookup"><span data-stu-id="a8056-155">It is possible that the conditions may become known at a future time.</span></span> <span data-ttu-id="a8056-156">(TAPI versions 1,4 et ultérieures)</span><span class="sxs-lookup"><span data-stu-id="a8056-156">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8056-157">Notes</span><span class="sxs-lookup"><span data-stu-id="a8056-157">Remarks</span></span>

<span data-ttu-id="a8056-158">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="a8056-158">No extensibility.</span></span> <span data-ttu-id="a8056-159">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="a8056-159">All 32 bits are reserved.</span></span>

<span data-ttu-id="a8056-160">Les indicateurs binaires définis par LINEFORWARDMODE ne \_ sont pas orthogonals.</span><span class="sxs-lookup"><span data-stu-id="a8056-160">The bit flags defined by LINEFORWARDMODE\_ are not orthogonal.</span></span> <span data-ttu-id="a8056-161">Le transfert non conditionnel ignore toute condition spécifique, telle que occupé ou aucune réponse.</span><span class="sxs-lookup"><span data-stu-id="a8056-161">Unconditional forwarding ignores any specific condition such as busy or no answer.</span></span> <span data-ttu-id="a8056-162">Si le transfert non conditionnel n’est pas activé, le transfert sur occupé et sur aucune réponse peut être contrôlé séparément ou non séparément.</span><span class="sxs-lookup"><span data-stu-id="a8056-162">If unconditional forwarding is not in effect, then forwarding on busy and on no answer can be controlled separately or not separately.</span></span> <span data-ttu-id="a8056-163">S’ils sont contrôlés séparément, les \_ indicateurs LINEFORWARDMODE Busy et LINEFORWARDMODE \_ NOANSW peuvent être utilisés séparément.</span><span class="sxs-lookup"><span data-stu-id="a8056-163">If controlled separately, the LINEFORWARDMODE\_BUSY and LINEFORWARDMODE\_NOANSW flags can be used separately.</span></span> <span data-ttu-id="a8056-164">S’il n’est pas contrôlé séparément, l’indicateur LINEFORWARDMODE \_ BUSYNA doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="a8056-164">If not controlled separately, the flag LINEFORWARDMODE\_BUSYNA must be used.</span></span> <span data-ttu-id="a8056-165">De même, si le transfert d’appels internes et externes peut être contrôlé séparément, \_ les indicateurs externes LINEFORWARDMODE internes et LINEFORWARDMODE \_ peuvent être utilisés séparément ; sinon, la combinaison est utilisée.</span><span class="sxs-lookup"><span data-stu-id="a8056-165">Similarly, if forwarding of internal and external calls can be controlled separately, then LINEFORWARDMODE\_INTERNAL and LINEFORWARDMODE\_EXTERNAL flags can be used separately; otherwise the combination is used.</span></span>

<span data-ttu-id="a8056-166">Les fonctionnalités d’adresse indiquent les modes de transfert disponibles pour chaque adresse affectée à une ligne.</span><span class="sxs-lookup"><span data-stu-id="a8056-166">Address capabilities indicate which forwarding modes are available for each address assigned to a line.</span></span> <span data-ttu-id="a8056-167">Une application peut utiliser [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) pour définir des conditions de transfert au niveau du commutateur.</span><span class="sxs-lookup"><span data-stu-id="a8056-167">An application can use [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) to set forwarding conditions at the switch.</span></span>

<span data-ttu-id="a8056-168">Pour la compatibilité descendante, il incombe au fournisseur de services d’examiner la version de l’API négociée sur la ligne et de ne pas utiliser ces \_ valeurs LINEFORWARDMODE si la version négociée ne les prend pas en charge.</span><span class="sxs-lookup"><span data-stu-id="a8056-168">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use these LINEFORWARDMODE\_ values if the negotiated version does not support them.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8056-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8056-169">Requirements</span></span>



| <span data-ttu-id="a8056-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8056-170">Requirement</span></span> | <span data-ttu-id="a8056-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8056-171">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a8056-172">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="a8056-172">TAPI version</span></span><br/> | <span data-ttu-id="a8056-173">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a8056-173">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="a8056-174">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8056-174">Header</span></span><br/>       | <dl> <span data-ttu-id="a8056-175"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8056-175"><dt>Tapi.h</dt></span></span> </dl> |



 

 




