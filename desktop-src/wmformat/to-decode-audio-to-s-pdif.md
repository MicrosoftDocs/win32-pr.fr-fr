---
title: Pour décoder l’audio en S/PDIF
description: Pour décoder l’audio en S/PDIF
ms.assetid: b56c2d0a-a7c6-44f8-832a-bbbe7ae053e6
keywords:
- Windows Media Format SDK, décodage audio en S/PDIF
- Windows Media Format SDK, Sony/Philips Digital Interconnect format (S/PDIF)
- ASF (Advanced Systems Format), décodage audio en S/PDIF
- ASF (format de systèmes avancés), décodage audio vers S/PDIF
- ASF (Advanced Systems Format), Sony/Philips Digital Interconnect format (S/PDIF)
- ASF (format de systèmes avancés), Sony/Philips Digital interconnexion (S/PDIF)
- Sony/Philips Digital Interconnect format (S/PDIF), décodage audio
- S/PDIF (format d’interconnexion numérique Sony/Philips), décodage audio
- décodage de l’audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33fa063baa8e9a88c2fb7a4d9c67375965282167
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724103"
---
# <a name="to-decode-audio-to-spdif"></a><span data-ttu-id="09dc0-112">Pour décoder l’audio en S/PDIF</span><span class="sxs-lookup"><span data-stu-id="09dc0-112">To Decode Audio to S/PDIF</span></span>

<span data-ttu-id="09dc0-113">L’encodage audio du codec Windows Media Audio 9 Professional peut être décodé au format S/PDIF de Sony/Philips.</span><span class="sxs-lookup"><span data-stu-id="09dc0-113">Audio encoded with the Windows Media Audio 9 Professional codec can be decoded to Sony/Philips Digital Interconnect Format (S/PDIF).</span></span> <span data-ttu-id="09dc0-114">Pour générer la sortie S/PDIF, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="09dc0-114">To generate S/PDIF output, perform the following steps:</span></span>

1.  <span data-ttu-id="09dc0-115">Ouvrez un fichier qui contient un flux Windows Media Audio 9 Professional en appelant la méthode [**IWMReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) .</span><span class="sxs-lookup"><span data-stu-id="09dc0-115">Open a file that contains a Windows Media Audio 9 Professional stream by calling the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method.</span></span>
2.  <span data-ttu-id="09dc0-116">Identifiez le numéro de sortie du flux de votre choix.</span><span class="sxs-lookup"><span data-stu-id="09dc0-116">Identify the output number of the stream that you want.</span></span> <span data-ttu-id="09dc0-117">Pour plus d’informations, consultez [pour identifier les numéros de sortie](to-identify-output-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="09dc0-117">For more information, see [To Identify Output Numbers](to-identify-output-numbers.md).</span></span>
3.  <span data-ttu-id="09dc0-118">Appelez la méthode [**IWMReaderAdvanced2 :: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) pour configurer la sortie S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="09dc0-118">Call the [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) method to configure S/PDIF output.</span></span> <span data-ttu-id="09dc0-119">Utilisez g \_ wszEnableWMAProSPDIFOutput pour le nom du paramètre.</span><span class="sxs-lookup"><span data-stu-id="09dc0-119">Use g\_wszEnableWMAProSPDIFOutput for the setting name.</span></span> <span data-ttu-id="09dc0-120">Le type de données est de **\_ type WMT \_ bool**; affectez la valeur **true** pour activer la sortie S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="09dc0-120">The data type is **WMT\_TYPE\_BOOL**; set the value to **TRUE** to enable S/PDIF output.</span></span>
4.  <span data-ttu-id="09dc0-121">Récupérez l’interface des propriétés de sortie ([**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) du format de sortie souhaité en appelant la méthode [**IWMReader :: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) .</span><span class="sxs-lookup"><span data-stu-id="09dc0-121">Get the output properties interface ([**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) of the desired output format by calling the [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) method.</span></span> <span data-ttu-id="09dc0-122">Pour plus d’informations sur l’énumération des formats de sortie, consultez [assignation de formats de sortie](assigning-output-formats.md).</span><span class="sxs-lookup"><span data-stu-id="09dc0-122">For more information about enumerating output formats, see [Assigning Output Formats](assigning-output-formats.md).</span></span>
5.  <span data-ttu-id="09dc0-123">Définissez le format de sortie en appelant la méthode [**IWMReader :: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) .</span><span class="sxs-lookup"><span data-stu-id="09dc0-123">Set the output format by calling the [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) method.</span></span> <span data-ttu-id="09dc0-124">Transmettez un pointeur vers l’interface **IWMOutputMediaProps** obtenue à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="09dc0-124">Pass in a pointer to the **IWMOutputMediaProps** interface obtained in step 4.</span></span>
6.  <span data-ttu-id="09dc0-125">Apportez d’autres modifications à la configuration et commencez la lecture.</span><span class="sxs-lookup"><span data-stu-id="09dc0-125">Make any other configuration changes and begin playback.</span></span>

> [!Note]  
> <span data-ttu-id="09dc0-126">Vous pouvez effectuer les étapes précédentes sur le lecteur synchrone à l’aide des méthodes correspondantes de l’interface [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) .</span><span class="sxs-lookup"><span data-stu-id="09dc0-126">You can perform the preceding steps on the synchronous reader by using the corresponding methods of the [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) interface.</span></span>

 

<span data-ttu-id="09dc0-127">L’exemple de code suivant montre comment définir un flux audio en sortie audio en tant que données S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="09dc0-127">The following example code demonstrates how to set an audio stream to output audio as S/PDIF data.</span></span> <span data-ttu-id="09dc0-128">Cette fonction suppose qu’un fichier a déjà été chargé dans le lecteur et que le numéro de sortie a été identifié.</span><span class="sxs-lookup"><span data-stu-id="09dc0-128">This function assumes that a file has already been loaded in the reader and that the output number has been identified.</span></span> <span data-ttu-id="09dc0-129">Pour plus d’informations sur l’utilisation de ce code, consultez [utilisation des exemples de code](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="09dc0-129">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT SetSPDIF(DWORD dwOutputNum, IWMReader* pReader)
{
    HRESULT hr = S_OK;

    IWMReaderAdvanced2*  pReaderAdv   = NULL;
    IWMOutputMediaProps* pOutputProps = NULL; 

    BOOL fValue = TRUE;

    // Get the advanced reader interface.
    hr = pReader->QueryInterface(IID_IWMReaderAdvanced2,
                                 (void**)&pReaderAdv);
    GOTO_EXIT_IF_FAILED(hr);

    // Set S/PDIF output.
    hr = pReaderAdv->SetOutputSetting(dwOutputNum, 
                                      g_wszEnableWMAProSPDIFOutput, 
                                      WMT_TYPE_BOOL, 
                                      (BYTE*)&fValue, 
                                      sizeof(BOOL));
    GOTO_EXIT_IF_FAILED(hr);

    // Get the first output format for the stream.
    // NOTE: You could also enumerate the available output formats
    // and pick one to use.

    hr = pReader->GetOutputFormat(dwOutputNum, 0, &pOutputProps);
    GOTO_EXIT_IF_FAILED(hr);

    // Set the output properties back on the reader.
    hr = pReader->SetOutputProps(dwOutputNum, pOutputProps);

Exit:
    SAFE_RELEASE(pReaderAdv);
    SAFE_RELEASE(pOutputProps);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="09dc0-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="09dc0-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09dc0-131">**Rubriques avancées**</span><span class="sxs-lookup"><span data-stu-id="09dc0-131">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="09dc0-132">**Lecture des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="09dc0-132">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="09dc0-133">**Interface IWMReader**</span><span class="sxs-lookup"><span data-stu-id="09dc0-133">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="09dc0-134">**Interface IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="09dc0-134">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[<span data-ttu-id="09dc0-135">**Interface IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="09dc0-135">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> </dl>

 

 




