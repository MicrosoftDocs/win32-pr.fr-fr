---
title: 'RWByteAddressBuffer :: Store, fonction'
description: Définit une valeur.
ms.assetid: edfda955-602c-44f4-adc3-77b61c9dcd05
keywords:
- Fonction de stockage HLSL
topic_type:
- apiref
api_name:
- Store
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e161e4fb64d09e41c6529954e63b2ace55207e9
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104971486"
---
# <a name="store-function"></a>Store, fonction

Définit une valeur.

## <a name="syntax"></a>Syntaxe

``` syntax
void Store(
  in uint address,
  in uint value
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*adresse* \[ dans\]
</dt> <dd>

Type : **uint**

Adresse d’entrée en octets, qui doit être un multiple de 4.

</dd> <dt>

*valeur* \[ dans\]
</dt> <dd>

Type : **uint**

Une valeur d’entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




