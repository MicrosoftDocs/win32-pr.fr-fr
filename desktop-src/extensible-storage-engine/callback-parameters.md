---
description: 'En savoir plus sur : paramètres de rappel'
title: Paramètres de rappel
TOCTitle: Callback Parameters
ms:assetid: 7f3cdc13-ffbd-4e5a-b650-1c6388e784dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269310(v=EXCHG.10)
ms:contentKeyID: 32765600
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e06ed65bbeae195060e4de10424a76a4228f20f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114095"
---
# <a name="callback-parameters"></a><span data-ttu-id="40172-103">Paramètres de rappel</span><span class="sxs-lookup"><span data-stu-id="40172-103">Callback Parameters</span></span>


<span data-ttu-id="40172-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="40172-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="callback-parameters"></a><span data-ttu-id="40172-105">Paramètres de rappel</span><span class="sxs-lookup"><span data-stu-id="40172-105">Callback Parameters</span></span>

<span data-ttu-id="40172-106">Cette rubrique contient des paramètres qui sont utilisés pour les rappels.</span><span class="sxs-lookup"><span data-stu-id="40172-106">This topic contains parameters that are used for callbacks.</span></span>

<span data-ttu-id="40172-107">*JET_paramDisableCallbacks*</span><span class="sxs-lookup"><span data-stu-id="40172-107">*JET_paramDisableCallbacks*</span></span>  
<span data-ttu-id="40172-108">65</span><span class="sxs-lookup"><span data-stu-id="40172-108">65</span></span>  

<span data-ttu-id="40172-109">Ce paramètre désactive tous les rappels du moteur de base de données pour les fonctions fournies par l’application.</span><span class="sxs-lookup"><span data-stu-id="40172-109">This parameter disables all database engine callbacks to application provided functions.</span></span> <span data-ttu-id="40172-110">Elle est principalement destinée à prendre en charge les utilitaires du moteur de base de données et n’est pas destinée à être utilisée dans votre application.</span><span class="sxs-lookup"><span data-stu-id="40172-110">It is primarily intended to support the database engine utilities and is not intended to be used in your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40172-111">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="40172-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="40172-112">Faux</span><span class="sxs-lookup"><span data-stu-id="40172-112">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40172-113">Tapez :</span><span class="sxs-lookup"><span data-stu-id="40172-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="40172-114">Boolean</span><span class="sxs-lookup"><span data-stu-id="40172-114">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40172-115">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="40172-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="40172-116">False, True</span><span class="sxs-lookup"><span data-stu-id="40172-116">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40172-117">Étendue :</span><span class="sxs-lookup"><span data-stu-id="40172-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="40172-118">Instance</span><span class="sxs-lookup"><span data-stu-id="40172-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40172-119">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="40172-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="40172-120">Oui</span><span class="sxs-lookup"><span data-stu-id="40172-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40172-121">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="40172-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="40172-122">Non</span><span class="sxs-lookup"><span data-stu-id="40172-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40172-123">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="40172-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="40172-124">Non</span><span class="sxs-lookup"><span data-stu-id="40172-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40172-125">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="40172-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="40172-126">Non</span><span class="sxs-lookup"><span data-stu-id="40172-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40172-127">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="40172-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="40172-128">Non</span><span class="sxs-lookup"><span data-stu-id="40172-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40172-129">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="40172-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="40172-130">Non</span><span class="sxs-lookup"><span data-stu-id="40172-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40172-131">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="40172-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="40172-132">Windows XP et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="40172-132">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="40172-133">*JET_paramEnablePersistedCallbacks*</span><span class="sxs-lookup"><span data-stu-id="40172-133">*JET_paramEnablePersistedCallbacks*</span></span>  
<span data-ttu-id="40172-134">156</span><span class="sxs-lookup"><span data-stu-id="40172-134">156</span></span>  

<span data-ttu-id="40172-135">Ce paramètre permet l’utilisation de rappels persistants dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="40172-135">This parameter enables the use of persistent callbacks in the database.</span></span> <span data-ttu-id="40172-136">Dans les versions antérieures à Windows Vista, l’utilisation de rappels persistants était activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="40172-136">In releases prior to Windows Vista, the use of persistent callbacks was enabled by default.</span></span> <span data-ttu-id="40172-137">Les applications doivent maintenant activer explicitement l’utilisation de rappels persistants au moment de l’exécution à l’aide de ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="40172-137">Applications must now explicitly enable the use of persistent callbacks at runtime using this parameter.</span></span> <span data-ttu-id="40172-138">Si ce paramètre n’est pas défini, toute opération de base de données qui requiert l’appel d’un rappel échouera avec JET_errCallbackFailed.</span><span class="sxs-lookup"><span data-stu-id="40172-138">If this parameter is not set, then any database operation that requires the invocation of a callback will fail with JET_errCallbackFailed.</span></span> <span data-ttu-id="40172-139">Ce paramètre n’affecte pas les rappels spécifiés au moment de l’exécution avec les mécanismes suivants : JET_paramRuntimeCallback, [JetRegisterCallback](./jetregistercallback-function.md)ou un paramètre de rappel explicite à une API jet.</span><span class="sxs-lookup"><span data-stu-id="40172-139">This parameter does not affect any callbacks that are specified at runtime with the following mechanisms: JET_paramRuntimeCallback, [JetRegisterCallback](./jetregistercallback-function.md), or an explicit callback parameter to a JET API.</span></span> <span data-ttu-id="40172-140">Il est toujours possible de créer des éléments de schéma qui contiennent des rappels persistants, même si l’utilisation de ces rappels persistants est interdite.</span><span class="sxs-lookup"><span data-stu-id="40172-140">It is still possible to create schema elements that contain persistent callbacks even when the use of those persistent callbacks is disallowed.</span></span> <span data-ttu-id="40172-141">Quand ce paramètre est défini sur false, il remplace JET_paramDisableCallbacks.</span><span class="sxs-lookup"><span data-stu-id="40172-141">When this parameter is set to false it overrides JET_paramDisableCallbacks.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40172-142">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="40172-142">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="40172-143">Faux</span><span class="sxs-lookup"><span data-stu-id="40172-143">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40172-144">Tapez :</span><span class="sxs-lookup"><span data-stu-id="40172-144">Type:</span></span></p></td>
<td><p><span data-ttu-id="40172-145">Boolean</span><span class="sxs-lookup"><span data-stu-id="40172-145">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40172-146">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="40172-146">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="40172-147">False, True</span><span class="sxs-lookup"><span data-stu-id="40172-147">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40172-148">Étendue :</span><span class="sxs-lookup"><span data-stu-id="40172-148">Scope:</span></span></p></td>
<td><p><span data-ttu-id="40172-149">Instance</span><span class="sxs-lookup"><span data-stu-id="40172-149">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40172-150">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="40172-150">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="40172-151">Oui</span><span class="sxs-lookup"><span data-stu-id="40172-151">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40172-152">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="40172-152">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="40172-153">Non</span><span class="sxs-lookup"><span data-stu-id="40172-153">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40172-154">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="40172-154">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="40172-155">Non</span><span class="sxs-lookup"><span data-stu-id="40172-155">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40172-156">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="40172-156">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="40172-157">Non</span><span class="sxs-lookup"><span data-stu-id="40172-157">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40172-158">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="40172-158">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="40172-159">Non</span><span class="sxs-lookup"><span data-stu-id="40172-159">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40172-160">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="40172-160">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="40172-161">Non</span><span class="sxs-lookup"><span data-stu-id="40172-161">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40172-162">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="40172-162">Availability:</span></span></p></td>
<td><p><span data-ttu-id="40172-163">Windows Vista et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="40172-163">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="40172-164">*JET_paramRuntimeCallback*</span><span class="sxs-lookup"><span data-stu-id="40172-164">*JET_paramRuntimeCallback*</span></span>  
<span data-ttu-id="40172-165">73</span><span class="sxs-lookup"><span data-stu-id="40172-165">73</span></span>  

<span data-ttu-id="40172-166">Ce paramètre configure le moteur à l’aide d’une fonction de rappel d’exécution qui implémente l’interface [JET_CALLBACK](./jet-callback-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="40172-166">This parameter configures the engine with a runtime callback function implementing the [JET_CALLBACK](./jet-callback-callback-function.md) interface.</span></span> <span data-ttu-id="40172-167">Ce rappel peut être appelé pour les raisons suivantes : [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md)ou [JET_cbtypNull](./jet-cbtyp.md).</span><span class="sxs-lookup"><span data-stu-id="40172-167">This callback may be called for the following reasons: [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md), or [JET_cbtypNull](./jet-cbtyp.md).</span></span> <span data-ttu-id="40172-168">Pour plus d’informations, consultez [JetSetLS](./jetsetls-function.md) .</span><span class="sxs-lookup"><span data-stu-id="40172-168">Please see [JetSetLS](./jetsetls-function.md) for more information.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40172-169">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="40172-169">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="40172-170">NULL</span><span class="sxs-lookup"><span data-stu-id="40172-170">NULL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40172-171">Tapez :</span><span class="sxs-lookup"><span data-stu-id="40172-171">Type:</span></span></p></td>
<td><p><span data-ttu-id="40172-172">Pointeur de fonction (JET_API_PTR)</span><span class="sxs-lookup"><span data-stu-id="40172-172">Function Pointer (JET_API_PTR)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40172-173">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="40172-173">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="40172-174">NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>\*</span><span class="sxs-lookup"><span data-stu-id="40172-174">NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>\*</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40172-175">Étendue :</span><span class="sxs-lookup"><span data-stu-id="40172-175">Scope:</span></span></p></td>
<td><p><span data-ttu-id="40172-176">Instance</span><span class="sxs-lookup"><span data-stu-id="40172-176">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40172-177">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="40172-177">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="40172-178">Oui</span><span class="sxs-lookup"><span data-stu-id="40172-178">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40172-179">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="40172-179">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="40172-180">Non</span><span class="sxs-lookup"><span data-stu-id="40172-180">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40172-181">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="40172-181">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="40172-182">Non</span><span class="sxs-lookup"><span data-stu-id="40172-182">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40172-183">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="40172-183">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="40172-184">Non</span><span class="sxs-lookup"><span data-stu-id="40172-184">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40172-185">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="40172-185">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="40172-186">Non</span><span class="sxs-lookup"><span data-stu-id="40172-186">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40172-187">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="40172-187">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="40172-188">Non</span><span class="sxs-lookup"><span data-stu-id="40172-188">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40172-189">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="40172-189">Availability:</span></span></p></td>
<td><p><span data-ttu-id="40172-190">Windows XP et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="40172-190">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="40172-191">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40172-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40172-192"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="40172-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="40172-193">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="40172-193">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40172-194"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="40172-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="40172-195">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="40172-195">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40172-196"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="40172-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="40172-197">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="40172-197">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="40172-198">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40172-198">See Also</span></span>

[<span data-ttu-id="40172-199">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="40172-199">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="40172-200">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="40172-200">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="40172-201">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="40172-201">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="40172-202">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="40172-202">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="40172-203">JetInit</span><span class="sxs-lookup"><span data-stu-id="40172-203">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="40172-204">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="40172-204">JetSetLS</span></span>](./jetsetls-function.md)
