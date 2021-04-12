---
description: Une fonction Effect est écrite en langage HLSL et est déclarée avec la syntaxe suivante.
ms.assetid: 5ac85f09-50ac-4e8f-b4d2-ae8306b59348
title: Syntaxe des fonctions Effect (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88521eeb85d1e5f54500a045fe5dcfd81d6be2cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483200"
---
# <a name="effect-function-syntax-direct3d-10"></a>Syntaxe des fonctions Effect (Direct3D 10)

Une fonction Effect est écrite en langage HLSL et est déclarée avec la syntaxe suivante.

## <a name="syntax"></a>Syntaxe

 *Nomdefonction nomfonction* ( \[ *argumentlist* \] )

{

<dl> \[ *Instructions* \]
</dl>

};



| Nom         | Description                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReturnType   | Tout [type HLSL](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md)                                                                                                                                                                                                       |
| FunctionName | Chaîne ASCII qui identifie de façon unique le nom de la fonction de nuanceur.                                                                                                                                                                                            |
| ArgumentList | Un ou plusieurs arguments, séparés par des virgules (consultez [arguments de fonction (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-function-parameters.md)).                                                                                                                             |
| Instructions   | Une ou plusieurs instructions (consultez [instructions (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-statements.md)) qui composent le corps de la fonction. Si une fonction est définie sans corps, elle est considérée comme un prototype ; et doivent être redéfinis avec un corps avant l’utilisation. |



 

Une fonction Effect peut être un nuanceur ou il peut simplement s’agir d’une fonction appelée par un nuanceur. Une fonction est identifiée de manière unique par son nom, les types de ses paramètres et la plateforme cible ; par conséquent, les fonctions peuvent être surchargées. Toute fonction HLSL valide doit respecter ce format ; pour obtenir une liste plus détaillée de la syntaxe des fonctions HLSL, consultez [fonctions (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-functions.md).

## <a name="example"></a>Exemple

L' [exemple BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) utilise à la fois un nuanceur de pixels et un nuanceur de sommets. La fonction de nuanceur de pixels est appelée RenderScenePS et est illustrée ci-dessous.


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

[Format d’effet](d3d10-effect-format.md)
</dt> </dl>

 

 
