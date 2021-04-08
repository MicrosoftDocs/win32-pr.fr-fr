---
description: Montre comment utiliser la haute définition de l’accélération vidéo Microsoft DirectX (DXVA-HD).
ms.assetid: dfd5cf5c-7d6e-4894-8d9b-41ef0293b3d3
title: DXVA-HD, exemple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ae1945a98bc668aa12cc6cdf8d9e4693cbde27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861802"
---
# <a name="dxva-hd-sample"></a><span data-ttu-id="aac2a-103">DXVA-HD, exemple</span><span class="sxs-lookup"><span data-stu-id="aac2a-103">DXVA-HD Sample</span></span>

<span data-ttu-id="aac2a-104">Montre comment utiliser la haute définition de l’accélération vidéo Microsoft DirectX (DXVA-HD).</span><span class="sxs-lookup"><span data-stu-id="aac2a-104">Shows how to use Microsoft DirectX Video Acceleration High Definition (DXVA-HD).</span></span>

<span data-ttu-id="aac2a-105">Cet exemple est essentiellement un port de l' [ \_ exemple DXVA2 VideoProc](dxva2-videoproc-sample.md).</span><span class="sxs-lookup"><span data-stu-id="aac2a-105">This sample is essentially a port of the [DXVA2\_VideoProc Sample](dxva2-videoproc-sample.md).</span></span> <span data-ttu-id="aac2a-106">Il a les mêmes fonctions de base, et la plupart des commandes de clavier sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="aac2a-106">It has the same basic functions, and most of the keyboard commands are the same.</span></span>

<span data-ttu-id="aac2a-107">L’exemple génère par programmation une vidéo avec un flux principal et un sous-flux.</span><span class="sxs-lookup"><span data-stu-id="aac2a-107">The sample programmatically generates video with a primary stream and a substream.</span></span> <span data-ttu-id="aac2a-108">Le flux principal affiche les barres de couleur SMPTE.</span><span class="sxs-lookup"><span data-stu-id="aac2a-108">The primary stream displays SMPTE color bars.</span></span> <span data-ttu-id="aac2a-109">Le sous-flux est mélangé en alpha sur le flux principal à l’aide du masquage par luminance.</span><span class="sxs-lookup"><span data-stu-id="aac2a-109">The substream is alpha-blended onto the primary stream using luma keying.</span></span> <span data-ttu-id="aac2a-110">L’utilisateur peut modifier les paramètres de traitement vidéo, y compris la valeur alpha planaire, les rectangles source et destination, les réglages de couleur et l’espace colorimétrique.</span><span class="sxs-lookup"><span data-stu-id="aac2a-110">The user can change the video processing parameters, including the planar alpha value, source and destination rectangles, color adjustments, and color space.</span></span> <span data-ttu-id="aac2a-111">L’illustration suivante montre la vidéo qui est générée.</span><span class="sxs-lookup"><span data-stu-id="aac2a-111">The following image shows that video that is generated.</span></span>

![capture d’écran de l’exemple DXVA-HD](images/dxva-hd-sample.png)

## <a name="apis-demonstrated"></a><span data-ttu-id="aac2a-113">API illustrées</span><span class="sxs-lookup"><span data-stu-id="aac2a-113">APIs Demonstrated</span></span>

<span data-ttu-id="aac2a-114">Cet exemple illustre les interfaces DXVA-HD suivantes :</span><span class="sxs-lookup"><span data-stu-id="aac2a-114">This sample demonstrates the following DXVA-HD interfaces:</span></span>

-   [<span data-ttu-id="aac2a-115">**\_Appareil IDXVAHD**</span><span class="sxs-lookup"><span data-stu-id="aac2a-115">**IDXVAHD\_Device**</span></span>](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device)
-   [<span data-ttu-id="aac2a-116">**IDXVAHD \_ VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="aac2a-116">**IDXVAHD\_VideoProcessor**</span></span>](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor)

## <a name="requirements"></a><span data-ttu-id="aac2a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aac2a-117">Requirements</span></span>



| <span data-ttu-id="aac2a-118">Produit</span><span class="sxs-lookup"><span data-stu-id="aac2a-118">Product</span></span>                                                        | <span data-ttu-id="aac2a-119">Version</span><span class="sxs-lookup"><span data-stu-id="aac2a-119">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="aac2a-120">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="aac2a-120">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="aac2a-121">Windows 7</span><span class="sxs-lookup"><span data-stu-id="aac2a-121">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="aac2a-122">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="aac2a-122">Downloading the Sample</span></span>

<span data-ttu-id="aac2a-123">Cet exemple est disponible dans le [référentiel GitHub des exemples classiques Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/DXVA_HD).</span><span class="sxs-lookup"><span data-stu-id="aac2a-123">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/DXVA_HD).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aac2a-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aac2a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aac2a-125">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="aac2a-125">DXVA-HD</span></span>](dxva-hd.md)
</dt> <dt>

[<span data-ttu-id="aac2a-126">Exemples du kit de développement logiciel Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aac2a-126">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



