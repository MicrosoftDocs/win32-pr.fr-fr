---
description: cette rubrique fournit une vue d’ensemble de la façon dont vous pouvez utiliser les api du composant de création d’images Windows (WIC) pour lire et écrire des métadonnées incorporées dans des fichiers image.
ms.assetid: b1e0b936-a13a-42dd-8470-957ba1d90423
title: Vue d’ensemble de la lecture et de l’écriture des métadonnées d’image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 484d562b71184c20adf054f1de2a4203878da9b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293246"
---
# <a name="overview-of-reading-and-writing-image-metadata"></a>Vue d’ensemble de la lecture et de l’écriture des métadonnées d’image

cette rubrique fournit une vue d’ensemble de la façon dont vous pouvez utiliser les api du composant de création d’images Windows (WIC) pour lire et écrire des métadonnées incorporées dans des fichiers image.

Cette rubrique contient les sections suivantes.

-   [Composants requis](#prerequisites)
-   [Introduction](#introduction)
-   [Lecture de Metadadata à l’aide d’un lecteur de requêtes](#reading-metadadata-using-a-query-reader)
    -   [Obtention d’un lecteur de requêtes](#obtaining-a-query-reader)
    -   [Lecture des métadonnées](#reading-metadata)
    -   [Méthodes de lecteur de requête supplémentaires](#additional-query-reader-methods)
-   [Écriture de métadonnées à l’aide d’un générateur de requêtes](#writing-metadata-using-a-query-writer)
    -   [Obtention d’un générateur de requêtes](#obtaining-a-query-writer)
    -   [Ajout de métadonnées](#adding-metadata)
    -   [Suppression de métadonnées](#removing-metadata)
    -   [Copie des métadonnées pour le ré-encodage](#copying-metadata-for-re-encoding)
-   [Encodage de métadonnées rapide](#fast-metadata-encoding)
    -   [Ajout d’un remplissage à des blocs de métadonnées](#adding-padding-to-metadata-blocks)
    -   [Obtention d’un encodeur de métadonnées rapide](#obtaining-a-fast-metadata-encoder)
    -   [Utilisation de l’encodeur de métadonnées rapide](#using-the-fast-metadata-encoder)
-   [Rubriques connexes](#related-topics)

## <a name="prerequisites"></a>Prérequis

Pour comprendre cette rubrique, vous devez être familiarisé avec le système de métadonnées WIC, comme décrit dans [vue d’ensemble des métadonnées WIC](-wic-about-metadata.md). Vous devez également être familiarisé avec le langage de requête utilisé pour lire et écrire des métadonnées, comme décrit dans [vue d’ensemble du langage de requête de métadonnées](-wic-codec-metadataquerylanguage.md).

## <a name="introduction"></a>Introduction

WIC fournit aux développeurs d’applications des composants COM (Component Object Model) pour lire et écrire des métadonnées incorporées dans des fichiers image. Il existe deux façons de lire et d’écrire des métadonnées :

-   Utilisation d’un enregistreur/lecteur de requête et d’une expression de requête pour interroger des blocs de métadonnées pour des blocs imbriqués ou des métadonnées spécifiques au sein d’un bloc.
-   En utilisant un gestionnaire de métadonnées (un lecteur de métadonnées ou un enregistreur de métadonnées) pour accéder aux blocs de métadonnées imbriqués ou à des métadonnées spécifiques dans les blocs de métadonnées.

La plus simple consiste à utiliser un lecteur/enregistreur de requêtes et une expression de requête pour accéder aux métadonnées. Un lecteur de requête ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) est utilisé pour lire les métadonnées lorsqu’un enregistreur de requête ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) est utilisé pour écrire des métadonnées. Les deux utilisent une expression de requête pour lire ou écrire les métadonnées souhaitées. En arrière-plan, un lecteur de requête (et un enregistreur) utilise un gestionnaire de métadonnées pour accéder aux métadonnées décrites par l’expression de requête.

La méthode la plus avancée consiste à accéder directement aux gestionnaires de métadonnées. Un gestionnaire de métadonnées est obtenu à partir des frames individuels à l’aide d’un lecteur de bloc ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) ou d’un enregistreur de bloc ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)). Les deux types de gestionnaires de métadonnées disponibles sont le lecteur de métadonnées ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) et le writer de métadonnées ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)).

Le diagramme suivant du contenu d’un fichier image JPEG est utilisé dans les exemples de cette rubrique. L’image représentée par ce diagramme a été créée à l’aide de Microsoft Paint ; les métadonnées d’évaluation ont été ajoutées à l’aide de la fonctionnalité galerie de photos de Windows Vista.

![illustration de l’image JPEG avec les métadonnées d’évaluation](graphics/jpeg.png)

## <a name="reading-metadadata-using-a-query-reader"></a>Lecture de Metadadata à l’aide d’un lecteur de requêtes

Le moyen le plus simple de lire les métadonnées consiste à utiliser l’interface du lecteur de requêtes, [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader). Le lecteur de requête vous permet de lire des blocs de métadonnées et des éléments dans des blocs de métadonnées à l’aide d’une expression de requête.

Il existe trois façons d’obtenir un lecteur de requête : par le biais d’un décodeur bitmap ([**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)), par le biais de ses cadres individuels ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) ou par le biais d’un générateur de requêtes ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).

### <a name="obtaining-a-query-reader"></a>Obtention d’un lecteur de requêtes

L’exemple de code suivant montre comment obtenir un décodeur bitmap à partir de la fabrique d’images et récupérer un frame bitmap individuel. Ce code effectue également le travail d’installation nécessaire à l’obtention d’un lecteur de requêtes à partir d’une trame décodée.


```
IWICImagingFactory *pFactory = NULL;
IWICBitmapDecoder *pDecoder = NULL;
IWICBitmapFrameDecode *pFrameDecode = NULL;
IWICMetadataQueryReader *pQueryReader = NULL;
IWICMetadataQueryReader *pEmbedReader = NULL;
PROPVARIANT value;

// Initialize COM
CoInitialize(NULL);

// Initialize PROPVARIANT
PropVariantInit(&value);

//Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_IWICImagingFactory,
    (LPVOID*)&pFactory);

// Create the decoder
if (SUCCEEDED(hr))
{
    hr = pFactory->CreateDecoderFromFilename(
        L"test.jpg",
        NULL,
        GENERIC_READ,
        WICDecodeMetadataCacheOnDemand,
        &pDecoder);
}

// Get a single frame from the image
if (SUCCEEDED(hr))
{
    hr = pDecoder->GetFrame(
         0,  //JPEG has only one frame.
         &pFrameDecode); 
}
```



Le décodeur bitmap du fichier test.jpg est obtenu à l’aide de la méthode **CreateDecoderFromFilename** de la fabrique d’images. Dans cette méthode, le quatrième paramètre est défini sur la valeur WICDecodeMetadataCacheOnDemand à partir de l’énumération [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) . Cela indique au décodeur de mettre en cache les métadonnées lorsque les métadonnées sont nécessaires ; en obtenant un lecteur de requête ou le lecteur de métadonnées sous-jacent. L’utilisation de cette option vous permet de conserver le flux vers les métadonnées requises pour l’encodage rapide des métadonnées et active le décodage sans perte de l’image JPEG. Vous pouvez également utiliser l’autre valeur **WICDecodeOptions** , WICDecodeMetadataCacheOnLoad, qui met en cache les métadonnées de l’image incorporée dès le chargement de l’image.

Pour obtenir le lecteur de requête du frame, effectuez un appel simple à la méthode **GetMetadataQueryReader** du frame. L’exemple de code suivant illustre cet appel.


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



De même, un lecteur de requête peut également être obtenu au niveau du décodeur. Un simple appel à la méthode **GetMetadataQueryReader** du décodeur obtient le lecteur de requête du décodeur. Le lecteur de requêtes d’un décodeur, à la différence du lecteur de requêtes d’un frame, lit les métadonnées d’une image qui se trouve en dehors des frames individuels. Toutefois, ce scénario n’est pas courant et les formats d’images natives ne prennent pas en charge cette fonctionnalité. Les CODECs d’image native fournis par le WIC lisent et écrivent les métadonnées au niveau de la trame, même pour les formats à image unique, tels que JPEG.

### <a name="reading-metadata"></a>Lecture des métadonnées

Avant de passer à la lecture effective des métadonnées, examinez le diagramme suivant d’un fichier JPEG qui comprend des blocs de métadonnées incorporés et des données réelles à récupérer. Ce diagramme fournit des légendes pour des blocs de métadonnées et des éléments de l’image qui fournissent l’expression de requête de métadonnées à chaque bloc ou élément.

![illustration de l’image JPEG avec des légendes de métadonnées](graphics/jpegwithcallouts.png)

Pour rechercher des blocs de métadonnées incorporés ou des éléments spécifiques par nom, appelez la méthode **GetMetadataByName** . Cette méthode prend une expression de requête et un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) dans lequel l’élément de métadonnées est retourné. Le code suivant interroge un bloc de métadonnées imbriqué et convertit le composant [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) fourni par la valeur PROPVARIANT en un lecteur de requêtes, s’il est trouvé.


```
if (SUCCEEDED(hr))
{
    // Get the nested IFD reader
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd", &value);
    if (value.vt == VT_UNKNOWN)
    {
        hr = value.punkVal->QueryInterface(IID_IWICMetadataQueryReader, (void **)&pEmbedReader);
    }
    PropVariantClear(&value); // Clear value for new query
}
```



L’expression de requête « /App1/IFD » interroge le bloc IFD imbriqué dans le bloc App1. Le fichier image JPEG contient le bloc de métadonnées imbriquées IFD, donc le [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) est retourné avec un type de variable (VT) de `VT_UNKNOWN` et un pointeur vers une interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) (punkVal). Vous interrogez ensuite l’interface IUnknown pour obtenir un lecteur de requête.

Le code suivant illustre une nouvelle requête basée sur le nouveau lecteur de requêtes relatif au bloc IFD imbriqué.


```
if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetMetadataByName(L"/{ushort=18249}", &value);
    PropVariantClear(&value); // Clear value for new query
}
```



L’expression de requête « /{UShort = 18249} » interroge le bloc IFD pour l’évaluation de MicrosoftPhoto incorporée sous la balise 18249. La valeur [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) contient maintenant un type valeur `VT_UI2` et une valeur de données de 50.

Toutefois, il n’est pas nécessaire d’obtenir un bloc imbriqué avant d’interroger des valeurs de données spécifiques. Par exemple, au lieu d’interroger l’IFD imbriqué, puis pour l’évaluation de MicrosoftPhoto, vous pouvez utiliser à la place le bloc de métadonnées racine et la requête illustrée dans le code suivant pour obtenir les mêmes informations.


```
if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);
    PropVariantClear(&value);
}
```



Outre l’interrogation d’éléments de métadonnées spécifiques dans un bloc de métadonnées, vous pouvez également énumérer tous les éléments de métadonnées dans un bloc de métadonnées (à l’exclusion des éléments de métadonnées dans les blocs de métadonnées imbriqués). Pour énumérer les éléments de métadonnées dans le bloc actuel, la méthode **GetEnumeration** du lecteur de requête est utilisée. Cette méthode obtient une interface **IEnumString** remplie avec les éléments de métadonnées du bloc en cours. Par exemple, le code suivant énumère les évaluations XMP et MicrosoftPhoto pour le bloc IFD imbriqué qui a été obtenu précédemment.


```
IEnumString *metadataItems = NULL;

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetEnumerator(&metadataItems);
}
```



Pour plus d’informations sur l’identification des balises appropriées pour différents formats d’image et formats de métadonnées, consultez [requêtes de métadonnées de format d’image native](-wic-native-image-format-metadata-queries.md).

### <a name="additional-query-reader-methods"></a>Méthodes de lecteur de requête supplémentaires

Outre la lecture des métadonnées, vous pouvez également obtenir des informations supplémentaires sur le lecteur de requête et obtenir des métadonnées par d’autres moyens. Le lecteur de requête fournit deux méthodes qui fournissent des informations sur le lecteur de requêtes, **GetContainerFormat** et **GetLocation**.

Avec le lecteur de requête incorporé, vous pouvez utiliser **GetContainerFormat** pour déterminer le type de bloc de métadonnées, et vous pouvez appeler **GetLocation** pour obtenir le chemin d’accès relatif au bloc de métadonnées racine. Le code suivant interroge le lecteur de requête incorporé pour obtenir son emplacement.


```
// Determine the metadata block format

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetContainerFormat(&containerGUID);
}

// Determine the query reader's location
if (SUCCEEDED(hr))
{
    UINT length;
    WCHAR readerNamespace[100];
    hr = pEmbedReader->GetLocation(100, readerNamespace, &length);
}
```



L’appel à **GetContainerFormat** pour le lecteur de requêtes incorporées retourne le GUID du format de métadonnées IFD. L’appel à **GetLocation** retourne un espace de noms de « /App1/IFD »; fournir le chemin d’accès relatif à partir duquel les requêtes suivantes au nouveau lecteur de requête seront exécutées. Bien entendu, le code précédent n’est pas très utile, mais il montre comment utiliser la méthode **GetLocation** pour rechercher des blocs de métadonnées imbriqués.

## <a name="writing-metadata-using-a-query-writer"></a>Écriture de métadonnées à l’aide d’un générateur de requêtes

> [!Note]  
> Certains des exemples de code fournis dans cette section ne sont pas affichés dans le contexte des étapes réelles requises pour écrire des métadonnées. Pour afficher les exemples de code dans le contexte d’un exemple fonctionnel, consultez le didacticiel Comment : recoder une image avec des métadonnées.

 

Le principal composant pour écrire des métadonnées est le générateur de requêtes ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)). Le générateur de requêtes vous permet de définir et de supprimer des blocs de métadonnées et des éléments au sein d’un bloc de métadonnées.

À l’instar du lecteur de requêtes, il existe trois façons d’obtenir un générateur de requêtes : par le biais d’un encodeur bitmap ([**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)), par le biais de ses propres frames ([**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)) ou par l’intermédiaire d’un encodeur de métadonnées rapide ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)).

### <a name="obtaining-a-query-writer"></a>Obtention d’un générateur de requêtes

Le générateur de requêtes le plus courant concerne un frame individuel d’une image bitmap. Cet enregistreur de requêtes définit et supprime les éléments et les blocs de métadonnées d’un frame d’image. Pour obtenir le générateur de requêtes d’un frame d’image, appelez la méthode **GetMetadataQueryWriter** du frame. Le code suivant illustre l’appel de méthode simple pour obtenir le générateur de requêtes d’un frame.


```
IWICMetadataQueryWriter &pFrameQWriter = NULL;

//Obtain a query writer from the frame.
hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
```



De même, un enregistreur de requête peut également être obtenu pour le niveau de l’encodeur. Un simple appel à la méthode **GetMetadataQueryWriter** de l’encodeur obtient le générateur de requêtes de l’encodeur. Le générateur de requêtes d’un encodeur, à la différence du writer de requête d’un frame, écrit les métadonnées d’une image en dehors du frame individuel. Toutefois, ce scénario n’est pas courant et les formats d’images natives ne prennent pas en charge cette fonctionnalité. Les codecs d’image native fournis par le WIC lisent et écrivent les métadonnées au niveau de la trame, même pour les formats à image unique, tels que JPEG.

Vous pouvez également obtenir un enregistreur de requête directement à partir de la fabrique d’images ([**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)). Deux méthodes de fabrique d’images renvoient un générateur de requêtes : **CreateQueryWriter** et **CreateQueryWriterFromReader**.

**CreateQueryWriter** crée un enregistreur de requête pour le format de métadonnées et le fournisseur spécifiés. Ce writer de requête vous permet d’écrire des métadonnées pour un format de métadonnées spécifique et de les ajouter à l’image. Le code suivant illustre un appel **CreateQueryWriter** pour créer un générateur de requêtes XMP.


```
IWICMetadataQueryWriter *pXMPWriter = NULL;

// Create XMP block
GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriter(
        GUID_MetadataFormatXMP,
        &vendor,
        &pXMPWriter);
```



Dans cet exemple, le nom convivial `GUID_MetadataFormatXMP` est utilisé comme paramètre *guidMetadataFormat* . Il représente le GUID du format de métadonnées XMP et le fournisseur représente le gestionnaire créé par Microsoft. Sinon, la **valeur null** peut être transmise en tant que paramètre *pGuidVendor* avec les mêmes résultats si aucun autre gestionnaire XMP n’existe. Si un gestionnaire XMP personnalisé est installé en même temps que le gestionnaire XMP natif, le passage de la **valeur null** pour le fournisseur entraînera le renvoi du GUID le plus bas dans le générateur de requêtes.

**CreateQueryWriterFromReader** est similaire à la méthode **CreateQueryWriter** , à ceci près qu’elle préremplit le nouvel enregistreur de requête avec les données fournies par le lecteur de requête. Cela est utile pour recoder une image tout en conservant les métadonnées existantes ou pour supprimer les métadonnées indésirables. Le code suivant illustre un appel **CreateQueryWriterFromReader** .


```
hr = pFrameDecode->GetMetadataQueryReader(&pFrameQReader);

// Copy metadata using query readers
if(SUCCEEDED(hr) && pFrameQReader)
{
    IWICMetadataQueryWriter *pNewWriter = NULL;

    GUID vendor = GUID_VendorMicrosoft;
    hr = pFactory->CreateQueryWriterFromReader(
        pFrameQReader,
        &vendor,
        &pNewWriter);
```



### <a name="adding-metadata"></a>Ajout de métadonnées

Une fois que vous avez obtenu un générateur de requêtes, vous pouvez l’utiliser pour ajouter des blocs de métadonnées et des éléments. Pour écrire des métadonnées, vous utilisez la méthode **SetMetadataByName** du générateur de requêtes. **SetMetadataByName** accepte deux paramètres : une expression de requête (*wzName*) et un pointeur vers [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*pvarValue*). L’expression de requête définit le bloc ou l’élément à définir lorsque le PROPVARIANT fournit la valeur de données réelle à définir.

L’exemple suivant montre comment ajouter un titre à l’aide du writer de requête XMP obtenu précédemment à l’aide de la méthode **CreateQueryWriter** .


```
// Write metadata to the XMP writer
if (SUCCEEDED(hr))
{
    PROPVARIANT value;
    PropVariantInit(&value);

    value.vt = VT_LPWSTR;
    value.pwszVal = L"Metadata Test Image.";
   
    hr = pXMPWriter->SetMetadataByName(L"/dc:title", &value);

    PropVariantClear(&value);
}
```



Dans cet exemple, le type de la valeur (VT) a `VT_LPWSTR` la valeur, ce qui indique qu’une chaîne sera utilisée comme valeur de données. Étant donné que le type de la *valeur* est une chaîne, *pwszVal* est utilisé pour définir le titre à utiliser. **SetMetadataByName** est ensuite appelée à l’aide de l’expression de requête « /DC : title » et du [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)nouvellement défini. L’expression de requête utilisée indique que la propriété titre du schéma de l’appareil photo numérique (DC) doit être définie. Notez que l’expression n’est pas « /XMP/DC : title »; Cela est dû au fait que le générateur de requêtes est déjà spécifique à XMP et qu’il ne contient pas de bloc XMP incorporé, que « /XMP/DC : title » suggère.

Jusqu’à présent, vous n’avez pas ajouté de métadonnées à une image. Vous avez simplement renseigné un générateur de requêtes avec des données. Pour ajouter à un frame un bloc de métadonnées représenté par le générateur de requêtes, vous appelez à nouveau **SetMetadataByName** à l’aide du générateur de requêtes comme valeur de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant). Cela copie efficacement les métadonnées dans le générateur de requêtes dans le frame d’image. Le code suivant montre comment ajouter les métadonnées dans le générateur de requêtes XMP précédemment obtenues dans le bloc de métadonnées racine d’un frame.


```
// Get the frame's query writer and write the XMP query writer to it
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);

    // Copy the metadata in the XMP query writer to the frame
    if (SUCCEEDED(hr))
    {
        PROPVARIANT value;

        PropVariantInit(&value);
        value.vt = VT_UNKNOWN;
        value.punkVal = pXMPWriter;
        value.punkVal->AddRef();

        hr = pFrameQWriter->SetMetadataByName(L"/", &value);

        PropVariantClear(&value);
    }
}
```



Dans cet exemple, un type valeur (VT) de `VT_UNKOWN` est utilisé, ce qui indique un type valeur d’interface com. Le générateur de requêtes XMP (piXMPWriter) est ensuite utilisé comme valeur du [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), en y ajoutant une référence à l’aide de la méthode AddRef. Enfin, le générateur de requêtes XMP est défini en appelant la méthode **SetMetadataByName** du frame et en passant l’expression de requête « / », en indiquant le bloc racine et le PROPVARIANT nouvellement défini.

> [!Note]  
> Si le frame contient déjà le bloc de métadonnées que vous essayez d’ajouter, les métadonnées que vous ajoutez seront ajoutées et les métadonnées existantes seront remplacées.

 

### <a name="removing-metadata"></a>Suppression de métadonnées

Un générateur de requêtes vous permet également de supprimer des métadonnées en appelant la méthode **RemoveMetadataByName** . **RemoveMetadataByName** prend une expression de requête et supprime le bloc de métadonnées ou l’élément s’il existe. Le code suivant montre comment supprimer le titre précédemment ajouté.


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp/dc:title");
}
```



Le code suivant montre comment supprimer l’intégralité du bloc de métadonnées XMP.


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp");
}
```



### <a name="copying-metadata-for-re-encoding"></a>Copie des métadonnées pour le ré-encodage

> [!Note]  
> Le code de cette section est valide uniquement lorsque les formats d’image source et de destination sont identiques. Vous ne pouvez pas copier toutes les métadonnées d’une image en une seule opération lors de l’encodage dans un format d’image différent.

 

Pour conserver les métadonnées tout en recodant une image au même format d’image, il existe des méthodes permettant de copier toutes les métadonnées en une seule opération. Chacune de ces opérations suit un modèle similaire. chaque définit les métadonnées de l’image décodée directement dans le nouveau Frame encodé.

La méthode recommandée pour copier les métadonnées consiste à initialiser le writer de bloc du nouveau Frame avec le lecteur de bloc du frame décodé. L’exemple de code suivant illustre cette méthode.


```
if (SUCCEEDED(hr) && formatsEqual)
{
    // Copy metadata using metadata block reader/writer
    if (SUCCEEDED(hr))
    {
        pFrameDecode->QueryInterface(
            IID_IWICMetadataBlockReader,
            (void**)&pBlockReader);
    }
    if (SUCCEEDED(hr))
    {
        pFrameEncode->QueryInterface(
            IID_IWICMetadataBlockWriter,
            (void**)&pBlockWriter);
    }
    if (SUCCEEDED(hr))
    {
        pBlockWriter->InitializeFromBlockReader(pBlockReader);
    }
}
```



Dans cet exemple, le lecteur de bloc et le writer de bloc sont obtenus à partir de l’image source et du frame de destination, respectivement. Le writer de bloc est ensuite initialisé à partir du lecteur de bloc. Cela initialise le lecteur de bloc avec les métadonnées préremplies du lecteur de bloc.

Une autre méthode pour copier les métadonnées consiste à écrire le bloc de métadonnées référencé par le lecteur de requête à l’aide du générateur de requêtes de l’encodeur. L’exemple de code suivant illustre cette méthode.


```
if (SUCCEEDED(hr) && formatsEqual)
{
    hr = pFrameDecode->GetMetadataQueryReader(&pFrameQReader);

    // Copy metadata using query readers
    if(SUCCEEDED(hr))
    {
        hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
        if (SUCCEEDED(hr))
        {
            PropVariantClear(&value);
            value.vt=VT_UNKNOWN;
            value.punkVal=pFrameQReader;
            value.punkVal->AddRef();
            hr = pFrameQWriter->SetMetadataByName(L"/", &value);
            PropVariantClear(&value);
        }
    }
}
```



Ici, un lecteur de requête est obtenu à partir de l’image décodée, puis utilisé en tant que valeur de propriété du [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) avec un type valeur défini sur VT \_ inconnu. Le générateur de requêtes pour l’encodeur est obtenu et l’expression de requête « / » est utilisée pour définir les métadonnées au niveau du chemin de navigation racine. Vous pouvez également utiliser cette méthode lors de la définition de blocs de métadonnées imbriqués, en ajustant l’expression de requête à l’emplacement souhaité.

De même, vous pouvez créer un writer de requête basé sur le lecteur de requêtes de l’image décodée à l’aide de la méthode **CreateQueryWriterFromReader** de la fabrique d’images. Le générateur de requêtes créé dans cette opération est prérempli avec les métadonnées du lecteur de requêtes et peut ensuite être défini dans le frame. Le code suivant illustre l’opération de copie **CreateQueryWriterFromReader** .


```
IWICMetadataQueryWriter *pNewWriter = NULL;

GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriterFromReader(
    pFrameQReader,
    &vendor,
    &pNewWriter);

if (SUCCEEDED(hr))
{
    // Get the frame's query writer
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

// Set the query writer to the frame.
if (SUCCEEDED(hr))
{
    PROPVARIANT value;

    PropVariantInit(&value);
    value.vt = VT_UNKNOWN;
    value.punkVal = pNewWriter;
    value.punkVal->AddRef();
    hr = pFrameQWriter->SetMetadataByName(L"/",&value);
}
```



Cette méthode utilise un writer de requête distinct créé en fonction des données du lecteur de requête. Ce nouvel enregistreur de requête est ensuite défini dans le frame.

Là encore, ces opérations de copie des métadonnées fonctionnent uniquement lorsque les images source et de destination ont le même format. Cela est dû au fait que différents formats d’image stockent les blocs de métadonnées à différents emplacements. Par exemple, les fichiers JPEG et TIFF prennent en charge les blocs de métadonnées XMP. Dans les images JPEG, le bloc XMP se trouve dans le bloc de métadonnées racine, comme illustré dans la [vue d’ensemble des métadonnées WIC](-wic-about-metadata.md). Toutefois, dans une image TIFF, le bloc XMP est imbriqué dans un bloc IFD racine. Le diagramme suivant illustre les différences entre une image JPEG et une image TIFF avec les mêmes métadonnées d’évaluation.

![comparaison JPEG et TIFF.](graphics/jpgvstiff.png)

## <a name="fast-metadata-encoding"></a>Encodage de métadonnées rapide

Il n’est pas toujours nécessaire de recoder une image pour y écrire de nouvelles métadonnées. Les métadonnées peuvent également être écrites à l’aide d’un encodeur de métadonnées rapide. Un encodeur de métadonnées rapide peut écrire une quantité limitée de métadonnées dans une image sans recodage de l’image. Pour ce faire, vous devez écrire les nouvelles métadonnées dans le remplissage vide fourni par certains formats de métadonnées. Les formats de métadonnées natifs qui prennent en charge le remplissage des métadonnées sont EXIF, IFD, GPS et XMP.

### <a name="adding-padding-to-metadata-blocks"></a>Ajout d’un remplissage à des blocs de métadonnées

Avant de pouvoir effectuer un encodage de métadonnées rapide, il doit y avoir de l’espace dans le bloc de métadonnées pour écrire davantage de métadonnées. S’il n’y a pas assez de place dans le remplissage existant pour écrire les nouvelles métadonnées, l’encodage de métadonnées rapide échoue. Pour ajouter une marge intérieure des métadonnées à une image, l’image doit être à nouveau codée. Vous pouvez ajouter un remplissage de la même façon que vous ajoutez tout autre élément de métadonnées, à l’aide d’une expression de requête, si le bloc de métadonnées que vous complétez le prend en charge. L’exemple suivant montre comment ajouter un remplissage à un bloc IFD incorporé dans un bloc App1.


```
if (SUCCEEDED(hr))
{
    // Add metadata padding
    PROPVARIANT padding;

    PropVariantInit(&padding);
    padding.vt = VT_UI4;
    padding.uiVal = 4096; // 4KB

    hr = pFrameQWriter->SetMetadataByName(L"/app1/ifd/PaddingSchema:padding", &padding);

    PropVariantClear(&padding);
}
```



Pour ajouter le remplissage, créez un PROPVARIANT de type VT \_ UI4 et une valeur correspondant au nombre d’octets de remplissage à ajouter. Une valeur typique est 4096 octets. Les requêtes de métadonnées pour JPEG, TIFF et JPEG-XR sont répertoriées dans ce tableau.



| Format de métadonnées | Requête de métadonnées JPEG                  | TIFF, JPEG-requête de métadonnées XR    |
|-----------------|--------------------------------------|---------------------------------|
| IFD             | /app1/ifd/PaddingSchema : remplissage      | /ifd/PaddingSchema : remplissage      |
| EXIF            | /app1/ifd/exif/PaddingSchema : remplissage | /ifd/exif/PaddingSchema : remplissage |
| XMP             | /xmp/PaddingSchema : remplissage           | /ifd/xmp/PaddingSchema : remplissage  |
| GPS             | /app1/ifd/gps/PaddingSchema : remplissage  | /ifd/gps/PaddingSchema : remplissage  |



 

### <a name="obtaining-a-fast-metadata-encoder"></a>Obtention d’un encodeur de métadonnées rapide

Lorsque vous disposez d’une image avec remplissage des métadonnées, un encodeur de métadonnées rapide peut être obtenu à l’aide des méthodes de fabrique d’images **CreateFastMetadataEncoderFromDecoder** et **CreateFastMetadataEncoderFromFrameDecode**.

Comme son nom l’indique, **CreateFastMetadataEncoderFromDecoder** crée un encodeur de métadonnées rapide pour les métadonnées au niveau du décodeur. Les formats d’images natifs fournis par WIC ne prennent pas en charge les métadonnées au niveau du décodeur, mais cette méthode est fournie au cas où un tel format d’image serait développé à l’avenir.

Le scénario le plus courant consiste à obtenir un encodeur de métadonnées rapide à partir d’une image à l’aide de **CreateFastMetadataEncoderFromFrameDecode**. Le code suivant obtient l’encodeur des métadonnées rapides d’un frame décodé et modifie la valeur d’évaluation dans le bloc App1.


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode, 
        &pFME);
}
```



### <a name="using-the-fast-metadata-encoder"></a>Utilisation de l’encodeur de métadonnées rapide

À partir de l’encodeur de métadonnées rapide, vous pouvez obtenir un générateur de requêtes. Cela vous permet d’écrire des métadonnées à l’aide d’une expression de requête comme indiqué précédemment. Une fois les métadonnées définies dans le générateur de requêtes, validez l’encodeur de métadonnées rapide pour finaliser la mise à jour des métadonnées. Le code suivant illustre la définition et la validation des modifications de métadonnées.


```
    if (SUCCEEDED(hr))
    {
        hr = pFME->GetMetadataQueryWriter(&pFMEQW);
    }

    if (SUCCEEDED(hr))
    {
        // Add additional metadata
        PROPVARIANT value;

        PropVariantInit(&value);

        value.vt = VT_UI4;
        value.uiVal = 99;
        hr = pFMEQW->SetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);

        PropVariantClear(&value);
    }

    if (SUCCEEDED(hr))
    {
        hr = pFME->Commit();
    }
}
```



Si la **validation** échoue pour une raison quelconque, vous devrez recoder l’image pour vous assurer que les nouvelles métadonnées sont ajoutées à l’image.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Vue d’ensemble des métadonnées WIC](-wic-about-metadata.md)
</dt> <dt>

[Vue d’ensemble du langage de requête de métadonnées](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Vue d’ensemble de l’extensibilité des métadonnées](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Comment : recoder une image JPEG avec des métadonnées](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 
