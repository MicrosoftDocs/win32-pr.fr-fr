---
description: Filtre d’enregistreur ASF WM
ms.assetid: 1b12f65f-8d77-4d38-aad9-92bb15cc0426
title: Filtre de rédacteur ASF WM (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf09a99673b07e88198fd57b95a766ce821eb02
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909277"
---
# <a name="wm-asf-writer-filter-directshow"></a>Filtre de rédacteur ASF WM (DirectShow)

L’enregistreur ASF WM est un filtre de wrapper pour l’objet Writer fourni avec le kit de développement logiciel (SDK) du format Windows Media™. Le filtre accepte un nombre variable de flux d’entrée et crée un fichier ASF (Advanced Systems Format). Le filtre gère l’ensemble de la compression et du multiplexage (bien que le mécanisme de compression puisse être contourné). Vous pouvez utiliser l’enregistreur ASF WM dans différents scénarios, y compris la capture vidéo numérique (DV), la recompression audio et la conversion de fichiers multimédias Audio-Video entrelacés (AVI) ou MPEG pour la diffusion réseau. Ce filtre offre la seule façon de créer des fichiers audio et Windows Media Video Microsoft® Windows Media™ dans Microsoft DirectShow.

Pour plus d’informations, consultez [création de fichiers ASF dans DirectShow](creating-asf-files-in-directshow.md).



| Étiquette | Valeur |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter), [**IConfigAsfWriter2**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter2), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), **IPersistStream**, **IServiceProvider**, **ISpecifyPropertyPages** de plus, le filtre expose les interfaces du kit de développement logiciel (SDK) du format Windows Media suivantes : **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**<br/> |
| Types de média de broche d’entrée                    | Dépend du profil ASF. En général, les types audio et vidéo non compressés, bien que le filtre accepte les types compressés s’ils correspondent au profil ASF.                                                                                                                                                                                                                                                                                                                                             |
| Interfaces pin d’entrée                     | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), **IServiceProvider** en outre, le code confidentiel expose l’interface du kit de développement logiciel (SDK) du format Windows Media suivante : **IWMStreamConfig2** (via **IServiceProvider**)<br/>                                                                                                                                                                                 |
| Types de média de broche de sortie                   | Non applicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Interfaces de broche de sortie                    | Non applicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| CLSID du filtre                             | CLSID \_ WMAsfWriter                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CLSID de page de propriétés                      | CLSID \_ AsfWriterProperties                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Exécutable                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Mérite](merit.md)                       | MÉRITE \_ n' \_ \_ utilise pas                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Catégorie de filtre](filter-categories.md) | Non spécifié                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Remarques

Le filtre requiert le kit de développement logiciel (SDK) du format Windows Media et ses dépendances sous-jacentes.

Le nombre de broches d’entrée sur le filtre dépend de l’identificateur de profil ou de profil du flux ASF.

Les broches d’entrée prennent en charge une méthode à partir de l’interface **IAMStreamConfig** : [**IAMStreamConfig :: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat). Toutes les autres méthodes retournent E \_ NOTIMPL. Appelez la méthode **GetFormat** pour interroger le format de compression de destination du pin, qui est défini par le profil ASF actuel. Utilisez l’interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) pour définir le profil.

Vous pouvez utiliser l’interface **IServiceProvider** du filtre pour obtenir un pointeur vers l’interface **IWMWriterAdvanced2** , qui est définie dans le kit de développement logiciel (SDK) du format Windows Media. Vous pouvez utiliser l’interface **IWMWriterAdvanced2** pour contrôler le désentrelacement vidéo lorsque la vidéo source est entrelacée. Pour définir le mode de désentrelacement, appelez **IWMWriterAdvanced2 :: SetInputSetting**. Pour le paramètre *dwInputNum* , utilisez l’index de base zéro de la broche d’entrée vidéo, tel qu’il est énuméré par l’interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .

L’exemple suivant montre comment interroger cette interface :


```C++
// Assume that pAsfWriter is a valid IBaseFilter pointer.
IServiceProvider *pProvider = NULL;
IWMWriterAdvanced2 *pWMWA2 = NULL;

hr = pAsfWriter->QueryInterface(
    IID_IServiceProvider, 
    (void**)&pProvider
    );
if (SUCCEEDED(hr))
{
    hr = pProvider->QueryService(
        IID_IWMWriterAdvanced2,
        IID_IWMWriterAdvanced2, 
        (void**)&pWMWA2
        );
    pProvider->Release();
    if (SUCCEEDED(hr))
    {
        // Use pWMWA2. (Not shown.)
        pWMWA2->Release();
    }
}
```



Les applications ne doivent pas utiliser les méthodes **IWMWriterAdvanced** héritées par l’interface **IWMWriterAdvanced2** . L’appel de ces méthodes pourrait interere avec le fonctionnement du filtre.

Le seul mode d’écriture de fichier pris en charge par ce filtre est le remplacement des \_ fichiers am \_ . Consultez [**IFileSinkFilter2 :: GetMode**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter2-getmode).

Lorsque le runtime du SDK Windows Media format envoie des \_ messages d’État WMT au filtre de l’enregistreur ASF WM, le filtre les transfère en tant qu’événements d' [**\_ \_ événements**](ec-wmt-event.md) de l’échange de fichiers de la norme ec.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 




