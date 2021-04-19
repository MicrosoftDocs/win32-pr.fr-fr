---
title: VIEW. timerInterval
description: L’attribut timerInterval spécifie ou récupère l’intervalle, en millisecondes, auquel la minuterie déclenche des événements dans le gestionnaire d’événements OnTimer.
ms.assetid: 1a69890f-5ea4-493a-8a9e-04fe60a41804
keywords:
- VIEW. timerInterval Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.timerInterval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790c95fbb2cded134222271d04c4c37dae412b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535870"
---
# <a name="viewtimerinterval"></a>VIEW. timerInterval

L’attribut **timerInterval** spécifie ou récupère l’intervalle, en millisecondes, auquel la minuterie déclenche des événements dans le gestionnaire d’événements **OnTimer** .

``` syntax
        elementID.timerInterval
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**long**) avec une valeur par défaut de 1000.



| Valeur        | Description                    |
|--------------|--------------------------------|
| 0            | L’événement du minuteur ne se déclenche pas. |
| 50 et versions ultérieures | Intervalle en millisecondes.  |



 

Toute valeur inférieure à 50 (y compris les nombres négatifs, mais qui n’inclut pas zéro) génère une erreur et la valeur précédente est conservée.

## <a name="remarks"></a>Notes

Cela ne se déclenchera pas automatiquement si aucun gestionnaire d’événements **OnTimer** n’est implémenté. Il n’y a donc pas de dégradation des performances, même si la valeur par défaut est différente de zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément VIEW**](view-element.md)
</dt> <dt>

[**VIEW. OnTimer**](view-ontimer.md)
</dt> </dl>

 

 





