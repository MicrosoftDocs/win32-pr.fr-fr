---
description: Montre comment implémenter un effet vidéo en tant que transformation de Media Foundation (MFT).
ms.assetid: ad7d20bc-5eab-4390-a48b-5ea8e97ead7d
title: Exemple de MFT_Grayscale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273c562eb5985d0a329c434a8e4aa44119744496
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114394"
---
# <a name="mft_grayscale-sample"></a><span data-ttu-id="414e7-103">\_Exemple de nuances de gris MFT</span><span class="sxs-lookup"><span data-stu-id="414e7-103">MFT\_Grayscale Sample</span></span>

<span data-ttu-id="414e7-104">Montre comment implémenter un effet vidéo en tant que transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="414e7-104">Shows how to implement a video effect as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="414e7-105">La MFT en nuances de gris convertit la vidéo YUV en nuances de gris en définissant les valeurs de chrominance dans la vidéo sur neutre.</span><span class="sxs-lookup"><span data-stu-id="414e7-105">The grayscale MFT converts YUV video to grayscale by setting the chroma values in the video to neutral.</span></span> <span data-ttu-id="414e7-106">La table MFT accepte les vidéos non compressées dans les formats UYVY, YUY2 ou NV12.</span><span class="sxs-lookup"><span data-stu-id="414e7-106">The MFT accepts uncompressed video in UYVY, YUY2, or NV12 formats.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="414e7-107">API illustrées</span><span class="sxs-lookup"><span data-stu-id="414e7-107">APIs Demonstrated</span></span>

<span data-ttu-id="414e7-108">Cet exemple illustre les interfaces de Microsoft Media Foundation suivantes :</span><span class="sxs-lookup"><span data-stu-id="414e7-108">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="414e7-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="414e7-109">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a><span data-ttu-id="414e7-110">Utilisation</span><span class="sxs-lookup"><span data-stu-id="414e7-110">Usage</span></span>

<span data-ttu-id="414e7-111">L’exemple MFT en \_ nuances de gris génère une dll qui est un serveur com pour la MFT.</span><span class="sxs-lookup"><span data-stu-id="414e7-111">The MFT\_GrayScale sample builds a DLL that is a COM server for the MFT.</span></span> <span data-ttu-id="414e7-112">Avant d’utiliser la MFT, vous devez inscrire la DLL.</span><span class="sxs-lookup"><span data-stu-id="414e7-112">Before using the MFT, you must register the DLL.</span></span>

<span data-ttu-id="414e7-113">Pour voir la MFT en nuances de gris en cours d’utilisation, exécutez l' [exemple PlaybackFX](/previous-versions//bb970336(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="414e7-113">To see the grayscale MFT in use, run the [PlaybackFX Sample](/previous-versions//bb970336(v=vs.85)).</span></span> <span data-ttu-id="414e7-114">Vous pouvez également utiliser l’outil TopoEdit pour créer une topologie qui comprend la MFT en nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="414e7-114">You can also use the TopoEdit tool to build a topology that includes the grayscale MFT.</span></span> <span data-ttu-id="414e7-115">Pour plus d’informations sur TopoEdit, consultez [TopoEdit](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="414e7-115">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="414e7-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="414e7-116">Requirements</span></span>



| <span data-ttu-id="414e7-117">Produit</span><span class="sxs-lookup"><span data-stu-id="414e7-117">Product</span></span>                                                        | <span data-ttu-id="414e7-118">Version</span><span class="sxs-lookup"><span data-stu-id="414e7-118">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="414e7-119">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="414e7-119">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="414e7-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="414e7-120">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="414e7-121">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="414e7-121">Downloading the Sample</span></span>

<span data-ttu-id="414e7-122">Cet exemple est disponible dans le [référentiel GitHub des exemples classiques Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_grayscale).</span><span class="sxs-lookup"><span data-stu-id="414e7-122">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_grayscale).</span></span>

## <a name="related-topics"></a><span data-ttu-id="414e7-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="414e7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="414e7-124">À propos de la vidéo YUV</span><span class="sxs-lookup"><span data-stu-id="414e7-124">About YUV Video</span></span>](about-yuv-video.md)
</dt> <dt>

[<span data-ttu-id="414e7-125">Exemples du kit de développement logiciel Media Foundation</span><span class="sxs-lookup"><span data-stu-id="414e7-125">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="414e7-126">Transformations de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="414e7-126">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="414e7-127">\_Exemple AUDIODELAY MFT</span><span class="sxs-lookup"><span data-stu-id="414e7-127">MFT\_AudioDelay Sample</span></span>](mft-audiodelay-sample.md)
</dt> <dt>

[<span data-ttu-id="414e7-128">Écriture d’une table MFT personnalisée</span><span class="sxs-lookup"><span data-stu-id="414e7-128">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 
