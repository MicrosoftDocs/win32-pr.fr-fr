---
title: Diffusion de données ASF
description: Diffusion de données ASF
ms.assetid: 1b04f361-8147-4f6a-8c9d-d8eeed28550a
keywords:
- Windows Media Format SDK, diffusion de données ASF
- ASF (Advanced Systems Format), diffusion des données
- ASF (format des systèmes avancés), diffusion des données
- Windows Media Format SDK, envoyer des données ASF
- ASF (Advanced Systems Format), envoi de données
- ASF (format des systèmes avancés), envoyer des données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a44fc9ea0515822c765b0cb3af457254341a64f08e64d566aa9e226a48758e7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434463"
---
# <a name="broadcasting-asf-data"></a>Diffusion de données ASF

Cette rubrique explique comment envoyer des données ASF sur un réseau à l’aide du protocole HTTP. L’envoi de fichiers sur un réseau requiert l’utilisation de l’objet Writer. vous devez donc avoir une compréhension générale de cet objet avant de lire cette rubrique. Pour plus d’informations, consultez [écriture de fichiers ASF](writing-asf-files.md).

Si vous démarrez avec des données non compressées, procédez comme suit :

1.  Créez l’objet writer en appelant la fonction [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) . Cette fonction retourne un pointeur **IWMWriter** .
    ```C++
    IWMWriter *pWriter;
    hr = WMCreateWriter(NULL, &pWriter);
    ```

    

2.  Créez l’objet récepteur réseau en appelant la fonction [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) , qui retourne un pointeur **IWMWriterNetworkSink** .
    ```C++
    IWMWriterNetworkSink *pNetSink;
    hr = WMCreateWriterNetworkSink(&pNetSink);
    ```

    

3.  Appelez [**IWMWriterNetworkSink :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) sur le récepteur réseau et spécifiez le numéro de port à ouvrir. par exemple, 8080. Vous pouvez également appeler [**IWMWriterNetworkSink :: GetHostURL**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) pour récupérer l’URL de l’hôte. Les clients accéderont au contenu à partir de cette URL. Vous pouvez également appeler [**IWMWriterNetworkSink :: SetMaximumClients**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) pour restreindre le nombre de clients.
    ```C++
    DWORD dwPortNum = 8080;
    hr = pNetSink->Open( &dwPortNum)
    ```

    

4.  Attachez le récepteur réseau au writer en appelant [**IWMWriterAdvanced :: AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) sur le writer, avec un pointeur vers l’interface **IWMWriterNetworkSink** du récepteur réseau.
    ```C++
    IWMWriterAdvanced *pWriterAdvanced;
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, ( void** ) pWriterAdvanced );
    if (SUCCEEDED(hr))
    {
        pWriterAdvanced->AddSink(pNetSink);
    }
    ```

    

5.  Définissez le profil ASF en appelant la méthode [**IWMWriter :: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) sur l’objet Writer, avec un pointeur [**IWMProfile**](iwmprofile.md) . Pour plus d’informations sur la création d’un profil, consultez [utilisation des profils](working-with-profiles.md).
6.  Si vous le souhaitez, spécifiez des métadonnées à l’aide de l’interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) sur le writer.
7.  Appelez [**IWMWriter :: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) sur le writer.
    ```C++
    hr = pWriter->BeginWriting();
    ```

    

8.  Pour chaque exemple, appelez la méthode [**IWMWriter :: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) . Spécifiez le numéro du flux, l’heure de la présentation, la durée de l’échantillon et un pointeur vers l’exemple de mémoire tampon. La méthode **WriteSample** compresse les exemples.
9.  Lorsque vous avez terminé, appelez [**IWMWriter :: EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) sur le writer.
    ```C++
    hr = pWriter->EndWriting();
    ```

    

10. Appelez [**IWMWriterAdvanced :: RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) sur le writer pour détacher l’objet récepteur réseau.
    ```C++
    hr = pWriterAdvanced->RemoveSink(pNetSink);
    ```

    

11. Appelez [**IWMWriterNetworkSink :: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) sur le récepteur réseau pour libérer le port.
    ```C++
    hr = pNetSink->Close();
    ```

    

Une autre façon de diffuser du contenu ASF sur un réseau consiste à le lire à partir d’un fichier ASF existant. L’exemple WMVNetWrite fourni dans le kit de développement logiciel (SDK) illustre cette approche. En plus des étapes indiquées précédemment, procédez comme suit :

1.  Créez un objet lecteur et appelez la méthode **Open** avec le nom du fichier.
2.  Appelez [**IWMReaderAdvanced :: SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) sur l’objet Reader, avec la valeur **true**. Cela permet à l’application de lire chaque flux du fichier, y compris les flux avec exclusion mutuelle.
3.  Interrogez le lecteur de l’interface [**IWMProfile**](iwmprofile.md) . Utilisez ce pointeur lorsque vous appelez [**IWMWriter :: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) sur l’objet Writer (étape 5 de la procédure précédente).
4.  Pour chaque flux défini dans le profil, appelez [**IWMProfile :: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) pour obtenir le numéro du flux. Transmettez ce numéro de flux à la méthode [**IWMReaderAdvanced :: SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) du lecteur. Cette méthode informe le lecteur qu’il doit remettre des exemples compressés, plutôt que de les décoder. Les exemples sont remis à l’application par le biais de la méthode de rappel [**IWMReaderCallbackAdvanced :: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) de l’application.

    Vous devez obtenir les informations de codec pour chaque flux que vous lisez non compressé et l’ajouter à l’en-tête avant la diffusion. Pour obtenir les informations du codec, appelez [**IWMHeaderInfo2 :: GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) et [**IWMHeaderInfo2 :: GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) pour énumérer les codecs associés au fichier dans le lecteur. Sélectionnez les informations du codec qui correspondent à la configuration du flux. Définissez ensuite les informations du codec dans le writer en appelant [**IWMHeaderInfo3 :: AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), en passant les informations obtenues à partir du lecteur.

5.  Une fois que vous avez défini le profil sur le writer, appelez [**IWMWriter :: GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) sur le writer pour connaître le nombre d’entrées. Pour chaque entrée, appelez [**IWMWriter :: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) avec la valeur **null**. Cela indique à l’objet enregistreur que l’application remet les exemples compressés, de sorte que le Writer n’a pas besoin d’utiliser de codec pour compresser les données. Veillez à appeler **SetInputProps** avant d’appeler **BeginWriting**.
6.  Éventuellement, copiez les attributs de métadonnées du lecteur vers le writer.
7.  Étant donné que les exemples du lecteur sont déjà compressés, utilisez la méthode [**IWMWriterAdvanced :: WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) pour écrire les exemples au lieu de la méthode **WriteSample** . La méthode **WriteStreamSample** ignore les procédures de compression habituelles de l’objet Writer.
8.  Lorsque le lecteur atteint la fin du fichier, il envoie une \_ notification de EOF WMT à l’application.

En outre, l’application doit piloter l’horloge sur l’objet lecteur, afin que le lecteur extraie les données du fichier le plus rapidement possible. Pour ce faire, appelez la méthode [**IWMReaderAdvanced :: SetUserProvidedClock**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) sur le lecteur, avec la valeur **true**. Une fois que le lecteur a envoyé la notification de démarrage de WMT \_ , appelez [**IWMReaderAdvanced ::D elivertime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) et spécifiez l’intervalle de temps que le lecteur doit remettre. Une fois que le lecteur a fini de lire cet intervalle de temps, il appelle la méthode de rappel [**IWMReaderCallbackAdvanced :: OnTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) de l’application. L’application doit à nouveau appeler **DeliverTime** pour lire l’intervalle de temps suivant. Par exemple, pour lire le fichier à intervalles d’une seconde :


```C++
// Initial call to DeliverTime.
QWORD m_qwTime = 10000000; // 1 second.
hr = m_pReaderAdvanced->DeliverTime(m_qwTime);

// In the callback:
HRESULT CNetWrite::OnTime(QWORD cnsCurrentTime, void *pvContext)
{
    HRESULT hr = S_OK;
    // Continue calling DeliverTime until the end of the file.
    if(!m_bEOF)
    {
        m_qwTime += 10000000; // 1 second.
        hr = m_pReaderAdvanced->DeliverTime(m_qwTime);
    }
    return S_OK;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Envoi de données ASF sur un réseau**](sending-asf-data-over-a-network.md)
</dt> <dt>

[**Utilisation des récepteurs d’écriture**](working-with-writer-sinks.md)
</dt> </dl>

 

 




