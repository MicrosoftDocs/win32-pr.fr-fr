---
description: le WiLstScr.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. cet exemple de script illustre la Windows Installer script viewer.
ms.assetid: 18989c16-e0c8-4d11-b915-730951b6845b
title: Afficher le script du programme d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4797d73c4c90266b94a02b9d73657fb95de75e153617ef1e34797f28035ee701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803980"
---
# <a name="view-installer-script"></a>Afficher le script du programme d’installation

le WiLstScr.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). cet exemple de script illustre la Windows Installer script viewer.

L’exemple illustre l’utilisation de :

-   [**OpenDatabase, méthode (objet installer)**](installer-opendatabase.md)
-   Méthode [**LastErrorRecord**](installer-lasterrorrecord.md) de l’objet [**installer**](installer-object.md)
-   Méthode [**OpenView**](database-openview.md) de l’objet [**Database**](database-object.md)
-   Méthode [**Fetch**](view-fetch.md) de l’objet [**View**](view-object.md)
-   Méthode [**FormatText**](record-formattext.md)
-   [**FieldCount**](record-fieldcount.md) , propriété
-   Propriété [**StringData**](record-stringdata.md) de l’objet [**Record**](record-object.md)
-   [\_Table TransformView](-transformview-table.md)

l’utilisation de cet exemple nécessite la version CScript.exe de Windows hôte de Script. Pour utiliser CScript.exe pour exécuter cet exemple, tapez une commande à l’invite de commandes en utilisant la syntaxe suivante. L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant. Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.

**cscript WiLstScr.vbs** *\[ chemin d’accès au script \] d’exécution de Windows Installer*

Spécifiez le chemin d’accès au script d’exécution du programme d’installation.

pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md). pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows hôte de Script, consultez [Windows Installer outils de développement](windows-installer-development-tools.md).

 

 



