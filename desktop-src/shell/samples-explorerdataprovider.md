---
description: Montre comment implémenter une extension d’espace de noms Shell, y compris le comportement de menu contextuel et des tâches personnalisées dans le navigateur.
title: Fournisseur de données de l’Explorateur, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B1B20AF8-3DDE-467b-A49E-A77849CF9F1B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6bd15cbef62ff69efcccd28fcb625fc1432fdf89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210310"
---
# <a name="explorer-data-provider-sample"></a><span data-ttu-id="6db2f-103">Fournisseur de données de l’Explorateur, exemple</span><span class="sxs-lookup"><span data-stu-id="6db2f-103">Explorer Data Provider Sample</span></span>

<span data-ttu-id="6db2f-104">Montre comment implémenter une extension d’espace de noms Shell, y compris le comportement de menu contextuel et des tâches personnalisées dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="6db2f-104">Demonstrates how to implement a Shell namespace extension, including context menu behavior and custom tasks in the browser.</span></span>

<span data-ttu-id="6db2f-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="6db2f-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6db2f-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6db2f-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="6db2f-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="6db2f-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="6db2f-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="6db2f-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="6db2f-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="6db2f-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="6db2f-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6db2f-110">Requirements</span></span>



| <span data-ttu-id="6db2f-111">Produit</span><span class="sxs-lookup"><span data-stu-id="6db2f-111">Product</span></span>                                | <span data-ttu-id="6db2f-112">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="6db2f-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="6db2f-113">Windows</span><span class="sxs-lookup"><span data-stu-id="6db2f-113">Windows</span></span>                                | <span data-ttu-id="6db2f-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6db2f-114">Windows Vista</span></span>           |
| <span data-ttu-id="6db2f-115">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="6db2f-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="6db2f-116">6.1</span><span class="sxs-lookup"><span data-stu-id="6db2f-116">6.1</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="6db2f-117">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="6db2f-117">Downloading the Sample</span></span>

| <span data-ttu-id="6db2f-118">Emplacement</span><span class="sxs-lookup"><span data-stu-id="6db2f-118">Location</span></span>      | <span data-ttu-id="6db2f-119">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="6db2f-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6db2f-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="6db2f-120">GitHub</span></span>  | [<span data-ttu-id="6db2f-121">Exemple ExplorerDataProvider</span><span class="sxs-lookup"><span data-stu-id="6db2f-121">ExplorerDataProvider sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/explorerdataprovider) |

## <a name="building-the-sample"></a><span data-ttu-id="6db2f-122">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="6db2f-122">Building the Sample</span></span>

<span data-ttu-id="6db2f-123">Pour générer l’exemple à partir de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="6db2f-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="6db2f-124">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **ExplorerDataProvider** .</span><span class="sxs-lookup"><span data-stu-id="6db2f-124">Open the command prompt window and navigate to the **ExplorerDataProvider** project directory.</span></span>
2.  <span data-ttu-id="6db2f-125">Entrez `msbuild ExplorerDataProvider.sln`.</span><span class="sxs-lookup"><span data-stu-id="6db2f-125">Enter `msbuild ExplorerDataProvider.sln`.</span></span>

<span data-ttu-id="6db2f-126">Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :</span><span class="sxs-lookup"><span data-stu-id="6db2f-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="6db2f-127">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **ExplorerDataProvider** .</span><span class="sxs-lookup"><span data-stu-id="6db2f-127">Open Windows Explorer and navigate to the **ExplorerDataProvider** project directory.</span></span>
2.  <span data-ttu-id="6db2f-128">Double-cliquez sur l’icône du fichier ExplorerDataProvider. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6db2f-128">Double-click the icon for the ExplorerDataProvider.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="6db2f-129">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="6db2f-129">From the **Build** menu, select **Build Solution**.</span></span> <span data-ttu-id="6db2f-130">La DLL sera générée dans le répertoire de \\ débogage ou de version par défaut \\ .</span><span class="sxs-lookup"><span data-stu-id="6db2f-130">The DLL will be built in the default \\Debug or \\Release directory.</span></span>

> [!Note]  
> <span data-ttu-id="6db2f-131">Dans la version de cet exemple incluse dans le SDK Windows, la configuration de la version 64 bits n’inclut pas le fichier ExplorerDataProvider. def dans l’option de **fichier de définition de module** de l’éditeur de liens.</span><span class="sxs-lookup"><span data-stu-id="6db2f-131">In the version of this sample included in the Windows SDK, the configuration for the 64-bit Release build does not include the ExplorerDataProvider.def file in the linker's **Module Definition File** option.</span></span> <span data-ttu-id="6db2f-132">Vous devez spécifier ce fichier vous-même avant de générer dans un environnement 64 bits.</span><span class="sxs-lookup"><span data-stu-id="6db2f-132">You must specify that file yourself before building in a 64-bit environment.</span></span> <span data-ttu-id="6db2f-133">Ajoutez la ligne `ModuleDefinitionFile="ExplorerDataProvider.def"` à la section VCLinkerTool (commence à la ligne 329) du fichier ExplorerDataProvider. vcproj comme indiqué ici :</span><span class="sxs-lookup"><span data-stu-id="6db2f-133">Add the line `ModuleDefinitionFile="ExplorerDataProvider.def"` to the VCLinkerTool section (begins at line 329) of the ExplorerDataProvider.vcproj file as shown here:</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>LinkIncremental=&quot;1&quot;
> AdditionalLibraryDirectories=&quot;&quot;c:\Program Files\Microsoft SDKs\Windows\v6.0\Lib\x64&quot;&quot;
> ModuleDefinitionFile=&quot;ExplorerDataProvider.def&quot;
> GenerateDebugInformation=&quot;true&quot;</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> <span data-ttu-id="6db2f-134">La version de cet exemple téléchargeable à partir de la Galerie de code a été corrigée pour ce problème et aucune action supplémentaire n’est requise de votre part.</span><span class="sxs-lookup"><span data-stu-id="6db2f-134">The version of this sample downloadable from Code Gallery has been corrected for this issue and no extra action is required on your part.</span></span>
>
>  
>
> ## <a name="running-the-sample"></a><span data-ttu-id="6db2f-135">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="6db2f-135">Running the Sample</span></span>
>
> 1.  <span data-ttu-id="6db2f-136">Accédez au répertoire qui contient le nouveau fichier. dll et. propDesc à l’aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="6db2f-136">Navigate to the directory that contains the new .dll and .propdesc file, using the command prompt or Windows Explorer.</span></span>
> 2.  <span data-ttu-id="6db2f-137">Sur la ligne de commande, tapez `regsvr32.exe` .</span><span class="sxs-lookup"><span data-stu-id="6db2f-137">At the command line, type `regsvr32.exe`.</span></span>
>     > [!Note]  
>     > <span data-ttu-id="6db2f-138">Si vous exécutez cette commande à partir d’une invite de commandes avec élévation de privilèges, l’inscription automatique inscrira également le fichier. propDesc automatiquement.</span><span class="sxs-lookup"><span data-stu-id="6db2f-138">If you run this command from an elevated command prompt, the self-registration will also register the .propdesc file automatically.</span></span> <span data-ttu-id="6db2f-139">S’il est exécuté à partir d’une invite de commandes non élevée, l’extension de l’espace de noms fonctionne, mais sans fonctionnalité de propriété personnalisée.</span><span class="sxs-lookup"><span data-stu-id="6db2f-139">If it is run from a non-elevated command prompt then the namespace extension will work, but without custom property functionality.</span></span>
>
>      
>
> 3.  <span data-ttu-id="6db2f-140">Ouvrez le dossier **poste de travail** et parcourez l’extension de l’espace de noms qui s’y trouve.</span><span class="sxs-lookup"><span data-stu-id="6db2f-140">Open the **My Computer** folder and browse the new namespace extension present there.</span></span>
>
>  
>
>  
>


