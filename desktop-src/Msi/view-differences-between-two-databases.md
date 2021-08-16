---
description: le WiDiffDb.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. cet exemple de script génère un fichier de transformation temporaire entre deux Windows Installer bases de données et affiche la transformation.
ms.assetid: 9750ddc6-de8d-48e9-a984-892f0cf4ac3b
title: Afficher les différences entre deux bases de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbb04ad6ed1ecaa9d4d5be73708c5edc7dc8c84c9fe230a3725f971d949d335
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375912"
---
# <a name="view-differences-between-two-databases"></a>Afficher les différences entre deux bases de données

le WiDiffDb.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). cet exemple de script génère un fichier de transformation temporaire entre deux Windows Installer bases de données et affiche la transformation.

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

l’utilisation de cet exemple nécessite la version CScript.exe de Windows hôte de Script. Pour utiliser CScript.exe pour exécuter cet exemple, tapez une commande à l’invite de commandes en utilisant la syntaxe suivante. L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant. Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.

**cscript WiDiffDb.vbs** chemin d’accès *\[ au \] \[ chemin d’accès \] de la base* de données modifiée

spécifiez le chemin d’accès à la base de données d’Windows Installer d’origine. Spécifiez le chemin d’accès à la base de données modifiée. L’exemple de script affiche la transformation.

pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md). pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows hôte de Script, consultez [Windows Installer outils de développement](windows-installer-development-tools.md).

 

 



