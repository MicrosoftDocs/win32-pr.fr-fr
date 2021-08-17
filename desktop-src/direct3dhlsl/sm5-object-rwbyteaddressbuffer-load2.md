---
title: 'RWByteAddressBuffer :: Load2 (uint), fonction'
description: 'Obtient deux valeurs. | RWByteAddressBuffer :: Load2 (uint), fonction'
ms.assetid: a00396cb-e68d-479e-ab3f-4c52f2cfc3bc
keywords:
- Load2 fonction HLSL
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f71fd2d0585803fb10de3fddfa29c10838d73e32ba7d63b5619be91b042cb71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725056"
---
# <a name="rwbyteaddressbufferload2uint-function"></a>RWByteAddressBuffer :: Load2 (uint), fonction

Obtient deux valeurs.

## <a name="syntax"></a>Syntaxe

``` syntax
uint2 Load2(
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

Type : **uint2**

Deux valeurs.

## <a name="remarks"></a>Remarques

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes Load2](rwbyteaddressbuffer-load2.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




