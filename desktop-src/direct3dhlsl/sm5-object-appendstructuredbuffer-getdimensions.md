---
title: 'AppendStructuredBuffer :: GetDimensions,, fonction'
description: 'Obtient les dimensions de ressource. | AppendStructuredBuffer :: GetDimensions,, fonction'
ms.assetid: 41ed86d5-25c0-48bd-add9-792eb89605c3
keywords:
- GetDimensions, fonction HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96f40417834b8e23a9e746e4e4e3df93b96c1fc2affc7cd9147842e389dc99d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790650"
---
# <a name="appendstructuredbuffergetdimensions-function"></a>AppendStructuredBuffer :: GetDimensions,, fonction

Obtient les dimensions de ressource.

## <a name="syntax"></a>Syntaxe

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*numStructs* \[ à\]
</dt> <dd>

Type : **uint**

Nombre de structures.

</dd> <dt>

*Stride* \[ à\]
</dt> <dd>

Type : **uint**

Nombre d’octets dans chaque élément.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[AppendStructuredBuffer](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




