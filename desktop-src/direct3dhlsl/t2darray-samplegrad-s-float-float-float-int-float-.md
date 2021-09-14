---
title: 'Fonction SampleGrad :: SampleGrad (S, float, float, float, int, float) pour Texture2DArray'
description: Découvrez comment cette fonction échantillonne une texture, en utilisant un dégradé pour influencer la manière dont l’emplacement de l’échantillon est calculé, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à. Pour Texture2DArray.
ms.assetid: CBC940D5-FC09-498D-9C7A-3CBAB2EC2D4D
keywords:
- SampleGrad fonction HLSL
topic_type:
- apiref
api_name:
- SampleGrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 032d2b228800ffca654704c85a72d5ada76e65ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127236922"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture2darray"></a>Fonction SampleGrad :: SampleGrad (S, float, float, float, int, float) pour Texture2DArray

Échantillonne une texture en utilisant un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.

## <a name="syntax"></a>Syntaxe


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

 \[ Dans\]
</dt> <dd>

Type : **SamplerState**

État de l' [échantillonneur](dx-graphics-hlsl-sampler.md). Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.

</dd> <dt>

*Emplacement* \[ dans\]
</dt> <dd>

Type : **float**

Coordonnées de texture. Le type d’argument est dépendant du type de texture-objet.



| Type de Texture-Object                    | Type de paramètre |
|----------------------------------------|----------------|
| Texture1D                              | float          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*Ddx* \[ dans\]
</dt> <dd>

Type : **float**

Taux de modification de la géométrie de la surface dans l’axe x. Le type d’argument est dépendant du type de texture-objet.



| Type de Texture-Object                      | Type de paramètre |
|------------------------------------------|----------------|
| Texture1D, Texture1DArray                | float          |
| Texture2D, Texture2DArray                | float2         |
| Texture3D, TextureCube, TextureCubeArray | float3         |
| Texture2DMS, Texture2DMSArray            | non pris en charge  |



 

</dd> <dt>

*Ddy* \[ dans\]
</dt> <dd>

Type : **float**

Taux de modification de la géométrie de la surface dans l’axe y. Le type d’argument est dépendant du type de texture-objet.



| Type de Texture-Object                      | Type de paramètre |
|------------------------------------------|----------------|
| Texture1D, Texture1DArray                | float          |
| Texture2D, Texture2DArray                | float2         |
| Texture3D, TextureCube, TextureCubeArray | float3         |
| Texture2DMS, Texture2DMSArray            | non pris en charge  |



 

</dd> <dt>

*Décalage* \[ dans\]
</dt> <dd>

Type : **int**

Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage. Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel. Le type d’argument est dépendant du type de texture-objet. Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).



| Type de Texture-Object           | Type de paramètre |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | int            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | non pris en charge  |



 

</dd> <dt>

*Clamp* \[ dans\]
</dt> <dd>

Type : **float**

Valeur facultative pour fixer l’exemple de valeurs LOD à. Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes SampleGrad](texture2darray-samplegrad.md)
</dt> <dt>

[**Texture2DArray**](sm5-object-texture2darray.md)
</dt> </dl>

 

 
