---
title: Filtre de lecteur ASF WM (kit de développement logiciel (SDK) Windows Media format 11)
description: Filtre de lecteur ASF WM
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
ms.openlocfilehash: e13b7944f45b850a158c9832e174ae5ec7dce4d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739381"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a>Filtre de lecteur ASF WM (kit de développement logiciel (SDK) Windows Media format 11)

En fonction du nom d’un fichier ASF ou d’une URL, le lecteur ASF WM lit le contenu compressé, analyse les flux et expose une broche de sortie pour chacun d’entre eux. Ce filtre se connecte en aval au Windows Media Audio ou Windows Media Video DMOs, qui effectue la décompression. La recherche est prise en charge si le fichier ASF est accessible en recherche. Le lecteur ASF WM applique des horodatages aux échantillons de support en fonction de l’horodatage dans le fichier ASF, mais il ne modifie pas les horodatages de quelque manière que ce soit. En interne, le filtre utilise l’objet lecteur de format Windows Media pour lire le contenu Windows Media.

> [!Note]  
> Dans le kit de développement logiciel (SDK) DirectX, ce filtre n’est pas le filtre source par défaut pour les fichiers ASF. ainsi, avec ce kit de développement logiciel (SDK), vous ne pouvez pas utiliser ce filtre avec la méthode **RenderFile** . vous devez l’ajouter explicitement au graphique de filtre à l’aide de son identificateur de classe (CLSID). Ce comportement est différent avec le kit de développement logiciel (SDK) du format Windows Media. Lorsque vous installez les bibliothèques Runtime SDK du format Windows Media, le lecteur ASF WM est inscrit comme filtre par défaut pour les fichiers ASF.

 

Le tableau suivant contient des informations sur le filtre de lecteur ASF WM, telles que les interfaces et les types de médias qu’il prend en charge.



|                        |                                                                                                                                                                                                                                               |
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



 

## <a name="remarks"></a>Notes

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

[**Informations de référence sur DirectShow QASF**](directshow-qasf-reference.md)
</dt> <dt>

[**Lecture de fichiers ASF dans DirectShow**](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




