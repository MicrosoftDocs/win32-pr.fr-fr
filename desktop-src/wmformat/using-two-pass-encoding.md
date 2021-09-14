---
title: utilisation de l’encodage Two-Pass (kit de développement logiciel (SDK) Windows Media Format 11)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295843"
---
# <a name="using-two-pass-encoding-windows-media-format-11-sdk"></a>utilisation de l’encodage Two-Pass (kit de développement logiciel (SDK) Windows Media Format 11)

Certains codecs prennent en charge l’encodage en deux passes pour certains formats. Dans certains cas, un codec requiert qu’un format spécifié soit encodé à l’aide de deux passes. Lorsque l’encodage en deux passes est utilisé, vous envoyez les exemples du flux au codec avant le passage de l’encodage. Le codec analyse les exemples et configure la passe d’encodage en fonction de l’analyse. Cela génère un fichier encodé plus efficacement.

Pour déterminer si un codec prend en charge l’encodage en une seule passe, ou les deux à la fois, pour un format donné, appelez [**IWMCodecInfo3 :: SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) avec g \_ wszNumPasses et la valeur appropriée, puis Énumérez les formats pour voir si celui que vous souhaitez est retourné. pour plus d’informations sur les codecs multimédias Windows qui prennent en charge l’encodage en deux passes, consultez [choix d’une méthode d’encodage](choosing-an-encoding-method.md).

vous pouvez utiliser l’encodage en deux passes avec le kit de développement logiciel (SDK) Format multimédia Windows en appelant des méthodes de l’interface [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) .

Dans les cas où l’encodage en deux passes est requis pour un format particulier, mais que l’application ne parvient pas à effectuer une étape de prétraitement, le premier appel à [**WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) échouera avec le \_ nombre de \_ \_ passes NS E non valides \_ .

L’exemple de fonction suivant montre comment effectuer un encodage en deux passes. Cette fonction est appelée une fois que le writer a été défini avec un profil et a démarré. Pour plus d’informations sur l’utilisation de ce code, consultez [utilisation des exemples de code](using-the-code-examples.md).


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Écriture de fichiers ASF**](writing-asf-files.md)
</dt> </dl>

 

 




