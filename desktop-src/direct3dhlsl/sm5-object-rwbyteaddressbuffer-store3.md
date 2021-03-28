---
title: 'RWByteAddressBuffer :: Store3, fonction'
description: Définit trois valeurs.
ms.assetid: eaf12b5a-c9c6-413a-9646-3d14e7825460
keywords:
- Store3 fonction HLSL
topic_type:
- apiref
api_name:
- Store3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd27684c3adf506e086fb17f789272c6b263ab20
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104313345"
---
# <a name="store3-function"></a>Store3 fonction)

Définit trois valeurs.

## <a name="syntax"></a>Syntaxe

``` syntax
void Store3(
  in uint address,
  in uint3 values
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

Type : **uint3**

Trois valeurs d’entrée.

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

 

 




