---
title: Configuration de flux vidéo
description: Configuration de flux vidéo
ms.assetid: caffdfc1-3c35-4b7b-8643-5a9095cc11f6
keywords:
- flux, configuration de flux vidéo
- codecs, configuration des flux vidéo
- flux vidéo, configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d2389026dc1061064c5e687da60c3350ad94a4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106512082"
---
# <a name="configuring-video-streams"></a><span data-ttu-id="3effe-106">Configuration de flux vidéo</span><span class="sxs-lookup"><span data-stu-id="3effe-106">Configuring Video Streams</span></span>

<span data-ttu-id="3effe-107">Les flux vidéo sont plus flexibles dans leur configuration que les flux audio.</span><span class="sxs-lookup"><span data-stu-id="3effe-107">Video streams are more flexible in their configuration than audio streams.</span></span> <span data-ttu-id="3effe-108">Cela est dû au fait que les propriétés des frames qui composent la vidéo peuvent varier considérablement d’un fichier à l’autre.</span><span class="sxs-lookup"><span data-stu-id="3effe-108">This is because the properties of the frames that make up the video can vary widely from one file to the next.</span></span> <span data-ttu-id="3effe-109">Lorsque vous récupérez le format de codec du codec que vous utilisez, vous devez définir les valeurs suivantes pour les objets de configuration de flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="3effe-109">When you retrieve the codec format for the codec you are using, you must set the following values for video stream configuration objects.</span></span>



| <span data-ttu-id="3effe-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="3effe-110">Value</span></span>                                 | <span data-ttu-id="3effe-111">Description</span><span class="sxs-lookup"><span data-stu-id="3effe-111">Description</span></span>                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3effe-112">Vitesse de transmission</span><span class="sxs-lookup"><span data-stu-id="3effe-112">Bit rate</span></span>                              | <span data-ttu-id="3effe-113">Appelez [**IWMStreamConfig :: SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) pour définir la valeur souhaitée.</span><span class="sxs-lookup"><span data-stu-id="3effe-113">Call [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) to set to the desired value.</span></span> <span data-ttu-id="3effe-114">Le codec vidéo essaiera de compresser le média pour répondre à vos spécifications.</span><span class="sxs-lookup"><span data-stu-id="3effe-114">The video codec will try to compress the media to meet your specifications.</span></span> <span data-ttu-id="3effe-115">Si vos valeurs sont trop basses, la vidéo compressée obtenue sera très détériorée.</span><span class="sxs-lookup"><span data-stu-id="3effe-115">If your values are too low, the resulting compressed video will be very degraded.</span></span>           |
| <span data-ttu-id="3effe-116">Fenêtre de mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="3effe-116">Buffer window</span></span>                         | <span data-ttu-id="3effe-117">Appelez [**IWMStreamConfig :: SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) pour définir la valeur souhaitée.</span><span class="sxs-lookup"><span data-stu-id="3effe-117">Call [**IWMStreamConfig::SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) to set to the desired value.</span></span> <span data-ttu-id="3effe-118">Le codec vidéo essaiera de compresser le média pour répondre à vos spécifications.</span><span class="sxs-lookup"><span data-stu-id="3effe-118">The video codec will try to compress the media to meet your specifications.</span></span> <span data-ttu-id="3effe-119">Si vos valeurs sont trop basses, la vidéo compressée obtenue sera très détériorée.</span><span class="sxs-lookup"><span data-stu-id="3effe-119">If your values are too low, the resulting compressed video will be very degraded.</span></span> |
| <span data-ttu-id="3effe-120">**WMVIDEOINFOHEADER.rcSource**</span><span class="sxs-lookup"><span data-stu-id="3effe-120">**WMVIDEOINFOHEADER.rcSource**</span></span>        | <span data-ttu-id="3effe-121">L’angle supérieur gauche doit avoir la valeur 0, 0.</span><span class="sxs-lookup"><span data-stu-id="3effe-121">The upper left corner must be set to 0,0.</span></span> <span data-ttu-id="3effe-122">L’angle inférieur droit doit être défini sur les dimensions du cadre.</span><span class="sxs-lookup"><span data-stu-id="3effe-122">The lower right corner must be set to the frame dimensions.</span></span> <span data-ttu-id="3effe-123">Par exemple, dans un flux de 640 x 480, ces paramètres sont 0, 0640480.</span><span class="sxs-lookup"><span data-stu-id="3effe-123">For example, in a 640x480 stream, these settings would be 0,0,640,480.</span></span>                                                                                                |
| <span data-ttu-id="3effe-124">**WMVIDEOINFOHEADER.rcTarget**</span><span class="sxs-lookup"><span data-stu-id="3effe-124">**WMVIDEOINFOHEADER.rcTarget**</span></span>        | <span data-ttu-id="3effe-125">Doit correspondre à **rcSource**.</span><span class="sxs-lookup"><span data-stu-id="3effe-125">Must match **rcSource**.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="3effe-126">**WMVIDEOINFOHEADER.dwBitRate**</span><span class="sxs-lookup"><span data-stu-id="3effe-126">**WMVIDEOINFOHEADER.dwBitRate**</span></span>       | <span data-ttu-id="3effe-127">Doit correspondre à la vitesse de transmission définie pour le flux.</span><span class="sxs-lookup"><span data-stu-id="3effe-127">Must match the bit rate set for the stream.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="3effe-128">**WMVIDEOINFOHEADER. AvgTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="3effe-128">**WMVIDEOINFOHEADER.AvgTimePerFrame**</span></span> | <span data-ttu-id="3effe-129">Définissez sur le temps approximatif par cadre.</span><span class="sxs-lookup"><span data-stu-id="3effe-129">Set to the approximate time per frame.</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="3effe-130">**BITMAPINFOHEADER. bichasse**</span><span class="sxs-lookup"><span data-stu-id="3effe-130">**BITMAPINFOHEADER.biWidth**</span></span>          | <span data-ttu-id="3effe-131">Définissez sur la largeur, en pixels, de la taille de frame souhaitée.</span><span class="sxs-lookup"><span data-stu-id="3effe-131">Set to the width, in pixels, of the desired frame size.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="3effe-132">**BITMAPINFOHEADER. bihauteur**</span><span class="sxs-lookup"><span data-stu-id="3effe-132">**BITMAPINFOHEADER.biHeight**</span></span>         | <span data-ttu-id="3effe-133">Définissez sur la hauteur, en pixels, de la taille de trame souhaitée.</span><span class="sxs-lookup"><span data-stu-id="3effe-133">Set to the height, in pixels, of the desired frame size.</span></span>                                                                                                                                                                                                                    |



 

<span data-ttu-id="3effe-134">Le contenu vidéo ne s’exécute pas correctement, sauf s’il est encodé à une taille qui est un multiple de quatre pour la largeur et la hauteur.</span><span class="sxs-lookup"><span data-stu-id="3effe-134">Video content does not play correctly unless it is encoded to a size that is a multiple of four for both width and height.</span></span> <span data-ttu-id="3effe-135">L’exception est une vidéo [*RGB*](wmformat-glossary.md) non compressée, qui peut avoir n’importe quelle taille.</span><span class="sxs-lookup"><span data-stu-id="3effe-135">The exception is [*RGB*](wmformat-glossary.md) uncompressed video, which can be any size.</span></span> <span data-ttu-id="3effe-136">Si vous essayez de définir une taille qui n’est pas un multiple de quatre, l’une des erreurs suivantes est retournée par le writer :</span><span class="sxs-lookup"><span data-stu-id="3effe-136">If you try to set a size that is not a multiple of four, one of the following errors will be returned by the writer:</span></span>

-   <span data-ttu-id="3effe-137">\_ \_ \_ format d’entrée NS E non valide \_</span><span class="sxs-lookup"><span data-stu-id="3effe-137">NS\_E\_INVALID\_INPUT\_FORMAT</span></span>
-   <span data-ttu-id="3effe-138">NS \_ E \_ \_ format de sortie non valide \_</span><span class="sxs-lookup"><span data-stu-id="3effe-138">NS\_E\_INVALID\_OUTPUT\_FORMAT</span></span>
-   <span data-ttu-id="3effe-139">\_INVALIDPROFILE NS E \_</span><span class="sxs-lookup"><span data-stu-id="3effe-139">NS\_E\_INVALIDPROFILE</span></span>

<span data-ttu-id="3effe-140">Si vous utilisez un encodage à vitesse de transmission variable, vous devrez peut-être effectuer d’autres ajustements.</span><span class="sxs-lookup"><span data-stu-id="3effe-140">If you are using variable bit rate encoding, you may need to make other adjustments.</span></span> <span data-ttu-id="3effe-141">Pour plus d’informations, consultez [Configuration des flux VBR](configuring-vbr-streams.md).</span><span class="sxs-lookup"><span data-stu-id="3effe-141">For more information, see [Configuring VBR Streams](configuring-vbr-streams.md).</span></span>

<span data-ttu-id="3effe-142">Certains codecs Windows Media Video prennent en charge plusieurs niveaux de complexité.</span><span class="sxs-lookup"><span data-stu-id="3effe-142">Some Windows Media Video codecs support multiple complexity levels.</span></span> <span data-ttu-id="3effe-143">Les niveaux de complexité déterminent les algorithmes qui seront utilisés par le codec lors de l’encodage d’un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="3effe-143">Complexity levels determine the algorithms that the codec will use when encoding a video stream.</span></span> <span data-ttu-id="3effe-144">L’utilisation d’un niveau de complexité élevé nécessitera davantage de puissance de traitement pour l’encodage et le décodage.</span><span class="sxs-lookup"><span data-stu-id="3effe-144">Using a high complexity level will require more processing power for encoding and decoding.</span></span>

<span data-ttu-id="3effe-145">Chaque codec qui prend en charge les paramètres de complexité expose les paramètres suivants que vous pouvez récupérer à l’aide de la méthode [**IWMCodecInfo3 :: GetCodecProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop) .</span><span class="sxs-lookup"><span data-stu-id="3effe-145">Each codec that supports complexity settings exposes the following settings that you can retrieve with the [**IWMCodecInfo3::GetCodecProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop) method.</span></span>



| <span data-ttu-id="3effe-146">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3effe-146">Setting</span></span>                 | <span data-ttu-id="3effe-147">Description</span><span class="sxs-lookup"><span data-stu-id="3effe-147">Description</span></span>                                         |
|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="3effe-148">\_wszComplexityMax g</span><span class="sxs-lookup"><span data-stu-id="3effe-148">g\_wszComplexityMax</span></span>     | <span data-ttu-id="3effe-149">Niveau de qualité maximal pris en charge par le codec.</span><span class="sxs-lookup"><span data-stu-id="3effe-149">The maximum quality level supported by the codec.</span></span>   |
| <span data-ttu-id="3effe-150">\_wszComplexityOffline g</span><span class="sxs-lookup"><span data-stu-id="3effe-150">g\_wszComplexityOffline</span></span> | <span data-ttu-id="3effe-151">Niveau de qualité suggéré pour la lecture hors connexion.</span><span class="sxs-lookup"><span data-stu-id="3effe-151">The suggested quality level for offline playback.</span></span>   |
| <span data-ttu-id="3effe-152">\_wszComplexityLive g</span><span class="sxs-lookup"><span data-stu-id="3effe-152">g\_wszComplexityLive</span></span>    | <span data-ttu-id="3effe-153">Niveau de qualité suggéré pour la lecture en continu.</span><span class="sxs-lookup"><span data-stu-id="3effe-153">The suggested quality level for streaming playback.</span></span> |



 

<span data-ttu-id="3effe-154">Pour définir la complexité d’un flux vidéo dans un profil, utilisez la méthode [**IWMPropertyVault :: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) à l’aide de la propriété g \_ wszComplexity.</span><span class="sxs-lookup"><span data-stu-id="3effe-154">To set the complexity for a video stream in a profile, use the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method using the property g\_wszComplexity.</span></span> <span data-ttu-id="3effe-155">La valeur que vous définissez doit être inférieure ou égale à la complexité maximale prise en charge pour le codec.</span><span class="sxs-lookup"><span data-stu-id="3effe-155">The value you set must be less than or equal to the maximum supported complexity for the codec.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3effe-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3effe-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3effe-157">**Configuration commune à tous les flux**</span><span class="sxs-lookup"><span data-stu-id="3effe-157">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="3effe-158">**Configuration de flux**</span><span class="sxs-lookup"><span data-stu-id="3effe-158">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="3effe-159">**Paramètres de complexité de la vidéo**</span><span class="sxs-lookup"><span data-stu-id="3effe-159">**Video Complexity Settings**</span></span>](video-complexity-settings.md)
</dt> </dl>

 

 




