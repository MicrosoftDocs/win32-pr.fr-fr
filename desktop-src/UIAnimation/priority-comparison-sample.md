---
title: Exemple de comparaison de priorité
description: Montre comment utiliser l’animation Windows avec votre propre comparaison de priorité, à l’aide de Direct2D pour le rendu.
ms.assetid: aa09f8a7-1919-4a44-832f-be8b848d6a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bfcb20785d6a4c3c3384b85327a0e27d93c58d7
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/10/2020
ms.locfileid: "104101392"
---
# <a name="priority-comparison-sample"></a><span data-ttu-id="b6537-103">Exemple de comparaison de priorité</span><span class="sxs-lookup"><span data-stu-id="b6537-103">Priority Comparison Sample</span></span>

<span data-ttu-id="b6537-104">Montre comment utiliser l’animation Windows avec votre propre comparaison de priorité, à l’aide de Direct2D pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="b6537-104">Shows how to use Windows Animation with your own Priority Comparison, using Direct2D for rendering.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="b6537-105">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="b6537-105">Downloading the Sample</span></span>

<span data-ttu-id="b6537-106">Cet exemple est disponible aux emplacements suivants.</span><span class="sxs-lookup"><span data-stu-id="b6537-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="b6537-107">Emplacement</span><span class="sxs-lookup"><span data-stu-id="b6537-107">Location</span></span>                               | <span data-ttu-id="b6537-108">Chemin d’accès/URL</span><span class="sxs-lookup"><span data-stu-id="b6537-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6537-109">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="b6537-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="b6537-110">Kit de développement logiciel (SDK) Microsoft Windows 7,0</span><span class="sxs-lookup"><span data-stu-id="b6537-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="b6537-111">Galerie de code</span><span class="sxs-lookup"><span data-stu-id="b6537-111">Code Gallery</span></span>                           | [<span data-ttu-id="b6537-112">Exemple de code du gestionnaire d’animations Windows</span><span class="sxs-lookup"><span data-stu-id="b6537-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

<span data-ttu-id="b6537-113">Une fois que vous avez téléchargé et installé le SDK Windows, vous trouverez les exemples dans le répertoire d’installation.</span><span class="sxs-lookup"><span data-stu-id="b6537-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="b6537-114">Par exemple, si vous utilisez le chemin d’installation par défaut pour le SDK Windows pour Windows 7, les exemples sont installés dans C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples.</span><span class="sxs-lookup"><span data-stu-id="b6537-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="b6537-115">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="b6537-115">Building the Sample</span></span>

<span data-ttu-id="b6537-116">Utilisez l’une des méthodes suivantes pour générer l’exemple.</span><span class="sxs-lookup"><span data-stu-id="b6537-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="b6537-117">**Pour générer l’exemple à partir de l’invite de commandes**</span><span class="sxs-lookup"><span data-stu-id="b6537-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="b6537-118">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet PriorityComparison.</span><span class="sxs-lookup"><span data-stu-id="b6537-118">Open the Command Prompt window and navigate to the PriorityComparison project directory.</span></span> <span data-ttu-id="b6537-119">Par exemple, le chemin d’installation par défaut de cet exemple est C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ WindowsAnimation \\ PriorityComparison.</span><span class="sxs-lookup"><span data-stu-id="b6537-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\PriorityComparison.</span></span>

2.  <span data-ttu-id="b6537-120">Exécutez la commande suivante : **MSBuild PriorityComparison. sln**</span><span class="sxs-lookup"><span data-stu-id="b6537-120">Run the following command: **msbuild PriorityComparison.sln**</span></span>

<span data-ttu-id="b6537-121">**Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut)**</span><span class="sxs-lookup"><span data-stu-id="b6537-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="b6537-122">Ouvrez l’Explorateur Windows et accédez au répertoire du projet PriorityComparison.</span><span class="sxs-lookup"><span data-stu-id="b6537-122">Open Windows Explorer and navigate to the PriorityComparison project directory.</span></span>

2.  <span data-ttu-id="b6537-123">Double-cliquez sur l’icône du fichier PriorityComparison. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b6537-123">Double-click the icon for the PriorityComparison.sln file to open the project in Visual Studio.</span></span>

    > [!Note]  
    > <span data-ttu-id="b6537-124">L’extension de nom de fichier. sln n’est pas affichée sous paramètres de dossier par défaut.</span><span class="sxs-lookup"><span data-stu-id="b6537-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="b6537-125">Dans ce cas, il peut être identifié par son icône unique ou par sa description de type, « Microsoft Visual Studio solution ».</span><span class="sxs-lookup"><span data-stu-id="b6537-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="b6537-126">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="b6537-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="b6537-127">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="b6537-127">Running the Sample</span></span>

<span data-ttu-id="b6537-128">Pour exécuter l’exemple :</span><span class="sxs-lookup"><span data-stu-id="b6537-128">To run the sample:</span></span>

1.  <span data-ttu-id="b6537-129">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="b6537-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="b6537-130">Exécutez **PriorityComparison.exe** à partir de l’invite de commandes, ou double-cliquez sur l’icône de PriorityComparison.exe dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="b6537-130">Run **PriorityComparison.exe** at the command prompt, or double-click the icon for PriorityComparison.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="b6537-131">Les exemples d’images sont chargés à partir de la bibliothèque d’images.</span><span class="sxs-lookup"><span data-stu-id="b6537-131">Sample images are loaded from the Picture Library.</span></span> <span data-ttu-id="b6537-132">Redimensionnez la fenêtre ou appuyez sur la barre d’espace et les images seront déplacées au centre.</span><span class="sxs-lookup"><span data-stu-id="b6537-132">Resize the window or press the spacebar and the images will move to the center.</span></span>

4.  <span data-ttu-id="b6537-133">Utilisez les touches de direction gauche et droite pour sélectionner différentes images (plus la touche est rapide, plus la sélection sera rapide).</span><span class="sxs-lookup"><span data-stu-id="b6537-133">Use the left and right arrow keys to select different images (the faster the key is pressed the faster the selection will change).</span></span>

5.  <span data-ttu-id="b6537-134">Utilisez les touches de direction vers le haut et vers le bas pour créer une vague à travers les images (plus la touche est rapide, plus l’onde est rapide).</span><span class="sxs-lookup"><span data-stu-id="b6537-134">Use the up and down arrow keys to create a wave through the images (the faster the key is pressed, the faster the wave).</span></span>

 

 




