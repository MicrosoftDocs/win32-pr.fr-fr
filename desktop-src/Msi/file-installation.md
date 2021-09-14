---
description: 'Une fois le coût du fichier terminé, le programme d’installation dispose de toutes les informations requises pour traiter les deux actions de manipulation de fichiers : DuplicateFiles et MoveFiles.'
ms.assetid: 2e6d6eb3-1e71-46e6-a946-d9cc0b209325
title: Installation du fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472c58db3dc2e9094a26d57f871359a38930877b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021751"
---
# <a name="file-installation"></a>Installation du fichier

Une fois le [coût du fichier](file-costing.md) terminé, le programme d’installation dispose de toutes les informations requises pour traiter les deux actions de manipulation de fichiers : [DuplicateFiles](duplicatefiles-action.md) et [MoveFiles](movefiles-action.md).

Utilisez l' [action DuplicateFiles](duplicatefiles-action.md) pour spécifier les fichiers que le programme d’installation doit dupliquer dans la [table DuplicateFile](duplicatefile-table.md). Utilisez l' [action MoveFiles](movefiles-action.md)pour déterminer les fichiers à déplacer en interrogeant la [table MoveFile](movefile-table.md).

Notez que le champ options de la [table MoveFile](movefile-table.md) spécifie si le fichier d’origine doit être supprimé de son emplacement actuel. Les fichiers qui sont déplacés ou copiés par l’action MoveFiles ne sont pas supprimés lorsque le produit est désinstallé.

L' [action InstallFiles](installfiles-action.md) est appelée une fois toutes les autres opérations de manipulation de fichier terminées. L’action InstallFiles traite la table [multimédia](media-table.md), la [table de fichiers](file-table.md)et la [table de composants](component-table.md) pour déterminer quels fichiers seront copiés de la source vers la destination.

L' [action InstallFiles](installfiles-action.md) crée la structure de répertoire nécessaire à l’installation de tous les fichiers. Si vous devez installer un dossier explicitement vide, l' [action CreateFolders](createfolders-action.md) peut être appelée pour le créer.

 

 



