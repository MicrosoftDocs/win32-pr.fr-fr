---
title: Configuration de flux vidéo pour la recherche de performances
description: Configuration de flux vidéo pour la recherche de performances
ms.assetid: 2df507f9-60a5-4489-b3db-7fe15604e625
keywords:
- flux, configuration de flux vidéo
- codecs, configuration des flux vidéo
- flux vidéo, configuration
- flux vidéo, performances
- performances, flux vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4fc68e0b3a91cf135d29dc7123d5af88db84c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723435"
---
# <a name="configuring-video-streams-for-seeking-performance"></a><span data-ttu-id="d33ea-108">Configuration de flux vidéo pour la recherche de performances</span><span class="sxs-lookup"><span data-stu-id="d33ea-108">Configuring Video Streams for Seeking Performance</span></span>

<span data-ttu-id="d33ea-109">Certaines applications de lecture effectuent beaucoup de recherches sur des flux individuels.</span><span class="sxs-lookup"><span data-stu-id="d33ea-109">Some playback applications perform a lot of seeking on individual streams.</span></span> <span data-ttu-id="d33ea-110">La recherche est une zone où les performances peuvent varier considérablement en fonction des paramètres du flux.</span><span class="sxs-lookup"><span data-stu-id="d33ea-110">Seeking is an area where performance can vary greatly depending upon the settings of the stream.</span></span> <span data-ttu-id="d33ea-111">Si vous savez que votre contenu doit être optimisé pour une recherche rapide, vous pouvez adapter la configuration de votre flux pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="d33ea-111">If you know your content needs to be optimized for quick seeking, you can tailor your stream configuration to improve performance.</span></span>

<span data-ttu-id="d33ea-112">Le plus grand facteur affectant la vitesse des opérations de recherche dans la vidéo est l’espacement des images clés.</span><span class="sxs-lookup"><span data-stu-id="d33ea-112">The biggest factor affecting the speed of seeking operations in video is the spacing of the key frames.</span></span> <span data-ttu-id="d33ea-113">Étant donné que chaque trame entre les images clés doit être reconstruite en fonction des frames qui le précèdent, les images clés largement espacées génèrent des temps de recherche plus longs.</span><span class="sxs-lookup"><span data-stu-id="d33ea-113">Because every frame between key frames needs to be reconstructed based on the frames that come before it, widely spaced key frames result longer seek times.</span></span> <span data-ttu-id="d33ea-114">Par exemple, si un flux vidéo de 30 images par seconde a un espacement de trame de clé maximal de 10 secondes, il y a potentiellement 300 images entre les images clés.</span><span class="sxs-lookup"><span data-stu-id="d33ea-114">For example, if a video stream with 30 frames per second has a maximum key-frame spacing of 10 seconds, there are potentially 300 frames between key frames.</span></span> <span data-ttu-id="d33ea-115">Si vous recherchez la dernière [*image Delta*](wmformat-glossary.md), 299 frames doivent être reconstruits pour que le frame soit décompressé.</span><span class="sxs-lookup"><span data-stu-id="d33ea-115">If you seek to the last [*delta frame*](wmformat-glossary.md), 299 frames have to be reconstructed for the frame to be decompressed.</span></span> <span data-ttu-id="d33ea-116">Si chaque reconstruction de frame a pris 0,01 seconde, la recherche prendrait presque 3 secondes.</span><span class="sxs-lookup"><span data-stu-id="d33ea-116">If each frame reconstruction took .01 second, the seek would take almost 3 seconds.</span></span> <span data-ttu-id="d33ea-117">Si vous souhaitez augmenter l’efficacité de la recherche, il peut être utile de réduire l’espacement entre les images clés.</span><span class="sxs-lookup"><span data-stu-id="d33ea-117">If you want to increase the efficiency of seeking, lowering the key-frame spacing can help.</span></span> <span data-ttu-id="d33ea-118">Toutefois, si vous définissez les images clés trop près, vous risquez de perdre la qualité.</span><span class="sxs-lookup"><span data-stu-id="d33ea-118">However, if you set the key frames too close together, you can lose quality.</span></span>

<span data-ttu-id="d33ea-119">Vous pouvez définir l’espacement maximal de l’image clé en appelant [**IWMVideoMediaProps :: SetMaxKeyFrameSpacing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing).</span><span class="sxs-lookup"><span data-stu-id="d33ea-119">You can set the maximum key-frame spacing by calling [**IWMVideoMediaProps::SetMaxKeyFrameSpacing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing).</span></span> <span data-ttu-id="d33ea-120">Les valeurs recommandées, basées sur la vitesse de transmission du flux, sont répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d33ea-120">The recommended values, based on the bit rate of the stream, are listed in the following table.</span></span> <span data-ttu-id="d33ea-121">Ces valeurs fournissent un bon compromis entre les performances et la qualité.</span><span class="sxs-lookup"><span data-stu-id="d33ea-121">These values provide a good balance of seeking performance and quality.</span></span> <span data-ttu-id="d33ea-122">Le kit de développement logiciel (SDK) n’impose aucune limite de temps entre les images clés.</span><span class="sxs-lookup"><span data-stu-id="d33ea-122">The SDK does not enforce any limit on the time between key frames.</span></span> <span data-ttu-id="d33ea-123">En général, les temps de plus de 30 secondes peuvent nuire aux heures de recherche lorsque le contenu est diffusé sur un réseau et lorsqu’il est lu localement.</span><span class="sxs-lookup"><span data-stu-id="d33ea-123">In general, times longer than 30 seconds can adversely affect seek times both when the content is streamed over a network, and when it is played back locally.</span></span>



| <span data-ttu-id="d33ea-124">Vitesse de transmission</span><span class="sxs-lookup"><span data-stu-id="d33ea-124">Bit rate</span></span>             | <span data-ttu-id="d33ea-125">Espace d’image clé maximal suggéré</span><span class="sxs-lookup"><span data-stu-id="d33ea-125">Suggested maximum key-frame spacing</span></span> |
|----------------------|-------------------------------------|
| <span data-ttu-id="d33ea-126">de 22 Kbits/s à 300 Kbits/s</span><span class="sxs-lookup"><span data-stu-id="d33ea-126">22 Kbps to 300 Kbps</span></span>  | <span data-ttu-id="d33ea-127">8 secondes</span><span class="sxs-lookup"><span data-stu-id="d33ea-127">8 seconds</span></span>                           |
| <span data-ttu-id="d33ea-128">300 Kbits/s à 600 kbps</span><span class="sxs-lookup"><span data-stu-id="d33ea-128">300 Kbps to 600 Kbps</span></span> | <span data-ttu-id="d33ea-129">6 secondes</span><span class="sxs-lookup"><span data-stu-id="d33ea-129">6 seconds</span></span>                           |
| <span data-ttu-id="d33ea-130">600 Kbits/s à 2 Mbits/s</span><span class="sxs-lookup"><span data-stu-id="d33ea-130">600 Kbps to 2 Mbps</span></span>   | <span data-ttu-id="d33ea-131">4 secondes</span><span class="sxs-lookup"><span data-stu-id="d33ea-131">4 seconds</span></span>                           |
| <span data-ttu-id="d33ea-132">2 Mbits/s et plus</span><span class="sxs-lookup"><span data-stu-id="d33ea-132">2 Mbps and higher</span></span>    | <span data-ttu-id="d33ea-133">3 secondes</span><span class="sxs-lookup"><span data-stu-id="d33ea-133">3 seconds</span></span>                           |



 

<span data-ttu-id="d33ea-134">Pour plus d’informations sur l’obtention des meilleures performances lors de la recherche de fichiers vidéo, consultez [obtention de meilleures performances de recherche de vidéos](getting-the-best-video-seeking-performance.md).</span><span class="sxs-lookup"><span data-stu-id="d33ea-134">For more information about getting the best performance when seeking video files, see [Getting the Best Video Seeking Performance](getting-the-best-video-seeking-performance.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d33ea-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d33ea-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d33ea-136">**Configuration de flux**</span><span class="sxs-lookup"><span data-stu-id="d33ea-136">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




