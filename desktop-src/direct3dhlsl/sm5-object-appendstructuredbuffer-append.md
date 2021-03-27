---
title: 'AppendStructuredBuffer :: Append, fonction'
description: Ajoute une valeur à la fin de la mémoire tampon.
ms.assetid: 667bc6dc-c0d0-419a-9227-99ce30b9cc73
keywords:
- Fonction Append, HLSL
topic_type:
- apiref
api_name:
- Append
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79db73558cb243437560cc77ed66b64f2807fe13
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "103940527"
---
# <a name="append-function"></a>Append, fonction

Ajoute une valeur à la fin de la mémoire tampon.

## <a name="syntax"></a>Syntaxe

``` syntax
void Append(
  in T value
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ dans\]
</dt> <dd>

Type : **T**

Valeur d'entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

None

## <a name="remarks"></a>Notes

T peut être n’importe quel type de données, y compris les structures.

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[AppendStructuredBuffer](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




