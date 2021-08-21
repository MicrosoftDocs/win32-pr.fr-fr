---
title: Syntaxe des fonctions Effect (Direct3D 11)
description: Une fonction Effect est écrite en langage HLSL et est déclarée avec la syntaxe décrite dans cette section.
ms.assetid: 5e12ba65-98bf-4f21-be75-602687157eb1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 945f7104d44947f37af71ce664dd99ff64362062b1d42af62af2054538bacb52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046617"
---
# <a name="effect-function-syntax-direct3d-11"></a>Syntaxe des fonctions Effect (Direct3D 11)

Une fonction Effect est écrite en langage HLSL et est déclarée avec la syntaxe décrite dans cette section.

## <a name="syntax"></a>Syntaxe

 *Nomdefonction nomfonction* ( \[ *argumentlist* \] )

{

<dl> \[ *Instructions* \]
</dl>

};



| Name         | Description                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReturnType   | Tout [type HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)                                                                                                                                                                                                       |
| FunctionName | Chaîne ASCII qui identifie de façon unique le nom de la fonction de nuanceur.                                                                                                                                                                                            |
| ArgumentList | Un ou plusieurs arguments, séparés par des virgules (consultez [arguments de fonction (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)).                                                                                                                             |
| Instructions   | Une ou plusieurs instructions (consultez [instructions (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)) qui composent le corps de la fonction. Si une fonction est définie sans corps, elle est considérée comme un prototype ; et doivent être redéfinis avec un corps avant l’utilisation. |



 

Une fonction Effect peut être un nuanceur ou il peut simplement s’agir d’une fonction appelée par un nuanceur. Une fonction est identifiée de manière unique par son nom, les types de ses paramètres et la plateforme cible ; par conséquent, les fonctions peuvent être surchargées. Toute fonction HLSL valide doit respecter ce format ; pour obtenir une liste plus détaillée de la syntaxe des fonctions HLSL, consultez [fonctions (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions).

## <a name="example"></a>Exemples

Voici un exemple de fonction de nuanceur de pixels.


```
       
PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    // Lookup mesh texture and modulate it with diffuse
    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) *  
                              In.Diffuse;
    else
        Output.RGBColor = In.Diffuse;

    return Output;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format d’effet](d3d11-effect-format.md)
</dt> </dl>

 

 