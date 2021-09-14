---
description: le WiImport.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. cet exemple montre comment écrire un script pour importer des tables dans une base de données Windows Installer.
ms.assetid: 37580bd6-30c7-4239-9717-223a381ba021
title: Importer des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8508ee4e385e3edc737515f1b524de074489fb2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021396"
---
# <a name="import-files"></a>Importer des fichiers

le WiImport.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). cet exemple montre comment écrire un script pour importer des tables dans une base de données Windows Installer.

Le script se connecte à un objet [**installer**](installer-object.md) , ouvre une base de données, traite une liste de fichiers et valide les modifications avant de fermer la base de données.

L’exemple illustre l’utilisation de :

-   [**OpenDatabase, méthode (objet installer)**](installer-opendatabase.md)
-   [**Méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [ **objet installer**](installer-object.md)
-   [**Import, méthode**](database-import.md)
-   [**Méthode Commit**](database-commit.md) de l' [ **objet Database**](database-object.md)

vous aurez besoin de la version CScript.exe ou WScript.exe de Windows Script Host pour utiliser cet exemple. Pour utiliser CScript.exe pour exécuter cet exemple, utilisez la syntaxe suivante à l’invite de commandes.

**cscript WiImport.vbs \[ chemin de la base de données \] \[ chemin d’accès aux options de dossier \] \[ liste des fichiers d' \] \[ Archive**\]

L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant. Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ chemin d’accès au fichier \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.

spécifiez le chemin d’accès à un Windows base de données du programme d’installation qui doit être créé ou qui doit recevoir les tables importées. Spécifiez le chemin d’accès au dossier contenant les fichiers d’archive des tables en cours d’importation. Répertoriez les noms des fichiers d’archive en cours d’importation. Les noms de fichiers génériques, tels que \* . IDT, peuvent être utilisés pour importer plusieurs fichiers.

Les options suivantes peuvent être spécifiées n’importe où sur la ligne de commande avant la liste des fichiers.



| Option              | Description                                                                                                                          |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| aucune option spécifiée | importez la liste des fichiers d’archive de table à partir du dossier spécifié dans la base de données Windows Installer.                                |
| /C                  | créez un Windows Installer base de données, puis importez la liste des fichiers d’archive de table à partir du dossier spécifié dans la nouvelle base de données. |



 

pour plus d’informations, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md) pour des exemples de scripts supplémentaires. pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows hôte de Script, consultez [Windows Installer outils de développement](windows-installer-development-tools.md).

Notez qu' [un exemple de localisation](a-localization-example.md) illustre également l' [importation de tables Error et ActionText localisées](importing-localized-error-and-actiontext-tables.md).

 

 



