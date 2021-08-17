---
title: Syntaxe de la déclaration des fonctions
description: Les fonctions HLSL sont déclarées avec la syntaxe suivante.
ms.assetid: f8968de2-7b2d-4a2e-8312-cec5b652f700
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce8c6ec83963dac74dce32d248b23548c767192a604ddb8afbe35cf932dedee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514604"
---
# <a name="function-declaration-syntax"></a>Syntaxe de la déclaration des fonctions

Les fonctions HLSL sont déclarées avec la syntaxe suivante.

\[*StorageClass* \] \[clipplanes () \] \[ \] \_ *nom* de valeur de retour précis ( \[ *argumentlist* \] ) \[ : *sémantique* \] { \[ *StatementBlock* \] };



 

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*
</dt> <dd>

Modificateur qui redéfinit une déclaration de fonction. **inline** est actuellement la seule valeur de modificateur. La valeur du modificateur doit être **inline** , car il s’agit également de la valeur par défaut. Par conséquent, une fonction est Inline, que **vous spécifiiez inline et** que toutes les fonctions en HLSL soient Inline. Une fonction inline génère une copie du corps de la fonction (lors de la compilation) pour chaque appel de fonction. Cela permet de réduire la surcharge liée à l’appel de la fonction.

</dd> <dt>

<span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*
</dt> <dd>

Liste facultative de plans de clip, qui correspond à 6 plans de clip spécifiés par l’utilisateur. Il s’agit d’un mécanisme de remplacement pour [SV \_ ClipDistance](dx-graphics-hlsl-semantics.md) qui fonctionne sur le [niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x et supérieur.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomme*
</dt> <dd>

Chaîne ASCII qui identifie de façon unique le nom de la fonction de nuanceur.

</dd> <dt>

<span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*
</dt> <dd>

Liste d’arguments facultative, qui est une liste séparée par des virgules des [arguments](dx-graphics-hlsl-function-parameters.md) passés dans une fonction.

</dd> <dt>

<span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Équivalent*
</dt> <dd>

Chaîne facultative qui identifie l’utilisation prévue des données de retour (voir [sémantique (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).

</dd> <dt>

<span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*
</dt> <dd>

[Instructions](dx-graphics-hlsl-statement-blocks.md) facultatives qui composent le corps de la fonction. Une fonction définie sans corps est appelée un prototype de fonction. le corps d’une fonction prototype doit être défini ailleurs avant que la fonction puisse être appelée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Le type de retour peut être l’un de ces [types HLSL](dx-graphics-hlsl-data-types.md).

## <a name="remarks"></a>Remarques

La syntaxe de cette page décrit presque tous les types de fonctions HLSL, y compris les nuanceurs vertex, les nuanceurs de pixels et les fonctions d’assistance. Bien qu’un nuanceur Geometry soit également implémenté avec une fonction, sa syntaxe est un peu plus compliquée. il existe donc une page distincte qui définit une déclaration de fonction de nuanceur Geometry (voir [Geometry-Shader Object (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).

Une fonction peut être surchargée tant qu’elle reçoit une combinaison unique de types de paramètres et/ou l’ordre des paramètres. Le langage HLSL implémente également un certain nombre de fonctions intégrées ou [**intrinsèques**](dx-graphics-hlsl-intrinsic-functions.md).

Vous pouvez spécifier des plans de clips spécifiques à l’utilisateur avec l’attribut **clipplanes** . Windows applique ces plans de séquences à toutes les primitives dessinées. L’attribut **clipplanes** fonctionne comme [SV \_ ClipDistance](dx-graphics-hlsl-semantics.md) , mais fonctionne sur toutes les [fonctionnalités](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) matérielles 9 \_ x et supérieures. Pour plus d’informations, consultez l' [image des plans d’utilisateur sur le matériel de niveau de fonctionnalité 9](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).

## <a name="examples"></a>Exemples

Cet exemple provient de BasicHLSL10. FX de l' [exemple BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).


```hlsl
struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; 
    float4 Diffuse    : COLOR0;
    float2 TextureUV  : TEXCOORD0;
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    ...
    return Output;    
}
```



Cet exemple de AdvancedParticles. FX de l' [exemple AdvancedParticles](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)illustre l’utilisation d’une sémantique pour le type de retour.


```hlsl
//
// PS for particles
//
float4 PSPointSprite(PSSceneIn input) : SV_Target
{   
    return g_txDiffuse.Sample( g_samLinear, input.tex ) * input.color;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions (DirectX HLSL)](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 
