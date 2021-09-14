---
description: le WiSubStg.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer.
ms.assetid: a0248dfb-e406-4ce6-ab11-1e428aa67af4
title: Gérer les sous-stockages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01876efdb85bdc89df1b4d64332d44674e5e860e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011919"
---
# <a name="manage-substorages"></a>Gérer les sous-stockages

le WiSubStg.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). cet exemple montre comment le script peut être utilisé pour gérer les sous-stockages dans une base de données Windows Installer. une transformation peut être ajoutée à une base de données Windows Installer existante en tant que sous-stockage.

L’exemple illustre l’utilisation de :

-   [\_Table de stockage](-storages-table.md)
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

**cscript WiSubStg.vbs \[ chemin du chemin de la base de données \] \[ vers les options de fichier \] \[ \] \[ nom du sous-stockage\]**

spécifiez le chemin d’accès à la base de données Windows Installer pour ajouter ou supprimer le sous-stockage. Spécifiez un chemin d’accès à la transformation ou au fichier de base de données qui est ajouté en tant que sous-stockage. pour répertorier les sous-stockages de la base de données Windows Installer, omettez le chemin d’accès à ce fichier. Vous pouvez spécifier un nom de sous-stockage facultatif. Si cette valeur est omise, le nom du sous-stockage est par défaut le nom du fichier.

L’option suivante peut être spécifiée.



| Option              | Description                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| aucune option spécifiée | ajoutez un sous-stockage à la base de données Windows Installer.                                                 |
| /d                  | Supprimer un sous-stockage. Cet indicateur d’option doit être suivi du nom du sous-stockage à supprimer. |



 

pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md). pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows hôte de Script, consultez [Windows Installer outils de développement](windows-installer-development-tools.md).

Notez qu' [un exemple de localisation](a-localization-example.md) illustre l' [incorporation de transformations de personnalisation en tant que sous-stockage](embedding-customization-transforms-as-substorage.md).

 

 



