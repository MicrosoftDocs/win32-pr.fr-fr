---
title: Planificateur de tâches pour les développeurs
description: Le Planificateur de tâches vous permet d’effectuer automatiquement des tâches de routine sur un ordinateur choisi. Pour ce faire, Planificateur de tâches analysez les critères que vous choisissez (appelés déclencheurs), puis exécutez les tâches lorsque ces critères sont satisfaits.
ms.assetid: 15970a51-c139-48b8-b82b-605728d0f386
keywords:
- Planificateur de tâches pour les développeurs
- Planificateur de tâches pour le développement
- Développement avec Planificateur de tâches
- Planificateur de tâches, page du portail
ms.topic: article
ms.date: 10/18/2019
ms.openlocfilehash: dfbfb76145e38003e7c501b98c817f4aaca3ff09
ms.sourcegitcommit: 087843ef08ddcd8bce9ed647b610035925da2b3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/19/2019
ms.locfileid: "104100825"
---
# <a name="task-scheduler-for-developers"></a>Planificateur de tâches pour les développeurs

> [!IMPORTANT]
> Cette rubrique et les autres rubriques de cette section sont destinées aux développeurs. Si vous souhaitez utiliser le composant Planificateur de tâches de votre capacité en tant qu’administrateur ou professionnel de l’informatique, consultez [Planificateur de tâches](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler).

## <a name="about-the-task-scheduler"></a>À propos de l’Planificateur de tâches

Le Planificateur de tâches vous permet d’effectuer automatiquement des tâches de routine sur un ordinateur choisi. Pour ce faire, Planificateur de tâches analysez les critères que vous choisissez (appelés déclencheurs), puis exécutez les tâches lorsque ces critères sont satisfaits.

Vous pouvez utiliser la Planificateur de tâches pour exécuter des tâches telles que le démarrage d’une application, l’envoi d’un message électronique ou l’émission d’un message. Les tâches peuvent être planifiées pour s’exécuter en réponse à ces événements ou à ces déclencheurs. 

- Lorsqu’un événement système spécifique se produit.
- À un moment donné.
- À un moment donné sur une planification quotidienne.
- À un moment donné sur une planification hebdomadaire.
- À un moment donné sur une planification mensuelle.
- À un moment donné, selon une planification mensuelle de jour de semaine.
- Lorsque l’ordinateur passe à l’état inactif.
- Lorsque la tâche est inscrite.
- Lors du démarrage du système.
- Lorsqu’un utilisateur ouvre une session.
- Quand une session de Terminal Server change d’État.

## <a name="developers"></a>Développeurs

Le Planificateur de tâches fournit des API dans ces formes.

- Planificateur de tâches 2,0 : les interfaces et les objets sont fournis pour C++ et, pour le développement de script, respectivement.
- Planificateur de tâches 1,0 : les interfaces sont fournies pour le développement C++.

## <a name="run-time-requirements"></a>Conditions d’exécution

Le Planificateur de tâches requiert les systèmes d’exploitation suivants.

- Planificateur de tâches 2,0 : le client requiert Windows Vista ou version ultérieure. Le serveur nécessite Windows Server 2008 ou une version ultérieure.
- Planificateur de tâches 1,0 : le client requiert Windows Vista ou Windows XP. Le serveur nécessite Windows Server 2008 ou Windows Server 2003.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [Nouveautés de Planificateur de tâches](what-s-new-in-task-scheduler.md) | Résumé des nouvelles fonctionnalités introduites par le Planificateur de tâches. |
| [À propos de l’Planificateur de tâches](about-the-task-scheduler.md) | Informations conceptuelles générales sur l’API Planificateur de tâches. |
| [Utilisation de l’Planificateur de tâches](using-the-task-scheduler.md) | Exemples de code qui montrent comment utiliser les API Planificateur de tâches. |
| [Référence Planificateur de tâches](task-scheduler-reference.md) | Informations de référence détaillées pour les API Planificateur de tâches et le schéma Planificateur de tâches. |