---
title: Démarrage d’un exécutable lorsqu’un utilisateur ouvre une session
description: L’écriture d’une tâche qui démarre un exécutable quand un utilisateur se connecte est effectuée en définissant un déclencheur LOGON et une action exécutable.
ms.assetid: 0c5912aa-913d-42ce-a01b-b1359b49bb2f
keywords:
- Planificateur de tâches des exemples de Planificateur de tâches, déclencheur de connexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa758546dbd08b6ccf27412f38891589cb9643
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379585"
---
# <a name="starting-an-executable-when-a-user-logs-on"></a>Démarrage d’un exécutable lorsqu’un utilisateur ouvre une session

L’écriture d’une tâche qui démarre un exécutable quand un utilisateur se connecte est effectuée en définissant un déclencheur LOGON et une action exécutable.

## <a name="logon-trigger"></a>Déclencheur de connexion

Les déclencheurs de connexion sont activés par leur limite de démarrage, mais ils ne démarrent pas l’exécutable tant qu’un utilisateur spécifié n’ouvre pas une session. Vous pouvez spécifier le déclencheur d’ouverture de session à démarrer lorsqu’un utilisateur se connecte en spécifiant l’utilisateur dans la propriété [**userid**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) de l’interface [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) ([**LogonTrigger**](logontrigger.md) pour l’écriture de scripts).

## <a name="logontrigger-examples"></a>Exemples LogonTrigger

Les exemples suivants démarrent le bloc-notes après qu’un utilisateur ouvre une session.

-   [Exemple de déclencheur LOGON (script)](logon-trigger-example--scripting-.md)
-   [Exemple de déclencheur LOGON (C++)](logon-trigger-example--c---.md)
-   [Exemple de déclencheur LOGON (XML)](logon-trigger-example--xml-.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’Planificateur de tâches](using-the-task-scheduler.md)
</dt> </dl>

 

 




