---
title: Exemple d’interpolateur personnalisé
description: Montre comment utiliser l’animation Windows avec votre propre interpolateur personnalisé, avec Direct2D utilisé pour le rendu.
ms.assetid: 90c4a53a-5c5e-4dcc-8946-bc8f23a07ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833a1a2ef09d603eaefac90b2ae25b3f533ba307
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/10/2020
ms.locfileid: "104101393"
---
# <a name="custom-interpolator-sample"></a><span data-ttu-id="d7465-103">Exemple d’interpolateur personnalisé</span><span class="sxs-lookup"><span data-stu-id="d7465-103">Custom Interpolator Sample</span></span>

<span data-ttu-id="d7465-104">Montre comment utiliser l’animation Windows avec votre propre interpolateur personnalisé, avec Direct2D utilisé pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="d7465-104">Shows how to use Windows Animation with your own Custom Interpolator, with Direct2D used for rendering.</span></span> <span data-ttu-id="d7465-105">Les exemples d’images sont chargés à partir de la bibliothèque d’images.</span><span class="sxs-lookup"><span data-stu-id="d7465-105">Sample images are loaded from the Picture Library.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="d7465-106">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="d7465-106">Downloading the Sample</span></span>

<span data-ttu-id="d7465-107">Cet exemple est disponible aux emplacements suivants.</span><span class="sxs-lookup"><span data-stu-id="d7465-107">This sample is available in the following locations.</span></span>



| <span data-ttu-id="d7465-108">Emplacement</span><span class="sxs-lookup"><span data-stu-id="d7465-108">Location</span></span>                               | <span data-ttu-id="d7465-109">Chemin d’accès/URL</span><span class="sxs-lookup"><span data-stu-id="d7465-109">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7465-110">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="d7465-110">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="d7465-111">Kit de développement logiciel (SDK) Microsoft Windows 7,0</span><span class="sxs-lookup"><span data-stu-id="d7465-111">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="d7465-112">Galerie de code</span><span class="sxs-lookup"><span data-stu-id="d7465-112">Code Gallery</span></span>                           | [<span data-ttu-id="d7465-113">Exemple de code du gestionnaire d’animations Windows</span><span class="sxs-lookup"><span data-stu-id="d7465-113">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

<span data-ttu-id="d7465-114">Une fois que vous avez téléchargé et installé le SDK Windows, vous trouverez les exemples dans le répertoire d’installation.</span><span class="sxs-lookup"><span data-stu-id="d7465-114">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="d7465-115">Par exemple, si vous utilisez le chemin d’installation par défaut pour le SDK Windows pour Windows 7, les exemples sont installés dans C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples.</span><span class="sxs-lookup"><span data-stu-id="d7465-115">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="d7465-116">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="d7465-116">Building the Sample</span></span>

<span data-ttu-id="d7465-117">Utilisez l’une des méthodes suivantes pour générer l’exemple.</span><span class="sxs-lookup"><span data-stu-id="d7465-117">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="d7465-118">**Pour générer l’exemple à partir de l’invite de commandes**</span><span class="sxs-lookup"><span data-stu-id="d7465-118">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="d7465-119">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet CustomInterpolator.</span><span class="sxs-lookup"><span data-stu-id="d7465-119">Open the Command Prompt window and navigate to the CustomInterpolator project directory.</span></span> <span data-ttu-id="d7465-120">Par exemple, le chemin d’installation par défaut de cet exemple est C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ WindowsAnimation \\ CustomInterpolator</span><span class="sxs-lookup"><span data-stu-id="d7465-120">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\CustomInterpolator</span></span>

2.  <span data-ttu-id="d7465-121">Exécutez la commande suivante : **MSBuild CustomInterpolator. sln**</span><span class="sxs-lookup"><span data-stu-id="d7465-121">Run the following command: **msbuild CustomInterpolator.sln**</span></span>

<span data-ttu-id="d7465-122">**Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut)**</span><span class="sxs-lookup"><span data-stu-id="d7465-122">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="d7465-123">Ouvrez l’Explorateur Windows et accédez au répertoire du projet CustomInterpolator.</span><span class="sxs-lookup"><span data-stu-id="d7465-123">Open Windows Explorer and navigate to the CustomInterpolator project directory.</span></span>

    > [!Note]  
    > <span data-ttu-id="d7465-124">L’extension de nom de fichier. sln n’est pas affichée sous paramètres de dossier par défaut.</span><span class="sxs-lookup"><span data-stu-id="d7465-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="d7465-125">Dans ce cas, il peut être identifié par son icône unique ou par sa description de type, « Microsoft Visual Studio solution ».</span><span class="sxs-lookup"><span data-stu-id="d7465-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

2.  <span data-ttu-id="d7465-126">Double-cliquez sur l’icône du fichier CustomInterpolator. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d7465-126">Double-click the icon for the CustomInterpolator.sln file to open the project in Visual Studio.</span></span>

3.  <span data-ttu-id="d7465-127">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="d7465-127">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="d7465-128">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="d7465-128">Running the Sample</span></span>

<span data-ttu-id="d7465-129">Pour exécuter l’exemple :</span><span class="sxs-lookup"><span data-stu-id="d7465-129">To run the sample:</span></span>

1.  <span data-ttu-id="d7465-130">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="d7465-130">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="d7465-131">Exécutez **CustomInterpolator.exe** à partir de l’invite de commandes, ou double-cliquez sur l’icône de CustomInterpolator.exe dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="d7465-131">Run **CustomInterpolator.exe** at the command prompt, or double-click the icon for CustomInterpolator.exe in Windows Explorer.</span></span>
3.  <span data-ttu-id="d7465-132">Redimensionnez la fenêtre ou appuyez sur la barre d’espace, et les images se réorganiseront de manière aléatoire au milieu de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="d7465-132">Resize the window or press the spacebar, and the images will arrange themselves randomly in the middle of the client area.</span></span>

4.  <span data-ttu-id="d7465-133">Appuyez sur la flèche haut ou bas. les images s’accélèrent vers le haut ou le bas de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="d7465-133">Press the up or down arrow and the images will accelerate toward the top or bottom of the client area.</span></span>

 

 




