---
title: dcl_interface_dynamicindexed (SM5-ASM)
description: Déclarez les pointeurs de table de fonction (interfaces). | dcl_interface_dynamicindexed (SM5-ASM)
ms.assetid: 5C77EBB6-7AEC-4471-AA6E-0F6D3E215156
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f78bb0152b44f7e29b9e76221db13da0c465a434
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992069"
---
# <a name="dcl_interface_dynamicindexed-sm5---asm"></a><span data-ttu-id="2bda9-104">\_dynamicindexed d’interface DCL \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="2bda9-104">dcl\_interface\_dynamicindexed (sm5 - asm)</span></span>

<span data-ttu-id="2bda9-105">Déclarez les pointeurs de table de fonction (interfaces).</span><span class="sxs-lookup"><span data-stu-id="2bda9-105">Declare function table pointers (interfaces).</span></span>



| <span data-ttu-id="2bda9-106">DCL \_ interface \_ dynamicindexed FP \# \[ arraySize \] \[ numCallSites \] = {ft \# , ft \# ,...}</span><span class="sxs-lookup"><span data-stu-id="2bda9-106">dcl\_interface\_dynamicindexed fp\#\[arraySize\]\[numCallSites\] = {ft\#, ft\#, ...}</span></span> |
|--------------------------------------------------------------------------------------|



 



| <span data-ttu-id="2bda9-107">Élément</span><span class="sxs-lookup"><span data-stu-id="2bda9-107">Item</span></span>                                                          | <span data-ttu-id="2bda9-108">Description</span><span class="sxs-lookup"><span data-stu-id="2bda9-108">Description</span></span>                                    |
|---------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="2bda9-109"><span id="fp_"></span><span id="FP_"></span>*ép\#*</span><span class="sxs-lookup"><span data-stu-id="2bda9-109"><span id="fp_"></span><span id="FP_"></span>*fp\#*</span></span><br/> | <span data-ttu-id="2bda9-110">\[dans \] les pointeurs de table de fonctions.</span><span class="sxs-lookup"><span data-stu-id="2bda9-110">\[in\] The function table pointers.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2bda9-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2bda9-111">Remarks</span></span>

<span data-ttu-id="2bda9-112">Chaque interface doit être liée à partir de l’API avant que le nuanceur ne soit utilisable.</span><span class="sxs-lookup"><span data-stu-id="2bda9-112">Each interface needs to be bound from the API before the shader is usable.</span></span> <span data-ttu-id="2bda9-113">La liaison fournit une référence à l’une des tables de fonctions afin que les emplacements de méthode puissent être remplis.</span><span class="sxs-lookup"><span data-stu-id="2bda9-113">Binding gives a reference to one of the function tables so that the method slots can be filled in.</span></span> <span data-ttu-id="2bda9-114">Le compilateur ne génère pas de pointeurs pour les objets non référencés.</span><span class="sxs-lookup"><span data-stu-id="2bda9-114">The compiler will not generate pointers for unreferenced objects.</span></span>

<span data-ttu-id="2bda9-115">Un pointeur de table de fonction a un jeu complet d’emplacements de méthode pour éviter le niveau supplémentaire d’indirection qu’une représentation de pointeur vers vtable C++ nécessiterait.</span><span class="sxs-lookup"><span data-stu-id="2bda9-115">A function table pointer has a full set of method slots to avoid the extra level of indirection that a C++ pointer-to- pointer-to-vtable representation would require.</span></span> <span data-ttu-id="2bda9-116">Cela nécessite également que les pointeurs soient de 5 tuples.</span><span class="sxs-lookup"><span data-stu-id="2bda9-116">That would also require that this pointers be 5-tuples.</span></span> <span data-ttu-id="2bda9-117">Dans le modèle d’incorporation virtuel HLSL, il est toujours connu de quelle variable/entrée globale est utilisée pour un appel afin de pouvoir configurer des tables par objet racine.</span><span class="sxs-lookup"><span data-stu-id="2bda9-117">In the HLSL virtual inlining model it's always known what global variable/input is used for a call so we can set up tables per root object.</span></span>

<span data-ttu-id="2bda9-118">Les déclarations de pointeur de fonction indiquent les tables de fonctions qui sont autorisées à être utilisées avec elles.</span><span class="sxs-lookup"><span data-stu-id="2bda9-118">Function pointer declarations indicate which function tables are legal to use with them.</span></span> <span data-ttu-id="2bda9-119">Cela permet également la dérivation des informations de corrélation de méthode.</span><span class="sxs-lookup"><span data-stu-id="2bda9-119">This also allows derivation of method correlation information.</span></span>

<span data-ttu-id="2bda9-120">La première \[ \] d’une déclaration d’interface correspond à la taille du tableau.</span><span class="sxs-lookup"><span data-stu-id="2bda9-120">The first \[\] of an interface declaration is the array size.</span></span> <span data-ttu-id="2bda9-121">Si l’indexation dynamique est utilisée, la déclaration indiquera que comme indiqué.</span><span class="sxs-lookup"><span data-stu-id="2bda9-121">If dynamic indexing is used the declaration will indicate that as shown.</span></span> <span data-ttu-id="2bda9-122">Un tableau de pointeurs d’interface peut également être indexé de manière statique. en outre, il n’est pas nécessaire que les tableaux de pointeurs d’interface représentent l’indexation dynamique.</span><span class="sxs-lookup"><span data-stu-id="2bda9-122">An array of interface pointers can be indexed statically also, it is not required that arrays of interface pointers mean dynamic indexing.</span></span>

<span data-ttu-id="2bda9-123">La numérotation des pointeurs d’interface commence à 0 pour la première déclaration et prend ensuite en compte la taille du tableau. le premier pointeur après un tableau d’entrée FP0 \[ 4 \] \[ 1 \] est donc FP4 \[ \] \[ \] .</span><span class="sxs-lookup"><span data-stu-id="2bda9-123">Numbering of interface pointers starts at 0 for the first declaration and subsequently takes array size into account, so the first pointer after a four entry array fp0\[4\]\[1\] would be fp4\[\]\[\].</span></span>

<span data-ttu-id="2bda9-124">La deuxième \[ \] d’une déclaration d’interface est le nombre de sites d’appel, qui doivent correspondre au nombre de corps dans chaque table référencée dans la déclaration.</span><span class="sxs-lookup"><span data-stu-id="2bda9-124">The second \[\] of an interface declaration is the number of call sites, which must match the number of bodies in each table referenced in the declaration.</span></span>

<span data-ttu-id="2bda9-125">Il n’existe aucune limite au nombre de choix de table de fonctions (ft \# ) pouvant être répertoriés dans une déclaration d’interface.</span><span class="sxs-lookup"><span data-stu-id="2bda9-125">There are no bounds to how many function table (ft\#) choices can be listed in an interface declaration.</span></span>

<span data-ttu-id="2bda9-126">Une table de fonctions donnée \# peut apparaître plusieurs fois dans une ou plusieurs déclarations d’interface.</span><span class="sxs-lookup"><span data-stu-id="2bda9-126">A given function table (ft\#) can appear more than once in one or more interface declarations.</span></span>

### <a name="restrictions"></a><span data-ttu-id="2bda9-127">Restrictions</span><span class="sxs-lookup"><span data-stu-id="2bda9-127">Restrictions</span></span>

-   <span data-ttu-id="2bda9-128">Le nombre de sites d’objets dans un nuanceur, qui est la somme de toutes les déclarations *FP \#* de leurs \[ \] déclarations arraySize, ne doit pas être supérieur à 253.</span><span class="sxs-lookup"><span data-stu-id="2bda9-128">The number of object sites in a shader, which is the sum across all *fp\#* declarations of their \[arraySize\] declarations, must be no more than 253.</span></span> <span data-ttu-id="2bda9-129">Ce nombre correspond au nombre de **ces** pointeurs pouvant être présents.</span><span class="sxs-lookup"><span data-stu-id="2bda9-129">This number corresponds to how many **this** pointers can be present.</span></span> <span data-ttu-id="2bda9-130">Le runtime applique cette limite de 253 pour conserver une limite sur la taille de l’interface DDI pour communiquer ces données de pointeur.</span><span class="sxs-lookup"><span data-stu-id="2bda9-130">The runtime enforces this 253 limit to keep a bound on the size of the DDI for communicating this pointer data.</span></span>
-   <span data-ttu-id="2bda9-131">Le nombre de sites d’appel dans un nuanceur, qui est la somme de toutes les instructions FCALL du nombre de cibles de branche potentielles, ne doit pas être supérieur à 4096.</span><span class="sxs-lookup"><span data-stu-id="2bda9-131">The number of call sites in a shader, which is the sum across all fcall statements of the number of potential branch targets, must be no more than 4096.</span></span>

    <span data-ttu-id="2bda9-132">Par exemple, un [FCALL](fcall--sm5---asm-.md) qui utilise un index statique pour la première *dimension \[ \] \[ \] FP* compte comme un :</span><span class="sxs-lookup"><span data-stu-id="2bda9-132">For example, an [fcall](fcall--sm5---asm-.md) that uses a static index for the first *fp\[\]\[\]* dimension counts as one:</span></span>

    `                       fcall fp0[0][0]         // +1`

    <span data-ttu-id="2bda9-133">Un **FCALL** qui utilise un index dynamique compte comme nombre d’éléments dans le tableau (premier \[ \] de l' **\_ interface DCL**) :</span><span class="sxs-lookup"><span data-stu-id="2bda9-133">An **fcall** that uses a dynamic index counts as the number of elements in the array (first \[\] of **dcl\_interface**):</span></span>

    `                    dcl_interface_dynamicindexed fp1[2][1] = {ft2, ft3, ft4}                      ...                     `

    `fcall fp1[r0.z + 0][1]  // +2`

    <span data-ttu-id="2bda9-134">Cette limite aide certaines implémentations à adapter facilement les tables des sélections de corps de fonction dans un stockage de type mémoire tampon constant.</span><span class="sxs-lookup"><span data-stu-id="2bda9-134">This limit helps some implementations easily fit tables of function body selections in constant buffer-like storage.</span></span>

<span data-ttu-id="2bda9-135">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="2bda9-135">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2bda9-136">Sommet</span><span class="sxs-lookup"><span data-stu-id="2bda9-136">Vertex</span></span> | <span data-ttu-id="2bda9-137">Forme</span><span class="sxs-lookup"><span data-stu-id="2bda9-137">Hull</span></span> | <span data-ttu-id="2bda9-138">Domain</span><span class="sxs-lookup"><span data-stu-id="2bda9-138">Domain</span></span> | <span data-ttu-id="2bda9-139">Géométrie</span><span class="sxs-lookup"><span data-stu-id="2bda9-139">Geometry</span></span> | <span data-ttu-id="2bda9-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="2bda9-140">Pixel</span></span> | <span data-ttu-id="2bda9-141">Compute</span><span class="sxs-lookup"><span data-stu-id="2bda9-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2bda9-142">X</span><span class="sxs-lookup"><span data-stu-id="2bda9-142">X</span></span>      | <span data-ttu-id="2bda9-143">X</span><span class="sxs-lookup"><span data-stu-id="2bda9-143">X</span></span>    | <span data-ttu-id="2bda9-144">X</span><span class="sxs-lookup"><span data-stu-id="2bda9-144">X</span></span>      | <span data-ttu-id="2bda9-145">X</span><span class="sxs-lookup"><span data-stu-id="2bda9-145">X</span></span>        | <span data-ttu-id="2bda9-146">X</span><span class="sxs-lookup"><span data-stu-id="2bda9-146">X</span></span>     | <span data-ttu-id="2bda9-147">X</span><span class="sxs-lookup"><span data-stu-id="2bda9-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2bda9-148">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="2bda9-148">Minimum Shader Model</span></span>

<span data-ttu-id="2bda9-149">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="2bda9-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2bda9-150">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="2bda9-150">Shader Model</span></span>                                              | <span data-ttu-id="2bda9-151">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="2bda9-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2bda9-152">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="2bda9-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2bda9-153">Oui</span><span class="sxs-lookup"><span data-stu-id="2bda9-153">yes</span></span>       |
| [<span data-ttu-id="2bda9-154">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="2bda9-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2bda9-155">non</span><span class="sxs-lookup"><span data-stu-id="2bda9-155">no</span></span>        |
| [<span data-ttu-id="2bda9-156">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="2bda9-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2bda9-157">non</span><span class="sxs-lookup"><span data-stu-id="2bda9-157">no</span></span>        |
| [<span data-ttu-id="2bda9-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2bda9-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2bda9-159">non</span><span class="sxs-lookup"><span data-stu-id="2bda9-159">no</span></span>        |
| [<span data-ttu-id="2bda9-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2bda9-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2bda9-161">non</span><span class="sxs-lookup"><span data-stu-id="2bda9-161">no</span></span>        |
| [<span data-ttu-id="2bda9-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2bda9-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2bda9-163">non</span><span class="sxs-lookup"><span data-stu-id="2bda9-163">no</span></span>        |



 

<span data-ttu-id="2bda9-164">CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge cette instruction pour UAV et SRV.</span><span class="sxs-lookup"><span data-stu-id="2bda9-164">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and SRV.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2bda9-165">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2bda9-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bda9-166">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2bda9-166">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





