---
title: MONTHDAYSTATE
description: Le type de données MONTHDAYSTATE est un champ de type binaire qui contient l’état de chaque jour dans un mois.
ms.assetid: eb3dd6cb-738e-424b-945b-1485798a444c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e21eed1293a53bce8f38f5bd4db09b8cbe3fbf649fb07348a5dca65e908727
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079859"
---
# <a name="monthdaystate"></a>MONTHDAYSTATE

Le type de données MONTHDAYSTATE est un champ de type binaire qui contient l’état de chaque jour dans un mois. Le type de données est défini dans commctrl. h comme suit :


```
typedef DWORD MONTHDAYSTATE, *LPMONTHDAYSTATE;
```



Chaque bit (0 à 30) représente l’état d’un jour dans un mois. Si un bit est activé, le jour correspondant s'affiche en gras ; sinon il s'affiche sans l'accentuation.

Ce type de données est utilisé avec le message [**MCM \_ SETDAYSTATE**](mcm-setdaystate.md) et la macro correspondante, [**calendrier monthcal \_ SETDAYSTATE**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate). Lorsque les valeurs MONTHDAYSTATE sont utilisées en référence à des mois plus courts que 31 jours, seuls les bits nécessaires sont accessibles.

Ce type de données a d’abord été défini dans la [Version 4,70](common-control-versions.md) de Comctl32.dll.

 

 




