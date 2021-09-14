---
description: Vous pouvez générer un fichier de transformation à l’aide de MsiDatabaseGenerateTransform ou de la méthode GenerateTransform de l’objet de base de données.
ms.assetid: c016fcba-0d54-4b99-bcdd-36967b2c9da0
title: Génération d’une transformation de personnalisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f73609b7be60dbfe236d31ed5a865e86ff6e310
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021692"
---
# <a name="generating-a-customization-transform"></a>Génération d’une transformation de personnalisation

Vous pouvez générer un fichier de transformation à l’aide de [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma) ou de la [**méthode GenerateTransform**](database-generatetransform.md) de l' [**objet de base de données**](database-object.md). un exemple est fourni dans le kit de développement logiciel (SDK) Windows Installer, car l’utilitaire WiGenXfm.vbs. l’extrait de code suivant, Gen.vbs, illustre également la méthode **GenerateTransform** et est destiné à être utilisé avec Windows hôte de Script.


```VB
'Gen.vbs. Argument(0) is the original database. Argument(1) is the
'    customized database. Argument(2) is the transform file.
 
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is gen.vbs [original database] [customized database] [transform file]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer") 
' Open databases
Dim database1 : Set database1 = 
    installer.OpenDatabase(Wscript.Arguments(0), 0) 
Dim database2 : Set database2 = 
    installer.OpenDatabase(Wscript.Arguments(1), 0) 
' Generate transform
Dim transform : transform = Database2.GenerateTransform(Database1,
    Wscript.Arguments(2))
```



Pour générer le fichier de transformation MNPtrans. MST à partir de la base de données d’origine MNP2000.msi et de la base de données MNP2000t.msi que vous avez modifiée dans [Personnalisation d’une base de données d’origine](customizing-an-original-database.md), accédez au dossier contenant Gen.vbs, à la base de données d’origine et à la base de données du programme d’installation mise à jour, puis entrez la ligne de commande suivante.

**Cscript.exe Gen.vbs MNP2000.msi MNP2000t.msi MNPtrans. MST**

[Continuer](adding-summary-information-to-customization-transform.md)

 

 



