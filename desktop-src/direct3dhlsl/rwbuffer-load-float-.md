---
title: 'RWBuffer :: Load (int), fonction'
description: 'Lit les données de la mémoire tampon. | RWBuffer :: Load (int), fonction'
ms.assetid: 3066E244-DE56-4F0D-8443-018B9EFEC1FF
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
ms.openlocfilehash: 561f055990bbca683bf9c55b5805b8d3c55b3272
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761690"
---
# <a name="rwbufferloadint-function"></a>RWBuffer :: Load (int), fonction

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

Le type de retour correspond au type dans la déclaration pour l’objet [**RWBuffer**](sm5-object-rwbuffer.md) .

## <a name="remarks"></a>Notes

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes Load](rwbuffer-load.md)
</dt> </dl>

 

 




