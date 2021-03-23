---
title: Liaison de ressources en HLSL
description: Cette rubrique décrit certaines fonctionnalités spécifiques à l’utilisation du modèle de nuanceur HLSL (High Level Shader Language) 5,1 avec Direct3D 12.
ms.assetid: 3CD4BDAD-8AE3-4DE0-B3F8-9C9F9E83BBE9
ms.localizationpriority: high
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 749fed319f9ffe840f2b06512e337efa28081e24
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548566"
---
# <a name="resource-binding-in-hlsl"></a><span data-ttu-id="fcc6e-103">Liaison de ressources en HLSL</span><span class="sxs-lookup"><span data-stu-id="fcc6e-103">Resource binding in HLSL</span></span>

<span data-ttu-id="fcc6e-104">Cette rubrique décrit certaines fonctionnalités spécifiques à l’utilisation du [modèle de nuanceur](/windows/desktop/direct3dhlsl/shader-model-5-1) HLSL (High Level Shader Language) 5,1 avec Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-104">This topic describes some specific features of using High Level Shader Language (HLSL) [Shader Model 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) with Direct3D 12.</span></span> <span data-ttu-id="fcc6e-105">Tout le matériel Direct3D 12 prend en charge le modèle de nuanceur 5,1. par conséquent, la prise en charge de ce modèle ne dépend pas du niveau de fonctionnalité matérielle.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-105">All Direct3D 12 hardware supports Shader Model 5.1, so support for this model does not depend on what the hardware feature level is.</span></span>

-   [<span data-ttu-id="fcc6e-106">Types de ressources et tableaux</span><span class="sxs-lookup"><span data-stu-id="fcc6e-106">Resource types and arrays</span></span>](#resource-types-and-arrays)
-   [<span data-ttu-id="fcc6e-107">Tableaux de descripteurs et tableaux de texture</span><span class="sxs-lookup"><span data-stu-id="fcc6e-107">Descriptor arrays and texture arrays</span></span>](#descriptor-arrays-and-texture-arrays)
-   [<span data-ttu-id="fcc6e-108">Alias des ressources</span><span class="sxs-lookup"><span data-stu-id="fcc6e-108">Resource aliasing</span></span>](#resource-aliasing)
-   [<span data-ttu-id="fcc6e-109">Divergence et dérivées</span><span class="sxs-lookup"><span data-stu-id="fcc6e-109">Divergence and derivatives</span></span>](#divergence-and-derivatives)
-   [<span data-ttu-id="fcc6e-110">UAVs dans les nuanceurs de pixels</span><span class="sxs-lookup"><span data-stu-id="fcc6e-110">UAVs in pixel shaders</span></span>](#uavs-in-pixel-shaders)
-   [<span data-ttu-id="fcc6e-111">Mémoires tampons constantes</span><span class="sxs-lookup"><span data-stu-id="fcc6e-111">Constant Buffers</span></span>](#constant-buffers)
-   [<span data-ttu-id="fcc6e-112">Changements de bytecode dans SM 5.1</span><span class="sxs-lookup"><span data-stu-id="fcc6e-112">Bytecode changes in SM5.1</span></span>](#bytecode-changes-in-sm51)
-   [<span data-ttu-id="fcc6e-113">Exemples de déclarations HLSL</span><span class="sxs-lookup"><span data-stu-id="fcc6e-113">Example HLSL Declarations</span></span>](#example-hlsl-declarations)
-   [<span data-ttu-id="fcc6e-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fcc6e-114">Related topics</span></span>](#related-topics)

## <a name="resource-types-and-arrays"></a><span data-ttu-id="fcc6e-115">Types de ressources et tableaux</span><span class="sxs-lookup"><span data-stu-id="fcc6e-115">Resource types and arrays</span></span>

<span data-ttu-id="fcc6e-116">La syntaxe de ressource Shader Model 5 (SM 5.0) utilise le `register` mot clé pour transmettre les informations importantes sur la ressource au compilateur HLSL.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-116">Shader Model 5 (SM5.0) resource syntax uses the `register` keyword to relay important information about the resource to the HLSL compiler.</span></span> <span data-ttu-id="fcc6e-117">Par exemple, l’instruction suivante déclare un tableau de quatre textures liées aux emplacements T3, T4, T5 et T6.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-117">For example, the following statement declares an array of four textures bound at slots t3, t4, t5, and t6.</span></span> <span data-ttu-id="fcc6e-118">T3 est le seul emplacement de Registre qui s’affiche dans l’instruction, qui est simplement le premier dans le tableau de quatre.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-118">t3 is the only register slot appearing in the statement, simply being the first in the array of four.</span></span>

``` syntax
Texture2D<float4> tex1[4] : register(t3)
```

<span data-ttu-id="fcc6e-119">La syntaxe de ressource du Shader Model 5,1 (SM 5.1) en langage HLSL est basée sur la syntaxe de ressource de Registre existante, pour faciliter le portage.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-119">Shader Model 5.1 (SM5.1) resource syntax in HLSL is based on existing register resource syntax, to allow easier porting.</span></span> <span data-ttu-id="fcc6e-120">Les ressources Direct3D 12 en HLSL sont liées à des registres virtuels au sein d’espaces de registres logiques :</span><span class="sxs-lookup"><span data-stu-id="fcc6e-120">Direct3D 12 resources in HLSL are bound to virtual registers within logical register spaces:</span></span>

-   <span data-ttu-id="fcc6e-121">t – pour les vues des ressources de nuanceur (SRV)</span><span class="sxs-lookup"><span data-stu-id="fcc6e-121">t – for shader resource views (SRV)</span></span>
-   <span data-ttu-id="fcc6e-122">s : pour les échantillonneurs</span><span class="sxs-lookup"><span data-stu-id="fcc6e-122">s – for samplers</span></span>
-   <span data-ttu-id="fcc6e-123">u : pour les vues d’accès non ordonnées (UAV)</span><span class="sxs-lookup"><span data-stu-id="fcc6e-123">u – for unordered access views (UAV)</span></span>
-   <span data-ttu-id="fcc6e-124">b – pour les vues de mémoire tampon constantes (CBV)</span><span class="sxs-lookup"><span data-stu-id="fcc6e-124">b – for constant buffer views (CBV)</span></span>

<span data-ttu-id="fcc6e-125">La signature racine faisant référence au nuanceur doit être compatible avec les emplacements de Registre déclarés.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-125">The root signature referencing the shader must be compatible with the declared register slots.</span></span> <span data-ttu-id="fcc6e-126">Par exemple, la partie suivante d’une signature racine est compatible avec l’utilisation d’emplacements de texture T3 à T6, car elle décrit une table de descripteur avec les emplacements T0 à T98.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-126">For example, the following portion of a root signature would be compatible with the use of texture slots t3 through t6, as it describes a descriptor table with slots t0 through t98.</span></span>

``` syntax
DescriptorTable( CBV(b1), SRV(t0,numDescriptors=99), CBV(b2) )
```

<span data-ttu-id="fcc6e-127">Une déclaration de ressource peut être un scalaire, un tableau 1D ou un tableau multidimensionnel :</span><span class="sxs-lookup"><span data-stu-id="fcc6e-127">A resource declaration may be a scalar, a 1D array, or a multidimensional array:</span></span>

``` syntax
Texture2D<float4> tex1 : register(t3,  space0)
Texture2D<float4> tex2[4] : register(t10)
Texture2D<float4> tex3[7][5][3] : register(t20, space1)
```

<span data-ttu-id="fcc6e-128">SM 5.1 utilise les mêmes types de ressource et types d’éléments que le SM 5.0.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-128">SM5.1 uses the same resource types and element types as SM5.0 does.</span></span> <span data-ttu-id="fcc6e-129">Les limites de déclaration de SM 5.1 sont plus flexibles et limitées uniquement par les limites de Runtime/matériel.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-129">SM5.1 declaration limits are more flexible, and constrained only by the runtime/hardware limits.</span></span> <span data-ttu-id="fcc6e-130">Le `space` mot clé spécifie l’espace de Registre logique auquel la variable déclarée est liée.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-130">The `space` keyword specifies to which logical register space the declared variable is bound.</span></span> <span data-ttu-id="fcc6e-131">Si le `space` mot clé est omis, l’index d’espace par défaut 0 est implicitement affecté à la plage (la `tex2` plage ci-dessus réside dans `space0` ).</span><span class="sxs-lookup"><span data-stu-id="fcc6e-131">If the `space` keyword is omitted, then the default space index of 0 is implicitly assigned to the range (so the `tex2` range above resides in `space0`).</span></span> <span data-ttu-id="fcc6e-132">`register(t3,  space0)` n’est jamais en conflit avec `register(t3,  space1)` , ni avec un tableau dans un autre espace qui peut inclure T3.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-132">`register(t3,  space0)` will never conflict with `register(t3,  space1)`, nor with any array in another space that might include t3.</span></span>

<span data-ttu-id="fcc6e-133">Une ressource de tableau peut avoir une taille illimitée, qui est déclarée en spécifiant que la toute première dimension doit être vide, ou 0 :</span><span class="sxs-lookup"><span data-stu-id="fcc6e-133">An array resource may have an unbounded size, which is declared by specifying the very first dimension to be empty, or 0:</span></span>

``` syntax
Texture2D<float4> tex1[] : register(t0)
```

<span data-ttu-id="fcc6e-134">La table de descripteurs correspondante peut être :</span><span class="sxs-lookup"><span data-stu-id="fcc6e-134">The matching descriptor table could be:</span></span>

``` syntax
DescriptorTable( CBV(b1), UAV(u0, numDescriptors = 4), SRV(t0, numDescriptors=unbounded)
```

<span data-ttu-id="fcc6e-135">Un tableau non lié en HLSL ne correspond pas à un nombre fixe défini avec `numDescriptors` dans la table du descripteur, et une taille fixe dans le langage HLSL correspond à une déclaration non liée dans la table du descripteur.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-135">An unbounded array in HLSL does match a fixed number set with `numDescriptors` in the descriptor table, and a fixed size in the HLSL does match an unbounded declaration in the descriptor table.</span></span>

<span data-ttu-id="fcc6e-136">Les tableaux multidimensionnels sont autorisés, y compris une taille illimitée.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-136">Multi-dimensional arrays are allowed, including of an unbounded size.</span></span> <span data-ttu-id="fcc6e-137">Ces tableaux multidimensionnels sont aplatis dans l’espace de registre.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-137">These multidimensional arrays are flattened out in register space.</span></span>

``` syntax
Texture2D<float4> tex2[3000][10] : register(t0, space0); // t0-t29999 in space0
Texture2D<float4> tex3[0][5][3] : register(t5, space1)
```

<span data-ttu-id="fcc6e-138">L’alias des plages de ressources n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-138">Aliasing of resource ranges is not allowed.</span></span> <span data-ttu-id="fcc6e-139">En d’autres termes, pour chaque type de ressource (t, s, u, b), les plages de registres déclarées ne doit pas se chevauchent.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-139">In other words, for each resource type (t, s, u, b), declared register ranges mustn't overlap.</span></span> <span data-ttu-id="fcc6e-140">Cela comprend également les plages non liées.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-140">That includes unbounded ranges, too.</span></span> <span data-ttu-id="fcc6e-141">Les plages déclarées dans des espaces de registres différents ne se chevauchent jamais.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-141">Ranges declared in different register spaces never overlap.</span></span> <span data-ttu-id="fcc6e-142">Notez que le non lié `tex2` (ci-dessus) réside dans `space0` , tandis que le non lié `tex3` réside dans `space1` , de sorte qu’ils ne se chevauchent pas.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-142">Note that unbounded `tex2` (above) resides in `space0`, while unbounded `tex3` resides in `space1`, such that they don't overlap.</span></span>

<span data-ttu-id="fcc6e-143">L’accès aux ressources qui ont été déclarées en tant que tableaux est aussi simple que l’indexation.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-143">Accessing resources that have been declared as arrays is as simple as indexing them.</span></span>

``` syntax
Texture2D<float4> tex1[400] : register(t3);
sampler samp[7] : register(s0);
tex1[myMaterialID].Sample(samp[samplerID], texCoords);
```

<span data-ttu-id="fcc6e-144">Il existe une restriction par défaut importante sur l’utilisation des index ( `myMaterialID` et `samplerID` dans le code ci-dessus) en ce sens qu’ils ne sont pas autorisés à varier au sein d’une [vague](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology).</span><span class="sxs-lookup"><span data-stu-id="fcc6e-144">There's an important default restriction on the use of the indices (`myMaterialID` and `samplerID` in the code above) in that they're not allowed to vary within a [wave](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology).</span></span> <span data-ttu-id="fcc6e-145">Même la modification de l’index en fonction du nombre d’instanciations est variable.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-145">Even changing the index based on instancing counts as varying.</span></span>

<span data-ttu-id="fcc6e-146">Si vous devez faire varier l’index, spécifiez le `NonUniformResourceIndex` qualificateur sur l’index, par exemple :</span><span class="sxs-lookup"><span data-stu-id="fcc6e-146">If varying the index is required then specify the `NonUniformResourceIndex` qualifier on the index, for example:</span></span>

``` syntax
tex1[NonUniformResourceIndex(myMaterialID)].Sample(samp[NonUniformResourceIndex(samplerID)], texCoords);
```

<span data-ttu-id="fcc6e-147">Sur un matériel, l’utilisation de ce qualificateur génère du code supplémentaire pour assurer l’exactitude (y compris entre les threads), mais à un coût de performances mineur.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-147">On some hardware the use of this qualifier generates additional code to enforce correctness (including across threads) but at a minor performance cost.</span></span> <span data-ttu-id="fcc6e-148">Si un index est modifié sans ce qualificateur et dans un dessin/Dispatch, les résultats ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-148">If an index is changed without this qualifier and within a draw/dispatch the results are undefined.</span></span>

## <a name="descriptor-arrays-and-texture-arrays"></a><span data-ttu-id="fcc6e-149">Tableaux de descripteurs et tableaux de texture</span><span class="sxs-lookup"><span data-stu-id="fcc6e-149">Descriptor arrays and texture arrays</span></span>

<span data-ttu-id="fcc6e-150">Les tableaux de textures sont disponibles depuis DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-150">Texture arrays have been available since DirectX 10.</span></span> <span data-ttu-id="fcc6e-151">Les tableaux de textures requièrent un descripteur, mais tous les secteurs de tableau doivent partager les mêmes format, largeur, hauteur et compte MIP.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-151">Texture arrays require one descriptor, however all the array slices must share the same format, width, height and mip count.</span></span> <span data-ttu-id="fcc6e-152">En outre, le tableau doit occuper une plage contiguë dans l’espace d’adressage virtuel.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-152">Also, the array must occupy a contiguous range in virtual address space.</span></span> <span data-ttu-id="fcc6e-153">Le code suivant montre un exemple d’accès à un tableau de texture à partir d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-153">The following code shows an example of accessing a texture array from a shader.</span></span>

``` syntax
float3 myCoord(1.0f,1.4f,2.2f); // 2.2f is array index (rounded to int)
color = myTex2DArray.Sample(mySampler, myCoord);
```

<span data-ttu-id="fcc6e-154">Dans un tableau de textures, l’index peut être librement modifié, sans nécessiter de qualificateurs tels que `NonUniformResourceIndex` .</span><span class="sxs-lookup"><span data-stu-id="fcc6e-154">In a texture array, the index can be varied freely, without any need for qualifiers such as `NonUniformResourceIndex`.</span></span>

<span data-ttu-id="fcc6e-155">Le tableau de descripteurs équivalent serait :</span><span class="sxs-lookup"><span data-stu-id="fcc6e-155">The equivalent descriptor array would be:</span></span>

``` syntax
Texture2D<float4> myTex2DArray[] : register(t0); // t0+
float2 myCoord(1.0f, 1.4f);
color = myTex2D[2].Sample(mySampler,myCoord); // 2 is index
```

<span data-ttu-id="fcc6e-156">Remarque l’utilisation maladroite d’un float pour l’index de tableau est remplacée par `myTex2D[2]` .</span><span class="sxs-lookup"><span data-stu-id="fcc6e-156">Note the awkward use of a float for the array index is replaced with `myTex2D[2]`.</span></span> <span data-ttu-id="fcc6e-157">En outre, les tableaux de descripteurs offrent davantage de flexibilité avec les dimensions.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-157">Also descriptor arrays offer more flexibility with the dimensions.</span></span> <span data-ttu-id="fcc6e-158">Le type `Texture2D` est cet exemple, ne peut pas varier, mais le format, la largeur, la hauteur et le nombre MIP peuvent varier avec chaque descripteur.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-158">The type, `Texture2D` is this example, cannot vary, but the format, width, height, and mip count can all vary with each descriptor.</span></span>

<span data-ttu-id="fcc6e-159">Il est légitime d’avoir un tableau de descripteurs de tableaux de textures :</span><span class="sxs-lookup"><span data-stu-id="fcc6e-159">It is legitimate to have a descriptor array of texture arrays:</span></span>

``` syntax
Texture2DArray<float4> myTex2DArrayOfArrays[2] : register(t0);
```

<span data-ttu-id="fcc6e-160">Il n’est pas possible de déclarer un tableau de structures, chaque structure contenant des descripteurs, par exemple le code suivant n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-160">It is not legitimate to declare an array of structures, each structure containing descriptors, for example the following code is not supported.</span></span>

``` syntax
struct myStruct {
    Texture2D                    a; 
    Texture2D                    b;
    ConstantBuffer<myConstants>  c;
};
myStruct foo[10000] : register(....);
```

<span data-ttu-id="fcc6e-161">Cela aurait permis d’autoriser la disposition de la mémoire **abcabcabc.**..., mais il s’agit d’une limitation de langage et n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-161">This would have allowed the memory layout **abcabcabc....**, but is a language limitation and is not supported.</span></span> <span data-ttu-id="fcc6e-162">L’une des méthodes prises en charge est la suivante, bien que la disposition de la mémoire dans ce cas soit **AAA... BBB... CCC...**.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-162">One supported method of doing this would be as follows, though the memory layout in this case is **aaa...bbb...ccc...**.</span></span>

``` syntax
Texture2D                     a[10000] : register(t0);
Texture2D                     b[10000] : register(t10000);
ConstantBuffer<myConstants>   c[10000] : register(b0);
```

<span data-ttu-id="fcc6e-163">Pour obtenir la disposition **abcabcabc....** Memory, utilisez une table de descripteur sans utiliser la `myStruct` structure.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-163">To achieve the **abcabcabc....** memory layout, use a descriptor table without use of the `myStruct` structure.</span></span>

## <a name="resource-aliasing"></a><span data-ttu-id="fcc6e-164">Alias des ressources</span><span class="sxs-lookup"><span data-stu-id="fcc6e-164">Resource aliasing</span></span>

<span data-ttu-id="fcc6e-165">Les plages de ressources spécifiées dans les nuanceurs HLSL sont des plages logiques.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-165">The resource ranges specified in the HLSL shaders are logical ranges.</span></span> <span data-ttu-id="fcc6e-166">Elles sont liées à des plages de tas concrètes au moment de l’exécution via le mécanisme de signature racine.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-166">They are be bound to concrete heap ranges at runtime via the root signature mechanism.</span></span> <span data-ttu-id="fcc6e-167">Normalement, une plage logique est mappée à une plage de tas qui ne se chevauche pas avec d’autres plages de tas.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-167">Normally, a logical range maps to a heap range that does not overlap with other heap ranges.</span></span> <span data-ttu-id="fcc6e-168">Toutefois, le mécanisme de signature racine permet d’effectuer un alias (chevauchement) des plages de tas de types compatibles.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-168">However, the root signature mechanism makes it possible to alias (overlap) heap ranges of compatible types.</span></span> <span data-ttu-id="fcc6e-169">Par exemple, `tex2` les `tex3` plages de l’exemple ci-dessus peuvent être mappées à la même plage de tas (ou chevauchement), ce qui a pour effet d’affecter des textures à des textures dans le programme HLSL.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-169">For example, `tex2` and `tex3` ranges from the above example may be mapped to the same (or overlapping) heap range, which has the effect of aliasing textures in the HLSL program.</span></span> <span data-ttu-id="fcc6e-170">Si de tels alias sont souhaités, le nuanceur doit être compilé avec les \_ ressources de nuanceur D3D10 peuvent être définies à l' \_ \_ \_ aide de l’option d' *\_ \_ alias/res peut* être définie pour l' [outil Effect-compiler Tool](/windows/desktop/direct3dtools/fxc) (fxc).</span><span class="sxs-lookup"><span data-stu-id="fcc6e-170">If such aliasing is desired, the shader must be compiled with D3D10\_SHADER\_RESOURCES\_MAY\_ALIAS option, which is set by using the */res\_may\_alias* option for the [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC).</span></span> <span data-ttu-id="fcc6e-171">L’option permet au compilateur de générer un code correct en empêchant certaines optimisations de charge/stockage en supposant que les ressources peuvent créer un alias.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-171">The option makes the compiler produce correct code by preventing certain load/store optimizations under the assumption that resources may alias.</span></span>

## <a name="divergence-and-derivatives"></a><span data-ttu-id="fcc6e-172">Divergence et dérivées</span><span class="sxs-lookup"><span data-stu-id="fcc6e-172">Divergence and derivatives</span></span>

<span data-ttu-id="fcc6e-173">Le SM 5.1 n’impose pas de limitations sur l’index de ressource ; c’est-à-dire ` tex2[idx].Sample(…)` : l’index idx peut être une constante littérale, une constante CBuffer ou une valeur interpolée.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-173">SM5.1 does not impose limitations on the resource index; i.e.,` tex2[idx].Sample(…)` – the index idx can be a literal constant, a cbuffer constant, or an interpolated value.</span></span> <span data-ttu-id="fcc6e-174">Bien que le modèle de programmation offre une telle flexibilité exceptionnelle, il existe des problèmes à connaître :</span><span class="sxs-lookup"><span data-stu-id="fcc6e-174">While the programming model provides such great flexibility, there are issues to be aware of:</span></span>

-   <span data-ttu-id="fcc6e-175">Si l’index est divergent sur un quadruple, les dérivés calculés sur le matériel et les quantités dérivées telles que LOD peuvent ne pas être définies.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-175">If index diverges across a quad, the hardware-computed derivative and derived quantities such as LOD may be undefined.</span></span> <span data-ttu-id="fcc6e-176">Le compilateur HLSL fait le meilleur effort pour émettre un avertissement dans ce cas, mais n’empêchera pas la compilation d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-176">The HLSL compiler makes the best effort to issue a warning in this case, but will not prevent a shader from compiling.</span></span> <span data-ttu-id="fcc6e-177">Ce comportement est similaire à celui des dérivés de calcul dans un workflow de contrôle divergent.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-177">This behavior is similar to computing derivatives in divergent control flow.</span></span>
-   <span data-ttu-id="fcc6e-178">Si l’index de ressource est divergent, les performances sont réduites par rapport à la casse d’un index uniforme, car le matériel doit effectuer des opérations sur plusieurs ressources.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-178">If the resource index is divergent, the performance is diminished compared to the case of a uniform index, because the hardware needs to perform operations on several resources.</span></span> <span data-ttu-id="fcc6e-179">Les index de ressources qui peuvent être divergents doivent être marqués avec la `NonUniformResourceIndex` fonction en code HLSL.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-179">Resource indexes that may be divergent must be marked with the `NonUniformResourceIndex` function in HLSL code.</span></span> <span data-ttu-id="fcc6e-180">Sinon, les résultats ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-180">Otherwise results are undefined.</span></span>

## <a name="uavs-in-pixel-shaders"></a><span data-ttu-id="fcc6e-181">UAVs dans les nuanceurs de pixels</span><span class="sxs-lookup"><span data-stu-id="fcc6e-181">UAVs in pixel shaders</span></span>

<span data-ttu-id="fcc6e-182">Le SM 5.1 n’impose pas de contraintes sur les plages de UAV dans les nuanceurs de pixels comme c’était le cas pour le SM 5.0.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-182">SM5.1 does not impose constraints on UAV ranges in pixel shaders as was the case for SM5.0.</span></span>

## <a name="constant-buffers"></a><span data-ttu-id="fcc6e-183">Mémoires tampons constantes</span><span class="sxs-lookup"><span data-stu-id="fcc6e-183">Constant Buffers</span></span>

<span data-ttu-id="fcc6e-184">La syntaxe des tampons constantes du SM 5.1 (CBuffer) est passée de SM 5.0 pour permettre aux développeurs d’indexer des mémoires tampons constantes.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-184">SM5.1 constant buffers (cbuffer) syntax has changed from SM5.0 to enable developers to index constant buffers.</span></span> <span data-ttu-id="fcc6e-185">Pour activer les mémoires tampons constantes indexables, le SM 5.1 introduit la `ConstantBuffer` construction « modèle » :</span><span class="sxs-lookup"><span data-stu-id="fcc6e-185">To enable indexable constant buffers, SM5.1 introduces the `ConstantBuffer` “template” construct:</span></span>

``` syntax
struct Foo
{
    float4 a;
    int2 b;
};
ConstantBuffer<Foo> myCB1[2][3] : register(b2, space1);
ConstantBuffer<Foo> myCB2 : register(b0, space1);
```

<span data-ttu-id="fcc6e-186">Le code précédent déclare une variable de mémoire tampon constante `myCB1` de type `Foo` et de taille 6, ainsi qu’une variable de mémoire tampon constante scalaire `myCB2` .</span><span class="sxs-lookup"><span data-stu-id="fcc6e-186">The preceding code declares constant buffer variable `myCB1` of type `Foo` and size 6, and a scalar, constant buffer variable `myCB2`.</span></span> <span data-ttu-id="fcc6e-187">Une variable de mémoire tampon constante peut maintenant être indexée dans le nuanceur en tant que :</span><span class="sxs-lookup"><span data-stu-id="fcc6e-187">A constant buffer variable can now be indexed in the shader as:</span></span>

``` syntax
myCB1[i][j].a.xyzw
myCB2.b.yy
```

<span data-ttu-id="fcc6e-188">Les champs « a » et « b » ne deviennent pas des variables globales, mais doivent plutôt être traités comme des champs.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-188">Fields ‘a’ and ‘b’ do not become global variables, but rather must be treated as fields.</span></span> <span data-ttu-id="fcc6e-189">Pour la compatibilité descendante, SM 5.1 prend en charge l’ancien concept CBuffer pour Scala cbuffers.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-189">For backward compatibility, SM5.1 supports the old cbuffer concept for scalar cbuffers.</span></span> <span data-ttu-id="fcc6e-190">L’instruction suivante fait des variables globales « a » et « b », en lecture seule, comme dans SM 5.0.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-190">The following statement makes ‘a’ and ‘b’ global, read-only variables as in SM5.0.</span></span> <span data-ttu-id="fcc6e-191">Toutefois, un CBuffer de style ancien ne peut pas être indexé.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-191">However, such an old-style cbuffer cannot be indexable.</span></span>

``` syntax
cbuffer : register(b1)
{
    float4 a;
    int2 b;
};
```

<span data-ttu-id="fcc6e-192">Actuellement, le compilateur du nuanceur prend en charge le `ConstantBuffer` modèle uniquement pour les structures définies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-192">Currently, the shader compiler supports the `ConstantBuffer` template for user-defined structures only.</span></span>

<span data-ttu-id="fcc6e-193">Pour des raisons de compatibilité, le compilateur HLSL peut affecter automatiquement des registres de ressources pour les plages déclarées dans `space0` .</span><span class="sxs-lookup"><span data-stu-id="fcc6e-193">For compatibility reasons, the HLSL compiler may automatically assign resource registers for ranges declared in `space0`.</span></span> <span data-ttu-id="fcc6e-194">Si « Space » est omis dans la clause Register, la valeur par défaut `space0` est utilisée.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-194">If ‘space’ is omitted in the register clause, the default `space0` is used.</span></span> <span data-ttu-id="fcc6e-195">Le compilateur utilise l’heuristique « First-Hole » pour assigner les registres.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-195">The compiler uses the first-hole-fits heuristic to assign the registers.</span></span> <span data-ttu-id="fcc6e-196">L’attribution peut être récupérée par le biais de l’API de réflexion, qui a été étendue pour ajouter le champ *espace* pour l’espace, tandis que le champ *BindPoint* indique la limite inférieure de la plage du registre des ressources.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-196">The assignment can be retrieved via the reflection API, which has been extended to add the *Space* field for space, while the *BindPoint* field indicates the lower bound of the resource register range.</span></span>

## <a name="bytecode-changes-in-sm51"></a><span data-ttu-id="fcc6e-197">Changements de bytecode dans SM 5.1</span><span class="sxs-lookup"><span data-stu-id="fcc6e-197">Bytecode changes in SM5.1</span></span>

<span data-ttu-id="fcc6e-198">SM 5.1 change la façon dont les registres de ressources sont déclarés et référencés dans les instructions.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-198">SM5.1 changes how resource registers are declared and referenced in instructions.</span></span> <span data-ttu-id="fcc6e-199">La syntaxe implique la déclaration d’un registre « variable », de la même façon que pour les registres de mémoire partagée de groupe :</span><span class="sxs-lookup"><span data-stu-id="fcc6e-199">The syntax involves declaring a register “variable”, similar to how it is done for group shared memory registers:</span></span>

``` syntax
Texture2D<float4> tex0          : register(t5,  space0);
Texture2D<float4> tex1[][5][3]  : register(t10, space0);
Texture2D<float4> tex2[8]       : register(t0,  space1);
SamplerState samp0              : register(s5, space0);

float4 main(float4 coord : COORD) : SV_TARGET
{
    float4 r = coord;
    r += tex0.Sample(samp0, r.xy);
    r += tex2[r.x].Sample(samp0, r.xy);
    r += tex1[r.x][r.y][r.z].Sample(samp0, r.xy);
    return r;
}
```

<span data-ttu-id="fcc6e-200">Cela va désassembler :</span><span class="sxs-lookup"><span data-stu-id="fcc6e-200">This will disassemble to:</span></span>

``` syntax
// Resource Bindings:
//
// Name                                 Type  Format         Dim    ID   HLSL Bind     Count
// ------------------------------ ---------- ------- ----------- -----   --------- ---------
// samp0                             sampler      NA          NA     S0    a5            1
// tex0                              texture  float4          2d     T0    t5            1
// tex1[0][5][3]                     texture  float4          2d     T1   t10        unbounded
// tex2[8]                           texture  float4          2d     T2    t0.space1     8
//
//
//
// Input signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// COORD                    0   xyzw        0     NONE   float   xyzw
//
//
// Output signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// SV_TARGET                0   xyzw        0   TARGET   float   xyzw
//
ps_5_1
dcl_globalFlags refactoringAllowed
dcl_sampler s0[5:5], mode_default, space=0
dcl_resource_texture2d (float,float,float,float) t0[5:5], space=0
dcl_resource_texture2d (float,float,float,float) t1[10:*], space=0
dcl_resource_texture2d (float,float,float,float) t2[0:7], space=1
dcl_input_ps linear v0.xyzw
dcl_output o0.xyzw
dcl_temps 2
sample r0.xyzw, v0.xyxx, t0[0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, v0.xyzw
ftou r1.x, r0.x
sample r1.xyzw, r0.xyxx, t2[r1.x + 0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, r1.xyzw
ftou r1.xyz, r0.zyxz
imul null, r1.yz, r1.zzyz, l(0, 15, 3, 0)
iadd r1.y, r1.z, r1.y
iadd r1.x, r1.x, r1.y
sample r1.xyzw, r0.xyxx, t1[r1.x + 10].xyzw, s0[5]
add o0.xyzw, r0.xyzw, r1.xyzw
ret
// Approximately 12 instruction slots are used.
```

<span data-ttu-id="fcc6e-201">Chaque plage de ressources de nuanceur a maintenant un ID (un nom) qui est unique pour le bytecode du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-201">Each shader resource range now has an ID (a name) that is unique to the shader bytecode.</span></span> <span data-ttu-id="fcc6e-202">Par exemple, le tableau de texture Tex1 (T10) devient « t 1 » dans le bytecode du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-202">For example, tex1 (t10) texture array becomes ‘T1’ in the shader bytecode.</span></span> <span data-ttu-id="fcc6e-203">L’attribution d’ID uniques à chaque plage de ressources permet d’effectuer deux opérations :</span><span class="sxs-lookup"><span data-stu-id="fcc6e-203">Giving unique IDs to each resource range allows two things:</span></span>

-   <span data-ttu-id="fcc6e-204">Identifiez clairement la plage de ressources (voir la \_ ressource DCL \_ Texture2D) qui est indexée dans une instruction (voir exemple d’instruction).</span><span class="sxs-lookup"><span data-stu-id="fcc6e-204">Unambiguously identify which resource range (see dcl\_resource\_texture2d) is being indexed in an instruction (see sample instruction).</span></span>
-   <span data-ttu-id="fcc6e-205">Attachement d’un ensemble d’attributs à la déclaration, par exemple, type d’élément, taille de numérisation, mode de fonctionnement raster, etc.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-205">Attaching a set of attributes to the declaration, e.g., element type, stride size, raster operation mode, etc.</span></span>

<span data-ttu-id="fcc6e-206">Notez que l’ID de la plage n’est pas associé à la déclaration de la limite inférieure HLSL.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-206">Note that the ID of the range is not related to the HLSL lower bound declaration.</span></span>

<span data-ttu-id="fcc6e-207">L’ordre des liaisons de ressources de réflexion (répertoriées en haut) et les instructions de déclaration de nuanceur (DCL \_ \* ) sont les mêmes pour faciliter l’identification de la correspondance entre les variables HLSL et les ID de bytecode.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-207">The order of reflection resource bindings (listing at the top) and shader declaration instructions (dcl\_\*) is the same to aid in identifying the correspondence between HLSL variables and bytecode IDs.</span></span>

<span data-ttu-id="fcc6e-208">Chaque instruction de déclaration dans le SM 5.1 utilise un opérande 3D pour définir : ID de plage, limites inférieure et supérieure.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-208">Each declaration instruction in SM5.1 uses a 3D operand to define: range ID, lower and upper bounds.</span></span> <span data-ttu-id="fcc6e-209">Un jeton supplémentaire est émis pour spécifier l’espace de registre.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-209">An additional token is emitted to specify the register space.</span></span> <span data-ttu-id="fcc6e-210">D’autres jetons peuvent être émis pour transmettre des propriétés supplémentaires de la plage, par exemple, CBuffer ou une instruction de déclaration de mémoire tampon structurée émet la taille de la structure ou du CBuffer.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-210">Other tokens may be emitted as well to convey additional properties of the range, e.g., cbuffer or structured buffer declaration instruction emits the size of the cbuffer or structure.</span></span> <span data-ttu-id="fcc6e-211">Les détails exacts de l’encodage se trouvent dans d3d12TokenizedProgramFormat. h et **D3D10ShaderBinary :: CShaderCodeParser**.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-211">The exact details of encoding can be found in d3d12TokenizedProgramFormat.h and **D3D10ShaderBinary::CShaderCodeParser**.</span></span>

<span data-ttu-id="fcc6e-212">Les instructions du SM 5.1 n’émettent pas d’informations d’opérande de ressource supplémentaires dans le cadre de l’instruction (comme dans le SM 5.0).</span><span class="sxs-lookup"><span data-stu-id="fcc6e-212">SM5.1 instructions will not emit additional resource operand information as part of the instruction (as in SM5.0).</span></span> <span data-ttu-id="fcc6e-213">Ces informations se trouvent maintenant dans les instructions de déclaration.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-213">This information is now in the declaration instructions.</span></span> <span data-ttu-id="fcc6e-214">Dans SM 5.0, les instructions d’indexation des ressources nécessitant des attributs de ressource sont décrites dans les jetons d’opcode étendus, car l’indexation a obscurci l’Association à la déclaration.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-214">In SM5.0, instructions indexing resources required resource attributes to be described in extended opcode tokens, since indexing obfuscated the association to the declaration.</span></span> <span data-ttu-id="fcc6e-215">Dans le SM 5.1, chaque ID (par exemple, « t 1 ») est associé de manière non équivoque à une déclaration unique qui décrit les informations sur les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-215">In SM5.1, each ID (such as ‘t1’) is unambiguously associated with a single declaration that describes the required resource information.</span></span> <span data-ttu-id="fcc6e-216">Par conséquent, les jetons d’opcode étendus utilisés sur les instructions pour décrire les informations sur les ressources ne sont plus émis.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-216">Therefore, the extended opcode tokens used on instructions to describe resource information are no longer emitted.</span></span>

<span data-ttu-id="fcc6e-217">Dans les instructions de non-déclaration, un opérande de ressource pour les échantillonneurs, SRVs et UAVs est un opérande 2D.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-217">In non-declaration instructions, a resource operand for samplers, SRVs, and UAVs is a 2D operand.</span></span> <span data-ttu-id="fcc6e-218">Le premier index est une constante littérale qui spécifie l’ID de la plage.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-218">The first index is a literal constant that specifies the range ID.</span></span> <span data-ttu-id="fcc6e-219">Le deuxième index représente la valeur linéarisée de l’index.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-219">The second index represents the linearized value of the index.</span></span> <span data-ttu-id="fcc6e-220">La valeur est calculée par rapport au début de l’espace de Registre correspondant (et non par rapport au début de la plage logique) afin d’améliorer la corrélation avec la signature racine et réduire la charge de compilateur du pilote pour l’ajustement de l’index.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-220">The value is computed relative to the beginning of the corresponding register space (not relative to the beginning of the logical range) to better correlate with the root signature and to reduce the driver compiler burden of adjusting the index.</span></span>

<span data-ttu-id="fcc6e-221">Un opérande de ressource pour CBVs est un opérande 3D, contenant : ID littéral de la plage, index de la mémoire tampon constante, décalage dans l’instance particulière de la mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-221">A resource operand for CBVs is a 3D operand, containing: literal ID of the range, index of the constant buffer, offset into the particular instance of constant buffer.</span></span>

## <a name="example-hlsl-declarations"></a><span data-ttu-id="fcc6e-222">Exemples de déclarations HLSL</span><span class="sxs-lookup"><span data-stu-id="fcc6e-222">Example HLSL Declarations</span></span>

<span data-ttu-id="fcc6e-223">Les programmes HLSL n’ont pas besoin de savoir quoi que ce soit sur les signatures racines.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-223">HLSL programs do not need to know anything about root signatures.</span></span> <span data-ttu-id="fcc6e-224">Ils peuvent assigner des liaisons à l’espace de liaison « Register » virtuel, t \# pour SRVs, u \# pour UAVs, b \# pour CBVS, s \# pour les échantillonneurs, ou s’appuyer sur le compilateur pour sélectionner des assignations (et interroger les mappages résultants à l’aide de la réflexion du nuanceur par la suite).</span><span class="sxs-lookup"><span data-stu-id="fcc6e-224">They can assign bindings to the virtual “register” binding space, t\# for SRVs, u\# for UAVs, b\# for CBVs, s\# for samplers, or rely on the compiler to pick assignments (and query the resulting mappings using shader reflection afterwards).</span></span> <span data-ttu-id="fcc6e-225">La signature racine mappe les tables de descripteurs, les descripteurs racines et les constantes racine à cet espace de Registre virtuel.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-225">The root signature maps descriptor tables, root descriptors, and root constants to this virtual register space.</span></span>

<span data-ttu-id="fcc6e-226">Voici quelques exemples de déclarations qu’un nuanceur HLSL peut avoir.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-226">The following are some example declarations an HLSL shader might have.</span></span> <span data-ttu-id="fcc6e-227">Notez qu’il n’existe aucune référence aux signatures racines ou aux tables de descripteurs.</span><span class="sxs-lookup"><span data-stu-id="fcc6e-227">Note that there are no references to root signatures or descriptor tables.</span></span>

``` syntax
Texture2D foo[5] : register(t2);
Buffer bar : register(t7);
RWBuffer dataLog : register(u1);

Sampler samp : register(s0);

struct Data
{
    UINT index;
    float4 color;
};
ConstantBuffer<Data> myData : register(b0);

Texture2D terrain[] : register(t8); // Unbounded array
Texture2D misc[] : register(t0,space1); // Another unbounded array 
                                        // space1 avoids overlap with above t#

struct MoreData
{
    float4x4 xform;
};
ConstantBuffer<MoreData> myMoreData : register(b1);

struct Stuff
{
    float2 factor;
    UINT drawID;
};
ConstantBuffer<Stuff> myStuff[][3][8]  : register(b2, space3)
```

## <a name="related-topics"></a><span data-ttu-id="fcc6e-228">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fcc6e-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcc6e-229">Indexation dynamique à l’aide de HLSL 5.1</span><span class="sxs-lookup"><span data-stu-id="fcc6e-229">Dynamic Indexing using HLSL 5.1</span></span>](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[<span data-ttu-id="fcc6e-230">Effect-Tool du compilateur</span><span class="sxs-lookup"><span data-stu-id="fcc6e-230">Effect-Compiler Tool</span></span>](/windows/desktop/direct3dtools/fxc)
</dt> <dt>

[<span data-ttu-id="fcc6e-231">Caractéristiques du modèle de nuanceur HLSL 5,1 pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="fcc6e-231">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[<span data-ttu-id="fcc6e-232">Affichages ordonnés du rastériseur</span><span class="sxs-lookup"><span data-stu-id="fcc6e-232">Rasterizer Ordered Views</span></span>](rasterizer-order-views.md)
</dt> <dt>

[<span data-ttu-id="fcc6e-233">Liaison de ressource</span><span class="sxs-lookup"><span data-stu-id="fcc6e-233">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="fcc6e-234">Signatures racines</span><span class="sxs-lookup"><span data-stu-id="fcc6e-234">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="fcc6e-235">Modèle de nuanceur 5,1</span><span class="sxs-lookup"><span data-stu-id="fcc6e-235">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="fcc6e-236">Valeur de référence du stencil spécifié par le nuanceur</span><span class="sxs-lookup"><span data-stu-id="fcc6e-236">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)
</dt> <dt>

[<span data-ttu-id="fcc6e-237">Spécification de signatures racines en langage HLSL</span><span class="sxs-lookup"><span data-stu-id="fcc6e-237">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 