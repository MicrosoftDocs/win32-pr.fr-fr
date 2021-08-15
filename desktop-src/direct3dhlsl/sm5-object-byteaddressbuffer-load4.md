---
title: 'ByteAddressBuffer :: Load4 (uint), fonction'
description: 'Obtient quatre valeurs. | ByteAddressBuffer :: Load4 (uint), fonction'
ms.assetid: bc74bf29-1c22-4e47-bafc-ecef194f54b8
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
ms.openlocfilehash: a623c62ce9038d4e06cfbb952808aeb0530cb2e937c83578d9ef0e71c9b0a038
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509999"
---
# <a name="byteaddressbufferload4uint-function"></a>ByteAddressBuffer :: Load4 (uint), fonction

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
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes Load4](byteaddressbuffer-load4.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




