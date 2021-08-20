---
description: le WiGenXfm.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. cet exemple de script peut générer une transformation de deux bases de données Windows Installer. Pour plus d’informations, consultez transformations de base de données.
ms.assetid: bfa918b8-8d90-4e14-8a06-6c3d5b5dc13b
title: Générer une transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba16c894ec32bf300f1572eb26311be70315872b9711ca46573ce65e18802308
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142766"
---
# <a name="generate-a-transform"></a>Générer une transformation

le WiGenXfm.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). cet exemple de script peut générer une transformation de deux bases de données Windows Installer. Pour plus d’informations, consultez [transformations de base de données](database-transforms.md).

L’exemple illustre l’utilisation de :

[**OpenDatabase, méthode (objet installer)**](installer-opendatabase.md)

[**Méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [ **objet installer**](installer-object.md)

[**Méthode GenerateTransform**](database-generatetransform.md) de l' [ **objet de base de données**](database-object.md)

vous aurez besoin de la version CScript.exe ou WScript.exe de Windows Script Host pour utiliser cet exemple. Pour utiliser CScript.exe pour exécuter cet exemple, tapez une ligne de commande à l’invite de commandes en utilisant la syntaxe suivante. L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant. Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.

**cscript WiGenXfm.vbs chemin du chemin de la base de données d’origine vers le chemin \[ \] \[ de la base de données modifiée \] \[ pour transformer le fichier\]**

spécifiez le chemin d’accès à la base de données d’Windows Installer d’origine. Spécifiez le chemin d’accès à la base de données modifiée. Spécifiez le chemin d’accès au fichier de transformation à créer. Si le chemin d’accès au fichier de transformation est omis, les deux bases de données sont comparées uniquement.

pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md). pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows hôte de Script, consultez [Windows Installer outils de développement](windows-installer-development-tools.md).

Notez qu' [un exemple de localisation](a-localization-example.md) illustre la [génération d’une transformation de personnalisation](generating-a-customization-transform.md).

 

 



