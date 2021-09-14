---
description: les composants SDK Windows pour les Windows Installer developers contiennent des fichiers VBScript qui vous montrent comment l’interface d’automatisation Windows Installer est utilisée pour modifier des packages Windows Installer.
ms.assetid: 93747a8d-32e0-4f31-a5cf-f95fb26b97df
title: Windows Exemples de scripts d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c2ad75411201cdbf74ef3aa035906d7e58aa7b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009558"
---
# <a name="windows-installer-scripting-examples"></a>Windows Exemples de scripts d’installation

les [composants SDK Windows pour les Windows Installer developers contiennent des](platform-sdk-components-for-windows-installer-developers.md) fichiers VBScript qui vous montrent comment l’interface d’automatisation Windows Installer est utilisée pour modifier des packages Windows Installer.

Les exemples de scripts identifiés dans cette rubrique ne sont pas pris en charge par Microsoft Corporation, et ne sont fournis qu’en tant que référence potentiellement utile. pour exécuter ces exemples, vous devez disposer de l’hôte de Script Windows. pour plus d’informations sur Windows script host, consultez la section [Windows script host](/previous-versions//9bbdkx3k(v=vs.85)) du kit de développement logiciel (SDK) de Microsoft Windows.



| Exemple de fichier de script | Description                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------|
| WiLstPrd.vbs       | [Répertorier les produits, les propriétés, les fonctionnalités et les composants](list-products-properties-features-and-components.md) |
| WiImport.vbs       | [Importer des fichiers](import-files.md)                                                                            |
| WiExport.vbs       | [Exporter des fichiers](export-files.md)                                                                            |
| WiSubStg.vbs       | [Gérer les sous-stockages](manage-substorages.md)                                                                |
| WiStream.vbs       | [Gérer les Flux binaires](manage-binary-streams.md)                                                          |
| WiMerge.vbs        | [Fusionner deux bases de données](merge-two-databases.md)                                                              |
| WiGenXfm.vbs       | [Générer une transformation](generate-a-transform.md)                                                            |
| WiUseXfm.vbs       | [Appliquer une transformation](apply-a-transform.md)                                                                  |
| WiLstXfm.vbs       | [Afficher une transformation](view-a-transform.md) (cscript uniquement)                                                     |
| WiDiffDb.vbs       | [Afficher les différences entre deux bases de données](view-differences-between-two-databases.md) (cscript uniquement)         |
| WiLstScr.vbs       | [Afficher le script du programme d’installation](view-installer-script.md) (cscript uniquement)                                           |
| WiSumInf.vbs       | [Gérer les informations récapitulatives](manage-summary-information.md)                                                |
| WiPolicy.vbs       | [Gérer des paramètres de stratégie](manage-policy-settings.md)                                                        |
| WiLangId.vbs       | [Gérer la langue et la page de codes](manage-language-and-codepage.md)                                            |
| WiToAnsi.vbs       | [Copier un fichier Unicode dans un fichier ANSI](copy-a-unicode-file-to-an-ansi-file.md)                              |
| WiFilVer.vbs       | [Gérer les tailles et les versions des fichiers](manage-file-sizes-and-versions.md)                                        |
| WiMakCab.vbs       | [Générer un fichier CAB](generate-file-cabinet.md)                                                          |
| WiRunSQL.vbs       | [exécuter des instructions SQL](execute-sql-statements.md)                                                        |
| WiTextIn.vbs       | [Copier le fichier ANSI dans un champ de base de données](copy-ansi-file-into-a-database-field.md)                            |
| WiCompon.vbs       | [Répertorier les composants](list-components.md)                                                                      |
| WiFeatur.vbs       | [Répertorier les fonctionnalités](list-features.md)                                                                          |
| WiDialog.vbs       | [Aperçu de l’interface utilisateur](preview-user-interface.md)                                                        |



 

Tous ces scripts affichent un écran d’aide qui décrit leurs arguments de ligne de commande. pour afficher l’écran d’aide dans Windows double-cliquez sur le fichier. Pour afficher l’écran d’aide à partir d’une ligne de commande, entrez un ? comme premier argument, ou entrez moins d’arguments que nécessaire. Les scripts retournent la valeur 0 en cas de réussite, la valeur 1 si l’aide est appelée et la valeur 2 en cas d’échec.

ces exemples requièrent Windows Script Host pour s’exécuter. Windows Script Host est en fait deux hôtes :

-   CScript.exe est la version qui vous permet d’exécuter des scripts à partir de l’invite de commandes et fournit des commutateurs de ligne de commande pour définir les propriétés de script.
-   WScript.exe est la version de Windows hôte de Script qui vous permet d’exécuter des scripts à partir de Windows. pour plus d’informations, consultez la section [Windows Script Host](/previous-versions//9bbdkx3k(v=vs.85)) dans le SDK Windows.

l’utilitaire de Makecab.exe est fourni avec les exemples de correctifs dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

pour plus d’informations sur wmi, consultez [utilisation de Windows Installer avec wmi](using-windows-installer-with-wmi.md).

 

 
