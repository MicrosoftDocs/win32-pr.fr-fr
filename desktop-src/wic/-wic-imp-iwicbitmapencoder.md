---
description: Implémentation de IWICBitmapEncoder
ms.assetid: b671e941-ded6-4bde-bc4d-461f13feade0
title: Implémentation de IWICBitmapEncoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d02105470f837dba0689b665473c01c42f6cd6497a85424ea6eea3371696f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088011"
---
# <a name="implementing-iwicbitmapencoder"></a>Implémentation de IWICBitmapEncoder

-   [IWICBitmapEncoder](#implementing-iwicbitmapencoder)
    -   [Initialiser](#initialize)
    -   [GetContainerFormat](#getcontainerformat)
    -   [GetEncoderInfo](#getencoderinfo)
    -   [CreateNewFrame](#createnewframe)
    -   [Commiter](#commit)
    -   [SetPreview](#setpreview)
-   [Rubriques connexes](#related-topics)

## <a name="iwicbitmapencoder"></a>IWICBitmapEncoder

-   [Initialiser](#initialize)
-   [GetContainerFormat](#getcontainerformat)
-   [GetEncoderInfo](#getencoderinfo)
-   [CreateNewFrame](#createnewframe)
-   [Commiter](#commit)
-   [SetPreview](#setpreview)

Cette interface est l’équivalent de l’interface [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) et est le point de départ pour l’encodage d’un fichier image. Tout comme **IWICBitmapDecoder** est utilisé pour récupérer des propriétés au niveau du conteneur et des frames individuels à partir du conteneur d’images, [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) est utilisé pour définir les propriétés au niveau du conteneur et sérialiser les trames d’image individuelles dans le conteneur. Vous implémentez cette interface sur votre classe d’encodeur au niveau du conteneur.

``` syntax
interface IWICBitmapEncoder : public IUnknown
{
   // Required methods
   HRESULT Initialize ( IStream *pIStream,
              WICBitmapEncoderCacheOption cacheOption );
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetEncoderInfo ( IWICBitmapEncoderInfo **pIEncoderInfo );
   HRESULT CreateNewFrame ( IWICBitmapFrameEncode **ppIFrameEncode,
              IPropertyBag2 **ppIEncoderOptions );
   HRESULT Commit ( void );

   // Optional methods
   HRESULT SetPreview ( IWICBitmapSource *pIPreview );
   HRESULT SetThumbnail ( IWICBitmapSource *pIThumbnail );
   HRESULT SetColorContexts ( UINT cCount,
              IWICColorContext **ppIColorContext );
   HRESULT GetMetadataQueryWriter ( IWICMetadataQueryWriter 
              **ppIMetadataQueryWriter );
   HRESULT SetPalette ( IWICPalette *pIPalette);
};
```

Comme nous l’avons vu dans [implémentation de IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md), certains formats d’image ont des miniatures globales, des contextes de couleur ou des métadonnées, tandis que de nombreux formats d’image les fournissent uniquement pour chaque image. Par conséquent, les méthodes de définition de ces options sont facultatives sur [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder), mais elles sont requises sur [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode). Nous allons aborder les méthodes facultatives sur **IWICBitmapEncoder** dans la section sur **IWICBitmapFrameEncode**, où elles sont le plus souvent implémentées.

Si vous ne prenez pas en charge les miniatures globales, retournez WINCODEC \_ Err \_ CODECNOTHUMBNAIL à partir de la méthode SetThumbnail sur [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder). Si vous ne prenez pas en charge une palette au niveau du conteneur, ou si l’image que vous encodez n’a pas de format indexé, retournez WINCODEC \_ Err \_ PALETTEUNAVAILABLE à partir de la méthode SetPalette. Pour toute autre méthode non prise en charge, retournez WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.

### <a name="initialize"></a>Initialiser

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) est la première méthode appelée sur un [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) une fois qu’elle a été instanciée. Un flux d’image est passé à l’encodeur et un appelant peut éventuellement spécifier une option de cache. Dans le cas du décodeur, le flux est en lecture seule, mais le flux passé à un encodeur est un flux accessible en écriture, dans lequel l’encodeur sérialise toutes les données et métadonnées de l’image. Les options de cache sur l’encodeur sont également différentes.

``` syntax
enum WICBitmapEncoderCacheOption
{
   WICBitmapEncoderCacheInMemory,
   WICBitmapEncoderCacheTempFile,
   WICBitmapEncoderNoCache
}
```

L’application a la possibilité de demander à l’encodeur de mettre en cache les données de l’image en mémoire, de les mettre en cache dans un fichier temporaire ou de les écrire directement dans le fichier de disque sans mise en cache. Lorsque vous êtes invité à mettre en cache les données dans un fichier temporaire, l’encodeur doit créer un fichier temporaire sur le disque et écrire directement dans ce fichier sans mise en cache en mémoire. Lorsque l’appelant sélectionne l’option no cache, chaque frame doit être validé dans l’ordre avant de pouvoir créer le frame suivant.

### <a name="getcontainerformat"></a>GetContainerFormat

[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat) est implémenté de la même façon que la méthode [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) lors de l' [implémentation de IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).

### <a name="getencoderinfo"></a>GetEncoderInfo

[**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) retourne un objet [**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo) . Pour obtenir l’objet **IWICBitmapEncoderInfo** , il vous suffit de transmettre le GUID de votre encodeur à la méthode [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) sur [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), puis de demander l’interface **IWICBitmapEncoderInfo** .

Consultez l’exemple dans [Implementing IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) sous [GetDecoderInfo](-wic-imp-iwicbitmapdecoder.md).

### <a name="createnewframe"></a>CreateNewFrame

[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) est l’équivalent de l’encodeur de [**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) sur [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder). Cette méthode retourne un objet [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) , qui est l’objet qui sérialise réellement les données d’image pour un frame spécifique dans le conteneur.

l’un des avantages du composant WIC (Windows Imaging Component) est qu’il fournit une couche d’abstraction pour les applications qui leur permet de travailler avec tous les formats d’image de la même façon. Toutefois, tous les formats d’image ne sont pas exactement identiques. Certains formats d’image ont des fonctionnalités que d’autres n’ont pas. Pour que les applications puissent tirer parti de ces fonctionnalités uniques, il est nécessaire de fournir un moyen de les exposer au codec. C’est l’objectif des options de l’encodeur. Si votre CODEC prend en charge les options de l’encodeur, vous devez créer un objet [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) qui expose les options d’encodeur que vous prenez en charge et le retourner dans le paramètre *ppIEncoderOptions* de cette méthode. L’appelant peut ensuite utiliser cet objet IPropertyBag2 pour déterminer les options de codeur prises en charge par votre codec. Si l’appelant souhaite spécifier des valeurs pour l’une des options d’encodeur prises en charge, il assignera la valeur à la propriété appropriée dans l’objet IPropertyBag2 et la passera à l’objet [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) nouvellement créé dans sa méthode Initialize.

Pour instancier un objet [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) , vous devez d’abord créer un struct PROPBAG2 pour spécifier chaque option d’encodeur prise en charge par votre encodeur et son type de données pour chaque propriété. Vous devez ensuite implémenter un objet IPropertyBag2 qui applique les plages de valeurs pour chaque propriété lors de l’écriture, et rapproche toutes les valeurs en conflit ou en chevauchement. Pour les ensembles simples d’options d’encodeur non conflictuelles, vous pouvez appeler la méthode [**CreateEncoderPropertyBag**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createencoderpropertybag) , qui créera un objet IPropertyBag2 simple à l’aide des propriétés que vous spécifiez dans votre struct PROPBAG2. Vous devez toujours appliquer les plages de valeurs. Pour obtenir des options d’encodeur plus avancées, ou si vous devez rapprocher des valeurs conflictuelles, vous devez écrire votre propre implémentation de IPropertyBag2.


```C++
UINT cuiPropertyCount = 0;
IPropertyBag2* pPropertyBag = NULL;
PROPBAG2* pPropBagOptions;
HRESULT hr;

// Insert code here to initialize piPropertyBag with the 
// supported options for your encoder, and to initialize 
// cuiPropertyCount to the number of encoder option properties
// you are exposing.
...

hr = pComponentFactory->CreateEncoderPropertyBag( 
   pPropBagOptions, cuiPropertyCount, &pPropertyBag);
```



WIC fournit un petit ensemble d’options de codeur canoniques utilisées par certains formats d’image courants. Toutes les options de codeur canoniques sont facultatives, et les codecs ne sont pas nécessaires pour prendre en charge l’un d’eux. La raison pour laquelle elles sont fournies en tant qu’options canoniques est que de nombreuses applications exposent l’interface utilisateur pour que les utilisateurs spécifient ces options lors de l’enregistrement d’un fichier image dans un format qui les prend en charge. Le fait de fournir une méthode canonique de spécification de ces options permet aux applications de les communiquer facilement aux encodeurs de manière cohérente. Les options de codeur canoniques sont répertoriées dans le tableau suivant.



| Option d’encodeur     | VARTYPE  | Plage de valeurs               |
|--------------------|----------|---------------------------|
| Lossless           | VT \_ bool | Vrai/Faux                |
| ImageQuality       | VT \_ R4   | 0.0-1.0                   |
| CompressionQuality | VT \_ R4   | 0.0-1.0                   |
| BitmapTransform    | \_UI1 VT  | WICBitmapTransformOptions |



 

Si votre CODEC prend en charge l’encodage sans perte, vous devez exposer l’option d’encodeur sans perte comme un moyen pour les applications de demander qu’une image soit encodée sans perte de code. Si un appelant affecte la valeur true à cette propriété, vous devez ignorer l’option ImageQuality et encoder l’image sans perte.

L’option ImageQuality permet à une application de spécifier le degré de fidélité avec lequel encoder l’image. Cette option permet à un utilisateur de faire un compromis entre la qualité de l’image et la vitesse et/ou la taille du fichier. JPEG est un exemple de format d’image qui prend en charge ce compromis. Une valeur de 0,0 indique que la fidélité est faible et que l’encodeur doit utiliser l’algorithme le plus perdu. Une valeur de 1,0 indique que la fidélité est la plus importante et que l’encodeur doit préserver la fidélité la plus élevée possible. (En fonction de votre codec, cela peut être synonyme de l’option Lossless. Toutefois, si votre CODEC prend en charge l’encodage sans perte, et si l’option Lossless est définie sur true, l’option ImageQuality doit être ignorée.)

L’option CompressionQuality permet à une application de spécifier l’efficacité de la compression à utiliser lors de l’encodage de l’image. Un algorithme très efficace peut produire un fichier image plus petit avec la même qualité qu’un algorithme de compression moins efficace, mais peut nécessiter plus de temps pour l’encodage. Cette option permet à un utilisateur de spécifier un compromis entre la taille de fichier et la vitesse d’encodage, tout en conservant le même niveau de qualité. TIFF est un exemple de format d’image qui prend en charge ce compromis. (Notez qu’un format tel que JPEG prend en charge différents niveaux de compression, mais un taux de compression plus élevé entraîne une qualité d’image inférieure. Par conséquent, un format d’image JPEG expose l’option ImageQuality au lieu de l’option CompressionQuality.) Une valeur de 0,0 pour cette option indique que vous devez compresser l’image aussi rapidement que possible, sans réduire la fidélité, au détriment d’une plus grande taille de fichier. Une valeur de 1,0 indique que vous devez créer la plus petite taille de fichier possible (au même niveau de qualité), quel que soit le temps qu’il peut prendre pour l’encoder. Un codec peut prendre en charge à la fois l’option ImageQuality et l’option CompressionQuality, où l’option ImageQuality spécifie le degré acceptable de lossiness, tandis que l’option CompressionQuality offre un compromis entre la taille et la vitesse au niveau de qualité spécifié.

L’option BitmapTransform permet à l’appelant de spécifier un angle de rotation ou un sens de retournement vertical ou horizontal lors de l’encodage. L’énumération WICBitmapTransformOptions utilisée pour spécifier la transformation demandée est identique à celle utilisée lors de la demande d’une transformation pendant le décodage via l’interface IWICBitmapSourceTransform.

Notez que les encodeurs ne sont pas limités aux options d’encodeur canoniques. L’objectif des options de codeur est de permettre aux encodeurs d’exposer leurs fonctionnalités, et il n’existe aucune limite aux types de fonctionnalités que vous pouvez exposer. Assurez-vous que les options de votre encodeur sont bien documentées. Même si une application peut utiliser le jeu de propriétés que vous retournez à partir de cette méthode pour découvrir les noms, les types et les plages de valeurs pour les options que vous prenez en charge, le seul moyen de déterminer leurs significations, ou comment les exposer dans l’interface utilisateur, provient de votre documentation.

### <a name="commit"></a>Commit

La [**validation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) est la méthode que vous appelez après que toutes les données et métadonnées de l’image ont été sérialisées dans le flux. Vous devez utiliser cette méthode pour sérialiser les données d’image d’aperçu dans le flux, ainsi que les miniatures globales, les métadonnées, la palette ou d’autres éléments, le cas échéant. Cette méthode ne doit pas fermer le flux de fichier, car l’application qui a ouvert le flux est censée la fermer.

La section sur la méthode IWICBitmapFrameEncode : Commit contient des détails sur la façon dont les IWICBitmapEncoderCacheOptions affectent le comportement de cette méthode.

### <a name="setpreview"></a>SetPreview

[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) est utilisé pour créer un aperçu de l’image. Bien qu’il ne soit pas strictement nécessaire que chaque image ait une version préliminaire, elle est fortement recommandée. Les scanneurs et appareils photo numériques modernes génèrent des images de haute résolution, qui ont tendance à être très volumineuses et, par conséquent, prennent un temps de traitement important pour le décodage. Les images de la prochaine génération de caméras seront encore plus volumineuses. Il est judicieux de fournir une version plus petite et plus basse pour une image, généralement au format JPEG, qui peut être rapidement décodée et affichée « instantanément » lorsqu’un utilisateur la demande. Une application peut demander une préversion avant de demander l’image réelle à décoder pour fournir une meilleure expérience aux utilisateurs, et leur montrer une représentation de la taille de l’image à l’écran pendant que theyare attend de décoder l’image réelle. Bien que les codecs doivent fournir des préversions, les codecs qui ne prennent pas en charge [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) doivent absolument le faire.

Si vous fournissez une version préliminaire JPEG, vous n’êtes pas obligé d’écrire un encodeur JPEG pour l’encoder. Vous devez déléguer à l’encodeur JPEG fourni avec la plateforme WIC pour encoder les miniatures et les aperçus.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Interfaces d’encodeur](-wic-encoderinterfaces.md)
</dt> <dt>

[Implémentation de IWICBitmapCodecProgressNotification (encodeur)](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
