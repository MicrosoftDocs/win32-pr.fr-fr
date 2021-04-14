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
ms.openlocfilehash: 93db905ae40f1bec7488eca292f4ea44d87950d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973919"
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

## <a name="remarks"></a>Notes

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[AppendStructuredBuffer](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




