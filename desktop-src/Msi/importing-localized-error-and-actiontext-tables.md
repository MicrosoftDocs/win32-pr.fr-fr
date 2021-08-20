---
description: les versions localisées de la table d’erreurs et de la table ActionText sont fournies par le kit de développement logiciel (SDK) Windows Installer. les versions en anglais de ces tables, Error. fra et ActionTe. fra, se trouvent dans le dossier Intl du kit de développement logiciel (SDK) Windows Installer.
ms.assetid: 8de687c8-c7da-497e-8a90-2404096ad100
title: Importation de tables Error et ActionText localisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda0916f634d986874cd17f9871fa602277b180e1ba436e9d9786fb061f3ac4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142234"
---
# <a name="importing-localized-error-and-actiontext-tables"></a>Importation de tables Error et ActionText localisées

les versions localisées de la [table d’erreurs](error-table.md) et de la [table ActionText](actiontext-table.md) sont fournies par le kit de développement logiciel (SDK) Windows Installer. les versions en anglais de ces tables, Error. fra et ActionTe. fra, se trouvent dans le dossier Intl du kit de développement logiciel (SDK) Windows Installer.

Vous pouvez utiliser l’éditeur de table Orca ou l’utilitaire Msidb.exe fourni avec le kit de développement logiciel (SDK) pour importer les versions françaises de ces tables dans la base de données.

un exemple d’utilisation de [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) et de la [**méthode d’importation**](database-import.md) de l' [**objet de base de données**](database-object.md) est fourni dans le kit de développement logiciel (SDK) Windows Installer en tant que WiImport.vbs de l’utilitaire. l’extrait de code suivant, Imp.vbs, illustre également l’utilisation de la méthode d’importation et est destiné à être utilisé avec Windows hôte de Script.


```VB
'Imp.vbs. Argument(0) is the original database. Argument(1) is the
'    path of the folder containing the file to be imported. Argument(2) is the name of the file to be imported.
'
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is imp.vbs [original database] [folder path] [import file]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Wscript.CreateObject("WindowsInstaller.Installer")
Dim databasePath : databasePath = Wscript.Arguments(0)
Dim folder : folder = Wscript.Arguments(1)
 
' Open database and process file
Dim database : Set database = installer.OpenDatabase(databasePath, 1)
Dim table : table = Wscript.Arguments(2)
database.Import folder, table 
 
' Commit database changes
database.Commit 'commit changes
Wscript.Quit 0
```



Pour importer et remplacer la table d’erreurs par Error. FRA, vous pouvez utiliser une ligne de commande telle que la suivante.

**Cscript Imp.vbs MNPFren.msi C : \\ Remarque : \_ Erreur du programme d’installation du \\ français. fra**

Pour importer et remplacer la table ActionText par ActionTe. FRA, vous pouvez utiliser une ligne de commande telle que la suivante.

**Cscript Imp.vbs MNPFren.msi C : \\ Note \_ installer \\ français ActionTe. fra**

Réexécutez la validation sur MNPFren.msi comme décrit dans [validation d’une mise à niveau d’installation](validating-an-installation-upgrade.md).

[Continuer](localizing-database-columns.md)

 

 



