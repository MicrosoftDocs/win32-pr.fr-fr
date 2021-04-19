---
description: Le WiRunSQL.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer.
ms.assetid: 1027b187-1237-43d1-9905-8fcdaec63903
title: Exécuter des instructions SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99da54f85b02ee867003b140d505f5754f58cc00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527845"
---
# <a name="execute-sql-statements"></a>Exécuter des instructions SQL

Le WiRunSQL.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Cet exemple montre comment le script est utilisé pour exécuter des requêtes SQL et des mises à jour sur une base de données Windows Installer. Pour plus d’informations, consultez [syntaxe SQL](sql-syntax.md) et [exemples de requêtes de base de données à l’aide de SQL et de script](examples-of-database-queries-using-sql-and-script.md).

L’exemple de script illustre les éléments suivants :

-   [**OpenDatabase, méthode (objet installer)**](installer-opendatabase.md) et [**méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [**objet installer**](installer-object.md)
-   [**OpenView, méthode**](database-openview.md)et [**méthode Commit**](database-commit.md) de l' [**objet Database**](database-object.md)
-   [**Méthode Execute**](view-execute.md) de l' [ **objet View**](view-object.md)
-   [**Propriété StringData**](record-stringdata.md) Propertyof l' [ **objet record**](record-object.md)

L’utilisation de cet exemple nécessite la version CScript.exe ou WScript.exe de Windows Script Host. Pour utiliser CScript.exe pour exécuter cet exemple, tapez une commande à l’invite de commandes en utilisant la syntaxe suivante. L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant. Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.

**cscript WiRunSQL.vbs \[ chemin d’accès aux \] \[ requêtes SQL de base de données\]**

Spécifiez le chemin d’accès à une base de données Windows Installer. Spécifiez les requêtes SQL à exécuter. Notez que la requête SQL doit être placée entre guillemets doubles. Les requêtes SELECT affichent les lignes de la liste de résultats spécifiée dans la requête. Les colonnes de données binaires sélectionnées par une requête ne sont pas affichées.

Pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md). Pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows Script Host, consultez [Windows Installer les outils de développement](windows-installer-development-tools.md).

Pour plus d’informations, consultez [utilisation de requêtes](working-with-queries.md) et [d’exemples de requêtes de base de données à l’aide de SQL et de script](examples-of-database-queries-using-sql-and-script.md). L' [exemple](a-localization-example.md) suivant illustre l’utilisation de SQL pour la localisation des [colonnes de base de données](localizing-database-columns.md) et [la mise à jour d’un flux d’informations de synthèse](updating-a-summary-information-stream.md).

 

 



