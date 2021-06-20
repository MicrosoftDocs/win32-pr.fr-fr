---
description: Certaines constantes d’effet doivent uniquement être initialisées. Consultez le code de base pour définir des variables d’effet dans Direct3D 10.
ms.assetid: 743261a8-fdd8-492e-be8a-4faeb9b6f986
title: Définir l’état de l’effet (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df7133276b6392abca8d75eed16de896fb58f84
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404722"
---
# <a name="set-effect-state-direct3d-10"></a>Définir l’état de l’effet (Direct3D 10)

Certaines constantes d’effet doivent uniquement être initialisées. Une fois initialisé, l’état de l’effet est défini sur l’appareil pour l’ensemble de la boucle de rendu. D’autres variables doivent être mises à jour chaque fois que la boucle de rendu est appelée. Le code de base pour définir des variables d’effet est illustré ci-dessous, pour chacun des types de variables.

Un effet encapsule tout l’état de rendu requis pour effectuer une passe de rendu. En termes d’API, il existe trois types d’État encapsulés dans un effet.

-   [État constant](#constant-state)
-   [État du nuanceur](#shader-state)
-   [État de la texture](#texture-state)

## <a name="constant-state"></a>État constant

Tout d’abord, déclarez les variables dans un effet à l’aide des types de données HLSL.


```
//--------------------------------------------------------------------------------------
// Global variables
//--------------------------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
int g_nNumLights;

float3 g_LightDir[3];               // Light's direction in world space
float4 g_LightDiffuse[3];           // Light's diffuse color
float4 g_LightAmbient;              // Light's ambient color

Texture2D g_MeshTexture;            // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
```



Ensuite, déclarez les variables de l’application qui peuvent être définies par l’application, puis mettez à jour les variables d’effet.


```
           
    D3DXMATRIX  mWorldViewProjection;
    D3DXVECTOR3 vLightDir[MAX_LIGHTS];
    D3DXVECTOR4 vLightDiffuse[MAX_LIGHTS];
    D3DXMATRIX  mWorld;
    D3DXMATRIX  mView;
    D3DXMATRIX  mProj;

    // Get the projection and view matrix from the camera class
    mWorld = g_mCenterMesh * *g_Camera.GetWorldMatrix();
    mProj = *g_Camera.GetProjMatrix();
    mView = *g_Camera.GetViewMatrix();

    
OnD3D10CreateDevice()
{
  ...
    g_pLightDir = g_pEffect10->GetVariableByName( "g_LightDir" )->AsVector();
    g_pLightDiffuse = g_pEffect10->GetVariableByName( "g_LightDiffuse" )->AsVector();
    g_pmWorldViewProjection = g_pEffect10->GetVariableByName( 
        "g_mWorldViewProjection" )->AsMatrix();
    g_pmWorld = g_pEffect10->GetVariableByName( "g_mWorld" )->AsMatrix();
    g_pfTime = g_pEffect10->GetVariableByName( "g_fTime" )->AsScalar();
    g_pMaterialAmbientColor = g_pEffect10->GetVariableByName("g_MaterialAmbientColor")->AsVector();
    g_pMaterialDiffuseColor = g_pEffect10->GetVariableByName( 
        "g_MaterialDiffuseColor" )->AsVector();
    g_pnNumLights = g_pEffect10->GetVariableByName( "g_nNumLights" )->AsScalar();
}
```



Enfin, utilisez les méthodes de mise à jour pour définir la valeur des variables de l’application dans les variables d’effet.


```
           
OnD3D10FrameRender()
{
    ...
    g_pLightDir->SetRawValue( vLightDir, 0, sizeof(D3DXVECTOR3)*MAX_LIGHTS );
    g_pLightDiffuse->SetFloatVectorArray( (float*)vLightDiffuse, 0, MAX_LIGHTS );
    g_pmWorldViewProjection->SetMatrix( (float*)&mWorldViewProjection );
    g_pmWorld->SetMatrix( (float*)&mWorld );
    g_pfTime->SetFloat( (float)fTime );
    g_pnNumLights->SetInt( g_nNumActiveLights );
}
```



### <a name="two-ways-to-get-the-state-in-an-effect-variable"></a>Deux façons d’afficher l’État dans une variable Effect

Il existe deux façons d’accéder à l’État contenu dans une variable Effect. En fonction d’un effet qui a été chargé en mémoire.

L’une des méthodes consiste à obtenir l’état de l’échantillonneur à partir d’une [**interface ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) qui a été transtypée comme une interface d’échantillonnage.


```
D3D10_SAMPLER_DESC sampler_desc;
ID3D10EffectVariable* l_pD3D10EffectVariable = NULL;
if( g_pEffect10 )
{
    l_pD3D10EffectVariable = g_pEffect10->GetVariableByName( "MeshTextureSampler" );
    if( l_pD3D10EffectVariable )
        hr = (l_pD3D10EffectVariable->AsSampler())->GetBackingStore( 0, 
            &sampler_desc );
}
```



L’autre méthode consiste à récupérer l’état de l’échantillonneur à partir d’une [**interface ID3D10SamplerState**](/windows/desktop/api/D3D10/nn-d3d10-id3d10samplerstate).


```
ID3D10SamplerState* l_ppSamplerState = NULL;
D3D10_SAMPLER_DESC sampler_desc;
ID3D10EffectVariable* l_pD3D10EffectVariable = NULL;
if( g_pEffect10 )
{
    l_pD3D10EffectVariable = g_pEffect10->GetVariableByName( "MeshTextureSampler" );
    if( l_pD3D10EffectVariable )
    {
        hr = (l_pD3D10EffectVariable->AsSampler())->GetSampler( 0, 
            &l_ppSamplerState );
        if( l_ppSamplerState )
            l_ppSamplerState->GetDesc( &sampler_desc );
    }
}
```



## <a name="shader-state"></a>État du nuanceur

L’état du nuanceur est déclaré et affecté dans une technique d’effet, au sein d’une passe.


```
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, RenderSceneVS( 1, true, true ) ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}
```



Cela fonctionne comme si vous n’utilisiez pas d’effet. Il y a trois appels, un pour chaque type de nuanceur (vertex, Geometry et pixel). Le premier, SetVertexShader, appelle [**ID3D10Device :: VSSetShader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader). CompileShader est une fonction d’effet spéciale qui prend le profil de nuanceur (vs \_ 4 \_ 0) et le nom de la fonction de nuanceur de sommets (RenderVS). En d’autres termes, chacun de ces appels SetXXXShader compile la fonction de nuanceur associée et retourne un pointeur vers le nuanceur compilé.

## <a name="texture-state"></a>État de la texture

L’état de la texture est un peu plus complexe que la définition d’une variable, car les données de texture ne sont pas simplement lues comme une variable, elles sont échantillonnées à partir d’une texture. Par conséquent, vous devez définir la variable de texture (tout comme une variable normale, sauf qu’elle utilise un type de texture) et vous devez définir les conditions d’échantillonnage. Voici un exemple de déclaration de variable de texture et de déclaration d’état d’échantillonnage correspondante.


```
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

```



Voici un exemple de définition d’une texture à partir d’une application. Dans cet exemple, la texture est stockée dans les données de maillage, qui ont été chargées lors de la création de l’effet.

La première étape consiste à obtenir un pointeur vers la texture à partir de l’effet (à partir de la maille).


```
ID3D10EffectShaderResourceVariable* g_ptxDiffuse = NULL;

    // Obtain variables
    g_ptxDiffuse = g_pEffect10->GetVariableByName( "g_MeshTexture" )->AsShaderResource();
```



La deuxième étape consiste à spécifier une vue pour accéder à la texture. La vue définit un moyen général d’accéder aux données à partir de la ressource de texture.


```
   
OnD3D10FrameRender()
{
  ID3D10ShaderResourceView* pDiffuseRV = NULL;

   ...
   pDiffuseRV = g_Mesh10.GetMaterial(pSubset->MaterialID)->pDiffuseRV10;
   g_ptxDiffuse->SetResource( pDiffuseRV );
   ...
}   
```



Pour plus d’informations sur l’affichage des ressources, consultez [affichages des textures (Direct3D 10)](d3d10-graphics-programming-guide-resources-access-views.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu d’un effet (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



