---
description: Le WiDiffDb.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. Cet exemple de script génère un fichier de transformation temporaire entre deux Windows Installer bases de données et affiche la transformation.
ms.assetid: 9750ddc6-de8d-48e9-a984-892f0cf4ac3b
title: Afficher les différences entre deux bases de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b0c97afc0bd7145170209ed87497b6af90e64d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525875"
---
# <a name="view-differences-between-two-databases"></a>Afficher les différences entre deux bases de données

Le WiDiffDb.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Cet exemple de script génère un fichier de transformation temporaire entre deux Windows Installer bases de données et affiche la transformation.

L’exemple illustre l’utilisation de :

-   [**OpenDatabase, méthode (objet installer)**](installer-opendatabase.md)
-   [**Méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [ **objet installer**](installer-object.md)
-   [**OpenView, méthode**](database-openview.md)
-   [**Propriété SummaryInformation (objet Database)**](database-summaryinformation.md)
-   [**GenerateTransform, méthode**](database-generatetransform.md)
-   [**Méthode ApplyTransform**](database-applytransform.md)
-   [**Objet de base de données**](database-object.md)
-   [**Méthode fetch**](view-fetch.md) de l' [ **objet View**](view-object.md)
-   [**IsNull, propriété**](record-isnull.md)
-   [**Propriété StringData**](record-stringdata.md) de l' [ **objet record**](record-object.md)
-   [\_Table TransformView](-transformview-table.md)

L’utilisation de cet exemple nécessite la version CScript.exe de Windows Script Host. Pour utiliser CScript.exe pour exécuter cet exemple, tapez une commande à l’invite de commandes en utilisant la syntaxe suivante. L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant. Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.

**cscript WiDiffDb.vbs** chemin d’accès *\[ au \] \[ chemin d’accès \] de la base* de données modifiée

Spécifiez le chemin d’accès à la base de données d’Windows Installer d’origine. Spécifiez le chemin d’accès à la base de données modifiée. L’exemple de script affiche la transformation.

Pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md). Pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows Script Host, consultez [Windows Installer les outils de développement](windows-installer-development-tools.md).

 

 



