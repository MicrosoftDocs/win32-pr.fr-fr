---
description: le WiFilVer.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. L’exemple vous montre comment vous pouvez utiliser un script pour signaler ou mettre à jour la version de fichier, la taille et les informations de langue.
ms.assetid: 21550eea-c30b-4738-9201-ab500356fabf
title: Gérer les tailles et les versions des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426acf71956d87fe1458447119d79bc142f1ee75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021358"
---
# <a name="manage-file-sizes-and-versions"></a>Gérer les tailles et les versions des fichiers

le WiFilVer.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). L’exemple vous montre comment vous pouvez utiliser un script pour signaler ou mettre à jour la version de fichier, la taille et les informations de langue.

l’exemple montre également Windows Installer actions, comment accéder à une base de données Windows Installer et utiliser les éléments suivants :

-   Méthode [**installer. OpenDatabase**](installer-opendatabase.md) de l' [ **objet installer**](installer-object.md)
-   [**Installer. FileAttributes,**](installer-fileattributes.md) propriété
-   [**Installer. FileHash,**](installer-filehash.md) méthode
-   [**Installer. FileVersion,**](installer-fileversion.md) méthode
-   Méthode [**installer. LastErrorRecord**](installer-lasterrorrecord.md) de l' [ **objet installer**](installer-object.md)
-   [**Database. OpenView,**](database-openview.md) méthode
-   Propriété [**Database. SummaryInformation**](database-summaryinformation.md) de l' [ **objet Database**](database-object.md)
-   [**Session. subaction,**](session-doaction.md) méthode
-   [**Session. Property**](session-session.md)
-   [**Session. SourcePath,**](session-sourcepath.md) propriété
-   Propriété [**session. mode**](session-mode.md) de l' [ **objet session**](session-object.md)
-   [**Record. StringData,**](record-stringdata.md) propriété
-   Propriété [**record. IntegerData**](record-integerdata.md) de l' [ **objet record**](record-object.md)

l’utilisation de cet exemple nécessite la version CScript.exe ou WScript.exe de Windows Script Host. Pour utiliser CScript.exe pour exécuter cet exemple, tapez une commande à l’invite de commandes en utilisant la syntaxe suivante :

**cscript WiFilVer.vbs \[ chemin d’accès à la base de données \] \[ emplacements sources facultatifs\]**

Tenez également compte des éléments suivants :

-   L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant.
-   Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] .
-   L’exemple retourne la valeur 0 (zéro) pour Success, 1 (un) si l’aide est appelée, et 2 (deux) si le script échoue.

spécifiez la base de données Windows Installer que vous souhaitez mettre à jour, qui doit se trouver à la racine du fichier source. Toutefois, vous pouvez spécifier des sources pour la base de données à des emplacements distincts. Si la source est compressée, tous les fichiers sont ouverts à la racine.

Les options suivantes peuvent être spécifiées à n’importe quel emplacement sur la ligne de commande.



| Option                | Description                                                                              |
|-----------------------|------------------------------------------------------------------------------------------|
| *aucune option spécifiée* | Affichez les informations de fichier de la base de données.                                            |
| /U                    | Mettez à jour la taille du fichier, la version et les informations de langue dans la base de données à partir de la source. |



 

pour plus d’informations, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md) et [Windows Installer outils de développement](windows-installer-development-tools.md).

 

 



