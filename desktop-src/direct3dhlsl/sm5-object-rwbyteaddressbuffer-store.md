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
ms.openlocfilehash: 5be699a28eea213b8847f32a3b66f53739a7db86ee5964bd97559a6d534fff6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724941"
---
# <a name="store-function"></a>Store, fonction

Définit une valeur.

## <a name="syntax"></a>Syntaxe

``` syntax
void Store(
  in uint address,
  in uint value
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

## <a name="remarks"></a>Remarques

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




