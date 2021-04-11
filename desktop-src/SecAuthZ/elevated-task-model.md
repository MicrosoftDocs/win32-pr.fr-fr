---
description: Une application s’exécutant en tant qu’utilisateur standard effectue des opérations qui requièrent des privilèges d’administrateur en démarrant une tâche planifiée.
ms.assetid: cd7485b3-6be5-4163-9a86-7892dbc59181
title: Modèle de tâche avec élévation de privilèges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27006e32210cfea05de5c2b3b9adf36613dc4f5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320549"
---
# <a name="elevated-task-model"></a>Modèle de tâche avec élévation de privilèges

Dans le modèle de tâche avec élévation de privilèges, une application qui s’exécute en tant qu’utilisateur standard effectue des opérations qui requièrent des privilèges d’administrateur en démarrant une tâche planifiée.

**Windows Server 2003 et Windows XP :** Le modèle de tâche avec élévation de privilèges n’est pas pris en charge.

Les tâches ne consomment pas autant de ressources système que de services et les tâches se ferment automatiquement lorsqu’elles sont terminées. Envisagez d’utiliser ce modèle au lieu du [modèle de service du système d’exploitation](operating-system-service-model.md) , sauf si la compatibilité descendante avec les systèmes d’exploitation antérieurs est nécessaire.

Pour utiliser une tâche afin d’effectuer des opérations privilégiées pour une application utilisateur standard, les conditions suivantes doivent être remplies :

-   La tâche doit être définie pour s’exécuter en tant que **système**.
-   Le [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) associé à la tâche doit être configuré pour permettre aux utilisateurs standard de démarrer la tâche.
-   Le service du planificateur de tâches doit être en cours d’exécution.

Pour plus d’informations sur la création et le démarrage de tâches, consultez [Planificateur de tâches](/windows/desktop/TaskSchd/task-scheduler-start-page).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement d’applications nécessitant des privilèges d’administrateur](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modèle de Broker administrateur](administrator-broker-model.md)
</dt> <dt>

[Modèle d’objet COM administrateur](administrator-com-object-model.md)
</dt> <dt>

[Modèle de service du système d’exploitation](operating-system-service-model.md)
</dt> </dl>

 

 
