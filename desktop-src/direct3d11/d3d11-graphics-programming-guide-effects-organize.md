---
title: Organisation de l’État dans un effet (Direct3D 11)
description: Avec Direct3D 11, l’état d’effet de certaines étapes de pipeline est organisé par structures.
ms.assetid: e5057f94-69dd-4219-a5f4-569e48502475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a0523dd8abdabde29a5485b8d3b1e6d13b9429
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127526173"
---
# <a name="organizing-state-in-an-effect-direct3d-11"></a>Organisation de l’État dans un effet (Direct3D 11)

Avec Direct3D 11, l’état d’effet de certaines étapes de pipeline est organisé par structures. Voici les structures :



| État du pipeline | Structure                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------|
| Rastérisation  | [**D3D11 \_ rastériseur \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)                                                           |
| Fusion de sortie  | [**D3d11 \_ DESC \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) et [ **d3d11 \_ profondeur \_ du \_ stencil**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) |
| Nuanceurs        | Voir ci-dessous                                                                                                          |



 

Pour les étapes du nuanceur, où le nombre de modifications d’État doit être plus contrôlé par une application, l’État a été divisé en état de mémoire tampon constante, état de l’échantillonneur, état de la ressource du nuanceur et état d’affichage de l’accès non ordonné (pour les nuanceurs de pixels et de calcul). Cela permet à une application conçue pour mettre à jour uniquement l’État qui change, ce qui améliore les performances en réduisant la quantité de données qui doit être transmise au GPU.

Comment organiser l’état du pipeline en conséquence ?

La réponse est que l’ordre n’a pas d’importance. Les variables globales n’ont pas besoin d’être situées en haut. Toutefois, tous les exemples du kit de développement logiciel (SDK) suivent le même ordre, car il est recommandé d’organiser les données de la même façon. Il s’agit donc d’une brève description de l’ordonnancement des données dans les exemples du kit de développement logiciel (SDK) DirectX.

-   [Variables globales](#global-variables)
-   [Nuanceurs](#shaders)
-   [Groupes, techniques et passes](#groups-techniques-and-passes)

## <a name="global-variables"></a>Variables globales

Tout comme la pratique C standard, les variables globales sont déclarées en premier, en haut du fichier. Le plus souvent, il s’agit de variables qui seront initialisées par une application, puis utilisées dans un effet. Parfois, elles sont initialisées et jamais modifiées, à l’heure où elles sont mises à jour toutes les trames. Tout comme les règles de portée de fonction C, les variables d’effet déclarées en dehors de la portée des fonctions Effects sont visibles tout au long de l’effet. toute variable déclarée à l’intérieur d’une fonction Effect n’est visible que dans cette fonction.

Voici un exemple des variables déclarées dans BasicHLSL10. fx.


```
// Global variables
float4 g_MaterialAmbientColor;      // Material's ambient color

Texture2D g_MeshTexture;            // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix


// Texture samplers
SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};
```



La syntaxe des variables Effects est plus détaillée dans la [syntaxe de variable d’effet (Direct3D 11)](d3d11-effect-variable-syntax.md). La syntaxe des échantillonneurs de texture d’effet est plus détaillée dans le [type d’échantillonneur (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).

## <a name="shaders"></a>Nuanceurs

Les nuanceurs sont de petits programmes exécutables. Vous pouvez considérer les nuanceurs comme l’encapsulation de l’état du nuanceur, puisque le code HLSL implémente la fonctionnalité de nuanceur. Le pipeline graphique jusqu’à cinq types différents de nuanceurs.

-   Nuanceurs de vertex : opèrent sur les données de vertex. Un vertex dans produit un sommet.
-   Nuanciers de coque : opèrent sur les données des correctifs. Phase du point de contrôle : un appel produit un point de contrôle ; Pour chaque phase de bifurcation et de jointure : un correctif produit une quantité de données constantes de correctifs.
-   Nuanceurs de domaine-opèrent sur les données Primitives. Une primitive peut générer 0, 1 ou plusieurs Primitives.
-   Nuanceurs Geometry : opère sur les données Primitives. Une primitive dans peut donner 0, 1 ou plusieurs Primitives.
-   Nuanceurs de pixels : opèrent sur les données de pixels. Un pixel dans produit une sortie de 1 pixel (sauf si le pixel n’est pas éliminé d’un rendu).

Le pipeline du nuanceur de calcul utilise un nuanceur :

-   Nuanciers de calcul : opère sur tout type de données. La sortie est indépendante du nombre de threads.

Les nuanceurs sont des fonctions locales et suivent les règles de fonction de style C. Lorsqu’un effet est compilé, chaque nuanceur est compilé et un pointeur vers chaque fonction de nuanceur est stocké en interne. Une interface ID3D11Effect est retournée lorsque la compilation réussit. À ce stade, l’effet compilé est dans un format intermédiaire.

Pour obtenir plus d’informations sur les nuanceurs compilés, vous devez utiliser la réflexion du nuanceur. Cela revient essentiellement à demander au runtime de décompiler les nuanceurs et de retourner des informations sur le code du nuanceur.


```
struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; // vertex position 
    float4 Diffuse    : COLOR0;      // vertex diffuse color
    float2 TextureUV  : TEXCOORD0;   // vertex texture coords 
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    float3 vNormalWorldSpace;
 
    ....    
    
    return Output;    
}


struct PS_OUTPUT
{
    float4 RGBColor : SV_Target;  // Pixel color
};

PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;
    ....

    return Output;
}
```



La syntaxe des nuanceurs Effects est plus détaillée dans la syntaxe de la [fonction Effect (Direct3D 11)](d3d11-effect-function-syntax.md).

## <a name="groups-techniques-and-passes"></a>Groupes, techniques et passes

Un groupe est un ensemble de techniques. Une technique est une collection de passes de rendu (il doit y avoir au moins une passe). Chaque passe d’effet (qui est similaire à une seule passe dans une boucle de rendu) définit l’état du nuanceur et tout autre État de pipeline nécessaire pour afficher la géométrie.

Les groupes sont facultatifs. Il y a un seul groupe sans nom qui englobe toutes les techniques globales. Tous les autres groupes doivent être nommés.

Voici un exemple d’une technique (qui comprend une passe) à partir de BasicHLSL10. fx.


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

fxgroup g0
{
    technique11 RunComputeShader
    {
        pass P0
        {
            SetComputeShader( CompileShader( cs_5_0, CS() ) );
        }
    }
}

```



La syntaxe des nuanceurs d’effets est plus détaillée dans la [syntaxe de technique d’effet (Direct3D 11)](d3d11-effect-technique-syntax.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 