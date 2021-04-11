---
title: Objet de propriétés du média de sortie
description: Objet de propriétés du média de sortie
ms.assetid: 96fa7c66-59a0-4eb3-ace4-a827b139f978
keywords:
- Windows Media Format SDK, sortie objets propriétés du média
- ASF (Advanced Systems Format), sortie objets propriétés du média
- ASF (format des systèmes avancés), objets de propriétés de média de sortie
- objets, propriétés du média de sortie objets
- objets de propriétés de média de sortie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61490464381a0b4e58be7994dfaeb0dfec2baa76
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104030936"
---
# <a name="output-media-properties-object"></a><span data-ttu-id="b0b00-108">Objet de propriétés du média de sortie</span><span class="sxs-lookup"><span data-stu-id="b0b00-108">Output Media Properties Object</span></span>

<span data-ttu-id="b0b00-109">Un objet de propriétés de média de sortie est utilisé pour récupérer et définir une propriété de sortie.</span><span class="sxs-lookup"><span data-stu-id="b0b00-109">An output media properties object is used to retrieve and set an output property.</span></span> <span data-ttu-id="b0b00-110">Les objets de propriétés de média de sortie sont créés pour les formats de sortie de flux pris en charge dans un fichier qui est chargé dans un objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="b0b00-110">Output media properties objects are created for supported output formats of streams in a file that is loaded into a reader object.</span></span> <span data-ttu-id="b0b00-111">Pour les flux compressés, les propriétés de sortie sont déterminées par les sorties possibles du codec de décompression.</span><span class="sxs-lookup"><span data-stu-id="b0b00-111">For compressed streams, the output properties are determined by the possible outputs of the decompressing codec.</span></span>

<span data-ttu-id="b0b00-112">Un objet de propriétés de média de sortie est créé par [**IWMReader :: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) cette méthode crée un objet de propriétés de média de sortie qui contient les propriétés du format de sortie par défaut.</span><span class="sxs-lookup"><span data-stu-id="b0b00-112">An output media properties object is created by [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) This method creates an output media properties object that contains the properties of the default output format.</span></span> <span data-ttu-id="b0b00-113">D’autres formats peuvent être pris en charge pour une sortie.</span><span class="sxs-lookup"><span data-stu-id="b0b00-113">Other formats may be supported for an output.</span></span> <span data-ttu-id="b0b00-114">Pour obtenir des formats de sortie supplémentaires, vous pouvez appeler [**IWMReader :: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) pour obtenir le nombre de formats de sortie pris en charge, puis les parcourir à l’aide d’appels à [**IWMReader :: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat).</span><span class="sxs-lookup"><span data-stu-id="b0b00-114">To obtain additional output formats, you can call [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) to get the number of supported output formats and then loop through them using calls to [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat).</span></span> <span data-ttu-id="b0b00-115">**GetOutputFormat** crée un objet de propriétés de média de sortie rempli avec les données pour le format de sortie sélectionné.</span><span class="sxs-lookup"><span data-stu-id="b0b00-115">**GetOutputFormat** creates an output media properties object populated with the data for the selected output format.</span></span>

<span data-ttu-id="b0b00-116">Les objets de propriétés de média de sortie peuvent également être créés avec le lecteur synchrone.</span><span class="sxs-lookup"><span data-stu-id="b0b00-116">Output media properties objects can also be created with the synchronous reader.</span></span> <span data-ttu-id="b0b00-117">Tous les noms de méthode sont identiques à ceux du lecteur et sont tous exposés par l’interface [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) .</span><span class="sxs-lookup"><span data-stu-id="b0b00-117">All of the method names are identical to those in the reader and they are all exposed by the [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) interface.</span></span>

<span data-ttu-id="b0b00-118">**GetOutputProps** et **GetOutputFormat** définissent tous deux un pointeur vers une interface [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) .</span><span class="sxs-lookup"><span data-stu-id="b0b00-118">**GetOutputProps** and **GetOutputFormat** both set a pointer to an [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface.</span></span> <span data-ttu-id="b0b00-119">Les autres interfaces de l’objet de propriétés de média de sortie peuvent être obtenues en appelant la méthode **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="b0b00-119">The other interfaces of the output media properties object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="b0b00-120">Les interfaces suivantes sont prises en charge par chaque objet de propriétés de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="b0b00-120">The following interfaces are supported by every output media properties object.</span></span>



| <span data-ttu-id="b0b00-121">Interface</span><span class="sxs-lookup"><span data-stu-id="b0b00-121">Interface</span></span>                                          | <span data-ttu-id="b0b00-122">Description</span><span class="sxs-lookup"><span data-stu-id="b0b00-122">Description</span></span>                                                                                                |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0b00-123">**IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="b0b00-123">**IWMMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)             | <span data-ttu-id="b0b00-124">Utilisé comme interface de base pour les autres interfaces de propriété de média (entrée, sortie et vidéo).</span><span class="sxs-lookup"><span data-stu-id="b0b00-124">Used as the base interface for the other media-property interfaces (input, output, and video).</span></span>             |
| [<span data-ttu-id="b0b00-125">**IWMOutputMediaProps**</span><span class="sxs-lookup"><span data-stu-id="b0b00-125">**IWMOutputMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) | <span data-ttu-id="b0b00-126">Récupère les propriétés d’une sortie.</span><span class="sxs-lookup"><span data-stu-id="b0b00-126">Retrieves the properties of an output.</span></span>                                                                     |
| [<span data-ttu-id="b0b00-127">**IWMVideoMediaProps**</span><span class="sxs-lookup"><span data-stu-id="b0b00-127">**IWMVideoMediaProps**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops)   | <span data-ttu-id="b0b00-128">Gère les propriétés d’un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="b0b00-128">Manages the properties of a video stream.</span></span> <span data-ttu-id="b0b00-129">Il s’agit d’une interface facultative, disponible uniquement pour les flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="b0b00-129">This is an optional interface, available only for video streams.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b0b00-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b0b00-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0b00-131">**Objets**</span><span class="sxs-lookup"><span data-stu-id="b0b00-131">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="b0b00-132">**Lecteur, objet**</span><span class="sxs-lookup"><span data-stu-id="b0b00-132">**Reader Object**</span></span>](reader-object.md)
</dt> </dl>

 

 




