---
description: Les expressions sont des instructions mathématiques ou logiques qui sont utilisées sur le côté droit d’un signe égal. Il existe de nombreux types d’expressions.
ms.assetid: 642aa188-5dd7-49fc-b6cc-845f8fc22530
title: Expressions (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa574069094853eb506f7a1b38cdb6cd4379d3b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515118"
---
# <a name="expressions-direct3d-9"></a><span data-ttu-id="26405-104">Expressions (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="26405-104">Expressions (Direct3D 9)</span></span>

<span data-ttu-id="26405-105">Les expressions sont des instructions mathématiques ou logiques qui sont utilisées sur le côté droit d’un signe égal.</span><span class="sxs-lookup"><span data-stu-id="26405-105">Expressions are mathematical or logical statements that are used on the right hand side of an equals sign.</span></span> <span data-ttu-id="26405-106">Il existe de nombreux types d’expressions.</span><span class="sxs-lookup"><span data-stu-id="26405-106">There are many types of expressions.</span></span>

## <a name="expressions"></a><span data-ttu-id="26405-107">Expressions</span><span class="sxs-lookup"><span data-stu-id="26405-107">Expressions</span></span>

1.  <span data-ttu-id="26405-108">Référence de variable</span><span class="sxs-lookup"><span data-stu-id="26405-108">Variable Reference</span></span>
    ```
    ( variable ) or<variable >
    ```

    

2.  <span data-ttu-id="26405-109">Scalaire numérique</span><span class="sxs-lookup"><span data-stu-id="26405-109">Numeric Scalar</span></span>
    ```
    scalar 
    ```

    

3.  <span data-ttu-id="26405-110">Expression numérique</span><span class="sxs-lookup"><span data-stu-id="26405-110">Numeric Expression</span></span>

    ```
    ( numeric expression )
    ```

    

    <span data-ttu-id="26405-111">Toutes les expressions HLL numériques standard sont prises en charge ici.</span><span class="sxs-lookup"><span data-stu-id="26405-111">All standard numeric HLL expressions are supported here.</span></span>

4.  <span data-ttu-id="26405-112">Constructeur</span><span class="sxs-lookup"><span data-stu-id="26405-112">Constructor</span></span>
    ```
    type ( constructor arguments )
    ```

    

5.  <span data-ttu-id="26405-113">Liste des initialiseurs</span><span class="sxs-lookup"><span data-stu-id="26405-113">List of Initializers</span></span>

    ```
    { scalar value [, scalar value ...  ] }
    
    ```

    

    <span data-ttu-id="26405-114">Les valeurs scalaires doivent être des valeurs scalaires littérales.</span><span class="sxs-lookup"><span data-stu-id="26405-114">The scalars must be literal scalar values.</span></span>

    <span data-ttu-id="26405-115">Le nombre d’initialiseurs doit être compatible avec la variable (State) sur le côté gauche du signe égal.</span><span class="sxs-lookup"><span data-stu-id="26405-115">The number of initializers must be compatible with the variable (state) on the left hand side of the equals sign.</span></span>

6.  <span data-ttu-id="26405-116">OU expression</span><span class="sxs-lookup"><span data-stu-id="26405-116">OR Expression</span></span>

    ```
    token [ | token ... ]
    ```

    

    <span data-ttu-id="26405-117">Les jetons doivent être compatibles avec la variable (État) sur le côté gauche du signe égal.</span><span class="sxs-lookup"><span data-stu-id="26405-117">The tokens must be compatible with the variable (state) on the left hand side of the equals sign.</span></span>

    <span data-ttu-id="26405-118">Les jetons ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="26405-118">The tokens are not case sensitive.</span></span>

7.  <span data-ttu-id="26405-119">NULL</span><span class="sxs-lookup"><span data-stu-id="26405-119">NULL</span></span>

    ```
    NULL
    ```

    

    <span data-ttu-id="26405-120">La valeur NULL ne peut être assignée qu’à un nuanceur, un échantillonneur ou un objet texture.</span><span class="sxs-lookup"><span data-stu-id="26405-120">NULL can only be assigned to a shader, sampler, or a texture object.</span></span>

8.  <span data-ttu-id="26405-121">Bloc d’assembly</span><span class="sxs-lookup"><span data-stu-id="26405-121">Assembly Block</span></span>

    ```
    asm { code }
    ```

    

    <span data-ttu-id="26405-122">Les blocs d’assembly PS doivent être affectés à l’État PIXELSHADER.</span><span class="sxs-lookup"><span data-stu-id="26405-122">PS Assembly Blocks must be assigned to the PIXELSHADER state.</span></span>

    <span data-ttu-id="26405-123">Les blocs d’assembly VS doivent être affectés à l’État VERTEXSHADER.</span><span class="sxs-lookup"><span data-stu-id="26405-123">VS Assembly Blocks must be assigned to the VERTEXSHADER state.</span></span>

9.  <span data-ttu-id="26405-124">Bloc d’état de l’échantillonneur</span><span class="sxs-lookup"><span data-stu-id="26405-124">Sampler State Block</span></span>

    ```
    sampler_state { [ state = expression ; [ state = ... ] ] }
    ```

    

    <span data-ttu-id="26405-125">Les blocs d’état de l’échantillonneur sont des séquences d’état d’une étape d’échantillonnage non indexée ou d’affectations de texture.</span><span class="sxs-lookup"><span data-stu-id="26405-125">Sampler state blocks are sequences of un-indexed sampler stage state or texture assignments.</span></span>

    <span data-ttu-id="26405-126">Les blocs d’état de l’échantillonneur doivent être affectés à l’état de l’effet d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="26405-126">Sampler state blocks must be assigned to the SAMPLER effect state.</span></span>

10. <span data-ttu-id="26405-127">Bloc d’état de l’état d’effet</span><span class="sxs-lookup"><span data-stu-id="26405-127">Effect State State Block</span></span>

    ```
    stateblock_state { [ state [ [index] ] = expression; 
        [ state [ [index] ] = ... ] ] }
    ```

    

    <span data-ttu-id="26405-128">Les blocs d’État sont des séquences d’état général.</span><span class="sxs-lookup"><span data-stu-id="26405-128">State blocks are sequences of general state.</span></span> <span data-ttu-id="26405-129">Les blocs d’État peuvent être imbriqués, mais ne peuvent pas contenir de références circulaires.</span><span class="sxs-lookup"><span data-stu-id="26405-129">State blocks can be nested, but cannot contain circular references.</span></span>

    <span data-ttu-id="26405-130">Les blocs d’État doivent être affectés à l’état de l’effet STATEBLOCK.</span><span class="sxs-lookup"><span data-stu-id="26405-130">State blocks must be assigned to the STATEBLOCK effect state.</span></span>

11. <span data-ttu-id="26405-131">Compilation HLSL</span><span class="sxs-lookup"><span data-stu-id="26405-131">HLSL Compile</span></span>

    ```
    compile target entrypoint ( [ arguments ] )
    ```

    

    <span data-ttu-id="26405-132">Le nuanceur vertex et la \_ \_ cible m n indiquent la \_ version du nuanceur de sommets de la version D3DVS (m, n).</span><span class="sxs-lookup"><span data-stu-id="26405-132">The vertex shader vs\_m\_n target indicates D3DVS\_VERSION(m, n) vertex shader version.</span></span> <span data-ttu-id="26405-133">La cible de nuanceur de pixels PS \_ m \_ n indique la \_ version de nuanceur de pixels de la version D3DPS (m, n).</span><span class="sxs-lookup"><span data-stu-id="26405-133">The pixel shader ps\_m\_n target indicates D3DPS\_VERSION(m, n) pixel shader version.</span></span>

    <span data-ttu-id="26405-134">Les expressions de compilation du langage de niveau supérieur du nuanceur de sommets ne peuvent être assignées qu’à l’état de l’effet VERTEXSHADER.</span><span class="sxs-lookup"><span data-stu-id="26405-134">Vertex shader high-level language compile expressions can only be assigned to the VERTEXSHADER effect state.</span></span> <span data-ttu-id="26405-135">Les expressions de compilation du langage de haut niveau de nuanceur de pixels ne peuvent être assignées qu’à l’état d’effet PIXELSHADER.</span><span class="sxs-lookup"><span data-stu-id="26405-135">Pixel shader high-level language compile expressions can only be assigned to the PIXELSHADER effect state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26405-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="26405-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26405-137">Format d’effet</span><span class="sxs-lookup"><span data-stu-id="26405-137">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



