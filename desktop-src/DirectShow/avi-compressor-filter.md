---
description: Filtre de compresseur AVI
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: Filtre de compresseur AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa074f5ad4a72fe1e1a32f45baa4888a526b1a0532a562c2fadb7753ea71e0aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159271"
---
# <a name="avi-compressor-filter"></a>Filtre de compresseur AVI

Le filtre de compresseur AVI permet aux codecs du gestionnaire de compression vidéo (VCM) de joindre un graphique de filtres. Chaque codec apparaît sous la forme d’une instance distincte du filtre. Vous ne pouvez pas créer directement ce filtre avec CoCreateInstance. Au lieu de cela, vous devez utiliser l’énumérateur du périphérique système. Pour plus d’informations, consultez [utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md).

La broche d’entrée du filtre se connecte aux filtres qui génèrent des données vidéo non compressées, telles que les filtres de capture vidéo ou le [filtre de séparateur AVI](avi-splitter-filter.md). La broche de sortie du filtre se connecte généralement à un filtre MUX, tel que le [filtre multiplex MUX](avi-mux-filter.md).

Si le codec prend en charge une boîte de dialogue de configuration de VFW de style ancien ou une boîte de dialogue à propos de, une application peut l’afficher à l’aide de l’interface [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) .

> [!Note]  
> les compresseurs MPEG ne sont jamais implémentés en tant que codecs VCM, mais uniquement en tant que filtres de DirectShow natifs.

 



| Étiquette | Valeur |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages                                                                                                             |
| Types de média de broche d’entrée                    | \_Vidéo MediaType, MEDIASUBTYPE \_ null                                                                                                                                                                                                               |
| Interfaces pin d’entrée                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Types de média de broche de sortie                   | \_Vidéo MediaType, MEDIASUBTYPE \_ null                                                                                                                                                                                                               |
| Interfaces de broche de sortie                    | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID du filtre                             | Non applicable                                                                                                                                                                                                                                     |
| CLSID de page de propriétés                      | Aucune page de propriétés.                                                                                                                                                                                                                                  |
| Exécutable                               | qcap.dll                                                                                                                                                                                                                                           |
| [Mérite](merit.md)                       | MÉRITE \_ n' \_ \_ utilise pas                                                                                                                                                                                                                                |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ VideoCompressorCategory                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 



