---
description: Configurer le format de sortie vidéo
ms.assetid: 1969072e-575e-49b4-88db-4c7e7a5a1c37
title: Configurer le format de sortie vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d09ac64d7f43e6c39377277544867491a93a6f3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104562308"
---
# <a name="configure-the-video-output-format"></a>Configurer le format de sortie vidéo

> [!Note]  
> La fonctionnalité décrite dans cette rubrique est déconseillée. Pour configurer le format de sortie d’un périphérique de capture, une application doit utiliser la structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) renvoyée par [**IAMStreamConfig :: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) dans le paramètre *VPM* .

 

Un périphérique de capture peut prendre en charge une plage de formats de sortie. Par exemple, un appareil peut prendre en charge les couleurs RVB 16 bits, 32 bits et YUYV. Dans chacun de ces formats, l’appareil peut prendre en charge une plage de tailles d’image.

Dans un périphérique WDM, l’interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) est utilisée pour signaler les formats pris en charge par l’appareil et pour définir le format. (Pour les appareils VFW hérités, utilisez la boîte de dialogue Format vidéo VFW, comme décrit dans [afficher des boîtes de dialogue de capture VFW](display-vfw-capture-dialog-boxes.md).) L’interface **IAMStreamConfig** est exposée sur le code confidentiel de capture, le code confidentiel de la préversion du filtre de capture ou les deux. Utilisez la méthode [**ICaptureGraphBuilder2 :: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) pour accéder au pointeur d’interface :


```C++
IAMStreamConfig *pConfig = NULL;
hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, // Preview pin.
    0,    // Any media type.
    pCap, // Pointer to the capture filter.
    IID_IAMStreamConfig, (void**)&pConfig);
```



L’appareil dispose d’une liste de types de médias qu’il prend en charge. Pour chaque type de média, l’appareil fournit également un ensemble de fonctionnalités. Il s’agit notamment de la plage de tailles d’images disponibles pour ce format, de la façon dont l’appareil peut étirer ou réduire l’image, ainsi que de la plage de fréquences d’images.

Pour connaître le nombre de types de médias, appelez la méthode [**IAMStreamConfig :: GetNumberOfCapabilities**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getnumberofcapabilities) . La méthode retourne deux valeurs :

-   Nombre de types de médias.
-   Taille de la structure qui contient les informations sur les fonctionnalités.

La valeur de taille est nécessaire car l’interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) est utilisée pour l’audio et la vidéo (et peut être étendue à d’autres types de média). Pour la vidéo, les fonctionnalités sont décrites à l’aide de la structure d' [**\_ \_ \_ embouts de la configuration de flux vidéo**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) , tandis que l’audio utilise la structure de la [**\_ configuration de flux \_ \_ audio**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) .

Pour énumérer les types de média, appelez la méthode [**IAMStreamConfig :: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) avec un index de base zéro. La méthode **GetStreamCaps** retourne un type de média et la structure de fonctionnalité correspondante :


```C++
int iCount = 0, iSize = 0;
hr = pConfig->GetNumberOfCapabilities(&iCount, &iSize);

// Check the size to make sure we pass in the correct structure.
if (iSize == sizeof(VIDEO_STREAM_CONFIG_CAPS))
{
    // Use the video capabilities structure.

    for (int iFormat = 0; iFormat < iCount; iFormat++)
    {
        VIDEO_STREAM_CONFIG_CAPS scc;
        AM_MEDIA_TYPE *pmtConfig;
        hr = pConfig->GetStreamCaps(iFormat, &pmtConfig, (BYTE*)&scc);
        if (SUCCEEDED(hr))
        {
            /* Examine the format, and possibly use it. */

            // Delete the media type when you are done.
            DeleteMediaType(pmtConfig);
        }
}
```



Notez comment les structures sont allouées pour la méthode [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) . La méthode alloue la structure de type de média, tandis que l’appelant alloue la structure de fonctionnalités. Forcez la structure de fonctionnalités en pointeur de tableau d’octets. Une fois que vous avez terminé avec le type de média, supprimez la structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , ainsi que le bloc de format du type de média.

Vous pouvez configurer l’appareil pour qu’il utilise un format retourné dans la méthode [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) . Appelez simplement [**IAMStreamConfig :: SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) avec le type de média :


```C++
hr = pConfig->SetFormat(pmtConfig);
```



Si le code pin n’est pas connecté, il tente d’utiliser ce format quand il se connecte. Si le code PIN est déjà connecté, il tente de se reconnecter à l’aide du nouveau format. Dans les deux cas, il est possible que le filtre en aval rejette le format.

Vous pouvez également modifier le type de média avant de le passer à la méthode [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) . C’est là qu’intervient la structure de la [**\_ configuration du flux \_ \_ vidéo**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) . Il décrit toutes les méthodes valides pour modifier le type de média. Pour utiliser ces informations, vous devez comprendre les détails de ce type de média particulier.

Par exemple, supposons que [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) retourne un format RGB de 24 bits, avec une taille de trame de 320 x 240 pixels. Vous pouvez accéder à ces informations en examinant le type principal, le sous-type et le bloc de format du type de média :


```C++
if ((pmtConfig.majortype == MEDIATYPE_Video) &&
    (pmtConfig.subtype == MEDIASUBTYPE_RGB24) &&
    (pmtConfig.formattype == FORMAT_VideoInfo) &&
    (pmtConfig.cbFormat >= sizeof (VIDEOINFOHEADER)) &&
    (pmtConfig.pbFormat != NULL))
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)pmtConfig.pbFormat;
    // pVih contains the detailed format information.
    LONG lWidth = pVih->bmiHeader.biWidth;
    LONG lHeight = pVih->bmiHeader.biHeight;
}
```



La structure d' [**\_ \_ \_ embouts de la configuration de flux vidéo**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) donne la largeur et la hauteur minimales et maximales qui peuvent être utilisées pour ce type de média. Il vous donne également la taille d’étape, qui définit les incréments par lesquels vous pouvez ajuster la largeur ou la hauteur. Par exemple, l’appareil peut retourner les éléments suivants :

-   MinOutputSize : 160 x 120
-   MaxOutputSize : 320 x 240
-   OutputGranularityX : 8 pixels (taille d’étape horizontale)
-   OutputGranularityY : 8 pixels (taille d’étape verticale)

À partir de ces nombres, vous pouvez définir la largeur sur n’importe quelle valeur dans la plage (160, 168, 176,... 304, 312, 320) et la hauteur à toute valeur comprise dans la plage (120, 128, 136,... 104, 112, 120). Le diagramme suivant illustre ce processus.

![tailles de format vidéo](images/strmcap3.png)

Pour définir une nouvelle taille de frame, modifiez directement la structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) renvoyée dans [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps):


```C++
pVih->bmiHeader.biWidth = 160;
pVih->bmiHeader.biHeight = 120;
pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader);
```



Transmettez ensuite le type de média à la méthode [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) , comme décrit précédemment.

Les membres **MinFrameInterval** et **MaxFrameInterval** de [**la \_ configuration de flux \_ \_ vidéo**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) sont la longueur minimale et maximale de chaque image vidéo, que vous pouvez traduire en fréquences d’images comme suit :

`frames per second = 10,000,000 / frame duration`

Pour demander une fréquence d’images particulière, modifiez la valeur de **AvgTimePerFrame** dans la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ou [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) dans le type de média. L’appareil peut ne pas prendre en charge chaque valeur possible comprise entre le minimum et le maximum, de sorte que le pilote utilise la valeur la plus proche possible. Pour voir quelle valeur le pilote a réellement utilisé, appelez [**IAMStreamConfig :: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) après avoir appelé [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat).

Certains pilotes peuvent signaler **MAXLONGLONG** (0x7FFFFFFFFFFFFFFF) pour la valeur de **MaxFrameInterval**, ce qui signifie qu’il n’y a pas de durée maximale. Toutefois, vous souhaiterez peut-être appliquer une fréquence d’images minimale dans votre application, par exemple 1 i/s.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des types de média](about-media-types.md)
</dt> <dt>

[Configuration d’un périphérique de capture vidéo](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



