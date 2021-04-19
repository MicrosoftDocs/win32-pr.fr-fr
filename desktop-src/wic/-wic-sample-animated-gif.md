---
description: Cet exemple illustre le décodage de différents frames dans un fichier GIF, la lecture des métadonnées appropriées pour chaque frame, la composition des frames et le rendu de l’animation avec Direct2D.
ms.assetid: d71c66b5-d37c-4c8a-bfd7-b97c69c3b8e9
title: Exemple de gif animé WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: afb0c1368e2c66d40d1be4095ec56d5daeb5ab53
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2021
ms.locfileid: "106528588"
---
# <a name="wic-animated-gif-sample"></a><span data-ttu-id="b4244-103">Exemple de GIF animé WIC</span><span class="sxs-lookup"><span data-stu-id="b4244-103">WIC animated GIF sample</span></span>

<span data-ttu-id="b4244-104">Cet exemple illustre le décodage de différents frames dans un fichier GIF, la lecture des métadonnées appropriées pour chaque frame, la composition des frames et le rendu de l’animation avec Direct2D.</span><span class="sxs-lookup"><span data-stu-id="b4244-104">This sample demonstrates decoding various frames in a GIF file, reading appropriate metadata for each frame, composing frames, and rendering the animation with Direct2D.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4244-105">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4244-105">Requirements</span></span>

<span data-ttu-id="b4244-106">Cet exemple présente les exigences suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4244-106">This sample has the following requirements.</span></span>

| <span data-ttu-id="b4244-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4244-107">Requirement</span></span> | <span data-ttu-id="b4244-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4244-108">Value</span></span> |
|-|-|
| <span data-ttu-id="b4244-109">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4244-109">Minimum supported client</span></span> | <span data-ttu-id="b4244-110">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b4244-110">Windows 7</span></span> |
| <span data-ttu-id="b4244-111">SDK Windows minimal</span><span class="sxs-lookup"><span data-stu-id="b4244-111">Minimum Windows SDK</span></span> | <span data-ttu-id="b4244-112">[Kit de développement logiciel (SDK) Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) pour Windows 7</span><span class="sxs-lookup"><span data-stu-id="b4244-112">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for Windows 7</span></span> |

## <a name="downloading-the-sample"></a><span data-ttu-id="b4244-113">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="b4244-113">Downloading the sample</span></span>

<span data-ttu-id="b4244-114">Cet exemple est disponible dans le fichier [gif animé WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif).</span><span class="sxs-lookup"><span data-stu-id="b4244-114">This sample is available at [WIC animated GIF](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif).</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="b4244-115">Génération de l’exemple</span><span class="sxs-lookup"><span data-stu-id="b4244-115">Building the sample</span></span>

### <a name="using-visual-studio-preferred-method"></a><span data-ttu-id="b4244-116">Utilisation de Visual Studio (méthode recommandée)</span><span class="sxs-lookup"><span data-stu-id="b4244-116">Using Visual Studio (preferred method)</span></span>

1. <span data-ttu-id="b4244-117">Ouvrez l’Explorateur Windows et accédez au répertoire.</span><span class="sxs-lookup"><span data-stu-id="b4244-117">Open Windows Explorer and navigate to the directory.</span></span>
2. <span data-ttu-id="b4244-118">Double-cliquez sur l’icône du fichier. sln (solution) pour ouvrir le fichier dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b4244-118">Double-click the icon for the .sln (solution) file to open the file in Visual Studio.</span></span>
3. <span data-ttu-id="b4244-119">Dans le menu **Générer**, sélectionnez **Générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="b4244-119">In the **Build** menu, select **Build Solution**.</span></span> <span data-ttu-id="b4244-120">L’application sera générée dans le répertoire de \\ débogage ou de libération par défaut \\ .</span><span class="sxs-lookup"><span data-stu-id="b4244-120">The application will be built in the default \\Debug or \\Release directory.</span></span>

### <a name="using-the-command-prompt"></a><span data-ttu-id="b4244-121">À l’aide de l’invite de commandes</span><span class="sxs-lookup"><span data-stu-id="b4244-121">Using the command prompt</span></span>

<span data-ttu-id="b4244-122">Pour générer l’exemple à l’aide d’une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="b4244-122">To build the sample by using a command prompt.</span></span>

1. <span data-ttu-id="b4244-123">Ouvrez l’invite de commandes et accédez au répertoire de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="b4244-123">Open the command prompt and navigate to the sample directory.</span></span>
2. <span data-ttu-id="b4244-124">Saisissez `msbuild WICAnimatedGif.sln`</span><span class="sxs-lookup"><span data-stu-id="b4244-124">Type `msbuild WICAnimatedGif.sln`</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="b4244-125">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="b4244-125">Running the sample</span></span>

<span data-ttu-id="b4244-126">Une fois l’application lancée, chargez un fichier image à l’aide de la commande **ouvrir** du menu **fichier** .</span><span class="sxs-lookup"><span data-stu-id="b4244-126">After the application is launched, load an image file by using the **Open** command of the **File** menu.</span></span> <span data-ttu-id="b4244-127">Le redimensionnement de fenêtre est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b4244-127">Window resizing is supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4244-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4244-128">See also</span></span>

[<span data-ttu-id="b4244-129">Codec d’image Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="b4244-129">Microsoft Windows Imaging Codec</span></span>](-wic-lh.md)

[<span data-ttu-id="b4244-130">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="b4244-130">Programming guide</span></span>](-wic-programming-guide.md)

[<span data-ttu-id="b4244-131">Référence</span><span class="sxs-lookup"><span data-stu-id="b4244-131">Reference</span></span>](-wic-codec-reference.md)

[<span data-ttu-id="b4244-132">Direct2D</span><span class="sxs-lookup"><span data-stu-id="b4244-132">Direct2D</span></span>](../direct2d/direct2d-portal.md)

[<span data-ttu-id="b4244-133">Exemples et exemples de code</span><span class="sxs-lookup"><span data-stu-id="b4244-133">Samples and code examples</span></span>](-wic-samples.md)
