---
title: Append (objet Stream-Output HLSL DirectX)
description: Ajoutez Geometry-Shader-output Data à un flux existant.
ms.assetid: 7df51383-7fc7-4a6f-aaa2-6c929f0443a3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 19d767f3c501cc42e21bbc44a196ba08cd6f1883
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120184"
---
# <a name="append-directx-hlsl-stream-output-object"></a>Append (objet Stream-Output HLSL DirectX)

Ajoutez Geometry-Shader-output Data à un flux existant.

Append ( *StreamDataType*);



 

## <a name="parameters"></a>Paramètres



| Élément                                                                                                                             | Description                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**<br/> | Description de l’entrée de données. Cette description doit correspondre au paramètre de modèle Stream-Object appelé [DataType](dx-graphics-hlsl-so-type.md).<br/> |



 

## <a name="return-value"></a>Valeur de retour

None

## <a name="example"></a>Exemple

Cet extrait de code (à partir de l' [exemple CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) illustre un exemple partiel d’ajout de primitives de bandes de triangles à un objet de sortie de flux.


```
[maxvertexcount(18)]
void GS_CubeMap( triangle GS_CUBEMAP_IN input[3], 
                 inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream )
{
    for( int f = 0; f < 6; ++f )
    {
        // Compute screen coordinates
        PS_CUBEMAP_IN output;
        output.RTIndex = f;
        for( int v = 0; v < 3; v++ )
        {
            output.Pos = mul( input[v].Pos, g_mViewCM[f] );
            output.Pos = mul( output.Pos, mProj );
            output.Tex = input[v].Tex;
            CubeMapStream.Append( output );
        }
        CubeMapStream.RestartStrip();
    }
}
```



## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | yes       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Stream-sortie (objet)](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

 





