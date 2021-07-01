---
description: En savoir plus sur le filtre de lecteur ASF WM pour DirectShow. Il s’agit d’un filtre de wrapper pour l’objet lecteur fourni avec le kit de développement logiciel (SDK) du format Windows Media.
ms.assetid: 82b9f849-b9dc-439b-8ca7-9dcd992338ab
title: Filtre de lecteur ASF WM (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 330ab870b97fc3e84ccb5b0f726d4f35ef1af147
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118664"
---
# <a name="wm-asf-reader-filter-directshow"></a>Filtre de lecteur ASF WM (DirectShow)

Le lecteur ASF WM est un filtre de wrapper pour l’objet lecteur fourni avec le kit de développement logiciel (SDK) du format Windows Media. il s’agit du filtre source recommandé pour la lecture de fichiers Windows Media et de contenu créé avec l’un des encodeurs Microsoft MPEG-4 DMOs.



| Étiquette | Value |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter), [**IAMExtendedSeeking**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking), **IServiceProvider** en outre, le filtre expose les interfaces du kit de développement logiciel (SDK) de format Windows Media suivantes : [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo), [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced), [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2), [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) (via **IServiceProvider**)<br/> |
| Types de média de broche d’entrée                    | Non applicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Interfaces pin d’entrée                     | Non applicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Types de média de broche de sortie                   | \_Video MediaType, MediaType \_ audio, MediaType \_ commande, MediaType \_ filetransfer                                                                                                                                                                                                                                                                                                                                                                                                     |
| Interfaces de broche de sortie                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass), **IServiceProvider** en outre, les broches exposent les interfaces du kit de développement logiciel (SDK) du format Windows Media suivantes : **IWMStreamConfig2** (via **IServiceProvider**)<br/>                                                                                                                                                                                                                                    |
| CLSID du filtre                             | CLSID \_ WMAsfReader                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID de page de propriétés                      | Aucune page de propriétés.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Exécutable                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Mérite](merit.md)                       | MÉRITE \_ improbable                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Remarques

En fonction du nom d’un fichier ASF ou d’une URL, le lecteur ASF WM lit le contenu compressé, analyse les flux compressés et expose une broche de sortie pour chacun d’eux. Ce filtre permet de se connecter en aval des filtres de codecs audio et/ou vidéo, qui effectuent la décompression. La recherche est prise en charge si le fichier ASF est accessible en recherche. L’heure du lecteur ASF marque les échantillons avant de les envoyer en aval, mais ne modifie pas les horodatages de quelque manière que ce soit.

La lecture à des vitesses autres que 1,0 (comme spécifié dans [**IMediaSeeking ::**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)sesente) n’est pas prise en charge.

Lorsque l’exécution du SDK Windows Media format envoie des messages d' [**\_ État WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_status) au filtre de l’enregistreur ASF WM, le filtre transfère tous les messages relatifs à l’acquisition de licence DRM en tant qu’événements d' [**\_ \_ événements EC WMT**](ec-wmt-event.md) . Pour plus d’informations, consultez [lecture de fichiers ASF DRM-Protected dans DirectShow](reading-drm-protected-asf-files-in-directshow.md).

Le lecteur ASF WM implémente partiellement les interfaces [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) et [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) afin de permettre aux applications d’accéder aux méthodes d’information sur l’objet lecteur. L’implémentation du filtre passe simplement les appels par le biais de à l’interface sur l’objet lecteur. Les méthodes de streaming ne sont pas implémentées, car le filtre doit avoir un contrôle total sur le processus de diffusion en continu. Les méthodes suivantes sont implémentées :

-   [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [**IWMReaderAdvanced :: SetClientInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [**IWMReaderAdvanced2::GetBufferProgress**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [**IWMReaderAdvanced2::GetDownloadProgress**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [**IWMReaderAdvanced2::GetPlayMode**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [**IWMReaderAdvanced2::GetProtocolName**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [**IWMReaderAdvanced2::SetPlayMode**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> <dt>

[Lecture de fichiers ASF dans DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
