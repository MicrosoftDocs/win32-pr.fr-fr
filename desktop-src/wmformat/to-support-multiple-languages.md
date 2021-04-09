---
title: Pour prendre en charge plusieurs langues
description: Pour prendre en charge plusieurs langues
ms.assetid: b0061de4-d725-455f-9d9b-5bd0dbe8ff53
keywords:
- Windows Media Format SDK, prenant en charge plusieurs langues
- Windows Media Format SDK, prise en charge de plusieurs langues
- Kit de développement logiciel (SDK) Windows Media format, prise en charge linguistique
- ASF (Advanced Systems Format), prenant en charge plusieurs langues
- ASF (format de systèmes avancés), prenant en charge plusieurs langues
- ASF (Advanced Systems Format), prise en charge de plusieurs langues
- ASF (Advanced Systems Format), prise en charge de plusieurs langues
- ASF (Advanced Systems Format), prise en charge des langues
- ASF (format des systèmes avancés), prise en charge des langues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc070bda1cc25c6b7fd0fa583a8ac63a55fa603
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103940758"
---
# <a name="to-support-multiple-languages"></a><span data-ttu-id="5902f-112">Pour prendre en charge plusieurs langues</span><span class="sxs-lookup"><span data-stu-id="5902f-112">To Support Multiple Languages</span></span>

<span data-ttu-id="5902f-113">Vous pouvez prendre en charge plusieurs langues dans les flux et dans les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="5902f-113">You can support multiple languages both in streams and in metadata.</span></span> <span data-ttu-id="5902f-114">Le cœur de la prise en charge de plusieurs langues dans le kit de développement logiciel (SDK) Windows Media format est l’interface [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) , qui gère une liste des langues prises en charge.</span><span class="sxs-lookup"><span data-stu-id="5902f-114">The core of multiple language support in the Windows Media Format SDK is the [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) interface, which maintains a list of the languages supported.</span></span> <span data-ttu-id="5902f-115">La liste de langues donne à chaque langage pris en charge un index, qui est utilisé dans différents objets du kit de développement logiciel (SDK) lors du traitement de plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="5902f-115">The language list gives each supported language an index, which is used in various objects in the SDK when dealing with the multiple languages.</span></span>

<span data-ttu-id="5902f-116">La méthode [**IWMLanguageList :: AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) ajoute une langue à la liste.</span><span class="sxs-lookup"><span data-stu-id="5902f-116">The [**IWMLanguageList::AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) method adds a language to the list.</span></span> <span data-ttu-id="5902f-117">Vous pouvez identifier les langues déjà présentes dans la liste en obtenant le nombre total de langues avec [**IWMLanguageList :: GetLanguageCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) , puis en parcourant les langages appelant [**IWMLanguageList :: GetLanguageDetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) pour chaque.</span><span class="sxs-lookup"><span data-stu-id="5902f-117">You can identify the languages already in the list by obtaining the total number of languages with [**IWMLanguageList::GetLanguageCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) and then looping through the languages calling [**IWMLanguageList::GetLanguageDetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) for each.</span></span> <span data-ttu-id="5902f-118">L’index de langue est basé sur zéro.</span><span class="sxs-lookup"><span data-stu-id="5902f-118">The language index is zero based.</span></span>

## <a name="to-configure-mutual-exclusion-by-language"></a><span data-ttu-id="5902f-119">Pour configurer l’exclusion mutuelle par langue</span><span class="sxs-lookup"><span data-stu-id="5902f-119">To Configure Mutual Exclusion by Language</span></span>

<span data-ttu-id="5902f-120">La configuration d’un objet d’exclusion mutuelle simple par langue est très simple.</span><span class="sxs-lookup"><span data-stu-id="5902f-120">Configuring a simple mutual exclusion object by language is very simple.</span></span> <span data-ttu-id="5902f-121">Chaque flux est maintenant associé à une langue.</span><span class="sxs-lookup"><span data-stu-id="5902f-121">Each stream is now associated with a language.</span></span> <span data-ttu-id="5902f-122">Le langage associé à un flux peut être défini à l’aide de [**IWMStreamConfig3 :: SetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage).</span><span class="sxs-lookup"><span data-stu-id="5902f-122">The language associated with a stream can be set using [**IWMStreamConfig3::SetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage).</span></span> <span data-ttu-id="5902f-123">Une fois que tous les flux mutuellement exclusifs sont configurés, créez simplement un objet d’exclusion mutuelle comme vous le feriez pour tout autre type.</span><span class="sxs-lookup"><span data-stu-id="5902f-123">After all of the mutually exclusive streams are configured, simply create a mutual exclusion object as you would for any other type.</span></span> <span data-ttu-id="5902f-124">Appelez ensuite [**IWMMutualExclusion :: setType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) en passant \_ \_ le langage WMMUTEX CLSID pour le type.</span><span class="sxs-lookup"><span data-stu-id="5902f-124">Then call [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) passing CLSID\_WMMUTEX\_Language for the type.</span></span>

<span data-ttu-id="5902f-125">Les flux qui s’excluent mutuellement par langue deviennent plus compliqués lorsque les flux exclusifs sont également mutuellement exclusifs par vitesse de transmission.</span><span class="sxs-lookup"><span data-stu-id="5902f-125">Streams that are mutually exclusive by language become more complicated when the exclusive streams are also mutually exclusive by bit rate.</span></span> <span data-ttu-id="5902f-126">Dans ce cas, vous devez utiliser des enregistrements qui s’excluent mutuellement, en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="5902f-126">In this case you must use mutually exclusive records, by performing the following steps:</span></span>

1.  <span data-ttu-id="5902f-127">Créez un objet d’exclusion mutuelle pour les flux de différents débits binaires dans chaque langue.</span><span class="sxs-lookup"><span data-stu-id="5902f-127">Create a mutual exclusion object for the streams of differing bit rates in each language.</span></span> <span data-ttu-id="5902f-128">Pour plus d’informations sur la création d’un objet d’exclusion mutuelle par vitesse de transmission, consultez [utilisation de l’exclusion mutuelle à vitesse de transmission multiple](using-multiple-bit-rate-mutual-exclusion.md).</span><span class="sxs-lookup"><span data-stu-id="5902f-128">For more information about creating a mutual exclusion object by bit rate, see [Using Multiple Bit Rate Mutual Exclusion](using-multiple-bit-rate-mutual-exclusion.md).</span></span>
2.  <span data-ttu-id="5902f-129">Créez un objet d’exclusion mutuelle.</span><span class="sxs-lookup"><span data-stu-id="5902f-129">Create a mutual exclusion object.</span></span> <span data-ttu-id="5902f-130">Appelez [**IWMMutualExclusion :: setType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) et transmettez \_ le \_ langage WMMUTEX CLSID pour spécifier l’exclusivité par langue.</span><span class="sxs-lookup"><span data-stu-id="5902f-130">Call [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) and pass CLSID\_WMMUTEX\_Language to specify exclusivity by language.</span></span>
3.  <span data-ttu-id="5902f-131">Obtenez un pointeur vers l’interface [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) de l’objet exclusion mutuelle créé à l’étape 2 en appelant la méthode **QueryInterface** de [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="5902f-131">Obtain a pointer to the [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) interface of the mutual exclusion object created in step 2 by calling the **QueryInterface** method of [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion).</span></span>
4.  <span data-ttu-id="5902f-132">Appelez la méthode [**IWMMutualExclusion2 :: AddRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) une fois pour chaque langage pour créer des enregistrements de flux qui s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="5902f-132">Call the [**IWMMutualExclusion2::AddRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) method once for each language, to create stream records that will be mutually exclusive.</span></span>
5.  <span data-ttu-id="5902f-133">Pour chaque enregistrement créé à l’étape 4, ajoutez les flux de la langue appropriée avec les appels à [**IWMMutualExclusion2 :: AddStreamForRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord).</span><span class="sxs-lookup"><span data-stu-id="5902f-133">For each record created in step 4, add the streams of the appropriate language with calls to [**IWMMutualExclusion2::AddStreamForRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord).</span></span>

## <a name="to-read-files-with-multiple-languages"></a><span data-ttu-id="5902f-134">Pour lire des fichiers avec plusieurs langues</span><span class="sxs-lookup"><span data-stu-id="5902f-134">To Read Files with Multiple Languages</span></span>

<span data-ttu-id="5902f-135">L’objet Reader fournit des méthodes permettant d’identifier les langages de flux disponibles dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="5902f-135">The reader object provides methods to identify the available languages of streams in a file.</span></span> <span data-ttu-id="5902f-136">Vous pouvez récupérer le nombre de langues prises en charge pour une sortie en appelant [**IWMReaderAdvanced4 :: GetLanguageCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount).</span><span class="sxs-lookup"><span data-stu-id="5902f-136">You can retrieve the number of supported languages for an output by calling [**IWMReaderAdvanced4::GetLanguageCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount).</span></span> <span data-ttu-id="5902f-137">Vous pouvez ensuite récupérer des détails sur chaque langue avec des appels à [**IWMReaderAdvanced4 :: GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage).</span><span class="sxs-lookup"><span data-stu-id="5902f-137">You can then retrieve details about each language with calls to [**IWMReaderAdvanced4::GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage).</span></span>

<span data-ttu-id="5902f-138">Vous pouvez spécifier le langage à lire en passant l’index de cette langue au lecteur avec un appel à [**IWMReaderAdvanced2 :: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span><span class="sxs-lookup"><span data-stu-id="5902f-138">You can specify the language to play by passing the index of that language to the reader with a call to [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span></span> <span data-ttu-id="5902f-139">Cela permet de sélectionner la langue spécifiée tout en conservant la sélection de flux automatique pour tous les autres objets d’exclusion mutuelle dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="5902f-139">This will select the specified language while maintaining automatic stream selection for any other mutual exclusion objects in the file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5902f-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5902f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5902f-141">**Rubriques avancées**</span><span class="sxs-lookup"><span data-stu-id="5902f-141">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="5902f-142">**Interface IWMLanguageList**</span><span class="sxs-lookup"><span data-stu-id="5902f-142">**IWMLanguageList Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist)
</dt> <dt>

[<span data-ttu-id="5902f-143">**Interface IWMMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="5902f-143">**IWMMutualExclusion Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[<span data-ttu-id="5902f-144">**Interface IWMMutualExclusion2**</span><span class="sxs-lookup"><span data-stu-id="5902f-144">**IWMMutualExclusion2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2)
</dt> <dt>

[<span data-ttu-id="5902f-145">**Interface IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="5902f-145">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[<span data-ttu-id="5902f-146">**Interface IWMReaderAdvanced4**</span><span class="sxs-lookup"><span data-stu-id="5902f-146">**IWMReaderAdvanced4 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)
</dt> <dt>

[<span data-ttu-id="5902f-147">**Interface IWMStreamConfig3**</span><span class="sxs-lookup"><span data-stu-id="5902f-147">**IWMStreamConfig3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)
</dt> </dl>

 

 




