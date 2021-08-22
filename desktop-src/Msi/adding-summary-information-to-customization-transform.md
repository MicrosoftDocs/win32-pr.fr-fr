---
description: Pour appliquer la transformation de personnalisation lors de l’installation du produit, vous devez ajouter un flux d’informations de synthèse au fichier de transformation MNPtrans. MST généré lors de la génération d’une transformation de personnalisation.
ms.assetid: 586f6c43-7449-4d06-9201-9b4b4919871e
title: Ajout d’informations de résumé à la transformation de personnalisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ea4c9aa505d425bfd06fe5cac1f45666e794624618db14100ee5f517dd3048
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639469"
---
# <a name="adding-summary-information-to-customization-transform"></a>Ajout d’informations de résumé à la transformation de personnalisation

Pour appliquer la transformation de personnalisation lors de l’installation du produit, vous devez ajouter un [flux d’informations de synthèse](summary-information-stream.md) au fichier de transformation MNPtrans. MST généré lors de la [génération d’une transformation de personnalisation](generating-a-customization-transform.md).

Vous pouvez générer des informations de synthèse pour une transformation à l’aide de [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) ou de la [**méthode CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md). l’extrait de code suivant, Sum.vbs, illustre la [**méthode CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) et est destiné à être utilisé avec Windows hôte de Script. Notez que cet exemple n’effectue aucune validation et ne supprime aucune condition d’erreur.


```VB
'Sum.vbs. Argument(0) is the original database. Argument(1) is the
'    customized database. Argument(2) is the transform file.
 
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is sum.vbs [original database] [customized database] [transform]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer") 
 
' Open databases and transform 
Dim database1 : Set database1 =
    installer.OpenDatabase(Wscript.Arguments(0), 0) 
Dim database2 : Set database2 =
    installer.OpenDatabase(Wscript.Arguments(1), 0) 
Dim transform : transform = Wscript.Arguments(2)
 
' Create and add Summary Information
Dim transinfo : transinfo =
    Database2.CreateTransformSummaryInfo(Database1, transform,0,0)
```



Pour créer et ajouter des informations de synthèse au fichier de transformation MNPtrans. MST que vous avez créé lors de la [génération d’une transformation de personnalisation](generating-a-customization-transform.md), modifiez les répertoires dans le dossier contenant Gen.vbs, la base de données d’origine, la base de données mise à jour et la transformation, puis entrez la ligne de commande suivante.

**Cscript.exe Sum.vbs MNP2000.msi MNP2000t.msi MNPtrans. MST**

Cliquez sur l’icône MNP2000.msi pour lancer une installation ou utilisez la ligne de commande suivante.

**msiexec/i MNP2000.msi**

Cela installe le produit sans les personnalisations. Pour effectuer l’installation avec la personnalisation, entrez la ligne de commande suivante. Notez que la valeur de la propriété [**TRANSformations**](transforms.md) fait référence au fichier de transformation situé à la source.

**msiexec/i MNP2000.msi transformations = MNPtrans. MST**

La fonctionnalité porte n’apparaît pas dans l’arborescence de sélection des fonctionnalités et les composants de la fonctionnalité porte ne sont pas installés même si un type complet d’installation est sélectionné dans l’interface utilisateur.

[Continuer](embedding-customization-transforms-as-substorage.md)

 

 



