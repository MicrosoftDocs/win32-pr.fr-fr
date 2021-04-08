---
description: Le WiCompon.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. Cet exemple de script peut être utilisé pour répertorier les composants d’une base de données Windows Installer.
ms.assetid: 4e6cc6f4-821a-4a10-a897-5c6aace1f702
title: Répertorier les composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b79fa34f62374632ec7fdf52a13c6da8ddbfd82a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751701"
---
# <a name="list-components"></a>Répertorier les composants

Le WiCompon.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Cet exemple de script peut être utilisé pour répertorier les composants d’une base de données Windows Installer.

Cet exemple illustre l’utilisation de la clé primaire dans la [table des composants](component-table.md).

L’exemple illustre également les éléments suivants :

-   [**OpenDatabase, méthode (objet installer)**](installer-opendatabase.md), la [**méthode CreateRecord**](installer-createrecord.md)et la [**méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [**objet installer**](installer-object.md).
-   [**OpenView**](database-openview.md), la [**propriété TablePersistent**](database-tablepersistent.md)et la [**propriété PrimaryKeys**](database-primarykeys.md) de l' [**objet de base de données**](database-object.md).
-   [**Méthode Execute**](view-execute.md) et [**méthode fetch**](view-fetch.md) de l' [**objet View**](view-object.md).
-   Propriété [**StringData**](record-stringdata.md) de l' [**objet record**](record-object.md).

L’utilisation de cet exemple nécessite la version CScript.exe ou WScript.exe de Windows Script Host. Pour utiliser CScript.exe pour exécuter cet exemple, tapez une commande à l’invite de commandes en utilisant la syntaxe suivante. L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant. Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.

**cscript WiCompon.vbs \[ chemin d’accès au \] \[ nom du composant de base de données\]**

Spécifiez le chemin d’accès à la base de données Windows Installer. Spécifiez le nom du composant. Le nom doit figurer dans la colonne composant de la [table des composants](component-table.md). Si le nom du composant est omis, tous les composants sont répertoriés. Si un astérisque ( \* ) est utilisé comme nom de composant, WiCompon.vbs répertorie la composition de tous les composants. Notez que les bases de données volumineuses sont mieux affichées en utilisant CScript plutôt que WScript.

Pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md). Pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows Script Host, consultez [Windows Installer les outils de développement](windows-installer-development-tools.md).

 

 



