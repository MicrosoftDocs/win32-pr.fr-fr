---
title: 'RWStructuredBuffer :: GetDimensions,, fonction'
description: 'Obtient les dimensions de ressource. | RWStructuredBuffer :: GetDimensions,, fonction'
ms.assetid: 842b3d21-2e2b-4906-93ee-0252b2e8cf85
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
ms.openlocfilehash: 760a546d7d60afbb41438416a9602ab55981834acd9969bc535c9a82df6e5e50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789925"
---
# <a name="rwstructuredbuffergetdimensions-function"></a>RWStructuredBuffer :: GetDimensions,, fonction

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

Nombre de structures dans la ressource.

</dd> <dt>

*Stride* \[ à\]
</dt> <dd>

Type : **uint**

STRIDE, en octets, de chaque élément de structure.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Rien

## <a name="remarks"></a>Remarques

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[RWStructuredBuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




