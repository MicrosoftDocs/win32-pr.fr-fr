---
description: Montre comment lire du contenu multimédia protégé dans Microsoft Media Foundation.
ms.assetid: e4a47e1c-16aa-45c1-8aa8-8929d6e1e653
title: Exemple ProtectedPlayback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee64b2a64ce4d40b6f15c2e5afb3b9a39e84c619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753901"
---
# <a name="protectedplayback-sample"></a><span data-ttu-id="ebe02-103">Exemple ProtectedPlayback</span><span class="sxs-lookup"><span data-stu-id="ebe02-103">ProtectedPlayback Sample</span></span>

<span data-ttu-id="ebe02-104">Montre comment lire du contenu multimédia protégé dans Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ebe02-104">Shows how to play protected media content in Microsoft Media Foundation.</span></span>

## <a name="usage"></a><span data-ttu-id="ebe02-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="ebe02-105">Usage</span></span>

<span data-ttu-id="ebe02-106">L’exemple ProtectedPlayback génère une application Windows.</span><span class="sxs-lookup"><span data-stu-id="ebe02-106">The ProtectedPlayback sample builds a Windows application.</span></span>

<span data-ttu-id="ebe02-107">Pour lire un fichier multimédia local, sélectionnez **ouvrir un fichier** dans le menu **fichier** .</span><span class="sxs-lookup"><span data-stu-id="ebe02-107">To play a local media file, select **Open File** from the **File** menu.</span></span> <span data-ttu-id="ebe02-108">Pour spécifier un fichier par URL, sélectionnez **ouvrir l’URL** dans le menu **fichier** .</span><span class="sxs-lookup"><span data-stu-id="ebe02-108">To specify a file by URL, select **Open URL** from the **File** menu.</span></span> <span data-ttu-id="ebe02-109">Une fois que vous avez sélectionné un fichier, la lecture commence automatiquement.</span><span class="sxs-lookup"><span data-stu-id="ebe02-109">After you select a file, playback begins automatically.</span></span> <span data-ttu-id="ebe02-110">Pour suspendre la lecture, appuyez sur la barre d’espace.</span><span class="sxs-lookup"><span data-stu-id="ebe02-110">To pause playback, press the SPACEBAR.</span></span> <span data-ttu-id="ebe02-111">Pour reprendre la lecture, appuyez de nouveau sur la barre d’espace.</span><span class="sxs-lookup"><span data-stu-id="ebe02-111">To resume playback, press the SPACEBAR again.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="ebe02-112">API illustrées</span><span class="sxs-lookup"><span data-stu-id="ebe02-112">APIs Demonstrated</span></span>

<span data-ttu-id="ebe02-113">Cet exemple illustre les interfaces de Media Foundation suivantes :</span><span class="sxs-lookup"><span data-stu-id="ebe02-113">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="ebe02-114">**IMFContentEnabler**</span><span class="sxs-lookup"><span data-stu-id="ebe02-114">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
-   [<span data-ttu-id="ebe02-115">**IMFContentProtectionManager**</span><span class="sxs-lookup"><span data-stu-id="ebe02-115">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)

## <a name="requirements"></a><span data-ttu-id="ebe02-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebe02-116">Requirements</span></span>



| <span data-ttu-id="ebe02-117">Produit</span><span class="sxs-lookup"><span data-stu-id="ebe02-117">Product</span></span>                                                        | <span data-ttu-id="ebe02-118">Version</span><span class="sxs-lookup"><span data-stu-id="ebe02-118">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="ebe02-119">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="ebe02-119">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="ebe02-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ebe02-120">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="ebe02-121">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="ebe02-121">Downloading the Sample</span></span>

<span data-ttu-id="ebe02-122">Cet exemple est disponible dans le [référentiel GitHub des exemples classiques Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback).</span><span class="sxs-lookup"><span data-stu-id="ebe02-122">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebe02-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ebe02-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebe02-124">Comment lire des fichiers multimédias protégés</span><span class="sxs-lookup"><span data-stu-id="ebe02-124">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)
</dt> <dt>

[<span data-ttu-id="ebe02-125">Exemples du kit de développement logiciel Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ebe02-125">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

<span data-ttu-id="ebe02-126">[Exemple MFPlayer](/previous-versions//bb970516(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ebe02-126">[MFPlayer Sample](/previous-versions//bb970516(v=vs.85))</span></span>
</dt> </dl>

 

 
