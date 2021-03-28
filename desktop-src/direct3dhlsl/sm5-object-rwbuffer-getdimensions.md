---
title: 'RWBuffer :: GetDimensions,, fonction'
description: 'Obtient la longueur de la mémoire tampon. | RWBuffer :: GetDimensions,, fonction'
ms.assetid: 600147cb-9513-4b74-a873-1ed22b31cdf7
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
ms.openlocfilehash: 98e419d3e77a27f211f0e063573caffcd6c61ce8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992065"
---
# <a name="rwbuffergetdimensions-function"></a>RWBuffer :: GetDimensions,, fonction

Obtient la longueur de la mémoire tampon.

## <a name="syntax"></a>Syntaxe

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*Dim* \[ out\]
</dt> <dd>

Type : **uint**

Longueur, en octets, de la mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Rien

## <a name="remarks"></a>Notes

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[RWBuffer](sm5-object-rwbuffer.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




