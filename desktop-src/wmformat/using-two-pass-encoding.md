---
title: Utilisation de l’encodage Two-Pass (kit de développement logiciel (SDK) Windows Media format 11)
description: Utilisation de l’encodage Two-Pass
ms.assetid: 55fc768b-15f0-4236-ad0d-3792ccaa9b4f
keywords:
- ASF (Advanced Systems Format), encodage en deux passes
- ASF (format de systèmes avancés), encodage en deux passes
- encodage en deux passes, à propos de
- 2-encodage Pass, à propos de
- codecs, encodage en deux passes
- encodage en deux passes, interface IWMWriterPreprocess
- 2-encodage Pass, interface IWMWriterPreprocess
- IWMWriterPreprocess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3794856f47c1656cc53006268c41a063cdde96
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508281"
---
# <a name="using-two-pass-encoding-windows-media-format-11-sdk"></a><span data-ttu-id="f7c3e-111">Utilisation de l’encodage Two-Pass (kit de développement logiciel (SDK) Windows Media format 11)</span><span class="sxs-lookup"><span data-stu-id="f7c3e-111">Using Two-Pass Encoding (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="f7c3e-112">Certains codecs prennent en charge l’encodage en deux passes pour certains formats.</span><span class="sxs-lookup"><span data-stu-id="f7c3e-112">Some codecs support two-pass encoding for certain formats.</span></span> <span data-ttu-id="f7c3e-113">Dans certains cas, un codec requiert qu’un format spécifié soit encodé à l’aide de deux passes.</span><span class="sxs-lookup"><span data-stu-id="f7c3e-113">In some cases, a codec requires that a specified format be encoded using two passes.</span></span> <span data-ttu-id="f7c3e-114">Lorsque l’encodage en deux passes est utilisé, vous envoyez les exemples du flux au codec avant le passage de l’encodage.</span><span class="sxs-lookup"><span data-stu-id="f7c3e-114">When two-pass encoding is used, you send the samples for the stream to the codec before the encoding pass.</span></span> <span data-ttu-id="f7c3e-115">Le codec analyse les exemples et configure la passe d’encodage en fonction de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="f7c3e-115">The codec analyzes the samples and configures the encoding pass based on the analysis.</span></span> <span data-ttu-id="f7c3e-116">Cela génère un fichier encodé plus efficacement.</span><span class="sxs-lookup"><span data-stu-id="f7c3e-116">This results in a more efficiently encoded file.</span></span>

<span data-ttu-id="f7c3e-117">Pour déterminer si un codec prend en charge l’encodage en une seule passe, ou les deux à la fois, pour un format donné, appelez [**IWMCodecInfo3 :: SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) avec g \_ wszNumPasses et la valeur appropriée, puis Énumérez les formats pour voir si celui que vous souhaitez est retourné.</span><span class="sxs-lookup"><span data-stu-id="f7c3e-117">To determine whether a codec supports one-pass encoding, or two-pass, or both, for a given format, call [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) with g\_wszNumPasses and the appropriate value, and then enumerate the formats to see if the one you want is returned.</span></span> <span data-ttu-id="f7c3e-118">Pour plus d’informations sur les codecs Windows Media prenant en charge l’encodage en deux passes, consultez [choix d’une méthode d’encodage](choosing-an-encoding-method.md).</span><span class="sxs-lookup"><span data-stu-id="f7c3e-118">For more information about the Windows Media codecs that support two-pass encoding, see [Choosing an Encoding Method](choosing-an-encoding-method.md).</span></span>

<span data-ttu-id="f7c3e-119">Vous pouvez utiliser l’encodage en deux passes avec le kit de développement logiciel (SDK) Windows Media format en appelant les méthodes de l’interface [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="f7c3e-119">You can use two-pass encoding with the Windows Media Format SDK by calling methods of the [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) interface.</span></span>

<span data-ttu-id="f7c3e-120">Dans les cas où l’encodage en deux passes est requis pour un format particulier, mais que l’application ne parvient pas à effectuer une étape de prétraitement, le premier appel à [**WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) échouera avec le \_ nombre de \_ \_ passes NS E non valides \_ .</span><span class="sxs-lookup"><span data-stu-id="f7c3e-120">In cases where two-pass encoding is required for a particular format, but the application fails to perform a preprocessing pass, the first call to [**WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) will fail with NS\_E\_INVALID\_NUM\_PASSES.</span></span>

<span data-ttu-id="f7c3e-121">L’exemple de fonction suivant montre comment effectuer un encodage en deux passes.</span><span class="sxs-lookup"><span data-stu-id="f7c3e-121">The following example function demonstrates how to perform two-pass encoding.</span></span> <span data-ttu-id="f7c3e-122">Cette fonction est appelée une fois que le writer a été défini avec un profil et a démarré.</span><span class="sxs-lookup"><span data-stu-id="f7c3e-122">This function is called after the writer has been set with a profile and started.</span></span> <span data-ttu-id="f7c3e-123">Pour plus d’informations sur l’utilisation de ce code, consultez [utilisation des exemples de code](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="f7c3e-123">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT PreProcess(IWMWriter* pWriter, DWORD dwInputNum)
{
    HRESULT hr        = S_OK;
    DWORD   dwMaxPass = 0;

    IWMWriterPreprocess* pPreProc = NULL;

    // Get the writer preprocessor interface.
    hr = pWriter->QueryInterface(IID_IWMWriterPreprocess, 
                                 (void**) &pPreProc);
    GOTO_EXIT_IF_FAILED(hr);

    // Check that the input can be preprocessed.
    hr = pPreProc->GetMaxPreprocessingPasses(dwInputNum,0, &dwMaxPass);
    GOTO_EXIT_IF_FAILED(hr);

    if(dwMaxPass == 0)
    {
        hr = NS_E_INVALID_REQUEST;
        goto Exit;
    }

    // Set the number of preprocessing passes to the maximum.
    hr = pPreProc->SetNumPreprocessingPasses(dwInputNum, 0, dwMaxPass);
    GOTO_EXIT_IF_FAILED(hr);

    // Call BeginWriting before calling BeginPreprocessingPass
    hr = pWriter->BeginWriting();

    // Start preprocessing the first pass.
    hr = pPreProc->BeginPreprocessingPass(dwInputNum, 0);
    GOTO_EXIT_IF_FAILED(hr);

    // TODO: Make repeated calls to pPreProc->PreprocessSample to
    // preprocess all the samples in the stream.

    // End preprocessing.
    hr = pPreProc->EndPreprocessingPass(dwInputNum, 0);
    GOTO_EXIT_IF_FAILED(hr);

    // TODO: If the maximum number of preprocessing passes is greater
    // than one, repeat the preprocessing steps for each pass.

Exit:
    SAFE_RELEASE(pPreProc);
    Return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="f7c3e-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f7c3e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7c3e-125">**Écriture de fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="f7c3e-125">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




