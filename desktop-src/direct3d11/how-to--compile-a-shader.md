---
title: Compilation d’un nuanceur
description: Cette rubrique montre comment utiliser la fonction D3DCompileFromFile au moment de l’exécution pour compiler le code du nuanceur.
ms.assetid: A2CE368F-E72A-453D-BA4D-3D1D53DDDEE0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb5eadb1d6627f553a9d769e6a0f43ab3ebe3a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728733"
---
# <a name="how-to-compile-a-shader"></a><span data-ttu-id="e0b79-103">Comment : compiler un nuanceur</span><span class="sxs-lookup"><span data-stu-id="e0b79-103">How To: Compile a Shader</span></span>

<span data-ttu-id="e0b79-104">En général, vous utilisez le compilateur de code [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL dans le cadre du processus de génération pour compiler le code du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="e0b79-104">You typically use the [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL code compiler as part of the build process to compile shader code.</span></span> <span data-ttu-id="e0b79-105">Pour plus d’informations à ce sujet, consultez [compilation des nuanceurs](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-part1).</span><span class="sxs-lookup"><span data-stu-id="e0b79-105">For more info about this, see [Compiling Shaders](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-part1).</span></span> <span data-ttu-id="e0b79-106">Cette rubrique montre comment utiliser la fonction [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) au moment de l’exécution pour compiler le code du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="e0b79-106">This topic shows how to use the [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) function at run time to compile shader code.</span></span>

<span data-ttu-id="e0b79-107">**Pour compiler un nuanceur :**</span><span class="sxs-lookup"><span data-stu-id="e0b79-107">**To compile a shader:**</span></span>

-   <span data-ttu-id="e0b79-108">Compilez le code du nuanceur HLSL en appelant [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile).</span><span class="sxs-lookup"><span data-stu-id="e0b79-108">Compile HLSL shader code by calling [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile).</span></span>
    ```C++
        UINT flags = D3DCOMPILE_ENABLE_STRICTNESS;
    #if defined( DEBUG ) || defined( _DEBUG )
        flags |= D3DCOMPILE_DEBUG;
    #endif
        // Prefer higher CS shader profile when possible as CS 5.0 provides better performance on 11-class hardware.
        LPCSTR profile = ( device->GetFeatureLevel() >= D3D_FEATURE_LEVEL_11_0 ) ? "cs_5_0" : "cs_4_0";
        const D3D_SHADER_MACRO defines[] = 
        {
            "EXAMPLE_DEFINE", "1",
            NULL, NULL
        };
        ID3DBlob* shaderBlob = nullptr;
        ID3DBlob* errorBlob = nullptr;
        HRESULT hr = D3DCompileFromFile( srcFile, defines, D3D_COMPILE_STANDARD_FILE_INCLUDE,
                                         entryPoint, profile,
                                         flags, 0, &shaderBlob, &errorBlob );
    ```

    

<span data-ttu-id="e0b79-109">L’exemple de code suivant montre comment compiler divers nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="e0b79-109">The following code example shows how to compile various shaders.</span></span>

> [!Note]  
> <span data-ttu-id="e0b79-110">Pour cet exemple de code, vous avez besoin de la SDK Windows 8,0 et du \_ fichier d3dcompiler44.dll à partir du dossier% Program \_ % \\ Windows kits \\ 8,0 \\ Redist \\ D3D \\ <arch> dans votre chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="e0b79-110">For this example code, you need the Windows SDK 8.0 and the d3dcompiler\_44.dll file from the %PROGRAM\_FILE%\\Windows Kits\\8.0\\Redist\\D3D\\<arch> folder in your path.</span></span> <span data-ttu-id="e0b79-111">Les applications du Windows Store prennent en charge la compilation au moment de l’exécution pour le développement, mais pas pour le déploiement.</span><span class="sxs-lookup"><span data-stu-id="e0b79-111">Windows Store apps support run time compilation for development but not for deployment.</span></span>

 


```C++
#define _WIN32_WINNT 0x600
#include <stdio.h>

#include <d3dcompiler.h>

#pragma comment(lib,"d3dcompiler.lib")

HRESULT CompileShader( _In_ LPCWSTR srcFile, _In_ LPCSTR entryPoint, _In_ LPCSTR profile, _Outptr_ ID3DBlob** blob )
{
    if ( !srcFile || !entryPoint || !profile || !blob )
       return E_INVALIDARG;

    *blob = nullptr;

    UINT flags = D3DCOMPILE_ENABLE_STRICTNESS;
#if defined( DEBUG ) || defined( _DEBUG )
    flags |= D3DCOMPILE_DEBUG;
#endif

    const D3D_SHADER_MACRO defines[] = 
    {
        "EXAMPLE_DEFINE", "1",
        NULL, NULL
    };

    ID3DBlob* shaderBlob = nullptr;
    ID3DBlob* errorBlob = nullptr;
    HRESULT hr = D3DCompileFromFile( srcFile, defines, D3D_COMPILE_STANDARD_FILE_INCLUDE,
                                     entryPoint, profile,
                                     flags, 0, &shaderBlob, &errorBlob );
    if ( FAILED(hr) )
    {
        if ( errorBlob )
        {
            OutputDebugStringA( (char*)errorBlob->GetBufferPointer() );
            errorBlob->Release();
        }

        if ( shaderBlob )
           shaderBlob->Release();

        return hr;
    }    

    *blob = shaderBlob;

    return hr;
}

int main()
{
    // Compile vertex shader shader
    ID3DBlob *vsBlob = nullptr;
    HRESULT hr = CompileShader( L"BasicHLSL11_VS.hlsl", "VSMain", "vs_4_0_level_9_1", &vsBlob );
    if ( FAILED(hr) )
    {
        printf("Failed compiling vertex shader %08X\n", hr );
        return -1;
    }

    // Compile pixel shader shader
    ID3DBlob *psBlob = nullptr;
    hr = CompileShader( L"BasicHLSL11_PS.hlsl", "PSMain", "ps_4_0_level_9_1", &psBlob );
    if ( FAILED(hr) )
    {
        vsBlob->Release();
        printf("Failed compiling pixel shader %08X\n", hr );
        return -1;
    }

    printf("Success\n");

    // Clean up
    vsBlob->Release();
    psBlob->Release();

    return 0;
}

```



<span data-ttu-id="e0b79-112">L’exemple de code précédent compile les blocs de code de nuanceur de pixels et de vertex dans les \_ fichiers BasicHLSL11 PS. HLSL et BasicHLSL11 \_ vs. HLSL.</span><span class="sxs-lookup"><span data-stu-id="e0b79-112">The preceding code example compiles the pixel and vertex shader code blocks in the BasicHLSL11\_PS.hlsl and BasicHLSL11\_VS.hlsl files.</span></span> <span data-ttu-id="e0b79-113">Voici le code dans BasicHLSL11 \_ PS. HLSL :</span><span class="sxs-lookup"><span data-stu-id="e0b79-113">Here is the code in BasicHLSL11\_PS.hlsl:</span></span>


```hlsl
//--------------------------------------------------------------------------------------
// File: BasicHLSL11_PS.hlsl
//
// The pixel shader file for the BasicHLSL11 sample.  
// 
// Copyright (c) Microsoft Corporation. All rights reserved.
//--------------------------------------------------------------------------------------

//--------------------------------------------------------------------------------------
// Globals
//--------------------------------------------------------------------------------------
cbuffer cbPerObject : register( b0 )
{
    float4        g_vObjectColor            : packoffset( c0 );
};

cbuffer cbPerFrame : register( b1 )
{
    float3        g_vLightDir                : packoffset( c0 );
    float        g_fAmbient                : packoffset( c0.w );
};

//--------------------------------------------------------------------------------------
// Textures and Samplers
//--------------------------------------------------------------------------------------
Texture2D    g_txDiffuse : register( t0 );
SamplerState g_samLinear : register( s0 );

//--------------------------------------------------------------------------------------
// Input / Output structures
//--------------------------------------------------------------------------------------
struct PS_INPUT
{
    float3 vNormal        : NORMAL;
    float2 vTexcoord    : TEXCOORD0;
};

//--------------------------------------------------------------------------------------
// Pixel Shader
//--------------------------------------------------------------------------------------
float4 PSMain( PS_INPUT Input ) : SV_TARGET
{
    float4 vDiffuse = g_txDiffuse.Sample( g_samLinear, Input.vTexcoord );
    
    float fLighting = saturate( dot( g_vLightDir, Input.vNormal ) );
    fLighting = max( fLighting, g_fAmbient );
    
    return vDiffuse * fLighting;
}
```



<span data-ttu-id="e0b79-114">Voici le code dans BasicHLSL11 \_ et HLSL :</span><span class="sxs-lookup"><span data-stu-id="e0b79-114">Here is the code in BasicHLSL11\_VS.hlsl:</span></span>


```hlsl
//--------------------------------------------------------------------------------------
// File: BasicHLSL11_VS.hlsl
//
// The vertex shader file for the BasicHLSL11 sample.  
// 
// Copyright (c) Microsoft Corporation. All rights reserved.
//--------------------------------------------------------------------------------------

//--------------------------------------------------------------------------------------
// Globals
//--------------------------------------------------------------------------------------
cbuffer cbPerObject : register( b0 )
{
    matrix        g_mWorldViewProjection    : packoffset( c0 );
    matrix        g_mWorld                : packoffset( c4 );
};

//--------------------------------------------------------------------------------------
// Input / Output structures
//--------------------------------------------------------------------------------------
struct VS_INPUT
{
    float4 vPosition    : POSITION;
    float3 vNormal        : NORMAL;
    float2 vTexcoord    : TEXCOORD0;
};

struct VS_OUTPUT
{
    float3 vNormal        : NORMAL;
    float2 vTexcoord    : TEXCOORD0;
    float4 vPosition    : SV_POSITION;
};

//--------------------------------------------------------------------------------------
// Vertex Shader
//--------------------------------------------------------------------------------------
VS_OUTPUT VSMain( VS_INPUT Input )
{
    VS_OUTPUT Output;
    
    Output.vPosition = mul( Input.vPosition, g_mWorldViewProjection );
    Output.vNormal = mul( Input.vNormal, (float3x3)g_mWorld );
    Output.vTexcoord = Input.vTexcoord;
    
    return Output;
}
```



## <a name="related-topics"></a><span data-ttu-id="e0b79-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e0b79-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0b79-116">Comment utiliser Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="e0b79-116">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 