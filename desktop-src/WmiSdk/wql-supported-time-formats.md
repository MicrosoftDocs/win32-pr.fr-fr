---
description: Décrit les formats d’heure pris en charge pour une utilisation dans la clause WHERE WQL.
ms.assetid: d86bd2e3-f5cb-488f-9cd6-5105d82a1842
ms.tgt_platform: multiple
title: Formats d’heure WQL-Supported
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 627b46ef7d01a2eb3e8e40484b37822c9ebca55a9487b1ffb0e1a138ab7378d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049737"
---
# <a name="wql-supported-time-formats"></a>Formats d’heure WQL-Supported

Outre le format DATETIME WMI, les formats de date suivants sont pris en charge pour une utilisation dans la clause WQL WQL.



| Format                                    | Description                                                                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HH \[ \] {AP} M<br/>                   | Heure comme indiqué sur une horloge de 12 heures, et une désignation AM ou PM.<br/> 16:00<br/>                                                                                                             |
| hh:mm<br/>                          | Heures et minutes délimitées par deux-points. Aucune dénomination AM ou PM.<br/> 3:23<br/>                                                                                                                  |
| hh : mm \[ \] {AP} M<br/>                | Heures et minutes délimitées par deux-points, espace facultatif et désignation AM ou PM.<br/> 3:23<br/>                                                                                              |
| hh:mm:ss<br/>                       | Heure délimitée par deux-points, en minutes et en secondes. Aucune désignation AM/PM.<br/> 3:23:00<br/>                                                                                                         |
| hh : mm : SS \[ \] {AP} M<br/>             | L’heure, les minutes et les secondes, l’espace facultatif et la désignation AM/PM sont délimités par deux-points.<br/> 3:23:14:00<br/>                                                                                      |
| hh : mm : SS : uuu<br/>                   | Heure, minutes et secondes délimitée par deux-points, et décalage à trois chiffres qui indique le nombre de minutes pendant lequel le fuseau horaire d’origine s’écarte de l’heure UTC.<br/>                                    |
| hh : mm : \[ SS : u u u \[ \] \]<br/>           | Heure délimitée par deux-points, minutes et secondes ; et un décalage d’un, deux ou trois chiffres qui indique le nombre de minutes pendant lequel le fuseau horaire d’origine s’écarte de l’heure UTC.<br/>                       |
| hh : mm : SS : uuu \[ \] {AP} M<br/>         | Heure délimitée par deux-points, minutes et secondes, décalage à trois chiffres qui indique le nombre de minutes pendant lequel le fuseau horaire d’origine s’écarte de l’heure UTC et de la désignation AM ou PM.<br/>              |
| hh : mm : SS : u u u \[ \[ \] \] \[ \] {AP} M<br/> | Heure délimitée par deux-points, minutes et secondes ; décalage un, deux ou trois chiffres qui indique le nombre de minutes que le fuseau horaire d’origine s’écarte de l’heure UTC ; et la désignation AM ou PM.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Clause WHERE](where-clause.md)
</dt> </dl>

 

 




