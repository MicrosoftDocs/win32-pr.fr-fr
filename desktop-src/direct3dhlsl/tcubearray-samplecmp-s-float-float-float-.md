---
title: 'Fonction SampleCmp :: SampleCmp (S, float, float, float) pour TextureCubeArray'
description: 'Échantillonne une texture, en utilisant une valeur de comparaison pour rejeter les exemples, avec une valeur facultative pour fixer des exemples de valeurs de niveau de détail (LOD) à. | Fonction SampleCmp :: SampleCmp (S, float, float, float) pour TextureCubeArray'
ms.assetid: A8824A82-A3FD-4FEE-BC10-56843997BBCE
keywords:
- SampleCmp fonction HLSL
topic_type:
- apiref
api_name:
- SampleCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e65b1747d03b3a0555267f7b57e95a4d5aba54da
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982642"
---
# <a name="samplecmpsamplecmpsfloatfloatfloat-function-for-texturecubearray"></a>Fonction SampleCmp :: SampleCmp (S, float, float, float) pour TextureCubeArray

Échantillonne une texture, en utilisant une valeur de comparaison pour rejeter les exemples, avec une valeur facultative pour fixer des exemples de valeurs de niveau de détail (LOD) à.

## <a name="syntax"></a>Syntaxe


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
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

*CompareValue* \[ dans\]
</dt> <dd>

Type : **float**

Valeur à virgule flottante à utiliser comme valeur de comparaison.

</dd> <dt>

*Clamp* \[ dans\]
</dt> <dd>

Type : **float**

Valeur facultative pour fixer l’exemple de valeurs LOD à. Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes SampleCmp](texturecubearray-samplecmp.md)
</dt> <dt>

[**TextureCubeArray**](texturecubearray.md)
</dt> </dl>

 

 
