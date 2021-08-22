---
description: L’action RemoveFiles supprime les fichiers précédemment installés par l’action InstallFiles.
ms.assetid: 1079be89-515c-443e-8927-46ddf7891a59
title: Action RemoveFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b50e23a7d2eb3c9bb23575d83d000b053f0de06907541777e43b5476f8c722ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626449"
---
# <a name="removefiles-action"></a>Action RemoveFiles

L’action RemoveFiles supprime les fichiers précédemment installés par l’action [InstallFiles](installfiles-action.md) . Chacun de ces fichiers est contrôlé par un lien vers une entrée de la table des [composants](component-table.md) . Seuls les fichiers dont les composants sont résolus à l’état *msiInstallStateAbsent* ou *msiInstallStateLocal* si le composant est installé localement sont supprimés.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action [InstallValidate](installvalidate-action.md) doit être appelée avant d’appeler RemoveFiles. Si une action [InstallFiles](installfiles-action.md) est utilisée, elle doit apparaître après RemoveFiles.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                    |
|-------|-----------------------------------------------|
| \[1\] | Identificateur du fichier supprimé.                   |
| \[9\] | Identificateur du répertoire contenant le fichier supprimé. |



 

## <a name="remarks"></a>Remarques

La table [RemoveFile](removefile-table.md) peut être omise de la base de données du programme d’installation s’il n’y a pas de fichiers divers à supprimer.

L’action RemoveFiles peut également supprimer les fichiers spécifiés par l’auteur qui ne sont pas installés par l’action InstallFiles. Ces fichiers sont spécifiés dans la table [RemoveFile](removefile-table.md) . Chacun de ces fichiers est contrôlé par un lien vers une entrée de la table des [composants](component-table.md) . Les fichiers dont les composants sont résolus en un état d’action actif (autrement dit, qui n’est pas à l’état désactivé ou null) sont supprimés si le fichier existe dans le répertoire spécifié. La suppression des fichiers spécifiés dans la table RemoveFile est tentée lorsque le composant lié est installé pour la première fois, lors d’une réinstallation, puis à nouveau lorsque le composant lié est supprimé.

L’action RemoveFiles peut également supprimer des dossiers. Un dossier vide est supprimé si la valeur de la colonne FileName de la table RemoveFile est null.

Lors de la suppression des fichiers installés précédemment, l’action RemoveFiles interroge les mêmes champs dans les mêmes tables que ceux interrogés par l’action [InstallFiles](installfiles-action.md) , à l’exception du fait que la [table multimédia](media-table.md) n’est pas utilisée par l’action RemoveFiles.

Le nom du fichier cible peut être spécifié dans le texte localisé dans la colonne FileName de la table RemoveFile.

 

 



