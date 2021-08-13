---
description: 'Une fois le coût du fichier terminé, le programme d’installation dispose de toutes les informations requises pour traiter les deux actions de manipulation de fichiers : DuplicateFiles et MoveFiles.'
ms.assetid: 2e6d6eb3-1e71-46e6-a946-d9cc0b209325
title: Installation du fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005a987a7e61f646f58abd0ec699ce03bd29d85dfa2ddb01e8f693750acda740
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636697"
---
# <a name="file-installation"></a>Installation du fichier

Une fois le [coût du fichier](file-costing.md) terminé, le programme d’installation dispose de toutes les informations requises pour traiter les deux actions de manipulation de fichiers : [DuplicateFiles](duplicatefiles-action.md) et [MoveFiles](movefiles-action.md).

Utilisez l' [action DuplicateFiles](duplicatefiles-action.md) pour spécifier les fichiers que le programme d’installation doit dupliquer dans la [table DuplicateFile](duplicatefile-table.md). Utilisez l' [action MoveFiles](movefiles-action.md)pour déterminer les fichiers à déplacer en interrogeant la [table MoveFile](movefile-table.md).

Notez que le champ options de la [table MoveFile](movefile-table.md) spécifie si le fichier d’origine doit être supprimé de son emplacement actuel. Les fichiers qui sont déplacés ou copiés par l’action MoveFiles ne sont pas supprimés lorsque le produit est désinstallé.

L' [action InstallFiles](installfiles-action.md) est appelée une fois toutes les autres opérations de manipulation de fichier terminées. L’action InstallFiles traite la table [multimédia](media-table.md), la [table de fichiers](file-table.md)et la [table de composants](component-table.md) pour déterminer quels fichiers seront copiés de la source vers la destination.

L' [action InstallFiles](installfiles-action.md) crée la structure de répertoire nécessaire à l’installation de tous les fichiers. Si vous devez installer un dossier explicitement vide, l' [action CreateFolders](createfolders-action.md) peut être appelée pour le créer.

 

 



