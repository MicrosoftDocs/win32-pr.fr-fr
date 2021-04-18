---
title: Exemple d’animation Timer-Driven
description: Montre comment utiliser l’animation Windows avec le minuteur d’animation, tout en utilisant GDI+ pour animer la couleur d’arrière-plan d’une fenêtre.
ms.assetid: c50a4bfb-855b-4837-a117-84f412943b14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec145b087a112c7482de3a749c690a1824195ea3
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/10/2020
ms.locfileid: "104314585"
---
# <a name="timer-driven-animation-sample"></a><span data-ttu-id="cf9b2-103">Exemple d’animation Timer-Driven</span><span class="sxs-lookup"><span data-stu-id="cf9b2-103">Timer-Driven Animation Sample</span></span>

<span data-ttu-id="cf9b2-104">Montre comment utiliser l’animation Windows avec le minuteur d’animation, tout en utilisant GDI+ pour animer la couleur d’arrière-plan d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cf9b2-104">Shows how to use Windows Animation with the Animation Timer, while using GDI+ to animate the background color of a window.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="cf9b2-105">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="cf9b2-105">Downloading the Sample</span></span>

<span data-ttu-id="cf9b2-106">Cet exemple est disponible aux emplacements suivants.</span><span class="sxs-lookup"><span data-stu-id="cf9b2-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="cf9b2-107">Emplacement</span><span class="sxs-lookup"><span data-stu-id="cf9b2-107">Location</span></span>                               | <span data-ttu-id="cf9b2-108">Chemin d’accès/URL</span><span class="sxs-lookup"><span data-stu-id="cf9b2-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf9b2-109">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="cf9b2-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="cf9b2-110">Kit de développement logiciel (SDK) Microsoft Windows 7,0</span><span class="sxs-lookup"><span data-stu-id="cf9b2-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="cf9b2-111">Galerie de code</span><span class="sxs-lookup"><span data-stu-id="cf9b2-111">Code Gallery</span></span>                           | [<span data-ttu-id="cf9b2-112">Exemple de code du gestionnaire d’animations Windows</span><span class="sxs-lookup"><span data-stu-id="cf9b2-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

<span data-ttu-id="cf9b2-113">Une fois que vous avez téléchargé et installé le SDK Windows, vous trouverez les exemples dans le répertoire d’installation.</span><span class="sxs-lookup"><span data-stu-id="cf9b2-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="cf9b2-114">Par exemple, si vous utilisez le chemin d’installation par défaut pour le SDK Windows pour Windows 7, les exemples sont installés dans C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples.</span><span class="sxs-lookup"><span data-stu-id="cf9b2-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="cf9b2-115">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="cf9b2-115">Building the Sample</span></span>

<span data-ttu-id="cf9b2-116">Utilisez l’une des méthodes suivantes pour générer l’exemple.</span><span class="sxs-lookup"><span data-stu-id="cf9b2-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="cf9b2-117">**Pour générer l’exemple à partir de l’invite de commandes**</span><span class="sxs-lookup"><span data-stu-id="cf9b2-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="cf9b2-118">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet TimerDriven.</span><span class="sxs-lookup"><span data-stu-id="cf9b2-118">Open the Command Prompt window and navigate to the TimerDriven project directory.</span></span> <span data-ttu-id="cf9b2-119">Par exemple, le chemin d’installation par défaut de cet exemple est C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ WindowsAnimation \\ TimerDriven.</span><span class="sxs-lookup"><span data-stu-id="cf9b2-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\TimerDriven.</span></span>

2.  <span data-ttu-id="cf9b2-120">Exécutez la commande suivante : **MSBuild TimerDriven. sln**</span><span class="sxs-lookup"><span data-stu-id="cf9b2-120">Run the following command: **msbuild TimerDriven.sln**</span></span>

<span data-ttu-id="cf9b2-121">**Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut)**</span><span class="sxs-lookup"><span data-stu-id="cf9b2-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="cf9b2-122">Ouvrez l’Explorateur Windows et accédez au répertoire du projet TimerDriven.</span><span class="sxs-lookup"><span data-stu-id="cf9b2-122">Open Windows Explorer and navigate to the TimerDriven project directory.</span></span>

2.  <span data-ttu-id="cf9b2-123">Double-cliquez sur l’icône du fichier TimerDriven. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="cf9b2-123">Double-click the icon for the TimerDriven.sln file to open the project in Visual Studio.</span></span>

    > [!Note]  
    > <span data-ttu-id="cf9b2-124">L’extension de nom de fichier. sln n’est pas affichée sous paramètres de dossier par défaut.</span><span class="sxs-lookup"><span data-stu-id="cf9b2-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="cf9b2-125">Dans ce cas, il peut être identifié par son icône unique ou par sa description de type, « Microsoft Visual Studio solution ».</span><span class="sxs-lookup"><span data-stu-id="cf9b2-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="cf9b2-126">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="cf9b2-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="cf9b2-127">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="cf9b2-127">Running the Sample</span></span>

<span data-ttu-id="cf9b2-128">Pour exécuter l’exemple :</span><span class="sxs-lookup"><span data-stu-id="cf9b2-128">To run the sample:</span></span>

1.  <span data-ttu-id="cf9b2-129">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="cf9b2-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="cf9b2-130">Exécutez **TimerDriven.exe** à partir de l’invite de commandes, ou double-cliquez sur l’icône de TimerDriven.exe dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="cf9b2-130">Run **TimerDriven.exe** at the command prompt, or double-click the icon for TimerDriven.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="cf9b2-131">Cliquez n’importe où dans la zone cliente et la couleur d’arrière-plan de la fenêtre passe à une couleur aléatoire.</span><span class="sxs-lookup"><span data-stu-id="cf9b2-131">Click anywhere in the client area, and the background color of the window will change to a random color.</span></span>

 

 




