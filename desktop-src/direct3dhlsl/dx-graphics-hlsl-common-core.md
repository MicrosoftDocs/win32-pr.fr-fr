---
title: Common-Shader Core
description: Common-Shader Core
ms.assetid: f3cf2969-83a4-461f-8177-d336536194ba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 66c1f763c4771a8406acd2f3401445d1a29cde79
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129716"
---
# <a name="common-shader-core"></a><span data-ttu-id="09826-103">Common-Shader Core</span><span class="sxs-lookup"><span data-stu-id="09826-103">Common-Shader Core</span></span>

<span data-ttu-id="09826-104">Dans le nuanceur modèle 4, toutes les étapes de nuanceur implémentent les mêmes fonctionnalités de base à l’aide d’un noyau de nuanceur commun.</span><span class="sxs-lookup"><span data-stu-id="09826-104">In Shader Model 4, all shader stages implement the same base functionality using a common-shader core.</span></span> <span data-ttu-id="09826-105">En outre, chacune des trois étapes de nuanceur (vertex, Geometry et pixel) offre des fonctionnalités uniques à chaque étape, telles que la possibilité de générer de nouvelles primitives à partir de l’étape de nuanceur Geometry ou d’ignorer un pixel spécifique dans l’étape de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="09826-105">In addition, each of the three shader stages (vertex, geometry, and pixel) offer functionality unique to each stage, such as the ability to generate new primitives from the geometry shader stage or to discard a specific pixel in the pixel shader stage.</span></span> <span data-ttu-id="09826-106">Le diagramme suivant illustre la façon dont les données circulent dans une étape de nuanceur, ainsi que la relation entre le noyau-nuanceur commun et les ressources de mémoire du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="09826-106">The following diagram shows how data flows through a shader stage, and the relationship of the common-shader core with shader memory resources.</span></span>

![diagramme du workflow de données dans une étape de nuanceur](images/d3d10-shader-unit.png)

-   <span data-ttu-id="09826-108">**Données d’entrée**: un nuanceur de sommets reçoit ses entrées de l’étape assembleur d’entrée ; les nuanceurs de géométrie et de pixels reçoivent leurs entrées de l’étape de nuanceur précédente.</span><span class="sxs-lookup"><span data-stu-id="09826-108">**Input Data**: A vertex shader receives its inputs from the input assembler stage; geometry and pixel shaders receive their inputs from the previous shader stage.</span></span> <span data-ttu-id="09826-109">Les entrées supplémentaires incluent la [sémantique de valeur système](dx-graphics-hlsl-semantics.md), qui sont consommables par la première unité dans le pipeline auquel elles s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="09826-109">Additional inputs include [system-value semantics](dx-graphics-hlsl-semantics.md), which are consumable by the first unit in the pipeline to which they are applicable.</span></span>
-   <span data-ttu-id="09826-110">**Données de sortie**: les nuanceurs génèrent des résultats de sortie à passer à l’étape suivante dans le pipeline.</span><span class="sxs-lookup"><span data-stu-id="09826-110">**Output Data**: Shaders generate output results to be passed onto the subsequent stage in the pipeline.</span></span> <span data-ttu-id="09826-111">Pour un nuanceur Geometry, la quantité de données générées par un appel unique peut varier.</span><span class="sxs-lookup"><span data-stu-id="09826-111">For a geometry shader, the amount of data output from a single invocation can vary.</span></span> <span data-ttu-id="09826-112">Certaines sorties sont interprétées par le Common-Shader Core (par exemple, position de vertex et index de tableau de cibles de rendu), d’autres sont conçues pour être interprétées par une application.</span><span class="sxs-lookup"><span data-stu-id="09826-112">Some outputs are interpreted by the common-shader core (such as vertex position and render-target-array index), others are designed to be interpreted by an application.</span></span>
-   <span data-ttu-id="09826-113">**Code du nuanceur**: les nuanceurs peuvent lire à partir de la mémoire, effectuer des opérations arithmétiques de vecteurs et d’entiers, ou effectuer des opérations de contrôle de Workflow.</span><span class="sxs-lookup"><span data-stu-id="09826-113">**Shader Code**: Shaders can read from memory, perform vector floating point and integer arithmetic operations, or flow control operations.</span></span> <span data-ttu-id="09826-114">Il n’existe aucune limite quant au nombre d’instructions qui peuvent être implémentées dans un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="09826-114">There is no limit to the number of statements that can be implemented in a shader.</span></span>
-   <span data-ttu-id="09826-115">**Échantillonneurs**: les échantillonneurs définissent comment échantillonner et filtrer les textures.</span><span class="sxs-lookup"><span data-stu-id="09826-115">**Samplers**: Samplers define how to sample and filter textures.</span></span> <span data-ttu-id="09826-116">Jusqu’à 16 échantillons peuvent être liés simultanément à un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="09826-116">As many as 16 samplers can be bound to a shader simultaneously.</span></span>
-   <span data-ttu-id="09826-117">**Textures**: les textures peuvent être filtrées à l’aide d’échantillonneurs ou lues sur une base par Texel directement avec la fonction intrinsèque [Load](dx-graphics-hlsl-to-load.md) .</span><span class="sxs-lookup"><span data-stu-id="09826-117">**Textures**: Textures can be filtered using samplers or read on a per-texel basis directly with the [load](dx-graphics-hlsl-to-load.md) intrinsic function.</span></span>
-   <span data-ttu-id="09826-118">**Mémoires tampons**: les mémoires tampons ne sont jamais filtrées, mais peuvent être lues à partir de la mémoire à chaque élément directement avec la fonction intrinsèque [Load](dx-graphics-hlsl-to-load.md) .</span><span class="sxs-lookup"><span data-stu-id="09826-118">**Buffers**: Buffers are never filtered, but can be read from memory on a per-element basis directly with the [load](dx-graphics-hlsl-to-load.md) intrinsic function.</span></span> <span data-ttu-id="09826-119">Jusqu’à 128 de ressources de texture et de mémoire tampon (combinées) peuvent être liées simultanément à un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="09826-119">As many as 128 texture and buffer resources (combined) can be bound to a shader simultaneously.</span></span>
-   <span data-ttu-id="09826-120">**Mémoires tampons constantes**: les mémoires tampons constantes sont optimisées pour les variables constantes de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="09826-120">**Constant Buffers**: Constant buffers are optimized for shader constant-variables.</span></span> <span data-ttu-id="09826-121">Jusqu’à 16 mémoires tampons constantes peuvent être liées simultanément à une étape de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="09826-121">As many as 16 constant buffers can be bound to a shader stage simultaneously.</span></span> <span data-ttu-id="09826-122">Elles sont conçues pour des mises à jour plus fréquentes à partir de l’UC. par conséquent, elles ont des restrictions de taille, de mise en page et d’accès supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="09826-122">They are designed for more frequent update from the CPU; therefore, they have additional size, layout, and access restrictions.</span></span>


<span data-ttu-id="09826-123">Différences entre Direct3D 9 et Direct3D 10 :</span><span class="sxs-lookup"><span data-stu-id="09826-123">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="09826-124">Dans Direct3D 9, chaque unité de nuanceur avait un seul fichier de registre de constantes de petite taille pour stocker toutes les variables de nuanceur constantes.</span><span class="sxs-lookup"><span data-stu-id="09826-124">In Direct3D 9, each shader unit had a single, small constant register file to store all constant shader variables.</span></span> <span data-ttu-id="09826-125">L’utilisation de tous les nuanceurs avec cet espace constant limité nécessitait un recyclage fréquent des constantes par le processeur.</span><span class="sxs-lookup"><span data-stu-id="09826-125">Accommodating all shaders with this limited constant space required frequent recycling of constants by the CPU.</span></span>
- <span data-ttu-id="09826-126">Dans Direct3D 10, les constantes sont stockées dans des mémoires tampons immuables en mémoire et sont gérées comme n’importe quelle autre ressource.</span><span class="sxs-lookup"><span data-stu-id="09826-126">In Direct3D 10, constants are stored in immutable buffers in memory and are managed like any other resource.</span></span> <span data-ttu-id="09826-127">Il n’existe pas de limite au nombre de mémoires tampons constantes qu’une application peut créer.</span><span class="sxs-lookup"><span data-stu-id="09826-127">There is no limit to the number of constant buffers an application can create.</span></span> <span data-ttu-id="09826-128">En organisant des constantes dans des mémoires tampons en fonction de la fréquence des mises à jour et de l’utilisation, la quantité de bande passante requise pour mettre à jour les constantes pour prendre en charge tous les nuanceurs peut être considérablement réduite.</span><span class="sxs-lookup"><span data-stu-id="09826-128">By organizing constants into buffers by frequency of update and usage, the amount of bandwidth required to update constants to accommodate all shaders can be significantly reduced.</span></span>



 

## <a name="integer-and-bitwise-support"></a><span data-ttu-id="09826-129">Prise en charge des bits et des entiers</span><span class="sxs-lookup"><span data-stu-id="09826-129">Integer and Bitwise Support</span></span>

<span data-ttu-id="09826-130">Le Common Shader Core fournit un ensemble complet d’opérations au niveau du bit et d’entier 32 bits conformes à IEEE.</span><span class="sxs-lookup"><span data-stu-id="09826-130">The common shader core provides a full set of IEEE-compliant 32-bit integer and bitwise operations.</span></span> <span data-ttu-id="09826-131">Ces opérations activent une nouvelle classe d’algorithmes dans des exemples de matériel graphique, notamment des techniques de compression et d’empaquetage, FFTs et un contrôle de déroulement de programme de champ de bits.</span><span class="sxs-lookup"><span data-stu-id="09826-131">These operations enable a new class of algorithms in graphics hardware examples include compression and packing techniques, FFTs, and bitfield program-flow control.</span></span>

<span data-ttu-id="09826-132">Les types de données **int** et **uint** dans Direct3D 10 HLSL sont mappés à des entiers 32 bits dans le matériel.</span><span class="sxs-lookup"><span data-stu-id="09826-132">The **int** and **uint** data types in Direct3D 10 HLSL map to 32-bit integers in hardware.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09826-133">Différences entre Direct3D 9 et Direct3D 10 :</span><span class="sxs-lookup"><span data-stu-id="09826-133">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="09826-134">Dans Direct3D 9, les entrées marquées comme étant des entiers en HLSL étaient interprétées comme étant à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="09826-134">In Direct3D 9 stream inputs marked as integer in HLSL were interpreted as floating-point.</span></span> <span data-ttu-id="09826-135">Dans Direct3D 10, les entrées de flux marquées comme Integer sont interprétées comme un entier 32 bits.</span><span class="sxs-lookup"><span data-stu-id="09826-135">In Direct3D 10, stream inputs marked as integer are interpreted as a 32- bit integer.</span></span><br/> <span data-ttu-id="09826-136">En outre, les valeurs booléennes sont maintenant tous les bits définis ou tous les bits non définis.</span><span class="sxs-lookup"><span data-stu-id="09826-136">In addition, boolean values are now all bits set or all bits unset.</span></span> <span data-ttu-id="09826-137">Les données converties en **bool** seront interprétées comme true si la valeur n’est pas égale à 0.0 f (les valeurs NULL positives et négatives sont autorisées à être false) et false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="09826-137">Data converted to **bool** will be interpreted as true if the value is not equal to 0.0f (both positive and negative zero are allowed to be false) and false otherwise.</span></span><br/> |



 

## <a name="bitwise-operators"></a><span data-ttu-id="09826-138">Opérateurs au niveau du bit</span><span class="sxs-lookup"><span data-stu-id="09826-138">Bitwise operators</span></span>

<span data-ttu-id="09826-139">Le Common Shader Core prend en charge les opérateurs de bits suivants :</span><span class="sxs-lookup"><span data-stu-id="09826-139">The common shader core supports the following bitwise operators:</span></span>



| <span data-ttu-id="09826-140">Opérateur</span><span class="sxs-lookup"><span data-stu-id="09826-140">Operator</span></span>  | <span data-ttu-id="09826-141">Fonction</span><span class="sxs-lookup"><span data-stu-id="09826-141">Function</span></span>          |
|-----------|-------------------|
| ~         | <span data-ttu-id="09826-142">Not logique</span><span class="sxs-lookup"><span data-stu-id="09826-142">Logical Not</span></span>       |
| <<  | <span data-ttu-id="09826-143">Décalage vers la gauche</span><span class="sxs-lookup"><span data-stu-id="09826-143">Left Shift</span></span>        |
| >>  | <span data-ttu-id="09826-144">Décalage vers la droite</span><span class="sxs-lookup"><span data-stu-id="09826-144">Right Shift</span></span>       |
| &         | <span data-ttu-id="09826-145">AND logique</span><span class="sxs-lookup"><span data-stu-id="09826-145">Logical And</span></span>       |
| \|        | <span data-ttu-id="09826-146">Or logique</span><span class="sxs-lookup"><span data-stu-id="09826-146">Logical Or</span></span>        |
| ^         | <span data-ttu-id="09826-147">XOR logique</span><span class="sxs-lookup"><span data-stu-id="09826-147">Logical Xor</span></span>       |
| <<= | <span data-ttu-id="09826-148">Décalage vers la gauche égal</span><span class="sxs-lookup"><span data-stu-id="09826-148">Left shift Equal</span></span>  |
| >>= | <span data-ttu-id="09826-149">Décalage vers la droite égal</span><span class="sxs-lookup"><span data-stu-id="09826-149">Right Shift Equal</span></span> |
| &=        | <span data-ttu-id="09826-150">Et égal à</span><span class="sxs-lookup"><span data-stu-id="09826-150">And Equal</span></span>         |
| \|=       | <span data-ttu-id="09826-151">Ou égal à</span><span class="sxs-lookup"><span data-stu-id="09826-151">Or Equal</span></span>          |
| ^=        | <span data-ttu-id="09826-152">XOR égal</span><span class="sxs-lookup"><span data-stu-id="09826-152">Xor Equal</span></span>         |



 

<span data-ttu-id="09826-153">Les opérateurs au niveau du bit sont définis pour fonctionner uniquement sur les types de données **int** et **uint** .</span><span class="sxs-lookup"><span data-stu-id="09826-153">Bitwise operators are defined to operate only on **int** and **uint** data types.</span></span> <span data-ttu-id="09826-154">Toute tentative d’utilisation d’opérateurs de bits sur des types de données **float** ou **struct** génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="09826-154">Attempting to use bitwise operators on **float** or **struct** data types will result in an error.</span></span> <span data-ttu-id="09826-155">Les opérateurs au niveau du bit suivent la même priorité que C en ce qui concerne les autres opérateurs.</span><span class="sxs-lookup"><span data-stu-id="09826-155">Bitwise operators follow the same precedence as C with regard to other operators.</span></span>

## <a name="binary-casts"></a><span data-ttu-id="09826-156">Casts binaires</span><span class="sxs-lookup"><span data-stu-id="09826-156">Binary Casts</span></span>

<span data-ttu-id="09826-157">Le cast entre un entier et un type à virgule flottante convertit la valeur numérique à la suite des règles de troncation C.</span><span class="sxs-lookup"><span data-stu-id="09826-157">Casting between an integer and a floating-point type will convert the numeric value following C truncation rules.</span></span> <span data-ttu-id="09826-158">Effectuer un cast d’une valeur d’un **float** vers un **int**, puis revenir à un **float** est une conversion avec perte dépendante de la précision du type de données cible.</span><span class="sxs-lookup"><span data-stu-id="09826-158">Casting a value from a **float**, to an **int**, and back to a **float** is a lossy conversion dependent on the precision of the target data type.</span></span> <span data-ttu-id="09826-159">Voici quelques-unes des fonctions de conversion : [**asfloat (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**ASINT (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).</span><span class="sxs-lookup"><span data-stu-id="09826-159">Here are some of the conversion functions: [**asfloat (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**asint (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).</span></span>

<span data-ttu-id="09826-160">Les casts binaires peuvent également être effectués à l’aide de fonctions intrinsèques HLSL.</span><span class="sxs-lookup"><span data-stu-id="09826-160">Binary casts can also be performed using HLSL intrinsic functions.</span></span> <span data-ttu-id="09826-161">En conséquence, le compilateur réinterprète la représentation sous forme de bit d’un nombre dans le type de données cible.</span><span class="sxs-lookup"><span data-stu-id="09826-161">These cause the compiler to reinterpret the bit representation of a number into the target data type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09826-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="09826-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09826-163">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="09826-163">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





