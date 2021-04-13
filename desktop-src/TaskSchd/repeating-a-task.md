---
title: Répétition d’une tâche
description: Planificateur de tâches pouvez exécuter une tâche autant de fois qu’un déclencheur a été déclenché.
ms.assetid: 69c60713-134c-4602-9e7b-cc3eea871068
keywords:
- modèle de répétition Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451b2c2cf7e48c40496ddba95728f435ab494ab7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310654"
---
# <a name="repeating-a-task"></a>Répétition d’une tâche

Planificateur de tâches pouvez exécuter une tâche autant de fois qu’un déclencheur a été déclenché. Pour ce faire, le déclencheur définit un modèle de répétition qui indique Planificateur de tâches combien de temps il doit continuer à répéter la tâche et l’intervalle de temps entre chaque répétition de tâche.

## <a name="repetition-pattern"></a>Modèle de répétition

L’illustration suivante montre un modèle de répétition avec une durée de 60 minutes et un intervalle de 25 minutes. Sachez que dans ce cas, Planificateur de tâches exécute la tâche lorsque le déclencheur est activé, il réexécute la tâche après 25 minutes, puis réexécute la tâche après 50 minutes en fonction du paramètre de la [**propriété StopAtDurationEnd de IRepetitionPattern**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) ([**RepetitionPattern. StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) pour les scripts). Si la propriété **StopAtDurationEnd** est définie sur True, planificateur de tâches arrête la dernière instance de la tâche si elle est toujours en cours d’exécution après 60 minutes. Si la propriété **StopAtDurationEnd** est définie sur false, la dernière instance de la tâche est exécutée, quelle que soit la durée.

![modèle de répétition de déclencheur](images/repetition-pattern.png)

Si vous enregistrez une tâche qui contient un déclencheur avec un intervalle de répétition égal à une minute et une durée de répétition égale à quatre minutes, la tâche est démarrée cinq fois. Les cinq répétitions peuvent être définies par le modèle suivant :

1.  Une tâche commence au début de la première minute.
2.  La tâche suivante démarre à la fin de la première minute.
3.  La tâche suivante démarre à la fin de la seconde minute.
4.  La tâche suivante démarre à la fin de la troisième minute.
5.  La tâche suivante démarre à la fin de la quatrième minute.

**Windows Server 2003, Windows XP et windows 2000 :** Si vous enregistrez une tâche qui contient un déclencheur avec un intervalle de répétition égal à une minute et une durée de répétition égale à quatre minutes, la tâche est démarrée quatre fois.

## <a name="objects-interfaces-and-xml-elements"></a>Objets, interfaces et éléments XML

Pour le développement de scripts, le modèle de répétition est défini à l’aide de l’objet [**RepetitionPattern**](repetitionpattern.md) .

Pour le développement C++, le modèle de répétition est défini par l’interface [**IRepetitionPattern**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern) .

Lors de la lecture ou de l’écriture de données XML pour une tâche, le modèle de répétition est spécifié dans l’élément à [**répétition**](taskschedulerschema-repetition-triggerbasetype-element.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Déclencheurs de tâche](task-triggers.md)
</dt> </dl>

 

 




