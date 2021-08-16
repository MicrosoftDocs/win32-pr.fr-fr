---
title: 'RWByteAddressBuffer :: Load4 (uint), fonction'
description: 'Obtient quatre valeurs. | RWByteAddressBuffer :: Load4 (uint), fonction'
ms.assetid: b46cd119-75be-4c2d-82f9-5dcabd7e4400
keywords:
- Load4 fonction HLSL
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7545c27ccd5f82b3fed1f36a1cc2b0f9d92a9d901f5614ba3b6bec4068cb8abb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724969"
---
# <a name="rwbyteaddressbufferload4uint-function"></a>RWByteAddressBuffer :: Load4 (uint), fonction

Obtient quatre valeurs.

## <a name="syntax"></a>Syntaxe

``` syntax
uint4 Load4(
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

Type : **uint4**

Quatre valeurs.

## <a name="remarks"></a>Remarques

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes Load4](rwbyteaddressbuffer-load4.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




