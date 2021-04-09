---
description: Le filtre EVR (Enhanced Video Renderer) est un mélangeur vidéo à 16 canaux et un convertisseur. Il a les mêmes fonctionnalités de base et le même modèle de plug-in que le récepteur multimédia Media Foundation EVR.
ms.assetid: ead99cb3-2be2-42c6-ac22-be0c2ddf28d5
title: Filtre de convertisseur vidéo amélioré
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ba6e7c14386ea37424364274263859844182ed7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033466"
---
# <a name="enhanced-video-renderer-filter"></a>Filtre de convertisseur vidéo amélioré

> [!Note]  
> Cette rubrique s’applique à Windows Vista et versions ultérieures.

 

Le filtre EVR (Enhanced Video Renderer) est un mélangeur vidéo à 16 canaux et un convertisseur. Il a les mêmes fonctionnalités de base et le même modèle de plug-in que le récepteur multimédia Media Foundation EVR.

Le filtre DirectShow EVR est documenté dans la documentation du kit de développement logiciel (SDK) Media Foundation ; Pour plus d’informations, consultez [rendu vidéo amélioré](../medfound/enhanced-video-renderer.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtre (via <strong>QueryInterface</strong>)</td>
<td>Interfaces DirectShow :
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li>
<li><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>IMediaEventSink</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></li>
</ul>
Interfaces de Media Foundation :<br/>
<ul>
<li><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a></li>
<li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></li>
<li><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a></li>
<li><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Types de média de broche d’entrée</td>
<td>Variable, en fonction du pilote Graphics.</td>
</tr>
<tr class="odd">
<td>Interfaces pin d’entrée (via <strong>QueryInterface</strong>)</td>
<td>Interfaces DirectShow :
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li>
</ul>
Interfaces de Media Foundation :<br/>
<ul>
<li><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a></li>
<li><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a></li>
<li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Types de média de broche de sortie</td>
<td>Non applicable.</td>
</tr>
<tr class="odd">
<td>Interfaces de broche de sortie</td>
<td>Non applicable.</td>
</tr>
<tr class="even">
<td>CLSID du filtre</td>
<td>CLSID_EnhancedVideoRenderer</td>
</tr>
<tr class="odd">
<td>Exécutable</td>
<td>evr.dll</td>
</tr>
<tr class="even">
<td><a href="merit.md">Mérite</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="odd">
<td><a href="filter-categories.md">Catégorie de filtre</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Notes

En plus des interfaces exposées via **QueryInterface**, EVR expose d’autres interfaces par le biais de la méthode [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) . Certaines de ces interfaces sont implémentées par le présentateur EVR ou le mélangeur EVR, plutôt que par le EVR lui-même. Si l’application définit un présentateur ou un mélangeur personnalisé sur le EVR, les versions personnalisées peuvent exposer un autre ensemble d’interfaces.



| Object     | Identificateur de service                                              | Interfaces                                                                                                                                                                                                                                                                                                     |
|------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtre EVR | \_ \_ Service de rendu vidéo Mr \_ (requêtes EVR ou Presenter)<br/> | [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)<br/> [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)<br/>                                                          |
| Filtre EVR | \_ \_ Service accélérateur vidéo Mr \_ (requêtes Presenter)<br/>  | [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)                                                                                                                                                                                                                                                      |
| Filtre EVR | \_ \_ Service de mixage vidéo Mr \_ (mélangeur de requêtes)<br/>             | [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)<br/> [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)<br/> [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)<br/> |
| Broches d’entrée | \_ \_ service accélérateur vidéo \_ Mr                                | [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                                                                                                                                                                                                    |



 

Le EVR peut combiner jusqu’à 16 flux vidéo. Le premier flux d’entrée (broche 0) est appelé le *flux de référence*. Le flux de référence apparaît toujours en premier dans l’ordre de plan. Tous les flux supplémentaires sont appelés des sous-flux et sont mélangés au-dessus du flux de référence. L’application peut modifier l’ordre de plan des sous-flux, mais aucun sous-flux ne peut être d’abord dans l’ordre de plan.

Le pilote Graphics détermine les formats vidéo pris en charge, mais ils sont généralement limités aux éléments suivants :

-   Flux de référence : YUV progressif ou entrelacé, sans alpha par pixel (comme NV12 ou YUY2); ou RGB progressif.
-   Sous-flux : YUV progressifs avec par pixel-alpha, tels que AYUV ou AI44.

Les formats de sous-flux disponibles peuvent dépendre du format du flux de référence.

EVR transfère les commandes de recherche en amont via la broche 0. Les broches de sous-flux ne transfèrent pas les commandes de recherche. Il incombe au filtre de la source ou du séparateur de conserver les sous-flux synchronisés avec le flux de référence.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

