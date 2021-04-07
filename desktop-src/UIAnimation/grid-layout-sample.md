---
title: Exemple de disposition en grille
description: Montre comment utiliser l’animation Windows, à l’aide de Direct2D pour animer une grille d’images.
ms.assetid: f2f24058-c532-45ad-bde8-d05cfffcd505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4d691ffa6396e294fd2dfbd07eaf9329f19519
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/10/2020
ms.locfileid: "103724357"
---
# <a name="grid-layout-sample"></a><span data-ttu-id="9e66d-103">Exemple de disposition en grille</span><span class="sxs-lookup"><span data-stu-id="9e66d-103">Grid Layout Sample</span></span>

<span data-ttu-id="9e66d-104">Montre comment utiliser l’animation Windows, à l’aide de Direct2D pour animer une grille d’images.</span><span class="sxs-lookup"><span data-stu-id="9e66d-104">Shows how to use Windows Animation, using Direct2D to animate a grid of images.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="9e66d-105">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="9e66d-105">Downloading the Sample</span></span>

<span data-ttu-id="9e66d-106">Cet exemple est disponible aux emplacements suivants.</span><span class="sxs-lookup"><span data-stu-id="9e66d-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="9e66d-107">Emplacement</span><span class="sxs-lookup"><span data-stu-id="9e66d-107">Location</span></span>                               | <span data-ttu-id="9e66d-108">Chemin d’accès/URL</span><span class="sxs-lookup"><span data-stu-id="9e66d-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e66d-109">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="9e66d-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="9e66d-110">Kit de développement logiciel (SDK) Microsoft Windows 7,0</span><span class="sxs-lookup"><span data-stu-id="9e66d-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="9e66d-111">Galerie de code</span><span class="sxs-lookup"><span data-stu-id="9e66d-111">Code Gallery</span></span>                           | [<span data-ttu-id="9e66d-112">Exemple de code du gestionnaire d’animations Windows</span><span class="sxs-lookup"><span data-stu-id="9e66d-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

<span data-ttu-id="9e66d-113">Une fois que vous avez téléchargé et installé le SDK Windows, vous trouverez les exemples dans le répertoire d’installation.</span><span class="sxs-lookup"><span data-stu-id="9e66d-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="9e66d-114">Par exemple, si vous utilisez le chemin d’installation par défaut pour le SDK Windows pour Windows 7, les exemples sont installés dans C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples.</span><span class="sxs-lookup"><span data-stu-id="9e66d-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="9e66d-115">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="9e66d-115">Building the Sample</span></span>

<span data-ttu-id="9e66d-116">Utilisez l’une des méthodes suivantes pour générer l’exemple.</span><span class="sxs-lookup"><span data-stu-id="9e66d-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="9e66d-117">**Pour générer l’exemple à partir de l’invite de commandes**</span><span class="sxs-lookup"><span data-stu-id="9e66d-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="9e66d-118">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet GridLayout.</span><span class="sxs-lookup"><span data-stu-id="9e66d-118">Open the Command Prompt window and navigate to the GridLayout project directory.</span></span> <span data-ttu-id="9e66d-119">Par exemple, le chemin d’installation par défaut de cet exemple est C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ WindowsAnimation \\ GridLayout</span><span class="sxs-lookup"><span data-stu-id="9e66d-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\GridLayout</span></span>

2.  <span data-ttu-id="9e66d-120">Exécutez la commande suivante : **MSBuild GridLayout. sln**</span><span class="sxs-lookup"><span data-stu-id="9e66d-120">Run the following command: **msbuild GridLayout.sln**</span></span>

<span data-ttu-id="9e66d-121">**Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut)**</span><span class="sxs-lookup"><span data-stu-id="9e66d-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="9e66d-122">Ouvrez l’Explorateur Windows et accédez au répertoire du projet GridLayout.</span><span class="sxs-lookup"><span data-stu-id="9e66d-122">Open Windows Explorer and navigate to the GridLayout project directory.</span></span>

    > [!Note]  
    > <span data-ttu-id="9e66d-123">L’extension de nom de fichier. sln n’est pas affichée sous paramètres de dossier par défaut.</span><span class="sxs-lookup"><span data-stu-id="9e66d-123">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="9e66d-124">Dans ce cas, il peut être identifié par son icône unique ou par sa description de type, « Microsoft Visual Studio solution ».</span><span class="sxs-lookup"><span data-stu-id="9e66d-124">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

2.  <span data-ttu-id="9e66d-125">Double-cliquez sur l’icône du fichier GridLayout. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9e66d-125">Double-click the icon for the GridLayout.sln file to open the project in Visual Studio.</span></span>

3.  <span data-ttu-id="9e66d-126">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="9e66d-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="9e66d-127">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="9e66d-127">Running the Sample</span></span>

<span data-ttu-id="9e66d-128">Pour exécuter l’exemple :</span><span class="sxs-lookup"><span data-stu-id="9e66d-128">To run the sample:</span></span>

1.  <span data-ttu-id="9e66d-129">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="9e66d-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="9e66d-130">Exécutez **GridLayout.exe** à partir de l’invite de commandes, ou double-cliquez sur l’icône de GridLayout.exe dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="9e66d-130">Run **GridLayout.exe** at the command prompt, or double-click the icon for GridLayout.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="9e66d-131">Les exemples d’images sont chargés à partir de la bibliothèque d’images.</span><span class="sxs-lookup"><span data-stu-id="9e66d-131">Sample images are loaded from the Picture Library.</span></span> <span data-ttu-id="9e66d-132">Redimensionner la fenêtre et les images se réorganiser dans une grille.</span><span class="sxs-lookup"><span data-stu-id="9e66d-132">Resize the window and the images will arrange themselves into a grid.</span></span>

 

 




