---
title: 'RWBuffer :: Operator, fonction'
description: 'Retourne une variable de ressource. | RWBuffer :: Operator, fonction'
ms.assetid: 59e5e4ec-ff0d-43aa-805a-04b79f5ab57f
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
ms.openlocfilehash: 40336c8ad6ee9e8008b82c172f1a5b863e967c0d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991877"
---
# <a name="rwbufferoperator--function"></a>RWBuffer :: Operator, fonction

Retourne une variable de ressource.

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

Position d’index.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **R**

Variable de ressource.

## <a name="remarks"></a>Notes

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[RWBuffer](sm5-object-rwbuffer.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




