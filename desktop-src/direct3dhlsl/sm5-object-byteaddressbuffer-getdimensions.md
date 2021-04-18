---
title: 'ByteAddressBuffer :: GetDimensions,, fonction'
description: 'Obtient la longueur de la mémoire tampon. | ByteAddressBuffer :: GetDimensions,, fonction'
ms.assetid: 32099118-8d8a-440e-96ba-2580d905f068
keywords:
- GetDimensions, fonction HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1cbb705789e444a6fa54aeb87190912996f65621
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991869"
---
# <a name="byteaddressbuffergetdimensions-function"></a>ByteAddressBuffer :: GetDimensions,, fonction

Obtient la longueur de la mémoire tampon.

## <a name="syntax"></a>Syntaxe

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*Dim* \[ out\]
</dt> <dd>

Type : **uint**

Longueur, en octets, de la mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ByteAddressBuffer](sm5-object-byteaddressbuffer.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




