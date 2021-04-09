---
title: Utilisation d' High-Resolution audio PCM
description: Utilisation d' High-Resolution audio PCM
ms.assetid: 422a78f9-0f43-4edb-acaf-7f6e3f4a1cb8
keywords:
- ASF (Advanced Systems Format), audio PCM haute résolution
- ASF (format de systèmes avancés), audio PCM haute résolution
- profils, audio PCM haute résolution
- codecs, audio PCM haute résolution
- ASF (Advanced Systems Format), audio PCM
- ASF (format des systèmes avancés), audio PCM
- profils, audio PCM
- codecs, audio PCM
- audio PCM haute résolution
- Audio PCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73a45904072307e915065ba3a5946d5ef774c73b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941106"
---
# <a name="working-with-high-resolution-pcm-audio"></a><span data-ttu-id="ef5f4-113">Utilisation d' High-Resolution audio PCM</span><span class="sxs-lookup"><span data-stu-id="ef5f4-113">Working with High-Resolution PCM Audio</span></span>

<span data-ttu-id="ef5f4-114">Certains des formats d’entrée pour le codec Windows Media Audio 9 Professional et le codec Windows Media Audio 9 Lossless sont des formats PCM haute résolution.</span><span class="sxs-lookup"><span data-stu-id="ef5f4-114">Some of the input formats for the Windows Media Audio 9 Professional codec and the Windows Media Audio 9 Lossless codec are high-resolution PCM formats.</span></span> <span data-ttu-id="ef5f4-115">Il s’agit de formats PCM qui ont plus de deux canaux, ou plus de 16 bits par échantillon (l’audio avec plus de deux canaux est également appelé audio multicanal).</span><span class="sxs-lookup"><span data-stu-id="ef5f4-115">These are PCM formats that have more than two channels, or more than 16 bits per sample (audio with more than two channels is also called multichannel audio).</span></span>

<span data-ttu-id="ef5f4-116">Ces formats sont configurés à l’aide d’une extension structurée de la structure [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) , appelée [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ef5f4-116">These formats are configured by using a structured extension of the [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) structure, called [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)).</span></span> <span data-ttu-id="ef5f4-117">La structure **WAVEFORMATEXTENSIBLE** inclut des informations sur les canaux inclus dans l’audio.</span><span class="sxs-lookup"><span data-stu-id="ef5f4-117">The **WAVEFORMATEXTENSIBLE** structure includes information about the channels included in the audio.</span></span> <span data-ttu-id="ef5f4-118">Cette structure est requise lors de l’utilisation de l’audio PCM haute résolution, car certaines API Windows n’acceptent pas les structures **WAVEFORMATEX** qui contiennent des valeurs haute résolution.</span><span class="sxs-lookup"><span data-stu-id="ef5f4-118">This structure is required when using high-resolution PCM audio, because some Windows APIs will not accept **WAVEFORMATEX** structures that contain high-resolution values.</span></span>

<span data-ttu-id="ef5f4-119">Les formats PCM haute résolution comportent 22 octets de données étendues, qui sont spécifiées dans le membre **cbSize** de la structure **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="ef5f4-119">High-resolution PCM formats have 22 bytes of extended data, which is specified in the **cbSize** member of the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="ef5f4-120">Les formats audio Windows Media haute résolution n’utilisent pas la structure **WAVEFORMATEXTENSIBLE** , mais les données étendues sont ajoutées à la structure **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="ef5f4-120">High-resolution Windows Media audio formats do not use the **WAVEFORMATEXTENSIBLE** structure, but do have extended data appended to the **WAVEFORMATEX** structure.</span></span>

<span data-ttu-id="ef5f4-121">Les codecs audio Windows Media prennent uniquement en charge le décodage des formats PCM haute résolution lorsque l’application s’exécute sur Windows XP ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ef5f4-121">The Windows Media audio codecs only support decoding to high-resolution PCM formats when the application is running on Windows XP or later.</span></span> <span data-ttu-id="ef5f4-122">Dans les versions antérieures de Microsoft Windows, les codecs décodent dans un format avec un maximum de 16 bits par échantillon et de 2 canaux.</span><span class="sxs-lookup"><span data-stu-id="ef5f4-122">On previous versions of Microsoft Windows, the codecs decode to a format with a maximum of 16 bits per sample and 2 channels.</span></span> <span data-ttu-id="ef5f4-123">En outre, vous devez spécifier que le codec doit être décodé en PCM haute définition en affectant la \_ **valeur true** au paramètre de sortie g wszEnableDiscreteOutput à l’aide de la méthode [**IWMReaderAdvanced2 :: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) .</span><span class="sxs-lookup"><span data-stu-id="ef5f4-123">In addition, you must specify that you want the codec to decode to high-definition PCM by setting the g\_wszEnableDiscreteOutput output setting to **TRUE** using the [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) method.</span></span> <span data-ttu-id="ef5f4-124">Après avoir effectué cet appel, les sorties énumérées par le lecteur incluent des formats de haute définition.</span><span class="sxs-lookup"><span data-stu-id="ef5f4-124">After making this call, the outputs enumerated by the reader will include high-definition formats.</span></span>

<span data-ttu-id="ef5f4-125">L’audio multicanal nécessite davantage de configuration.</span><span class="sxs-lookup"><span data-stu-id="ef5f4-125">Multichannel audio requires more configuration.</span></span> <span data-ttu-id="ef5f4-126">Pour plus d’informations, consultez lecture de l' [audio multicanal](reading-multichannel-audio.md).</span><span class="sxs-lookup"><span data-stu-id="ef5f4-126">For more information, see [Reading Multichannel Audio](reading-multichannel-audio.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef5f4-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ef5f4-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef5f4-128">**Utilisation des entrées**</span><span class="sxs-lookup"><span data-stu-id="ef5f4-128">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 