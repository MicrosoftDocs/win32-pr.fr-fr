---
description: le WiDialog.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. cet exemple montre comment le script est utilisé pour afficher un aperçu des dialogues dans une base de données Windows Installer.
ms.assetid: b3d72ba1-1d19-4460-8b9b-94f72214e8b1
title: Aperçu de l’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572ab444cc2f6acb6ec426f842318201187336121aa9c2a0557fca8cab94a3ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074709"
---
# <a name="preview-user-interface"></a>Aperçu de l’interface utilisateur

le WiDialog.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). cet exemple montre comment le script est utilisé pour afficher un aperçu des dialogues dans une base de données Windows Installer.

Cet exemple montre :

-   [**OpenDatabase, méthode (objet installer)**](installer-opendatabase.md), [**méthode CreateRecord**](installer-createrecord.md)et [**méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [**objet installer**](installer-object.md)
-   [**OpenView, méthode**](database-openview.md) et [**méthode EnableUIpreview**](database-enableuipreview.md) de l' [**objet Database**](database-object.md)
-   [**Méthode Execute**](view-execute.md) et [**méthode fetch**](view-fetch.md) de l' [**objet View**](view-object.md)
-   [**Propriété StringData**](record-stringdata.md) Propertyof l' [ **objet record**](record-object.md)

cet exemple requiert la version CScript.exe ou WScript.exe de Windows Script Host. Pour utiliser CScript.exe pour cet exemple, tapez une commande à l’invite de commandes en utilisant la syntaxe suivante. L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant. Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.

**cscript WiDialog.vbs** *\[ chemin d’accès aux \] \[ noms \] de boîte de dialogue de base de données*

spécifiez le chemin d’accès à une base de données Windows Installer. Spécifiez le nom d’une boîte de dialogue. Ce nom doit figurer dans la colonne boîte de dialogue de la [table boîte de dialogue](dialog-table.md). Pour afficher un panneau, ajoutez le nom de la boîte de dialogue avec le nom du contrôle à partir de la [table de contrôle](control-table.md) , puis ajoutez-le au nom du tableau blanc dans la [table du tableau blanc](billboard-table.md). Si aucune boîte de dialogue n’est spécifiée, toutes les boîtes de dialogue de la table de boîte de dialogue s’affichent de façon séquentielle.

pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md). pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows hôte de Script, consultez [Windows Installer outils de développement](windows-installer-development-tools.md).

 

 



