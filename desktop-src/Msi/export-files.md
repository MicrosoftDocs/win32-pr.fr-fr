---
description: le WiExport.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer.
ms.assetid: 3ff7bd48-cb22-4d5b-a607-39eaeb67c55b
title: Exporter des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7cab882778bce6d84412f53987c65211f70f4a8a10b52836ad993d8e813304
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044439"
---
# <a name="export-files"></a>Exporter des fichiers

le WiExport.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). cet exemple montre comment écrire un script pour exporter des tables dans une base de données Windows Installer. L’exemple de script se connecte à un objet [**installer**](installer-object.md) , ouvre une base de données et exporte des tables vers des fichiers d’archive.

L’exemple illustre l’utilisation de :

-   [**OpenDatabase, méthode (objet installer)**](installer-opendatabase.md)
-   [**Méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [ **objet installer**](installer-object.md)
-   [**Méthode d’exportation**](database-export.md)
-   [**Méthode OpenView**](database-openview.md) de l' [ **objet Database**](database-object.md)
-   [**Méthode fetch**](view-fetch.md) de l' [ **objet View**](view-object.md)
-   [**Propriété StringData**](record-stringdata.md) de l' [ **objet record**](record-object.md)

vous aurez besoin de la version CScript.exe ou WScript.exe de Windows Script Host pour utiliser cet exemple. Pour utiliser CScript.exe pour exécuter cet exemple, tapez une ligne de commande à l’invite de commandes en utilisant la syntaxe suivante. L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant. Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.

**cscript WiExport.vbs chemin d’accès de la \[ base de données \] \[ aux options du dossier \] \[ liste des noms de \] \[ table\]**

Spécifiez le chemin d’accès à la base de données du programme d’installation à partir de laquelle les tables sont exportées. Spécifiez le chemin d’accès au dossier dans lequel les fichiers d’archive exportés doivent être copiés. Répertorie les noms qui respectent la casse des [tables de base de données](database-tables.md) en cours d’exportation. Spécifiez « \* » pour exporter toutes les tables, y compris \_ SummaryInformation.

Les options suivantes peuvent être spécifiées n’importe où sur la ligne de commande avant la liste nom de la table.



| Option              | Description                                            |
|---------------------|--------------------------------------------------------|
| aucune option spécifiée | Les fichiers d’archive exportés peuvent avoir un nom de fichier long.      |
| /s                  | Obliger les fichiers d’archive exportés à avoir des noms de fichiers courts. |



 

pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md). pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows hôte de Script, consultez [Windows Installer outils de développement](windows-installer-development-tools.md).

 

 



