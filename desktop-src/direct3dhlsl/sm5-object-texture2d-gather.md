---
title: 'Texture2D :: Gather (S, float, int) (fonction)'
description: 'Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire. | Texture2D :: Gather (S, float, int) (fonction)'
ms.assetid: 5d196c1c-8cc9-4add-9d33-654294314ee2
keywords:
- Fonction de collecte HLSL
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d0a58be0580572441f91a3b3f637601d70cd9c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761761"
---
# <a name="texture2dgathersfloatint-function"></a>Texture2D :: Gather (S, float, int) (fonction)

Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.

## <a name="syntax"></a>Syntaxe

``` syntax
TemplateType Gather(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

 \[ dans\]
</dt> <dd>

Type : **échantillonneur**

Index de base zéro de l’échantillonneur.

</dd> <dt>

*emplacement* \[ dans\]
</dt> <dd>

Type : **float2**

Les coordonnées de l’échantillon (u, v).

</dd> <dt>

*décalage* \[ dans\]
</dt> <dd>

Type : **Int2**

Décalage appliqué aux coordonnées de texture avant l’échantillonnage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **TemplateType**

Valeur à quatre composants dont le type est identique au type de modèle.

## <a name="remarks"></a>Notes

Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes de collecte](texture2d-gather.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




