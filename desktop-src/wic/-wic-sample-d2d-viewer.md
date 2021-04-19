---
description: Cet exemple illustre l’utilisation de WIC (Windows Imaging Component) pour décoder un fichier image et Direct2D pour afficher l’image à l’écran.
ms.assetid: 4f989ff6-b513-4354-a1bb-8d9521f693a2
title: Visionneuse d’images WIC avec l’exemple Direct2D
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: a18bf17e7f43d3c4ad935bae9f8ed42e7b48db01
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2021
ms.locfileid: "106532697"
---
# <a name="wic-image-viewer-using-direct2d-sample"></a><span data-ttu-id="11fcd-103">Visionneuse d’images WIC avec l’exemple Direct2D</span><span class="sxs-lookup"><span data-stu-id="11fcd-103">WIC image viewer using Direct2D sample</span></span>

<span data-ttu-id="11fcd-104">Cet exemple illustre l’utilisation de WIC (Windows Imaging Component) pour décoder un fichier image et Direct2D pour afficher l’image à l’écran.</span><span class="sxs-lookup"><span data-stu-id="11fcd-104">This sample demonstrates the use of Windows Imaging Component (WIC) to decode an image file and Direct2D to render the image to the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="11fcd-105">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11fcd-105">Requirements</span></span>

<span data-ttu-id="11fcd-106">Cet exemple présente les exigences suivantes.</span><span class="sxs-lookup"><span data-stu-id="11fcd-106">This sample has the following requirements.</span></span>

| <span data-ttu-id="11fcd-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11fcd-107">Requirement</span></span> | <span data-ttu-id="11fcd-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="11fcd-108">Value</span></span> |
|-|-|
| <span data-ttu-id="11fcd-109">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11fcd-109">Minimum supported client</span></span> | <span data-ttu-id="11fcd-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11fcd-110">Windows Vista</span></span> |
| <span data-ttu-id="11fcd-111">SDK Windows minimal</span><span class="sxs-lookup"><span data-stu-id="11fcd-111">Minimum Windows SDK</span></span> | <span data-ttu-id="11fcd-112">[Kit de développement logiciel (SDK) Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) pour Windows 7</span><span class="sxs-lookup"><span data-stu-id="11fcd-112">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for Windows 7</span></span> |

## <a name="downloading-the-sample"></a><span data-ttu-id="11fcd-113">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="11fcd-113">Downloading the sample</span></span>

<span data-ttu-id="11fcd-114">Cet exemple est disponible dans la [visionneuse WIC D2D](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewerd2d).</span><span class="sxs-lookup"><span data-stu-id="11fcd-114">This sample is available at [WIC Viewer D2D](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewerd2d).</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="11fcd-115">Génération de l’exemple</span><span class="sxs-lookup"><span data-stu-id="11fcd-115">Building the sample</span></span>

### <a name="using-visual-studio-preferred-method"></a><span data-ttu-id="11fcd-116">Utilisation de Visual Studio (méthode recommandée)</span><span class="sxs-lookup"><span data-stu-id="11fcd-116">Using Visual Studio (preferred method)</span></span>

1. <span data-ttu-id="11fcd-117">Ouvrez l’Explorateur Windows et accédez au répertoire.</span><span class="sxs-lookup"><span data-stu-id="11fcd-117">Open Windows Explorer and navigate to the directory.</span></span>
2. <span data-ttu-id="11fcd-118">Double-cliquez sur l’icône du fichier. sln (solution) pour ouvrir le fichier dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="11fcd-118">Double-click the icon for the .sln (solution) file to open the file in Visual Studio.</span></span>
3. <span data-ttu-id="11fcd-119">Dans le menu **Générer**, sélectionnez **Générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="11fcd-119">In the **Build** menu, select **Build Solution**.</span></span> <span data-ttu-id="11fcd-120">L’application sera générée dans le répertoire de \\ débogage ou de libération par défaut \\ .</span><span class="sxs-lookup"><span data-stu-id="11fcd-120">The application will be built in the default \\Debug or \\Release directory.</span></span>

### <a name="using-the-command-prompt"></a><span data-ttu-id="11fcd-121">À l’aide de l’invite de commandes</span><span class="sxs-lookup"><span data-stu-id="11fcd-121">Using the command prompt</span></span>

<span data-ttu-id="11fcd-122">Pour générer l’exemple à l’aide d’une invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="11fcd-122">To build the sample by using a command prompt:</span></span>

1. <span data-ttu-id="11fcd-123">Ouvrez une fenêtre d’invite de commandes et accédez au répertoire de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="11fcd-123">Open a command prompt window and navigate to the sample directory.</span></span>
2. <span data-ttu-id="11fcd-124">Saisissez `msbuild WICViewerD2D.sln`</span><span class="sxs-lookup"><span data-stu-id="11fcd-124">Type `msbuild WICViewerD2D.sln`</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="11fcd-125">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="11fcd-125">Running the sample</span></span>

<span data-ttu-id="11fcd-126">Après avoir démarré l’application, chargez un fichier image à l’aide de la commande **ouvrir** du menu **fichier** .</span><span class="sxs-lookup"><span data-stu-id="11fcd-126">After you start the application, load an image file by using the **Open** command of the **File** menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="11fcd-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11fcd-127">See also</span></span>

[<span data-ttu-id="11fcd-128">Codec d’image Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="11fcd-128">Microsoft Windows Imaging Codec</span></span>](-wic-lh.md)

[<span data-ttu-id="11fcd-129">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="11fcd-129">Programming guide</span></span>](-wic-programming-guide.md)

[<span data-ttu-id="11fcd-130">Référence</span><span class="sxs-lookup"><span data-stu-id="11fcd-130">Reference</span></span>](-wic-codec-reference.md)

[<span data-ttu-id="11fcd-131">Direct2D</span><span class="sxs-lookup"><span data-stu-id="11fcd-131">Direct2D</span></span>](../direct2d/direct2d-portal.md)

[<span data-ttu-id="11fcd-132">Exemples et exemples de code</span><span class="sxs-lookup"><span data-stu-id="11fcd-132">Samples and code examples</span></span>](-wic-samples.md)
