---
title: 'ConsumeStructuredBuffer :: GetDimensions,, fonction'
description: 'Obtient les dimensions de ressource. | ConsumeStructuredBuffer :: GetDimensions,, fonction'
ms.assetid: 0710a4fb-23b0-4b19-b9ed-21bbb9874d33
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
ms.openlocfilehash: a204ed44c90c60b327ceb201037c6758763b3a05
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991881"
---
# <a name="consumestructuredbuffergetdimensions-function"></a>ConsumeStructuredBuffer :: GetDimensions,, fonction

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

STRIDE, en octets, de chaque élément.

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

[ConsumeStructuredBuffer](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




