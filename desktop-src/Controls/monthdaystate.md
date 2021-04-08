---
title: MONTHDAYSTATE
description: Le type de données MONTHDAYSTATE est un champ de type binaire qui contient l’état de chaque jour dans un mois.
ms.assetid: eb3dd6cb-738e-424b-945b-1485798a444c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2286482460ec87982c46a564e8441edd9bf7bb43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839382"
---
# <a name="monthdaystate"></a>MONTHDAYSTATE

Le type de données MONTHDAYSTATE est un champ de type binaire qui contient l’état de chaque jour dans un mois. Le type de données est défini dans commctrl. h comme suit :


```
typedef DWORD MONTHDAYSTATE, *LPMONTHDAYSTATE;
```



Chaque bit (0 à 30) représente l’état d’un jour dans un mois. Si un bit est activé, le jour correspondant s'affiche en gras ; sinon il s'affiche sans l'accentuation.

Ce type de données est utilisé avec le message [**MCM \_ SETDAYSTATE**](mcm-setdaystate.md) et la macro correspondante, [**calendrier monthcal \_ SETDAYSTATE**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate). Lorsque les valeurs MONTHDAYSTATE sont utilisées en référence à des mois plus courts que 31 jours, seuls les bits nécessaires sont accessibles.

Ce type de données a d’abord été défini dans la [Version 4,70](common-control-versions.md) de Comctl32.dll.

 

 




