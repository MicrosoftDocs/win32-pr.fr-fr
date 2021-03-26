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
# <a name="packaging-a-shader-library"></a>Empaquetage d’une bibliothèque de nuanceur

Ici, nous vous montrons comment compiler votre code de nuanceur, charger le code compilé dans une bibliothèque de nuanceur et lier les ressources des emplacements sources aux emplacements de destination.

**Objectif :** Pour empaqueter une bibliothèque de nuanceur à utiliser pour la liaison de nuanceur.

## <a name="prerequisites"></a>Prérequis

Nous partons du principe que vous êtes familiarisé avec C++. Vous avez également besoin d’une expérience de base dans les concepts de programmation graphique.

**Durée d’exécution :** 30 minutes.

## <a name="instructions"></a>Instructions

### <a name="1-compiling-your-shader-code"></a>1. compilation de votre code de nuanceur

Compilez votre code de nuanceur avec l’une des fonctions de compilation. Par exemple, cet extrait de code utilise [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile).

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

La chaîne source contient le code HLSL ASCII non compilé.

### <a name="2-load-the-compiled-code-into-a-shader-library"></a>2. Chargez le code compilé dans une bibliothèque de nuanceur.

Appelez la fonction [**D3DLoadModule**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule) pour charger le code compilé ([**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))) dans un module ([**ID3D11Module**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module)) qui représente une bibliothèque de nuanceur.


```C++
    // Load the compiled library code into a module object.
    ComPtr<ID3D11Module> shaderLibrary;
    DX::ThrowIfFailed(D3DLoadModule(codeBlob->GetBufferPointer(), codeBlob->GetBufferSize(), &shaderLibrary));
```



### <a name="3-bind-resources-from-source-slots-to-destination-slots"></a>3. liez les ressources des emplacements sources aux emplacements de destination.

Appelez la méthode [**ID3D11Module :: CreateInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance) pour créer une instance ([**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)) de la bibliothèque afin de pouvoir définir ensuite des liaisons de ressources pour l’instance.

Appelez les méthodes de liaison de [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance) pour lier les ressources dont vous avez besoin, des emplacements sources aux emplacements de destination. Les ressources peuvent être des textures, des mémoires tampons, des échantillonneurs, des mémoires tampons constantes ou des UAVs. En règle générale, vous allez utiliser les mêmes emplacements que la bibliothèque source.


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



Ce code HLSL montre que la bibliothèque source utilise les mêmes emplacements (T0, S0, B0, B1 et B2) que les emplacements utilisés dans les méthodes de liaison précédentes de [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance).

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

## <a name="summary-and-next-steps"></a>Résumé et étapes suivantes

Nous avons compilé le code du nuanceur, chargé le code compilé dans une bibliothèque de nuanceur et lié les ressources des emplacements sources aux emplacements de destination.

Ensuite, nous créons des graphes de liaison de fonction (FLGs) pour les nuanceurs, les liez à du code compilé et produisent des objets BLOB de nuanceur que le runtime Direct3D peut utiliser.

[Construction d’un graphique de fonctions de liaison de fonction et de son lien au code compilé](constructing-a-function-linking-graph.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la liaison de nuanceur](using-shader-linking.md)
</dt> </dl>

 

 