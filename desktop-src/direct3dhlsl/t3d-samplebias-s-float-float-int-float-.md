---
title: 'Fonction SampleBias :: SampleBias (S, float, float, int, float) pour Texture3D'
description: 'La fonction SampleBias :: SampleBias (S, float, float, int, float) de Texture3D échantillonne une texture après avoir appliqué la valeur de biais au niveau du mipmap.'
keywords:
- SampleBias fonction HLSL
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c7ef038a3faa4cb0a208e9a9d05de230d2b87231
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122445"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function-for-texture3d"></a>Fonction SampleBias :: SampleBias (S, float, float, int, float) pour Texture3D

Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.

## <a name="syntax"></a>Syntaxe


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
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

*Biais* \[ dans\]
</dt> <dd>

Type : **float**

La valeur de biais, qui est un nombre à virgule flottante compris entre 0,0 et 1,0 inclus, est appliquée à un niveau MIP avant l’échantillonnage.

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

[Méthodes SampleBias](texture3d-samplebias.md)
</dt> <dt>

[**Texture3D**](sm5-object-texture3d.md)
</dt> </dl>

 

 
