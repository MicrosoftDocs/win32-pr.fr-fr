---
description: Filtre d’enregistreur ASF WM
ms.assetid: 1b12f65f-8d77-4d38-aad9-92bb15cc0426
title: Filtre d’enregistreur ASF WM (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9281d09e609bd51bc0d0ab42291bd183e782df447e918d3c478e4e857063c21b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650820"
---
# <a name="wm-asf-writer-filter-directshow"></a>Filtre d’enregistreur ASF WM (DirectShow)

l’enregistreur ASF WM est un filtre de wrapper pour l’objet Writer fourni avec le kit de développement logiciel (SDK) Windows Media™ Format. Le filtre accepte un nombre variable de flux d’entrée et crée un fichier ASF (Advanced Systems Format). Le filtre gère l’ensemble de la compression et du multiplexage (bien que le mécanisme de compression puisse être contourné). Vous pouvez utiliser l’enregistreur ASF WM dans différents scénarios, y compris la capture vidéo numérique (DV), la recompression audio et la conversion de fichiers multimédias Audio-Video entrelacés (AVI) ou MPEG pour la diffusion réseau. ce filtre offre la seule façon de créer des fichiers microsoft® Windows Media™ Audio et Windows Media Video dans microsoft DirectShow.

Pour plus d’informations, consultez [création de fichiers ASF dans DirectShow](creating-asf-files-in-directshow.md).



| Étiquette | Valeur |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter), [**IConfigAsfWriter2**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter2), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), **IPersistStream**, **IServiceProvider**, **ISpecifyPropertyPages** de plus, le filtre expose les interfaces suivantes Windows Media Format SDK : **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**<br/> |
| Types de média de broche d’entrée                    | Dépend du profil ASF. En général, les types audio et vidéo non compressés, bien que le filtre accepte les types compressés s’ils correspondent au profil ASF.                                                                                                                                                                                                                                                                                                                                             |
| Interfaces pin d’entrée                     | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), **IServiceProvider** en outre, le code confidentiel expose les éléments suivants Windows interface du kit de développement logiciel (SDK) Media Format : **IWMStreamConfig2** (via **IServiceProvider**)<br/>                                                                                                                                                                                 |
| Types de média de broche de sortie                   | Non applicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Interfaces de broche de sortie                    | Non applicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| CLSID du filtre                             | CLSID \_ WMAsfWriter                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CLSID de page de propriétés                      | CLSID \_ AsfWriterProperties                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Exécutable                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Mérite](merit.md)                       | MÉRITE \_ n' \_ \_ utilise pas                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Catégorie de filtre](filter-categories.md) | Non spécifié                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Remarques

le filtre requiert le kit de développement logiciel (SDK) Windows Media Format et ses dépendances sous-jacentes.

Le nombre de broches d’entrée sur le filtre dépend de l’identificateur de profil ou de profil du flux ASF.

Les broches d’entrée prennent en charge une méthode à partir de l’interface **IAMStreamConfig** : [**IAMStreamConfig :: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat). Toutes les autres méthodes retournent E \_ NOTIMPL. Appelez la méthode **GetFormat** pour interroger le format de compression de destination du pin, qui est défini par le profil ASF actuel. Utilisez l’interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) pour définir le profil.

vous pouvez utiliser l’interface **IServiceProvider** du filtre pour obtenir un pointeur vers l’interface **IWMWriterAdvanced2** , qui est définie dans le kit de développement logiciel (SDK) de Format multimédia Windows. Vous pouvez utiliser l’interface **IWMWriterAdvanced2** pour contrôler le désentrelacement vidéo lorsque la vidéo source est entrelacée. Pour définir le mode de désentrelacement, appelez **IWMWriterAdvanced2 :: SetInputSetting**. Pour le paramètre *dwInputNum* , utilisez l’index de base zéro de la broche d’entrée vidéo, tel qu’il est énuméré par l’interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .

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

lorsque le runtime SDK Windows Media Format envoie des \_ messages d’état WMT au filtre de l’enregistreur ASF WM, le filtre les transfère en tant qu’événements d' [**\_ \_ événements**](ec-wmt-event.md) de l’échange de fichiers de l’échange de fichiers.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 




