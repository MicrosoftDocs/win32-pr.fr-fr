---
title: 'RWTexture1DArray :: Operator, fonction'
description: 'Retourne une variable de ressource. | RWTexture1DArray :: Operator, fonction'
ms.assetid: 7047e670-dd78-4b73-8d80-5575e458f27c
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
ms.openlocfilehash: 6f8623ab25b42f6865e401c5b263a1774206c752
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974227"
---
# <a name="rwtexture1darrayoperator--function"></a>RWTexture1DArray :: Operator, fonction

Retourne une variable de ressource.

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

## <a name="return-value"></a>Valeur retournée

Type : **R**

Variable de ressource.

## <a name="remarks"></a>Notes

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[RWTexture1DArray](sm5-object-rwtexture1darray.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




