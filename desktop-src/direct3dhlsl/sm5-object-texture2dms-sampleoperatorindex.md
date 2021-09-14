---
title: 'Texture2DMS :: Sample. Operator, fonction'
description: 'Récupère une valeur de la ressource à l’emplacement et l’exemple d’index fournis. | Texture2DMS :: Sample. Operator, fonction'
ms.assetid: 5bc24129-b690-44dd-ae85-8533b10befaa
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
ms.openlocfilehash: 1a73577fa67992b212b4769059f1523e584acbaf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922292"
---
# <a name="texture2dmssampleoperator----function"></a>Texture2DMS :: Sample. Operator, fonction

Récupère une valeur de la ressource à l’emplacement et l’exemple d’index fournis.

## <a name="syntax"></a>Syntaxe

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint2 pos
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

Type : **uint2**

Position d’index. Les composants contiennent les coordonnées (x, y).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **R**

Variable de ressource en lecture seule.

## <a name="remarks"></a>Notes

### <a name="usage-example"></a>Exemple d'utilisation


```
Texture2DMS<float4, 8> tex;

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

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




