---
description: Le WiLstScr.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. Cet exemple de script illustre la Windows Installer script Viewer.
ms.assetid: 18989c16-e0c8-4d11-b915-730951b6845b
title: Afficher le script du programme d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56888f478bb7cdd43ebcee817c86f6f9f163840e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527345"
---
# <a name="view-installer-script"></a>Afficher le script du programme d’installation

Le WiLstScr.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Cet exemple de script illustre la Windows Installer script Viewer.

L’exemple illustre l’utilisation de :

-   [**OpenDatabase, méthode (objet installer)**](installer-opendatabase.md)
-   Méthode [**LastErrorRecord**](installer-lasterrorrecord.md) de l’objet [**installer**](installer-object.md)
-   Méthode [**OpenView**](database-openview.md) de l’objet [**Database**](database-object.md)
-   Méthode [**Fetch**](view-fetch.md) de l’objet [**View**](view-object.md)
-   Méthode [**FormatText**](record-formattext.md)
-   [**FieldCount**](record-fieldcount.md) , propriété
-   Propriété [**StringData**](record-stringdata.md) de l’objet [**Record**](record-object.md)
-   [\_Table TransformView](-transformview-table.md)

L’utilisation de cet exemple nécessite la version CScript.exe de Windows Script Host. Pour utiliser CScript.exe pour exécuter cet exemple, tapez une commande à l’invite de commandes en utilisant la syntaxe suivante. L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant. Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.

**cscript WiLstScr.vbs** *\[ chemin d’accès au script \] d’exécution de Windows Installer*

Spécifiez le chemin d’accès au script d’exécution du programme d’installation.

Pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md). Pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows Script Host, consultez [Windows Installer les outils de développement](windows-installer-development-tools.md).

 

 



