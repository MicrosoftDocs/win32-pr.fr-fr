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
ms.openlocfilehash: 2e0735e3d9945d15c2f8473155612a40cbf652349eb531f089f5a4aa44451484
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509281"
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

## <a name="remarks"></a>Remarques

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[RWTexture1DArray](sm5-object-rwtexture1darray.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




