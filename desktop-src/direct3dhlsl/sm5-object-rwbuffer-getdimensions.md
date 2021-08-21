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
ms.openlocfilehash: 586f266fea0dbc035e8ff3a61e39cb18a7102d792ee05c44345a1b702cc1b574
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118239"
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

## <a name="remarks"></a>Remarques

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[RWBuffer](sm5-object-rwbuffer.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




