---
title: Exemples de types d’extension
description: Exemples de types d’extension
ms.assetid: 8de2e003-cb21-4be9-bcde-7f5909b6260a
keywords:
- Windows Media Format SDK, exemples d’extensions
- ASF (Advanced Systems Format), exemples d’extensions
- ASF (Advanced Systems Format), exemples d’extensions
- Windows Media Format SDK, Data Unit extensions
- ASF (Advanced Systems Format), extensions d’unité de données
- ASF (format de systèmes avancés), extensions d’unité de données
- Windows Media Format SDK, propriétés de mémoire tampon
- ASF (Advanced Systems Format), propriétés de mémoire tampon
- ASF (format de systèmes avancés), propriétés de mémoire tampon
- exemples d’extensions, types
- extensions d’unité de données, types
- Propriétés de la mémoire tampon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972e3da1ecaad277158bb270cc358436f53db9e2
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2020
ms.locfileid: "106509431"
---
# <a name="sample-extension-types"></a><span data-ttu-id="824ef-115">Exemples de types d’extension</span><span class="sxs-lookup"><span data-stu-id="824ef-115">Sample Extension Types</span></span>

<span data-ttu-id="824ef-116">Des exemples d’extensions, également appelées « extensions d’unité de données » (cotisations) ou des propriétés de mémoire tampon, sont des éléments de données attachés aux exemples de média dans la section données du fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="824ef-116">Sample extensions, also called data unit extensions (DUEs) or buffer properties, are items of data that are attached to the media samples in the data section of the ASF file.</span></span> <span data-ttu-id="824ef-117">Plusieurs types d’exemples d’extensions sont définis dans le kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="824ef-117">Several types of sample extensions are defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="824ef-118">Vous pouvez également créer vos propres types d’extensions.</span><span class="sxs-lookup"><span data-stu-id="824ef-118">You can also create your own extension types.</span></span>

<span data-ttu-id="824ef-119">Pour utiliser des exemples d’extensions, vous devez identifier le type d’extension dans les données de configuration de flux du profil.</span><span class="sxs-lookup"><span data-stu-id="824ef-119">To use sample extensions, you must identify the extension type in the stream configuration data of the profile.</span></span> <span data-ttu-id="824ef-120">Appelez la méthode [**IWMStreamConfig2 :: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) pour configurer un flux afin d’accepter des exemples avec des données étendues.</span><span class="sxs-lookup"><span data-stu-id="824ef-120">Call the [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) method to configure a stream to accept samples with extended data.</span></span>

<span data-ttu-id="824ef-121">Des exemples d’extensions individuelles doivent être ajoutés aux exemples d’entrée en appelant la méthode [**INSSBuffer3 :: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="824ef-121">Individual sample extensions must be added to the input samples by calling the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method.</span></span> <span data-ttu-id="824ef-122">Lors de la lecture des exemples, vous pouvez appeler la méthode [**INSSBuffer3 :: GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) pour récupérer les données d’extension.</span><span class="sxs-lookup"><span data-stu-id="824ef-122">When reading samples, you can call the [**INSSBuffer3::GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) method to retrieve the extension data.</span></span> <span data-ttu-id="824ef-123">Vous pouvez également utiliser les méthodes de l’interface [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) pour énumérer les extensions d’unité de données jointes à un exemple.</span><span class="sxs-lookup"><span data-stu-id="824ef-123">You can also use the methods of the [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) interface to enumerate the data unit extensions attached to a sample.</span></span>

<span data-ttu-id="824ef-124">Le tableau suivant répertorie les identificateurs d’extension d’unité de données prédéfinis, et décrit les données jointes aux exemples pour chacune d’elles.</span><span class="sxs-lookup"><span data-stu-id="824ef-124">The following table lists the predefined data unit extension identifiers, and describes the data that is attached to samples for each.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="824ef-125">Exemple de GUID d’extension</span><span class="sxs-lookup"><span data-stu-id="824ef-125">Sample extension GUID</span></span></th>
<th><span data-ttu-id="824ef-126">Description</span><span class="sxs-lookup"><span data-stu-id="824ef-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="824ef-127">WM_SampleExtensionGUID_OutputCleanPoint</span><span class="sxs-lookup"><span data-stu-id="824ef-127">WM_SampleExtensionGUID_OutputCleanPoint</span></span></td>
<td><span data-ttu-id="824ef-128">Les données indiquent si l’échantillon est un <a href="wmformat-glossary.md"><em>Cleanpoint</em></a>.</span><span class="sxs-lookup"><span data-stu-id="824ef-128">The data indicates whether the sample is a <a href="wmformat-glossary.md"><em>cleanpoint</em></a>.</span></span> <span data-ttu-id="824ef-129">La valeur zéro indique que l’exemple n’est pas un Cleanpoint.</span><span class="sxs-lookup"><span data-stu-id="824ef-129">A value of zero indicates that the sample is not a cleanpoint.</span></span> <span data-ttu-id="824ef-130">Une valeur différente de zéro indique qu’il s’agit d’un Cleanpoint.</span><span class="sxs-lookup"><span data-stu-id="824ef-130">A non-zero value indicates that it is a cleanpoint.</span></span> <span data-ttu-id="824ef-131">Cet exemple de type d’extension d’unité de données (DUE) est utilisé pour effectuer le suivi des cleanpoints lors de l’écriture de flux de données multimédias précompressés qui ont été encodés avec des codecs tiers.</span><span class="sxs-lookup"><span data-stu-id="824ef-131">This sample data unit extension (DUE) type is used to keep track of cleanpoints when writing precompressed media streams that were encoded with third-party codecs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="824ef-132">WM_SampleExtensionGUID_Timecode</span><span class="sxs-lookup"><span data-stu-id="824ef-132">WM_SampleExtensionGUID_Timecode</span></span></td>
<td><span data-ttu-id="824ef-133">Les données sont une structure <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> contenant les données de code horaire SMPTE associées à l’exemple. La taille de cet échéance est toujours WM_SampleExtension_Timecode_Size, soit 14 octets.</span><span class="sxs-lookup"><span data-stu-id="824ef-133">The data is a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> structure containing SMPTE time code data associated with the sample.The size for this DUE is always WM_SampleExtension_Timecode_Size, which is 14 bytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="824ef-134">WM_SampleExtensionGUID_FileName</span><span class="sxs-lookup"><span data-stu-id="824ef-134">WM_SampleExtensionGUID_FileName</span></span></td>
<td><span data-ttu-id="824ef-135">Ce type d’exemple d’extension est utilisé pour les flux de fichiers.</span><span class="sxs-lookup"><span data-stu-id="824ef-135">This type of sample extension is used for file streams.</span></span> <span data-ttu-id="824ef-136">Les données d’un exemple de flux de fichier sont une partie d’un fichier de données.</span><span class="sxs-lookup"><span data-stu-id="824ef-136">The data in a file stream sample is a piece of a data file.</span></span> <span data-ttu-id="824ef-137">Les données de l’exemple d’extension spécifient le nom du fichier à partir duquel le contenu de l’échantillon a été pris. Le nom de fichier est une chaîne de caractères larges contenant le nom de fichier au format name. extension sans aucune information de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="824ef-137">The data in the sample extension specifies the name of the file from which the content in the sample was taken.The file name is a wide-character string containing the file name in name.extension format without any path information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="824ef-138">WM_SampleExtensionGUID_ContentType</span><span class="sxs-lookup"><span data-stu-id="824ef-138">WM_SampleExtensionGUID_ContentType</span></span></td>
<td><span data-ttu-id="824ef-139">Les données identifient le type de contenu que l’exemple contient.</span><span class="sxs-lookup"><span data-stu-id="824ef-139">The data identifies the type of content that the sample contains.</span></span> <span data-ttu-id="824ef-140">Ce type d’exemple d’extension est utilisé avec les flux vidéo entrelacés. Tout le contenu entrelacé utilise l’indicateur WM_CT_INTERLACED combiné par <strong>une opération or au niveau</strong> du bit avec WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST ou WM_CT_REPEAT_FIRST_FIELD.</span><span class="sxs-lookup"><span data-stu-id="824ef-140">This type of sample extension is used with interlaced video streams.All interlaced content uses the WM_CT_INTERLACED flag combined by a bitwise <strong>OR</strong> with either WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST, or WM_CT_REPEAT_FIRST_FIELD.</span></span><br/> <span data-ttu-id="824ef-141">L’ordre des champs n’est pas utilisé dans le processus d’encodage, mais est conservé avec les exemples compressés pour pouvoir être transmis au matériel de rendu.</span><span class="sxs-lookup"><span data-stu-id="824ef-141">The field order is not used in the encoding process, but is maintained with the compressed samples so that it can be passed to the rendering hardware.</span></span> <span data-ttu-id="824ef-142">La diffusion de contenu entrelacé avec un ordre de champ incorrect présente des artefacts tels que le bougé de mouvement dans la vidéo.</span><span class="sxs-lookup"><span data-stu-id="824ef-142">Playing interlaced content with the incorrect field order introduces artifacts such as motion jitter in the video.</span></span><br/> <span data-ttu-id="824ef-143">La taille de cet échéance est toujours WM_SampleExtension_ContentType_Size.</span><span class="sxs-lookup"><span data-stu-id="824ef-143">The size for this DUE is always WM_SampleExtension_ContentType_Size.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="824ef-144">WM_SampleExtensionGUID_PixelAspectRatio</span><span class="sxs-lookup"><span data-stu-id="824ef-144">WM_SampleExtensionGUID_PixelAspectRatio</span></span></td>
<td><span data-ttu-id="824ef-145">Les données indiquent les proportions de pixels du contenu de l’échantillon.</span><span class="sxs-lookup"><span data-stu-id="824ef-145">The data indicates the pixel aspect ratio of the content in the sample.</span></span> <span data-ttu-id="824ef-146">Cela s’applique uniquement à la vidéo. Ce type d’extension est utilisé pour identifier les proportions des pixels non carrés.</span><span class="sxs-lookup"><span data-stu-id="824ef-146">This applies only to video.This extension type is used to identify the aspect ratio of non-square pixels.</span></span> <span data-ttu-id="824ef-147">Pour plus d’informations, consultez <a href="to-read-and-write-video-streams-with-non-square-pixels.md">pour lire et écrire des flux vidéo avec des pixels non carrés</a>.</span><span class="sxs-lookup"><span data-stu-id="824ef-147">For more information, see <a href="to-read-and-write-video-streams-with-non-square-pixels.md">To Read and Write Video Streams with Non-Square Pixels</a>.</span></span><br/> <span data-ttu-id="824ef-148">Les valeurs de proportions sont stockées sous la forme d’un mot dont l’octet de poids faible est l’aspect X et dont l’octet de poids fort est l’aspect Y.</span><span class="sxs-lookup"><span data-stu-id="824ef-148">Aspect ratio values are stored as a word whose low byte is the X aspect and whose high byte is the Y aspect.</span></span> <span data-ttu-id="824ef-149">Par exemple, 16:9 est stocké en tant que 0x0910.</span><span class="sxs-lookup"><span data-stu-id="824ef-149">For example, 16:9 is stored as 0x0910.</span></span><br/> <span data-ttu-id="824ef-150">La taille de cet échéance est toujours WM_SampleExtension_PixelAspectRatio_Size, soit 2 octets.</span><span class="sxs-lookup"><span data-stu-id="824ef-150">The size for this DUE is always WM_SampleExtension_PixelAspectRatio_Size, which is 2 bytes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="824ef-151">WM_SampleExtensionGUID_SampleDuration</span><span class="sxs-lookup"><span data-stu-id="824ef-151">WM_SampleExtensionGUID_SampleDuration</span></span></td>
<td><span data-ttu-id="824ef-152">Les données indiquent la durée, en millisecondes, de l’échantillon contenu dans l’objet buffer.</span><span class="sxs-lookup"><span data-stu-id="824ef-152">The data indicates the duration, in milliseconds, of the sample contained in the buffer object.</span></span> <span data-ttu-id="824ef-153">Lors de la lecture, si cette raison est définie, l’objet lecteur l’utilise pour remplacer la valeur de durée d’exemple existante. Cette échéance est définie automatiquement par les composants d’exécution du kit de développement logiciel (SDK) sur les flux vidéo avec des vitesses de transmission de 100 Kbits/s ou plus, où la surcharge des informations en attente n’est pas significative.</span><span class="sxs-lookup"><span data-stu-id="824ef-153">On playback, if this DUE is set the reader object will use it to overwrite the existing sample duration value.This DUE is set automatically by the SDK run-time components on video streams with bit rates of 100 kbps or greater, where the overhead of the DUE information is not significant.</span></span> <span data-ttu-id="824ef-154">Elle n’est pas définie pour les flux avec des vitesses de transmission inférieures à 100 Kbits/s.</span><span class="sxs-lookup"><span data-stu-id="824ef-154">It is not set for streams with bit rates under 100 kbps.</span></span> <span data-ttu-id="824ef-155">Les applications ne doivent pas définir cette raison manuellement, car le rédacteur (sur des flux à débit élevé) remplacera la valeur par ses propres données.</span><span class="sxs-lookup"><span data-stu-id="824ef-155">Applications should not set this DUE manually because the writer (on high-bit-rate streams) will overwrite the value with its own data.</span></span><br/> <span data-ttu-id="824ef-156">La taille de cet échéance est toujours WM_SampleExtension_SampleDuration_Size, soit 2 octets.</span><span class="sxs-lookup"><span data-stu-id="824ef-156">The size for this DUE is always WM_SampleExtension_SampleDuration_Size, which is 2 bytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="824ef-157">WM_SampleExtensionGUID_ChromaLocation</span><span class="sxs-lookup"><span data-stu-id="824ef-157">WM_SampleExtensionGUID_ChromaLocation</span></span></td>
<td><span data-ttu-id="824ef-158">Les données indiquent le type de sous-échantillonnage de chrominance utilisé dans le format vidéo I420. La valeur de cette extension est définie sur l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="824ef-158">The data indicates the type of chroma subsampling used in the I420 video format.The value of this extension is set to one of the follow values:</span></span><br/>
<ul>
<li><span data-ttu-id="824ef-159">WM_CL_INTERLACED420</span><span class="sxs-lookup"><span data-stu-id="824ef-159">WM_CL_INTERLACED420</span></span></li>
<li><span data-ttu-id="824ef-160">WM_CL_PROGRESSIVE420</span><span class="sxs-lookup"><span data-stu-id="824ef-160">WM_CL_PROGRESSIVE420</span></span></li>
</ul>
<span data-ttu-id="824ef-161">Cette extension d’unité de données n’est pas configurée dans le profil.</span><span class="sxs-lookup"><span data-stu-id="824ef-161">This data unit extension is not configured in the profile.</span></span> <span data-ttu-id="824ef-162">Elle est incluse dans les exemples de sortie du décodeur.</span><span class="sxs-lookup"><span data-stu-id="824ef-162">It is included in samples output from the decoder.</span></span><br/> <span data-ttu-id="824ef-163">La taille de cet échéance est toujours WM_SampleExtension_ChromaLocation_Size, soit 1 octet.</span><span class="sxs-lookup"><span data-stu-id="824ef-163">The size of this DUE is always WM_SampleExtension_ChromaLocation_Size, which is 1 byte.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="824ef-164">WM_SampleExtensionGUID_ColorSpaceInfo</span><span class="sxs-lookup"><span data-stu-id="824ef-164">WM_SampleExtensionGUID_ColorSpaceInfo</span></span></td>
<td><span data-ttu-id="824ef-165">Les données fournissent des informations sur l’espace colorimétrique utilisé pour la trame vidéo actuelle. La valeur de cette extension est une structure <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="824ef-165">The data provides information about the color space used for the current video frame.The value of this extension is a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> structure.</span></span><br/> <span data-ttu-id="824ef-166">Cette extension d’unité de données n’est pas configurée dans le profil.</span><span class="sxs-lookup"><span data-stu-id="824ef-166">This data unit extension is not configured in the profile.</span></span> <span data-ttu-id="824ef-167">Elle est incluse dans les exemples de sortie du décodeur.</span><span class="sxs-lookup"><span data-stu-id="824ef-167">It is included in samples output from the decoder.</span></span><br/> <span data-ttu-id="824ef-168">La taille de cet échéance est toujours WM_SampleExtension_ColorSpaceInfo_Size, soit 3 octets.</span><span class="sxs-lookup"><span data-stu-id="824ef-168">The size of this DUE is always WM_SampleExtension_ColorSpaceInfo_Size, which is 3 bytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="824ef-169">WM_SampleExtensionGUID_UserDataInfo</span><span class="sxs-lookup"><span data-stu-id="824ef-169">WM_SampleExtensionGUID_UserDataInfo</span></span></td>
<td><span data-ttu-id="824ef-170">Les données sont des données utilisateur personnalisées. Les quatre premiers octets des données contiennent la taille des données personnalisées.</span><span class="sxs-lookup"><span data-stu-id="824ef-170">The data is custom user data.The first four bytes of the data contain the size of the custom data.</span></span><br/> <span data-ttu-id="824ef-171">L’octet suivant contient le type de données utilisateur fourni dans l’exemple d’extension.</span><span class="sxs-lookup"><span data-stu-id="824ef-171">The next byte contains the type of user data provided in the sample extension.</span></span> <span data-ttu-id="824ef-172">Les types suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="824ef-172">The following types are supported:</span></span><br/>
<ul>
<li><span data-ttu-id="824ef-173">0x1F-données utilisateur au niveau de la séquence</span><span class="sxs-lookup"><span data-stu-id="824ef-173">0x1F - Sequence level user data</span></span></li>
<li><span data-ttu-id="824ef-174">0x1E-données utilisateur de niveau de point d’entrée</span><span class="sxs-lookup"><span data-stu-id="824ef-174">0x1E - Entry-point level user data</span></span></li>
<li><span data-ttu-id="824ef-175">0x1D-données utilisateur au niveau de la trame</span><span class="sxs-lookup"><span data-stu-id="824ef-175">0x1D - Frame level user data</span></span></li>
<li><span data-ttu-id="824ef-176">0x1C-données utilisateur au niveau du champ</span><span class="sxs-lookup"><span data-stu-id="824ef-176">0x1C - Field level user data</span></span></li>
<li><span data-ttu-id="824ef-177">0x1B-données utilisateur au niveau de la tranche</span><span class="sxs-lookup"><span data-stu-id="824ef-177">0x1B - Slice level user data</span></span></li>
</ul>
<span data-ttu-id="824ef-178">Le sixième octets et les suivants contiennent les données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="824ef-178">The sixth and subsequent bytes contain the user data.</span></span> <span data-ttu-id="824ef-179">Il y a autant d’octets de données utilisateur que ceux spécifiés par le nombre dans les quatre premiers octets.</span><span class="sxs-lookup"><span data-stu-id="824ef-179">There are as many bytes of user data as specified by the number in the first four bytes.</span></span><br/> <span data-ttu-id="824ef-180">Cette extension d’unité de données n’est pas configurée dans le profil.</span><span class="sxs-lookup"><span data-stu-id="824ef-180">This data unit extension is not configured in the profile.</span></span> <span data-ttu-id="824ef-181">Il est inclus dans les exemples qui sont générés par le décodeur.</span><span class="sxs-lookup"><span data-stu-id="824ef-181">It is included in samples that are output from the decoder.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="824ef-182">WM_SampleExtensionGUID_SampleProtectionSalt</span><span class="sxs-lookup"><span data-stu-id="824ef-182">WM_SampleExtensionGUID_SampleProtectionSalt</span></span></td>
<td><span data-ttu-id="824ef-183">Les données sont chiffrées par exemple.</span><span class="sxs-lookup"><span data-stu-id="824ef-183">The data is encrypted by sample.</span></span> <span data-ttu-id="824ef-184">Cet exemple de type d’extension est utilisé pour le contenu importé à partir d’un format de fichier non ASF et d’un schéma de protection des droits autre que Windows Media DRM. Lorsque vous importez du contenu protégé, chaque exemple doit inclure un Salt unique.</span><span class="sxs-lookup"><span data-stu-id="824ef-184">This sample extension type is used for content that is imported from a non-ASF file format and a rights protection scheme other than Windows Media DRM.When importing protected content, each sample must include a unique salt.</span></span> <span data-ttu-id="824ef-185">En général, cette valeur est un compteur à croissance monotone.</span><span class="sxs-lookup"><span data-stu-id="824ef-185">Typically, this value is a monotonically increasing counter.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="824ef-186">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="824ef-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="824ef-187">**Guide de référence de programmation**</span><span class="sxs-lookup"><span data-stu-id="824ef-187">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 





