---
description: Capture vidéo dans un fichier AVI
ms.assetid: 0f5f4a82-4a2e-4c48-b201-bda641cb8619
title: Capture vidéo dans un fichier AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86504e9ce149f495e1ea31664f56382340d33887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104551755"
---
# <a name="capturing-video-to-an-avi-file"></a>Capture vidéo dans un fichier AVI

L’illustration suivante montre le graphique le plus simple possible pour capturer des vidéos dans un fichier AVI.

![graphique de capture vidéo AVI](images/vidcap02.png)

Le filtre [multiplex MUX](avi-mux-filter.md) prend le flux vidéo de la broche de capture et le reporte dans un flux avi. Un flux audio peut également être connecté au filtre multiplex MUX, auquel cas le multiplexeur entrelace les deux flux. Le filtre du [writer de fichier](file-writer-filter.md) écrit le flux AVI sur le disque.

Pour générer le graphique, commencez par appeler la méthode [**ICaptureGraphBuilder2 :: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) , comme suit :


```C++
IBaseFilter *pMux;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Avi,  // Specifies AVI for the target file.
    L"C:\\Example.avi", // File name.
    &pMux,              // Receives a pointer to the mux.
    NULL);              // (Optional) Receives a pointer to the file sink.
```



Le premier paramètre spécifie le type de fichier, en l’occurrence AVI. Le deuxième paramètre donne le nom du fichier. Pour AVI, la méthode SetOutputFileName cocrée le filtre multiplex MUX et le filtre de writer de fichier et les ajoute au graphique. Il définit également le nom de fichier sur le filtre du writer de fichier, en appelant la méthode [**IFileSinkFilter :: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) et connecte les deux filtres. La méthode retourne un pointeur vers le multiplexeur de la valeur AVI dans le troisième paramètre. Le cas échéant, elle retourne un pointeur vers l’interface [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) dans le quatrième paramètre. Si vous n’avez pas besoin de cette interface, vous pouvez définir ce paramètre sur la **valeur null**, comme indiqué dans l’exemple précédent.

Ensuite, appelez la méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) pour connecter le filtre de capture à AVI MUX, comme suit :


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                  // Capture filter.
    NULL,                  // Intermediate filter (optional).
    pMux);                 // Mux or file sink filter.

// Release the mux filter.
pMux->Release();
```



Le premier paramètre donne la catégorie pin, qui est la \_ \_ capture de catégorie pin pour la capture. Le deuxième paramètre donne le type de média. Le troisième paramètre est un pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du filtre de capture. Le quatrième paramètre est facultatif ; elle vous permet d’acheminer le flux vidéo via un filtre intermédiaire, tel qu’un encodeur, avant de le passer au filtre Mux. Sinon, affectez la valeur **null** à ce paramètre, comme indiqué dans l’exemple précédent. Le cinquième paramètre est le pointeur vers le filtre Mux. Ce pointeur est obtenu en appelant la méthode SetOutputFileName.

Pour capturer l’audio, appelez RenderStream avec le type de média \_ audio MediaType. Si vous capturez des données audio et vidéo à partir de deux appareils distincts, il est judicieux de faire en sorte que le flux audio soit le flux principal. Cela permet d’éviter la dérive entre les deux flux, car le filtre multiplex MUX ajuste la vitesse de lecture du flux vidéo pour qu’elle corresponde au flux audio. Pour définir le flux principal, appelez la méthode [**IConfigAviMux :: SetMasterStream**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) sur le filtre multiplex Mux :


```C++
IConfigAviMux *pConfigMux = NULL;
hr = pMux->QueryInterface(IID_IConfigAviMux, (void**)&pConfigMux);
if (SUCCEEDED(hr))
{
    pConfigMux->SetMasterStream(1);
    pConfigMux->Release();
}
```



Le paramètre de SetMasterStream est le numéro du flux, qui est déterminé par l’ordre dans lequel vous appelez RenderStream. Par exemple, si vous appelez d’abord RenderStream pour la vidéo, puis pour l’audio, la vidéo est Stream 0 et l’audio est Stream 1.

Vous pouvez également définir la manière dont le filtre multiplex MUX entrelace les flux audio et vidéo, en appelant la méthode [**IConfigInterleaving ::p ut \_ mode**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode) .


```C++
IConfigInterleaving *pInterleave = NULL;
hr = pMux->QueryInterface(IID_IConfigInterleaving, (void**)&pInterleave);
if (SUCCEEDED(hr))
{
    pInterleave->put_Mode(INTERLEAVE_CAPTURE);
    pInterleave->Release();
}
```



Avec l’indicateur ENTRELACement \_ , le multiplexeur de contenu AVI effectue l’entrelacement à un débit adapté à la capture vidéo. Vous pouvez également utiliser l’ENTRELACement \_ aucun, ce qui signifie qu’il n’y a pas d’entrelacement. le multiplexeur de données AVI écrira simplement les données dans l’ordre dans lequel elles arrivent. L’indicateur d’ENTRELACement \_ complet signifie que le multiplexeur de contenu AVI effectue un entrelacement complet. Toutefois, ce mode est moins adapté à la capture vidéo, car il requiert le plus de surentendus.

Encodage du flux vidéo

Vous pouvez encoder le flux vidéo en insérant un filtre d’encodeur entre le filtre de capture et le filtre multiplex Mux. Utilisez l' [énumérateur de périphérique système](system-device-enumerator.md) ou le [Mappeur de filtre](filter-mapper.md) pour sélectionner un filtre d’encodeur. (Pour plus d’informations, consultez [énumération d’appareils et de filtres](enumerating-devices-and-filters.md).)

Spécifiez le filtre d’encodeur en tant que quatrième paramètre de RenderStream, affiché en gras dans l’exemple suivant :


```C++
IBaseFilter *pEncoder;
/* Create the encoder filter (not shown). */
// Add it to the filter graph.
pGraph->AddFilter(pEncoder, L"Encoder");

/* Call SetOutputFileName as shown previously. */

// Render the stream.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, 
    pCap, 
pEncoder, pMux);
pEncoder->Release();
```



Le filtre d’encodeur peut prendre en charge les [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) ou d’autres interfaces pour définir les paramètres d’encodage. Pour obtenir la liste des interfaces possibles, consultez [encodage et décodage des interfaces](file-encoding-and-decoding-interfaces.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Capture vidéo dans un fichier](capturing-video-to-a-file.md)
</dt> </dl>

 

 



