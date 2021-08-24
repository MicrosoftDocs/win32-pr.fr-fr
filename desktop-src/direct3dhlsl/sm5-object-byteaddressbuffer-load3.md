---
title: 'ByteAddressBuffer :: Load3 (uint), fonction'
description: 'Obtient trois valeurs. | ByteAddressBuffer :: Load3 (uint), fonction'
ms.assetid: 79afeb36-e0e7-44a2-b252-8e3577f4c1a5
keywords:
- Load3 fonction HLSL
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bd36958eb2c16d45e6228c9919cb22bb772c8861131c26710fff032276bce6e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510009"
---
# <a name="byteaddressbufferload3uint-function"></a>ByteAddressBuffer :: Load3 (uint), fonction

Obtient trois valeurs.

## <a name="syntax"></a>Syntaxe

``` syntax
uint3 Load3(
  in uint address
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*adresse* \[ dans\]
</dt> <dd>

Type : **uint**

Adresse d’entrée en octets, qui doit être un multiple de 4.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **uint3**

Trois valeurs.

## <a name="remarks"></a>Remarques

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes Load3](byteaddressbuffer-load3.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




