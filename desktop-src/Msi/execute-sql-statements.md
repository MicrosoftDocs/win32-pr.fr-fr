---
description: le WiRunSQL.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer.
ms.assetid: 1027b187-1237-43d1-9905-8fcdaec63903
title: exécuter des instructions SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7893da9c49ad1aaff4d19726cbcfce86f80293d9ffaa4c8e01569dd83a2d3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044489"
---
# <a name="execute-sql-statements"></a>exécuter des instructions SQL

le WiRunSQL.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). cet exemple montre comment le script est utilisé pour exécuter des SQL des requêtes et des mises à jour sur une base de données Windows Installer. pour plus d’informations, consultez [SQL syntaxe](sql-syntax.md) et [des exemples de requêtes de base de données à l’aide d’SQL et d’un Script](examples-of-database-queries-using-sql-and-script.md).

L’exemple de script illustre les éléments suivants :

-   [**OpenDatabase, méthode (objet installer)**](installer-opendatabase.md) et [**méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [**objet installer**](installer-object.md)
-   [**OpenView, méthode**](database-openview.md)et [**méthode Commit**](database-commit.md) de l' [**objet Database**](database-object.md)
-   [**Méthode Execute**](view-execute.md) de l' [ **objet View**](view-object.md)
-   [**Propriété StringData**](record-stringdata.md) Propertyof l' [ **objet record**](record-object.md)

l’utilisation de cet exemple nécessite la version CScript.exe ou WScript.exe de Windows Script Host. Pour utiliser CScript.exe pour exécuter cet exemple, tapez une commande à l’invite de commandes en utilisant la syntaxe suivante. L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant. Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.

**cscript WiRunSQL.vbs \[ chemin d’accès aux \] \[ requêtes de SQL de base de données\]**

spécifiez le chemin d’accès à une base de données Windows Installer. spécifiez les SQL requêtes à exécuter. notez que la requête de SQL doit être placée entre guillemets doubles. Les requêtes SELECT affichent les lignes de la liste de résultats spécifiée dans la requête. Les colonnes de données binaires sélectionnées par une requête ne sont pas affichées.

pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md). pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows hôte de Script, consultez [Windows Installer outils de développement](windows-installer-development-tools.md).

pour plus d’informations, consultez [utilisation de requêtes](working-with-queries.md) et [d’exemples de requêtes de base de données à l’aide d’SQL et de scripts](examples-of-database-queries-using-sql-and-script.md). l' [exemple](a-localization-example.md) suivant illustre l’utilisation de SQL pour la localisation des [colonnes de base de données](localizing-database-columns.md) et [la mise à jour d’un flux d’informations de synthèse](updating-a-summary-information-stream.md).

 

 



