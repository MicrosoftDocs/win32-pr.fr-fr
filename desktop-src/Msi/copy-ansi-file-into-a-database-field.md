---
description: L’exemple de fichier de code VBScript WiTextIn.vbs est fourni dans les composants SDK Windows pour les développeurs Windows Installer.
ms.assetid: ba6c6367-ebb1-4981-ae3a-bcff68aacdbf
title: Copier le fichier ANSI dans un champ de base de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc6c4d3a945177581a35bf6b19d89855abb5ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541832"
---
# <a name="copy-ansi-file-into-a-database-field"></a>Copier le fichier ANSI dans un champ de base de données

L’exemple de fichier de code VBScript WiTextIn.vbs est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). L’exemple montre comment utiliser un script pour copier un fichier dans un champ de texte d’une base de données Windows Installer, et illustre le traitement des données de clé primaire.

L’exemple de code vous montre également les éléments suivants :

-   [**OpenDatabase, méthode (objet installer)**](installer-opendatabase.md) et [**méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [**objet installer**](installer-object.md)
-   [**Méthode OpenView**](database-openview.md), [**méthode Commit**](database-commit.md)et [**propriété PrimaryKeys**](database-primarykeys.md) de l' [**objet Database**](database-object.md)
-   [**Méthode fetch**](view-fetch.md) et [**méthode modify**](view-modify.md) de l' [**objet View**](view-object.md)
-   [**Propriété StringData**](record-stringdata.md) et [**méthode ReadStream**](record-readstream.md) de l' [**objet record**](record-object.md)

Pour utiliser l’exemple de code, vous avez besoin de la version CScript.exe ou WScript.exe de Windows Script Host.

**Pour utiliser CScript.exe pour exécuter cet exemple**

-   À l’invite de commandes, tapez la syntaxe suivante :

    **cscript WiTextIn.vbs \[ chemin d’accès au nom de la table de base de données \] \[ \] \[ valeurs de clé primaire \] \[ chemin d' \] \[ accès au fichier\]**

> [!Note]  
> L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant.

 

**Pour rediriger la sortie vers un fichier**

-   Terminez la ligne de commande avec les éléments suivants : **VBS > \[ chemin d’accès au fichier \] . T**

> [!Note]  
> L’exemple retourne la valeur 0 (zéro) pour Success, 1 (un) si l’aide est appelée, et 2 (deux) si le script échoue.

 

La liste suivante identifie les éléments que vous devez spécifier :

-   Spécifiez le chemin d’accès à la base de données Windows Installer.
-   Spécifiez le nom de la table de base de données.
-   Spécifiez toutes les valeurs de clé primaire pour la ligne, dans l’ordre, et concaténées avec les signes deux-points.
-   Spécifiez un nom de colonne qui n’est pas une colonne clé. Il s’agit de la colonne à laquelle vous souhaitez recevoir les données.
-   Spécifiez le chemin d’accès au fichier texte copié.

> [!Note]  
> Si le dernier argument est omis, la valeur actuelle dans le champ est affichée.

 

Pour obtenir d’autres exemples de script, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md). Pour obtenir des exemples d’utilitaires qui ne nécessitent pas l’environnement d’exécution de scripts Windows, consultez [Windows Installer les outils de développement](windows-installer-development-tools.md).

 

 



