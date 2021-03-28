---
description: Montre comment utiliser les méthodes de l’interface IFileOperationProgressSink pour analyser les détails des actions de l’interface IFileOperation.
title: Récepteur de progression d’opération sur les fichiers
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 196ABB75-1FE0-44f5-9060-59AAB4231567
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 60e3bde90da36a6122608b463b28df670f0d2a8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034677"
---
# <a name="file-operation-progress-sink"></a><span data-ttu-id="92d9e-103">Récepteur de progression d’opération sur les fichiers</span><span class="sxs-lookup"><span data-stu-id="92d9e-103">File Operation Progress Sink</span></span>

<span data-ttu-id="92d9e-104">Montre comment utiliser les méthodes de l’interface [**IFileOperationProgressSink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) pour analyser les détails des actions de l’interface [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) .</span><span class="sxs-lookup"><span data-stu-id="92d9e-104">Demonstrates how to use the [**IFileOperationProgressSink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) interface methods for monitoring the details of [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) interface actions.</span></span>

<span data-ttu-id="92d9e-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="92d9e-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="92d9e-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92d9e-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="92d9e-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="92d9e-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="92d9e-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="92d9e-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="92d9e-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="92d9e-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="92d9e-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="92d9e-110">Requirements</span></span>



| <span data-ttu-id="92d9e-111">Produit</span><span class="sxs-lookup"><span data-stu-id="92d9e-111">Product</span></span>                                | <span data-ttu-id="92d9e-112">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="92d9e-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="92d9e-113">Windows</span><span class="sxs-lookup"><span data-stu-id="92d9e-113">Windows</span></span>                                | <span data-ttu-id="92d9e-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92d9e-114">Windows Vista</span></span>           |
| <span data-ttu-id="92d9e-115">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="92d9e-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="92d9e-116">6.1</span><span class="sxs-lookup"><span data-stu-id="92d9e-116">6.1</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="92d9e-117">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="92d9e-117">Downloading the Sample</span></span>

| <span data-ttu-id="92d9e-118">Emplacement</span><span class="sxs-lookup"><span data-stu-id="92d9e-118">Location</span></span>      | <span data-ttu-id="92d9e-119">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="92d9e-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92d9e-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="92d9e-120">GitHub</span></span>  | [<span data-ttu-id="92d9e-121">Exemple FileOperationProgressSink</span><span class="sxs-lookup"><span data-stu-id="92d9e-121">FileOperationProgressSink sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/FileOperationProgressSink) |

## <a name="building-the-sample"></a><span data-ttu-id="92d9e-122">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="92d9e-122">Building the Sample</span></span>

<span data-ttu-id="92d9e-123">Pour générer l’exemple à partir de la fenêtre d’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="92d9e-123">To build the sample from the command prompt window:</span></span>

1.  <span data-ttu-id="92d9e-124">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **FileOperationProgressSink** .</span><span class="sxs-lookup"><span data-stu-id="92d9e-124">Open the command prompt window and navigate to the **FileOperationProgressSink** project directory.</span></span>
2.  <span data-ttu-id="92d9e-125">Entrez `msbuild FileOperationProgressSinkSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="92d9e-125">Enter `msbuild FileOperationProgressSinkSample.sln`.</span></span>

<span data-ttu-id="92d9e-126">Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :</span><span class="sxs-lookup"><span data-stu-id="92d9e-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="92d9e-127">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **FilesInUse** .</span><span class="sxs-lookup"><span data-stu-id="92d9e-127">Open Windows Explorer and navigate to the **FilesInUse** project directory.</span></span> <span data-ttu-id="92d9e-128">Par exemple, le chemin d’installation complet par défaut est `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample` .</span><span class="sxs-lookup"><span data-stu-id="92d9e-128">For example, the full default installation path is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample`.</span></span>
2.  <span data-ttu-id="92d9e-129">Double-cliquez sur l’icône du fichier FileOperationProgressSinkSample. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="92d9e-129">Double-click the icon for the FileOperationProgressSinkSample.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="92d9e-130">L’extension de nom de fichier. sln n’est pas affichée sous paramètres de dossier par défaut.</span><span class="sxs-lookup"><span data-stu-id="92d9e-130">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="92d9e-131">Dans ce cas, il peut être identifié par son icône unique ou par sa description de type, « Microsoft Visual Studio solution ».</span><span class="sxs-lookup"><span data-stu-id="92d9e-131">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="92d9e-132">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="92d9e-132">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="92d9e-133">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="92d9e-133">Running the Sample</span></span>

1.  <span data-ttu-id="92d9e-134">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="92d9e-134">Navigate to the directory that contains the new executable, using the command prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="92d9e-135">À l’invite de commandes, entrez `FileOperationProgressSinkSample.exe` , ou à partir de l’Explorateur Windows, double-cliquez sur l’icône de FileOperationProgressSinkSample.exe.</span><span class="sxs-lookup"><span data-stu-id="92d9e-135">At the command prompt, enter `FileOperationProgressSinkSample.exe`, or from Windows Explorer, double-click the icon for FileOperationProgressSinkSample.exe.</span></span>

 

 



