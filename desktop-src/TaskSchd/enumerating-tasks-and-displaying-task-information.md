---
title: Énumération des tâches et affichage des informations sur les tâches
description: L’affichage d’informations sur une tâche, telles que le nom de la tâche, l’État ou la dernière exécution de la tâche, s’effectue en énumérant des tâches en cours d’exécution ou les tâches d’un dossier de tâches et en affichant les informations souhaitées.
ms.assetid: a0305089-89ff-42b7-b3f1-99a6484d2e5e
keywords:
- énumération des tâches Planificateur de tâches
- Exemples de Planificateur de tâches Planificateur de tâches, énumération de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e4c1bbad0a1fa8892e38a001ff54e665f0c144
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008667"
---
# <a name="enumerating-tasks-and-displaying-task-information"></a>Énumération des tâches et affichage des informations sur les tâches

L’affichage d’informations sur une tâche, telles que le nom de la tâche, l’État ou la dernière exécution de la tâche, s’effectue en énumérant des tâches en cours d’exécution ou les tâches d’un dossier de tâches et en affichant les informations souhaitées.

## <a name="accessing-properties-of-registered-tasks"></a>Accès aux propriétés des tâches inscrites

Pour afficher la valeur de la propriété d’une tâche inscrite, vous devez vous connecter au service Planificateur de tâches, puis obtenir une instance du dossier de tâches qui contient les tâches pour lesquelles vous souhaitez obtenir des informations. Vous pouvez ensuite obtenir une collection de toutes les tâches inscrites dans le dossier de tâches. Vous allez ensuite énumérer chaque tâche inscrite et obtenir et afficher une valeur de propriété pour chaque tâche.

## <a name="accessing-properties-of-running-tasks"></a>Accès aux propriétés des tâches en cours d’exécution

Pour afficher la valeur de la propriété d’une tâche en cours d’exécution, vous devez vous connecter au service Planificateur de tâches, puis obtenir une collection de toutes les tâches en cours d’exécution (y compris ou excluant les tâches masquées). Ensuite, vous énumérez chaque tâche en cours d’exécution et récupérez et affichez une valeur de propriété pour chaque tâche.

## <a name="example"></a>Exemple

Les exemples suivants énumèrent les tâches et affichent le nom et l’état des tâches :

-   [Affichage des noms et des États des tâches (script)](displaying-task-names-and-state--scripting-.md)
-   [Affichage des noms et de l’état des tâches (C++)](displaying-task-names-and-state--c---.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’Planificateur de tâches](using-the-task-scheduler.md)
</dt> </dl>

 

 




