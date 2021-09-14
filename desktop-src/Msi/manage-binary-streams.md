---
description: le WiStream.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer.
ms.assetid: f96d1fdd-81c8-4fb2-a23e-fda49ace8bef
title: Gérer les Flux binaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877631a40157a5d286ef0c2575732a6d561eefb8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011923"
---
# <a name="manage-binary-streams"></a>Gérer les Flux binaires

le WiStream.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). cet exemple montre comment le script peut être utilisé pour gérer des flux binaires dans une base de données Windows Installer. L’exemple peut être utilisé pour entrer des fichiers CAB compressés dans une base de données. cet exemple illustre l’opération de la [ \_ table Flux](-streams-table.md) dans la base de données Windows Installer.

L’exemple illustre également l’utilisation de :

-   [**OpenDatabase, méthode (objet installer)**](installer-opendatabase.md)
-   [**Méthode CreateRecord**](installer-createrecord.md)
-   [**Méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [ **objet installer**](installer-object.md)
-   [**OpenView, méthode**](database-openview.md)
-   [**Méthode Commit**](database-commit.md) de l' [ **objet Database**](database-object.md)
-   [**Méthode fetch**](view-fetch.md)
-   [**Modify, méthode**](view-modify.md)
-   [**Méthode Execute**](view-execute.md) de l' [ **objet View**](view-object.md)
-   [**StringData, propriété**](record-stringdata.md)
-   [**Méthode SetStream**](record-setstream.md) de l' [ **objet record**](record-object.md)

vous aurez besoin de la version CScript.exe ou WScript.exe de Windows Script Host pour utiliser cet exemple. Pour utiliser CScript.exe pour exécuter cet exemple, tapez une ligne de commande à l’invite de commandes en utilisant la syntaxe suivante. L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant. Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.

**cscript WiStream.vbs \[ chemin d’accès au chemin de la base de données \] \[ Options du fichier \] \[ nom du \] \[ flux\]**

spécifiez le chemin d’accès à la base de données Windows Installer qui doit recevoir le flux. Spécifiez un chemin d’accès au fichier binaire contenant les données de flux. Pour afficher la liste des flux dans la base de données du programme d’installation, omettez ce chemin. Vous pouvez spécifier un nom de flux facultatif. si ce paramètre est omis, le nom de fichier est utilisé par défaut.

L’option suivante peut être spécifiée.



| Option              | Description                                                                                     |
|---------------------|-------------------------------------------------------------------------------------------------|
| aucune option spécifiée | ajoutez un flux à la base de données Windows Installer.                                                 |
| /d                  | Supprimer un flux. Cet indicateur d’option doit être suivi du nom du sous-stockage en cours de suppression. |



 

pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md). pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows hôte de Script, consultez [Windows Installer outils de développement](windows-installer-development-tools.md).

 

 



