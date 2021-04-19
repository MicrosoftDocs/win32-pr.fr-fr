---
description: Vous pouvez stocker la transformation de personnalisation dans un stockage du package Windows Installer pour garantir que la transformation est toujours disponible lorsque le package d’installation est disponible.
ms.assetid: d4c022d2-a8c4-4b4e-8a6c-b14e1bc6effe
title: Incorporation de transformations de personnalisation en tant que sous-stockage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd275d36b37b2e29ae166a2a464a62495d2ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519941"
---
# <a name="embedding-customization-transforms-as-substorage"></a><span data-ttu-id="b4487-103">Incorporation de transformations de personnalisation en tant que sous-stockage</span><span class="sxs-lookup"><span data-stu-id="b4487-103">Embedding Customization Transforms as Substorage</span></span>

<span data-ttu-id="b4487-104">Vous pouvez stocker la transformation de personnalisation dans un stockage du package Windows Installer pour garantir que la transformation est toujours disponible lorsque le package d’installation est disponible.</span><span class="sxs-lookup"><span data-stu-id="b4487-104">You may store the customization transform in a storage of the Windows Installer package to guarantee that the transform is always available when the installation package is available.</span></span> <span data-ttu-id="b4487-105">Consultez [transformations incorporées](embedded-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="b4487-105">See [Embedded Transforms](embedded-transforms.md).</span></span> <span data-ttu-id="b4487-106">Un exemple est fourni dans le kit de développement logiciel (SDK) Windows Installer, car l’utilitaire WiSubStg.vbs.</span><span class="sxs-lookup"><span data-stu-id="b4487-106">An example of this is provided in the Windows Installer SDK as the utility WiSubStg.vbs.</span></span> <span data-ttu-id="b4487-107">L’extrait de code suivant, Emb.vbs, illustre également l’utilisation de la [table storages](-storages-table.md) pour ajouter une transformation incorporée et est destinée à être utilisée avec Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="b4487-107">The following snippet, Emb.vbs, also illustrates the use of the [Storages table](-storages-table.md) to add an embedded transform and is for use with Windows Script Host.</span></span>


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



<span data-ttu-id="b4487-108">Pour ajouter un stockage nommé MNPtrans1 à MNP2000.msi et contenant la transformation que vous avez créée lors de l' [Ajout d’informations de résumé à la transformation de personnalisation](adding-summary-information-to-customization-transform.md), modifiez les répertoires dans le dossier contenant Emb.vbs, la base de données d’origine et le fichier de transformation, puis entrez la ligne de commande suivante.</span><span class="sxs-lookup"><span data-stu-id="b4487-108">To add a storage named MNPtrans1 to MNP2000.msi, and containing the transform you created in [Adding Summary Information to Customization Transform](adding-summary-information-to-customization-transform.md), change directories to the folder containing Emb.vbs, the original database, and the transform file, then enter the following command line.</span></span>

<span data-ttu-id="b4487-109">**Cscript.exe Emb.vbs MNP2000.msi MNPtrans. MST MNPtrans1**</span><span class="sxs-lookup"><span data-stu-id="b4487-109">**Cscript.exe Emb.vbs MNP2000.msi MNPtrans.mst MNPtrans1**</span></span>

<span data-ttu-id="b4487-110">Cela termine l’exemple de transformation de personnalisation.</span><span class="sxs-lookup"><span data-stu-id="b4487-110">This completes the customization transform example.</span></span> <span data-ttu-id="b4487-111">Une fois la transformation incorporée dans MNPtrans. MST, la transformation est toujours disponible avec le package d’installation.</span><span class="sxs-lookup"><span data-stu-id="b4487-111">After embedding the transform in MNPtrans.mst, the transform is always available with the installation package.</span></span> <span data-ttu-id="b4487-112">Le fichier MNPtrans. MST n’a pas besoin d’être localisé à la source pour appliquer la transformation.</span><span class="sxs-lookup"><span data-stu-id="b4487-112">The file MNPtrans.mst does not need to be located at the source to apply the transform.</span></span>

<span data-ttu-id="b4487-113">Supprimez MNPtrans. MST du dossier contenant l’exemple de package d’installation.</span><span class="sxs-lookup"><span data-stu-id="b4487-113">Remove MNPtrans.mst from the folder containing the sample installation package.</span></span> <span data-ttu-id="b4487-114">Cliquez sur l’icône MNP2000.msi pour lancer une installation ou utilisez la ligne de commande suivante.</span><span class="sxs-lookup"><span data-stu-id="b4487-114">Click the MNP2000.msi icon to launch an install or use the following command line.</span></span>

<span data-ttu-id="b4487-115">**msiexec/i MNP2000.msi**</span><span class="sxs-lookup"><span data-stu-id="b4487-115">**msiexec /i MNP2000.msi**</span></span>

<span data-ttu-id="b4487-116">Notez que cette procédure installe le produit sans les personnalisations.</span><span class="sxs-lookup"><span data-stu-id="b4487-116">Note that this installs the product without the customizations.</span></span> <span data-ttu-id="b4487-117">Pour effectuer l’installation avec les personnalisations, entrez la ligne de commande suivante.</span><span class="sxs-lookup"><span data-stu-id="b4487-117">To install with the customizations, enter the following command line.</span></span> <span data-ttu-id="b4487-118">Utilisez un signe deux-points pour indiquer que la valeur de la propriété [**TRANSformations**](transforms.md) fait référence à une transformation incorporée.</span><span class="sxs-lookup"><span data-stu-id="b4487-118">Use a colon to indicate that the value of the [**TRANSFORMS**](transforms.md) Property refers to an embedded transform.</span></span>

<span data-ttu-id="b4487-119">msiexec/i MNP2000.msi transformations = : MNPtrans1</span><span class="sxs-lookup"><span data-stu-id="b4487-119">msiexec /i MNP2000.msi TRANSFORMS=:MNPtrans1</span></span>

<span data-ttu-id="b4487-120">Notez que la fonctionnalité de porte n’apparaît pas dans l’arborescence de sélection des fonctionnalités et que les composants de la fonctionnalité de porte ne sont pas installés même si un type complet d’installation est sélectionné dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b4487-120">Note that the Gate feature does not appear in the feature selection tree and that the components of the Gate feature are not installed even if a Complete type of installation is selected in the user interface.</span></span>

## <a name="next-example"></a><span data-ttu-id="b4487-121">Exemple suivant</span><span class="sxs-lookup"><span data-stu-id="b4487-121">Next example</span></span>

[<span data-ttu-id="b4487-122">Exemple de mise à jour corrective de petite taille</span><span class="sxs-lookup"><span data-stu-id="b4487-122">A Small Update Patching Example</span></span>](a-small-update-patching-example.md)

 

 



