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
ms.openlocfilehash: 09ac18e7830dfe6b18718deed56e8495ba476dcedcb8290eab4e16aa0d7f24fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508324"
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

## <a name="remarks"></a>Remarques

### <a name="usage-example"></a>Exemple d'utilisation


```
Texture2DMSArray<float4, 4> alpha;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




