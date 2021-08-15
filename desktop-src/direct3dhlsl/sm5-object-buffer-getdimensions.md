---
title: 'Buffer :: GetDimensions,, fonction'
description: 'Obtient la longueur de la mémoire tampon. | Buffer :: GetDimensions,, fonction'
ms.assetid: 704890e8-43e4-4e72-b7e2-eeef331bef1c
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
ms.openlocfilehash: d7c56d673e533b4626a57669cf884d80da63d7848cfc7a3e248762f6c4f42088
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986099"
---
# <a name="buffergetdimensions-function"></a>Buffer :: GetDimensions,, fonction

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



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Buffer](sm5-object-buffer.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




