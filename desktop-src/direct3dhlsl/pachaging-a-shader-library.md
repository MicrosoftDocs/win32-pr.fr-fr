---
title: Empaquetage d’une bibliothèque de nuanceur
description: Ici, nous vous montrons comment compiler votre code de nuanceur, charger le code compilé dans une bibliothèque de nuanceur et lier les ressources des emplacements sources aux emplacements de destination.
ms.assetid: ED2EB1DE-3C25-4633-BFA7-C535ABBBAD28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90124ca9753a390b924d5ba702e1986e32eee9e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104991001"
---
# <a name="packaging-a-shader-library"></a><span data-ttu-id="eda67-103">Empaquetage d’une bibliothèque de nuanceur</span><span class="sxs-lookup"><span data-stu-id="eda67-103">Packaging a shader library</span></span>

<span data-ttu-id="eda67-104">Ici, nous vous montrons comment compiler votre code de nuanceur, charger le code compilé dans une bibliothèque de nuanceur et lier les ressources des emplacements sources aux emplacements de destination.</span><span class="sxs-lookup"><span data-stu-id="eda67-104">Here we show you how to compile your shader code, load the compiled code into a shader library, and bind resources from source slots to destination slots.</span></span>

<span data-ttu-id="eda67-105">**Objectif :** Pour empaqueter une bibliothèque de nuanceur à utiliser pour la liaison de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="eda67-105">**Objective:** To package a shader library to use for shader linking.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="eda67-106">Prérequis</span><span class="sxs-lookup"><span data-stu-id="eda67-106">Prerequisites</span></span>

<span data-ttu-id="eda67-107">Nous partons du principe que vous êtes familiarisé avec C++.</span><span class="sxs-lookup"><span data-stu-id="eda67-107">We assume that you are familiar with C++.</span></span> <span data-ttu-id="eda67-108">Vous avez également besoin d’une expérience de base dans les concepts de programmation graphique.</span><span class="sxs-lookup"><span data-stu-id="eda67-108">You also need basic experience with graphics programming concepts.</span></span>

<span data-ttu-id="eda67-109">**Durée d’exécution :** 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="eda67-109">**Time to complete:** 30 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="eda67-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="eda67-110">Instructions</span></span>

### <a name="1-compiling-your-shader-code"></a><span data-ttu-id="eda67-111">1. compilation de votre code de nuanceur</span><span class="sxs-lookup"><span data-stu-id="eda67-111">1. Compiling your shader code</span></span>

<span data-ttu-id="eda67-112">Compilez votre code de nuanceur avec l’une des fonctions de compilation.</span><span class="sxs-lookup"><span data-stu-id="eda67-112">Compile your shader code with one of the compile functions.</span></span> <span data-ttu-id="eda67-113">Par exemple, cet extrait de code utilise [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="eda67-113">For example, this code snippet uses [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile).</span></span>

```cpp
    string source;
 
    ComPtr<ID3DBlob> codeBlob;
    ComPtr<ID3DBlob> errorBlob;
    HRESULT hr = D3DCompile(
        source.c_str(),
        source.size(),
        "ShaderModule",
        NULL,
        NULL,
        NULL,
        ("lib" + m_shaderModelSuffix).c_str(),
        D3DCOMPILE_OPTIMIZATION_LEVEL3,
        0,
        &codeBlob,
        &errorBlob
        );
```

<span data-ttu-id="eda67-114">La chaîne source contient le code HLSL ASCII non compilé.</span><span class="sxs-lookup"><span data-stu-id="eda67-114">The source string contains the uncompiled ASCII HLSL code.</span></span>

### <a name="2-load-the-compiled-code-into-a-shader-library"></a><span data-ttu-id="eda67-115">2. Chargez le code compilé dans une bibliothèque de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="eda67-115">2. Load the compiled code into a shader library.</span></span>

<span data-ttu-id="eda67-116">Appelez la fonction [**D3DLoadModule**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule) pour charger le code compilé ([**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))) dans un module ([**ID3D11Module**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module)) qui représente une bibliothèque de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="eda67-116">Call the [**D3DLoadModule**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule) function to load the compiled code ([**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))) into a module ([**ID3D11Module**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module)) that represents a shader library.</span></span>


```C++
    // Load the compiled library code into a module object.
    ComPtr<ID3D11Module> shaderLibrary;
    DX::ThrowIfFailed(D3DLoadModule(codeBlob->GetBufferPointer(), codeBlob->GetBufferSize(), &shaderLibrary));
```



### <a name="3-bind-resources-from-source-slots-to-destination-slots"></a><span data-ttu-id="eda67-117">3. liez les ressources des emplacements sources aux emplacements de destination.</span><span class="sxs-lookup"><span data-stu-id="eda67-117">3. Bind resources from source slots to destination slots.</span></span>

<span data-ttu-id="eda67-118">Appelez la méthode [**ID3D11Module :: CreateInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance) pour créer une instance ([**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)) de la bibliothèque afin de pouvoir définir ensuite des liaisons de ressources pour l’instance.</span><span class="sxs-lookup"><span data-stu-id="eda67-118">Call the [**ID3D11Module::CreateInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance) method to create an instance ([**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)) of the library so you can then define resource bindings for the instance.</span></span>

<span data-ttu-id="eda67-119">Appelez les méthodes de liaison de [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance) pour lier les ressources dont vous avez besoin, des emplacements sources aux emplacements de destination.</span><span class="sxs-lookup"><span data-stu-id="eda67-119">Call the bind methods of [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance) to bind the resources you need from source slots to destination slots.</span></span> <span data-ttu-id="eda67-120">Les ressources peuvent être des textures, des mémoires tampons, des échantillonneurs, des mémoires tampons constantes ou des UAVs.</span><span class="sxs-lookup"><span data-stu-id="eda67-120">The resources can be textures, buffers, samplers, constant buffers, or UAVs.</span></span> <span data-ttu-id="eda67-121">En règle générale, vous allez utiliser les mêmes emplacements que la bibliothèque source.</span><span class="sxs-lookup"><span data-stu-id="eda67-121">Typically, you will use the same slots as the source library.</span></span>


```C++
    // Create an instance of the library and define resource bindings for it.
    // In this sample we use the same slots as the source library however this is not required.
    ComPtr<ID3D11ModuleInstance> shaderLibraryInstance;
    DX::ThrowIfFailed(shaderLibrary->CreateInstance("", &shaderLibraryInstance));
    // HRESULTs for Bind methods are intentionally ignored as compiler optimizations may eliminate the source
    // bindings. In these cases, the Bind operation will fail, but the final shader will function normally.
    shaderLibraryInstance->BindResource(0, 0, 1);
    shaderLibraryInstance->BindSampler(0, 0, 1);
    shaderLibraryInstance->BindConstantBuffer(0, 0, 0);
    shaderLibraryInstance->BindConstantBuffer(1, 1, 0);
    shaderLibraryInstance->BindConstantBuffer(2, 2, 0);
```



<span data-ttu-id="eda67-122">Ce code HLSL montre que la bibliothèque source utilise les mêmes emplacements (T0, S0, B0, B1 et B2) que les emplacements utilisés dans les méthodes de liaison précédentes de [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance).</span><span class="sxs-lookup"><span data-stu-id="eda67-122">This HLSL code shows that the source library uses the same slots (t0, s0, b0, b1, and b2) as the slots used in the preceding bind methods of [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance).</span></span>

``` syntax
// This is the default code in the fixed header section.
Texture2D<float3> Texture : register(t0);
SamplerState Anisotropic : register(s0);
cbuffer CameraData : register(b0)
{
    float4x4 Model;
    float4x4 View;
    float4x4 Projection;
};
cbuffer TimeVariantSignals : register(b1)
{
    float SineWave;
    float SquareWave;
    float TriangleWave;
    float SawtoothWave;
};

// This code is not displayed, but is used as part of the linking process.
cbuffer HiddenBuffer : register(b2)
{
    float3 LightDirection;
};
```

## <a name="summary-and-next-steps"></a><span data-ttu-id="eda67-123">Résumé et étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="eda67-123">Summary and next steps</span></span>

<span data-ttu-id="eda67-124">Nous avons compilé le code du nuanceur, chargé le code compilé dans une bibliothèque de nuanceur et lié les ressources des emplacements sources aux emplacements de destination.</span><span class="sxs-lookup"><span data-stu-id="eda67-124">We compiled shader code, loaded the compiled code into a shader library, and bound resources from source slots to destination slots.</span></span>

<span data-ttu-id="eda67-125">Ensuite, nous créons des graphes de liaison de fonction (FLGs) pour les nuanceurs, les liez à du code compilé et produisent des objets BLOB de nuanceur que le runtime Direct3D peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="eda67-125">Next we construct function-linking-graphs (FLGs) for shaders, link them to compiled code, and produce shader blobs that the Direct3D runtime can use.</span></span>

[<span data-ttu-id="eda67-126">Construction d’un graphique de fonctions de liaison de fonction et de son lien au code compilé</span><span class="sxs-lookup"><span data-stu-id="eda67-126">Constructing a function-linking-graph and linking it to compiled code</span></span>](constructing-a-function-linking-graph.md)

## <a name="related-topics"></a><span data-ttu-id="eda67-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eda67-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eda67-128">Utilisation de la liaison de nuanceur</span><span class="sxs-lookup"><span data-stu-id="eda67-128">Using shader linking</span></span>](using-shader-linking.md)
</dt> </dl>

 

 