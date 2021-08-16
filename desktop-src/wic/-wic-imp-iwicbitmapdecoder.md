---
description: Implémentation de IWICBitmapDecoder
ms.assetid: 9e316bdd-803a-47af-b004-7675478eb829
title: Implémentation de IWICBitmapDecoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0088b756a7a30134224e32fa67ee891f2c48339f9af70447cb760915ad420619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711146"
---
# <a name="implementing-iwicbitmapdecoder"></a>Implémentation de IWICBitmapDecoder

## <a name="iwicbitmapdecoder"></a>IWICBitmapDecoder

Quand une application demande un décodeur, le premier point d’interaction avec le codec se fait par le biais de l’interface [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) . Il s’agit de l’interface au niveau du conteneur qui fournit l’accès aux propriétés de niveau supérieur du conteneur et, plus important encore, aux frames qu’elle contient. Il s’agit de l’interface principale sur votre classe de décodeur au niveau du conteneur.

``` syntax
interface IWICBitmapDecoder : IUnknown
{
// Required methods
   HRESULT QueryCapability (IStream *pIStream, 
      DWORD *pdwCapabilities );
   HRESULT Initialize ( IStream *pIStream,
      WICDecodeOptions cacheOptions );
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetDecoderInfo ( IWICBitmapDecoderInfo **pIDecoderInfo );
   HRESULT GetFrameCount ( UINT *pCount );
   HRESULT GetFrame ( UINT index, 
      IWICBitmapFrameDecode **ppIBitmapFrame );

// Optional methods
   HRESULT GetPreview ( IWICBitmapSource **ppIPreview );
   HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
   HRESULT GetColorContexts ( UINT cCount, 
      IWICColorContext **ppIColorContexts, 
      UINT *pcActualCount );
   HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader);
   HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

Certains formats d’image ont des miniatures globales, des contextes de couleur ou des métadonnées, tandis que de nombreux formats d’image les fournissent uniquement pour chaque image. Les méthodes d’accès à ces éléments sont facultatives sur [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder), mais elles sont requises sur [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode). De même, certains codecs n’utilisent pas les formats de pixel indexés et n’ont donc pas besoin d’implémenter les méthodes [CopyPalette](-wic-imp-iwicbitmapframedecode.md) sur l’une ou l’autre des interfaces. Pour plus d’informations sur les méthodes **IWICBitmapDecoder** facultatives, consultez [implémentation de IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md), où elles sont le plus souvent implémentées.

### <a name="querycapability"></a>QueryCapability

[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) est la méthode utilisée pour l’arbitrage du codec. (pour plus d’informations, consultez [découverte et arbitrage](-wic-howwicworks.md) dans la rubrique fonctionnement [du composant de création d’images Windows](-wic-howwicworks.md) ). Si deux codecs sont capables de décoder le même format d’image, ou si une collision de modèle se produit dans laquelle deux codecs utilisent le même modèle d’identification, cette méthode vous permet de sélectionner le codec qui peut gérer au mieux une image spécifique.

lors de l’appel de cette méthode, Windows composant de création d’images (WIC) vous transmet le flux réel contenant l’image. Vous devez vérifier si vous pouvez décoder chaque frame dans l’image et énumérer les blocs de métadonnées, pour déclarer avec précision les fonctionnalités de ce décodeur par rapport au flux de fichier spécifique qui lui est passé. Cela est important pour tous les décodeurs, mais particulièrement important pour les formats d’image basés sur des conteneurs TIFF (Tagged Image File Format). Le processus de découverte fonctionne en faisant correspondre les modèles associés aux décodeurs dans le registre aux modèles dans le fichier image réel. La déclaration de votre modèle d’identification dans le registre garantit que votre décodeur sera toujours détecté pour les images dans votre format d’image. Toutefois, votre décodeur peut toujours être détecté pour les images dans d’autres formats. Par exemple, tous les conteneurs TIFF incluent le modèle TIFF, qui est un modèle d’identification valide pour le format d’image TIFF. Cela signifie que, pendant la découverte, au moins deux modèles d’identification se trouvent dans les fichiers image pour tout format d’image basé sur un conteneur de style TIFF. L’un est le modèle TIFF et l’autre est le modèle de format d’image réel. Bien qu’il soit moins probable, il peut y avoir des collisions de modèles entre d’autres formats d’image non liés. C’est pourquoi la découverte et l’arbitrage sont un processus en deux étapes. Vérifiez toujours que le flux d’image transmis à [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) est en fait une instance valide de votre propre format d’image. En outre, si votre codec décode un format d’image pour lequel vous n’êtes pas propriétaire de la spécification, votre implémentation de **QueryCapability** doit vérifier la présence de toute fonctionnalité qui peut être valide sous la spécification de format d’image que votre CODEC n’implémente pas. Cela permet de s’assurer que les utilisateurs ne subissent pas de décodage inutile ou obtiennent des résultats inattendus avec votre codec.

Avant d’effectuer une opération sur l’image, vous devez enregistrer la position actuelle du flux afin de pouvoir la restaurer à sa position d’origine avant de retourner à partir de la méthode. L’énumération [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) qui spécifie les fonctionnalités est définie comme suit :

``` syntax
enum WICBitmapDecoderCapabilities
{   
   WICBitmapDecoderCapabilitySameEncoder,
   WICBitmapDecoderCapabilityCanDecodeAllImages,
   WICBitmapDecoderCapabilityCanDecodeSomeImages,
   WICBitmapDecoderCapabilityCanEnumerateMetadata,
   WICBitmapDecoderCapabilityCanDecodeThumbnail
}
```

Vous devez déclarer **WICBitmapDecoderCapabilitySameEncoder** uniquement si votre encodeur était celui qui encodé l’image. Après avoir vérifié si vous pouvez décoder chaque frame dans le conteneur, déclarez **WICBitmapDecoderCapabilityCanDecodeSomeImages** si vous pouvez décoder certains des frames, mais pas tous, **WICBitmapDecoderCapabilityCanDecodeAllImages** si vous pouvez décoder tous les frames, ou si vous ne pouvez pas les décoder. (Ces deux énumérations s’excluent mutuellement ; si vous retournez **WICBitmapDecoderCapabilityCanDecodeAllImages**, **WICBitmapDecoderCapabilityCanDecodeSomeImages** sera ignoré.) Déclarez **WICBitmapDecoderCapabilityCanEnumerateMetadata** après avoir vérifié que vous pouvez énumérer les blocs de métadonnées dans le conteneur d’images. Vous n’avez pas besoin de rechercher une miniature dans chaque cadre. S’il existe une miniature globale et que vous pouvez la décoder, vous pouvez déclarer **WICBitmapDecoderCapabilityCanDecodeThumbnail**. S’il n’y a aucune miniature globale, essayez de décoder la miniature pour le frame 0. S’il n’y a aucune miniature à l’un de ces emplacements, ne déclarez pas cette fonctionnalité.

Après avoir déterminé les fonctionnalités du décodeur par rapport au flux d’image passé à cette méthode, effectuez une opération ou avec le [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) vous avez vérifié que ce décodeur peut effectuer sur cette image et retourner le résultat. N’oubliez pas de restaurer le flux à sa position d’origine avant de retourner.

### <a name="initialize"></a>Initialiser

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) est appelé par une application après qu’un décodeur a été sélectionné pour décoder une image spécifique. Le flux d’image est passé au décodeur et un appelant peut éventuellement spécifier l’option de cache [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) pour gérer les métadonnées dans le fichier.

``` syntax
enum WICDecodeOptions
{
   WICDecodeMetadataCacheOnDemand,
   WICDecodeMetadataCacheOnLoad
}
```

Certaines applications utilisent les métadonnées plus que d’autres. La plupart des applications n’ont pas besoin d’accéder à toutes les métadonnées d’un fichier image et demandent des métadonnées spécifiques en fonction de leurs besoins. D’autres applications préfèrent mettre en cache toutes les métadonnées en amont, de garder le flux de fichier ouvert et d’exécuter des e/s de disque chaque fois qu’ils ont besoin d’accéder aux métadonnées. Si l’appelant ne spécifie pas une option de cache des métadonnées, le comportement de mise en cache par défaut doit être cache à la demande. Cela signifie qu’aucune métadonnée ne doit être chargée en mémoire tant que l’application n’a pas effectué une demande spécifique pour ces métadonnées. Si l’application spécifie **WICDecodeMetadataCacheOnLoad**, les métadonnées doivent être chargées en mémoire immédiatement et mises en cache. Lorsque les métadonnées sont mises en cache lors du chargement, le flux de fichier peut être libéré une fois que les métadonnées ont été mises en cache.

### <a name="getcontainerformat"></a>GetContainerFormat

Pour implémenter [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat), il suffit de retourner le GUID du format d’image de l’image pour laquelle le décodeur est instancié. Cette méthode est également implémentée sur [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) et [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).

### <a name="getdecoderinfo"></a>GetDecoderInfo

[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) retourne un objet [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) . Pour obtenir l’objet **IWICBitmapDecoderInfo** , il vous suffit de transmettre le GUID de votre décodeur à la méthode [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) sur [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), puis de demander l’interface **IWICBitmapDecoderInfo** sur ce dernier, comme illustré dans l’exemple suivant.


```C++
IWICComponentInfo* pComponentInfo = NULL;
HRESULT hr;
 
hr = m_pImagingFactory->CreateComponentInfo(CLSID_This, &pComponentInfo);

hr = pComponentInfo->QueryInterface(IID_IWICBitmapDecoderInfo, (void**)ppIDecoderInfo);

```



### <a name="getframecount"></a>GetFrameCount

[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) retourne simplement le nombre de frames dans le conteneur. Certains formats de conteneur prennent en charge plusieurs frames, tandis que d’autres ne prennent en charge qu’une seule trame par conteneur.

### <a name="getframe"></a>GetFrame

[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) est une méthode importante sur l’interface [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) , car le frame contient les bits d’image réels, et l’objet décodeur de trame retourné par cette méthode est l’objet qui effectue le décodage réel de l’image demandée. Il s’agit de l’autre objet que vous devez implémenter lors de l’écriture d’un décodeur. Pour plus d’informations sur les décodeurs de frame, consultez [Implementing IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md).

### <a name="getpreview"></a>GetPreview

[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) retourne un aperçu de l’image. Pour obtenir une présentation détaillée des préversions, consultez la méthode [Implementing IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) sur l’interface [Implementing IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) .

Si votre format d’image contient une préversion JPEG incorporée, il est fortement recommandé, au lieu d’écrire un décodeur JPEG pour le décoder, de déléguer le décodeur JPEG fourni avec la plateforme WIC pour le décodage des aperçus et des miniatures. Pour ce faire, recherchez le début des données de l’image d’aperçu dans le flux et appelez la méthode [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) sur [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).


```C++
IWICBitmapDecoder* pPreviewDecoder = NULL;
IWICBitmapFrameDecode* pPreviewFrame = NULL;
IWICBitmapSource* pPreview = NULL;
HRESULT hr;

hr = m_pImagingFactory->CreateDecoderFromStream(
                               m_pStream, NULL, 
                               WICDecodeMetadataCacheOnDemand, &pPreviewDecoder);
hr = pPreviewDecoder->GetFrame(0, pPreviewFrame);
hr = pPreviewFrame->QueryInterface(IID_IWICBitmapSource, (void**)&pPreview);

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Interfaces de décodeur](-wic-decoderinterfaces.md)
</dt> <dt>

[Implémentation de IWICBitmapCodecProgressNotification (décodeur)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



