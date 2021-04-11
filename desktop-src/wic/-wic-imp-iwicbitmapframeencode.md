---
description: Implémentation de IWICBitmapFrameEncode
ms.assetid: 509fa49c-c90d-4270-a338-6ce638ccd89a
title: Implémentation de IWICBitmapFrameEncode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d2a5ea0412ea4a45ea329618d00443c1755391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204222"
---
# <a name="implementing-iwicbitmapframeencode"></a>Implémentation de IWICBitmapFrameEncode

## <a name="iwicbitmapframeencode"></a>IWICBitmapFrameEncode

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) est l’équivalent de l’encodeur à l’interface [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) . Vous pouvez implémenter cette interface sur votre classe de codage au niveau de la trame, qui est la classe qui effectue l’encodage réel des bits d’image pour chaque frame.


```C++
interface IWICBitmapFrameEncode : public IUnknown
{
   // Required methods
   HRESULT Initialize ( IPropertyBag2 *pIEncoderOptions );
   HRESULT SetSize ( UINT width,
               UINT height );
   HRESULT SetResolution ( double dpiX,
               double dpiY );
   HRESULT SetPixelFormat (WICPixelFormatGUID *pPixelFormat);
   HRESULT SetColorContexts ( UINT cCount,
               IWICColorContext **ppIColorContext );
   HRESULT GetMetadataQueryWriter ( IWICMetadataQueryWriter 
               **ppIMetadataQueryWriter );
   HRESULT SetThumbnail ( IWICBitmapSource *pIThumbnail );
   HRESULT WritePixels ( UINT lineCount,
               UINT cbStride,
               UINT cbBufferSize,
               BYTE *pbPixels );
   HRESULT WriteSource ( IWICBitmapSource *pIWICBitmapSource,
               WICRect *prc );
   HRESULT Commit ( void );

// Optional method
   HRESULT SetPalette ( IWICPalette *pIPalette );
};
```



-   [Initialiser](#initialize)
-   [Définit et SetResolution](#setsize-and-setresolution)
-   [SetPixelFormat](#setpixelformat)
-   [SetColorContexts](#setcolorcontexts)
-   [GetMetadataQueryWriter](#getmetadataquerywriter)
-   [SetThumbnail](#setthumbnail)
-   [WritePixels](#writepixels)
-   [WriteSource](#writesource)
-   [Commiter](#commit)
-   [SetPalette](#setpalette)

### <a name="initialize"></a>Initialiser

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) est la première méthode appelée sur un objet [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) une fois qu’elle a été instanciée. Cette méthode a un paramètre, qui peut être défini sur **null**. Ce paramètre représente les options de l’encodeur. il s’agit de la même instance [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que vous avez créée dans la méthode [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) sur le décodeur au niveau du conteneur, puis repassée à l’appelant dans le paramètre pIEncoderOptions de cette méthode. À ce moment-là, vous avez rempli le struct IPropertyBag2 avec des propriétés qui représentent les options d’encodage prises en charge par votre encodeur au niveau de la trame. L’appelant a maintenant fourni des valeurs pour ces propriétés afin d’indiquer certains paramètres d’option d’encodage et renvoie le même objet pour initialiser l’objet **IWICBitmapFrameEncode** . Vous devez appliquer les options spécifiées lors de l’encodage des bits de l’image.

### <a name="setsize-and-setresolution"></a>Définit et SetResolution

Les paramètres de la [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) et de la [**configuration**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) sont explicites. L’appelant utilise ces méthodes pour spécifier la taille et la résolution de l’image encodée.

### <a name="setpixelformat"></a>SetPixelFormat

[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) est utilisé pour demander un format de pixel dans lequel encoder l’image. Si le format de pixel demandé n’est pas pris en charge, vous devez retourner le GUID du format de pixel le plus proche qui est pris en charge dans *pPixelFormat*, qui est un paramètre in/out.

### <a name="setcolorcontexts"></a>SetColorContexts

[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) est utilisé pour spécifier un ou plusieurs contextes de couleur valides (également appelés profils de couleurs) pour cette image. Il est important de spécifier les contextes de couleur. par conséquent, une application qui décode l’image ultérieurement peut convertir le profil de couleurs source en profil de destination de l’appareil utilisé pour afficher ou imprimer l’image. Sans profil de couleurs, il n’est pas possible d’obtenir des couleurs cohérentes sur différents appareils. Cela peut être frustrant pour les utilisateurs finaux lorsque leurs photos semblent différentes sur des moniteurs différents et qu’ils ne peuvent pas obtenir les impressions correspondant à ce qu’elles voient à l’écran.

### <a name="getmetadataquerywriter"></a>GetMetadataQueryWriter

[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) retourne un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) qu’une application peut utiliser pour insérer ou modifier des propriétés de métadonnées spécifiques dans un bloc de métadonnées sur le frame d’image.

Vous pouvez instancier un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) à partir du [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) de plusieurs façons. Vous pouvez le créer à partir de votre [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter), de la même façon que [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) a été créé à partir d’un [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) dans la méthode [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) sur l’interface [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .


```C++
IWICMetadataQueryWriter* piMetadataQueryWriter = NULL;
HRESULT hr;

hr = m_piComponentFactory->CreateQueryWriterFromBlockWriter( 
      static_cast<IWICMetadataBlockWriter*>(this), 
      &piMetadataQueryWriter);

```



Vous pouvez également le créer à partir d’un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)existant, tel que celui obtenu à l’aide de la méthode précédente.


```C++
hr = m_piComponentFactory->CreateQueryWriterFromReader( 
      piMetadataQueryReader, pguidVendor, &piMetadataQueryWriter);
```



Le paramètre *pGuidVendor* vous permet de spécifier un fournisseur particulier à utiliser par le générateur de requêtes lors de l’instanciation d’un enregistreur de métadonnées. Par exemple, si vous fournissez vos propres enregistreurs de métadonnées, vous souhaiterez peut-être spécifier votre propre GUID de fournisseur. Si vous n’avez pas de préférence, vous pouvez passer la **valeur null** à ce paramètre.

### <a name="setthumbnail"></a>SetThumbnail

[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) est utilisé pour fournir une miniature. Toutes les images doivent fournir une miniature à l’échelle mondiale, sur chaque image, ou les deux. Les méthodes **miniature** et **SetThumbnail** sont facultatives au niveau du conteneur, mais si un codec retourne WINCODEC \_ Err \_ CODECNOTHUMBNAIL de la méthode [**miniature**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) , Windows Imaging Component (WIC) appellera la méthode [**miniature**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) pour le frame 0. Si aucune miniature n’est trouvée à l’un ou l’autre emplacement, WIC doit décoder l’image complète et l’adapter à la taille de la miniature, ce qui peut entraîner une baisse importante des performances pour les images de grande taille.

La miniature doit avoir une taille et une résolution qui accélèrent le décodage et l’affichage. Pour cette raison, les miniatures sont généralement des images JPEG. Notez que, si vous utilisez JPEG pour vos miniatures, vous n’êtes pas obligé d’écrire un encodeur JPEG pour les encoder ou un décodeur JPEG pour les décoder. Vous devez toujours déléguer au codec JPEG fourni avec la plateforme WIC pour l’encodage et le décodage des miniatures.

### <a name="writepixels"></a>WritePixels

[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) est la méthode utilisée pour transmettre des lignes d’analyse à partir d’une bitmap en mémoire pour l’encodage. La méthode est appelée à plusieurs reprises jusqu’à ce que toutes les lignes de numérisation aient été passées. Le paramètre *lineCount* indique le nombre de lignes de numérisation à écrire dans cet appel. Le paramètre *cbStride* indique le nombre d’octets par ligne d’analyse. *cbBufferSize* indique la taille de la mémoire tampon passée dans le paramètre pbPixels, qui contient les bits d’image réels à encoder. Si la hauteur combinée des lignes d’analyse des appels cumulatifs est supérieure à la hauteur spécifiée dans la méthode de la méthode de [**configuration**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) , retournez WINCODEC \_ Err \_ TOOMANYSCANLINES.

Lorsque le [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) est **WICBitmapEncoderCacheInMemory**, les lignes de numérisation doivent être mises en cache dans la mémoire jusqu’à ce que toutes les lignes de numérisation aient été transmises. Si l’option de mise en cache de l’encodeur est **WICBitmapEncoderCacheTempFile**, les lignes d’analyse doivent être mises en cache dans un fichier temporaire, créé lors de l’initialisation de l’objet. Dans l’un ou l’autre de ces cas, l’image ne doit pas être encodée tant que l’appelant n’appelle pas [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit). Dans le cas où l’option de cache est **WICBitmapEncoderNoCache**, l’encodeur doit encoder les lignes d’analyse à mesure qu’elles sont reçues, si possible. (Dans certains formats, cela n’est pas possible et les lignes d’analyse doivent être mises en cache jusqu’à ce que la validation soit appelée.)

La plupart des codecs bruts n’implémenteront pas [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), car ils ne prennent pas en charge la modification des bits d’image dans le fichier brut. Toutefois, les codecs bruts doivent toujours implémenter **WritePixels**, car lorsque les métadonnées sont ajoutées, il peut augmenter la taille du fichier, ce qui nécessite la réécriture du fichier sur le disque. Dans ce cas, il est nécessaire de pouvoir copier les bits d’image existants, ce que fait la méthode **WritePixels** .

### <a name="writesource"></a>WriteSource

[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) est utilisé pour encoder un objet [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) . Le premier paramètre est un pointeur vers un objet **IWICBitmapSource** . Le deuxième paramètre est un WICRect qui spécifie la région d’intérêt à encoder. Cette méthode peut être appelée plusieurs fois successivement, à condition que la largeur de chaque rectangle soit la même que celle de l’image finale à encoder. Si la largeur du rectangle passé dans le paramètre PRC est différente de la largeur spécifiée dans la méthode deinstall, retournez WINCODEC \_ Err \_ SOURCERECTDOESNOTMATCHDIMENSIONS. Si la hauteur combinée des lignes d’analyse des appels cumulatifs est supérieure à la hauteur spécifiée dans la méthode de la méthode de configuration, retournez WINCODEC \_ Err \_ TOOMANYSCANLINES.

Les options de cache fonctionnent de la même manière avec cette méthode qu’avec la méthode [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) décrite précédemment.

### <a name="commit"></a>Commit

La [**validation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) est la méthode qui sérialise les bits d’image encodés dans le flux de fichier et itère au sein de tous les enregistreurs de métadonnées pour le frame qui les demande de sérialiser leurs métadonnées dans le flux. Dans le cas où l’option de cache d’encodeur est WICBitmapEncoderCacheInMemory ou WICBitmapEncoderCacheTempFile, cette méthode est également responsable de l’encodage de l’image, et lorsque l’option de cache est WICBitmapEncoderCacheTempFile, la méthode de **validation** doit également supprimer le fichier temporaire utilisé pour mettre en cache les données d’image avant l’encodage.

Cette méthode est toujours appelée une fois que toutes les lignes de numérisation ou les rectangles qui composent l’image ont été transmis à l’aide de la méthode [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) ou [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) . La taille du rectangle final qui est composé par les appels accumulés à WritePixels ou WriteSource doit être de la même taille que celle spécifiée dans la méthode de configuration. Si la taille ne correspond pas à la taille attendue, cette méthode doit retourner WINCODECERROR \_ UNEXPECTEDSIZE.

Pour itérer au sein des enregistreurs de métadonnées et indiquer à chaque enregistreur de métadonnées de sérialiser les métadonnées, accédez au flux, appelez GetWriterByIndex pour itérer au sein des enregistreurs de chaque bloc, puis appelez IWICPersistStream. Save sur chaque enregistreur de métadonnées.


```C++
IWICMetadataWriter* piMetadataWRiter = NULL;
IWICPersistStream* piPersistStream = NULL;
HRESULT hr;

for (UINT x=0; x < m_blockCount; x++) 
{
    hr = GetWriterByIndex(x, & piMetadataWriter);
hr = piMetadataWriter->QueryInterface(
IID_IWICPersistStream,(void**)&piPersistStream);

hr = piPersistStream->Save(m_piStream, 
WICPersistOptions.WicPersistOptionDefault, 
true);
...
}
```



### <a name="setpalette"></a>SetPalette

Seuls les codecs ayant des formats indexés doivent implémenter la méthode [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpalette) . Si une image utilise un format indexé, utilisez cette méthode pour spécifier la palette des couleurs utilisées dans l’image. Si votre CODEC n’a pas de format indexé, retournez WINCODEC \_ Err \_ PALETTEUNAVAILABLE à partir de cette méthode.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Implémentation de IWICBitmapCodecProgressNotification (encodeur)](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[Implémentation de IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
