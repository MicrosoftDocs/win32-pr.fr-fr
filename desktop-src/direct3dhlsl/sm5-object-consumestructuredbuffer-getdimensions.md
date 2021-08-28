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
ms.openlocfilehash: 5cc7c7c9234d00343f91a3fcb137eed65b95515a07f765cf8fce6893e2d4998a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788389"
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

## <a name="remarks"></a>Remarques

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ConsumeStructuredBuffer](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




