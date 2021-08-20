---
description: le groupe de fichiers des tables contient toutes les tables de Windows Installer liées aux fichiers.
ms.assetid: 8f56328e-ed58-41a1-94b6-266e9c117246
title: Groupe de tables de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f8a73aa46b202d184356c14ff12da9ce9ce9880b009418e922b252cc35bc54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142902"
---
# <a name="file-tables-group"></a>Groupe de tables de fichiers

![Groupe de tables de fichiers](images/filegrp.png)

Pour plus d’informations sur ce diagramme, consultez la [légende diagramme de relation d’entité](entity-relationship-diagram-legend.md).

Un développeur de packages d’installation doit envisager de remplir le groupe de tables de fichiers de tables après avoir divisé l’application en [composants et fonctionnalités](components-and-features.md) et après avoir rempli le [groupe de tables principales](core-tables-group.md). Le groupe de tables file contient tous les fichiers appartenant à l’installation, et la plupart de ces fichiers sont répertoriés dans le [tableau file](file-table.md). La [table de répertoires](directory-table.md) n’est pas affichée dans la figure, mais elle est étroitement liée au groupe de tables de fichiers. La table de répertoires fournit la structure de répertoire de l’installation.

Le groupe de fichiers des tables contient toutes les tables liées aux fichiers.

-   Le [tableau fichier](file-table.md) répertorie les fichiers appartenant à l’installation. Les fichiers qui ne sont pas répertoriés dans le tableau de fichiers incluent les fichiers de disque, qui sont répertoriés dans la table des médias. Étant donné que chaque fichier appartient à un composant, la table de fichiers a une clé externe dans la table des composants.
-   La [table RemoveFile](removefile-table.md) contient une liste de fichiers à supprimer par l' [action RemoveFiles](removefiles-action.md).
-   Le [tableau des polices](font-table.md) répertorie les fichiers de polices à inscrire auprès du système.
-   La [table Selfreg](selfreg-table.md) répertorie les fichiers de module de l’installation qui sont auto-inscrits.
-   La [table des médias](media-table.md) répertorie le support source et les disques appartenant à l’installation.
-   La [table BindImage](bindimage-table.md) répertorie les fichiers qui sont liés aux dll importées par les exécutables.
-   La [table MoveFile](movefile-table.md) spécifie les fichiers qui sont déplacés au cours de l’installation.
-   La [table DuplicateFile](duplicatefile-table.md) spécifie les fichiers qui sont dupliqués pendant l’installation.
-   La [table inifile](inifile-table.md) répertorie les fichiers de .ini et les informations que l’application doit définir dans le fichier.
-   La [table RemoveIniFile](removeinifile-table.md) contient les informations qu’une application doit supprimer d’un fichier .ini.
-   La [table d’environnement](environment-table.md) est utilisée pour définir les valeurs des variables d’environnement.
-   Le [tableau icône](icon-table.md) contient des informations sur les icônes qui sont copiées dans un fichier dans le cadre de l’annonce du produit.
-   La [table FileSFPCatalog](filesfpcatalog-table.md) associe les fichiers spécifiés aux fichiers de catalogue de protection des fichiers système.

    **Windows Vista, Windows Server 2003 et Windows XP :** Non pris en charge.

-   La [table SFPCatalog](sfpcatalog-table.md) contient des catalogues de protection de fichiers système.

    **Windows Vista, Windows Server 2003 et Windows XP :** Non pris en charge.

-   la [table MsiFileHash](msifilehash-table.md) est utilisée pour stocker un hachage 128 bits d’un fichier source fourni par le package Windows Installer.

 

 



