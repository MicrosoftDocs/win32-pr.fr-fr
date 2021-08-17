---
description: En savoir plus sur les types de média dans DirectShow. Le type de média est un moyen universel et extensible de décrire les formats multimédias numériques.
ms.assetid: 9984ba36-4e43-4886-a073-34b330274c9c
title: À propos des types de média (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fa3034581e443472f1b73c0bc42ca7b8b532a18120df3e067b02ad16f37930e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074893"
---
# <a name="about-media-types-directshow"></a>À propos des types de média (DirectShow)

étant donné que DirectShow est modulaire, il est nécessaire de décrire le format des données à chaque point du graphique de filtre. Par exemple, envisagez la lecture AVI. Les données entrent dans le graphique sous forme de flux de blocs RIFF. Celles-ci sont analysées dans des flux vidéo et audio. Le flux vidéo est constitué de trames vidéo, qui sont probablement compressées. Après le décodage, le flux vidéo est une série de bitmaps non compressées. Le flux audio passe par un processus similaire.

Types de média : comment DirectShow représente les Formats

Le *type de média* est un moyen universel et extensible de décrire les formats multimédias numériques. Lorsque deux filtres se connectent, ils s’accordent sur un type de support. Le type de média identifie le type de données que le filtre en amont va remettre au filtre en aval et la disposition physique des données. Si deux filtres ne peuvent pas s’accorder sur un type de média, ils ne se connectent pas.

Pour certaines applications, vous n’aurez jamais à vous soucier des types de médias. dans le cas d’une lecture de fichier, par exemple, DirectShow gère tous les détails. D’autres types d’applications peuvent avoir besoin de travailler directement avec les types de média.

Les types de média sont définis à l’aide de la structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Cette structure contient les informations suivantes :

-   **Type majeur**: le type principal est un GUID qui définit la catégorie globale des données. Les types principaux incluent la vidéo, l’audio, le flux d’octets non analysés, les données MIDI, etc.
-   **SubType**: le sous-type est un autre GUID, qui définit le format de manière plus approfondie. Par exemple, dans le type principal vidéo, il existe des sous-types pour RGB-24, RGB-32, UYVY, et ainsi de suite. Dans l’audio, il y a des données audio PCM, une charge utile MPEG-1, et d’autres. Le sous-type fournit plus d’informations que le type principal, mais il ne définit pas tout ce qui concerne le format. Par exemple, les sous-types vidéo ne définissent pas la taille de l’image ni la fréquence d’images. Celles-ci sont définies par le bloc de format, décrit ci-dessous.
-   **Bloc de format**: le bloc de format est un bloc de données qui décrit le format en détail. Le bloc de format est alloué séparément de la structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Le membre **pbFormat** de la structure du **\_ \_ type de média am** pointe vers le bloc de format.

    Le membre **pbFormat** est typé **void \** _, car la disposition du bloc de format change en fonction du type de média. Par exemple, le son PCM utilise une structure [_ *WAVEFORMATEX* *](/previous-versions/dd757713(v=vs.85)) . La vidéo utilise différentes structures, notamment [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) et [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2). Le membre **formatType** de la structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) est un GUID qui spécifie la structure contenue dans le bloc de format. Un GUID est assigné à chaque structure de format. Le membre **cbFormat** spécifie la taille du bloc de format. Vérifiez toujours ces valeurs avant de déréférencer le pointeur **pbFormat** .

Si le bloc de format est rempli, le type et le sous-type principaux contiennent des informations redondantes. Toutefois, le type et le sous-type majeurs offrent un moyen pratique d’identifier des formats sans bloc de format complet. Par exemple, vous pouvez spécifier un format RGB 24 bits générique (MEDIASUBTYPE \_ Rgb24), sans connaître toutes les informations requises par la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , telles que la taille de l’image et la fréquence d’images.

Par exemple, un filtre peut utiliser le code suivant pour vérifier un type de média :


```C++
HRESULT CheckMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt == NULL) return E_POINTER;

    // Check the major type. We're looking for video.
    if (pmt->majortype != MEDIATYPE_Video)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the subtype. We're looking for 24-bit RGB.
    if (pmt->subtype != MEDIASUBTYPE_RGB24)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the format type and the size of the format block.
    if ((pmt->formattype == FORMAT_VideoInfo) &&
         (pmt->cbFormat >= sizeof(VIDEOINFOHEADER) &&
         (pmt->pbFormat != NULL))
    {
        // Now it's safe to coerce the format block pointer to the
        // correct structure, as defined by the formattype GUID.
        VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    
        // Examine pVIH (not shown). If it looks OK, return S_OK.
        return S_OK;
    }

    return VFW_E_INVALIDMEDIATYPE;
}
```



La structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) contient également des champs facultatifs. Ils peuvent être utilisés pour fournir des informations supplémentaires, mais les filtres ne sont pas requis pour les utiliser :

-   **lSampleSize**. Si ce champ est différent de zéro, il définit la taille de chaque échantillon. Si la valeur est égale à zéro, cela signifie que la taille de l’échantillon peut varier de sample à Sample.
-   **bFixedSizeSamples**. Si cet indicateur booléen a la valeur **true**, cela signifie que la valeur de **lSampleSize** est valide. Dans le cas contraire, vous devez ignorer **lSampleSize**.
-   **bTemporalCompression**. Si cet indicateur booléen a la **valeur false**, cela signifie que tous les frames sont des images clés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[le filtre Graph et ses composants](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 
