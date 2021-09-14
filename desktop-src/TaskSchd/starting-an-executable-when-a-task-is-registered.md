---
title: Démarrage d’un exécutable quand une tâche est inscrite
description: L’écriture d’une tâche qui démarre un exécutable quand une tâche est inscrite est effectuée en définissant un déclencheur d’inscription et une action exécutable.
ms.assetid: 426fa79d-7f0d-42fb-a8c4-15981d13be71
keywords:
- Planificateur de tâches des exemples de Planificateur de tâches, déclencheur d’inscription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8036b8bdff807ded582279e0ba7675bc2160811
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120610"
---
# <a name="starting-an-executable-when-a-task-is-registered"></a>Démarrage d’un exécutable quand une tâche est inscrite

L’écriture d’une tâche qui démarre un exécutable quand une tâche est inscrite est effectuée en définissant un déclencheur d’inscription et une action exécutable.

## <a name="registration-trigger"></a>Déclencheur d’inscription

Les déclencheurs d’inscription démarrent une tâche dès qu’elle est inscrite. Vous pouvez également spécifier un délai pour le déclencheur d’inscription, qui démarre une tâche après un laps de temps spécifique (délai) après l’inscription de la tâche. Le délai est spécifié dans la propriété [**delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) de l’interface [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) ([**RegistrationTrigger**](registrationtrigger.md) pour l’écriture de scripts).

> [!Note]  
> Quand une tâche avec un déclencheur d’inscription est mise à jour, la tâche s’exécute une fois la mise à jour effectuée.

 

## <a name="registration-trigger-examples"></a>Exemples de déclencheurs d’inscription

les exemples suivants démarrent Bloc-notes lorsqu’une tâche est inscrite :

-   [Exemple de déclencheur d’inscription (script)](registration-trigger-example--scripting-.md)
-   [Exemple de déclencheur d’inscription (C++)](registration-trigger-example--c---.md)
-   [Exemple de déclencheur d’inscription (XML)](registration-trigger-example--xml-.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’Planificateur de tâches](using-the-task-scheduler.md)
</dt> </dl>

 

 




