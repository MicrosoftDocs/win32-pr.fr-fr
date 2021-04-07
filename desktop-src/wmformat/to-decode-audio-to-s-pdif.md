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
# <a name="to-decode-audio-to-spdif"></a>Pour décoder l’audio en S/PDIF

L’encodage audio du codec Windows Media Audio 9 Professional peut être décodé au format S/PDIF de Sony/Philips. Pour générer la sortie S/PDIF, procédez comme suit :

1.  Ouvrez un fichier qui contient un flux Windows Media Audio 9 Professional en appelant la méthode [**IWMReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) .
2.  Identifiez le numéro de sortie du flux de votre choix. Pour plus d’informations, consultez [pour identifier les numéros de sortie](to-identify-output-numbers.md).
3.  Appelez la méthode [**IWMReaderAdvanced2 :: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) pour configurer la sortie S/PDIF. Utilisez g \_ wszEnableWMAProSPDIFOutput pour le nom du paramètre. Le type de données est de **\_ type WMT \_ bool**; affectez la valeur **true** pour activer la sortie S/PDIF.
4.  Récupérez l’interface des propriétés de sortie ([**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) du format de sortie souhaité en appelant la méthode [**IWMReader :: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) . Pour plus d’informations sur l’énumération des formats de sortie, consultez [assignation de formats de sortie](assigning-output-formats.md).
5.  Définissez le format de sortie en appelant la méthode [**IWMReader :: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) . Transmettez un pointeur vers l’interface **IWMOutputMediaProps** obtenue à l’étape 4.
6.  Apportez d’autres modifications à la configuration et commencez la lecture.

> [!Note]  
> Vous pouvez effectuer les étapes précédentes sur le lecteur synchrone à l’aide des méthodes correspondantes de l’interface [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) .

 

L’exemple de code suivant montre comment définir un flux audio en sortie audio en tant que données S/PDIF. Cette fonction suppose qu’un fichier a déjà été chargé dans le lecteur et que le numéro de sortie a été identifié. Pour plus d’informations sur l’utilisation de ce code, consultez [utilisation des exemples de code](using-the-code-examples.md).


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Rubriques avancées**](advanced-topics.md)
</dt> <dt>

[**Lecture des fichiers ASF**](reading-asf-files.md)
</dt> <dt>

[**Interface IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Interface IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**Interface IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> </dl>

 

 




