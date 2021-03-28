---
title: 'RWByteAddressBuffer :: Load3 (uint), fonction'
description: 'Obtient trois valeurs. | RWByteAddressBuffer :: Load3 (uint), fonction'
ms.assetid: cf8c4c5d-4748-43d7-896e-33ed07c94b9e
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
ms.openlocfilehash: d6658b4929f09aa7296a284de1fdbf39c7c4f038
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974415"
---
# <a name="rwbyteaddressbufferload3uint-function"></a>RWByteAddressBuffer :: Load3 (uint), fonction

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

## <a name="remarks"></a>Notes

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes Load3](rwbyteaddressbuffer-load3.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




