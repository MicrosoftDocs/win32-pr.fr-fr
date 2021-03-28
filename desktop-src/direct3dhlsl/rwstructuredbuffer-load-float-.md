---
title: 'RWStructuredBuffer :: Load (int), fonction'
description: 'Lit les données de la mémoire tampon. | RWStructuredBuffer :: Load (int), fonction'
ms.assetid: 9CB40579-6BF8-468C-81B8-936D9940458E
keywords:
- Charger la fonction HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c20998faef8f5a018aaf95571be3c9d64730c436
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991905"
---
# <a name="rwstructuredbufferloadint-function"></a>RWStructuredBuffer :: Load (int), fonction

Lit les données de la mémoire tampon.

## <a name="syntax"></a>Syntaxe


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Emplacement* \[ dans\]
</dt> <dd>

Type : **int**

Emplacement de la mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Tapez :

Le type de retour correspond au type dans la déclaration pour l’objet [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) .

## <a name="remarks"></a>Notes

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes Load](rwstructuredbuffer-load.md)
</dt> </dl>

 

 




