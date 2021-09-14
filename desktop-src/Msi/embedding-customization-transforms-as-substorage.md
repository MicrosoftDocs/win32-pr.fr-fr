---
description: vous pouvez stocker la transformation de personnalisation dans un stockage du package Windows Installer pour garantir que la transformation est toujours disponible lorsque le package d’installation est disponible.
ms.assetid: d4c022d2-a8c4-4b4e-8a6c-b14e1bc6effe
title: Incorporation de transformations de personnalisation en tant que sous-stockage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd275d36b37b2e29ae166a2a464a62495d2ca9c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091418"
---
# <a name="embedding-customization-transforms-as-substorage"></a>Incorporation de transformations de personnalisation en tant que sous-stockage

vous pouvez stocker la transformation de personnalisation dans un stockage du package Windows Installer pour garantir que la transformation est toujours disponible lorsque le package d’installation est disponible. Consultez [transformations incorporées](embedded-transforms.md). un exemple est fourni dans le kit de développement logiciel (SDK) Windows Installer, car l’utilitaire WiSubStg.vbs. l’extrait de code suivant, Emb.vbs, illustre également l’utilisation de la [table storages](-storages-table.md) pour ajouter une transformation incorporée et est destinée à être utilisée avec Windows Script Host.


```VB
'Emb.vbs. Argument(0) is the original database. Argument(1) is the
'    path to the transform file. Argument(2) is the name of the storage.
'
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
 WScript.Echo "Usage is emb.vbs [original database] [transform] [storage name]"
 WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer")
 
' Evaluate command-line arguments and set open and update modes
Dim databasePath: databasePath = Wscript.Arguments(0)
Dim importPath  : importPath = Wscript.Arguments(1)
Dim storageName : storageName = Wscript.Arguments(2)
 
' Open database and create a view on the _Storages table
Dim sqlQuery : sqlQuery = "SELECT `Name`,`Data` FROM _Storages"
Dim database : Set database = installer.OpenDatabase(databasePath, 1)
Dim view     : Set view = database.OpenView(sqlQuery)
 
'Create and Insert the row.
Dim record   : Set record = installer.CreateRecord(2)
record.StringData(1) = storageName
view.Execute record
 
'Insert storage - copy data into stream
record.SetStream 2, importPath
view.Modify 3, record
database.Commit
Set view = Nothing
Set database = Nothing
```



Pour ajouter un stockage nommé MNPtrans1 à MNP2000.msi et contenant la transformation que vous avez créée lors de l' [Ajout d’informations de résumé à la transformation de personnalisation](adding-summary-information-to-customization-transform.md), modifiez les répertoires dans le dossier contenant Emb.vbs, la base de données d’origine et le fichier de transformation, puis entrez la ligne de commande suivante.

**Cscript.exe Emb.vbs MNP2000.msi MNPtrans. MST MNPtrans1**

Cela termine l’exemple de transformation de personnalisation. Une fois la transformation incorporée dans MNPtrans. MST, la transformation est toujours disponible avec le package d’installation. Le fichier MNPtrans. MST n’a pas besoin d’être localisé à la source pour appliquer la transformation.

Supprimez MNPtrans. MST du dossier contenant l’exemple de package d’installation. Cliquez sur l’icône MNP2000.msi pour lancer une installation ou utilisez la ligne de commande suivante.

**msiexec/i MNP2000.msi**

Notez que cette procédure installe le produit sans les personnalisations. Pour effectuer l’installation avec les personnalisations, entrez la ligne de commande suivante. Utilisez un signe deux-points pour indiquer que la valeur de la propriété [**TRANSformations**](transforms.md) fait référence à une transformation incorporée.

msiexec/i MNP2000.msi transformations = : MNPtrans1

Notez que la fonctionnalité de porte n’apparaît pas dans l’arborescence de sélection des fonctionnalités et que les composants de la fonctionnalité de porte ne sont pas installés même si un type complet d’installation est sélectionné dans l’interface utilisateur.

## <a name="next-example"></a>Exemple suivant

[Exemple de mise à jour corrective de petite taille](a-small-update-patching-example.md)

 

 



