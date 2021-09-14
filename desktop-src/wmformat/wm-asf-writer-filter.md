---
title: filtre de rédacteur ASF WM (kit de développement logiciel (SDK) Windows Media Format 11)
description: en savoir plus sur le filtre d’enregistreur ASF WM pour le SDK Windows Media Format 11. Passez en revue les informations de filtre et consultez les rubriques connexes.
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- Windows Kit de développement logiciel (SDK) Media format, l’enregistreur ASF WM
- DirectShow, le rédacteur WM ASF
- Filtres QASF, rédacteur WM ASF
- Enregistreur ASF WM, à propos de
- ASF (Advanced Systems Format), le rédacteur WM ASF
- ASF (format des systèmes avancés), enregistreur ASF WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ee013b55455c3100ee23e076b767d70fb3ffda
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195892"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a>filtre de rédacteur ASF WM (kit de développement logiciel (SDK) Windows Media Format 11)

Le filtre d’enregistreur ASF WM accepte un nombre variable de flux d’entrée et crée un fichier ASF. Le filtre gère l’ensemble de la compression et du multiplexage (bien que le mécanisme de compression puisse être contourné). Vous pouvez utiliser le filtre de l’enregistreur ASF WM dans différents scénarios, notamment la capture vidéo numérique (DV), la recompression audio et la conversion de fichiers multimédias numériques Audio-Video entrelacés (AVI) ou MPEG pour la diffusion réseau. ce filtre offre la seule façon de créer des fichiers Microsoft Windows Media Audio et Windows Media Video dans DirectShow.

Pour plus d’informations, consultez [création de fichiers ASF dans DirectShow](creating-asf-files-in-directshow.md).

Le tableau suivant contient des informations sur le filtre de l’enregistreur ASF WM, comme les interfaces et les types de médias qu’il prend en charge.



| Informations de filtre                       |  Types                                                                                                                                                                                                                       |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre      | **IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2** |
| Types de média de broche d’entrée  | Dépend du profil. En général, les types non compressés comme \_ les signaux audio ou MediaType \_ vidéo, bien que les types compressés puissent être acceptés s’ils correspondent au profil                                                   |
| Interfaces pin d’entrée   | **IPIN**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (à l’aide de **IServiceProvider**)                                                                         |
| Types de média de broche de sortie | Non applicable                                                                                                                                                                                                          |
| Interfaces de broche de sortie  | Non applicable                                                                                                                                                                                                          |
| CLSID du filtre           | CLSID \_ WMAsfWriter                                                                                                                                                                                                      |
| CLSID de page de propriétés    | CLSID \_ WMAsfWriterProperties                                                                                                                                                                                            |
| Exécutable             | Qasf.dll                                                                                                                                                                                                                |
| Mérite                  | MÉRITE \_ n' \_ \_ utilise pas                                                                                                                                                                                                     |
| Catégorie de filtre        | Non spécifié                                                                                                                                                                                                           |



 

## <a name="remarks"></a>Notes

Le nombre de broches d’entrée sur le filtre dépend du profil qui est passé au filtre. Une broche du type de média approprié est créée pour chaque flux défini dans le profil.

Les broches d’entrée prennent en charge une méthode à partir de l’interface **IAMStreamConfig** : **IAMStreamConfig :: GetFormat**. Toutes les autres méthodes retournent E \_ NOTIMPL. Appelez la méthode **GetFormat** pour interroger le format de compression de destination du pin, qui est défini par le profil actuel. Utilisez l’interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) pour définir le profil.

l’interface **IServiceProvider** du filtre permet aux applications de récupérer l’interface [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) , qui est définie dans le kit de développement logiciel (SDK) de Format multimédia Windows. L’interface **IWMWriterAdvanced2** contrôle la désentrelacement vidéo, et est utile si l’entrée est une source [*entrelacée*](wmformat-glossary.md) , telle qu’une vidéo numérique. Utilisez les méthodes **GetInputSetting** et **SetInputSetting** pour contrôler l’entrelacement. Il n’est pas recommandé que les clients utilisent l’une des autres méthodes sur cette interface. Cette interface ne peut être obtenue qu’une fois que le filtre a été ajouté au graphique de filtre. L’exemple suivant montre comment interroger cette interface :


```C++
// Assume that m_pGraph is a valid IGraphBuilder interface pointer,
// and that pAsfWriter points to the IBaseFilter interface
// on the WM ASF Writer filter.

IServiceProvider *pProvider = NULL;
IWMWriterAdvanced2 *pWMWA2 = NULL;

hr = m_pGraph->AddFilter(pAsfWriter, L"WM ASF Writer");
...
hr = pAsfWriter->QueryInterface(IID_IServiceProvider, (void**)&pProvider)
if (SUCCEEDED(hr))
{
    hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
        IID_IWMWriterAdvanced2, (void**)&pWMWA2);
    pProvider->Release();
}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**DirectShow Référence QASF**](directshow-qasf-reference.md)
</dt> </dl>

 

 
