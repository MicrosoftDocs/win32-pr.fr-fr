---
title: 'Texture2DMSArray :: Sample. Operator, fonction'
description: 'Retourne une variable de ressource en lecture seule. | Texture2DMSArray :: Sample. Operator, fonction'
ms.assetid: 5334c1d5-dfbd-4987-875c-0b92967b0f13
keywords:
- exemple. Fonction d’opérateur HLSL
topic_type:
- apiref
api_name:
- sample.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e78746e0afe03e65a313982ca35c27a75ea14f1b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974379"
---
# <a name="texture2dmsarraysampleoperator----function"></a>Texture2DMSArray :: Sample. Operator, fonction

Retourne une variable de ressource en lecture seule.

## <a name="syntax"></a>Syntaxe

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint3 pos
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*sampleSlice* \[ dans\]
</dt> <dd>

Type : **uint**

Exemple d’index de la tranche.

</dd> <dt>

*pos* \[ dans\]
</dt> <dd>

Type : **uint3**

Position d’index. Le premier et le deuxième composant contiennent les coordonnées (x, y). Le troisième composant indique la tranche de tableau souhaitée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **R**

Variable de ressource en lecture seule.

## <a name="remarks"></a>Notes

### <a name="usage-example"></a>Exemple d'utilisation


```
Texture2DMSArray<float4, 4> alpha;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




