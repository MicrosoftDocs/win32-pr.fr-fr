---
description: Pour appliquer la transformation de personnalisation lors de l’installation du produit, vous devez ajouter un flux d’informations de synthèse au fichier de transformation MNPtrans. MST généré lors de la génération d’une transformation de personnalisation.
ms.assetid: 586f6c43-7449-4d06-9201-9b4b4919871e
title: Ajout d’informations de résumé à la transformation de personnalisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64957fcf8f29ab8793517015c7018292ba9a6e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524178"
---
# <a name="adding-summary-information-to-customization-transform"></a><span data-ttu-id="0e13f-103">Ajout d’informations de résumé à la transformation de personnalisation</span><span class="sxs-lookup"><span data-stu-id="0e13f-103">Adding Summary Information to Customization Transform</span></span>

<span data-ttu-id="0e13f-104">Pour appliquer la transformation de personnalisation lors de l’installation du produit, vous devez ajouter un [flux d’informations de synthèse](summary-information-stream.md) au fichier de transformation MNPtrans. MST généré lors de la [génération d’une transformation de personnalisation](generating-a-customization-transform.md).</span><span class="sxs-lookup"><span data-stu-id="0e13f-104">To apply the customization transform during an installation of the product, you must add a [Summary Information Stream](summary-information-stream.md) to the transform file MNPtrans.mst generated in [Generating a Customization Transform](generating-a-customization-transform.md).</span></span>

<span data-ttu-id="0e13f-105">Vous pouvez générer des informations de synthèse pour une transformation à l’aide de [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) ou de la [**méthode CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md).</span><span class="sxs-lookup"><span data-stu-id="0e13f-105">You may generate summary information for a transform using [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) or the [**CreateTransformSummaryInfo Method**](database-createtransformsummaryinfo.md).</span></span> <span data-ttu-id="0e13f-106">L’extrait de code suivant, Sum.vbs, illustre la [**méthode CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) et est destiné à être utilisé avec Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="0e13f-106">The following snippet, Sum.vbs, illustrates the [**CreateTransformSummaryInfo Method**](database-createtransformsummaryinfo.md) and is for use with Windows Script Host.</span></span> <span data-ttu-id="0e13f-107">Notez que cet exemple n’effectue aucune validation et ne supprime aucune condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0e13f-107">Note that this example performs no validation and suppresses no error conditions.</span></span>


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



<span data-ttu-id="0e13f-108">Pour créer et ajouter des informations de synthèse au fichier de transformation MNPtrans. MST que vous avez créé lors de la [génération d’une transformation de personnalisation](generating-a-customization-transform.md), modifiez les répertoires dans le dossier contenant Gen.vbs, la base de données d’origine, la base de données mise à jour et la transformation, puis entrez la ligne de commande suivante.</span><span class="sxs-lookup"><span data-stu-id="0e13f-108">To create and add summary information to the transform file MNPtrans.mst you created in [Generating a Customization Transform](generating-a-customization-transform.md), change directories to the folder containing Gen.vbs, the original database, the updated database, and the transform, and enter the following command line.</span></span>

<span data-ttu-id="0e13f-109">**Cscript.exe Sum.vbs MNP2000.msi MNP2000t.msi MNPtrans. MST**</span><span class="sxs-lookup"><span data-stu-id="0e13f-109">**Cscript.exe Sum.vbs MNP2000.msi MNP2000t.msi MNPtrans.mst**</span></span>

<span data-ttu-id="0e13f-110">Cliquez sur l’icône MNP2000.msi pour lancer une installation ou utilisez la ligne de commande suivante.</span><span class="sxs-lookup"><span data-stu-id="0e13f-110">Click the MNP2000.msi icon to launch an install or use the following command line.</span></span>

<span data-ttu-id="0e13f-111">**msiexec/i MNP2000.msi**</span><span class="sxs-lookup"><span data-stu-id="0e13f-111">**msiexec /i MNP2000.msi**</span></span>

<span data-ttu-id="0e13f-112">Cela installe le produit sans les personnalisations.</span><span class="sxs-lookup"><span data-stu-id="0e13f-112">This installs the product without the customizations.</span></span> <span data-ttu-id="0e13f-113">Pour effectuer l’installation avec la personnalisation, entrez la ligne de commande suivante.</span><span class="sxs-lookup"><span data-stu-id="0e13f-113">To install with the customization, enter the following command line.</span></span> <span data-ttu-id="0e13f-114">Notez que la valeur de la propriété [**TRANSformations**](transforms.md) fait référence au fichier de transformation situé à la source.</span><span class="sxs-lookup"><span data-stu-id="0e13f-114">Note that the value of the [**TRANSFORMS**](transforms.md) Property refers to transform file located at the source.</span></span>

<span data-ttu-id="0e13f-115">**msiexec/i MNP2000.msi transformations = MNPtrans. MST**</span><span class="sxs-lookup"><span data-stu-id="0e13f-115">**msiexec /i MNP2000.msi TRANSFORMS=MNPtrans.mst**</span></span>

<span data-ttu-id="0e13f-116">La fonctionnalité porte n’apparaît pas dans l’arborescence de sélection des fonctionnalités et les composants de la fonctionnalité porte ne sont pas installés même si un type complet d’installation est sélectionné dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0e13f-116">The Gate feature does not appear in the feature selection tree and the components of the Gate feature are not installed even if a Complete type of installation is selected in the user interface.</span></span>

[<span data-ttu-id="0e13f-117">Continuer</span><span class="sxs-lookup"><span data-stu-id="0e13f-117">Continue</span></span>](embedding-customization-transforms-as-substorage.md)

 

 



