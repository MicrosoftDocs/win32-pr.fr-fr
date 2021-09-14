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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232229"
---
# <a name="append-function"></a>Append, fonction

Ajoute une valeur à la fin de la mémoire tampon.

## <a name="syntax"></a>Syntaxe

``` syntax
void Append(
  in T value
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ dans\]
</dt> <dd>

Type : **T**

Valeur d'entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

None

## <a name="remarks"></a>Notes

T peut être n’importe quel type de données, y compris les structures.

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[AppendStructuredBuffer](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




