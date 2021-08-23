---
title: 'RWTexture2D :: Operator, fonction'
description: 'Retourne une variable de ressource. | RWTexture2D :: Operator, fonction'
ms.assetid: 339dba7d-b0c6-4112-ae40-555661577a3e
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
ms.openlocfilehash: 4da16a89eb704e924931b8d3b4e5144d7154eed50f298aa0606b9b0fb5a45f46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985999"
---
# <a name="rwtexture2doperator--function"></a>RWTexture2D :: Operator, fonction

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

Position d’index. Contient les coordonnées (x, y).

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

[RWTexture2D](sm5-object-rwtexture2d.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




