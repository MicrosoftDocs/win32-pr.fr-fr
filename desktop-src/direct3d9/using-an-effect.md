---
description: Cette page vous indique comment générer et utiliser un effet.
ms.assetid: d9fdafed-5958-4995-a1b5-8881feca1291
title: Utilisation d’un effet (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1170fde625e5eee5e9665f0759d302b5f5450a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109883"
---
# <a name="using-an-effect-direct3d-9"></a>Utilisation d’un effet (Direct3D 9)

Cette page vous indique comment générer et utiliser un effet. Les sujets abordés sont les suivants :

-   [Créer un effet](#create-an-effect)
-   [Rendu d’un effet](#render-an-effect)
-   [Utiliser la sémantique pour rechercher les paramètres d’effet](#use-semantics-to-find-effect-parameters)
-   [Utiliser des handles pour récupérer et définir des paramètres efficacement](#use-handles-to-get-and-set-parameters-efficiently)
-   [Ajouter des informations sur les paramètres avec des annotations](#add-parameter-information-with-annotations)
-   [Paramètres d’effet de partage](#share-effect-parameters)
-   [Compiler un effet hors connexion](#compile-an-effect-offline)
-   [Améliorer les performances avec des prénuanceurs](#improve-performance-with-preshaders)
-   [Utiliser des blocs de paramètres pour gérer les paramètres d’effet](#use-parameter-blocks-to-manage-effect-parameters)

## <a name="create-an-effect"></a>Créer un effet

Voici un exemple de création d’un effet tiré de l' [exemple BasicHLSL](../directx-sdk--august-2009-.md). Le code de création de l’effet pour la création d’un nuanceur de débogage provient de **OnCreateDevice**:


```
ID3DXEffect* g_pEffect = NULL;
DWORD dwShaderFlags = 0;

    dwShaderFlags |= D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_NO_PRESHADER;

    // Read the D3DX effect file
    WCHAR str[MAX_PATH];
    DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL.fx" );

    D3DXCreateEffectFromFile( 
        pd3dDevice, 
        str, 
        NULL, // CONST D3DXMACRO* pDefines,
        NULL, // LPD3DXINCLUDE pInclude,
        dwShaderFlags, 
        NULL, // LPD3DXEFFECTPOOL pPool,
        &g_pEffect, 
        NULL );
```



Cette fonction accepte les arguments suivants :

-   Périphérique.
-   Nom de fichier du fichier d’effet.
-   Pointeur vers une liste de définitions se terminant par un caractère NULL \# , à utiliser lors de l’analyse du nuanceur.
-   Pointeur facultatif vers un gestionnaire d’inclusion écrit par l’utilisateur. Le gestionnaire est appelé par le processeur à chaque fois qu’il doit résoudre un \# include.
-   Indicateur de compilation de nuanceur qui fournit aux indicateurs du compilateur la manière dont le nuanceur sera utilisé. Ces options sont les suivantes :
    -   La validation est ignorée, si des nuanceurs corrects connus sont en cours de compilation.
    -   L’optimisation est ignorée (parfois utilisée lorsque les optimisations compliquent le débogage).
    -   Demande d’inclure des informations de débogage dans le nuanceur afin de pouvoir les déboguer.
-   Pool d’effets. Si plusieurs effets utilisent le même pointeur de pool de mémoire, les variables globales dans les effets sont partagées les unes avec les autres. Si vous n’avez pas besoin de partager des variables d’effet, le pool de mémoire peut être défini sur la **valeur null**.
-   Pointeur vers le nouvel effet.
-   Pointeur vers une mémoire tampon dans laquelle les erreurs de validation peuvent être envoyées. Dans cet exemple, le paramètre a la valeur **null** et n’est pas utilisé.

> [!Note]  
> À partir du kit de développement logiciel (SDK) 2006 du mois de décembre, le compilateur HLSL DirectX 10 est désormais le compilateur par défaut dans DirectX 9 et DirectX 10. Pour plus d’informations [, consultez outil de compilateur Effect](../direct3dtools/fxc.md) .

 

## <a name="render-an-effect"></a>Rendu d’un effet

La séquence d’appels pour l’application de l’état d’effet à un appareil est la suivante :

-   [**ID3DXEffect :: Begin**](id3dxeffect--begin.md) définit la technique active.
-   [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md) définit la passe active.
-   [**ID3DXEffect :: CommitChanges**](id3dxeffect--commitchanges.md) met à jour les modifications apportées aux appels définis dans la passe. Cette méthode doit être appelée avant tout appel de dessin.
-   [**ID3DXEffect :: EndPass**](id3dxeffect--endpass.md) termine une passe.
-   [**ID3DXEffect :: end**](id3dxeffect--end.md) termine la technique active.

Le code d’effet de rendu est également plus simple que le code de rendu correspondant sans effet. Voici le code de rendu ayant un effet :


```
// Apply the technique contained in the effect 
g_pEffect->Begin(&cPasses, 0);

for (iPass = 0; iPass < cPasses; iPass++)
{
    g_pEffect->BeginPass(iPass);

    // Only call CommitChanges if any state changes have happened
    // after BeginPass is called
    g_pEffect->CommitChanges();

    // Render the mesh with the applied technique
    g_pMesh->DrawSubset(0);

    g_pEffect->EndPass();
}
g_pEffect->End();
```



La boucle de rendu consiste à interroger l’effet pour voir le nombre de passes qu’il contient, puis à appeler toutes les passes pour une technique. La boucle de rendu peut être développée pour appeler plusieurs techniques, chacune avec plusieurs passes.

## <a name="use-semantics-to-find-effect-parameters"></a>Utiliser la sémantique pour rechercher les paramètres d’effet

Une sémantique est un identificateur attaché à un paramètre Effect pour permettre à une application de rechercher le paramètre. Un paramètre ne peut avoir qu’une seule sémantique. La sémantique se trouve à la suite d’un signe deux-points ( :) après le nom du paramètre. Exemple :


```
float4x4 matWorldViewProj : WORLDVIEWPROJ;
```



Si vous avez déclaré la variable globale Effect sans utiliser de sémantique, elle ressemble à ceci :


```
float4x4 matWorldViewProj;
```



L’interface Effect peut utiliser une sémantique pour obtenir un handle à un paramètre d’effet particulier. Par exemple, le code suivant retourne le handle de la matrice :


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



En plus de la recherche par nom sémantique, l’interface Effect possède de nombreuses autres méthodes pour rechercher des paramètres.

## <a name="use-handles-to-get-and-set-parameters-efficiently"></a>Utiliser des handles pour récupérer et définir des paramètres efficacement

Les handles offrent un moyen efficace de faire référence à des paramètres d’effet, des techniques, des passes et des annotations avec un effet. Les handles (qui sont de type D3DXHANDLE) sont des pointeurs de chaîne. Les handles passés dans des fonctions telles que GetParameterxxx ou GetAnnotationxxx peuvent se présenter sous l’une des trois formes suivantes :

-   Handle retourné par une fonction telle que GetParameterxxx.
-   Chaîne contenant le nom du paramètre, de la technique, de la passe ou de l’annotation.
-   Handle ayant la valeur **null**.

Cet exemple retourne un handle au paramètre auquel la sémantique WORLDVIEWPROJ est attachée :


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



## <a name="add-parameter-information-with-annotations"></a>Ajouter des informations sur les paramètres avec des annotations

Les annotations sont des données spécifiques à l’utilisateur qui peuvent être attachées à n’importe quelle technique, passe ou paramètre. Une annotation est un moyen flexible d’ajouter des informations à des paramètres individuels. Les informations peuvent être lues et utilisées de la manière choisie par l’application. Une annotation peut être de n’importe quel type de données et peut être ajoutée dynamiquement. Les déclarations d’annotation sont délimitées par des crochets pointus. Une annotation contient les éléments suivants :

-   Type de données.
-   Nom de variable.
-   Signe égal (=).
-   Valeur de données.
-   Point-virgule de fin (;).

Par exemple, les deux exemples précédents de ce document contiennent cette annotation :


```
texture Tex0 < string name = "tiger.bmp"; >;
```



L’annotation est attachée à l’objet texture et spécifie le fichier de texture qui doit être utilisé pour initialiser l’objet texture. L’annotation n’initialise pas l’objet texture, il s’agit simplement d’une partie des informations utilisateur jointes à la variable. Une application peut lire l’annotation avec [**ID3DXBaseEffect :: GetAnnotation**](id3dxbaseeffect--getannotation.md) ou [**ID3DXBaseEffect :: GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md) pour retourner la chaîne. Les annotations peuvent également être ajoutées par l’application.

Chaque annotation :

-   Doit être de type numeric ou Strings.
-   Doit toujours être initialisé avec une valeur par défaut.
-   Peut être associé à des [techniques et des passes (Direct3D 9)](techniques-and-passes.md) et à des [paramètres d’effet](/previous-versions/windows/desktop/ee417539(v=vs.85))de niveau supérieur.
-   Peut être écrit et lu à l’aide de [**ID3DXEffect**](id3dxeffect.md) ou de [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).
-   Peut être ajouté avec [**ID3DXEffect**](id3dxeffect.md).
-   Ne peut pas être référencé à l’intérieur de l’effet.
-   Impossible d’avoir des sous-sémantiques ou des sous-annotations.

## <a name="share-effect-parameters"></a>Paramètres d’effet de partage

Les paramètres Effects sont toutes les variables non statiques déclarées dans un effet. Cela peut inclure des variables globales et des annotations. Les paramètres Effects peuvent être partagés entre différents effets en déclarant des paramètres avec le mot clé « Shared », puis en créant l’effet avec un pool d’effets.

Un pool d’effets contient des paramètres d’effet partagé. Le pool est créé en appelant [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md), qui retourne une interface [**ID3DXEffectPool**](id3dxeffectpool.md) . L’interface peut être fournie en tant qu’entrée à l’une des fonctions D3DXCreateEffectxxx lors de la création d’un effet. Pour qu’un paramètre soit partagé entre plusieurs effets, le paramètre doit avoir le même nom, le même type et la même sémantique dans chacun des effets partagés.


```
ID3DXEffectPool* g_pEffectPool = NULL;   // Effect pool for sharing parameters

    D3DXCreateEffectPool( &g_pEffectPool );
```



Les effets qui partagent des paramètres doivent utiliser le même appareil. Cela est appliqué pour empêcher le partage des paramètres dépendants du périphérique (tels que les nuanceurs ou les textures) sur différents appareils. Les paramètres sont supprimés du pool chaque fois que les effets qui contiennent les paramètres partagés sont libérés. Si les paramètres de partage ne sont pas nécessaires, fournissez la **valeur null** pour le pool d’effets lorsqu’un effet est créé.

Les effets clonés utilisent le même pool d’effets que l’effet à partir duquel ils sont clonés. Le clonage d’un effet fait une copie exacte d’un effet, y compris les variables globales, les techniques, les passes et les annotations.

## <a name="compile-an-effect-offline"></a>Compiler un effet hors connexion

Vous pouvez compiler un effet au moment de l’exécution avec [**D3DXCreateEffect**](d3dxcreateeffect.md), ou vous pouvez compiler un effet hors connexion à l’aide de l’outil de compilateur de ligne de commande fxc.exe. L’effet de l' [exemple CompiledEffect](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx) contient un nuanceur de sommets, un nuanceur de pixels et une technique :


```
// File: CompiledEffect.fx

// Global variables
float4 g_MaterialAmbientColor;    // Material's ambient color
...

// Texture samplers
sampler RenderTargetSampler = 
   ...

// Type: Vertex shader                                      
VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0 )
{
   ...
};
// Type: Pixel shader
PS_OUTPUT RenderScenePS( VS_OUTPUT In ) 
{ 
   ...
}

// Type: Technique                                     
technique RenderScene
{
    pass P0
    {          
        ZENABLE = true;
        VertexShader = compile vs_1_1 RenderSceneVS();
        PixelShader  = compile ps_1_1 RenderScenePS();
    }
}
```



L’utilisation de l' [outil Effect-compiler Tool](../direct3dtools/fxc.md) pour compiler le nuanceur pour vs \_ 1 \_ 1 a généré les instructions de nuanceur d’assembly suivantes :


```
//
// Generated by Microsoft (R) D3DX9 Shader Compiler 4.09.02.1188
//
//   fxc /T vs_1_1 /E RenderSceneVS /Fc CompiledEffect.txt CompiledEffect.fx
//
//
// Parameters:
//
//   float4 g_LightAmbient;
//   float4 g_LightDiffuse;
//   float3 g_LightDir;
//   float4 g_MaterialAmbientColor;
//   float4 g_MaterialDiffuseColor;
//   float g_fTime;
//   float4x4 g_mWorld;
//   float4x4 g_mWorldViewProjection;
//
//
// Registers:
//
//   Name                   Reg   Size
//   ---------------------- ----- ----
//   g_mWorldViewProjection c0       4
//   g_mWorld               c4       3
//   g_MaterialAmbientColor c7       1
//   g_MaterialDiffuseColor c8       1
//   g_LightDir             c9       1
//   g_LightAmbient         c10      1
//   g_LightDiffuse         c11      1
//   g_fTime                c12      1
//
//
// Default values:
//
//   g_LightDir
//     c9   = { 0.57735, 0.57735, 0.57735, 0 };
//
//   g_LightAmbient
//     c10  = { 1, 1, 1, 1 };
//
//   g_LightDiffuse
//     c11  = { 1, 1, 1, 1 };
//

    vs_1_1
    def c13, 0.159154937, 0.25, 6.28318548, -3.14159274
    def c14, -2.52398507e-007, 2.47609005e-005, -0.00138883968, 0.0416666418
    def c15, -0.5, 1, 0.5, 0
    dcl_position v0
    dcl_normal v1
    dcl_texcoord v2
    mov r0.w, c12.x
    mad r0.w, r0.w, c13.x, c13.y
    expp r3.y, r0.w
    mov r0.w, r3.y
    mad r0.w, r0.w, c13.z, c13.w
    mul r0.w, r0.w, r0.w
    mad r1.w, r0.w, c14.x, c14.y
    mad r1.w, r0.w, r1.w, c14.z
    mad r1.w, r0.w, r1.w, c14.w
    mad r1.w, r0.w, r1.w, c15.x
    mad r0.w, r0.w, r1.w, c15.y
    mul r0.w, r0.w, v0.x
    mul r0.x, r0.w, c15.z
    dp3 r1.x, v1, c4
    dp3 r1.y, v1, c5
    dp3 r1.z, v1, c6
    mov r0.yzw, c15.w
    dp3 r2.x, r1, r1
    add r0, r0, v0
    rsq r1.w, r2.x
    dp4 oPos.x, r0, c0
    mul r1.xyz, r1, r1.w
    dp4 oPos.y, r0, c1
    dp3 r1.x, r1, c9
    dp4 oPos.z, r0, c2
    max r1.w, r1.x, c15.w
    mov r1.xyz, c8
    mul r1.xyz, r1, c11
    mov r2.xyz, c7
    mul r2.xyz, r2, c10
    dp4 oPos.w, r0, c3
    mad oD0.xyz, r1, r1.w, r2
    mov oD0.w, c15.y
    mov oT0.xy, v2

// approximately 34 instruction slots used
```



## <a name="improve-performance-with-preshaders"></a>Améliorer les performances avec des prénuanceurs

Un prénuanceur est une technique permettant d’accroître l’efficacité du nuanceur en précalculant les expressions de nuanceur constantes. Le compilateur d’effet extrait automatiquement les calculs du nuanceur à partir du corps d’un nuanceur et les exécute sur le processeur avant l’exécution du nuanceur. Par conséquent, les prénuanceurs fonctionnent uniquement avec les effets. Par exemple, ces deux expressions peuvent être évaluées en dehors du nuanceur avant d’être exécutées.


```
mul(World,mul(View, Projection));
sin(time)
```



Les calculs de nuanceur qui peuvent être déplacés sont ceux associés à des paramètres uniformes. autrement dit, les calculs ne changent pas pour chaque vertex ou pixel. Si vous utilisez Effects, le compilateur d’effet génère et exécute automatiquement un préombrage pour vous. aucun indicateur à activer. Les prénuanceurs peuvent réduire le nombre d’instructions par nuanceur et peuvent également réduire le nombre de registres constants consommés par un nuanceur.

Imaginez le compilateur Effects comme une sorte de compilateur multiprocesseur, car il compile le code du nuanceur pour deux types de processeurs : un processeur et un GPU. En outre, le compilateur d’effet est conçu pour déplacer le code du GPU vers le processeur et, par conséquent, améliorer les performances du nuanceur. Cela est très similaire à l’extraction d’une expression statique à partir d’une boucle. Un nuanceur qui transforme la position à partir de l’espace universel en espace de projection, et qui copie des coordonnées de texture ressemble à ceci en HLSL :


```
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
float4x4 g_mWorldInverse;           // Inverse World matrix
float3 g_LightDir;                  // Light direction in world space
float4 g_LightDiffuse;              // Diffuse color of the light

struct VS_OUTPUT
{
    float4 Position   : POSITION;   // vertex position 
    float2 TextureUV  : TEXCOORD0;  // vertex texture coords 
    float4 Diffuse    : COLOR0;     // vertex diffuse color
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0)
{
    VS_OUTPUT Output;
    
    // Transform the position from object space to projection space
    Output.Position = mul(vPos, g_mWorldViewProjection);

    // Transform the light from world space to object space    
    float3 vLightObjectSpace = normalize(mul(g_LightDir, (float3x3)g_mWorldInverse)); 

    // N dot L lighting
    Output.Diffuse = max(0,dot(vNormal, vLightObjectSpace));
    
    // Copy the texture coordinate
    Output.TextureUV = vTexCoord0; 
    
    return Output;    
}
technique RenderVS
{
    pass P0
    {          
        VertexShader = compile vs_1_1 RenderSceneVS();
    }
}
```



L’utilisation de l' [outil Effect-compiler Tool](../direct3dtools/fxc.md) pour compiler le nuanceur pour vs \_ 1 \_ 1 génère les instructions d’assembly suivantes :


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //   g_mWorldInverse        c4       3
            //   g_LightDir             c7       1
            //
            
                vs_1_1
                def c8, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                mov r1.xyz, c7
                dp3 r0.x, r1, c4
                dp3 r0.y, r1, c5
                dp3 r0.z, r1, c6
                dp4 oPos.x, v0, c0
                dp3 r1.x, r0, r0
                dp4 oPos.y, v0, c1
                rsq r0.w, r1.x
                dp4 oPos.z, v0, c2
                mul r0.xyz, r0, r0.w
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, r0
                max oD0, r0.x, c8.x
                mov oT0.xy, v2
            
            // approximately 14 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



Cela utilise environ 14 emplacements et utilise 9 registres constants. Avec un prénuancier, le compilateur déplace les expressions statiques hors du nuanceur et dans le prénuancier. Le même nuanceur doit ressembler à ceci avec un prénuanceur :


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //
            //
            // Registers:
            //
            //   Name            Reg   Size
            //   --------------- ----- ----
            //   g_mWorldInverse c0       3
            //   g_LightDir      c3       1
            //
            
                preshader
                dot r0.x, c3.xyz, c0.xyz
                dot r0.y, c3.xyz, c1.xyz
                dot r0.z, c3.xyz, c2.xyz
                dot r1.w, r0.xyz, r0.xyz
                rsq r0.w, r1.w
                mul c4.xyz, r0.w, r0.xyz
            
            // approximately 6 instructions used
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //
            
                vs_1_1
                def c5, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                dp4 oPos.x, v0, c0
                dp4 oPos.y, v0, c1
                dp4 oPos.z, v0, c2
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, c4
                max oD0, r0.x, c5.x
                mov oT0.xy, v2
            
            // approximately 7 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



Un effet exécute un préombrage juste avant d’exécuter un nuanceur. Le résultat est la même fonctionnalité avec des performances de nuanceur accrues, car le nombre d’instructions qui doivent être exécutées (pour chaque vertex ou pixel selon le type de nuanceur) a été réduit. En outre, moins de registres constants sont consommés par le nuanceur en raison des expressions statiques déplacées dans le prénuancier. Cela signifie que les nuanceurs précédemment limités par le nombre de registres de constantes qu’ils avaient nécessaires peuvent maintenant être compilés, car ils nécessitent moins de registres constants. Il est raisonnable d’attendre 5% et une amélioration des performances de 20% par rapport aux prénuanceurs.

Gardez à l’esprit que les constantes d’entrée sont différentes des constantes de sortie dans un prénuancier. La sortie C1 n’est pas la même que le registre d’entrée C1. L’écriture dans un registre de constante dans un prénuanceur écrit en fait dans l’emplacement d’entrée (constante) du nuanceur correspondant.


```
// BaseDelta c0 1
// Refinements c1 1
preshader
mul c1.x, c0.x, (-2)
add c0.x, c0.x, c0.x
cmp c5.x, c1.x, (1), (0)
```



L’instruction CMP ci-dessus lira la valeur C1 du prénuancier, tandis que l’instruction mul écrira dans les registres de nuanceur de matériel pour être utilisée par le nuanceur de sommets.

## <a name="use-parameter-blocks-to-manage-effect-parameters"></a>Utiliser des blocs de paramètres pour gérer les paramètres d’effet

Les blocs de paramètres sont des blocs de modifications de l’état d’effet. Un bloc de paramètres peut enregistrer des modifications d’État afin qu’elles puissent être appliquées ultérieurement avec un seul appel. Créez un bloc de paramètres en appelant [**ID3DXEffect :: BeginParameterBlock**](id3dxeffect--beginparameterblock.md):


```
    m_pEffect->SetTechnique( "RenderScene" );

    m_pEffect->BeginParameterBlock();
    D3DXVECTOR4 v4( Diffuse.r, Diffuse.g, Diffuse.b, Diffuse.a );
    m_pEffect->SetVector( "g_vDiffuse", &v4 );
    m_pEffect->SetFloat( "g_fReflectivity", fReflectivity );
    m_pEffect->SetFloat( "g_fAnimSpeed", fAnimSpeed );
    m_pEffect->SetFloat( "g_fSizeMul", fSize );
    m_hParameters = m_pEffect->EndParameterBlock();
```



Le bloc de paramètres enregistre quatre modifications appliquées par les appels d’API. L’appel de [**ID3DXEffect :: BeginParameterBlock**](id3dxeffect--beginparameterblock.md) démarre l’enregistrement des modifications d’État. [**ID3DXEffect :: EndParameterBlock**](id3dxeffect--endparameterblock.md) arrête l’ajout des modifications au bloc de paramètres et retourne un handle. Le descripteur est utilisé lors de l’appel de [**ID3DXEffect :: ApplyParameterBlock**](id3dxeffect--applyparameterblock.md).

Dans l' [exemple EffectParam](https://msdn.microsoft.com/library/Ee417535(v=VS.85).aspx), le bloc de paramètres est appliqué dans la séquence de rendu :


```
CObj g_aObj[NUM_OBJS];       // Object instances

    if( SUCCEEDED( pd3dDevice->BeginScene() ) )
    {
        // Set the shared parameters using the first mesh's effect.

        // Render the mesh objects
        for( int i = 0; i < NUM_OBJS; ++i )
        {
            ID3DXEffect *pEffect = g_aObj[i].m_pEffect;

            // Apply the parameters
            pEffect->ApplyParameterBlock( g_aObj[i].m_hParameters );

            ...

            pEffect->Begin( &cPasses, 0 );
            for( iPass = 0; iPass < cPasses; iPass++ )
            {
              ...
            }
            pEffect->End();
        }

        ...
        pd3dDevice->EndScene();
    }
```



Le bloc de paramètres définit la valeur des quatre modifications d’État juste avant l’appel de [**ID3DXEffect :: Begin**](id3dxeffect--begin.md) . Les blocs de paramètres sont un moyen pratique de définir plusieurs modifications d’État avec un seul appel d’API.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets](effects.md)
</dt> </dl>

 

 
