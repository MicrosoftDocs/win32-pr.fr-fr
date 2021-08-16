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
ms.openlocfilehash: 863269c5127915af82b8ef82aa36b60b17941d8627b3f81a789f75618219c773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725393"
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

## <a name="remarks"></a>Remarques

T peut être n’importe quel type de données, y compris les structures.

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[AppendStructuredBuffer](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




