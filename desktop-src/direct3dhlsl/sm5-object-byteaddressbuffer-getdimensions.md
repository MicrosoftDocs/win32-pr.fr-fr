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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524472"
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

## <a name="remarks"></a>Remarques

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

 

 




