---
title: Référence du nuanceur asm
description: Les nuanceurs pilotent le pipeline graphique programmable.
ms.assetid: 2c58815c-83b5-4ae8-a192-ba865b485bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2941f4c32d03187ce08266bf1382cd1d94301ce0
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2019
ms.locfileid: "104971643"
---
# <a name="asm-shader-reference"></a><span data-ttu-id="4a204-103">Référence du nuanceur asm</span><span class="sxs-lookup"><span data-stu-id="4a204-103">Asm Shader Reference</span></span>

<span data-ttu-id="4a204-104">Les nuanceurs pilotent le pipeline graphique programmable.</span><span class="sxs-lookup"><span data-stu-id="4a204-104">Shaders drive the programmable graphics pipeline.</span></span>

## <a name="vertex-shader-reference"></a><span data-ttu-id="4a204-105">Référence du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="4a204-105">Vertex Shader Reference</span></span>

-   [<span data-ttu-id="4a204-106">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="4a204-106">vs\_1\_1</span></span>](dx9-graphics-reference-asm-vs-1-1.md)
-   [<span data-ttu-id="4a204-107">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4a204-107">vs\_2\_0</span></span>](dx9-graphics-reference-asm-vs-2-0.md)
-   [<span data-ttu-id="4a204-108">vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4a204-108">vs\_2\_x</span></span>](dx9-graphics-reference-asm-vs-2-x.md)
-   [<span data-ttu-id="4a204-109">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4a204-109">vs\_3\_0</span></span>](dx9-graphics-reference-asm-vs-3-0.md)

<span data-ttu-id="4a204-110">[Différences entre vertex shader](dx9-graphics-reference-asm-vs-differences.md) résume les différences entre les versions de nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="4a204-110">[Vertex Shader Differences](dx9-graphics-reference-asm-vs-differences.md) summarizes the differences between vertex shader versions.</span></span>

## <a name="pixel-shader-reference"></a><span data-ttu-id="4a204-111">Référence du nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="4a204-111">Pixel Shader Reference</span></span>

-   [<span data-ttu-id="4a204-112">PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="4a204-112">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4</span></span>](dx9-graphics-reference-asm-ps-1-x.md)
-   [<span data-ttu-id="4a204-113">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4a204-113">ps\_2\_0</span></span>](dx9-graphics-reference-asm-ps-2-0.md)
-   [<span data-ttu-id="4a204-114">PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4a204-114">ps\_2\_x</span></span>](dx9-graphics-reference-asm-ps-2-x.md)
-   [<span data-ttu-id="4a204-115">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4a204-115">ps\_3\_0</span></span>](dx9-graphics-reference-asm-ps-3-0.md)

<span data-ttu-id="4a204-116">[Différences de nuanceur de pixels](dx9-graphics-reference-asm-ps-differences.md) résume les différences entre les versions de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="4a204-116">[Pixel Shader Differences](dx9-graphics-reference-asm-ps-differences.md) summarizes the differences between pixel shader versions.</span></span>

## <a name="shader-model-4-and-5-reference"></a><span data-ttu-id="4a204-117">Référence du modèle de nuanceur 4 et 5</span><span class="sxs-lookup"><span data-stu-id="4a204-117">Shader Model 4 and 5 Reference</span></span>

<span data-ttu-id="4a204-118">Les sections [Shader Model 4 assembly](dx-graphics-hlsl-sm4-asm.md) et [Shader Model 5 assembly](shader-model-5-assembly--directx-hlsl-.md) décrivent les instructions prises en charge par Shader Model 4 et 5.</span><span class="sxs-lookup"><span data-stu-id="4a204-118">The [Shader Model 4 Assembly](dx-graphics-hlsl-sm4-asm.md) and [Shader Model 5 Assembly](shader-model-5-assembly--directx-hlsl-.md) sections describe the instructions that shader model 4 and 5 support.</span></span>

## <a name="behavior-of-constant-registers-in-assembly-shaders"></a><span data-ttu-id="4a204-119">Comportement des registres de constantes dans les nuanceurs d’assembly</span><span class="sxs-lookup"><span data-stu-id="4a204-119">Behavior of Constant Registers in Assembly Shaders</span></span>

<span data-ttu-id="4a204-120">Il existe deux façons de définir des registres constants dans un nuanceur d’assembly :</span><span class="sxs-lookup"><span data-stu-id="4a204-120">There are two ways to set constant registers in an assembly shader:</span></span>

-   <span data-ttu-id="4a204-121">Déclarez une constante de nuanceur dans le code assembleur à l’aide de l’une des \* instructions Def.</span><span class="sxs-lookup"><span data-stu-id="4a204-121">Declare a shader constant in assembly code using one of the def\* instructions.</span></span>
-   <span data-ttu-id="4a204-122">Utilisez l’une des \* \* \* méthodes d' \* API Set ShaderConstant.</span><span class="sxs-lookup"><span data-stu-id="4a204-122">Use one of the Set\*\*\*ShaderConstant\* API methods.</span></span>

### <a name="direct3d-9-shader-constants"></a><span data-ttu-id="4a204-123">Constantes de nuanceur Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="4a204-123">Direct3D 9 Shader Constants</span></span>

<span data-ttu-id="4a204-124">Dans Direct3D 9, la durée de vie des constantes définies dans un nuanceur donné est limitée à l’exécution de ce nuanceur uniquement (et n’est pas remplaçable).</span><span class="sxs-lookup"><span data-stu-id="4a204-124">In Direct3D 9 the lifetime of defined constants in a given shader is confined to the execution of that shader only (and is non-overridable).</span></span> <span data-ttu-id="4a204-125">Les constantes définies dans Direct3D 9 n’ont pas d’effets secondaires en dehors du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="4a204-125">Defined constants in Direct3D 9 have no side effects outside of the shader.</span></span>

<span data-ttu-id="4a204-126">Voici un exemple utilisant Direct3D 9 :</span><span class="sxs-lookup"><span data-stu-id="4a204-126">Here's an example using Direct3D 9:</span></span>


```
Given: 
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1:
    Call Set***Shader shader1
    Call Set***ShaderConstant* to set c4
    Call Draw
    Result: The shader will see the def'd value in c4

    
Given: 
    Scenario 1 has just completed
    Create shader2 (which references c4 but does not use the def instruction
      to define it) 

Scenario 2: 
    Call Set***Shader shader2
    Call Draw
    Result: The shader will see the value last set in c4 by 
     Set***ShaderConstant* in scenario 1. This is because shader 2 
     didn't def c4.
```



<span data-ttu-id="4a204-127">Dans Direct3D 9, l’appel de l' \* \* \* opération obtenir ShaderConstant \* récupère uniquement les valeurs constantes définies via Set \* \* \* ShaderConstant \* .</span><span class="sxs-lookup"><span data-stu-id="4a204-127">In Direct3D 9, calling Get\*\*\*ShaderConstant\* will only retrieve constant values set via Set\*\*\*ShaderConstant\*.</span></span>

### <a name="direct3d-8-shader-constants"></a><span data-ttu-id="4a204-128">Constantes de nuanceur Direct3D 8</span><span class="sxs-lookup"><span data-stu-id="4a204-128">Direct3D 8 Shader Constants</span></span>

<span data-ttu-id="4a204-129">Ce comportement est différent dans Direct3D 8. x.</span><span class="sxs-lookup"><span data-stu-id="4a204-129">This behavior is different in Direct3D 8.x.</span></span>


```
Given:
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1 (repeated with Direct3D 8):
    Call Set***Shader with shader1
    Call Set***ShaderConstant to set c4
    Call Draw
    Result: The shader will see the value in c4 from Set***ShaderConstant
```



<span data-ttu-id="4a204-130">Dans Direct3D 8. x Set \* \* \* ShaderConstant prend effet immédiatement.</span><span class="sxs-lookup"><span data-stu-id="4a204-130">In Direct3D 8.x Set\*\*\*ShaderConstant takes effect immediately.</span></span> <span data-ttu-id="4a204-131">Examinez le scénario suivant :</span><span class="sxs-lookup"><span data-stu-id="4a204-131">Consider this scenario:</span></span>


```
Given:
    Create shader1 which references c4 and defines it with the def instruction
    
Scenario 3:
    Call Set***Shader with shader1
    Call Draw
    Result: The shader will see the def'd value in c4

Given:
    Scenario 3 has just completed
    Create shader2 (which references c4 but does not use the def instruction 
      to define it)     
    
Scenario 4 :    
    Call Set***Shader with shader2
    Call Draw
    Result: The shader will see the def'd value in c4 (set by def in shader 1)
```



<span data-ttu-id="4a204-132">Le résultat indésirable est que l’ordre dans lequel les nuanceurs sont définis peut affecter le comportement observé des nuanceurs individuels.</span><span class="sxs-lookup"><span data-stu-id="4a204-132">The undesirable result is that the order in which the shaders are set could affect the observed behavior of individual shaders.</span></span>

## <a name="shader-driver-model-requirements"></a><span data-ttu-id="4a204-133">Spécifications du modèle de pilote Shader</span><span class="sxs-lookup"><span data-stu-id="4a204-133">Shader Driver Model Requirements</span></span>

<span data-ttu-id="4a204-134">Les interfaces Direct3D 9 sont limitées aux pilotes d’interface de pilote de périphérique (DDI) qui sont au niveau de DirectX 7 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4a204-134">Direct3D 9 interfaces are restricted to device driver interface (DDI) drivers that are DirectX 7-level and above.</span></span> <span data-ttu-id="4a204-135">Pour vérifier le niveau DDI, exécutez l' [outil de diagnostic DirectX](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) et examinez le fichier texte enregistré.</span><span class="sxs-lookup"><span data-stu-id="4a204-135">To check the DDI level, run the [DirectX Diagnostic Tool](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) and examine the saved text file.</span></span>

<span data-ttu-id="4a204-136">Pour référence, les interfaces Direct3D 8 fonctionnent uniquement sur les pilotes DDI DirectX 6 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4a204-136">For reference, Direct3D 8 interfaces work only on DDI drivers that are DirectX 6-level and above.</span></span>

## <a name="shader-binary-format"></a><span data-ttu-id="4a204-137">Format binaire du nuanceur</span><span class="sxs-lookup"><span data-stu-id="4a204-137">Shader Binary Format</span></span>

<span data-ttu-id="4a204-138">La disposition au niveau du bit du flux d’instructions du nuanceur est définie dans D3d9types. h.</span><span class="sxs-lookup"><span data-stu-id="4a204-138">The bitwise layout of the shader instruction stream is defined in D3d9types.h.</span></span> <span data-ttu-id="4a204-139">Si vous souhaitez concevoir votre propre compilateur de nuanceur ou des outils de construction et que vous souhaitez obtenir plus d’informations sur le flux de jeton du nuanceur, consultez le kit de développement de pilotes (DDK) Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="4a204-139">If you want to design your own shader compiler or construction tools and you want more information about the shader token stream, refer to the Direct3D 9 Driver Development Kit (DDK).</span></span>

## <a name="c-like-shader-language"></a><span data-ttu-id="4a204-140">Langage de nuanceur de type C</span><span class="sxs-lookup"><span data-stu-id="4a204-140">C-like Shader Language</span></span>

<span data-ttu-id="4a204-141">Consultez [référence HLSL](dx-graphics-hlsl-reference.md) pour découvrir un langage de nuanceur de type C.</span><span class="sxs-lookup"><span data-stu-id="4a204-141">See [HLSL Reference](dx-graphics-hlsl-reference.md) to experience a C-like shader language.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a204-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4a204-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a204-143">Référence pour le langage HLSL</span><span class="sxs-lookup"><span data-stu-id="4a204-143">Reference for HLSL</span></span>](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 




