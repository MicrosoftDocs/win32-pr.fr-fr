---
title: VIEW. timerInterval
description: L’attribut timerInterval spécifie ou récupère l’intervalle, en millisecondes, auquel la minuterie déclenche des événements dans le gestionnaire d’événements OnTimer.
ms.assetid: 1a69890f-5ea4-493a-8a9e-04fe60a41804
keywords:
- VIEW. timerInterval Lecteur Windows Media
topic_type:
- apiref
api_name:
- VIEW.timerInterval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43b2b7bbd87663a35c43db733d3e11ff0dca5bc3ddfd00e57022b4df7122c3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001309"
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

## <a name="remarks"></a>Remarques

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

 

 





