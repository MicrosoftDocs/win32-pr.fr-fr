---
description: le WiUseXfm.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. cet exemple montre comment le script peut être utilisé pour appliquer une transformation à une base de données Windows Installer.
ms.assetid: e647388e-5211-463d-9e3e-b502af01fc0c
title: Appliquer une transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 001737b1a08ea33ce233fa0aad90e96e23a1079f2c28f9d6308219cba270f6ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381608"
---
# <a name="apply-a-transform"></a>Appliquer une transformation

le WiUseXfm.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). cet exemple montre comment le script peut être utilisé pour appliquer une transformation à une base de données Windows Installer.

L’exemple illustre l’utilisation de

-   [**OpenDatabase, méthode (objet installer)**](installer-opendatabase.md)
-   [**Méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [ **objet installer**](installer-object.md)
-   [**Méthode ApplyTransform**](database-applytransform.md)
-   [**Méthode Commit**](database-commit.md) de l' [ **objet Database**](database-object.md)

vous aurez besoin de la version CScript.exe ou WScript.exe de Windows Script Host pour utiliser cet exemple. Pour utiliser CScript.exe pour exécuter cet exemple, tapez une ligne de commande à l’invite de commandes en utilisant la syntaxe suivante. L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant. Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.

**cscript WiUseXfm.vbs \[ chemin d’accès au chemin d’accès de la base de données d’origine \] \[ pour transformer les \] \[ Options du fichier\]**

spécifiez le chemin d’accès à la base de données Windows Installer. Spécifiez le chemin d’accès au fichier de transformation. Si le chemin d’accès au fichier de transformation est omis, les deux bases de données sont comparées uniquement. Le troisième argument est une valeur numérique facultative qui spécifie un jeu de conditions d’erreur qui doivent être supprimées. Ajoutez ces valeurs ensemble pour supprimer plusieurs conditions.



| Valeur | Condition d’erreur à supprimer                   |
|-------|-----------------------------------------------|
| 1     | Ajout d’une ligne qui existe déjà.             |
| 2     | Suppression d’une ligne qui n’existe pas.           |
| 4     | Ajout d’une table qui existe déjà.           |
| 8     | Suppression d’une table qui n’existe pas.         |
| 16    | Mise à jour d’une ligne qui n’existe pas.           |
| 256   | Incompatibilité de la base de données et transformation de pages. |



 

pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md). pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows hôte de Script, consultez [Windows Installer outils de développement](windows-installer-development-tools.md).

 

 



