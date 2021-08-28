---
title: 'Texture1D :: Operator, fonction'
description: Retourne une variable de ressource en lecture seule pour un Texture1D.
ms.assetid: df54097d-4d1b-496a-a17d-6e9a10cfb996
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
ms.openlocfilehash: d2c11ef313531adb9b129ffb99103ea6c7778462eddf8c1c76f4b235c92951c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985909"
---
# <a name="texture1doperator--function"></a>Texture1D :: Operator, fonction

Retourne une variable de ressource en lecture seule pour un [**Texture1D**](sm5-object-texture1d.md).

## <a name="syntax"></a>Syntaxe

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*pos* \[ dans\]
</dt> <dd>

Type : **uint**

Position d’index. Contient la coordonnée x.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **R**

Variable de ressource en lecture seule.

## <a name="remarks"></a>Remarques

Cette méthode accède toujours au premier niveau MIP. Pour spécifier d’autres niveaux MIP, utilisez plutôt l' [**opérateur \[ \] \[ \] MIP.**](sm5-object-texture1d-mipsoperatorindex.md)

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Texture1D](sm5-object-texture1d.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




