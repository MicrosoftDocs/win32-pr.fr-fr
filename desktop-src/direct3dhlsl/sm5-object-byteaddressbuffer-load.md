---
title: 'ByteAddressBuffer :: Load (int), fonction'
description: 'Obtient une valeur. | ByteAddressBuffer :: Load (int), fonction'
ms.assetid: a63f4099-2c3b-4d37-9135-b8c63df30824
keywords:
- Charger la fonction HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0de7d1a8ef8a7fe3173016fe07a433a930c3d59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991916"
---
# <a name="byteaddressbufferloadint-function"></a>ByteAddressBuffer :: Load (int), fonction

Obtient une valeur.

## <a name="syntax"></a>Syntaxe

``` syntax
uint Load(
  in int address
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*adresse* \[ dans\]
</dt> <dd>

Type : **int**

Adresse d’entrée en octets, qui doit être un multiple de 4.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **uint**

Une valeur.

## <a name="remarks"></a>Notes

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes Load](byteaddressbuffer-load.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




