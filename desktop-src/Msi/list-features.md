---
description: le WiFeatur.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer.
ms.assetid: 797cb383-22c0-42b4-82c1-d5bcc3a8bafb
title: Répertorier les fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ace52bcbd4f2f456de5bc4dcbddc6b169e468d309190af0965dfe19304b05a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810979"
---
# <a name="list-features"></a>Répertorier les fonctionnalités

le WiFeatur.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). cet exemple montre comment le script est utilisé pour répertorier les fonctionnalités d’une base de données Windows Installer. cet exemple illustre l’ajout de colonnes temporaires à une base de données Windows Installer en lecture seule.

Cet exemple montre :

-   [**OpenDatabase, méthode (objet installer)**](installer-opendatabase.md), [**méthode CreateRecord**](installer-createrecord.md)et [**méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [**objet installer**](installer-object.md)
-   [**Méthode Execute**](view-execute.md) et [**méthode fetch**](view-fetch.md) de l' [**objet View**](view-object.md)
-   [**Méthode OpenView**](database-openview.md), [**propriété TablePersistent**](database-tablepersistent.md)et [**propriété PrimaryKeys**](database-primarykeys.md) de l' [**objet Database**](database-object.md)
-   [**FieldCount**](record-fieldcount.md), propriété, [**IntegerData**](record-integerdata.md), et la [**propriété StringData**](record-stringdata.md) de l' [**objet record**](record-object.md)

l’utilisation de cet exemple nécessite la version CScript.exe ou WScript.exe de Windows Script Host. Pour utiliser CScript.exe pour exécuter cet exemple, tapez une commande à l’invite de commandes en utilisant la syntaxe suivante. L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant. Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.

**cscript WiFeatur.vbs \[ chemin d’accès au nom de la fonctionnalité de base de données \] \[\]**

spécifiez le chemin d’accès à la base de données Windows Installer. Spécifiez le nom de la fonctionnalité. Elle doit figurer dans la colonne Feature de la [table Feature](feature-table.md). Si le nom de la fonctionnalité est omis, toutes les fonctionnalités sont répertoriées sous la forme d’une arborescence de fonctionnalités. Si un astérisque ( \* ) est utilisé comme nom de fonctionnalité, WiFeatur.vbs répertorie la composition de toutes les fonctionnalités. Notez que les bases de données volumineuses sont mieux affichées en utilisant CScript plutôt que WScript.

pour plus d’informations, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md) pour des exemples de scripts supplémentaires. pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows hôte de Script, consultez [Windows Installer outils de développement](windows-installer-development-tools.md).

 

 



