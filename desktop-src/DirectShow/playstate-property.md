---
description: La propriété lecture récupère l’état actuel de l’objet MSWebDVD.
ms.assetid: ffe71c3f-f8c2-45cc-84bf-e937cfbbe7b9
title: Propriété lecture
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8c699ce3f232f9afc14472f0308fa65adc6abb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121937"
---
# <a name="playstate-property"></a>Propriété lecture

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `PlayState` propriété récupère l’état actuel de l’objet **mswebdvd** .

``` syntax
[ iState = ] MSWebDVD.PlayState
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant l’état actuel du navigateur DVD.



| Code de retour | Description   |
|-------------|---------------|
| -2          | Indéfini     |
| -1          | Non initialisé(e) |
| 0           | Arrêté       |
| 1           | Suspendu        |
| 2           | Exécution en cours       |



 

## <a name="remarks"></a>Notes

Cette propriété est en lecture seule sans valeur par défaut.

l’objet **MSWebDVD** contrôle le DirectShow filtre du navigateur dvd, qui effectue le travail réel de navigation sur le dvd. Il s’agit en fait de l’état du navigateur DVD auquel cette propriété fait référence. Le navigateur DVD peut avoir plusieurs États, comme décrit ci-dessus. La `PlayState` propriété peut être utile en tant qu’outil de diagnostic, mais en général, il n’y a aucune raison pour qu’une application de script surveille l’état du navigateur DVD.

 

 



