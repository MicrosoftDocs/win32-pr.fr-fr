---
description: Cet exemple illustre l’utilisation de WIC (Windows Imaging Component) pour décoder une image encodée avec des niveaux progressifs.
ms.assetid: 14018dce-26f0-4e1e-9d19-c5b42dd2cdab
title: Exemple de décodage progressif WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: 2e4b1fc560af0ee8c817208fec628ddb068676bb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2021
ms.locfileid: "106543156"
---
# <a name="wic-progressive-decoding-sample"></a><span data-ttu-id="a13a4-103">Exemple de décodage progressif WIC</span><span class="sxs-lookup"><span data-stu-id="a13a4-103">WIC progressive decoding sample</span></span>

<span data-ttu-id="a13a4-104">Cet exemple illustre l’utilisation de WIC (Windows Imaging Component) pour décoder une image encodée avec des niveaux progressifs.</span><span class="sxs-lookup"><span data-stu-id="a13a4-104">This sample demonstrates the use of Windows Imaging Component (WIC) to decode an image that is encoded with progressive levels.</span></span> <span data-ttu-id="a13a4-105">Cet exemple utilise Direct2D pour restituer les différents niveaux progressifs à l’écran.</span><span class="sxs-lookup"><span data-stu-id="a13a4-105">This sample uses Direct2D to render the different progressive levels to the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="a13a4-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a13a4-106">Requirements</span></span>

<span data-ttu-id="a13a4-107">Cet exemple présente les exigences suivantes.</span><span class="sxs-lookup"><span data-stu-id="a13a4-107">This sample has the following requirements.</span></span>

| <span data-ttu-id="a13a4-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a13a4-108">Requirement</span></span> | <span data-ttu-id="a13a4-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="a13a4-109">Value</span></span> |
|-|
| <span data-ttu-id="a13a4-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a13a4-110">Minimum supported client</span></span> | <span data-ttu-id="a13a4-111">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a13a4-111">Windows 7</span></span> |
| <span data-ttu-id="a13a4-112">SDK Windows minimal</span><span class="sxs-lookup"><span data-stu-id="a13a4-112">Minimum Windows SDK</span></span> | <span data-ttu-id="a13a4-113">[Kit de développement logiciel (SDK) Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) pour Windows 7</span><span class="sxs-lookup"><span data-stu-id="a13a4-113">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for Windows 7</span></span> |

## <a name="downloading-the-sample"></a><span data-ttu-id="a13a4-114">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="a13a4-114">Downloading the sample</span></span>

<span data-ttu-id="a13a4-115">Cet exemple est disponible dans l' [encodage progressif WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/progressivedecoding).</span><span class="sxs-lookup"><span data-stu-id="a13a4-115">This sample is available at [WIC progressive encoding](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/progressivedecoding).</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="a13a4-116">Génération de l’exemple</span><span class="sxs-lookup"><span data-stu-id="a13a4-116">Building the sample</span></span>

### <a name="using-visual-studio-preferred-method"></a><span data-ttu-id="a13a4-117">Utilisation de Visual Studio (méthode recommandée)</span><span class="sxs-lookup"><span data-stu-id="a13a4-117">Using Visual Studio (preferred method)</span></span>

1. <span data-ttu-id="a13a4-118">Ouvrez l’Explorateur Windows et accédez au répertoire.</span><span class="sxs-lookup"><span data-stu-id="a13a4-118">Open Windows Explorer and navigate to the directory.</span></span>
2. <span data-ttu-id="a13a4-119">Double-cliquez sur l’icône du fichier. sln (solution) pour ouvrir le fichier dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a13a4-119">Double-click the icon for the .sln (solution) file to open the file in Visual Studio.</span></span>
3. <span data-ttu-id="a13a4-120">Dans le menu Générer, sélectionnez Générer la solution.</span><span class="sxs-lookup"><span data-stu-id="a13a4-120">In the Build menu, select Build Solution.</span></span> <span data-ttu-id="a13a4-121">L’application sera générée dans le répertoire de \\ débogage ou de libération par défaut \\ .</span><span class="sxs-lookup"><span data-stu-id="a13a4-121">The application will be built in the default \\Debug or \\Release directory.</span></span>

### <a name="using-the-command-prompt"></a><span data-ttu-id="a13a4-122">À l’aide de l’invite de commandes</span><span class="sxs-lookup"><span data-stu-id="a13a4-122">Using the command prompt</span></span>

<span data-ttu-id="a13a4-123">Pour générer l’exemple à l’aide de l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="a13a4-123">To build the sample using the command prompt.</span></span>

1. <span data-ttu-id="a13a4-124">Ouvrez l’invite de commandes et accédez au répertoire de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="a13a4-124">Open the command prompt and navigate to the sample directory.</span></span>
2. <span data-ttu-id="a13a4-125">Saisissez `msbuild WICProgressiveDecoding.sln`</span><span class="sxs-lookup"><span data-stu-id="a13a4-125">Type `msbuild WICProgressiveDecoding.sln`</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="a13a4-126">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="a13a4-126">Running the sample</span></span>

<span data-ttu-id="a13a4-127">Une fois l’application lancée, chargez un fichier image dans le menu fichier ouvrir.</span><span class="sxs-lookup"><span data-stu-id="a13a4-127">After the application is launched, load an image file through file open menu.</span></span> <span data-ttu-id="a13a4-128">Lors du chargement, le niveau de progressif par défaut est défini sur 0.</span><span class="sxs-lookup"><span data-stu-id="a13a4-128">On loading, the default progressive level is set to 0.</span></span> <span data-ttu-id="a13a4-129">Vous pouvez accéder à différents niveaux progressifs via le menu ou la touche haut/PG.</span><span class="sxs-lookup"><span data-stu-id="a13a4-129">You can navigate to different progressive levels either through menu or Up/Down key.</span></span> <span data-ttu-id="a13a4-130">Le texte de niveau progressif actuel est affiché dans la barre d’état de la fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="a13a4-130">The current progressive level text is displayed on the main window status bar.</span></span> <span data-ttu-id="a13a4-131">Le redimensionnement de fenêtre est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a13a4-131">Window resizing is supported.</span></span>

> [!NOTE]
> <span data-ttu-id="a13a4-132">Le décodage progressif est disponible uniquement pour les images qui ont été encodées progressivement.</span><span class="sxs-lookup"><span data-stu-id="a13a4-132">Progressive decoding is available only for images that have been progressively encoded.</span></span> <span data-ttu-id="a13a4-133">L’image fournie avec cet exemple a été encodée progressivement.</span><span class="sxs-lookup"><span data-stu-id="a13a4-133">The image provided with this sample has been progressively encoded.</span></span>

## <a name="see-also"></a><span data-ttu-id="a13a4-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a13a4-134">See also</span></span>

[<span data-ttu-id="a13a4-135">Codec d’image Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="a13a4-135">Microsoft Windows Imaging Codec</span></span>](-wic-lh.md)

[<span data-ttu-id="a13a4-136">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="a13a4-136">Programming guide</span></span>](-wic-programming-guide.md)

[<span data-ttu-id="a13a4-137">Référence</span><span class="sxs-lookup"><span data-stu-id="a13a4-137">Reference</span></span>](-wic-codec-reference.md)

[<span data-ttu-id="a13a4-138">Direct2D</span><span class="sxs-lookup"><span data-stu-id="a13a4-138">Direct2D</span></span>](../direct2d/direct2d-portal.md)

[<span data-ttu-id="a13a4-139">Exemples et exemples de code</span><span class="sxs-lookup"><span data-stu-id="a13a4-139">Samples and code examples</span></span>](-wic-samples.md)

[<span data-ttu-id="a13a4-140">Vue d’ensemble du décodage progressif</span><span class="sxs-lookup"><span data-stu-id="a13a4-140">Progressive decoding overview</span></span>](-wic-progressive-decoding.md)
