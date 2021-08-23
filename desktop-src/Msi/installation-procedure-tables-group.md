---
description: Les tables du groupe procédure d’installation contrôlent les tâches effectuées lors de l’installation par actions standard et actions personnalisées.
ms.assetid: dff7cf4a-89a2-47b0-9038-93b79c0d915a
title: Groupe de tables de procédure d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c66cc377fdf36969699f0e150fc30a02363ed24aa1848c4492917bffda7bc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633584"
---
# <a name="installation-procedure-tables-group"></a>Groupe de tables de procédure d’installation

Les tables du groupe procédure d’installation contrôlent les tâches effectuées lors de l’installation par [actions standard](standard-actions.md) et [actions personnalisées](custom-actions.md).

Certaines des tables de ce groupe contrôlent une action de haut niveau en fournissant une séquence d’actions. Chacune des tables de séquences suivantes contrôle une partie d’une action de haut niveau.

-   [Table InstallUISequence](installuisequence-table.md)
-   [Table InstallExecuteSequence](installexecutesequence-table.md)
-   [Table AdminUISequence](adminuisequence-table.md)
-   [Table AdminExecuteSequence](adminexecutesequence-table.md)
-   [Table AdvtUISequence](advtuisequence-table.md)
-   [Table AdvtExecuteSequence](advtexecutesequence-table.md)

Il peut y avoir des situations dans lesquelles une installation doit effectuer une opération qui n’est pas possible en utilisant uniquement des [actions standard](standard-actions.md). Pour offrir le plus grand degré de flexibilité, le programme d’installation fournit aux auteurs d’installation la possibilité de créer leurs propres actions personnalisées. Si vous avez des actions personnalisées, vous devez les inscrire auprès du programme d’installation en remplissant la table CustomAction.

La [table CustomAction](customaction-table.md) fournit les moyens d’intégrer du code personnalisé et des données dans le processus d’installation. Le code exécuté peut être un flux contenu dans la base de données, un fichier récemment installé ou un exécutable existant.

Les tableaux suivants étendent les fonctionnalités du programme d’installation pour manipuler les fichiers et les dossiers lors de l’installation.

-   La [table RemoveFile](removefile-table.md) contient la liste des fichiers qui sont supprimés au cours de l’installation.
-   La [table RemoveIniFile](removeinifile-table.md) contient les informations qu’une application doit supprimer de .ini fichiers.
-   La [table RemoveRegistry](removeregistry-table.md) contient les informations qui sont supprimées du Registre système lorsque le composant correspondant est sélectionné pour être installé.
-   Le [tableau CreateFolder](createfolder-table.md) répertorie les dossiers qui doivent être créés pendant l’installation. Bien que le programme d’installation crée des dossiers lorsqu’ils sont nécessaires, ceux-ci sont supprimés dès qu’ils sont vides. La liste des dossiers dans la table CreateFolder n’est pas supprimée tant que le composant n’est pas désinstallé.
-   La [table MoveFile](movefile-table.md) contient une liste de fichiers à déplacer ou à copier à partir d’un répertoire source spécifié sur l’ordinateur de l’utilisateur vers un répertoire de destination. Il n’est pas nécessaire d’utiliser la table MoveFile pour décrire les fichiers associés aux composants que vous installez.

Pour définir les conditions requises qui doivent être remplies pour lancer l’installation, remplissez la table LaunchCondition.

La [table LaunchCondition](launchcondition-table.md) contient une liste de conditions, qui doivent toutes être satisfaites pour que l’action aboutisse.

 

 



