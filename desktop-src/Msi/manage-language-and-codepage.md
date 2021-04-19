---
description: Le WiLangID.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer.
ms.assetid: 319e9ffd-ff9f-4b4c-913e-2c571f2ec9ee
title: Gérer la langue et la page de codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbfb96f04d75ed79f32c8a49fe58b8dcc86f184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523432"
---
# <a name="manage-language-and-codepage"></a>Gérer la langue et la page de codes

Le WiLangID.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Cet exemple montre comment le script est utilisé pour accéder aux informations de langage et à la page de codes d’un package. Pour plus d’informations, consultez [localisation d’un Package Windows Installer](localizing-a-windows-installer-package.md) et [gestion des pages de codes (Windows Installer)](code-page-handling-windows-installer-.md).

L’exemple illustre l’utilisation de :

-   [**OpenDatabase, méthode (objet installer)**](installer-opendatabase.md)
-   [**Méthode CreateRecord**](installer-createrecord.md)
-   [**Méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [ **objet installer**](installer-object.md)
-   [**OpenView, méthode**](database-openview.md)
-   [**Propriété SummaryInformation (objet Database)**](database-summaryinformation.md) de l' [ **objet Database**](database-object.md)

L’utilisation de cet exemple nécessite la version CScript.exe ou WScript.exe de Windows Script Host. Pour utiliser CScript.exe pour exécuter cet exemple, tapez une commande à l’invite de commandes en utilisant la syntaxe suivante. L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant. Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.

**cscript WiLangID.vbs \[ chemin d’accès à la \] \[ valeur du mot clé de \] base de données \[\]**

Spécifiez le chemin d’accès à la base de données Windows Installer. Pour modifier une valeur, spécifiez l’un des mots clés suivants, suivi de la nouvelle valeur. Si aucune valeur n’est spécifiée, l’exemple retourne la valeur actuelle.



| Mot clé      | Description                                                                                                                                                                                |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Package**  | Versions de langage prises en charge par la base de données. Pour plus d’informations, consultez la propriété [**Résumé du modèle**](template-summary.md) .                                                               |
| **Produit**  | Langue que le programme d’installation doit utiliser pour toutes les chaînes de l’interface utilisateur qui ne sont pas créées dans la base de données. Pour plus d’informations, consultez propriété [**ProductLanguage**](productlanguage.md) . |
| **Codepage** | Page de codes ANSI unique pour le pool de chaînes. Pour plus d’informations, consultez [gestion des pages de codes (Windows Installer)](code-page-handling-windows-installer-.md).                                       |



 

Pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md). Pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows Script Host, consultez [Windows Installer outils de développement](windows-installer-development-tools.md).

Pour plus d’informations, consultez Détermination de la page de codes d’une [base de données d’installation](determining-an-installation-database-s-code-page.md) et [définition de la page de codes d’une base de données](setting-the-code-page-of-a-database.md).

 

 



