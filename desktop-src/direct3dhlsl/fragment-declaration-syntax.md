---
title: Syntaxe de la déclaration de fragment (Direct3D 9 HLSL)
description: Chaque fonction HLSL (High Level Shader Language) de Microsoft peut être convertie en fragment de nuanceur avec l’ajout d’une déclaration de fragment.
ms.assetid: 34ceef8c-8fb9-4c73-86cc-014b7a2ee4d7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 60ac1153ff3491bc904f4f759f6653cb4243adff
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825726"
---
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a>Syntaxe de la déclaration de fragment (Direct3D 9 HLSL)

Chaque fonction HLSL (High Level Shader Language) de Microsoft peut être convertie en fragment de nuanceur avec l’ajout d’une déclaration de fragment.

## <a name="syntax"></a>Syntaxe


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



où :



| Valeur                  | Description                                                                                                                                                                                                                                                      |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fragmentKeyword   | Mot clé requis. Pixelfragment ou vertexfragment.                                                                                                                                                                                             |
| FragmentName      | Chaîne de texte ASCII qui spécifie le nom du fragment compilé.                                                                                                                                                                                       |
| fragment de compilation \_ | Mot clé requis.                                                                                                                                                                                                                                     |
| shaderProfile     | Modèle de nuanceur à compiler. Tout profil de nuanceur de sommets valide (consultez [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) ou profil de nuanceur de pixels (voir [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)). |
| Nomfonction ()    | Nom de la fonction de nuanceur, suivi de parenthèses.                                                                                                                                                                                                    |



 

Les paramètres de fragment partagés sont marqués en ajoutant un \_ préfixe’r’à leur sémantique.


```
void AmbientDiffuse( float3 vPosWorld: r_PosWorld,
                     float3 vNormalWorld: r_NormalWorld,
                     out float4 vColor: COLOR0 )
{  
    // Compute the light vector
    float3 vLight = normalize( g_vLightPosition - vPosWorld );
    
    // Compute the ambient and diffuse components of illumination
    vColor = g_vLightColor * g_vMaterialAmbient;
    vColor += g_vLightColor * g_vMaterialDiffuse * saturate( dot( vLight, vNormalWorld ) );
}
vertexfragment AmbientDiffuseFragment = compile_fragment vs_1_1 AmbientDiffuse();
```



Dans cet exemple, les \_ sémantiques r PosWorld et r \_ NormalWorld identifient que ces deux paramètres sont des paramètres partagés parmi d’autres fragments.

> [!Note]  
> L’éditeur de liens de fragment était une technologie Microsoft Direct3D 9 dans D3DX 9. Fragment Linker était un outil (Flink.exe), une API D3DX 9 et une amélioration HLSL. L’éditeur de liens de fragment a été supprimé depuis la version du SDK DirectX du 2009 août. L’éditeur de liens fragment n’est jamais appliqué à Microsoft Direct3D 10, Microsoft Direct3D 10,1 ou Microsoft Direct3D 11.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
