---
description: Vous pouvez générer un fichier de transformation à l’aide de MsiDatabaseGenerateTransform ou de la méthode GenerateTransform de l’objet de base de données.
ms.assetid: c016fcba-0d54-4b99-bcdd-36967b2c9da0
title: Génération d’une transformation de personnalisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f73609b7be60dbfe236d31ed5a865e86ff6e310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534345"
---
# <a name="generating-a-customization-transform"></a><span data-ttu-id="da196-103">Génération d’une transformation de personnalisation</span><span class="sxs-lookup"><span data-stu-id="da196-103">Generating a Customization Transform</span></span>

<span data-ttu-id="da196-104">Vous pouvez générer un fichier de transformation à l’aide de [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma) ou de la [**méthode GenerateTransform**](database-generatetransform.md) de l' [**objet de base de données**](database-object.md).</span><span class="sxs-lookup"><span data-stu-id="da196-104">You may generate a transform file by using [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma) or the [**GenerateTransform method**](database-generatetransform.md) of the [**Database object**](database-object.md).</span></span> <span data-ttu-id="da196-105">Un exemple est fourni dans le kit de développement logiciel (SDK) Windows Installer, car l’utilitaire WiGenXfm.vbs.</span><span class="sxs-lookup"><span data-stu-id="da196-105">An example of this is provided in the Windows Installer SDK as the utility WiGenXfm.vbs.</span></span> <span data-ttu-id="da196-106">L’extrait de code suivant, Gen.vbs, illustre également la méthode **GenerateTransform** et est destiné à être utilisé avec Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="da196-106">The following snippet, Gen.vbs, also illustrates the **GenerateTransform** method and is for use with Windows Script Host.</span></span>


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



<span data-ttu-id="da196-107">Pour générer le fichier de transformation MNPtrans. MST à partir de la base de données d’origine MNP2000.msi et de la base de données MNP2000t.msi que vous avez modifiée dans [Personnalisation d’une base de données d’origine](customizing-an-original-database.md), accédez au dossier contenant Gen.vbs, à la base de données d’origine et à la base de données du programme d’installation mise à jour, puis entrez la ligne de commande suivante.</span><span class="sxs-lookup"><span data-stu-id="da196-107">To generate the transform file MNPtrans.mst from the original MNP2000.msi database and the MNP2000t.msi database you modified in [Customizing an Original Database](customizing-an-original-database.md), change directories to the folder containing Gen.vbs, the original database, and the updated installer database and enter the following command line.</span></span>

<span data-ttu-id="da196-108">**Cscript.exe Gen.vbs MNP2000.msi MNP2000t.msi MNPtrans. MST**</span><span class="sxs-lookup"><span data-stu-id="da196-108">**Cscript.exe Gen.vbs MNP2000.msi MNP2000t.msi MNPtrans.mst**</span></span>

[<span data-ttu-id="da196-109">Continuer</span><span class="sxs-lookup"><span data-stu-id="da196-109">Continue</span></span>](adding-summary-information-to-customization-transform.md)

 

 



