---
title: Liaison de nuanceurs d’effet
description: Direct2D utilise une optimisation appelée liaison de nuanceur d’effet qui combine plusieurs passes de rendu de graphique d’effet dans une seule passe.
ms.assetid: 431A5B39-6C84-442D-AC66-0F341E10DF2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a17691346649b2ddcde7ca4f3e343be6a35a90
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104321677"
---
# <a name="effect-shader-linking"></a><span data-ttu-id="171a4-103">Liaison de nuanceurs d’effet</span><span class="sxs-lookup"><span data-stu-id="171a4-103">Effect Shader Linking</span></span>

<span data-ttu-id="171a4-104">Direct2D utilise une optimisation appelée liaison de nuanceur d’effet qui combine plusieurs passes de rendu de graphique d’effet dans une seule passe.</span><span class="sxs-lookup"><span data-stu-id="171a4-104">Direct2D uses an optimization called effect shader linking which combines multiple effect graph rendering passes into a single pass.</span></span>

-   [<span data-ttu-id="171a4-105">Vue d’ensemble de la liaison d’effet du nuanceur</span><span class="sxs-lookup"><span data-stu-id="171a4-105">Overview of Effect Shader Linking</span></span>](#overview-of-effect-shader-linking)
-   [<span data-ttu-id="171a4-106">Utilisation de la liaison de nuanceur d’effet</span><span class="sxs-lookup"><span data-stu-id="171a4-106">Using Effect Shader Linking</span></span>](#using-effect-shader-linking)
-   [<span data-ttu-id="171a4-107">Création d’un effet personnalisé compatible avec la liaison de nuanceur</span><span class="sxs-lookup"><span data-stu-id="171a4-107">Authoring a shader linking-compatible custom effect</span></span>](#authoring-a-shader-linking-compatible-custom-effect)
-   [<span data-ttu-id="171a4-108">Exemple de nuanceur d’effets compatibles avec la liaison</span><span class="sxs-lookup"><span data-stu-id="171a4-108">Example linking-compatible effect shader</span></span>](#example-linking-compatible-effect-shader)
-   [<span data-ttu-id="171a4-109">Compilation d’un nuanceur compatible avec les liaisons</span><span class="sxs-lookup"><span data-stu-id="171a4-109">Compiling a linking compatible-shader</span></span>](#compiling-a-linking-compatible-shader)
    -   [<span data-ttu-id="171a4-110">Étape 1 : compiler la fonction d’exportation</span><span class="sxs-lookup"><span data-stu-id="171a4-110">Step 1: Compile the export function</span></span>](#step-1-compile-the-export-function)
    -   [<span data-ttu-id="171a4-111">Étape 2 : compiler le nuanceur complet et incorporer la fonction d’exportation</span><span class="sxs-lookup"><span data-stu-id="171a4-111">Step 2: Compile the full shader and embed the export function</span></span>](#step-2-compile-the-full-shader-and-embed-the-export-function)
-   [<span data-ttu-id="171a4-112">Exporter les spécifications de fonction</span><span class="sxs-lookup"><span data-stu-id="171a4-112">Export function specifications</span></span>](#export-function-specifications)
-   [<span data-ttu-id="171a4-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="171a4-113">Related topics</span></span>](#related-topics)

## <a name="overview-of-effect-shader-linking"></a><span data-ttu-id="171a4-114">Vue d’ensemble de la liaison d’effet du nuanceur</span><span class="sxs-lookup"><span data-stu-id="171a4-114">Overview of Effect Shader Linking</span></span>

<span data-ttu-id="171a4-115">L’effet nuanceur de liaison des optimisations s’appuie sur la liaison de nuanceur HLSL, une fonctionnalité Direct3D 11,2 qui permet de générer des nuanceurs de pixels et de vertex au moment de l’exécution en liant des fonctions de nuanceur précompilées.</span><span class="sxs-lookup"><span data-stu-id="171a4-115">The effect shader linking optimizations builds on top of HLSL shader linking, a Direct3D 11.2 feature that allows pixel and vertex shaders to be generated at runtime by linking pre-compiled shader functions.</span></span> <span data-ttu-id="171a4-116">Les figures suivantes illustrent le concept de liaison de nuanceur d’effet dans un graphique d’effet.</span><span class="sxs-lookup"><span data-stu-id="171a4-116">The following figures illustrate the concept of effect shader linking in an effect graph.</span></span> <span data-ttu-id="171a4-117">La première figure montre un graphique d’effet Direct2D classique avec quatre transformations de rendu.</span><span class="sxs-lookup"><span data-stu-id="171a4-117">The first figure shows a typical Direct2D effect graph with four rendering transforms.</span></span> <span data-ttu-id="171a4-118">Sans liaison de nuanceur, chaque transformation consomme une passe de rendu et requiert une surface intermédiaire. au total, ce graphique nécessite 4 passes et 3 intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="171a4-118">Without shader linking, each transform consumes a rendering pass and requires an intermediate surface; in total, this graph requires 4 passes and 3 intermediates.</span></span>



|                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|
| ![graphique de transformation sans liaison de nuanceur : 4 passes et 3 intermédiaires.](images/shader-transform-graph.png) |



 

<span data-ttu-id="171a4-120">La deuxième figure présente le même graphique d’effet où chaque transformation de rendu a été remplacée par une version de fonction qui peut être liée.</span><span class="sxs-lookup"><span data-stu-id="171a4-120">The second figure shows the same effect graph where each rendering transform has been replaced with a linkable function version.</span></span> <span data-ttu-id="171a4-121">Direct2D est en mesure de lier l’intégralité du graphique et de l’exécuter en une seule passe sans aucun intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="171a4-121">Direct2D is able link the entire graph and execute it in one pass without requiring any intermediates.</span></span> <span data-ttu-id="171a4-122">Cela peut augmenter considérablement la durée d’exécution du GPU et réduire la consommation de mémoire du GPU.</span><span class="sxs-lookup"><span data-stu-id="171a4-122">This can provide a significant decrease in GPU execution time and reduction in peak GPU memory consumption.</span></span>



|                                                                                                   |
|---------------------------------------------------------------------------------------------------|
| ![graphique de transformation avec liaison de nuanceur : 1 passe, 0 intermédiaire.](images/shader-linking-graph.png) |



 

<span data-ttu-id="171a4-124">La liaison d’effet du nuanceur opère sur des transformations individuelles dans un effet ; Cela signifie que même un graphique avec un seul effet peut bénéficier d’une liaison de nuanceur si cet effet a plusieurs transformations valides.</span><span class="sxs-lookup"><span data-stu-id="171a4-124">Effect shader linking operates on individual transforms within an effect; this means that even a graph with a single effect may benefit from shader linking if that effect has multiple valid transforms.</span></span>

## <a name="using-effect-shader-linking"></a><span data-ttu-id="171a4-125">Utilisation de la liaison de nuanceur d’effet</span><span class="sxs-lookup"><span data-stu-id="171a4-125">Using Effect Shader Linking</span></span>

<span data-ttu-id="171a4-126">Si vous créez une application Direct2D qui utilise des effets, vous n’avez rien à faire pour tirer parti de la liaison d’effet du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="171a4-126">If you are building a Direct2D application that uses effects, you don’t need to do anything to take advantage of effect shader linking.</span></span> <span data-ttu-id="171a4-127">Direct2D analyse automatiquement le graphique d’effet pour déterminer la méthode la plus optimale pour lier chaque transformation.</span><span class="sxs-lookup"><span data-stu-id="171a4-127">Direct2D automatically analyzes the effect graph to determine the most optimal way to link each transform.</span></span>

<span data-ttu-id="171a4-128">Les auteurs des effets sont responsables de l’implémentation de leur effet de manière à prendre en charge la liaison de nuanceur d’effets ; Pour plus d’informations, consultez la section [création d’un effet personnalisé compatible avec les liaisons de nuanceur-](#authoring-a-shader-linking-compatible-custom-effect) ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="171a4-128">Effect authors are responsible for implementing their effect in a way that supports effect shader linking; for more information, see the [Authoring a shader linking-compatible custom effect](#authoring-a-shader-linking-compatible-custom-effect) section below.</span></span> <span data-ttu-id="171a4-129">Tous les effets intégrés prennent en charge la liaison de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="171a4-129">All of the built-in effects support shader linking.</span></span>

<span data-ttu-id="171a4-130">Direct2D liera uniquement les transformations de rendu adjacentes dans les situations où il est bénéfique.</span><span class="sxs-lookup"><span data-stu-id="171a4-130">Direct2D will only link adjacent rendering transforms in situations where it is beneficial.</span></span> <span data-ttu-id="171a4-131">Il prend en compte plusieurs facteurs pour déterminer s’il faut lier deux transformations.</span><span class="sxs-lookup"><span data-stu-id="171a4-131">It takes into account multiple factors when determining whether to link two transforms.</span></span> <span data-ttu-id="171a4-132">Par exemple, la liaison de nuanceur n’est pas effectuée si l’une des transformations utilise des nuanceurs de vertex ou de calcul, car seuls les nuanceurs de pixels peuvent être liés.</span><span class="sxs-lookup"><span data-stu-id="171a4-132">For example, shader linking is not performed if one of the transforms uses vertex or compute shaders, as only pixel shaders can be linked.</span></span> <span data-ttu-id="171a4-133">En outre, si un effet n’a pas été créé pour être compatible avec la liaison de nuanceur, les transformations environnantes ne sont pas liées.</span><span class="sxs-lookup"><span data-stu-id="171a4-133">Also, if an effect was not authored to be compatible with shader linking, then surrounding transforms will not be linked with it.</span></span>

<span data-ttu-id="171a4-134">Dans le cas où un tel risque de liaison existe, Direct2D ne lie pas les transformations adjacentes au risque, mais tente toujours de lier le reste du graphique.</span><span class="sxs-lookup"><span data-stu-id="171a4-134">In the case that such a linking hazard exists, Direct2D will not link any transforms adjacent to the hazard, but will still attempt to link the remainder of the graph.</span></span>



|                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|
| ![transformer le graphique avec un risque de liaison : 2 passes, 1 intermédiaire.](images/shader-linking-graph-hazard.png) |



 

## <a name="authoring-a-shader-linking-compatible-custom-effect"></a><span data-ttu-id="171a4-136">Création d’un effet personnalisé compatible avec la liaison de nuanceur</span><span class="sxs-lookup"><span data-stu-id="171a4-136">Authoring a shader linking-compatible custom effect</span></span>

<span data-ttu-id="171a4-137">Si vous créez votre propre effet Direct2D personnalisé, vous devez vous assurer que ses transformations prennent en charge la liaison de nuanceur Effects.</span><span class="sxs-lookup"><span data-stu-id="171a4-137">If you are authoring your own custom Direct2D effect, you need to ensure that its transforms supports effect shader linking.</span></span> <span data-ttu-id="171a4-138">Cela nécessite des modifications mineures par rapport à la façon dont les effets personnalisés précédents ont été implémentés.</span><span class="sxs-lookup"><span data-stu-id="171a4-138">This requires some minor changes from how previous custom effects were implemented.</span></span> <span data-ttu-id="171a4-139">Si une transformation dans votre effet personnalisé ne prend pas en charge la liaison de nuanceur, Direct2D ne la lie pas à des transformations adjacentes dans le graphique d’effet.</span><span class="sxs-lookup"><span data-stu-id="171a4-139">If a transform within your custom effect does not support shader linking, then Direct2D will not link it with any transforms adjacent to it in the effect graph.</span></span>

<span data-ttu-id="171a4-140">En tant qu’auteur d’effet personnalisé, vous devez être conscient de plusieurs concepts et exigences clés :</span><span class="sxs-lookup"><span data-stu-id="171a4-140">As a custom effect author, you should be aware of several key concepts and requirements:</span></span>

-   <span data-ttu-id="171a4-141">**Aucune modification n’est apportée aux implémentations d’interface**</span><span class="sxs-lookup"><span data-stu-id="171a4-141">**No changes to effect interface implementations**</span></span>

    <span data-ttu-id="171a4-142">Vous n’avez pas besoin de modifier le code qui implémente les différentes interfaces Effects, telles que [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform).</span><span class="sxs-lookup"><span data-stu-id="171a4-142">You do not need to modify any code implementing the various effect interfaces such as [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform).</span></span>

-   <span data-ttu-id="171a4-143">**Fournir une version de fonction d’exportation et complète des nuanceurs**</span><span class="sxs-lookup"><span data-stu-id="171a4-143">**Provide both a full and export function version of shaders**</span></span>

    <span data-ttu-id="171a4-144">Vous devez fournir une version de fonction d’exportation des nuanceurs de vos effets qui peuvent être liés par Direct2D.</span><span class="sxs-lookup"><span data-stu-id="171a4-144">You must provide an export function version of your effect’s shaders which are linkable by Direct2D.</span></span> <span data-ttu-id="171a4-145">En outre, vous devez également continuer à fournir le nuanceur complet original ; en effet, Direct2D sélectionne au moment de l’exécution la version de nuanceur appropriée, selon que la liaison de nuanceur doit être appliquée à un lien particulier dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="171a4-145">In addition, you must also continue to provide the original, full shader; this is because Direct2D selects at runtime the right shader version depending on whether shader linking is to be applied to a particular link in the graph.</span></span>

    <span data-ttu-id="171a4-146">Si une transformation fournit uniquement l’objet blob de nuanceur de pixels complet (via [ID2D1EffectContext :: LoadPixelShader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)), elle ne sera pas liée à des transformations adjacentes.</span><span class="sxs-lookup"><span data-stu-id="171a4-146">If a transform only provides the full pixel shader blob (via [ID2D1EffectContext::LoadPixelShader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)), it will not be linked to adjacent transforms.</span></span>

- <span data-ttu-id="171a4-147">**Fonctions d’assistance**</span><span class="sxs-lookup"><span data-stu-id="171a4-147">**Helper functions**</span></span>

    <span data-ttu-id="171a4-148">Direct2D fournit des fonctions et des macros [d’assistance HLSL](hlsl-helpers.md) qui génèrent automatiquement les versions complète et d’exportation des fonctions d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="171a4-148">Direct2D provides [HLSL helper functions](hlsl-helpers.md) and macros that will automatically generate both the full and export function versions of a shader.</span></span> <span data-ttu-id="171a4-149">Ces applications auxiliaires se trouvent dans d2d1effecthelpers. hlsli.</span><span class="sxs-lookup"><span data-stu-id="171a4-149">These helpers can be found in d2d1effecthelpers.hlsli.</span></span> <span data-ttu-id="171a4-150">En outre, le compilateur HLSL (FXC) vous permet d’insérer le nuanceur de fonction d’exportation dans un champ privé dans le nuanceur complet.</span><span class="sxs-lookup"><span data-stu-id="171a4-150">In addition, the HLSL compiler (FXC) lets you insert the export function shader into a private field in the full shader.</span></span> <span data-ttu-id="171a4-151">De cette façon, il vous suffit de créer un nuanceur une seule fois et de transmettre les deux versions à Direct2D simultanément.</span><span class="sxs-lookup"><span data-stu-id="171a4-151">In this way, you only need to author a shader once and pass both versions to Direct2D simultaneously.</span></span> <span data-ttu-id="171a4-152">D2d1effecthelpers. hlsli et le compilateur FXC sont inclus dans le cadre du SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="171a4-152">Both d2d1effecthelpers.hlsli and the FXC compiler are included as part of the Windows SDK.</span></span>

    <span data-ttu-id="171a4-153">Fonctions d’assistance :</span><span class="sxs-lookup"><span data-stu-id="171a4-153">The helper functions:</span></span>

  - [<span data-ttu-id="171a4-154">D2DGetInput</span><span class="sxs-lookup"><span data-stu-id="171a4-154">D2DGetInput</span></span>](d2dgetinput.md)  
  - [<span data-ttu-id="171a4-155">D2DSampleInput</span><span class="sxs-lookup"><span data-stu-id="171a4-155">D2DSampleInput</span></span>](d2dsampleinput.md)  
  - [<span data-ttu-id="171a4-156">D2DSampleInputAtOffset</span><span class="sxs-lookup"><span data-stu-id="171a4-156">D2DSampleInputAtOffset</span></span>](d2dsampleinputatoffset.md)  
  - [<span data-ttu-id="171a4-157">D2DSampleInputAtPosition</span><span class="sxs-lookup"><span data-stu-id="171a4-157">D2DSampleInputAtPosition</span></span>](d2dsampleinputatposition.md)  
  - [<span data-ttu-id="171a4-158">D2DGetInputCoordinate</span><span class="sxs-lookup"><span data-stu-id="171a4-158">D2DGetInputCoordinate</span></span>](d2dgetinputcoordinate.md)  
  - [<span data-ttu-id="171a4-159">D2DGetScenePosition</span><span class="sxs-lookup"><span data-stu-id="171a4-159">D2DGetScenePosition</span></span>](d2dgetsceneposition.md)  
  - [<span data-ttu-id="171a4-160">Entrée de la \_ PS D2D \_</span><span class="sxs-lookup"><span data-stu-id="171a4-160">D2D\_PS\_ENTRY</span></span>](d2d-ps-entry.md)  

  <span data-ttu-id="171a4-161">Vous pouvez également créer manuellement deux versions de chaque nuanceur et les compiler à deux reprises, à condition que les spécifications décrites ci-dessous dans les [spécifications de fonction d’exportation](#export-function-specifications) soient respectées.</span><span class="sxs-lookup"><span data-stu-id="171a4-161">You can also manually author two versions of each shader and compile them twice, as long as the specifications described below in [Export function specifications](#export-function-specifications) are met.</span></span>

-   <span data-ttu-id="171a4-162">**Nuanceurs de pixels uniquement**</span><span class="sxs-lookup"><span data-stu-id="171a4-162">**Pixel shaders only**</span></span>

    <span data-ttu-id="171a4-163">Direct2D ne prend pas en charge la liaison des nuanceurs de calcul ou de vertex.</span><span class="sxs-lookup"><span data-stu-id="171a4-163">Direct2D does not support linking compute or vertex shaders.</span></span> <span data-ttu-id="171a4-164">Toutefois, si votre effet utilise à la fois un nuanceur de sommets et de pixels, la sortie du nuanceur de pixels peut toujours être liée.</span><span class="sxs-lookup"><span data-stu-id="171a4-164">However, if your effect uses both a vertex and pixel shader, the output of the pixel shader can still be linked.</span></span>

-   <span data-ttu-id="171a4-165">**Échantillonnage simple et complexe**</span><span class="sxs-lookup"><span data-stu-id="171a4-165">**Simple versus complex sampling**</span></span>

    <span data-ttu-id="171a4-166">La liaison de fonction de nuanceur fonctionne en connectant la sortie d’un nuanceur de pixels à l’entrée d’une passe de nuanceur de pixels suivante.</span><span class="sxs-lookup"><span data-stu-id="171a4-166">Shader function linking works by connecting the output of one pixel shader pass to the input of a subsequent pixel shader pass.</span></span> <span data-ttu-id="171a4-167">Cela est possible uniquement lorsque le nuanceur de pixels consommatrice requiert une seule valeur d’entrée pour effectuer son calcul. Cette valeur provient normalement de l’échantillonnage d’une texture d’entrée au niveau des coordonnées de texture émises par le nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="171a4-167">This is only possible when the consuming pixel shader requires only a single input value to perform its computation; this value would normally come from sampling an input texture at the texture coordinate emitted by the vertex shader.</span></span> <span data-ttu-id="171a4-168">Un tel nuanceur de pixels est dit d’effectuer un échantillonnage simple.</span><span class="sxs-lookup"><span data-stu-id="171a4-168">Such a pixel shader is said to perform simple sampling.</span></span>

    

    |                                                                                                                                                                                            |
    |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | ![la conversion en nuances de gris est un exemple d’échantillonnage simple.](images/simple-sampling.png) |

    

     

    <span data-ttu-id="171a4-171">Certains nuanceurs de pixels, tels qu’un flou gaussien, calculent leur sortie à partir de plusieurs exemples d’entrée plutôt qu’un seul échantillon.</span><span class="sxs-lookup"><span data-stu-id="171a4-171">Some pixel shaders, such as a Gaussian blur, compute their output from multiple input samples rather than just a single sample.</span></span> <span data-ttu-id="171a4-172">Un tel nuanceur de pixels est dit d’effectuer un échantillonnage complexe.</span><span class="sxs-lookup"><span data-stu-id="171a4-172">Such a pixel shader is said to perform complex sampling.</span></span>

    

    |                                                                                                                                                           |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------|
    | ![le flou gaussien est un exemple d’échantillonnage complexe.](images/complex-sampling.png) |

    

     

    <span data-ttu-id="171a4-175">Seules les fonctions de nuanceur avec des entrées simples peuvent avoir leur entrée fournie par une autre fonction de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="171a4-175">Only shader functions with simple inputs can have their input provided by another shader function.</span></span> <span data-ttu-id="171a4-176">Les fonctions de nuanceur avec des entrées complexes doivent être fournies avec une texture d’entrée pour échantillonner.</span><span class="sxs-lookup"><span data-stu-id="171a4-176">Shader functions with complex inputs must be provided with an input texture to sample.</span></span> <span data-ttu-id="171a4-177">Cela signifie que Direct2D ne lie pas un nuanceur avec des entrées complexes à son prédécesseur.</span><span class="sxs-lookup"><span data-stu-id="171a4-177">This means that Direct2D will not link a shader with complex inputs to its predecessor.</span></span>

    <span data-ttu-id="171a4-178">Lorsque vous utilisez les [applications auxiliaires HLSL de Direct2D](hlsl-helpers.md), vous devez indiquer dans le langage HLSL si un nuanceur utilise des entrées complexes ou simples.</span><span class="sxs-lookup"><span data-stu-id="171a4-178">When using the [Direct2D HLSL helpers](hlsl-helpers.md), you must indicate in the HLSL whether a shader uses complex or simple inputs.</span></span>

## <a name="example-linking-compatible-effect-shader"></a><span data-ttu-id="171a4-179">Exemple de nuanceur d’effets compatibles avec la liaison</span><span class="sxs-lookup"><span data-stu-id="171a4-179">Example linking-compatible effect shader</span></span>

<span data-ttu-id="171a4-180">À l’aide des applications d’assistance D2D, l’extrait de code suivant représente un nuanceur d’effets compatible avec la liaison simple :</span><span class="sxs-lookup"><span data-stu-id="171a4-180">Using the D2D helpers, the following code snippet represents a simple linking-compatible effect shader:</span></span>

```syntax
#define D2D_INPUT_COUNT 1
#define D2D_INPUT0_SIMPLE
#include “d2d1effecthelpers.hlsli”

D2D_PS_ENTRY(LinkingCompatiblePixelShader)
{
    float4 input = D2DGetInput(0);
    input.rgb *= input.a;
    return input;
}          
```

<span data-ttu-id="171a4-181">Dans cet exemple bref, Notez qu’aucun paramètre de fonction n’est déclaré, que le nombre d’entrées et le type de chaque entrée sont déclarés avant la fonction d’entrée, que l’entrée est récupérée en appelant [D2DGetInput](d2dgetinput.md), et que les directives de préprocesseur doivent être définies avant l’inclusion du fichier d’assistance.</span><span class="sxs-lookup"><span data-stu-id="171a4-181">In this short example note that no function parameters are declared, that the number of inputs and type of each input is declared before the entry function, the input is retrieved by calling [D2DGetInput](d2dgetinput.md), and that preprocessor directives must be defined before the helper file is included.</span></span>

<span data-ttu-id="171a4-182">Un nuanceur compatible avec la liaison doit fournir un nuanceur de pixels à passage unique standard et une fonction d’exportation de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="171a4-182">A linking-compatible shader must provide both a regular single-pass pixel shader and an export shader function.</span></span> <span data-ttu-id="171a4-183">La macro d' [ \_ \_ entrée de la PS D2D](d2d-ps-entry.md) permet de générer chacune d’elles à partir du même code, quand elles sont utilisées conjointement avec le script de compilation du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="171a4-183">The [D2D\_PS\_ENTRY](d2d-ps-entry.md) macro allows each of these to be generated from the same code, when used in conjunction with the shader compilation script.</span></span>

<span data-ttu-id="171a4-184">Lors de la compilation d’un nuanceur complet, les macros sont développées dans le code suivant, qui a une signature d’entrée compatible avec les effets D2D.</span><span class="sxs-lookup"><span data-stu-id="171a4-184">When compiling a full shader, the macros are expanded into the following code, which has a D2D Effects-compatible input signature.</span></span>

```syntax
Texture2D<float4> InputTexture0;
SamplerState InputSampler0;

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,
    float4 posScene : SCENE_POSITION,
    float4 uv0  : TEXCOORD0
    ) : SV_Target
    {
        float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);
        input.rgb *= input.a;
        return input;
    }    
```

<span data-ttu-id="171a4-185">Lors de la compilation d’une version de fonction d’exportation du même code, le code suivant est généré :</span><span class="sxs-lookup"><span data-stu-id="171a4-185">When compiling an export function version of the same code, the following code is generated:</span></span>

```syntax
// Shader function version
export float4 LinkingCompatiblePixelShader_Function(
    float4 input0 : INPUT0)
    {
        input.rgb *= input.a;
        return input;
    }      
```

<span data-ttu-id="171a4-186">Notez que l’entrée de texture, normalement récupérée par l’échantillonnage d’un Texture2D, a été remplacée par une entrée de fonction (input0).</span><span class="sxs-lookup"><span data-stu-id="171a4-186">Note that the texture input, normally retrieved by sampling a Texture2D, has been replaced with a function input (input0).</span></span>

<span data-ttu-id="171a4-187">Pour obtenir une description détaillée de ce que vous devez faire pour écrire un effet compatible avec la liaison, consultez le didacticiel sur les [effets personnalisés](custom-effects.md) et l' [exemple effets d’images personnalisées Direct2D](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="171a4-187">To see a full, step by step description of what you need to do to write a linking-compatible effect, see the [Custom effects tutorial](custom-effects.md) and the [Direct2D custom image effects sample](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

## <a name="compiling-a-linking-compatible-shader"></a><span data-ttu-id="171a4-188">Compilation d’un nuanceur compatible avec les liaisons</span><span class="sxs-lookup"><span data-stu-id="171a4-188">Compiling a linking compatible-shader</span></span>

<span data-ttu-id="171a4-189">Pour pouvoir être lié, l’objet blob de nuanceur de pixels passé à D2D doit contenir à la fois les versions complète et d’exportation de la fonction du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="171a4-189">To be linkable, the pixel shader blob passed to D2D must contain both the full and export function versions of the shader.</span></span> <span data-ttu-id="171a4-190">Pour ce faire, incorporez la fonction d’exportation compilée dans la zone de données privées de l' \_ objet BLOB D3D \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="171a4-190">This is accomplished by embedding the compiled export function into the D3D\_BLOB\_PRIVATE\_DATA area.</span></span>

<span data-ttu-id="171a4-191">Lorsque les nuanceurs sont créés avec les fonctions d’assistance D2D, une cible de compilation D2D doit être définie au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="171a4-191">When the shaders are authored with the D2D helper functions, a D2D compilation target must be defined at compilation time.</span></span> <span data-ttu-id="171a4-192">Les types de cibles de compilation sont le \_ \_ nuanceur complet D2D et la \_ fonction D2D.</span><span class="sxs-lookup"><span data-stu-id="171a4-192">The compilation target types are D2D\_FULL\_SHADER and D2D\_FUNCTION.</span></span>

<span data-ttu-id="171a4-193">La compilation d’un nuanceur d’effets compatible avec la liaison est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="171a4-193">Compiling a linking-compatible effect shader is a two-step process:</span></span>

-   [<span data-ttu-id="171a4-194">Compiler la fonction d’exportation</span><span class="sxs-lookup"><span data-stu-id="171a4-194">Compile the export function</span></span>](#step-1-compile-the-export-function)
-   [<span data-ttu-id="171a4-195">Compiler le nuanceur complet et incorporer la fonction d’exportation</span><span class="sxs-lookup"><span data-stu-id="171a4-195">Compile the full shader and embed the export function</span></span>](#step-2-compile-the-full-shader-and-embed-the-export-function)

> [!Note]  
> <span data-ttu-id="171a4-196">Lors de la compilation d’un effet à l’aide de Visual Studio, vous devez créer un fichier de commandes qui exécute les deux commandes FXC et exécuter ce fichier de commandes en tant qu’étape de génération personnalisée qui s’exécute avant l’étape de compilation.</span><span class="sxs-lookup"><span data-stu-id="171a4-196">When compiling an effect using Visual Studio, you should create a batch file that executes both FXC commands and run this batch file as a custom build step that runs before the compile step.</span></span>

 

### <a name="step-1-compile-the-export-function"></a><span data-ttu-id="171a4-197">Étape 1 : compiler la fonction d’exportation</span><span class="sxs-lookup"><span data-stu-id="171a4-197">Step 1: Compile the export function</span></span>

```syntax
fxc /T <shadermodel> <MyShaderFile>.hlsl /D D2D_FUNCTION /D D2D_ENTRY=<entry> /Fl <MyShaderFile>.fxlib           
```

<span data-ttu-id="171a4-198">Pour compiler la version de la fonction d’exportation de votre nuanceur, vous devez passer les indicateurs suivants à FXC.</span><span class="sxs-lookup"><span data-stu-id="171a4-198">To compile the export function version of your shader, you must pass the following flags to FXC.</span></span>



|                                |                                                                                                                                                                                                                                                           |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="171a4-199">**Indicateur**</span><span class="sxs-lookup"><span data-stu-id="171a4-199">**Flag**</span></span>                       | <span data-ttu-id="171a4-200">**Description**</span><span class="sxs-lookup"><span data-stu-id="171a4-200">**Description**</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="171a4-201">Commutateur <ShaderModel></span><span class="sxs-lookup"><span data-stu-id="171a4-201">/T <ShaderModel></span></span>         | <span data-ttu-id="171a4-202">Définissez <ShaderModel> sur le profil de nuanceur de pixels approprié, tel que défini dans la [syntaxe fxc](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span><span class="sxs-lookup"><span data-stu-id="171a4-202">Set <ShaderModel> to the appropriate pixel shader profile as defined in [FXC Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span></span> <span data-ttu-id="171a4-203">Il doit s’agir de l’un des profils listés sous « liaison de nuanceur HLSL ».</span><span class="sxs-lookup"><span data-stu-id="171a4-203">This must be one of the profiles listed under “HLSL shader linking”.</span></span> |
| <span data-ttu-id="171a4-204"><MyShaderFile>.hlsl</span><span class="sxs-lookup"><span data-stu-id="171a4-204"><MyShaderFile>.hlsl</span></span>      | <span data-ttu-id="171a4-205">Définissez <MyShaderFile> sur le nom du fichier HLSL.</span><span class="sxs-lookup"><span data-stu-id="171a4-205">Set <MyShaderFile> to the name of the HLSL file.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="171a4-206">/D, \_ fonction D2D</span><span class="sxs-lookup"><span data-stu-id="171a4-206">/D D2D\_FUNCTION</span></span>               | <span data-ttu-id="171a4-207">Cette définition indique à FXC de compiler la version de la fonction d’exportation du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="171a4-207">This definition instructs FXC to compile the export function version of the shader.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="171a4-208">/D ( \_ entrée D2D) =<entry></span><span class="sxs-lookup"><span data-stu-id="171a4-208">/D D2D\_ENTRY=<entry></span></span>    | <span data-ttu-id="171a4-209">Définissez <entry> sur le nom du point d’entrée HLSL que vous avez défini dans la macro d' [ \_ \_ entrée](d2d-ps-entry.md) de l’extension de bloc D2D.</span><span class="sxs-lookup"><span data-stu-id="171a4-209">Set <entry> to the name of the HLSL entry point you defined inside the [D2D\_PS\_ENTRY](d2d-ps-entry.md) macro.</span></span>                                                                                                                                    |
| <span data-ttu-id="171a4-210">/FL <MyShaderFile> . fxlib</span><span class="sxs-lookup"><span data-stu-id="171a4-210">/Fl <MyShaderFile>.fxlib</span></span> | <span data-ttu-id="171a4-211">Affectez <MyShaderfile> la valeur à l’emplacement où vous souhaitez stocker la version de la fonction d’exportation du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="171a4-211">Set <MyShaderfile> to where you want to store the export function version of the shader.</span></span> <span data-ttu-id="171a4-212">Notez que l’extension. fxlib est uniquement destinée à faciliter l’identification.</span><span class="sxs-lookup"><span data-stu-id="171a4-212">Note the .fxlib extension is only for ease of identification.</span></span>                                                                                              |



 

### <a name="step-2-compile-the-full-shader-and-embed-the-export-function"></a><span data-ttu-id="171a4-213">Étape 2 : compiler le nuanceur complet et incorporer la fonction d’exportation</span><span class="sxs-lookup"><span data-stu-id="171a4-213">Step 2: Compile the full shader and embed the export function</span></span>

```syntax
fxc /T ps_<shadermodel> <MyShaderFile>.hlsl /D D2D_FULL_SHADER /D D2D_ENTRY=<entry> /E <entry> /setprivate <MyShaderFile>.fxlib /Fo <MyShader>.cso /Fh <MyShader>.h           
```

<span data-ttu-id="171a4-214">Pour compiler la version complète de votre nuanceur avec une version d’exportation incorporée, vous devez passer les indicateurs suivants à FXC.</span><span class="sxs-lookup"><span data-stu-id="171a4-214">To compile the full version of your shader with embedded export version, you must pass the following flags to FXC.</span></span>



|                                        |                                                                                                                                                                                                                                                                                      |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="171a4-215">**Indicateur**</span><span class="sxs-lookup"><span data-stu-id="171a4-215">**Flag**</span></span>                               | <span data-ttu-id="171a4-216">**Description**</span><span class="sxs-lookup"><span data-stu-id="171a4-216">**Description**</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="171a4-217">Commutateur <ShaderModel></span><span class="sxs-lookup"><span data-stu-id="171a4-217">/T <ShaderModel></span></span>                 | <span data-ttu-id="171a4-218">Définissez <ShaderModel> sur le profil de nuanceur de pixels approprié, tel que défini dans la [syntaxe fxc](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span><span class="sxs-lookup"><span data-stu-id="171a4-218">Set <ShaderModel> to the appropriate pixel shader profile as defined in [FXC Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span></span> <span data-ttu-id="171a4-219">Il doit s’agir du profil de nuanceur de pixels correspondant au profil de liaison spécifié à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="171a4-219">This must be the pixel shader profile corresponding to the linking profile specified in Step 1.</span></span> |
| <span data-ttu-id="171a4-220"><MyShaderFile>.hlsl</span><span class="sxs-lookup"><span data-stu-id="171a4-220"><MyShaderFile>.hlsl</span></span>              | <span data-ttu-id="171a4-221">Définissez <MyShaderFile> sur le nom du fichier HLSL.</span><span class="sxs-lookup"><span data-stu-id="171a4-221">Set <MyShaderFile> to the name of the HLSL file.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="171a4-222">/D D2D \_ - \_ nuanceur complet</span><span class="sxs-lookup"><span data-stu-id="171a4-222">/D D2D\_FULL\_SHADER</span></span>                   | <span data-ttu-id="171a4-223">Cette définition indique à FXC de compiler la version complète du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="171a4-223">This definition instructs FXC to compile the full version of the shader.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="171a4-224">/D ( \_ entrée D2D) =<entry></span><span class="sxs-lookup"><span data-stu-id="171a4-224">/D D2D\_ENTRY=<entry></span></span>            | <span data-ttu-id="171a4-225">Définissez <entry> sur le nom du point d’entrée HLSL que vous avez défini à l’intérieur de la \_ \_ macro entrée () D2D.</span><span class="sxs-lookup"><span data-stu-id="171a4-225">Set <entry> to the name of the HLSL entry point you defined inside the D2D\_PS\_ENTRY() macro.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="171a4-226">/E <entry></span><span class="sxs-lookup"><span data-stu-id="171a4-226">/E <entry></span></span>                       | <span data-ttu-id="171a4-227">Définissez <entry> sur le nom du point d’entrée HLSL que vous avez défini à l’intérieur de la \_ \_ macro entrée () D2D.</span><span class="sxs-lookup"><span data-stu-id="171a4-227">Set <entry> to the name of the HLSL entry point you defined inside the D2D\_PS\_ENTRY() macro.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="171a4-228">/SetPrivate <MyShaderFile> . fxlib</span><span class="sxs-lookup"><span data-stu-id="171a4-228">/setprivate <MyShaderFile>.fxlib</span></span> | <span data-ttu-id="171a4-229">Cet argument indique à FXC d’incorporer le nuanceur de fonction d’exportation généré à l’étape 1 dans la \_ zone de données privées de l’objet BLOB D3D \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="171a4-229">This argument instructs FXC to embed the export function shader generated in step 1 into the D3D\_BLOB\_PRIVATE\_DATA area.</span></span>                                                                                                                                                          |
| <span data-ttu-id="171a4-230">/FO <MyShader> . CSO</span><span class="sxs-lookup"><span data-stu-id="171a4-230">/Fo <MyShader>.cso</span></span>               | <span data-ttu-id="171a4-231">Affectez <MyShader> la valeur à l’emplacement où vous souhaitez stocker le nuanceur compilé final et combiné.</span><span class="sxs-lookup"><span data-stu-id="171a4-231">Set <MyShader> to where you want to store the final, combined compiled shader.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="171a4-232">/FH <MyShader> . h</span><span class="sxs-lookup"><span data-stu-id="171a4-232">/Fh <MyShader>.h</span></span>                 | <span data-ttu-id="171a4-233">Définissez <MyShader> sur l’emplacement où vous souhaitez stocker l’en-tête combiné final.</span><span class="sxs-lookup"><span data-stu-id="171a4-233">Set <MyShader> to where you want to store the final, combined header.</span></span>                                                                                                                                                                                                          |



 

## <a name="export-function-specifications"></a><span data-ttu-id="171a4-234">Exporter les spécifications de fonction</span><span class="sxs-lookup"><span data-stu-id="171a4-234">Export function specifications</span></span>

<span data-ttu-id="171a4-235">Il est possible, bien que cela ne soit pas recommandé, de créer un nuanceur d’effets compatible sans utiliser les applications d’assistance fournies par D2D.</span><span class="sxs-lookup"><span data-stu-id="171a4-235">It is possible – though not recommended – to author a compatible effect shader without using the D2D-provided helpers.</span></span> <span data-ttu-id="171a4-236">Vous devez veiller à ce que les signatures de l’entrée de la fonction de nuanceur et de l’exportation complète soient conformes aux spécifications D2D.</span><span class="sxs-lookup"><span data-stu-id="171a4-236">Care must be taken to ensure that both the full shader and export function input signatures conform to D2D specifications.</span></span>

<span data-ttu-id="171a4-237">Les spécifications des nuanceurs complets sont identiques à celles des versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="171a4-237">The specifications for full shaders are the same as earlier Windows versions.</span></span> <span data-ttu-id="171a4-238">Brièvement, les paramètres d’entrée de nuanceur de pixels doivent être \_ position de SV, position de scène \_ et une seule texcoord d’entrée par effet.</span><span class="sxs-lookup"><span data-stu-id="171a4-238">Briefly, the pixel shader input parameters must be SV\_POSITION, SCENE\_POSITION, and one TEXCOORD per effect input.</span></span>

<span data-ttu-id="171a4-239">Pour la fonction d’exportation, la fonction doit retourner un float4 et ses entrées doivent être de l’un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="171a4-239">For the export function, the function must return a float4 and its inputs must be one of the following types:</span></span>

-   <span data-ttu-id="171a4-240">Entrée simple</span><span class="sxs-lookup"><span data-stu-id="171a4-240">Simple input</span></span>

    ```syntax
    float4 d2d_inputN : INPUTN         
    ```

    <span data-ttu-id="171a4-241">Pour les entrées simples, D2D insère un exemple de fonction entre la texture d’entrée et la fonction de nuanceur, ou l’entrée est fournie par la sortie d’une autre fonction de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="171a4-241">For simple inputs, D2D will either insert a Sample function between the input texture and shader function, or the input will be provided by the output of another shader function.</span></span>

-   <span data-ttu-id="171a4-242">Entrée complexe</span><span class="sxs-lookup"><span data-stu-id="171a4-242">Complex input</span></span>

    ```syntax
    float4 d2d_uvN  : TEXCOORDN                
    ```

    <span data-ttu-id="171a4-243">Pour les entrées complexes, D2D passera uniquement une coordonnée de texture comme décrit dans la documentation de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="171a4-243">For complex inputs, D2D will only pass a texture coordinate as described in Windows 8 documentation.</span></span>

-   <span data-ttu-id="171a4-244">Emplacement de sortie</span><span class="sxs-lookup"><span data-stu-id="171a4-244">Output location</span></span>

    ```syntax
    float4 d2d_posScene : SCENE_POSITION                
    ```

    <span data-ttu-id="171a4-245">Une seule entrée de position de scène \_ peut être définie.</span><span class="sxs-lookup"><span data-stu-id="171a4-245">Only one SCENE\_POSITION input can be defined.</span></span> <span data-ttu-id="171a4-246">Ce paramètre doit être inclus uniquement lorsque cela est nécessaire, car une seule fonction par nuanceur lié peut utiliser ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="171a4-246">This parameter should only be included when necessary, since only one function per linked shader can utilize this parameter.</span></span>

<span data-ttu-id="171a4-247">La sémantique doit être définie comme ci-dessus, car D2D inspectera la sémantique pour décider comment lier des fonctions ensemble.</span><span class="sxs-lookup"><span data-stu-id="171a4-247">The semantics must be defined as above, as D2D will inspect the semantics to decide how to link functions together.</span></span> <span data-ttu-id="171a4-248">Si une entrée de fonction ne correspond pas à l’un des types ci-dessus, la fonction est rejetée pour la liaison de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="171a4-248">If any function input does not match one of the above types, the function will be rejected for shader linking.</span></span>

## <a name="related-topics"></a><span data-ttu-id="171a4-249">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="171a4-249">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="171a4-250">Applications auxiliaires HLSL</span><span class="sxs-lookup"><span data-stu-id="171a4-250">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> <dt>

[<span data-ttu-id="171a4-251">Interface ID3D11Linker</span><span class="sxs-lookup"><span data-stu-id="171a4-251">ID3D11Linker interface</span></span>](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)
</dt> <dt>

[<span data-ttu-id="171a4-252">Interface ID3D11FunctionLinkingGraph</span><span class="sxs-lookup"><span data-stu-id="171a4-252">ID3D11FunctionLinkingGraph interface</span></span>](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)
</dt> </dl>

 

 