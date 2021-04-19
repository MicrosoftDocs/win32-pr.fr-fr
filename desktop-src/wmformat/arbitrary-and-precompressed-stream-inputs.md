---
title: Entrées de flux arbitraires et précompressés
description: Entrées de flux arbitraires et précompressés
ms.assetid: 6debbae5-0c54-48db-9ef8-f84f74e2f090
keywords:
- ASF (Advanced Systems Format), entrées de flux arbitraires
- ASF (format de systèmes avancés), entrées de flux arbitraires
- profils, entrées de flux arbitraires
- codecs, entrées de flux arbitraires
- ASF (Advanced Systems Format), entrées de flux précompressées
- ASF (format des systèmes avancés), entrées de flux précompressées
- profils, entrées de flux précompressés
- codecs, entrées de flux précompressés
- entrées de flux précompressées
- entrées de flux arbitraires
- flux, entrées de flux arbitraires
- flux, entrées de flux précompressées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe1c95fe992c7638ac923ac07ce159fb5dc4126
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "106513514"
---
# <a name="arbitrary-and-precompressed-stream-inputs"></a><span data-ttu-id="1f8df-115">Entrées de flux arbitraires et précompressés</span><span class="sxs-lookup"><span data-stu-id="1f8df-115">Arbitrary and Precompressed Stream Inputs</span></span>

<span data-ttu-id="1f8df-116">Seules les entrées qui doivent être compressées par l’un des codecs Windows Media ont plusieurs entrées possibles.</span><span class="sxs-lookup"><span data-stu-id="1f8df-116">Only inputs that are to be compressed by one of the Windows Media codecs have multiple possible inputs.</span></span> <span data-ttu-id="1f8df-117">Les autres types d’entrées possibles sont les entrées arbitraires et les entrées précompressées.</span><span class="sxs-lookup"><span data-stu-id="1f8df-117">The other types of possible inputs are arbitrary inputs and precompressed inputs.</span></span> <span data-ttu-id="1f8df-118">La configuration requise pour les formats d’entrée pour ces types est décrite dans cette section.</span><span class="sxs-lookup"><span data-stu-id="1f8df-118">The requirements for input formats for these types are described in this section.</span></span>

## <a name="arbitrary-stream-inputs"></a><span data-ttu-id="1f8df-119">Entrées de flux arbitraires</span><span class="sxs-lookup"><span data-stu-id="1f8df-119">Arbitrary Stream Inputs</span></span>

<span data-ttu-id="1f8df-120">Les entrées des types de flux arbitraires sont les mêmes que les formats de flux décrits dans le profil.</span><span class="sxs-lookup"><span data-stu-id="1f8df-120">Inputs for arbitrary stream types are the same as the stream formats described in the profile.</span></span> <span data-ttu-id="1f8df-121">Vous ne devez pas avoir à définir des formats d’entrée pour ces types.</span><span class="sxs-lookup"><span data-stu-id="1f8df-121">You should not have to set input formats for these types.</span></span>

## <a name="precompressed-stream-inputs"></a><span data-ttu-id="1f8df-122">Entrées de flux précompressées</span><span class="sxs-lookup"><span data-stu-id="1f8df-122">Precompressed Stream Inputs</span></span>

<span data-ttu-id="1f8df-123">Lors de la copie d’un flux d’un fichier vers un autre, vous transmettez des exemples qui sont déjà compressés.</span><span class="sxs-lookup"><span data-stu-id="1f8df-123">When copying a stream from one file to another, you pass samples that are already compressed.</span></span> <span data-ttu-id="1f8df-124">Dans ce cas, vous devez affecter la **valeur null** à l’objet de propriétés d’entrée pour informer le writer qu’il n’a pas besoin de valider les données que vous passez.</span><span class="sxs-lookup"><span data-stu-id="1f8df-124">In this case, you must set the input properties object to **NULL** to inform the writer that it does not need to validate the data you are passing in.</span></span> <span data-ttu-id="1f8df-125">Pour définir le format d’entrée sur **null**, appelez [**IWMWriter :: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) et transmettez **null** comme deuxième paramètre.</span><span class="sxs-lookup"><span data-stu-id="1f8df-125">To set the input format to **NULL**, call [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) and pass **NULL** as the second parameter.</span></span> <span data-ttu-id="1f8df-126">Lors de l’appel de cette méthode avec un paramètre **null** , vous devez effectuer l’appel avant d’appeler [**BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="1f8df-126">When calling this method with a **NULL** parameter, you must make the call before calling [**BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

<span data-ttu-id="1f8df-127">Lorsque vous utilisez des flux précompressés, vous devez copier manuellement les informations du codec dans l’en-tête du fichier avant d’écrire.</span><span class="sxs-lookup"><span data-stu-id="1f8df-127">When using precompressed streams, you must manually copy codec information to the file header before writing.</span></span> <span data-ttu-id="1f8df-128">Pour obtenir les informations du codec, appelez [**IWMHeaderInfo2 :: GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) et [**IWMHeaderInfo2 :: GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) pour énumérer les codecs associés au fichier dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="1f8df-128">To obtain the codec information, call [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) and [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) to enumerate the codecs associated with the file in the reader.</span></span> <span data-ttu-id="1f8df-129">Sélectionnez les informations du codec qui correspondent à la configuration du flux du flux précompressé.</span><span class="sxs-lookup"><span data-stu-id="1f8df-129">Select the codec information that matches the stream configuration of the precompressed stream.</span></span> <span data-ttu-id="1f8df-130">Définissez ensuite les informations du codec dans le writer en appelant [**IWMHeaderInfo3 :: AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), en passant les informations obtenues à partir du lecteur.</span><span class="sxs-lookup"><span data-stu-id="1f8df-130">Then set the codec information in the writer by calling [**IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passing the information obtained from the reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f8df-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1f8df-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f8df-132">**Utilisation des entrées**</span><span class="sxs-lookup"><span data-stu-id="1f8df-132">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




