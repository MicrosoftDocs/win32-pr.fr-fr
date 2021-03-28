---
title: Arguments de fonction
description: Une fonction accepte un ou plusieurs arguments d’entrée ; pour déclarer chaque argument, utilisez la syntaxe ci-après.
ms.assetid: 80e0dbc8-26b7-4250-bb01-6856fc70f6b8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ba35ad04b20b67e45550644e842d69209ca5088
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104381432"
---
# <a name="function-arguments"></a><span data-ttu-id="9d01b-103">Arguments de fonction</span><span class="sxs-lookup"><span data-stu-id="9d01b-103">Function Arguments</span></span>

<span data-ttu-id="9d01b-104">Une fonction accepte un ou plusieurs arguments d’entrée ; pour déclarer chaque argument, utilisez la syntaxe ci-après.</span><span class="sxs-lookup"><span data-stu-id="9d01b-104">A function takes one or more input arguments; use the following syntax to declare each argument.</span></span>



|                                                                                             |
|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d01b-105">**\[\]Nom du type InputModifier \[ : sémantique \] \[ InterpolationModifier \] \[ = initialiseurs\]**</span><span class="sxs-lookup"><span data-stu-id="9d01b-105">**\[InputModifier\] Type Name \[: Semantic\] \[InterpolationModifier\] \[= Initializers\]**</span></span> |



 

<span data-ttu-id="9d01b-106">\[Nom du type de modificateur \] \[ : sémantique \] \[ : modificateur d’interpolation \] \[ = initialiseur (s)\]</span><span class="sxs-lookup"><span data-stu-id="9d01b-106">\[Modifier\] Type Name \[: Semantic\] \[: Interpolation Modifier\] \[= Initializer(s)\]</span></span>

<span data-ttu-id="9d01b-107">S’il existe plusieurs arguments de fonction, ils sont séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="9d01b-107">If there are multiple function arguments, they are separated by commas.</span></span>

## <a name="parameters"></a><span data-ttu-id="9d01b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d01b-108">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9d01b-109">Élément</span><span class="sxs-lookup"><span data-stu-id="9d01b-109">Item</span></span></th>
<th><span data-ttu-id="9d01b-110">Description</span><span class="sxs-lookup"><span data-stu-id="9d01b-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d01b-111"><span id="InputModifier"></span><span id="inputmodifier"></span><span id="INPUTMODIFIER"></span><strong>InputModifier</strong></span><span class="sxs-lookup"><span data-stu-id="9d01b-111"><span id="InputModifier"></span><span id="inputmodifier"></span><span id="INPUTMODIFIER"></span><strong>InputModifier</strong></span></span><br/></td>
<td><span data-ttu-id="9d01b-112">Terme facultatif qui identifie un argument comme une entrée, une sortie ou les deux.</span><span class="sxs-lookup"><span data-stu-id="9d01b-112">Optional term that identifies an argument as an input, an output, or both.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d01b-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d01b-113">Value</span></span></td>
<td><span data-ttu-id="9d01b-114">Description</span><span class="sxs-lookup"><span data-stu-id="9d01b-114">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d01b-115"><strong>in</strong></span><span class="sxs-lookup"><span data-stu-id="9d01b-115"><strong>in</strong></span></span></td>
<td><span data-ttu-id="9d01b-116">Entrée uniquement</span><span class="sxs-lookup"><span data-stu-id="9d01b-116">Input only</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d01b-117"><strong>INOUT</strong></span><span class="sxs-lookup"><span data-stu-id="9d01b-117"><strong>inout</strong></span></span></td>
<td><span data-ttu-id="9d01b-118">Entrée et sortie</span><span class="sxs-lookup"><span data-stu-id="9d01b-118">Input and an output</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d01b-119"><strong>out</strong></span><span class="sxs-lookup"><span data-stu-id="9d01b-119"><strong>out</strong></span></span></td>
<td><span data-ttu-id="9d01b-120">Sortie uniquement</span><span class="sxs-lookup"><span data-stu-id="9d01b-120">Output only</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d01b-121"><strong>uniforme</strong></span><span class="sxs-lookup"><span data-stu-id="9d01b-121"><strong>uniform</strong></span></span></td>
<td><span data-ttu-id="9d01b-122">Données de constante en entrée uniquement</span><span class="sxs-lookup"><span data-stu-id="9d01b-122">Input only constant data</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="9d01b-123">Les paramètres sont toujours passés par valeur.</span><span class="sxs-lookup"><span data-stu-id="9d01b-123">Parameters are always passed by value.</span></span> <span data-ttu-id="9d01b-124">dans indique que la valeur du paramètre doit être copiée à partir de l’application appelante avant le début de la fonction.</span><span class="sxs-lookup"><span data-stu-id="9d01b-124">in indicates that the value of the parameter should be copied in from the calling application before the function begins.</span></span> <span data-ttu-id="9d01b-125">out indique que la dernière valeur du paramètre doit être copiée et retournée à l’application appelante lorsque la fonction retourne.</span><span class="sxs-lookup"><span data-stu-id="9d01b-125">out indicates that the last value of the parameter should be copied out, and returned to the calling application when the function returns.</span></span> <span data-ttu-id="9d01b-126">INOUT est un raccourci permettant de spécifier les deux.</span><span class="sxs-lookup"><span data-stu-id="9d01b-126">inout is a shorthand for specifying both.</span></span></p>
<p><span data-ttu-id="9d01b-127">Une valeur uniforme provient d’un registre de constantes ; chaque appel de nuanceur de sommet ou de nuanceur de pixels affiche la même valeur initiale pour une variable uniforme.</span><span class="sxs-lookup"><span data-stu-id="9d01b-127">A uniform value comes from a constant register; each vertex shader or pixel shader invocation see the same initial value for a uniform variable.</span></span> <span data-ttu-id="9d01b-128">Les variables globales sont traitées comme si elles étaient déclarées comme uniformes.</span><span class="sxs-lookup"><span data-stu-id="9d01b-128">Global variables are treated as if they are declared uniform.</span></span> <span data-ttu-id="9d01b-129">Pour les fonctions non de niveau supérieur, Uniform est synonyme de <strong>dans</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d01b-129">For non-top-level functions, uniform is synonymous with <strong>in</strong>.</span></span> <span data-ttu-id="9d01b-130">Si aucune utilisation de paramètre n’est spécifiée, l’utilisation des paramètres est supposée être <strong>dans</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d01b-130">If no parameter usage is specified, the parameter usage is assumed to be <strong>in</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d01b-131"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>Entrer</strong></span><span class="sxs-lookup"><span data-stu-id="9d01b-131"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>Type</strong></span></span></p></td>
<td><p><span data-ttu-id="9d01b-132">Type d’argument ; peut être n’importe quel <a href="dx-graphics-hlsl-data-types.md">type</a>HLSL valide.</span><span class="sxs-lookup"><span data-stu-id="9d01b-132">The argument type; can be any valid HLSL <a href="dx-graphics-hlsl-data-types.md">type</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d01b-133"><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>Nomme</strong></span><span class="sxs-lookup"><span data-stu-id="9d01b-133"><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="9d01b-134">Chaîne ASCII qui identifie de façon unique le nom de la fonction de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="9d01b-134">An ASCII string that uniquely identifies the name of the shader function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d01b-135"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>Équivalent</strong></span><span class="sxs-lookup"><span data-stu-id="9d01b-135"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>Semantic</strong></span></span></p></td>
<td><p><span data-ttu-id="9d01b-136">Chaîne facultative qui identifie l’utilisation prévue des données (voir <a href="dx-graphics-hlsl-semantics.md">sémantique (DirectX HLSL)</a>).</span><span class="sxs-lookup"><span data-stu-id="9d01b-136">Optional string that identifies the intended usage of the data (see <a href="dx-graphics-hlsl-semantics.md">Semantics (DirectX HLSL)</a>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d01b-137"><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>InterpolationModifier</strong></span><span class="sxs-lookup"><span data-stu-id="9d01b-137"><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>InterpolationModifier</strong></span></span></p></td>
<td><p><span data-ttu-id="9d01b-138"><a href="dx-graphics-hlsl-struct.md">Modificateur d’interpolation</a> facultatif qui permet à un nuanceur de déterminer la méthode d’interpolation.</span><span class="sxs-lookup"><span data-stu-id="9d01b-138">Optional <a href="dx-graphics-hlsl-struct.md">interpolation modifier</a> which allows a shader to determine the method of interpolation.</span></span> <span data-ttu-id="9d01b-139">Un modificateur d’interpolation sur un argument de fonction s’applique uniquement à un argument utilisé comme entrée d’une fonction de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="9d01b-139">An interpolation modifier on a function argument only applies to an argument used as an input to a pixel shader function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d01b-140"><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>Initialiseurs</strong></span><span class="sxs-lookup"><span data-stu-id="9d01b-140"><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>Initializers</strong></span></span></p></td>
<td><p><span data-ttu-id="9d01b-141">Valeurs facultatives pour l’initialisation ; plusieurs valeurs sont requises pour initialiser des types de données à plusieurs composants.</span><span class="sxs-lookup"><span data-stu-id="9d01b-141">Optional values for initialization; multiple values are required to initialize multi-component data types.</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="9d01b-142">Notes</span><span class="sxs-lookup"><span data-stu-id="9d01b-142">Remarks</span></span>

<span data-ttu-id="9d01b-143">Les arguments de fonction sont répertoriés dans une liste d’arguments séparés par des virgules dans une déclaration de fonction.</span><span class="sxs-lookup"><span data-stu-id="9d01b-143">Function arguments are listed in a comma-separated argument list in a function declaration.</span></span> <span data-ttu-id="9d01b-144">Comme dans les fonctions C, chaque argument doit avoir un nom de paramètre et un type déclarés ; un argument d’une fonction HLSL peut éventuellement inclure une sémantique, une valeur initiale et une entrée de nuanceur de pixels peut inclure un type d’interpolation.</span><span class="sxs-lookup"><span data-stu-id="9d01b-144">As in C functions, each argument must have a parameter name and type declared; an argument to an HLSL function optionally can include a semantic, an initial value, and a pixel shader input can include an interpolation type.</span></span>

<span data-ttu-id="9d01b-145">Le *type* d’un argument de fonction peut être une structure, qui peut inclure un modificateur d’interpolation par membre.</span><span class="sxs-lookup"><span data-stu-id="9d01b-145">The *Type* of a function argument could be a structure, which could include a per-member interpolation modifier.</span></span> <span data-ttu-id="9d01b-146">Si l’argument de fonction a également un modificateur d’interpolation, le modificateur d’argument de fonction remplace les modificateurs d’interpolation déclarés dans le type.</span><span class="sxs-lookup"><span data-stu-id="9d01b-146">If the function argument also has an interpolation modifier, the function argument modifier overrides interpolation modifiers declared within the Type.</span></span>

## <a name="examples"></a><span data-ttu-id="9d01b-147">Exemples</span><span class="sxs-lookup"><span data-stu-id="9d01b-147">Examples</span></span>

<span data-ttu-id="9d01b-148">Cet exemple (à partir de l' [exemple BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) illustre des entrées uniformes et non uniformes dans une fonction de nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="9d01b-148">This example (from the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) illustrates uniform and non-uniform inputs to a vertex shader function.</span></span>


```
VS_OUTPUT RenderSceneVS( 
  float4 vPos : POSITION,
  float3 vNormal : NORMAL,
  float2 vTexCoord0 : TEXCOORD,
  uniform int nNumLights,
  uniform bool bTexture,
  uniform bool bAnimate )
{
  ...
}
```



<span data-ttu-id="9d01b-149">Cet exemple (à partir de l' [exemple ContentStreaming](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)) utilise une structure d’entrée pour passer des arguments à une fonction de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="9d01b-149">This example (from the [ContentStreaming Sample](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)) uses an input structure to pass arguments to a pixel shader function.</span></span>


```
VSBasicIn input
struct VSBasicIn
{
  float4 Pos    : POSITION;
  float3 Norm   : NORMAL;
  float2 Tex    : TEXCOORD0;
};

PSBasicIn VSBasic(VSBasicIn input)
{
  ...
}
```



## <a name="related-topics"></a><span data-ttu-id="9d01b-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9d01b-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d01b-151">Fonctions (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9d01b-151">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 





