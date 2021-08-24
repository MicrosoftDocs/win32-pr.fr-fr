---
title: 'RWByteAddressBuffer :: fonction de la fonction'
description: Définit deux valeurs.
ms.assetid: 7b32c84c-9ea2-47ae-a0f3-df6d95249163
keywords:
- Fonction de fonction du langage HLSL
topic_type:
- apiref
api_name:
- Store2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 723c2f895790618a14d6603acacb7e106a936ad5262696ef553dafa72c1332c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853309"
---
# <a name="store2-function"></a>Fonction de la Banque de fonctions

Définit deux valeurs.

## <a name="syntax"></a>Syntaxe

``` syntax
void Store2(
  in uint address,
  in uint2 values
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*adresse* \[ dans\]
</dt> <dd>

Type : **uint**

Adresse d’entrée en octets, qui doit être un multiple de 4.

</dd> <dt>

*valeurs* \[ dans\]
</dt> <dd>

Type : **uint2**

Deux valeurs d’entrée.

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

 

 




