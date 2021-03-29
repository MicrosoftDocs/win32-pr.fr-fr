---
title: 'Texture2D :: Operator, fonction'
description: 'Retourne une variable de ressource en lecture seule. | Texture2D :: Operator, fonction'
ms.assetid: 72ba3fc8-04c3-479a-b307-525020898bac
keywords:
- Fonction d’opérateur HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2c397b1b80836f48cb856d03ccdf52ad2c95ce48
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974223"
---
# <a name="texture2doperator--function"></a>Texture2D :: Operator, fonction

Retourne une variable de ressource en lecture seule.

## <a name="syntax"></a>Syntaxe

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*pos* \[ dans\]
</dt> <dd>

Type : **uint2**

Position d’index. Contient les coordonnées (x, y).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **R**

Variable de ressource en lecture seule.

## <a name="remarks"></a>Notes

Cette méthode accède toujours au premier niveau MIP. Pour spécifier d’autres niveaux MIP, utilisez plutôt la méthode [**MIP. Operator \[ \] \[ \]**](sm5-object-texture2d-mipsoperatorindex.md) .

Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Texture2D](sm5-object-texture2d.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




