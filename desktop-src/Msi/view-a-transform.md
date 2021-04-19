---
description: Le WiLstXfm.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. Cet exemple de script peut être utilisé pour afficher un fichier de transformation.
ms.assetid: c2e3dd56-b0e5-481a-b7b8-5000fa686850
title: Afficher une transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f4a858f8deb115de967da3b4d485b596f85cee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515634"
---
# <a name="view-a-transform"></a>Afficher une transformation

Le WiLstXfm.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Cet exemple de script peut être utilisé pour afficher un fichier de transformation.

L’exemple illustre l’utilisation de :

-   [\_Table TransformView](-transformview-table.md)
-   [**OpenDatabase, méthode (objet installer)**](installer-opendatabase.md)
-   [**Méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [ **objet installer**](installer-object.md)
-   [**Méthode ApplyTransform**](database-applytransform.md)
-   [**OpenView, méthode**](database-openview.md)
-   [**Méthode Commit**](database-commit.md) de l' [ **objet Database**](database-object.md)
-   [**IsNull, propriété**](record-isnull.md)
-   [**Propriété StringData**](record-stringdata.md) de l' [ **objet record**](record-object.md)

L’utilisation de cet exemple nécessite la version CScript.exe de Windows Script Host. Pour utiliser CScript.exe pour exécuter cet exemple, tapez une commande à l’invite de commandes en utilisant la syntaxe suivante. L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant. Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.

**cscript WiLstXfm.vbs** chemin d’accès de l' *\[ option de base de données de référence à \] \[ \] \[ transformer à afficher \]*

Spécifiez le chemin d’accès à la base de données de référence Windows Installer. Spécifiez une liste de chemins d’accès pour transformer les fichiers en cours d’affichage. Chaque chemin d’accès dans la liste peut être précédé d’une valeur numérique facultative. Cette valeur spécifie un ensemble de conditions d’erreur qui doivent être supprimées. Vous pouvez ajouter ces valeurs ensemble pour supprimer plusieurs conditions. Si aucune option numérique n’est spécifiée, toutes les conditions d’erreur sont supprimées. Les arguments de cette liste sont exécutés dans l’ordre de gauche à droite dans lequel ils apparaissent sur la ligne de commande.



| Valeur | Condition d’erreur à supprimer                   |
|-------|-----------------------------------------------|
| 1     | Ajout d’une ligne qui existe déjà.             |
| 2     | Suppression d’une ligne qui n’existe pas.           |
| 4     | Ajout d’une table qui existe déjà.           |
| 8     | Suppression d’une table qui n’existe pas.         |
| 16    | Mise à jour d’une ligne qui n’existe pas.           |
| 256   | Incompatibilité de la base de données et transformation de pages. |



 

Pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md). Pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows Script Host, consultez [Windows Installer les outils de développement](windows-installer-development-tools.md).

 

 



