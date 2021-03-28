---
title: Sync (SM5-ASM)
description: Synchronisation de groupe de threads ou barrière de mémoire.
ms.assetid: DCA637FE-8F5C-41D0-8B5E-F913463BA387
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be072b51b4a18d9f1408df0907ec0a55131c18d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990856"
---
# <a name="sync-sm5---asm"></a><span data-ttu-id="f371f-103">Sync (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f371f-103">sync (sm5 - asm)</span></span>

<span data-ttu-id="f371f-104">Synchronisation de groupe de threads ou barrière de mémoire.</span><span class="sxs-lookup"><span data-stu-id="f371f-104">Thread group sync or memory barrier.</span></span>



| <span data-ttu-id="f371f-105">synchroniser \[ \_ Uglobal </span><span class="sxs-lookup"><span data-stu-id="f371f-105">sync\[\_uglobal</span></span>\|<span data-ttu-id="f371f-106">\_ugroup \] \[ \_ g \] \[ \_ t\]</span><span class="sxs-lookup"><span data-stu-id="f371f-106">\_ugroup\]\[\_g\]\[\_t\]</span></span> |
|-------------------------------------------|



 

## <a name="remarks"></a><span data-ttu-id="f371f-107">Notes</span><span class="sxs-lookup"><span data-stu-id="f371f-107">Remarks</span></span>

<span data-ttu-id="f371f-108">La **synchronisation** possède \_ les options Uglobal, \_ ugroup, \_ g et \_ t.</span><span class="sxs-lookup"><span data-stu-id="f371f-108">**Sync** has options \_uglobal, \_ugroup, \_g and \_t.</span></span>

<span data-ttu-id="f371f-109">Dans le nuanceur de pixels, seul **\_ Uglobal de synchronisation** est autorisé.</span><span class="sxs-lookup"><span data-stu-id="f371f-109">In the pixel shader, only **sync\_uglobal** is allowed.</span></span>

<span data-ttu-id="f371f-110">Dans le nuanceur de calcul, vous \_ devez spécifier (Uglobal ou \_ ugroup \* ) et/ou \_ g.</span><span class="sxs-lookup"><span data-stu-id="f371f-110">In the compute shader, (\_uglobal or \_ugroup\*) and/or \_g must be specified.</span></span> <span data-ttu-id="f371f-111">\_t est facultatif en plus.</span><span class="sxs-lookup"><span data-stu-id="f371f-111">\_t is optional in addition.</span></span>

### <a name="_uglobal"></a><span data-ttu-id="f371f-112">\_uglobal</span><span class="sxs-lookup"><span data-stu-id="f371f-112">\_uglobal</span></span>

<span data-ttu-id="f371f-113">\#Limite de mémoire globale u (UAV).</span><span class="sxs-lookup"><span data-stu-id="f371f-113">Global u\# (UAV) memory fence.</span></span>

<span data-ttu-id="f371f-114">Toutes les opérations de \# lecture/écriture de la mémoire u précédentes par ce thread dans l’ordre du programme sont rendues visibles à tous les threads de l’ensemble du GPU avant tout \# accès à la mémoire u ultérieur par ce thread.</span><span class="sxs-lookup"><span data-stu-id="f371f-114">All prior u\# memory reads/writes by this thread in program order are made visible to all threads on the entire GPU before any subsequent u\# memory accesses by this thread.</span></span> <span data-ttu-id="f371f-115">La partie GPU entière de la définition est remplacée par une portée « inférieur à » dans un cas, décrite ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="f371f-115">The entire GPU part of the definition is replaced by a less-than-global scope in one case, described below.</span></span>

<span data-ttu-id="f371f-116">Cela s’applique à toutes les mémoires UAV liées à l’étape de nuanceur actuelle.</span><span class="sxs-lookup"><span data-stu-id="f371f-116">This applies to all UAV memory bound at the current shader stage.</span></span>

<span data-ttu-id="f371f-117">\_Uglobal est disponible dans le nuanceur de calcul ou le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="f371f-117">\_uglobal is available in the compute shader or pixel shader.</span></span>

<span data-ttu-id="f371f-118">Pour tout UAV lié qui n’a pas été déclaré par le nuanceur comme cohérent globalement, la \_ barrière de mémoire Uglobal u \# dispose uniquement de la visibilité dans le groupe de threads du nuanceur de calcul actuel pour ce UAV, comme s’il s’agissait \_ de ugroup au lieu de \_ Uglobal.</span><span class="sxs-lookup"><span data-stu-id="f371f-118">For any bound UAV that has not been declared by the shader as Globally Coherent, the \_uglobal u\# memory fence only has visibility within the current compute shader thread-group for that UAV, as if it is \_ugroup instead of \_uglobal.</span></span> <span data-ttu-id="f371f-119">Ce problème s’applique uniquement au nuanceur de calcul, étant donné que le nuanceur de pixels doit déclarer tous les UAVs comme cohérents globalement.</span><span class="sxs-lookup"><span data-stu-id="f371f-119">This issue only applies to the compute shader, since the pixel shader must declare all UAVs as Globally Coherent.</span></span>

### <a name="_ugroup"></a><span data-ttu-id="f371f-120">\_ugroup</span><span class="sxs-lookup"><span data-stu-id="f371f-120">\_ugroup</span></span>

<span data-ttu-id="f371f-121">\#Limite de mémoire de l’étendue de groupe de threads u (UAV).</span><span class="sxs-lookup"><span data-stu-id="f371f-121">Thread group scope u\# (UAV) memory fence.</span></span>

<span data-ttu-id="f371f-122">Toutes les opérations de \# lecture ou d’écriture de la mémoire en u antérieures par ce thread dans l’ordre du programme sont rendues visibles à tous les threads dans le groupe de threads avant que la mémoire u suivante n' \# accède à ce thread.</span><span class="sxs-lookup"><span data-stu-id="f371f-122">All prior u\# memory reads or writes by this thread in program order are made visible to all threads in the thread group before any subsequent u\# memory accesses by this thread.</span></span>

<span data-ttu-id="f371f-123">Cela s’applique à toutes les mémoires UAV liées à l’étape de nuanceur actuelle.</span><span class="sxs-lookup"><span data-stu-id="f371f-123">This applies to all UAV memory bound at the current shader stage.</span></span>

<span data-ttu-id="f371f-124">\_ugroup est disponible uniquement dans le nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="f371f-124">\_ugroup is available in the compute shader only.</span></span>

<span data-ttu-id="f371f-125">Si \_ ugroup est exposé, pour certaines implémentations.</span><span class="sxs-lookup"><span data-stu-id="f371f-125">If \_ugroup is exposed, for some implementations.</span></span> <span data-ttu-id="f371f-126">L’avantage de spécifier \_ ugroup au lieu de \_ Uglobal est que l’opération de **synchronisation** peut s’effectuer plus rapidement.</span><span class="sxs-lookup"><span data-stu-id="f371f-126">The advantage of specifying \_ugroup instead of \_uglobal is that the **sync** operation can complete more quickly.</span></span>

<span data-ttu-id="f371f-127">D’autres implémentations ne distinguent pas \_ ugroup de \_ Uglobal, donc les deux opérations sont équivalentes et se comportent comme \_ Uglobal.</span><span class="sxs-lookup"><span data-stu-id="f371f-127">Other implementations do not distinguish \_ugroup from \_uglobal, so both operations are equivalent and behave like \_uglobal.</span></span> <span data-ttu-id="f371f-128">Les applications peuvent spécifier leur intention en demandant l’étendue de **synchronisation** la plus étroite nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f371f-128">Applications can specify their intent by requesting the narrowest scope of **sync** necessary.</span></span>

<span data-ttu-id="f371f-129">Même si un UAV particulier est déclaré comme cohérent globalement, une \_ opération de **synchronisation** ugroup fonctionnera plus efficacement sur ce UAV si un cloisonnement global n’est pas requis.</span><span class="sxs-lookup"><span data-stu-id="f371f-129">Even if a particular UAV is declared as Globally Coherent, a \_ugroup **sync** operation will function more efficiently on that UAV if a global barrier is not required.</span></span>

### <a name="_g"></a><span data-ttu-id="f371f-130">\_activée</span><span class="sxs-lookup"><span data-stu-id="f371f-130">\_g</span></span>

<span data-ttu-id="f371f-131">\#limite g (thread de groupe de threads partagés).</span><span class="sxs-lookup"><span data-stu-id="f371f-131">g\# (thread group shared memory) fence.</span></span>

<span data-ttu-id="f371f-132">Toutes les opérations de \# lecture ou d’écriture de la mémoire antérieure à g par ce thread dans l’ordre du programme sont rendues visibles à tous les threads dans le groupe de threads avant les \# accès à la mémoire g suivants par ce thread.</span><span class="sxs-lookup"><span data-stu-id="f371f-132">All prior g\# memory reads or writes by this thread in program order are made visible to all threads in the thread group before any subsequent g\# memory accesses by this thread.</span></span>

<span data-ttu-id="f371f-133">Cela s’applique à l’ensemble de la mémoire partagée du groupe de threads actuel \# .</span><span class="sxs-lookup"><span data-stu-id="f371f-133">This applies to all of the current thread group's g\# shared memory.</span></span>

<span data-ttu-id="f371f-134">\_g est disponible uniquement dans le nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="f371f-134">\_g is available in the compute shader only.</span></span>

### <a name="_t"></a><span data-ttu-id="f371f-135">\_t</span><span class="sxs-lookup"><span data-stu-id="f371f-135">\_t</span></span>

<span data-ttu-id="f371f-136">Synchronisation du groupe de threads. Tous les threads d’un groupe de threads unique (ceux qui peuvent partager l’accès à un ensemble commun d’espace de Registre partagé) sont exécutés jusqu’à ce qu’ils atteignent cette instruction avant que tout thread puisse continuer.</span><span class="sxs-lookup"><span data-stu-id="f371f-136">Thread group sync. All threads within a single thread group (those that can share access to a common set of shared register space) will be executed up to the point where they reach this instruction before any thread can continue.</span></span>

<span data-ttu-id="f371f-137">\_t ne peut pas être placé dans un contrôle de flux dynamique, (branches pouvant varier au sein d’un groupe de threads), mais peut être présent dans un contrôle de flux uniforme, où tous les threads du groupe sélectionnent le même chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="f371f-137">\_t cannot be placed in dynamic flow control, (branches which could vary within a thread group), but can be present in uniform flow control, where all threads in the group pick the same path.</span></span>

<span data-ttu-id="f371f-138">\_t est disponible uniquement dans le nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="f371f-138">\_t is available in the compute shader only.</span></span>

<span data-ttu-id="f371f-139">La liste suivante répertorie les variantes de « Sync » du nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="f371f-139">The following is a listing of compute shader ‘sync’ variants.</span></span>

-   <span data-ttu-id="f371f-140">synchronisation \_ g</span><span class="sxs-lookup"><span data-stu-id="f371f-140">sync\_g</span></span>
-   <span data-ttu-id="f371f-141">synchroniser \_ ugroup\*</span><span class="sxs-lookup"><span data-stu-id="f371f-141">sync\_ugroup\*</span></span>
-   <span data-ttu-id="f371f-142">synchroniser \_ Uglobal</span><span class="sxs-lookup"><span data-stu-id="f371f-142">sync\_uglobal</span></span>
-   <span data-ttu-id="f371f-143">synchronisation \_ g \_ t</span><span class="sxs-lookup"><span data-stu-id="f371f-143">sync\_g\_t</span></span>
-   <span data-ttu-id="f371f-144">synchroniser \_ ugroup \_ t\*</span><span class="sxs-lookup"><span data-stu-id="f371f-144">sync\_ugroup\_t\*</span></span>
-   <span data-ttu-id="f371f-145">synchroniser \_ Uglobal \_ t</span><span class="sxs-lookup"><span data-stu-id="f371f-145">sync\_uglobal\_t</span></span>
-   <span data-ttu-id="f371f-146">synchroniser \_ ugroup \_ g\*</span><span class="sxs-lookup"><span data-stu-id="f371f-146">sync\_ugroup\_g\*</span></span>
-   <span data-ttu-id="f371f-147">synchroniser \_ Uglobal \_ g</span><span class="sxs-lookup"><span data-stu-id="f371f-147">sync\_uglobal\_g</span></span>
-   <span data-ttu-id="f371f-148">synchroniser \_ ugroup \_ g \_ t\*</span><span class="sxs-lookup"><span data-stu-id="f371f-148">sync\_ugroup\_g\_t\*</span></span>
-   <span data-ttu-id="f371f-149">synchroniser \_ Uglobal \_ g \_ t</span><span class="sxs-lookup"><span data-stu-id="f371f-149">sync\_uglobal\_g\_t</span></span>

<span data-ttu-id="f371f-150">\*Les variantes avec \_ ugroup peuvent ne pas être ciblées par le compilateur HLSL, conformément à la discussion précédente de la \_ section ugroup ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="f371f-150">\*Variants with \_ugroup may not be targeted by the HLSL compiler, per the earlier discussion in the \_ugroup section above.</span></span>

<span data-ttu-id="f371f-151">La liste des variantes de synchronisation de nuanceur de pixels inclut Sync \_ Uglobal uniquement.</span><span class="sxs-lookup"><span data-stu-id="f371f-151">Listing of pixel shader sync variants include sync\_uglobal only.</span></span>

<span data-ttu-id="f371f-152">Les limites de mémoire empêchent la réorganisation des instructions affectées par les compilateurs ou le matériel sur la clôture.</span><span class="sxs-lookup"><span data-stu-id="f371f-152">Memory fences prevent affected instructions from being reordered by compilers or hardware across the fence.</span></span>

<span data-ttu-id="f371f-153">Plusieurs lectures à partir de la même adresse par un appel de nuanceur qui ne sont pas séparées par des barrières de mémoire ou des écritures vers l’adresse peuvent être réduites ensemble.</span><span class="sxs-lookup"><span data-stu-id="f371f-153">Multiple reads from the same address by a shader invocation that are not separated by memory barriers or writes to the address can be collapsed together.</span></span> <span data-ttu-id="f371f-154">Il en va de même pour les écritures.</span><span class="sxs-lookup"><span data-stu-id="f371f-154">The same applies to writes.</span></span> <span data-ttu-id="f371f-155">Les accès séparés par un cloisonnement ne peuvent pas être fusionnés ou déplacés sur le cloisonnement.</span><span class="sxs-lookup"><span data-stu-id="f371f-155">Accesses separated by a barrier cannot be merged or moved across the barrier.</span></span>

<span data-ttu-id="f371f-156">Les limites de mémoire ne sont pas nécessaires pour que les opérations atomiques sur une adresse donnée par différents threads fonctionnent correctement.</span><span class="sxs-lookup"><span data-stu-id="f371f-156">Memory fences are not necessary for atomic operations to a given address by different threads to function correctly.</span></span> <span data-ttu-id="f371f-157">Les délimitations sont nécessaires lorsque les opérations atomiques et/ou de charge/stockage doivent être synchronisées les unes par rapport aux autres, dans la mesure où elles apparaissent dans des threads individuels du point de vue d’autres threads.</span><span class="sxs-lookup"><span data-stu-id="f371f-157">Fences are needed when atomics and/or load/store operations need to be synchronized with respect to each other as they appear in individual threads from the point of view of other threads.</span></span>

<span data-ttu-id="f371f-158">Dans le nuanceur de pixels, les instructions [ignorent](discard--sm4---asm-.md) une \_ clôture de Uglobal de synchronisation, dans le sens où les instructions ne peuvent pas être réorganisées à travers la **suppression**.</span><span class="sxs-lookup"><span data-stu-id="f371f-158">In the pixel shader, [discard](discard--sm4---asm-.md) instructions imply a sync\_uglobal fence, in that instructions cannot be reordered across the **discard**.</span></span> <span data-ttu-id="f371f-159">synchroniser les \_ Uglobal dans les pixels d’assistance (qui s’exécutent uniquement pour prendre en charge les dérivés) ou les pixels ignorés peuvent avoir un impact quelconque.</span><span class="sxs-lookup"><span data-stu-id="f371f-159">sync\_uglobal in helper pixels (which run only to support derivatives) or discarded pixels may or may not have any affect.</span></span> <span data-ttu-id="f371f-160">Elle n’est pas autorisée pour les pixels d’assistance ou ignorés à écrire dans UAVs si, dans le cas d’un rejet, les écritures sont émises après la suppression.</span><span class="sxs-lookup"><span data-stu-id="f371f-160">It is not allowed for helper or discarded pixels to write to UAVs if, in the case of discard, the writes are issued after the discard.</span></span> <span data-ttu-id="f371f-161">Les valeurs retournées à partir de UAVs ne sont pas autorisées à contribuer aux calculs dérivés.</span><span class="sxs-lookup"><span data-stu-id="f371f-161">Returned values from UAVs are not allowed to contribute to derivative calculations.</span></span> <span data-ttu-id="f371f-162">Par conséquent, si \_ la synchronisation u est respectée ou non pour les pixels d’assistance ou lorsqu’elle est émise après la discutable de la suppression.</span><span class="sxs-lookup"><span data-stu-id="f371f-162">Therefore whether or not sync\_u is honored for helper pixels or when issued after a discard is moot.</span></span>

<span data-ttu-id="f371f-163">CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge cette instruction.</span><span class="sxs-lookup"><span data-stu-id="f371f-163">cs\_4\_0 and cs\_4\_1 support this instruction.</span></span>

<span data-ttu-id="f371f-164">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="f371f-164">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f371f-165">Sommet</span><span class="sxs-lookup"><span data-stu-id="f371f-165">Vertex</span></span> | <span data-ttu-id="f371f-166">Forme</span><span class="sxs-lookup"><span data-stu-id="f371f-166">Hull</span></span> | <span data-ttu-id="f371f-167">Domain</span><span class="sxs-lookup"><span data-stu-id="f371f-167">Domain</span></span> | <span data-ttu-id="f371f-168">Géométrie</span><span class="sxs-lookup"><span data-stu-id="f371f-168">Geometry</span></span> | <span data-ttu-id="f371f-169">Pixel</span><span class="sxs-lookup"><span data-stu-id="f371f-169">Pixel</span></span> | <span data-ttu-id="f371f-170">Compute</span><span class="sxs-lookup"><span data-stu-id="f371f-170">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="f371f-171">X</span><span class="sxs-lookup"><span data-stu-id="f371f-171">X</span></span>     | <span data-ttu-id="f371f-172">X</span><span class="sxs-lookup"><span data-stu-id="f371f-172">X</span></span>       |



 

<span data-ttu-id="f371f-173">Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, la variante **Sync \_ Uglobal** de cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f371f-173">Because UAVs are available at all shader stages for Direct3D 11.1, the **sync\_uglobal** variant of this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="f371f-174">Sommet</span><span class="sxs-lookup"><span data-stu-id="f371f-174">Vertex</span></span> | <span data-ttu-id="f371f-175">Forme</span><span class="sxs-lookup"><span data-stu-id="f371f-175">Hull</span></span> | <span data-ttu-id="f371f-176">Domain</span><span class="sxs-lookup"><span data-stu-id="f371f-176">Domain</span></span> | <span data-ttu-id="f371f-177">Géométrie</span><span class="sxs-lookup"><span data-stu-id="f371f-177">Geometry</span></span> | <span data-ttu-id="f371f-178">Pixel</span><span class="sxs-lookup"><span data-stu-id="f371f-178">Pixel</span></span> | <span data-ttu-id="f371f-179">Compute</span><span class="sxs-lookup"><span data-stu-id="f371f-179">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f371f-180">X</span><span class="sxs-lookup"><span data-stu-id="f371f-180">X</span></span>      | <span data-ttu-id="f371f-181">X</span><span class="sxs-lookup"><span data-stu-id="f371f-181">X</span></span>    | <span data-ttu-id="f371f-182">X</span><span class="sxs-lookup"><span data-stu-id="f371f-182">X</span></span>      | <span data-ttu-id="f371f-183">X</span><span class="sxs-lookup"><span data-stu-id="f371f-183">X</span></span>        | <span data-ttu-id="f371f-184">X</span><span class="sxs-lookup"><span data-stu-id="f371f-184">X</span></span>     | <span data-ttu-id="f371f-185">X</span><span class="sxs-lookup"><span data-stu-id="f371f-185">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f371f-186">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="f371f-186">Minimum Shader Model</span></span>

<span data-ttu-id="f371f-187">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="f371f-187">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f371f-188">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="f371f-188">Shader Model</span></span>                                              | <span data-ttu-id="f371f-189">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="f371f-189">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f371f-190">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="f371f-190">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f371f-191">Oui</span><span class="sxs-lookup"><span data-stu-id="f371f-191">yes</span></span>       |
| [<span data-ttu-id="f371f-192">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="f371f-192">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f371f-193">non</span><span class="sxs-lookup"><span data-stu-id="f371f-193">no</span></span>        |
| [<span data-ttu-id="f371f-194">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="f371f-194">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f371f-195">non</span><span class="sxs-lookup"><span data-stu-id="f371f-195">no</span></span>        |
| [<span data-ttu-id="f371f-196">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f371f-196">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f371f-197">non</span><span class="sxs-lookup"><span data-stu-id="f371f-197">no</span></span>        |
| [<span data-ttu-id="f371f-198">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f371f-198">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f371f-199">non</span><span class="sxs-lookup"><span data-stu-id="f371f-199">no</span></span>        |
| [<span data-ttu-id="f371f-200">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f371f-200">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f371f-201">non</span><span class="sxs-lookup"><span data-stu-id="f371f-201">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f371f-202">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f371f-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f371f-203">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f371f-203">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




