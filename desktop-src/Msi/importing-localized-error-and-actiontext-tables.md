---
description: Les versions localisées de la table d’erreurs et de la table ActionText sont fournies par le kit de développement logiciel (SDK) Windows Installer. Les versions en anglais de ces tables, Error. FRA et ActionTe. FRA, se trouvent dans le dossier Intl du kit de développement logiciel (SDK) Windows Installer.
ms.assetid: 8de687c8-c7da-497e-8a90-2404096ad100
title: Importation de tables Error et ActionText localisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d48a68ca1053a1a1c66899a17802ac337c3ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521837"
---
# <a name="importing-localized-error-and-actiontext-tables"></a><span data-ttu-id="89c35-104">Importation de tables Error et ActionText localisées</span><span class="sxs-lookup"><span data-stu-id="89c35-104">Importing Localized Error and ActionText Tables</span></span>

<span data-ttu-id="89c35-105">Les versions localisées de la [table d’erreurs](error-table.md) et de la [table ActionText](actiontext-table.md) sont fournies par le kit de développement logiciel (SDK) Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="89c35-105">Localized language versions of the [Error table](error-table.md) and [ActionText table](actiontext-table.md) are provided by the Windows Installer SDK.</span></span> <span data-ttu-id="89c35-106">Les versions en anglais de ces tables, Error. FRA et ActionTe. FRA, se trouvent dans le dossier Intl du kit de développement logiciel (SDK) Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="89c35-106">The French language versions of these tables, Error.FRA and ActionTe.FRA, are located in the Intl folder of the Windows Installer SDK.</span></span>

<span data-ttu-id="89c35-107">Vous pouvez utiliser l’éditeur de table Orca ou l’utilitaire Msidb.exe fourni avec le kit de développement logiciel (SDK) pour importer les versions françaises de ces tables dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="89c35-107">You may use the table editor Orca or the utility Msidb.exe provided with the SDK to import the French versions of these tables into the database.</span></span>

<span data-ttu-id="89c35-108">Un exemple d’utilisation de [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) et de la [**méthode d’importation**](database-import.md) de l' [**objet de base de données**](database-object.md) est fourni dans le kit de développement logiciel (SDK) Windows Installer en tant que WiImport.vbs de l’utilitaire.</span><span class="sxs-lookup"><span data-stu-id="89c35-108">An example of using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) and the [**Import Method**](database-import.md) of the [**Database object**](database-object.md) is provided in the Windows Installer SDK as the utility WiImport.vbs.</span></span> <span data-ttu-id="89c35-109">L’extrait de code suivant, Imp.vbs, illustre également l’utilisation de la méthode Import et est destiné à être utilisé avec Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="89c35-109">The following snippet, Imp.vbs, also illustrates the use of the Import method and is for use with Windows Script Host.</span></span>


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



<span data-ttu-id="89c35-110">Pour importer et remplacer la table d’erreurs par Error. FRA, vous pouvez utiliser une ligne de commande telle que la suivante.</span><span class="sxs-lookup"><span data-stu-id="89c35-110">To import and replace the Error table with Error.FRA you may use a command line such as the following.</span></span>

<span data-ttu-id="89c35-111">**Cscript Imp.vbs MNPFren.msi C : \\ Remarque : \_ Erreur du programme d’installation du \\ français. fra**</span><span class="sxs-lookup"><span data-stu-id="89c35-111">**Cscript Imp.vbs MNPFren.msi C:\\Note\_Installer\\French Error.FRA**</span></span>

<span data-ttu-id="89c35-112">Pour importer et remplacer la table ActionText par ActionTe. FRA, vous pouvez utiliser une ligne de commande telle que la suivante.</span><span class="sxs-lookup"><span data-stu-id="89c35-112">To import and replace the ActionText table with ActionTe.FRA you may use a command line such as the following.</span></span>

<span data-ttu-id="89c35-113">**Cscript Imp.vbs MNPFren.msi C : \\ Note \_ installer \\ français ActionTe. fra**</span><span class="sxs-lookup"><span data-stu-id="89c35-113">**Cscript Imp.vbs MNPFren.msi C:\\Note\_Installer\\French ActionTe.FRA**</span></span>

<span data-ttu-id="89c35-114">Réexécutez la validation sur MNPFren.msi comme décrit dans [validation d’une mise à niveau d’installation](validating-an-installation-upgrade.md).</span><span class="sxs-lookup"><span data-stu-id="89c35-114">Rerun validation on MNPFren.msi as described in [Validating an Installation Upgrade](validating-an-installation-upgrade.md).</span></span>

[<span data-ttu-id="89c35-115">Continuer</span><span class="sxs-lookup"><span data-stu-id="89c35-115">Continue</span></span>](localizing-database-columns.md)

 

 



