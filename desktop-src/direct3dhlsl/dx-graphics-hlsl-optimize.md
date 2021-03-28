---
title: Optimisation des nuanceurs HLSL
description: Cette section décrit les stratégies à usage général que vous pouvez utiliser pour optimiser vos nuanceurs. Vous pouvez appliquer ces stratégies aux nuanceurs écrits dans n’importe quel langage, sur n’importe quelle plateforme.
ms.assetid: 014b9cb3-a489-48d7-8174-b97de168bf3a
keywords:
- langage de nuanceur de haut niveau
- HLSL, performances
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06d3bb806e98e489020aa1755ef2a6c952459d86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029598"
---
# <a name="optimizing-hlsl-shaders"></a><span data-ttu-id="a5419-106">Optimisation des nuanceurs HLSL</span><span class="sxs-lookup"><span data-stu-id="a5419-106">Optimizing HLSL Shaders</span></span>

<span data-ttu-id="a5419-107">Cette section décrit les stratégies à usage général que vous pouvez utiliser pour optimiser vos nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="a5419-107">This section describes general-purpose strategies that you can use to optimize your shaders.</span></span> <span data-ttu-id="a5419-108">Vous pouvez appliquer ces stratégies aux nuanceurs écrits dans n’importe quel langage, sur n’importe quelle plateforme.</span><span class="sxs-lookup"><span data-stu-id="a5419-108">You can apply these strategies to shaders that are written in any language, on any platform.</span></span>

-   [<span data-ttu-id="a5419-109">Savoir où effectuer les calculs des nuanceurs</span><span class="sxs-lookup"><span data-stu-id="a5419-109">Know Where To Perform Shader Calculations</span></span>](#know-where-to-perform-shader-calculations)
-   [<span data-ttu-id="a5419-110">Ignorer les instructions inutiles</span><span class="sxs-lookup"><span data-stu-id="a5419-110">Skip Unnecessary Instructions</span></span>](#skip-unnecessary-instructions)
-   [<span data-ttu-id="a5419-111">Variables et interpolations de Pack</span><span class="sxs-lookup"><span data-stu-id="a5419-111">Pack Variables and Interpolants</span></span>](#pack-variables-and-interpolants)
-   [<span data-ttu-id="a5419-112">Réduire la complexité des nuanceurs</span><span class="sxs-lookup"><span data-stu-id="a5419-112">Reduce Shader Complexity</span></span>](#reduce-shader-complexity)
-   [<span data-ttu-id="a5419-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a5419-113">Related Topics</span></span>](#related-topics)
-   [<span data-ttu-id="a5419-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a5419-114">Related topics</span></span>](#related-topics)

## <a name="know-where-to-perform-shader-calculations"></a><span data-ttu-id="a5419-115">Savoir où effectuer les calculs des nuanceurs</span><span class="sxs-lookup"><span data-stu-id="a5419-115">Know Where To Perform Shader Calculations</span></span>

<span data-ttu-id="a5419-116">Les nuanceurs vertex effectuent des opérations qui incluent l’extraction des sommets et la transformation de matrice des données de vertex.</span><span class="sxs-lookup"><span data-stu-id="a5419-116">Vertex shaders perform operations that include fetching vertices and performing matrix transformation of vertex data.</span></span> <span data-ttu-id="a5419-117">En règle générale, les nuanceurs de vertex sont exécutés une fois par vertex.</span><span class="sxs-lookup"><span data-stu-id="a5419-117">Typically, vertex shaders are executed once per vertex.</span></span>

<span data-ttu-id="a5419-118">Les nuanceurs de pixels effectuent des opérations qui incluent l’extraction des données de texture et l’exécution de calculs d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="a5419-118">Pixel Shaders perform operations that include fetching texture data and performing lighting calculations.</span></span> <span data-ttu-id="a5419-119">En règle générale, les nuanceurs de pixels sont exécutés une fois par pixel pour un élément de géométrie donné.</span><span class="sxs-lookup"><span data-stu-id="a5419-119">Typically, pixel shaders are executed once per pixel for a given piece of geometry.</span></span>

<span data-ttu-id="a5419-120">En général, le nombre de pixels dans une scène, les nuanceurs de pixels s’exécutent plus souvent que les nuanceurs de vertex.</span><span class="sxs-lookup"><span data-stu-id="a5419-120">Typically, pixels outnumber vertices in a scene, so pixel shaders execute more often than vertex shaders.</span></span>

<span data-ttu-id="a5419-121">Lorsque vous concevez des algorithmes de nuanceur, gardez à l’esprit les points suivants :</span><span class="sxs-lookup"><span data-stu-id="a5419-121">When you design shader algorithms, keep the following in mind:</span></span>

-   <span data-ttu-id="a5419-122">Effectuez des calculs sur le nuanceur de sommets, si possible.</span><span class="sxs-lookup"><span data-stu-id="a5419-122">Perform calculations on the vertex shader if possible.</span></span> <span data-ttu-id="a5419-123">Un calcul effectué sur un nuanceur de pixels est beaucoup plus onéreux qu’un calcul effectué sur un nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="a5419-123">A calculation that is performed on a pixel shader is much more expensive than a calculation that is performed on a vertex shader.</span></span>
-   <span data-ttu-id="a5419-124">Envisagez d’utiliser des calculs par vertex pour améliorer les performances dans des situations telles que des maillages denses.</span><span class="sxs-lookup"><span data-stu-id="a5419-124">Consider using per-vertex calculations to improve performance in situations such as dense meshes.</span></span> <span data-ttu-id="a5419-125">Pour les maillages denses, les calculs par vertex peuvent produire des résultats qui ne se distinguent pas visuellement des résultats produits par des calculs par pixel.</span><span class="sxs-lookup"><span data-stu-id="a5419-125">For dense meshes, per-vertex calculations may produce results that are visually indistinguishable from results produced with per-pixel calculations.</span></span>

## <a name="skip-unnecessary-instructions"></a><span data-ttu-id="a5419-126">Ignorer les instructions inutiles</span><span class="sxs-lookup"><span data-stu-id="a5419-126">Skip Unnecessary Instructions</span></span>

<span data-ttu-id="a5419-127">En HLSL, la fonctionnalité de branchement dynamique permet de limiter le nombre d’instructions exécutées.</span><span class="sxs-lookup"><span data-stu-id="a5419-127">In HLSL, dynamic branching provides the ability to limit the number of instructions that are executed.</span></span> <span data-ttu-id="a5419-128">Par conséquent, la création de branche dynamique peut accélérer la durée d’exécution du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a5419-128">Therefore, dynamic branching can help speed up shader execution time.</span></span> <span data-ttu-id="a5419-129">Si la géométrie ou les pixels ne sont pas affichés, utilisez la branche dynamique pour quitter le nuanceur ou pour limiter les instructions.</span><span class="sxs-lookup"><span data-stu-id="a5419-129">If geometry or pixels are not displayed, use dynamic branching to exit the shader or to limit instructions.</span></span> <span data-ttu-id="a5419-130">Par exemple, si un pixel n’est pas allumé, il n’y a aucun point dans l’exécution de l’algorithme d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="a5419-130">For example, if a pixel is not lit, there is no point in executing the lighting algorithm.</span></span>

<span data-ttu-id="a5419-131">Le tableau suivant répertorie certains cas où vous pouvez tester des conditions dans votre nuanceur et utiliser la branche dynamique pour ignorer les instructions inutiles.</span><span class="sxs-lookup"><span data-stu-id="a5419-131">The following table lists some cases where you can test conditions in your shader and use dynamic branching to skip unnecessary instructions.</span></span> <span data-ttu-id="a5419-132">La table n’est pas exhaustive.</span><span class="sxs-lookup"><span data-stu-id="a5419-132">The table not comprehensive.</span></span> <span data-ttu-id="a5419-133">Au lieu de cela, elle est destinée à vous donner des idées pour l’optimisation de votre code.</span><span class="sxs-lookup"><span data-stu-id="a5419-133">Rather, it is intended to give you ideas for optimizing your code.</span></span>



| <span data-ttu-id="a5419-134">Condition à vérifier</span><span class="sxs-lookup"><span data-stu-id="a5419-134">Condition to Check</span></span>                                    | <span data-ttu-id="a5419-135">Réponse dans le nuanceur</span><span class="sxs-lookup"><span data-stu-id="a5419-135">Response in the Shader</span></span>       |
|-------------------------------------------------------|------------------------------|
| <span data-ttu-id="a5419-136">La vérification alpha détermine qu’un pixel ne sera pas visible.</span><span class="sxs-lookup"><span data-stu-id="a5419-136">Alpha check determines that a pixel will not be seen.</span></span> | <span data-ttu-id="a5419-137">Ignorez le reste du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a5419-137">Skip the rest of the shader.</span></span> |
| <span data-ttu-id="a5419-138">Le pixel ou la géométrie est entièrement buée.</span><span class="sxs-lookup"><span data-stu-id="a5419-138">The pixel or geometry is fully fogged.</span></span>                | <span data-ttu-id="a5419-139">Ignorez le reste du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a5419-139">Skip the rest of the shader.</span></span> |
| <span data-ttu-id="a5419-140">Les pondérations de la peau sont égales à zéro.</span><span class="sxs-lookup"><span data-stu-id="a5419-140">Skin weights are zero.</span></span>                                | <span data-ttu-id="a5419-141">Ignore les segments.</span><span class="sxs-lookup"><span data-stu-id="a5419-141">Skip bones.</span></span>                  |
| <span data-ttu-id="a5419-142">L’atténuation légère est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="a5419-142">Light attenuation is zero.</span></span>                            | <span data-ttu-id="a5419-143">Ignorer l’éclairage.</span><span class="sxs-lookup"><span data-stu-id="a5419-143">Skip lighting.</span></span>               |
| <span data-ttu-id="a5419-144">Terme Lambert non positif.</span><span class="sxs-lookup"><span data-stu-id="a5419-144">Non-positive Lambertian term.</span></span>                         | <span data-ttu-id="a5419-145">Ignorer l’éclairage.</span><span class="sxs-lookup"><span data-stu-id="a5419-145">Skip lighting.</span></span>               |



 

## <a name="pack-variables-and-interpolants"></a><span data-ttu-id="a5419-146">Variables et interpolations de Pack</span><span class="sxs-lookup"><span data-stu-id="a5419-146">Pack Variables and Interpolants</span></span>

<span data-ttu-id="a5419-147">Gardez à l’esprit l’espace requis pour les données de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a5419-147">Be mindful of the space required for shader data.</span></span> <span data-ttu-id="a5419-148">Compressez autant d’informations que possible dans une variable ou une interpolation.</span><span class="sxs-lookup"><span data-stu-id="a5419-148">Pack as much information into a variable or interpolant as possible.</span></span> <span data-ttu-id="a5419-149">Parfois, les informations de deux variables peuvent être empaquetées dans l’espace mémoire d’une variable unique.</span><span class="sxs-lookup"><span data-stu-id="a5419-149">Sometimes, the information from two variables can be packed into the memory space of a single variable.</span></span>

## <a name="reduce-shader-complexity"></a><span data-ttu-id="a5419-150">Réduire la complexité des nuanceurs</span><span class="sxs-lookup"><span data-stu-id="a5419-150">Reduce Shader Complexity</span></span>

<span data-ttu-id="a5419-151">N’oubliez pas que vos nuanceurs sont petits et simples.</span><span class="sxs-lookup"><span data-stu-id="a5419-151">Keep your shaders small and simple.</span></span> <span data-ttu-id="a5419-152">En général, les nuanceurs avec moins d’instructions s’exécutent plus rapidement que les nuanceurs avec davantage d’instructions.</span><span class="sxs-lookup"><span data-stu-id="a5419-152">In general, shaders with fewer instructions execute more quickly than shaders with more instructions.</span></span> <span data-ttu-id="a5419-153">Il est également plus facile de déboguer et d’optimiser des nuanceurs plus petits et moins complexes.</span><span class="sxs-lookup"><span data-stu-id="a5419-153">It is also easier to debug and optimize smaller, less complex shaders.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5419-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a5419-154">Related Topics</span></span>

[<span data-ttu-id="a5419-155">Guide de programmation pour HLSL</span><span class="sxs-lookup"><span data-stu-id="a5419-155">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a><span data-ttu-id="a5419-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a5419-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5419-157">Guide de programmation pour HLSL</span><span class="sxs-lookup"><span data-stu-id="a5419-157">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




