---
title: 'Texture1DArray :: Operator, fonction'
description: 'Retourne une variable de ressource en lecture seule. | Texture1DArray :: Operator, fonction'
ms.assetid: 05ec9652-b5dd-41cf-8bef-730c507c5ba4
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
ms.openlocfilehash: 578d778cd1e0e064c435c19fb094feb66f651e05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126851757"
---
# <a name="texture1darrayoperator--function"></a>Texture1DArray :: Operator, fonction

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

Position d’index. Le premier composant contient la coordonnée x. Le deuxième composant indique la tranche de tableau souhaitée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **R**

Variable de ressource en lecture seule.

## <a name="remarks"></a>Notes

Cette méthode accède toujours au premier niveau MIP. Pour spécifier d’autres niveaux MIP, utilisez plutôt la méthode [**MIP. Operator \[ \] \[ \]**](sm5-object-texture1darray-mipsoperatorindex.md) .

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Texture1DArray](sm5-object-texture1darray.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




