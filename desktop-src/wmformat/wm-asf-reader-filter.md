---
title: filtre de lecteur ASF WM (kit de développement logiciel (SDK) Windows Media Format 11)
description: en savoir plus sur le filtre de lecteur ASF WM pour le SDK Windows Media Format 11. Passez en revue les informations de filtre et consultez les rubriques connexes.
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Windows Media Format SDK, lecteur ASF WM
- DirectShow, lecteur ASF WM
- Filtres QASF, lecteur ASF WM
- Lecteur ASF WM
- ASF (Advanced Systems Format), lecteur ASF WM
- ASF (format avancé des systèmes), lecteur ASF WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c825835e6d838a8a5d9b058f8bcf6ef52bd2a3d6a645787e0cf44da0f7573c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117844922"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a>filtre de lecteur ASF WM (kit de développement logiciel (SDK) Windows Media Format 11)

En fonction du nom d’un fichier ASF ou d’une URL, le lecteur ASF WM lit le contenu compressé, analyse les flux et expose une broche de sortie pour chacun d’entre eux. ce filtre se connecte en aval au Windows Media Audio ou Windows Media Video DMOs, qui effectue la décompression. La recherche est prise en charge si le fichier ASF est accessible en recherche. Le lecteur ASF WM applique des horodatages aux échantillons de support en fonction de l’horodatage dans le fichier ASF, mais il ne modifie pas les horodatages de quelque manière que ce soit. en interne, le filtre utilise l’objet Windows media Format reader pour lire le contenu multimédia Windows.

> [!Note]  
> Dans le kit de développement logiciel (SDK) DirectX, ce filtre n’est pas le filtre source par défaut pour les fichiers ASF. ainsi, avec ce kit de développement logiciel (SDK), vous ne pouvez pas utiliser ce filtre avec la méthode **RenderFile** . vous devez l’ajouter explicitement au graphique de filtre à l’aide de son identificateur de classe (CLSID). ce comportement est différent avec le kit de développement logiciel (SDK) de Format multimédia Windows. lorsque vous installez les bibliothèques d’exécution du SDK Windows Media Format, le lecteur asf WM est inscrit comme filtre par défaut pour les fichiers asf.

 

Le tableau suivant contient des informations sur le filtre de lecteur ASF WM, telles que les interfaces et les types de médias qu’il prend en charge.



|  Informations de filtre                      |  Types                                                                                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre      | **IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (implémenté partiellement. Consultez la section Notes.), **IWMReaderAdvanced2** (implémenté partiellement), **IWMDRMReader** (via **IServiceProvider**) |
| Types de média de broche d’entrée  | Non applicable                                                                                                                                                                                                                                |
| Interfaces pin d’entrée   | Non applicable                                                                                                                                                                                                                                |
| Types de média de broche de sortie | \_Video MediaType, MediaType \_ audio, MediaType \_ commande, MediaType \_ filetransfer                                                                                                                                                         |
| Type de format            | **VIDEOINFOHEADER2** si le contenu est [*entrelacé*](wmformat-glossary.md), sinon **VIDEOINFOHEADER**                                                                                                                    |
| Interfaces de broche de sortie  | **IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (via **IServiceProvider**)                                                                                                                             |
| CLSID du filtre           | CLSID \_ WMAsfReader                                                                                                                                                                                                                            |
| CLSID de page de propriétés    | Aucune page de propriétés                                                                                                                                                                                                                              |
| Exécutable             | Qasf.dll                                                                                                                                                                                                                                      |
| Mérite                  | MÉRITE \_ improbable                                                                                                                                                                                                                               |
| Catégorie de filtre        | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Remarques

Le lecteur ASF WM implémente partiellement les interfaces **IWMReaderAdvanced** et **IWMReaderAdvanced2** afin de permettre aux applications d’accéder aux méthodes d’information sur l’objet lecteur. L’implémentation du filtre passe simplement les appels par le biais de à l’interface sur l’objet lecteur. Les méthodes de streaming ne sont pas implémentées, car le filtre doit avoir un contrôle total sur le processus de diffusion en continu. Les méthodes **IWMReaderAdvanced** et **IWMReaderAdvanced2** suivantes sont implémentées :

-   [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [**IWMReaderAdvanced :: SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [**IWMReaderAdvanced2::GetBufferProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [**IWMReaderAdvanced2::GetDownloadProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [**IWMReaderAdvanced2::GetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [**IWMReaderAdvanced2::GetProtocolName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [**IWMReaderAdvanced2::SetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**DirectShow Référence QASF**](directshow-qasf-reference.md)
</dt> <dt>

[**Lecture des fichiers ASF dans DirectShow**](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




