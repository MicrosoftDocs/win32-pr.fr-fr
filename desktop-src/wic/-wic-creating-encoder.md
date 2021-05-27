---
description: Un encodeur écrit des données image dans un flux. Les encodeurs peuvent compresser, chiffrer et modifier les pixels de l’image de plusieurs manières avant de les écrire dans le flux.
ms.assetid: e1e3a9d9-209b-46a6-92da-5570476507cf
title: Vue d’ensemble de l’encodage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f938e184dee7fd9b3e5348365550615ee28de70d
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549484"
---
# <a name="encoding-overview"></a>Vue d’ensemble de l’encodage

Un encodeur écrit des données image dans un flux. Les encodeurs peuvent compresser, chiffrer et modifier les pixels de l’image de plusieurs manières avant de les écrire dans le flux. L’utilisation de certains encodeurs donne lieu à des compromis, par exemple JPEG, qui contourne les informations de couleur pour une meilleure compression. Les autres encodeurs n’entraînent pas de telles pertes, par exemple bitmap (BMP). Étant donné que de nombreux codecs utilisent la technologie propriétaire pour obtenir une meilleure compression et une meilleure fidélité des images, les détails sur la façon dont une image est encodée sont ceux du développeur du codec.

Cette rubrique comprend les sections suivantes.

-   [IWICBitmapEncoder](#iwicbitmapencoder)
-   [IWICBitmapFrameEncode](#iwicbitmapframeencode)
-   [Exemple d’encodage TIFF](#tiff-encoding-example)
-   [Utilisation des options d’encodeur](#encoder-options-usage)
-   [Options de l’encodeur](#encoder-options-usage)
-   [Exemples d’options d’encodeur](#encoder-options-examples)
-   [Rubriques connexes](#related-topics)

## <a name="iwicbitmapencoder"></a>IWICBitmapEncoder

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) est l’interface principale pour l’encodage d’une image au format cible et utilisée pour sérialiser les composants d’une image, tels que thumbnail ([**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) et frames ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)), dans le fichier image.

La façon dont et quand la sérialisation se produit est laissée au développeur du codec. Chaque bloc de données individuel dans le format de fichier cible doit pouvoir être défini indépendamment de l’ordre, mais là encore, il s’agit de la décision du développeur de codec. Une fois la méthode [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) appelée, les modifications apportées à l’image ne doivent pas être autorisées et le flux doit être fermé.

## <a name="iwicbitmapframeencode"></a>IWICBitmapFrameEncode

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) est l’interface pour l’encodage des frames individuels d’une image. Il fournit des méthodes pour définir des composants d’image de frame individuels, tels que des miniatures et des images, ainsi que des dimensions d’image, des PPP et des formats de pixel.

Des frames individuels peuvent être encodés avec des métadonnées propres au frame afin que [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) donne accès à un enregistreur de métadonnées via la méthode [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .

La méthode [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) du frame valide toutes les modifications apportées au frame individuel et indique que les modifications apportées à ce frame ne doivent plus être acceptées.

## <a name="tiff-encoding-example"></a>Exemple d’encodage TIFF

Dans l’exemple suivant, une image TIFF (Tagged Image File Format) est encodée à l’aide de [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) et d’un [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode). La sortie TIFF est personnalisée à l’aide de [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) et le frame bitmap est initialisé à l’aide des options données. Une fois que l’image a été créée à l’aide de [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), la trame est validée au moyen de la [**validation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) et l’image est enregistrée à l’aide de la [**validation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).


```C++
IWICImagingFactory *piFactory = NULL;
IWICBitmapEncoder *piEncoder = NULL;
IWICBitmapFrameEncode *piBitmapFrame = NULL;
IPropertyBag2 *pPropertybag = NULL;

IWICStream *piStream = NULL;
UINT uiWidth = 640;
UINT uiHeight = 480;

HRESULT hr = CoCreateInstance(
                CLSID_WICImagingFactory,
                NULL,
                CLSCTX_INPROC_SERVER,
                IID_IWICImagingFactory,
                (LPVOID*) &piFactory);

if (SUCCEEDED(hr))
{
    hr = piFactory->CreateStream(&piStream);
}

if (SUCCEEDED(hr))
{
    hr = piStream->InitializeFromFilename(L"output.tif", GENERIC_WRITE);
}

if (SUCCEEDED(hr))
{
   hr = piFactory->CreateEncoder(GUID_ContainerFormatTiff, NULL, &piEncoder);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->Initialize(piStream, WICBitmapEncoderNoCache);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetSize(uiWidth, uiHeight);
}

WICPixelFormatGUID formatGUID = GUID_WICPixelFormat24bppBGR;
if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetPixelFormat(&formatGUID);
}

if (SUCCEEDED(hr))
{
    // We're expecting to write out 24bppRGB. Fail if the encoder cannot do it.
    hr = IsEqualGUID(formatGUID, GUID_WICPixelFormat24bppBGR) ? S_OK : E_FAIL;
}

if (SUCCEEDED(hr))
{
    UINT cbStride = (uiWidth * 24 + 7)/8/***WICGetStride***/;
    UINT cbBufferSize = uiHeight * cbStride;

    BYTE *pbBuffer = new BYTE[cbBufferSize];

    if (pbBuffer != NULL)
    {
        for (UINT i = 0; i < cbBufferSize; i++)
        {
            pbBuffer[i] = static_cast<BYTE>(rand());
        }

        hr = piBitmapFrame->WritePixels(uiHeight, cbStride, cbBufferSize, pbBuffer);

        delete[] pbBuffer;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->Commit();
}    

if (SUCCEEDED(hr))
{
    hr = piEncoder->Commit();
}

if (piFactory)
    piFactory->Release();

if (piEncoder)
    piEncoder->Release();

if (piBitmapFrame)
    piBitmapFrame->Release();

if (pPropertybag)
    pPropertybag->Release();

if (piStream)
    piStream->Release();

return hr;
```



## <a name="encoder-options-usage"></a>Utilisation des options d’encodeur

Différents encodeurs pour différents formats doivent exposer des options différentes pour la façon dont une image est encodée. Le composant WIC (Windows Imaging Component) fournit un mécanisme cohérent pour exprimer si des options d’encodage sont requises tout en permettant aux applications de travailler avec plusieurs encodeurs sans avoir besoin de connaître un format particulier. Pour ce faire, vous devez fournir un paramètre [IPropertyBag](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) sur la méthode [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) et la méthode [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) .

La fabrique de composants fournit un point de création facile pour créer un jeu de propriétés d’options d’encodeur. Les codecs peuvent utiliser ce service s’ils ont besoin de fournir un ensemble simple, intuitif et non conflictuel d’options d’encodeur. Le jeu de propriétés d’acquisition d’images doit être initialisé lors de la création avec toutes les options de codeur pertinentes pour ce codec. Pour les options d’encodeur de l’ensemble canonique, la plage de valeurs sera appliquée lors de l’écriture. Pour les besoins plus avancés, les codecs doivent écrire leur propre implémentation de conteneur de propriétés.

Une application reçoit le jeu d’options d’encodeur pendant la création du frame et doit configurer toutes les valeurs avant d’initialiser le frame de l’encodeur. Pour une application pilotée par l’interface utilisateur, elle peut offrir une interface utilisateur fixe pour les options de codeur canoniques et une vue avancée pour les options restantes. Les modifications peuvent être apportées une par une à l’aide de la méthode Write et toute erreur sera signalée par le biais de IErrorLog. L’application d’interface utilisateur doit toujours relire et afficher toutes les options après avoir apporté une modification au cas où la modification a entraîné un effet en cascade. Une application doit être préparée à gérer l’initialisation des frames ayant échoué pour les codecs qui fournissent uniquement un rapport d’erreurs minimal par le biais de leur conteneur de propriétés.

## <a name="encoder-options"></a>Options de l’encodeur

Une application peut s’attendre à rencontrer l’ensemble d’options d’encodeur suivant. Les options d’encodeur reflètent les fonctionnalités d’un encodeur et du format de conteneur sous-jacent, et par conséquent, sont par leur nature pas vraiment indépendantes des codecs. Lorsque cela est possible, les nouvelles options doivent être normalisées pour pouvoir être appliquées aux nouveaux codecs qui émergent.



| Nom de la propriété      | VARTYPE  | Valeur                                                                     | Codecs applicables |
|--------------------|----------|---------------------------------------------------------------------------|-------------------|
| ImageQuality       | VT \_ R4   | 0-1,0                                                                     | JPEG, HDPhoto     |
| CompressionQuality | VT \_ R4   | 0-1,0                                                                     | TIFF              |
| Lossless           | VT \_ bool | **true**, **false**                                                       | HDPhoto           |
| BitmapTransform    | \_UI1 VT  | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | JPEG              |



 

ImageQualty de 0,0 signifie que le rendu de fidélité le plus bas possible et 1,0 correspond à la fidélité la plus élevée, qui peut également être sans perte en fonction du codec.

CompressionQuality de 0,0 signifie le schéma de compression le moins efficace disponible, ce qui entraîne généralement un encodage rapide mais une sortie plus grande. La valeur 1,0 correspond au schéma le plus efficace disponible, en utilisant généralement plus de temps pour encoder, mais en produisant une sortie plus petite. Selon les fonctionnalités du codec, cette plage peut être mappée sur un ensemble discret de méthodes de compression disponibles.

Lossless signifie que le codec encode l’image comme Lossless sans perte de données d’image. Si le Lossless est activé, ImageQuality est ignoré.

Outre les options de codeur génériques ci-dessus, les codecs fournis avec WIC prennent en charge les options suivantes. Si un codec a besoin de prendre en charge une option qui est cohérente avec l’utilisation dans ces codecs fournis, il est recommandé de le faire.



| Nom de la propriété           | VARTYPE           | Valeur                                                                             | Codecs applicables |
|-------------------------|-------------------|-----------------------------------------------------------------------------------|-------------------|
| InterlaceOption         | VT \_ bool          | Actif/inactif                                                                            | PNG               |
| FilterOption            | \_UI1 VT           | [**WICPngFilterOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)                       | PNG               |
| TiffCompressionMethod   | \_UI1 VT           | [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)           | TIFF              |
| Luminance               | \_Groupe VT UI4/VT \_ | 64 entrées (DCT)                                                                  | JPEG              |
| Chrominance             | \_Groupe VT UI4/VT \_ | 64 entrées (DCT)                                                                  | JPEG              |
| JpegYCrCbSubsampling    | \_UI1 VT           | [**WICJpegYCrCbSubsamplingOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | JPEG              |
| SuppressApp0            | VT \_ bool          |                                                                                   | JPEG              |
| EnableV5Header32bppBGRA | VT \_ bool          | Actif/inactif                                                                            | BMP               |



 

Utilisez **VT \_ vide** pour indiquer qu’il **\* \* n’est pas défini** comme valeur par défaut. Si des propriétés supplémentaires sont définies mais pas prises en charge, l’encodeur doit les ignorer. Cela permet aux applications de coder moins de logique s’ils souhaitent une fonctionnalité qui peut ou non être présente.

## <a name="encoder-options-examples"></a>Exemples d’options d’encodeur

Dans l' [exemple d’encodage TIFF](#tiff-encoding-example) ci-dessus, une option d’encodeur spécifique est définie. Le membre *pstrName* de la structure PROPBAG2 est défini sur le nom de propriété approprié, et la variante est définie sur le VarType correspondant et la valeur souhaitée (dans ce cas, un membre de l’énumération [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) .


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



Pour utiliser les options d’encodeur par défaut, il vous suffit d’initialiser le frame de bitmap avec le jeu de propriétés retourné lors de la création du frame.


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // Accept the default encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



Il est également possible d’éliminer le jeu de propriétés quand aucune option d’encodeur n’est prise en compte.


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, 0);
}

if (SUCCEEDED(hr))
{        
    // No encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(0);
    }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Décodage, vue d’ensemble](-wic-creating-decoder.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
