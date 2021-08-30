---
description: le WiMerge.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. cet exemple de script fusionne une base de données Windows Installer dans une autre base de données. Pour plus d’informations, consultez fusions et transformations.
ms.assetid: 31867082-7c1d-4530-a066-236d8ee5f023
title: Fusionner deux bases de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e534e20c1717b1d014cae8ed9548fd1d0950d80b6b26ba5cfce6ba15bd7cb53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869179"
---
# <a name="merge-two-databases"></a>Fusionner deux bases de données

le WiMerge.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). cet exemple de script fusionne une base de données Windows Installer dans une autre base de données. Pour plus d’informations, consultez [fusions et transformations](merges-and-transforms.md).

La fonction [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) et la méthode [**Merge**](database-merge.md) de l’objet [**Database**](database-object.md) ne peuvent pas être utilisées pour fusionner un module inclus dans le package d’installation. ils ne doivent pas être utilisés pour fusionner des [Modules de fusion](merge-modules.md) dans un package de Windows Installer. Pour inclure un module de fusion dans un package d’installation, les auteurs des packages d’installation doivent suivre les instructions décrites dans la rubrique [application de modules de fusion](applying-merge-modules.md) .

L’exemple illustre l’utilisation des éléments suivants :

-   [**OpenDatabase, méthode (objet installer)**](installer-opendatabase.md)
-   [**Méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [ **objet installer**](installer-object.md)
-   [**OpenView, méthode**](database-openview.md)
-   [**Merge (méthode)**](database-merge.md)
-   [**Méthode Commit**](database-commit.md) de l' [ **objet Database**](database-object.md)
-   [**Méthode fetch**](view-fetch.md)
-   [**Afficher l’objet**](view-object.md)
-   [**Propriété StringData**](record-stringdata.md) de l' [ **objet record**](record-object.md)

vous devez disposer de la version CScript.exe ou WScript.exe de Windows Script Host pour utiliser cet exemple. Pour utiliser CScript.exe pour exécuter cet exemple, tapez une ligne de commande à l’invite de commandes en utilisant la syntaxe suivante. L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant. Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ chemin d’accès au fichier \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.

**cscript WiMerge.vbs \[ chemin d’accès au chemin d’accès de la base de données \] \[ importé \] \[\]**

spécifiez le chemin d’accès à la base de données Windows Installer qui reçoit la fusion. Spécifiez le chemin d’accès à la base de données importée dans la première. Vous pouvez spécifier un nom facultatif pour une table qui contiendra les erreurs de fusion. Si aucun nom de table n’est spécifié, le programme d’installation utilise le nom \_ MergeErrors et supprime la table après avoir affiché le contenu.

pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md). pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows hôte de Script, consultez [Windows Installer outils de développement](windows-installer-development-tools.md).

 

 



