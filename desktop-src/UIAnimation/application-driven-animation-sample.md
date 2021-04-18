---
title: Exemple d’animation Application-Driven
description: Montre les animations Windows dans la configuration pilotée par l’application à l’aide de Direct2D pour animer la couleur d’arrière-plan d’une fenêtre et la synchronisation avec la fréquence d’actualisation.
ms.assetid: deefc473-6749-4e2b-ad34-33ccd206d231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06b24905d09ac6559527146ebf572666a6a84f5
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/10/2020
ms.locfileid: "106512304"
---
# <a name="application-driven-animation-sample"></a><span data-ttu-id="c539a-103">Exemple d’animation Application-Driven</span><span class="sxs-lookup"><span data-stu-id="c539a-103">Application-Driven Animation Sample</span></span>

<span data-ttu-id="c539a-104">Montre les animations Windows dans la configuration pilotée par l’application à l’aide de Direct2D pour animer la couleur d’arrière-plan d’une fenêtre et la synchronisation avec la fréquence d’actualisation.</span><span class="sxs-lookup"><span data-stu-id="c539a-104">Shows Windows Animation in the application-driven configuration by using Direct2D to animate the background color of a window and syncing to the refresh rate.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="c539a-105">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="c539a-105">Downloading the Sample</span></span>

<span data-ttu-id="c539a-106">Cet exemple est disponible aux emplacements suivants.</span><span class="sxs-lookup"><span data-stu-id="c539a-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="c539a-107">Emplacement</span><span class="sxs-lookup"><span data-stu-id="c539a-107">Location</span></span>                               | <span data-ttu-id="c539a-108">Chemin d’accès/URL</span><span class="sxs-lookup"><span data-stu-id="c539a-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c539a-109">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="c539a-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="c539a-110">Kit de développement logiciel (SDK) Microsoft Windows 7,0</span><span class="sxs-lookup"><span data-stu-id="c539a-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="c539a-111">Galerie de code</span><span class="sxs-lookup"><span data-stu-id="c539a-111">Code Gallery</span></span>                           | [<span data-ttu-id="c539a-112">Exemple de code du gestionnaire d’animations Windows</span><span class="sxs-lookup"><span data-stu-id="c539a-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

<span data-ttu-id="c539a-113">Une fois que vous avez téléchargé et installé le SDK Windows, vous trouverez les exemples dans le répertoire d’installation.</span><span class="sxs-lookup"><span data-stu-id="c539a-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="c539a-114">Par exemple, si vous utilisez le chemin d’installation par défaut pour le SDK Windows pour Windows 7, les exemples sont installés dans C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples.</span><span class="sxs-lookup"><span data-stu-id="c539a-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="c539a-115">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="c539a-115">Building the Sample</span></span>

<span data-ttu-id="c539a-116">Utilisez l’une des méthodes suivantes pour générer l’exemple.</span><span class="sxs-lookup"><span data-stu-id="c539a-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="c539a-117">**Pour générer l’exemple à partir de l’invite de commandes**</span><span class="sxs-lookup"><span data-stu-id="c539a-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="c539a-118">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet AppDriven.</span><span class="sxs-lookup"><span data-stu-id="c539a-118">Open the Command Prompt window and navigate to the AppDriven project directory.</span></span> <span data-ttu-id="c539a-119">Par exemple, le chemin d’installation par défaut de cet exemple est C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ WindowsAnimation \\ AppDriven.</span><span class="sxs-lookup"><span data-stu-id="c539a-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\AppDriven.</span></span>

2.  <span data-ttu-id="c539a-120">Exécutez la commande suivante : **MSBuild AppDriven. sln**</span><span class="sxs-lookup"><span data-stu-id="c539a-120">Run the following command: **msbuild AppDriven.sln**</span></span>

<span data-ttu-id="c539a-121">**Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut)**</span><span class="sxs-lookup"><span data-stu-id="c539a-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="c539a-122">Ouvrez l’Explorateur Windows et accédez au répertoire du projet AppDriven.</span><span class="sxs-lookup"><span data-stu-id="c539a-122">Open Windows Explorer and navigate to the AppDriven project directory.</span></span>

2.  <span data-ttu-id="c539a-123">Double-cliquez sur l’icône du fichier AppDriven. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c539a-123">Double-click the icon for the AppDriven.sln file to open the project in Visual Studio.</span></span>

    > [!Note]  
    > <span data-ttu-id="c539a-124">L’extension de nom de fichier. sln n’est pas affichée sous paramètres de dossier par défaut.</span><span class="sxs-lookup"><span data-stu-id="c539a-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="c539a-125">Dans ce cas, il peut être identifié par son icône unique ou par sa description de type, « Microsoft Visual Studio solution ».</span><span class="sxs-lookup"><span data-stu-id="c539a-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="c539a-126">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="c539a-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c539a-127">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="c539a-127">Running the Sample</span></span>

<span data-ttu-id="c539a-128">Pour exécuter l’exemple :</span><span class="sxs-lookup"><span data-stu-id="c539a-128">To run the sample:</span></span>

1.  <span data-ttu-id="c539a-129">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="c539a-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="c539a-130">Exécutez **AppDriven.exe** à partir de l’invite de commandes, ou double-cliquez sur l’icône de AppDriven.exe dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="c539a-130">Run **AppDriven.exe** at the command prompt, or double-click the icon for AppDriven.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="c539a-131">Cliquez n’importe où dans la zone cliente et la couleur d’arrière-plan de la fenêtre passe à une couleur aléatoire.</span><span class="sxs-lookup"><span data-stu-id="c539a-131">Click anywhere in the client area, and the background color of the window will change to a random color.</span></span>

 

 




