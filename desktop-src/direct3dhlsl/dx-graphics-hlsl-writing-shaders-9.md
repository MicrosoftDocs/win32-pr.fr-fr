---
title: Écriture de nuanceurs HLSL dans Direct3D 9
description: Écriture de nuanceurs HLSL dans Direct3D 9
ms.assetid: 7db6b264-c96c-4298-9b8a-d0c488390e4e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 64a64d08518cb987850c87da3fb19c264519a7f7
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335383"
---
# <a name="writing-hlsl-shaders-in-direct3d-9"></a><span data-ttu-id="17407-103">Écriture de nuanceurs HLSL dans Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="17407-103">Writing HLSL Shaders in Direct3D 9</span></span>

-   [<span data-ttu-id="17407-104">Concepts de base des nuanceurs vertex</span><span class="sxs-lookup"><span data-stu-id="17407-104">Vertex-Shader Basics</span></span>](#vertex-shader-basics)
-   [<span data-ttu-id="17407-105">Notions de base des nuanceurs de pixels</span><span class="sxs-lookup"><span data-stu-id="17407-105">Pixel-Shader Basics</span></span>](#pixel-shader-basics)
    -   [<span data-ttu-id="17407-106">État de la texture et des États de l’échantillonneur</span><span class="sxs-lookup"><span data-stu-id="17407-106">Texture Stage and Sampler States</span></span>](#texture-stage-and-sampler-states)
    -   [<span data-ttu-id="17407-107">Entrées de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="17407-107">Pixel Shader Inputs</span></span>](#pixel-shader-inputs)
    -   [<span data-ttu-id="17407-108">Sorties de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="17407-108">Pixel Shader Outputs</span></span>](#pixel-shader-outputs)
-   [<span data-ttu-id="17407-109">Entrées de nuanceur et variables de nuanceur</span><span class="sxs-lookup"><span data-stu-id="17407-109">Shader Inputs and Shader Variables</span></span>](#shader-inputs-and-shader-variables)
    -   [<span data-ttu-id="17407-110">Déclaration de variables de nuanceur</span><span class="sxs-lookup"><span data-stu-id="17407-110">Declaring Shader Variables</span></span>](#declaring-shader-variables)
    -   [<span data-ttu-id="17407-111">Entrées uniformes de nuanceur</span><span class="sxs-lookup"><span data-stu-id="17407-111">Uniform Shader Inputs</span></span>](#uniform-shader-inputs)
    -   [<span data-ttu-id="17407-112">Variation des entrées et de la sémantique des nuanceurs</span><span class="sxs-lookup"><span data-stu-id="17407-112">Varying Shader Inputs and Semantics</span></span>](#varying-shader-inputs-and-semantics)
    -   [<span data-ttu-id="17407-113">Échantillonneurs et objets texture</span><span class="sxs-lookup"><span data-stu-id="17407-113">Samplers and Texture Objects</span></span>](#samplers-and-texture-objects)
-   [<span data-ttu-id="17407-114">Écriture de fonctions</span><span class="sxs-lookup"><span data-stu-id="17407-114">Writing Functions</span></span>](#writing-functions)
-   [<span data-ttu-id="17407-115">Contrôle de Flow</span><span class="sxs-lookup"><span data-stu-id="17407-115">Flow Control</span></span>](#flow-control)
-   [<span data-ttu-id="17407-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="17407-116">Related topics</span></span>](#related-topics)

## <a name="vertex-shader-basics"></a><span data-ttu-id="17407-117">Notions de base Vertex-Shader</span><span class="sxs-lookup"><span data-stu-id="17407-117">Vertex-Shader Basics</span></span>

<span data-ttu-id="17407-118">En cas de fonctionnement, un nuanceur de sommet programmable remplace le traitement de vertex effectué par le pipeline de graphiques Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="17407-118">When in operation, a programmable vertex shader replaces the vertex processing done by the Microsoft Direct3D graphics pipeline.</span></span> <span data-ttu-id="17407-119">Lors de l’utilisation d’un nuanceur de sommets, les informations d’État relatives aux opérations de transformation et d’éclairage sont ignorées par le pipeline de fonction fixe.</span><span class="sxs-lookup"><span data-stu-id="17407-119">While using a vertex shader, state information regarding transformation and lighting operations is ignored by the fixed function pipeline.</span></span> <span data-ttu-id="17407-120">Lorsque le nuanceur de sommets est désactivé et que le traitement de fonction fixe est retourné, tous les paramètres d’État actuels s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="17407-120">When the vertex shader is disabled and fixed function processing is returned, all current state settings apply.</span></span>

<span data-ttu-id="17407-121">Le pavage des primitives d’ordre élevé doit être effectué avant l’exécution du nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="17407-121">Tessellation of high-order primitives should be done before the vertex shader executes.</span></span> <span data-ttu-id="17407-122">Les implémentations qui effectuent un pavage de surface après le traitement du nuanceur doivent le faire d’une façon qui n’est pas apparente à l’application et au code du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="17407-122">Implementations that perform surface tessellation after the shader processing must do so in a way that is not apparent to the application and shader code.</span></span>

<span data-ttu-id="17407-123">Au minimum, un nuanceur de sommets doit sortir la position du vertex dans un espace de clip homogène.</span><span class="sxs-lookup"><span data-stu-id="17407-123">As a minimum, a vertex shader must output vertex position in homogeneous clip space.</span></span> <span data-ttu-id="17407-124">Le nuanceur de sommets peut éventuellement produire des coordonnées de texture, une couleur de vertex, un éclairage de vertex, des facteurs de brouillard, etc.</span><span class="sxs-lookup"><span data-stu-id="17407-124">Optionally, the vertex shader can output texture coordinates, vertex color, vertex lighting, fog factors, and so on.</span></span>

## <a name="pixel-shader-basics"></a><span data-ttu-id="17407-125">Notions de base Pixel-Shader</span><span class="sxs-lookup"><span data-stu-id="17407-125">Pixel-Shader Basics</span></span>

<span data-ttu-id="17407-126">Le traitement des pixels est effectué par les nuanceurs de pixels sur des pixels individuels.</span><span class="sxs-lookup"><span data-stu-id="17407-126">Pixel processing is performed by pixel shaders on individual pixels.</span></span> <span data-ttu-id="17407-127">Les nuanceurs de pixels fonctionnent de concert avec les nuanceurs de vertex. la sortie d’un nuanceur de sommets fournit les entrées d’un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="17407-127">Pixel shaders work in concert with vertex shaders; the output of a vertex shader provides the inputs for a pixel shader.</span></span> <span data-ttu-id="17407-128">D’autres opérations de pixel (fusion de brouillard, opérations de stencil et fusion de cibles de rendu) se produisent après l’exécution du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="17407-128">Other pixel operations (fog blending, stencil operations, and render-target blending) occur after execution of the shader.</span></span>

### <a name="texture-stage-and-sampler-states"></a><span data-ttu-id="17407-129">État de la texture et des États de l’échantillonneur</span><span class="sxs-lookup"><span data-stu-id="17407-129">Texture Stage and Sampler States</span></span>

<span data-ttu-id="17407-130">Un nuanceur de pixels remplace complètement la fonctionnalité de fusion de pixels spécifiée par le mélangeur à plusieurs textures, y compris les opérations précédemment définies par les États de l’étape de texture.</span><span class="sxs-lookup"><span data-stu-id="17407-130">A pixel shader completely replaces the pixel-blending functionality specified by the multi-texture blender including operations previously defined by the texture stage states.</span></span> <span data-ttu-id="17407-131">Les opérations de filtrage et d’échantillonnage de texture qui étaient contrôlées par les États de l’étape de texture standard pour la minimisation, le grossissement, le filtrage MIP et les modes d’adressage de renvoi à la ligne peuvent être initialisées dans les nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="17407-131">Texture sampling and filtering operations which were controlled by the standard texture stage states for minification, magnification, mip filtering, and the wrap addressing modes, can be initialized in shaders.</span></span> <span data-ttu-id="17407-132">L’application est libre de modifier ces États sans nécessiter la régénération du nuanceur actuellement lié.</span><span class="sxs-lookup"><span data-stu-id="17407-132">The application is free to change these states without requiring the regeneration of the currently bound shader.</span></span> <span data-ttu-id="17407-133">La définition de l’État peut être simplifiée si vos nuanceurs sont conçus dans un même but.</span><span class="sxs-lookup"><span data-stu-id="17407-133">Setting state can be made even easier if your shaders are designed within an effect.</span></span>

### <a name="pixel-shader-inputs"></a><span data-ttu-id="17407-134">Entrées de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="17407-134">Pixel Shader Inputs</span></span>

<span data-ttu-id="17407-135">Pour les versions de nuanceur de pixels PS \_ 1 \_ 1-PS \_ 2 \_ 0, les couleurs diffuses et spéculaires sont saturées (bloquées) dans la plage de 0 à 1 avant d’être utilisées par le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="17407-135">For pixel shader versions ps\_1\_1 - ps\_2\_0, diffuse and specular colors are saturated (clamped) in the range 0 to 1 before use by the shader.</span></span>

<span data-ttu-id="17407-136">Les valeurs de couleur entrées dans le nuanceur de pixels sont supposées être correctes, mais cela n’est pas garanti (pour tout le matériel).</span><span class="sxs-lookup"><span data-stu-id="17407-136">Color values input to the pixel shader are assumed to be perspective correct, but this is not guaranteed (for all hardware).</span></span> <span data-ttu-id="17407-137">Les couleurs échantillonnées à partir des coordonnées de texture sont répétées de manière correcte et sont ancrées à la plage de 0 à 1 pendant l’itération.</span><span class="sxs-lookup"><span data-stu-id="17407-137">Colors sampled from texture coordinates are iterated in a perspective correct manner, and are clamped to the 0 to 1 range during iteration.</span></span>

### <a name="pixel-shader-outputs"></a><span data-ttu-id="17407-138">Sorties de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="17407-138">Pixel Shader Outputs</span></span>

<span data-ttu-id="17407-139">Pour les versions de nuanceur de pixels PS \_ 1 \_ 1-PS \_ 1 \_ 4, le résultat émis par le nuanceur de pixels est le contenu de Register R0.</span><span class="sxs-lookup"><span data-stu-id="17407-139">For pixel shader versions ps\_1\_1 - ps\_1\_4, the result emitted by the pixel shader is the contents of register r0.</span></span> <span data-ttu-id="17407-140">Quel que soit l’moment où le nuanceur termine le traitement, il est envoyé à l’étape de brouillard et au mélangeur de cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="17407-140">Whatever it contains when the shader completes processing is sent to the fog stage and render-target blender.</span></span>

<span data-ttu-id="17407-141">Pour les versions de nuanceur de pixels PS \_ 2 \_ 0 et ultérieures, la couleur de sortie est émise à partir de OC0-oC4.</span><span class="sxs-lookup"><span data-stu-id="17407-141">For pixel shader versions ps\_2\_0 and above, output color is emitted from oC0 - oC4.</span></span>

## <a name="shader-inputs-and-shader-variables"></a><span data-ttu-id="17407-142">Entrées de nuanceur et variables de nuanceur</span><span class="sxs-lookup"><span data-stu-id="17407-142">Shader Inputs and Shader Variables</span></span>

-   [<span data-ttu-id="17407-143">Déclaration de variables de nuanceur</span><span class="sxs-lookup"><span data-stu-id="17407-143">Declaring Shader Variables</span></span>](#declaring-shader-variables)
-   [<span data-ttu-id="17407-144">Entrées uniformes de nuanceur</span><span class="sxs-lookup"><span data-stu-id="17407-144">Uniform Shader Inputs</span></span>](#uniform-shader-inputs)
-   [<span data-ttu-id="17407-145">Variation des entrées et de la sémantique des nuanceurs</span><span class="sxs-lookup"><span data-stu-id="17407-145">Varying Shader Inputs and Semantics</span></span>](#varying-shader-inputs-and-semantics)
-   [<span data-ttu-id="17407-146">Échantillonneurs et objets texture</span><span class="sxs-lookup"><span data-stu-id="17407-146">Samplers and Texture Objects</span></span>](#samplers-and-texture-objects)

### <a name="declaring-shader-variables"></a><span data-ttu-id="17407-147">Déclaration de variables de nuanceur</span><span class="sxs-lookup"><span data-stu-id="17407-147">Declaring Shader Variables</span></span>

<span data-ttu-id="17407-148">La déclaration de variable la plus simple comprend un type et un nom de variable, par exemple cette déclaration à virgule flottante :</span><span class="sxs-lookup"><span data-stu-id="17407-148">The simplest variable declaration includes a type and a variable name, such as this floating-point declaration:</span></span>


```
float fVar;
```



<span data-ttu-id="17407-149">Vous pouvez initialiser une variable dans la même instruction.</span><span class="sxs-lookup"><span data-stu-id="17407-149">You can initialize a variable in the same statement.</span></span>


```
float fVar = 3.1f;
```



<span data-ttu-id="17407-150">Un tableau de variables peut être déclaré,</span><span class="sxs-lookup"><span data-stu-id="17407-150">An array of variables can be declared,</span></span>


```
int iVar[3];
```



<span data-ttu-id="17407-151">ou déclarés et initialisés dans la même instruction.</span><span class="sxs-lookup"><span data-stu-id="17407-151">or declared and initialized in the same statement.</span></span>


```
int iVar[3] = {1,2,3};
```



<span data-ttu-id="17407-152">Voici quelques déclarations qui illustrent la plupart des caractéristiques des variables HLSL (High-Level Shader Language) :</span><span class="sxs-lookup"><span data-stu-id="17407-152">Here are a few declarations that demonstrate many of the characteristics of high-level shader language (HLSL) variables:</span></span>


```
float4 color;
uniform float4 position : POSITION; 
const float4 lightDirection = {0,0,1};
```



<span data-ttu-id="17407-153">Les déclarations de données peuvent utiliser n’importe quel type valide, y compris :</span><span class="sxs-lookup"><span data-stu-id="17407-153">Data declarations can use any valid type including:</span></span>

-   [<span data-ttu-id="17407-154">Types de données (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="17407-154">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
-   [<span data-ttu-id="17407-155">Type de vecteur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="17407-155">Vector Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-vector.md)
-   [<span data-ttu-id="17407-156">Type de matrice (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="17407-156">Matrix Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-matrix.md)
-   [<span data-ttu-id="17407-157">Type de nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="17407-157">Shader Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-shader.md)
-   [<span data-ttu-id="17407-158">Type d’échantillonneur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="17407-158">Sampler Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-sampler.md)
-   [<span data-ttu-id="17407-159">Type défini par l’utilisateur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="17407-159">User-Defined Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-user-defined.md)

<span data-ttu-id="17407-160">Un nuanceur peut avoir des variables, des arguments et des fonctions de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="17407-160">A shader can have top-level variables, arguments, and functions.</span></span>


```
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```



<span data-ttu-id="17407-161">Les variables de niveau supérieur sont déclarées en dehors de toutes les fonctions.</span><span class="sxs-lookup"><span data-stu-id="17407-161">Top-level variables are declared outside of all functions.</span></span> <span data-ttu-id="17407-162">Les arguments de niveau supérieur sont des paramètres d’une fonction de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="17407-162">Top-level arguments are parameters to a top-level function.</span></span> <span data-ttu-id="17407-163">Une fonction de niveau supérieur est toute fonction appelée par l’application (par opposition à une fonction qui est appelée par une autre fonction).</span><span class="sxs-lookup"><span data-stu-id="17407-163">A top-level function is any function called by the application (as opposed to a function that is called by another function).</span></span>

### <a name="uniform-shader-inputs"></a><span data-ttu-id="17407-164">Entrées uniformes de nuanceur</span><span class="sxs-lookup"><span data-stu-id="17407-164">Uniform Shader Inputs</span></span>

<span data-ttu-id="17407-165">Les nuanceurs vertex et de pixels acceptent deux types de données d’entrée : variable et uniforme.</span><span class="sxs-lookup"><span data-stu-id="17407-165">Vertex and pixel shaders accept two kinds of input data: varying and uniform.</span></span> <span data-ttu-id="17407-166">L’entrée variable correspond aux données qui sont propres à chaque exécution du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="17407-166">The varying input is the data that is unique to each execution of the shader.</span></span> <span data-ttu-id="17407-167">Pour un nuanceur de sommets, les données variables (par exemple, position, normal, etc.) proviennent des flux de vertex.</span><span class="sxs-lookup"><span data-stu-id="17407-167">For a vertex shader, the varying data (for example: position, normal, etc.) comes from the vertex streams.</span></span> <span data-ttu-id="17407-168">Les données uniformes (par exemple, les couleurs matérielles, les transformations universelles, etc.) sont constantes pour les exécutions multiples d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="17407-168">The uniform data (for example: material color, world transform, etc.) is constant for multiple executions of a shader.</span></span> <span data-ttu-id="17407-169">Pour ceux qui sont familiarisés avec les modèles de nuanceur d’assembly, les données uniformes sont spécifiées par des registres constants et des données variables par les registres v et t.</span><span class="sxs-lookup"><span data-stu-id="17407-169">For those familiar with the assembly shader models, uniform data is specified by constant registers and varying data by the v and t registers.</span></span>

<span data-ttu-id="17407-170">Les données uniformes peuvent être spécifiées par deux méthodes.</span><span class="sxs-lookup"><span data-stu-id="17407-170">Uniform data can be specified by two methods.</span></span> <span data-ttu-id="17407-171">La méthode la plus courante consiste à déclarer des variables globales et à les utiliser dans un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="17407-171">The most common method is to declare global variables and use them within a shader.</span></span> <span data-ttu-id="17407-172">Toute utilisation de variables globales dans un nuanceur entraîne l’ajout de cette variable à la liste des variables uniformes requises par ce nuanceur.</span><span class="sxs-lookup"><span data-stu-id="17407-172">Any use of global variables within a shader will result in adding that variable to the list of uniform variables required by that shader.</span></span> <span data-ttu-id="17407-173">La deuxième méthode consiste à marquer un paramètre d’entrée de la fonction de nuanceur de niveau supérieur comme uniforme.</span><span class="sxs-lookup"><span data-stu-id="17407-173">The second method is to mark an input parameter of the top-level shader function as uniform.</span></span> <span data-ttu-id="17407-174">Ce marquage spécifie que la variable donnée doit être ajoutée à la liste des variables uniformes.</span><span class="sxs-lookup"><span data-stu-id="17407-174">This marking specifies that the given variable should be added to the list of uniform variables.</span></span>

<span data-ttu-id="17407-175">Les variables uniformes utilisées par un nuanceur sont communiquées à l’application via la table constante.</span><span class="sxs-lookup"><span data-stu-id="17407-175">Uniform variables used by a shader are communicated back to the application via the constant table.</span></span> <span data-ttu-id="17407-176">La table de constantes est le nom de la table de symboles qui définit la façon dont les variables uniformes utilisées par un nuanceur s’intègrent aux registres de constantes.</span><span class="sxs-lookup"><span data-stu-id="17407-176">The constant table is the name for the symbol table that defines how the uniform variables used by a shader fit into the constant registers.</span></span> <span data-ttu-id="17407-177">Les paramètres de fonction uniforme apparaissent dans le tableau constant précédé d’un signe dollar ($), contrairement aux variables globales.</span><span class="sxs-lookup"><span data-stu-id="17407-177">The uniform function parameters appear in the constant table prepended with a dollar sign ($), unlike the global variables.</span></span> <span data-ttu-id="17407-178">Le signe dollar est nécessaire pour éviter les conflits de noms entre les entrées uniformes locales et les variables globales du même nom.</span><span class="sxs-lookup"><span data-stu-id="17407-178">The dollar sign is required to avoid name collisions between local uniform inputs and global variables of the same name.</span></span>

<span data-ttu-id="17407-179">La table constante contient les emplacements de Registre constants de toutes les variables uniformes utilisées par le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="17407-179">The constant table contains the constant register locations of all uniform variables used by the shader.</span></span> <span data-ttu-id="17407-180">Le tableau comprend également les informations de type et la valeur par défaut, si elles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="17407-180">The table also includes the type information and the default value, if specified.</span></span>

### <a name="varying-shader-inputs-and-semantics"></a><span data-ttu-id="17407-181">Variation des entrées et de la sémantique des nuanceurs</span><span class="sxs-lookup"><span data-stu-id="17407-181">Varying Shader Inputs and Semantics</span></span>

<span data-ttu-id="17407-182">La variation des paramètres d’entrée (d’une fonction de nuanceur de niveau supérieur) doit être marquée avec un mot clé sémantique ou uniforme, indiquant que la valeur est constante pour l’exécution du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="17407-182">Varying input parameters (of a top-level shader function) must be marked either with a semantic or uniform keyword indicating the value is constant for the execution of the shader.</span></span> <span data-ttu-id="17407-183">Si une entrée de nuanceur de niveau supérieur n’est pas marquée avec un mot clé sémantique ou uniforme, le nuanceur ne pourra pas être compilé.</span><span class="sxs-lookup"><span data-stu-id="17407-183">If a top-level shader input is not marked with a semantic or uniform keyword, then the shader will fail to compile.</span></span>

<span data-ttu-id="17407-184">La sémantique d’entrée est un nom utilisé pour lier l’entrée donnée à une sortie de la partie précédente du pipeline Graphics.</span><span class="sxs-lookup"><span data-stu-id="17407-184">The input semantic is a name used to link the given input to an output of the previous part of the graphics pipeline.</span></span> <span data-ttu-id="17407-185">Par exemple, le POSITION0 sémantique d’entrée est utilisé par les nuanceurs de vertex pour spécifier l’emplacement auquel les données de position de la mémoire tampon de vertex doivent être liées.</span><span class="sxs-lookup"><span data-stu-id="17407-185">For example, the input semantic POSITION0 is used by the vertex shaders to specify where the position data from the vertex buffer should be linked.</span></span>

<span data-ttu-id="17407-186">Les nuanceurs de pixels et vertex ont des jeux de sémantiques d’entrée différents en raison des différentes parties du pipeline graphique qui alimentent chaque unité de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="17407-186">Pixel and vertex shaders have different sets of input semantics due to the different parts of the graphics pipeline that feed into each shader unit.</span></span> <span data-ttu-id="17407-187">La sémantique d’entrée du nuanceur de sommets décrit les informations par vertex (par exemple, position, normal, coordonnées de texture, couleur, tangente, binormal, etc.) à charger à partir d’une mémoire tampon de vertex dans un format qui peut être consommé par le nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="17407-187">Vertex shader input semantics describe the per-vertex information (for example: position, normal, texture coordinates, color, tangent, binormal, etc.) to be loaded from a vertex buffer into a form that can be consumed by the vertex shader.</span></span> <span data-ttu-id="17407-188">La sémantique d’entrée est directement mappée à l’utilisation de la déclaration de vertex et à l’index d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="17407-188">The input semantics directly map to the vertex declaration usage and the usage index.</span></span>

<span data-ttu-id="17407-189">La sémantique d’entrée du nuanceur de pixels décrit les informations fournies par pixel par l’unité de rastérisation.</span><span class="sxs-lookup"><span data-stu-id="17407-189">Pixel shader input semantics describe the information that is provided per pixel by the rasterization unit.</span></span> <span data-ttu-id="17407-190">Les données sont générées par l’interpolation entre les sorties du nuanceur de sommets pour chaque vertex de la primitive actuelle.</span><span class="sxs-lookup"><span data-stu-id="17407-190">The data is generated by interpolating between outputs of the vertex shader for each vertex of the current primitive.</span></span> <span data-ttu-id="17407-191">La sémantique d’entrée de nuanceur de pixels de base lie la couleur de sortie et les informations de coordonnées de texture aux paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="17407-191">The basic pixel shader input semantics link the output color and texture coordinate information to input parameters.</span></span>

<span data-ttu-id="17407-192">La sémantique d’entrée peut être assignée à l’entrée de nuanceur par deux méthodes :</span><span class="sxs-lookup"><span data-stu-id="17407-192">Input semantics can be assigned to shader input by two methods:</span></span>

-   <span data-ttu-id="17407-193">Ajout d’un signe deux-points et du nom sémantique à la déclaration du paramètre.</span><span class="sxs-lookup"><span data-stu-id="17407-193">Appending a colon and the semantic name to the parameter declaration.</span></span>
-   <span data-ttu-id="17407-194">Définition d’une structure d’entrée avec la sémantique d’entrée assignée à chaque membre de la structure.</span><span class="sxs-lookup"><span data-stu-id="17407-194">Defining an input structure with input semantics assigned to each structure member.</span></span>

<span data-ttu-id="17407-195">Les nuanceurs vertex et de pixels fournissent des données de sortie à l’étape de canalisation Graphics suivante.</span><span class="sxs-lookup"><span data-stu-id="17407-195">Vertex and pixel shaders provide output data to the subsequent graphics pipeline stage.</span></span> <span data-ttu-id="17407-196">La sémantique de sortie est utilisée pour spécifier la façon dont les données générées par le nuanceur doivent être liées aux entrées de l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="17407-196">Output semantics are used to specify how data generated by the shader should be linked to the inputs of the next stage.</span></span> <span data-ttu-id="17407-197">Par exemple, la sémantique de sortie d’un nuanceur de sommets est utilisée pour lier les sorties des interpolateurs dans le rastériseur afin de générer les données d’entrée pour le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="17407-197">For example, the output semantics for a vertex shader are used to link the outputs of the interpolators in the rasterizer to generate the input data for the pixel shader.</span></span> <span data-ttu-id="17407-198">Les sorties de nuanceur de pixels sont les valeurs fournies à l’unité de fusion alpha pour chacune des cibles de rendu ou la valeur de profondeur écrite dans le tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="17407-198">The pixel shader outputs are the values provided to the alpha blending unit for each of the render targets or the depth value written to the depth buffer.</span></span>

<span data-ttu-id="17407-199">La sémantique de sortie du nuanceur de sommets est utilisée pour lier le nuanceur à la fois au nuanceur de pixels et à l’étape de rastérisation.</span><span class="sxs-lookup"><span data-stu-id="17407-199">Vertex shader output semantics are used to link the shader both to the pixel shader and to the rasterizer stage.</span></span> <span data-ttu-id="17407-200">Un nuanceur de sommets qui est consommé par le rastériseur et qui n’est pas exposé au nuanceur de pixels doit générer des données de position au minimum.</span><span class="sxs-lookup"><span data-stu-id="17407-200">A vertex shader that is consumed by the rasterizer and not exposed to the pixel shader must generate position data as a minimum.</span></span> <span data-ttu-id="17407-201">Les nuanceurs de sommets qui génèrent des coordonnées de texture et des données de couleur fournissent ces données à un nuanceur de pixels une fois l’interpolation effectuée.</span><span class="sxs-lookup"><span data-stu-id="17407-201">Vertex shaders that generate texture coordinate and color data provide that data to a pixel shader after interpolation is done.</span></span>

<span data-ttu-id="17407-202">La sémantique de sortie du nuanceur de pixels lie les couleurs de sortie d’un nuanceur de pixels à la cible de rendu appropriée.</span><span class="sxs-lookup"><span data-stu-id="17407-202">Pixel shader output semantics bind the output colors of a pixel shader with the correct render target.</span></span> <span data-ttu-id="17407-203">La couleur de sortie du nuanceur de pixels est liée à l’étape de fusion alpha, qui détermine la façon dont les cibles de rendu de destination sont modifiées.</span><span class="sxs-lookup"><span data-stu-id="17407-203">The pixel shader output color is linked to the alpha blend stage, which determines how the destination render targets are modified.</span></span> <span data-ttu-id="17407-204">La sortie de la profondeur du nuanceur de pixels peut être utilisée pour modifier les valeurs de profondeur de destination à l’emplacement de trame actuel.</span><span class="sxs-lookup"><span data-stu-id="17407-204">The pixel shader depth output can be used to change the destination depth values at the current raster location.</span></span> <span data-ttu-id="17407-205">La sortie de profondeur et plusieurs cibles de rendu sont uniquement prises en charge avec certains modèles de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="17407-205">The depth output and multiple render targets are only supported with some shader models.</span></span>

<span data-ttu-id="17407-206">La syntaxe de la sémantique de sortie est identique à celle de la spécification de la sémantique d’entrée.</span><span class="sxs-lookup"><span data-stu-id="17407-206">The syntax for output semantics is identical to the syntax for specifying input semantics.</span></span> <span data-ttu-id="17407-207">La sémantique peut être spécifiée directement sur les paramètres déclarés en tant que paramètres « out » ou assignées pendant la définition d’une structure qui est retournée en tant que paramètre « out » ou valeur de retour d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="17407-207">The semantics can be either specified directly on parameters declared as "out" parameters or assigned during the definition of a structure that either returned as an "out" parameter or the return value of a function.</span></span>

<span data-ttu-id="17407-208">La sémantique identifie l’origine des données.</span><span class="sxs-lookup"><span data-stu-id="17407-208">Semantics identify where data comes from.</span></span> <span data-ttu-id="17407-209">Les sémantiques sont des identificateurs facultatifs qui identifient les entrées et les sorties du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="17407-209">Semantics are optional identifiers that identify shader inputs and outputs.</span></span> <span data-ttu-id="17407-210">Les sémantiques s’affichent dans l’un des trois emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="17407-210">Semantics appear in one of three places:</span></span>

-   <span data-ttu-id="17407-211">Après un membre de structure.</span><span class="sxs-lookup"><span data-stu-id="17407-211">After a structure member.</span></span>
-   <span data-ttu-id="17407-212">Après un argument dans la liste d’arguments d’entrée d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="17407-212">After an argument in a function's input argument list.</span></span>
-   <span data-ttu-id="17407-213">Après la liste d’arguments d’entrée de la fonction.</span><span class="sxs-lookup"><span data-stu-id="17407-213">After the function's input argument list.</span></span>

<span data-ttu-id="17407-214">Cet exemple utilise une structure pour fournir une ou plusieurs entrées de nuanceur de vertex, et une autre structure pour fournir une ou plusieurs sorties de nuanceur de vertex.</span><span class="sxs-lookup"><span data-stu-id="17407-214">This example uses a structure to provide one or more vertex shader inputs, and another structure to provide one or more vertex shader outputs.</span></span> <span data-ttu-id="17407-215">Chacun des membres de la structure utilise une sémantique.</span><span class="sxs-lookup"><span data-stu-id="17407-215">Each of the structure members uses a semantic.</span></span>


```
vector vClr;

struct VS_INPUT
{
    float4 vPosition : POSITION;
    float3 vNormal : NORMAL;
    float4 vBlendWeights : BLENDWEIGHT;
};

struct VS_OUTPUT
{
    float4  vPosition : POSITION;
    float4  vDiffuse : COLOR;

};

float4x4 mWld1;
float4x4 mWld2;
float4x4 mWld3;
float4x4 mWld4;

float Len;
float4 vLight;

float4x4 mTot;

VS_OUTPUT VS_Skinning_Example(const VS_INPUT v, uniform float len=100)
{
    VS_OUTPUT out;

    // Skin position (to world space)
    float3 vPosition = 
        mul(v.vPosition, (float4x3) mWld1) * v.vBlendWeights.x +
        mul(v.vPosition, (float4x3) mWld2) * v.vBlendWeights.y +
        mul(v.vPosition, (float4x3) mWld3) * v.vBlendWeights.z +
        mul(v.vPosition, (float4x3) mWld4) * v.vBlendWeights.w;
    // Skin normal (to world space)
    float3 vNormal =
        mul(v.vNormal, (float3x3) mWld1) * v.vBlendWeights.x + 
        mul(v.vNormal, (float3x3) mWld2) * v.vBlendWeights.y + 
        mul(v.vNormal, (float3x3) mWld3) * v.vBlendWeights.z + 
        mul(v.vNormal, (float3x3) mWld4) * v.vBlendWeights.w;
    
    // Output stuff
    out.vPosition    = mul(float4(vPosition + vNormal * Len, 1), mTot);
    out.vDiffuse  = dot(vLight,vNormal);

    return out;
}
```



<span data-ttu-id="17407-216">La structure d’entrée identifie les données de la mémoire tampon de vertex qui fourniront les entrées de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="17407-216">The input structure identifies the data from the vertex buffer that will provide the shader inputs.</span></span> <span data-ttu-id="17407-217">Ce nuanceur mappe les données à partir des éléments position, normal et blendweight de la mémoire tampon de vertex dans des registres de nuanceur vertex.</span><span class="sxs-lookup"><span data-stu-id="17407-217">This shader maps the data from the position, normal, and blendweight elements of the vertex buffer into vertex shader registers.</span></span> <span data-ttu-id="17407-218">Le type de données d’entrée ne doit pas nécessairement correspondre exactement au type de données de la déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="17407-218">The input data type does not have to exactly match the vertex declaration data type.</span></span> <span data-ttu-id="17407-219">Si elle ne correspond pas exactement à, les données du vertex sont automatiquement converties dans le type de données du langage HLSL lorsqu’elles sont écrites dans les registres des nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="17407-219">If it doesn't exactly match, the vertex data will automatically be converted into the HLSL's data type when it is written into the shader registers.</span></span> <span data-ttu-id="17407-220">Par exemple, si les données normales ont été définies comme étant de type UINT par l’application, elles sont converties en float3 lors de la lecture par le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="17407-220">For instance, if the normal data were defined to be of type UINT by the application, it would be converted into a float3 when read by the shader.</span></span>

<span data-ttu-id="17407-221">Si les données du flux de vertex contiennent moins de composants que le type de données de nuanceur correspondant, les composants manquants seront initialisés à 0 (à l’exception de w, qui est initialisé à 1).</span><span class="sxs-lookup"><span data-stu-id="17407-221">If the data in the vertex stream contains fewer components than the corresponding shader data type, the missing components will be initialized to 0 (except for w, which is initialized to 1).</span></span>

<span data-ttu-id="17407-222">La sémantique d’entrée est semblable aux valeurs de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span><span class="sxs-lookup"><span data-stu-id="17407-222">Input semantics are similar to the values in the [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span></span>

<span data-ttu-id="17407-223">La structure de sortie identifie les paramètres de sortie du nuanceur de sommets de position et de couleur.</span><span class="sxs-lookup"><span data-stu-id="17407-223">The output structure identifies the vertex shader output parameters of position and color.</span></span> <span data-ttu-id="17407-224">Ces sorties seront utilisées par le pipeline pour la pixellisation des triangles (en traitement primitif).</span><span class="sxs-lookup"><span data-stu-id="17407-224">These outputs will be used by the pipeline for triangle rasterization (in primitive processing).</span></span> <span data-ttu-id="17407-225">La sortie marquée comme données de position indique la position d’un vertex dans un espace homogène.</span><span class="sxs-lookup"><span data-stu-id="17407-225">The output marked as position data denotes the position of a vertex in homogeneous space.</span></span> <span data-ttu-id="17407-226">Au minimum, un nuanceur de sommets doit générer des données de position.</span><span class="sxs-lookup"><span data-stu-id="17407-226">As a minimum, a vertex shader must generate position data.</span></span> <span data-ttu-id="17407-227">La position de l’espace de l’écran est calculée après la fin du nuanceur de sommets en divisant la coordonnée (x, y, z) par w.</span><span class="sxs-lookup"><span data-stu-id="17407-227">The screen space position is computed after the vertex shader completes by dividing the (x, y, z) coordinate by w.</span></span> <span data-ttu-id="17407-228">Dans l’espace d’écran,-1 et 1 sont les valeurs x et y minimales et maximales des limites de la fenêtre d’affichage, tandis que z est utilisé pour le test de la mémoire tampon z.</span><span class="sxs-lookup"><span data-stu-id="17407-228">In screen space, -1 and 1 are the minimum and maximum x and y values of the boundaries of the viewport, while z is used for z-buffer testing.</span></span>

<span data-ttu-id="17407-229">La sémantique de sortie est également similaire aux valeurs dans [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span><span class="sxs-lookup"><span data-stu-id="17407-229">Output semantics are also similar to the values in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span></span> <span data-ttu-id="17407-230">En général, une structure de sortie pour un nuanceur de sommets peut également être utilisée comme structure d’entrée pour un nuanceur de pixels, à condition que le nuanceur de pixels ne lise pas les variables marquées avec la position, la taille du point ou la sémantique du brouillard.</span><span class="sxs-lookup"><span data-stu-id="17407-230">In general, an output structure for a vertex shader can also be used as the input structure for a pixel shader, provided the pixel shader does not read from any variable marked with the position, point size, or fog semantics.</span></span> <span data-ttu-id="17407-231">Ces sémantiques sont associées à des valeurs scalaires par vertex qui ne sont pas utilisées par un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="17407-231">These semantics are associated with per-vertex scalar values that are not used by a pixel shader.</span></span> <span data-ttu-id="17407-232">Si ces valeurs sont nécessaires pour le nuanceur de pixels, elles peuvent être copiées dans une autre variable de sortie qui utilise une sémantique de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="17407-232">If these values are needed for the pixel shader, they can be copied into another output variable that uses a pixel shader semantic.</span></span>

<span data-ttu-id="17407-233">Les variables globales sont assignées automatiquement aux registres par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="17407-233">Global variables are assigned to registers automatically by the compiler.</span></span> <span data-ttu-id="17407-234">Les variables globales sont également appelées paramètres uniformes, car le contenu de la variable est le même pour tous les pixels traités chaque fois que le nuanceur est appelé.</span><span class="sxs-lookup"><span data-stu-id="17407-234">Global variables are also called uniform parameters because the contents of the variable is the same for all pixels processed each time the shader is called.</span></span> <span data-ttu-id="17407-235">Les registres sont contenus dans la table constante, qui peut être lue à l’aide de l’interface [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) .</span><span class="sxs-lookup"><span data-stu-id="17407-235">The registers are contained in the constant table, which can be read using the [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) interface.</span></span>

<span data-ttu-id="17407-236">La sémantique d’entrée pour les nuanceurs de pixels mappe les valeurs dans des registres matériels spécifiques pour le transport entre les nuanceurs de vertex et les nuanceurs de pixels.</span><span class="sxs-lookup"><span data-stu-id="17407-236">Input semantics for pixel shaders map values into specific hardware registers for transport between vertex shaders and pixel shaders.</span></span> <span data-ttu-id="17407-237">Chaque type de registre a des propriétés spécifiques.</span><span class="sxs-lookup"><span data-stu-id="17407-237">Each register type has specific properties.</span></span> <span data-ttu-id="17407-238">Étant donné qu’il n’existe actuellement que deux sémantiques pour les coordonnées de couleur et de texture, il est courant que la plupart des données soient marquées comme une coordonnée de texture même si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="17407-238">Because there are currently only two semantics for color and texture coordinates, it is common for most data to be marked as a texture coordinate even when it is not.</span></span>

<span data-ttu-id="17407-239">Notez que la structure de sortie du nuanceur de sommets utilisait une entrée avec des données de position, ce qui n’est pas utilisé par le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="17407-239">Notice that the vertex shader output structure used an input with position data, which is not used by the pixel shader.</span></span> <span data-ttu-id="17407-240">Le langage HLSL autorise des données de sortie valides d’un nuanceur de sommets qui ne sont pas des données d’entrée valides pour un nuanceur de pixels, à condition qu’il ne soit pas référencé dans le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="17407-240">HLSL allows valid output data of a vertex shader that is not valid input data for a pixel shader, provided that it is not referenced in the pixel shader.</span></span>

<span data-ttu-id="17407-241">Les arguments d’entrée peuvent également être des tableaux.</span><span class="sxs-lookup"><span data-stu-id="17407-241">Input arguments can also be arrays.</span></span> <span data-ttu-id="17407-242">La sémantique est automatiquement incrémentée par le compilateur pour chaque élément du tableau.</span><span class="sxs-lookup"><span data-stu-id="17407-242">Semantics are automatically incremented by the compiler for each element of the array.</span></span> <span data-ttu-id="17407-243">Par exemple, considérez la déclaration explicite suivante :</span><span class="sxs-lookup"><span data-stu-id="17407-243">For instance, consider the following explicit declaration:</span></span>


```
struct VS_OUTPUT
{
    float4 Position   : POSITION;
    float3 Diffuse    : COLOR0;
    float3 Specular   : COLOR1;               
    float3 HalfVector : TEXCOORD3;
    float3 Fresnel    : TEXCOORD2;               
    float3 Reflection : TEXCOORD0;               
    float3 NoiseCoord : TEXCOORD1;               
};

float4 Sparkle(VS_OUTPUT In) : COLOR
```



<span data-ttu-id="17407-244">La déclaration explicite fournie ci-dessus équivaut à la déclaration suivante dont la sémantique est automatiquement incrémentée par le compilateur :</span><span class="sxs-lookup"><span data-stu-id="17407-244">The explicit declaration given above is equivalent to the following declaration that will have semantics automatically incremented by the compiler:</span></span>


```
float4 Sparkle(float4 Position : POSITION,
                 float3 Col[2] : COLOR0,
                 float3 Tex[4] : TEXCOORD0) : COLOR0
{
   // shader statements
   ...
```



<span data-ttu-id="17407-245">Tout comme la sémantique d’entrée, la sémantique de sortie identifie l’utilisation des données pour les données de sortie du nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="17407-245">Just like input semantics, output semantics identify data usage for pixel shader output data.</span></span> <span data-ttu-id="17407-246">De nombreux nuanceurs de pixels écrivent dans une seule couleur de sortie.</span><span class="sxs-lookup"><span data-stu-id="17407-246">Many pixel shaders write to only one output color.</span></span> <span data-ttu-id="17407-247">Les nuanceurs de pixels peuvent également écrire une valeur de profondeur dans une ou plusieurs cibles de rendu multiples en même temps (jusqu’à quatre).</span><span class="sxs-lookup"><span data-stu-id="17407-247">Pixel shaders can also write out a depth value into one or more multiple render targets at the same time (up to four).</span></span> <span data-ttu-id="17407-248">Comme les nuanceurs vertex, les nuanceurs de pixels utilisent une structure pour retourner plusieurs sorties.</span><span class="sxs-lookup"><span data-stu-id="17407-248">Like vertex shaders, pixel shaders use a structure to return more than one output.</span></span> <span data-ttu-id="17407-249">Ce nuanceur écrit 0 dans les composants de couleur, ainsi que sur le composant profondeur.</span><span class="sxs-lookup"><span data-stu-id="17407-249">This shader writes 0 to the color components, as well as to the depth component.</span></span>


```
struct PS_OUTPUT
{
    float4 Color[4] : COLOR0;
    float  Depth  : DEPTH;
};

PS_OUTPUT main(void)
{
    PS_OUTPUT out;

   // Shader statements
   ...

  // Write up to four pixel shader output colors
  out.Color[0] =  ...
  out.Color[1] =  ...
  out.Color[2] =  ...
  out.Color[3] =  ...

  // Write pixel depth 
  out.Depth =  ...

    return out;
}
```



<span data-ttu-id="17407-250">Les couleurs de sortie du nuanceur de pixels doivent être de type float4.</span><span class="sxs-lookup"><span data-stu-id="17407-250">Pixel shader output colors must be of type float4.</span></span> <span data-ttu-id="17407-251">Lors de l’écriture de plusieurs couleurs, toutes les couleurs de sortie doivent être utilisées de manière contiguë.</span><span class="sxs-lookup"><span data-stu-id="17407-251">When writing multiple colors, all output colors must be used contiguously.</span></span> <span data-ttu-id="17407-252">En d’autres termes, [COLOR1](dx-graphics-hlsl-semantics.md) ne peut pas être output, sauf si [COLOR0](dx-graphics-hlsl-semantics.md) a déjà été écrit.</span><span class="sxs-lookup"><span data-stu-id="17407-252">In other words, [COLOR1](dx-graphics-hlsl-semantics.md) cannot be an output unless [COLOR0](dx-graphics-hlsl-semantics.md) has already been written.</span></span> <span data-ttu-id="17407-253">La sortie de la profondeur du nuanceur de pixels doit être de type float1.</span><span class="sxs-lookup"><span data-stu-id="17407-253">Pixel shader depth output must be of type float1.</span></span>

### <a name="samplers-and-texture-objects"></a><span data-ttu-id="17407-254">Échantillonneurs et objets texture</span><span class="sxs-lookup"><span data-stu-id="17407-254">Samplers and Texture Objects</span></span>

<span data-ttu-id="17407-255">Un échantillonneur contient l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="17407-255">A sampler contains sampler state.</span></span> <span data-ttu-id="17407-256">L’état de l’échantillonneur spécifie la texture à échantillonner et contrôle le filtrage effectué pendant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="17407-256">Sampler state specifies the texture to be sampled, and controls the filtering that is done during sampling.</span></span> <span data-ttu-id="17407-257">Trois éléments sont nécessaires pour échantillonner une texture :</span><span class="sxs-lookup"><span data-stu-id="17407-257">Three things are required to sample a texture:</span></span>

-   <span data-ttu-id="17407-258">Une texture</span><span class="sxs-lookup"><span data-stu-id="17407-258">A texture</span></span>
-   <span data-ttu-id="17407-259">Un échantillonneur (avec l’état de l’échantillonneur)</span><span class="sxs-lookup"><span data-stu-id="17407-259">A sampler (with sampler state)</span></span>
-   <span data-ttu-id="17407-260">Une instruction d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="17407-260">A sampling instruction</span></span>

<span data-ttu-id="17407-261">Les échantillonneurs peuvent être initialisés avec les textures et l’état de l’échantillonneur comme indiqué ici :</span><span class="sxs-lookup"><span data-stu-id="17407-261">Samplers can be initialized with textures and sampler state as shown here:</span></span>


```
sampler s = sampler_state 
{ 
  texture = NULL; 
  mipfilter = LINEAR; 
};
```



<span data-ttu-id="17407-262">Voici un exemple de code pour échantillonner une texture 2D :</span><span class="sxs-lookup"><span data-stu-id="17407-262">Here's an example of the code to sample a 2D texture:</span></span>


```
texture tex0;
sampler2D s_2D;

float2 sample_2D(float2 tex : TEXCOORD0) : COLOR
{
  return tex2D(s_2D, tex);
}
```



<span data-ttu-id="17407-263">La texture est déclarée avec une variable de texture tex0.</span><span class="sxs-lookup"><span data-stu-id="17407-263">The texture is declared with a texture variable tex0.</span></span>

<span data-ttu-id="17407-264">Dans cet exemple, une variable d’échantillonnage nommée s \_ 2D est déclarée.</span><span class="sxs-lookup"><span data-stu-id="17407-264">In this example, a sampler variable named s\_2D is declared.</span></span> <span data-ttu-id="17407-265">L’échantillonneur contient l’état de l’échantillonneur à l’intérieur des accolades.</span><span class="sxs-lookup"><span data-stu-id="17407-265">The sampler contains the sampler state inside of curly braces.</span></span> <span data-ttu-id="17407-266">Cela inclut la texture qui sera échantillonnée et, éventuellement, l’état du filtre (autrement dit, les modes de renvoi à la ligne, les modes de filtre, etc.).</span><span class="sxs-lookup"><span data-stu-id="17407-266">This includes the texture that will be sampled and, optionally, the filter state (that is, wrap modes, filter modes, etc.).</span></span> <span data-ttu-id="17407-267">Si l’état de l’échantillonneur est omis, un état d’échantillonneur par défaut est appliqué en spécifiant le filtrage linéaire et un mode habillage pour les coordonnées de la texture.</span><span class="sxs-lookup"><span data-stu-id="17407-267">If the sampler state is omitted, a default sampler state is applied specifying linear filtering and a wrap mode for the texture coordinates.</span></span> <span data-ttu-id="17407-268">La fonction d’échantillonneur prend une coordonnée de texture à virgule flottante à deux composants et retourne une couleur à deux composants.</span><span class="sxs-lookup"><span data-stu-id="17407-268">The sampler function takes a two-component floating-point texture coordinate, and returns a two-component color.</span></span> <span data-ttu-id="17407-269">Il est représenté par le type de retour float2 et représente les données dans les composants rouge et vert.</span><span class="sxs-lookup"><span data-stu-id="17407-269">This is represented with the float2 return type and represents data in the red and green components.</span></span>

<span data-ttu-id="17407-270">Quatre types d’échantillonneurs sont définis (consultez [Mots clés](dx-graphics-hlsl-appendix.md)) et les recherches de texture sont effectuées par les fonctions intrinsèques : [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md), [**tex2D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md), [**Tex3D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex3d.md), [**texCUBE (s, t) (DirectX HLSL)**](dx-graphics-hlsl-texcube.md).</span><span class="sxs-lookup"><span data-stu-id="17407-270">Four types of samplers are defined (see [Keywords](dx-graphics-hlsl-appendix.md)) and texture lookups are performed by the intrinsic functions: [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md), [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md), [**tex3D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex3d.md), [**texCUBE(s, t) (DirectX HLSL)**](dx-graphics-hlsl-texcube.md).</span></span> <span data-ttu-id="17407-271">Voici un exemple d’échantillonnage 3D :</span><span class="sxs-lookup"><span data-stu-id="17407-271">Here is an example of 3D sampling:</span></span>


```
texture tex0;
sampler3D s_3D;

float3 sample_3D(float3 tex : TEXCOORD0) : COLOR
{
  return tex3D(s_3D, tex);
}
```



<span data-ttu-id="17407-272">Cette déclaration d’échantillonneur utilise l’état d’échantillonnage par défaut pour les paramètres de filtre et le mode d’adresse.</span><span class="sxs-lookup"><span data-stu-id="17407-272">This sampler declaration uses default sampler state for the filter settings and address mode.</span></span>

<span data-ttu-id="17407-273">Voici l’exemple d’échantillonnage de cube correspondant :</span><span class="sxs-lookup"><span data-stu-id="17407-273">Here is the corresponding cube sampling example:</span></span>


```
texture tex0;
samplerCUBE s_CUBE;

float3 sample_CUBE(float3 tex : TEXCOORD0) : COLOR
{
  return texCUBE(s_CUBE, tex);
}
```



<span data-ttu-id="17407-274">Enfin, voici l’exemple d’échantillonnage 1D :</span><span class="sxs-lookup"><span data-stu-id="17407-274">And finally, here is the 1D sampling example:</span></span>


```
texture tex0;
sampler1D s_1D;

float sample_1D(float tex : TEXCOORD0) : COLOR
{
  return tex1D(s_1D, tex);
}
```



<span data-ttu-id="17407-275">Étant donné que le runtime ne prend pas en charge les textures 1D, le compilateur utilise une texture 2D avec la connaissance que la coordonnée y n’est pas importante.</span><span class="sxs-lookup"><span data-stu-id="17407-275">Because the runtime does not support 1D textures, the compiler will use a 2D texture with the knowledge that the y-coordinate is unimportant.</span></span> <span data-ttu-id="17407-276">Étant donné que [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) est implémenté en tant que recherche de texture 2D, le compilateur est libre de choisir le composant y de manière efficace.</span><span class="sxs-lookup"><span data-stu-id="17407-276">Since [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) is implemented as a 2D texture lookup, the compiler is free to choose the y-component in an efficient manner.</span></span> <span data-ttu-id="17407-277">Dans certains scénarios rares, le compilateur ne peut pas choisir un composant y efficace. dans ce cas, il émet un avertissement.</span><span class="sxs-lookup"><span data-stu-id="17407-277">In some rare scenarios, the compiler cannot choose an efficient y-component, in which case it will issue a warning.</span></span>


```
texture tex0;
sampler s_1D_float;

float4 main(float texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float, texCoords);
}
```



<span data-ttu-id="17407-278">Cet exemple particulier est inefficace, car le compilateur doit déplacer la coordonnée d’entrée dans un autre registre (car une recherche 1D est implémentée en tant que recherche 2D et la coordonnée de texture est déclarée en tant que float1).</span><span class="sxs-lookup"><span data-stu-id="17407-278">This particular example is inefficient because the compiler must move the input coordinate into another register (because a 1D lookup is implemented as a 2D lookup and the texture coordinate is declared as a float1).</span></span> <span data-ttu-id="17407-279">Si le code est réécrit à l’aide d’une entrée float2 au lieu d’un float1, le compilateur peut utiliser la coordonnée de texture d’entrée, car il sait que y est initialisé à un.</span><span class="sxs-lookup"><span data-stu-id="17407-279">If the code is rewritten using a float2 input instead of a float1, the compiler can use the input texture coordinate because it knows that y is initialized to something.</span></span>


```
texture tex0;
sampler s_1D_float2;

float4 main(float2 texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float2, texCoords);
}
```



<span data-ttu-id="17407-280">Toutes les recherches de texture peuvent être ajoutées avec « Bias » ou « proj » (autrement dit, [**tex2Dbias (DirectX HLSL)**](dx-graphics-hlsl-tex2dbias.md), [**TEXCUBEPROJ (DirectX HLSL)**](dx-graphics-hlsl-texcubeproj.md)).</span><span class="sxs-lookup"><span data-stu-id="17407-280">All texture lookups can be appended with "bias" or "proj" (that is, [**tex2Dbias (DirectX HLSL)**](dx-graphics-hlsl-tex2dbias.md), [**texCUBEproj (DirectX HLSL)**](dx-graphics-hlsl-texcubeproj.md)).</span></span> <span data-ttu-id="17407-281">Avec le suffixe « proj », la coordonnée de texture est divisée par le composant w.</span><span class="sxs-lookup"><span data-stu-id="17407-281">With the "proj" suffix, the texture coordinate is divided by the w-component.</span></span> <span data-ttu-id="17407-282">Avec « Bias », le niveau MIP est décalé par le composant w.</span><span class="sxs-lookup"><span data-stu-id="17407-282">With "bias," the mip level is shifted by the w-component.</span></span> <span data-ttu-id="17407-283">Ainsi, toutes les recherches de texture avec un suffixe prennent toujours une entrée float4.</span><span class="sxs-lookup"><span data-stu-id="17407-283">Thus, all texture lookups with a suffix always take a float4 input.</span></span> <span data-ttu-id="17407-284">[**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) et [**tex2D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) ignorent respectivement les composants YZ et z.</span><span class="sxs-lookup"><span data-stu-id="17407-284">[**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) and [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) ignore the yz- and z-components respectively.</span></span>

<span data-ttu-id="17407-285">Les échantillonneurs peuvent également être utilisés dans un tableau, même si aucun back end ne prend actuellement en charge l’accès aux tableaux dynamiques des échantillonneurs.</span><span class="sxs-lookup"><span data-stu-id="17407-285">Samplers may also be used in array, although no back end currently supports dynamic array access of samplers.</span></span> <span data-ttu-id="17407-286">Par conséquent, les éléments suivants sont valides, car ils peuvent être résolus au moment de la compilation :</span><span class="sxs-lookup"><span data-stu-id="17407-286">Therefore, the following is valid because it can be resolved at compile time:</span></span>


```
tex2D(s[0],tex)
```



<span data-ttu-id="17407-287">Toutefois, cet exemple n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="17407-287">However, this example is not valid.</span></span>


```
tex2D(s[a],tex)
```



<span data-ttu-id="17407-288">L’accès dynamique des échantillonneurs est principalement utile pour écrire des programmes avec des boucles littérales.</span><span class="sxs-lookup"><span data-stu-id="17407-288">Dynamic access of samplers is primarily useful for writing programs with literal loops.</span></span> <span data-ttu-id="17407-289">Le code suivant illustre l’accès au tableau d’échantillonneurs :</span><span class="sxs-lookup"><span data-stu-id="17407-289">The following code illustrates sampler array accessing:</span></span>


```
sampler sm[4];

float4 main(float4 tex[4] : TEXCOORD) : COLOR
{
    float4 retColor = 1;

    for(int i = 0; i < 4;i++)
    {
        retColor *= tex2D(sm[i],tex[i]);
    }

    return retColor;
}
```



> [!Note]
>
> <span data-ttu-id="17407-290">L’utilisation du runtime de débogage Microsoft Direct3D peut vous aider à intercepter les incompatibilités entre le nombre de composants dans une texture et un échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="17407-290">Using the Microsoft Direct3D debug runtime can help you catch mismatches between the number of components in a texture and a sampler.</span></span>

 

## <a name="writing-functions"></a><span data-ttu-id="17407-291">Écriture de fonctions</span><span class="sxs-lookup"><span data-stu-id="17407-291">Writing Functions</span></span>

<span data-ttu-id="17407-292">Les fonctions fractionnent les tâches de grande taille en plus petites.</span><span class="sxs-lookup"><span data-stu-id="17407-292">Functions break large tasks into smaller ones.</span></span> <span data-ttu-id="17407-293">Les petites tâches sont plus faciles à déboguer et peuvent être réutilisées, une fois qu’elles sont éprouvées.</span><span class="sxs-lookup"><span data-stu-id="17407-293">Small tasks are easier to debug and can be reused, once proven.</span></span> <span data-ttu-id="17407-294">Les fonctions peuvent être utilisées pour masquer les détails d’autres fonctions, ce qui rend un programme composé de fonctions plus facile à suivre.</span><span class="sxs-lookup"><span data-stu-id="17407-294">Functions can be used to hide details of other functions, which makes a program composed of functions easier to follow.</span></span>

<span data-ttu-id="17407-295">Les fonctions HLSL sont similaires aux fonctions C de plusieurs façons : elles contiennent toutes les deux une définition et un corps de fonction, et elles déclarent toutes deux des types de retour et des listes d’arguments.</span><span class="sxs-lookup"><span data-stu-id="17407-295">HLSL functions are similar to C functions in several ways: They both contain a definition and a function body and they both declare return types and argument lists.</span></span> <span data-ttu-id="17407-296">À l’instar des fonctions C, la validation HLSL effectue une vérification de type sur les arguments, les types d’arguments et la valeur de retour pendant la compilation du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="17407-296">Like C functions, HLSL validation does type checking on the arguments, argument types, and the return value during shader compilation.</span></span>

<span data-ttu-id="17407-297">Contrairement aux fonctions C, les fonctions de point d’entrée HLSL utilisent la sémantique pour lier les arguments de fonction aux entrées et sorties du nuanceur (fonctions HLSL appelées « ignorer la sémantique en interne »).</span><span class="sxs-lookup"><span data-stu-id="17407-297">Unlike C functions, HLSL entry point functions use semantics to bind function arguments to shader inputs and outputs (HLSL functions called internally ignore semantics).</span></span> <span data-ttu-id="17407-298">Cela facilite la liaison des données de mémoire tampon à un nuanceur et la liaison des sorties de nuanceur aux entrées de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="17407-298">This makes it easier to bind buffer data to a shader, and bind shader outputs to shader inputs.</span></span>

<span data-ttu-id="17407-299">Une fonction contient une déclaration et un corps, et la déclaration doit précéder le corps.</span><span class="sxs-lookup"><span data-stu-id="17407-299">A function contains a declaration and a body, and the declaration must precede the body.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



<span data-ttu-id="17407-300">La déclaration de fonction inclut tout ce qui se trouve devant les accolades :</span><span class="sxs-lookup"><span data-stu-id="17407-300">The function declaration includes everything in front of the curly braces:</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



<span data-ttu-id="17407-301">Une déclaration de fonction contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="17407-301">A function declaration contains:</span></span>

-   <span data-ttu-id="17407-302">Type de retour</span><span class="sxs-lookup"><span data-stu-id="17407-302">A return type</span></span>
-   <span data-ttu-id="17407-303">Nom de fonction</span><span class="sxs-lookup"><span data-stu-id="17407-303">A function name</span></span>
-   <span data-ttu-id="17407-304">Liste d’arguments (facultatif)</span><span class="sxs-lookup"><span data-stu-id="17407-304">An argument list (optional)</span></span>
-   <span data-ttu-id="17407-305">Une sémantique de sortie (facultatif)</span><span class="sxs-lookup"><span data-stu-id="17407-305">An output semantic (optional)</span></span>
-   <span data-ttu-id="17407-306">Une annotation (facultatif)</span><span class="sxs-lookup"><span data-stu-id="17407-306">An annotation (optional)</span></span>

<span data-ttu-id="17407-307">Le type de retour peut être l’un des types de données de base HLSL tels qu’un float4 :</span><span class="sxs-lookup"><span data-stu-id="17407-307">The return type can be any of the HLSL basic data types such as a float4:</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
   ...
}
```



<span data-ttu-id="17407-308">Le type de retour peut être une structure qui a déjà été définie :</span><span class="sxs-lookup"><span data-stu-id="17407-308">The return type can be a structure that has already been defined:</span></span>


```
struct VS_OUTPUT
{
    float4  vPosition        : POSITION;
    float4  vDiffuse         : COLOR;
}; 

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



<span data-ttu-id="17407-309">Si la fonction ne retourne pas de valeur, void peut être utilisé comme type de retour.</span><span class="sxs-lookup"><span data-stu-id="17407-309">If the function does not return a value, void can be used as the return type.</span></span>


```
void VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



<span data-ttu-id="17407-310">Le type de retour apparaît toujours en premier dans une déclaration de fonction.</span><span class="sxs-lookup"><span data-stu-id="17407-310">The return type always appears first in a function declaration.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



<span data-ttu-id="17407-311">Une liste d’arguments déclare les arguments d’entrée à une fonction.</span><span class="sxs-lookup"><span data-stu-id="17407-311">An argument list declares the input arguments to a function.</span></span> <span data-ttu-id="17407-312">Il peut également déclarer des valeurs qui seront retournées.</span><span class="sxs-lookup"><span data-stu-id="17407-312">It may also declare values that will be returned.</span></span> <span data-ttu-id="17407-313">Certains arguments sont à la fois des arguments d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="17407-313">Some arguments are both input and output arguments.</span></span> <span data-ttu-id="17407-314">Voici un exemple de nuanceur qui accepte quatre arguments d’entrée.</span><span class="sxs-lookup"><span data-stu-id="17407-314">Here is an example of a shader that takes four input arguments.</span></span>


```
float4 Light(float3 LightDir : TEXCOORD1, 
             uniform float4 LightColor,  
             float2 texcrd : TEXCOORD0, 
             uniform sampler samp) : COLOR 
{
    float3 Normal = tex2D(samp,texcrd);

    return dot((Normal*2 - 1), LightDir)*LightColor;
}
```



<span data-ttu-id="17407-315">Cette fonction retourne une couleur finale, qui est un mélange d’un échantillon de texture et de la couleur claire.</span><span class="sxs-lookup"><span data-stu-id="17407-315">This function returns a final color, that is a blend of a texture sample and the light color.</span></span> <span data-ttu-id="17407-316">La fonction accepte quatre entrées.</span><span class="sxs-lookup"><span data-stu-id="17407-316">The function takes four inputs.</span></span> <span data-ttu-id="17407-317">Deux entrées ont une sémantique : LightDir a la sémantique [TEXCOORD1](dx-graphics-hlsl-semantics.md) , et texcrd a la sémantique [TEXCOORD0](dx-graphics-hlsl-semantics.md) .</span><span class="sxs-lookup"><span data-stu-id="17407-317">Two inputs have semantics: LightDir has the [TEXCOORD1](dx-graphics-hlsl-semantics.md) semantic, and texcrd has the [TEXCOORD0](dx-graphics-hlsl-semantics.md) semantic.</span></span> <span data-ttu-id="17407-318">La sémantique signifie que les données de ces variables proviennent de la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="17407-318">The semantics mean that the data for these variables will come from the vertex buffer.</span></span> <span data-ttu-id="17407-319">Même si la variable LightDir a une sémantique [TEXCOORD1](dx-graphics-hlsl-semantics.md) , le paramètre n’est probablement pas une coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="17407-319">Even though the LightDir variable has a [TEXCOORD1](dx-graphics-hlsl-semantics.md) semantic, the parameter is probably not a texture coordinate.</span></span> <span data-ttu-id="17407-320">Le type sémantique TEXCOORDn est souvent utilisé pour fournir une sémantique pour un type qui n’est pas prédéfini (il n’y a pas de sémantique d’entrée de nuanceur de sommets pour une direction claire).</span><span class="sxs-lookup"><span data-stu-id="17407-320">The TEXCOORDn semantic type is often used to supply a semantic for a type that is not predefined (there is no vertex shader input semantic for a light direction).</span></span>

<span data-ttu-id="17407-321">Les deux autres entrées LightColor et SAMP sont étiquetées avec le mot clé [Uniform](dx-graphics-hlsl-appendix.md) .</span><span class="sxs-lookup"><span data-stu-id="17407-321">The other two inputs LightColor and samp are labeled with the [uniform](dx-graphics-hlsl-appendix.md) keyword.</span></span> <span data-ttu-id="17407-322">Il s’agit de constantes uniformes qui ne changent pas entre les appels de dessin.</span><span class="sxs-lookup"><span data-stu-id="17407-322">These are uniform constants that will not change between draw calls.</span></span> <span data-ttu-id="17407-323">Les valeurs de ces paramètres proviennent de variables globales de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="17407-323">The values for these parameters come from shader global variables.</span></span>

<span data-ttu-id="17407-324">Les arguments peuvent être étiquetés comme entrées avec le mot clé in, et les arguments de sortie avec le mot clé out.</span><span class="sxs-lookup"><span data-stu-id="17407-324">Arguments can be labeled as inputs with the in keyword, and output arguments with the out keyword.</span></span> <span data-ttu-id="17407-325">Les arguments ne peuvent pas être passés par référence ; Toutefois, un argument peut être à la fois une entrée et une sortie s’il est déclaré avec le mot clé INOUT.</span><span class="sxs-lookup"><span data-stu-id="17407-325">Arguments cannot be passed by reference; however, an argument can be both an input and an output if it is declared with the inout keyword.</span></span> <span data-ttu-id="17407-326">Les arguments passés à une fonction qui sont marqués avec le mot clé INOUT sont considérés comme des copies de l’original jusqu’au retour de la fonction, et ils sont recopiés.</span><span class="sxs-lookup"><span data-stu-id="17407-326">Arguments passed to a function that are marked with the inout keyword are considered copies of the original until the function returns, and they are copied back.</span></span> <span data-ttu-id="17407-327">Voici un exemple d’utilisation de INOUT :</span><span class="sxs-lookup"><span data-stu-id="17407-327">Here's an example using inout:</span></span>


```
void Increment_ByVal(inout float A, inout float B) 
{ 
    A++; B++;
}
```



<span data-ttu-id="17407-328">Cette fonction incrémente les valeurs dans A et B et les retourne.</span><span class="sxs-lookup"><span data-stu-id="17407-328">This function increments the values in A and B and returns them.</span></span>

<span data-ttu-id="17407-329">Le corps de la fonction est tout le code après la déclaration de la fonction.</span><span class="sxs-lookup"><span data-stu-id="17407-329">The function body is all of the code after the function declaration.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



<span data-ttu-id="17407-330">Le corps se compose d’instructions qui sont entourées d’accolades.</span><span class="sxs-lookup"><span data-stu-id="17407-330">The body consists of statements which are surrounded by curly braces.</span></span> <span data-ttu-id="17407-331">Le corps de la fonction implémente toutes les fonctionnalités à l’aide de variables, de littéraux, d’expressions et d’instructions.</span><span class="sxs-lookup"><span data-stu-id="17407-331">The function body implements all of the functionality using variables, literals, expressions, and statements.</span></span>

<span data-ttu-id="17407-332">Le corps du nuanceur effectue deux opérations : il effectue une multiplication de matrice et retourne un résultat float4.</span><span class="sxs-lookup"><span data-stu-id="17407-332">The shader body does two things: it performs a matrix multiply and returns a float4 result.</span></span> <span data-ttu-id="17407-333">La multiplication de matrice est effectuée à l’aide de la fonction [**mul (DirectX HLSL)**](dx-graphics-hlsl-mul.md) , qui effectue une multiplication de matrice 4x4.</span><span class="sxs-lookup"><span data-stu-id="17407-333">The matrix multiply is accomplished with the [**mul (DirectX HLSL)**](dx-graphics-hlsl-mul.md) function, which performs a 4x4 matrix multiply.</span></span> <span data-ttu-id="17407-334">**mul (DirectX HLSL)** est appelé fonction intrinsèque, car il est déjà intégré à la bibliothèque de fonctions HLSL.</span><span class="sxs-lookup"><span data-stu-id="17407-334">**mul (DirectX HLSL)** is called an intrinsic function because it is already built into the HLSL library of functions.</span></span> <span data-ttu-id="17407-335">Les fonctions intrinsèques seront couvertes plus en détail dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="17407-335">Intrinsic functions will be covered in more detail in the next section.</span></span>

<span data-ttu-id="17407-336">La matrice multiplie combine un POS d’entrée et un WorldViewProj de matrice composite.</span><span class="sxs-lookup"><span data-stu-id="17407-336">The matrix multiply combines an input vector Pos and a composite matrix WorldViewProj.</span></span> <span data-ttu-id="17407-337">Le résultat est la position des données transformées en espace à l’écran.</span><span class="sxs-lookup"><span data-stu-id="17407-337">The result is position data transformed into screen space.</span></span> <span data-ttu-id="17407-338">Il s’agit du traitement de nuanceur de vertex minimal que nous pouvons effectuer.</span><span class="sxs-lookup"><span data-stu-id="17407-338">This is the minimum vertex shader processing we can do.</span></span> <span data-ttu-id="17407-339">Si nous utilisons le pipeline de fonction fixe à la place d’un nuanceur de sommets, les données de vertex peuvent être dessinées après cette transformation.</span><span class="sxs-lookup"><span data-stu-id="17407-339">If we were using the fixed function pipeline instead of a vertex shader, the vertex data could be drawn after doing this transform.</span></span>

<span data-ttu-id="17407-340">La dernière instruction dans un corps de fonction est une instruction return.</span><span class="sxs-lookup"><span data-stu-id="17407-340">The last statement in a function body is a return statement.</span></span> <span data-ttu-id="17407-341">Tout comme C, cette instruction retourne le contrôle de la fonction à l’instruction qui a appelé la fonction.</span><span class="sxs-lookup"><span data-stu-id="17407-341">Just like C, this statement returns control from the function to the statement that called the function.</span></span>

<span data-ttu-id="17407-342">Les types de retour de fonction peuvent être l’un des types de données simples définis en HLSL, notamment bool, int Half, float et double.</span><span class="sxs-lookup"><span data-stu-id="17407-342">Function return types can be any of the simple data types defined in HLSL, including bool, int half, float, and double.</span></span> <span data-ttu-id="17407-343">Les types de retour peuvent être l’un des types de données complexes tels que les vecteurs et les matrices.</span><span class="sxs-lookup"><span data-stu-id="17407-343">Return types can be one of the complex data types such as vectors and matrices.</span></span> <span data-ttu-id="17407-344">Les types HLSL qui font référence aux objets ne peuvent pas être utilisés en tant que types de retour.</span><span class="sxs-lookup"><span data-stu-id="17407-344">HLSL types that refer to objects cannot be used as return types.</span></span> <span data-ttu-id="17407-345">Cela comprend PixelShader, VertexShader, texture et échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="17407-345">This includes pixelshader, vertexshader, texture, and sampler.</span></span>

<span data-ttu-id="17407-346">Voici un exemple de fonction qui utilise une structure pour un type de retour.</span><span class="sxs-lookup"><span data-stu-id="17407-346">Here is an example of a function that uses a structure for a return type.</span></span>


```
float4x4 WorldViewProj : WORLDVIEWPROJ;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VS_HLL_Example(float4 inPos : POSITION )
{
    VS_OUTPUT Out;

    Out.Pos = mul(inPos,  WorldViewProj );

    return Out;
};
```



<span data-ttu-id="17407-347">Le type de retour float4 a été remplacé par la structure et la \_ sortie, qui contient maintenant un seul membre float4.</span><span class="sxs-lookup"><span data-stu-id="17407-347">The float4 return type has been replaced with the structure VS\_OUTPUT, which now contains a single float4 member.</span></span>

<span data-ttu-id="17407-348">Une instruction return signale la fin d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="17407-348">A return statement signals the end of a function.</span></span> <span data-ttu-id="17407-349">Il s’agit de l’instruction return la plus simple.</span><span class="sxs-lookup"><span data-stu-id="17407-349">This is the simplest return statement.</span></span> <span data-ttu-id="17407-350">Elle retourne le contrôle de la fonction au programme appelant.</span><span class="sxs-lookup"><span data-stu-id="17407-350">It returns control from the function to the calling program.</span></span> <span data-ttu-id="17407-351">Elle ne retourne aucune valeur.</span><span class="sxs-lookup"><span data-stu-id="17407-351">It returns no value.</span></span>


```
void main()
{
    return ;
}
```



<span data-ttu-id="17407-352">Une instruction return peut retourner une ou plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="17407-352">A return statement can return one or more values.</span></span> <span data-ttu-id="17407-353">Cet exemple retourne une valeur littérale :</span><span class="sxs-lookup"><span data-stu-id="17407-353">This example returns a literal value:</span></span>


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



<span data-ttu-id="17407-354">L’exemple suivant renvoie le résultat scalaire d’une expression :</span><span class="sxs-lookup"><span data-stu-id="17407-354">This example returns the scalar result of an expression:</span></span>


```
return  light.enabled;
```



<span data-ttu-id="17407-355">Cet exemple retourne un float4 construit à partir d’une variable locale et d’un littéral :</span><span class="sxs-lookup"><span data-stu-id="17407-355">This example returns a float4 constructed from a local variable and a literal:</span></span>


```
return  float4(color.rgb, 1) ;
```



<span data-ttu-id="17407-356">Cet exemple retourne un float4 qui est construit à partir du résultat retourné par une fonction intrinsèque, et quelques valeurs littérales :</span><span class="sxs-lookup"><span data-stu-id="17407-356">This example returns a float4 that is constructed from the result returned from an intrinsic function, and a few literal values:</span></span>


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



<span data-ttu-id="17407-357">Cet exemple retourne une structure qui contient un ou plusieurs membres :</span><span class="sxs-lookup"><span data-stu-id="17407-357">This example returns a structure that contains one or more members:</span></span>


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="flow-control"></a><span data-ttu-id="17407-358">Contrôle de flux</span><span class="sxs-lookup"><span data-stu-id="17407-358">Flow Control</span></span>

<span data-ttu-id="17407-359">Le matériel de nuanceur de vertex et de pixels actuel est conçu pour exécuter un nuanceur ligne par ligne, en exécutant chaque instruction une seule fois.</span><span class="sxs-lookup"><span data-stu-id="17407-359">Most current vertex and pixel shader hardware is designed to run a shader line by line, executing each instruction once.</span></span> <span data-ttu-id="17407-360">Le langage HLSL prend en charge le contrôle de Flow, qui comprend la création de branches statiques, les instructions prédicats, le bouclage statique, la création de branche dynamique et le bouclage dynamique.</span><span class="sxs-lookup"><span data-stu-id="17407-360">HLSL supports flow control, which includes static branching, predicated instructions, static looping, dynamic branching, and dynamic looping.</span></span>

<span data-ttu-id="17407-361">Auparavant, l’utilisation d’une instruction if entraînait le code du nuanceur de langage assembleur qui implémente à la fois le côté « si » et le côté « autre » du flot de code.</span><span class="sxs-lookup"><span data-stu-id="17407-361">Previously, using an if statement resulted in assembly-language shader code that implements both the if side and the else side of the code flow.</span></span> <span data-ttu-id="17407-362">Voici un exemple du code HLSL qui a été compilé pour vs \_ 1 \_ 1 :</span><span class="sxs-lookup"><span data-stu-id="17407-362">Here is an example of the in HLSL code that was compiled for vs\_1\_1:</span></span>


```
if (Value > 0)
    oPos = Value1; 
else
    oPos = Value2; 
```



<span data-ttu-id="17407-363">Et voici le code assembleur obtenu :</span><span class="sxs-lookup"><span data-stu-id="17407-363">And here is the resulting assembly code:</span></span>


```
// Calculate linear interpolation value in r0.w
mov r1.w, c2.x               
slt r0.w, c3.x, r1.w         
// Linear interpolation between value1 and value2
mov r7, -c1                      
add r2, r7, c0                   
mad oPos, r0.w, r2, c1  
```



<span data-ttu-id="17407-364">Certains matériels autorisent la boucle statique ou dynamique, mais la plupart nécessitent une exécution linéaire.</span><span class="sxs-lookup"><span data-stu-id="17407-364">Some hardware allows for either static or dynamic looping, but most require linear execution.</span></span> <span data-ttu-id="17407-365">Sur les modèles qui ne prennent pas en charge la boucle, toutes les boucles doivent être déroulées.</span><span class="sxs-lookup"><span data-stu-id="17407-365">On the models that do not support looping, all loops must be unrolled.</span></span> <span data-ttu-id="17407-366">C’est le cas, par exemple, de l’exemple [DepthOfField](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) qui utilise des boucles non restaurées même pour les \_ \_ nuanceurs PS 1 1.</span><span class="sxs-lookup"><span data-stu-id="17407-366">An example is the [DepthOfField Sample](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) sample that uses unrolled loops even for ps\_1\_1 shaders.</span></span>

<span data-ttu-id="17407-367">HLSL prend désormais en charge chacun de ces types de contrôle de flow :</span><span class="sxs-lookup"><span data-stu-id="17407-367">HLSL now includes support for each of these types of flow control:</span></span>

-   <span data-ttu-id="17407-368">Branchement statique</span><span class="sxs-lookup"><span data-stu-id="17407-368">static branching</span></span>
-   <span data-ttu-id="17407-369">instructions prédicats</span><span class="sxs-lookup"><span data-stu-id="17407-369">predicated instructions</span></span>
-   <span data-ttu-id="17407-370">bouclage statique</span><span class="sxs-lookup"><span data-stu-id="17407-370">static looping</span></span>
-   <span data-ttu-id="17407-371">Branchement dynamique</span><span class="sxs-lookup"><span data-stu-id="17407-371">dynamic branching</span></span>
-   <span data-ttu-id="17407-372">bouclage dynamique</span><span class="sxs-lookup"><span data-stu-id="17407-372">dynamic looping</span></span>

<span data-ttu-id="17407-373">La branche statique permet de basculer ou de désactiver des blocs de code de nuanceur en fonction d’une constante de nuanceur booléenne.</span><span class="sxs-lookup"><span data-stu-id="17407-373">Static branching allows blocks of shader code to be switched on or off based on a Boolean shader constant.</span></span> <span data-ttu-id="17407-374">Il s’agit d’une méthode pratique pour activer ou désactiver les chemins de code en fonction du type d’objet actuellement restitué.</span><span class="sxs-lookup"><span data-stu-id="17407-374">This is a convenient method for enabling or disabling code paths based on the type of object currently being rendered.</span></span> <span data-ttu-id="17407-375">Entre les appels de dessin, vous pouvez choisir les fonctionnalités que vous souhaitez prendre en charge avec le nuanceur actuel, puis définir les indicateurs booléens requis pour obtenir ce comportement.</span><span class="sxs-lookup"><span data-stu-id="17407-375">Between draw calls, you can decide which features you want to support with the current shader and then set the Boolean flags required to get that behavior.</span></span> <span data-ttu-id="17407-376">Toutes les instructions qui sont désactivées par une constante booléenne sont ignorées lors de l’exécution du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="17407-376">Any statements that are disabled by a Boolean constant are skipped during shader execution.</span></span>

<span data-ttu-id="17407-377">La prise en charge de la branche la plus familière est la branche dynamique.</span><span class="sxs-lookup"><span data-stu-id="17407-377">The most familiar branching support is dynamic branching.</span></span> <span data-ttu-id="17407-378">Avec la création de branche dynamique, la condition de comparaison réside dans une variable, ce qui signifie que la comparaison est effectuée pour chaque vertex ou chaque pixel au moment de l’exécution (par opposition à la comparaison qui se produit au moment de la compilation, ou entre deux appels de dessin).</span><span class="sxs-lookup"><span data-stu-id="17407-378">With dynamic branching, the comparison condition resides in a variable, which means that the comparison is done for each vertex or each pixel at run time (as opposed to the comparison occurring at compile time, or between two draw calls).</span></span> <span data-ttu-id="17407-379">L’impact sur les performances est le coût de la branche plus le coût des instructions sur le côté de la branche.</span><span class="sxs-lookup"><span data-stu-id="17407-379">The performance hit is the cost of the branch plus the cost of the instructions on the side of the branch taken.</span></span> <span data-ttu-id="17407-380">La branche dynamique est implémentée dans le nuanceur modèle 3 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="17407-380">Dynamic branching is implemented in shader model 3 or higher.</span></span> <span data-ttu-id="17407-381">L’optimisation des nuanceurs qui fonctionnent avec ces modèles est semblable à l’optimisation du code qui s’exécute sur un processeur.</span><span class="sxs-lookup"><span data-stu-id="17407-381">Optimizing shaders that work with these models is similar to optimizing code that runs on a CPU.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17407-382">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="17407-382">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17407-383">Guide de programmation pour HLSL</span><span class="sxs-lookup"><span data-stu-id="17407-383">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 
