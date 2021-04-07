---
description: Cette rubrique fournit une vue d’ensemble de la façon dont vous pouvez utiliser les API WIC (Windows Imaging Component) pour lire et écrire des métadonnées incorporées dans des fichiers image.
ms.assetid: b1e0b936-a13a-42dd-8470-957ba1d90423
title: Vue d’ensemble de la lecture et de l’écriture des métadonnées d’image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 484d562b71184c20adf054f1de2a4203878da9b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952191"
---
# <a name="overview-of-reading-and-writing-image-metadata"></a><span data-ttu-id="4309e-103">Vue d’ensemble de la lecture et de l’écriture des métadonnées d’image</span><span class="sxs-lookup"><span data-stu-id="4309e-103">Overview of Reading and Writing Image Metadata</span></span>

<span data-ttu-id="4309e-104">Cette rubrique fournit une vue d’ensemble de la façon dont vous pouvez utiliser les API WIC (Windows Imaging Component) pour lire et écrire des métadonnées incorporées dans des fichiers image.</span><span class="sxs-lookup"><span data-stu-id="4309e-104">This topic provides an overview of how you can use the Windows Imaging Component (WIC) APIs to read and write metadata that is embedded in image files.</span></span>

<span data-ttu-id="4309e-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="4309e-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="4309e-106">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="4309e-106">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="4309e-107">Introduction</span><span class="sxs-lookup"><span data-stu-id="4309e-107">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="4309e-108">Lecture de Metadadata à l’aide d’un lecteur de requêtes</span><span class="sxs-lookup"><span data-stu-id="4309e-108">Reading Metadadata Using a Query Reader</span></span>](#reading-metadadata-using-a-query-reader)
    -   [<span data-ttu-id="4309e-109">Obtention d’un lecteur de requêtes</span><span class="sxs-lookup"><span data-stu-id="4309e-109">Obtaining a Query Reader</span></span>](#obtaining-a-query-reader)
    -   [<span data-ttu-id="4309e-110">Lecture des métadonnées</span><span class="sxs-lookup"><span data-stu-id="4309e-110">Reading Metadata</span></span>](#reading-metadata)
    -   [<span data-ttu-id="4309e-111">Méthodes de lecteur de requête supplémentaires</span><span class="sxs-lookup"><span data-stu-id="4309e-111">Additional Query Reader Methods</span></span>](#additional-query-reader-methods)
-   [<span data-ttu-id="4309e-112">Écriture de métadonnées à l’aide d’un générateur de requêtes</span><span class="sxs-lookup"><span data-stu-id="4309e-112">Writing Metadata Using a Query Writer</span></span>](#writing-metadata-using-a-query-writer)
    -   [<span data-ttu-id="4309e-113">Obtention d’un générateur de requêtes</span><span class="sxs-lookup"><span data-stu-id="4309e-113">Obtaining a Query Writer</span></span>](#obtaining-a-query-writer)
    -   [<span data-ttu-id="4309e-114">Ajout de métadonnées</span><span class="sxs-lookup"><span data-stu-id="4309e-114">Adding Metadata</span></span>](#adding-metadata)
    -   [<span data-ttu-id="4309e-115">Suppression de métadonnées</span><span class="sxs-lookup"><span data-stu-id="4309e-115">Removing Metadata</span></span>](#removing-metadata)
    -   [<span data-ttu-id="4309e-116">Copie des métadonnées pour le ré-encodage</span><span class="sxs-lookup"><span data-stu-id="4309e-116">Copying Metadata for Re-encoding</span></span>](#copying-metadata-for-re-encoding)
-   [<span data-ttu-id="4309e-117">Encodage de métadonnées rapide</span><span class="sxs-lookup"><span data-stu-id="4309e-117">Fast Metadata Encoding</span></span>](#fast-metadata-encoding)
    -   [<span data-ttu-id="4309e-118">Ajout d’un remplissage à des blocs de métadonnées</span><span class="sxs-lookup"><span data-stu-id="4309e-118">Adding Padding to Metadata Blocks</span></span>](#adding-padding-to-metadata-blocks)
    -   [<span data-ttu-id="4309e-119">Obtention d’un encodeur de métadonnées rapide</span><span class="sxs-lookup"><span data-stu-id="4309e-119">Obtaining a Fast Metadata Encoder</span></span>](#obtaining-a-fast-metadata-encoder)
    -   [<span data-ttu-id="4309e-120">Utilisation de l’encodeur de métadonnées rapide</span><span class="sxs-lookup"><span data-stu-id="4309e-120">Using the Fast Metadata Encoder</span></span>](#using-the-fast-metadata-encoder)
-   [<span data-ttu-id="4309e-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4309e-121">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="4309e-122">Prérequis</span><span class="sxs-lookup"><span data-stu-id="4309e-122">Prerequisites</span></span>

<span data-ttu-id="4309e-123">Pour comprendre cette rubrique, vous devez être familiarisé avec le système de métadonnées WIC, comme décrit dans [vue d’ensemble des métadonnées WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="4309e-123">To understand this topic, you should be familiar with the WIC metadata system as described in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="4309e-124">Vous devez également être familiarisé avec le langage de requête utilisé pour lire et écrire des métadonnées, comme décrit dans [vue d’ensemble du langage de requête de métadonnées](-wic-codec-metadataquerylanguage.md).</span><span class="sxs-lookup"><span data-stu-id="4309e-124">You should also be familiar with the query language used to read and write metadata, as described in [Metadata Query Language Overview](-wic-codec-metadataquerylanguage.md).</span></span>

## <a name="introduction"></a><span data-ttu-id="4309e-125">Introduction</span><span class="sxs-lookup"><span data-stu-id="4309e-125">Introduction</span></span>

<span data-ttu-id="4309e-126">WIC fournit aux développeurs d’applications des composants COM (Component Object Model) pour lire et écrire des métadonnées incorporées dans des fichiers image.</span><span class="sxs-lookup"><span data-stu-id="4309e-126">WIC provides application developers with Component Object Model (COM) components to read and write metadata embedded in image files.</span></span> <span data-ttu-id="4309e-127">Il existe deux façons de lire et d’écrire des métadonnées :</span><span class="sxs-lookup"><span data-stu-id="4309e-127">There are two ways to read and write metadata:</span></span>

-   <span data-ttu-id="4309e-128">Utilisation d’un enregistreur/lecteur de requête et d’une expression de requête pour interroger des blocs de métadonnées pour des blocs imbriqués ou des métadonnées spécifiques au sein d’un bloc.</span><span class="sxs-lookup"><span data-stu-id="4309e-128">Using a query reader/writer and a query expression to query metadata blocks for nested blocks or specific metadata within a block.</span></span>
-   <span data-ttu-id="4309e-129">En utilisant un gestionnaire de métadonnées (un lecteur de métadonnées ou un enregistreur de métadonnées) pour accéder aux blocs de métadonnées imbriqués ou à des métadonnées spécifiques dans les blocs de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="4309e-129">Using a metadata handler (a metadata reader or a metadata writer) to access the nested metadata blocks or specific metadata within the metadata blocks.</span></span>

<span data-ttu-id="4309e-130">La plus simple consiste à utiliser un lecteur/enregistreur de requêtes et une expression de requête pour accéder aux métadonnées.</span><span class="sxs-lookup"><span data-stu-id="4309e-130">The easiest of these is to use a query reader/writer and a query expression to access the metadata.</span></span> <span data-ttu-id="4309e-131">Un lecteur de requête ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) est utilisé pour lire les métadonnées lorsqu’un enregistreur de requête ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) est utilisé pour écrire des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="4309e-131">A query reader ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) is used to read metadata while a query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) is used to write metadata.</span></span> <span data-ttu-id="4309e-132">Les deux utilisent une expression de requête pour lire ou écrire les métadonnées souhaitées.</span><span class="sxs-lookup"><span data-stu-id="4309e-132">Both of these use a query expression to read or write the desired metadata.</span></span> <span data-ttu-id="4309e-133">En arrière-plan, un lecteur de requête (et un enregistreur) utilise un gestionnaire de métadonnées pour accéder aux métadonnées décrites par l’expression de requête.</span><span class="sxs-lookup"><span data-stu-id="4309e-133">Behind the scenes, a query reader (and writer) uses a metadata handler to access the metadata described by the query expression.</span></span>

<span data-ttu-id="4309e-134">La méthode la plus avancée consiste à accéder directement aux gestionnaires de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="4309e-134">The more advanced method is to directly access the metadata handlers.</span></span> <span data-ttu-id="4309e-135">Un gestionnaire de métadonnées est obtenu à partir des frames individuels à l’aide d’un lecteur de bloc ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) ou d’un enregistreur de bloc ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)).</span><span class="sxs-lookup"><span data-stu-id="4309e-135">A metadata handler is obtained from the individual frames using a block reader ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) or a block writer ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)).</span></span> <span data-ttu-id="4309e-136">Les deux types de gestionnaires de métadonnées disponibles sont le lecteur de métadonnées ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) et le writer de métadonnées ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)).</span><span class="sxs-lookup"><span data-stu-id="4309e-136">The two types of metadata handlers available are the metadata reader ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) and the metadata writer ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)).</span></span>

<span data-ttu-id="4309e-137">Le diagramme suivant du contenu d’un fichier image JPEG est utilisé dans les exemples de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="4309e-137">The following diagram of the contents of a JPEG image file is used throughout the examples in this topic.</span></span> <span data-ttu-id="4309e-138">L’image représentée par ce diagramme a été créée à l’aide de Microsoft Paint ; les métadonnées d’évaluation ont été ajoutées à l’aide de la fonctionnalité Galerie de photos de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4309e-138">The image represented by this diagram was created by using Microsoft Paint; the rating metadata was added by using the Photo Gallery feature of Windows Vista.</span></span>

![illustration de l’image JPEG avec les métadonnées d’évaluation](graphics/jpeg.png)

## <a name="reading-metadadata-using-a-query-reader"></a><span data-ttu-id="4309e-140">Lecture de Metadadata à l’aide d’un lecteur de requêtes</span><span class="sxs-lookup"><span data-stu-id="4309e-140">Reading Metadadata Using a Query Reader</span></span>

<span data-ttu-id="4309e-141">Le moyen le plus simple de lire les métadonnées consiste à utiliser l’interface du lecteur de requêtes, [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span><span class="sxs-lookup"><span data-stu-id="4309e-141">The easiest way to read metadata is to use the query reader interface, [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span></span> <span data-ttu-id="4309e-142">Le lecteur de requête vous permet de lire des blocs de métadonnées et des éléments dans des blocs de métadonnées à l’aide d’une expression de requête.</span><span class="sxs-lookup"><span data-stu-id="4309e-142">The query reader enables you to read metadata blocks and items within metadata blocks using a query expression.</span></span>

<span data-ttu-id="4309e-143">Il existe trois façons d’obtenir un lecteur de requête : par le biais d’un décodeur bitmap ([**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)), par le biais de ses cadres individuels ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) ou par le biais d’un générateur de requêtes ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span><span class="sxs-lookup"><span data-stu-id="4309e-143">There are three ways to obtain a query reader: through a bitmap decoder ([**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)), through its individual frames ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)), or through a query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span></span>

### <a name="obtaining-a-query-reader"></a><span data-ttu-id="4309e-144">Obtention d’un lecteur de requêtes</span><span class="sxs-lookup"><span data-stu-id="4309e-144">Obtaining a Query Reader</span></span>

<span data-ttu-id="4309e-145">L’exemple de code suivant montre comment obtenir un décodeur bitmap à partir de la fabrique d’images et récupérer un frame bitmap individuel.</span><span class="sxs-lookup"><span data-stu-id="4309e-145">The following example code shows how to obtain a bitmap decoder from the imaging factory and retrieve an individual bitmap frame.</span></span> <span data-ttu-id="4309e-146">Ce code effectue également le travail d’installation nécessaire à l’obtention d’un lecteur de requêtes à partir d’une trame décodée.</span><span class="sxs-lookup"><span data-stu-id="4309e-146">This code also performs setup work needed to obtain a query reader from a decoded frame.</span></span>


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



<span data-ttu-id="4309e-147">Le décodeur bitmap du fichier test.jpg est obtenu à l’aide de la méthode **CreateDecoderFromFilename** de la fabrique d’images.</span><span class="sxs-lookup"><span data-stu-id="4309e-147">The bitmap decoder for the test.jpg file is obtained by using the **CreateDecoderFromFilename** method of the imaging factory.</span></span> <span data-ttu-id="4309e-148">Dans cette méthode, le quatrième paramètre est défini sur la valeur WICDecodeMetadataCacheOnDemand à partir de l’énumération [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) .</span><span class="sxs-lookup"><span data-stu-id="4309e-148">In this method, the fourth parameter is set to the value WICDecodeMetadataCacheOnDemand from the [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) enumeration.</span></span> <span data-ttu-id="4309e-149">Cela indique au décodeur de mettre en cache les métadonnées lorsque les métadonnées sont nécessaires ; en obtenant un lecteur de requête ou le lecteur de métadonnées sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="4309e-149">This tells the decoder to cache the metadata when the metadata is needed; either by obtaining a query reader or the underlying metadata reader.</span></span> <span data-ttu-id="4309e-150">L’utilisation de cette option vous permet de conserver le flux vers les métadonnées requises pour l’encodage rapide des métadonnées et active le décodage sans perte de l’image JPEG.</span><span class="sxs-lookup"><span data-stu-id="4309e-150">Using this option enables you to retain the stream to the metadata required for fast metadata encoding and enables lossless decoding of the JPEG image.</span></span> <span data-ttu-id="4309e-151">Vous pouvez également utiliser l’autre valeur **WICDecodeOptions** , WICDecodeMetadataCacheOnLoad, qui met en cache les métadonnées de l’image incorporée dès le chargement de l’image.</span><span class="sxs-lookup"><span data-stu-id="4309e-151">Alternatively, you could use the other **WICDecodeOptions** value, WICDecodeMetadataCacheOnLoad, which caches the embedded image metadata as soon as the image is loaded.</span></span>

<span data-ttu-id="4309e-152">Pour obtenir le lecteur de requête du frame, effectuez un appel simple à la méthode **GetMetadataQueryReader** du frame.</span><span class="sxs-lookup"><span data-stu-id="4309e-152">To obtain the frame's query reader, make a simple call to the frame's **GetMetadataQueryReader** method.</span></span> <span data-ttu-id="4309e-153">L’exemple de code suivant illustre cet appel.</span><span class="sxs-lookup"><span data-stu-id="4309e-153">The following code demonstrates this call.</span></span>


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



<span data-ttu-id="4309e-154">De même, un lecteur de requête peut également être obtenu au niveau du décodeur.</span><span class="sxs-lookup"><span data-stu-id="4309e-154">Similarly, a query reader can also be obtained at the decoder level.</span></span> <span data-ttu-id="4309e-155">Un simple appel à la méthode **GetMetadataQueryReader** du décodeur obtient le lecteur de requête du décodeur.</span><span class="sxs-lookup"><span data-stu-id="4309e-155">A simple call to the decoder's **GetMetadataQueryReader** method gets the decoder's query reader.</span></span> <span data-ttu-id="4309e-156">Le lecteur de requêtes d’un décodeur, à la différence du lecteur de requêtes d’un frame, lit les métadonnées d’une image qui se trouve en dehors des frames individuels.</span><span class="sxs-lookup"><span data-stu-id="4309e-156">An decoder's query reader, unlike a frame's query reader, reads metadata for an image that is outside of the individual frames.</span></span> <span data-ttu-id="4309e-157">Toutefois, ce scénario n’est pas courant et les formats d’images natives ne prennent pas en charge cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="4309e-157">However, this scenario is not common, and the native image formats do not support this capability.</span></span> <span data-ttu-id="4309e-158">Les CODECs d’image native fournis par le WIC lisent et écrivent les métadonnées au niveau de la trame, même pour les formats à image unique, tels que JPEG.</span><span class="sxs-lookup"><span data-stu-id="4309e-158">The native image CODECS provided by WIC read and write metadata at the frame level even for single-frame formats such as JPEG.</span></span>

### <a name="reading-metadata"></a><span data-ttu-id="4309e-159">Lecture des métadonnées</span><span class="sxs-lookup"><span data-stu-id="4309e-159">Reading Metadata</span></span>

<span data-ttu-id="4309e-160">Avant de passer à la lecture effective des métadonnées, examinez le diagramme suivant d’un fichier JPEG qui comprend des blocs de métadonnées incorporés et des données réelles à récupérer.</span><span class="sxs-lookup"><span data-stu-id="4309e-160">Before you move on to actually reading metadata, look at the following diagram of a JPEG file that includes embedded metadata blocks and actual data to retrieve.</span></span> <span data-ttu-id="4309e-161">Ce diagramme fournit des légendes pour des blocs de métadonnées et des éléments de l’image qui fournissent l’expression de requête de métadonnées à chaque bloc ou élément.</span><span class="sxs-lookup"><span data-stu-id="4309e-161">This diagram provides callouts to specific metadata blocks and items within the image providing the metadata query expression to each block or item.</span></span>

![illustration de l’image JPEG avec des légendes de métadonnées](graphics/jpegwithcallouts.png)

<span data-ttu-id="4309e-163">Pour rechercher des blocs de métadonnées incorporés ou des éléments spécifiques par nom, appelez la méthode **GetMetadataByName** .</span><span class="sxs-lookup"><span data-stu-id="4309e-163">To query for embedded metadata blocks or specific items by name, call the **GetMetadataByName** method.</span></span> <span data-ttu-id="4309e-164">Cette méthode prend une expression de requête et un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) dans lequel l’élément de métadonnées est retourné.</span><span class="sxs-lookup"><span data-stu-id="4309e-164">This method takes a query expression and a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in which the metadata item is returned.</span></span> <span data-ttu-id="4309e-165">Le code suivant interroge un bloc de métadonnées imbriqué et convertit le composant [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) fourni par la valeur PROPVARIANT en un lecteur de requêtes, s’il est trouvé.</span><span class="sxs-lookup"><span data-stu-id="4309e-165">The following code queries for a nested metadata block and converts the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) component provided by the PROPVARIANT value to a query reader if found.</span></span>


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



<span data-ttu-id="4309e-166">L’expression de requête « /App1/IFD » interroge le bloc IFD imbriqué dans le bloc App1.</span><span class="sxs-lookup"><span data-stu-id="4309e-166">The query expression "/app1/ifd" is querying for the IFD block nested in the App1 block.</span></span> <span data-ttu-id="4309e-167">Le fichier image JPEG contient le bloc de métadonnées imbriquées IFD, donc le [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) est retourné avec un type de variable (VT) de `VT_UNKNOWN` et un pointeur vers une interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) (punkVal).</span><span class="sxs-lookup"><span data-stu-id="4309e-167">The JPEG image file contains the IFD nested metadata block, so the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) is returned with a variable type (vt) of `VT_UNKNOWN` and a pointer to an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface (punkVal).</span></span> <span data-ttu-id="4309e-168">Vous interrogez ensuite l’interface IUnknown pour obtenir un lecteur de requête.</span><span class="sxs-lookup"><span data-stu-id="4309e-168">You then query the IUnknown interface for a query reader.</span></span>

<span data-ttu-id="4309e-169">Le code suivant illustre une nouvelle requête basée sur le nouveau lecteur de requêtes relatif au bloc IFD imbriqué.</span><span class="sxs-lookup"><span data-stu-id="4309e-169">The following code demonstrates a new query based on the new query reader relative to the nested IFD block.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetMetadataByName(L"/{ushort=18249}", &value);
    PropVariantClear(&value); // Clear value for new query
}
```



<span data-ttu-id="4309e-170">L’expression de requête « /{UShort = 18249} » interroge le bloc IFD pour l’évaluation de MicrosoftPhoto incorporée sous la balise 18249.</span><span class="sxs-lookup"><span data-stu-id="4309e-170">The query expression "/{ushort=18249}" queries the IFD block for the MicrosoftPhoto rating embedded under tag 18249.</span></span> <span data-ttu-id="4309e-171">La valeur [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) contient maintenant un type valeur `VT_UI2` et une valeur de données de 50.</span><span class="sxs-lookup"><span data-stu-id="4309e-171">The [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) value will now contain a value type of `VT_UI2` and a data value of 50.</span></span>

<span data-ttu-id="4309e-172">Toutefois, il n’est pas nécessaire d’obtenir un bloc imbriqué avant d’interroger des valeurs de données spécifiques.</span><span class="sxs-lookup"><span data-stu-id="4309e-172">However, it is not necessary to obtain a nested block before querying for specific data values.</span></span> <span data-ttu-id="4309e-173">Par exemple, au lieu d’interroger l’IFD imbriqué, puis pour l’évaluation de MicrosoftPhoto, vous pouvez utiliser à la place le bloc de métadonnées racine et la requête illustrée dans le code suivant pour obtenir les mêmes informations.</span><span class="sxs-lookup"><span data-stu-id="4309e-173">For instance, instead of querying for the nested IFD and then for the MicrosoftPhoto rating, you can instead use the root metadata block and the query shown in the following code to obtain the same information.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);
    PropVariantClear(&value);
}
```



<span data-ttu-id="4309e-174">Outre l’interrogation d’éléments de métadonnées spécifiques dans un bloc de métadonnées, vous pouvez également énumérer tous les éléments de métadonnées dans un bloc de métadonnées (à l’exclusion des éléments de métadonnées dans les blocs de métadonnées imbriqués).</span><span class="sxs-lookup"><span data-stu-id="4309e-174">In addition to querying for specific metadata items in a metadata block, you can also enumerate all the metadata items in a metadata block (not including metadata items in nested metadata blocks).</span></span> <span data-ttu-id="4309e-175">Pour énumérer les éléments de métadonnées dans le bloc actuel, la méthode **GetEnumeration** du lecteur de requête est utilisée.</span><span class="sxs-lookup"><span data-stu-id="4309e-175">To enumerate the metadata items in the current block, the query reader's **GetEnumeration** method is used.</span></span> <span data-ttu-id="4309e-176">Cette méthode obtient une interface **IEnumString** remplie avec les éléments de métadonnées du bloc en cours.</span><span class="sxs-lookup"><span data-stu-id="4309e-176">This method obtains an **IEnumString** interface populated with the metadata items in the current block.</span></span> <span data-ttu-id="4309e-177">Par exemple, le code suivant énumère les évaluations XMP et MicrosoftPhoto pour le bloc IFD imbriqué qui a été obtenu précédemment.</span><span class="sxs-lookup"><span data-stu-id="4309e-177">For example, the following code enumerates the XMP rating and MicrosoftPhoto rating for the nested IFD block that was obtained earlier.</span></span>


```
IEnumString *metadataItems = NULL;

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetEnumerator(&metadataItems);
}
```



<span data-ttu-id="4309e-178">Pour plus d’informations sur l’identification des balises appropriées pour différents formats d’image et formats de métadonnées, consultez [requêtes de métadonnées de format d’image native](-wic-native-image-format-metadata-queries.md).</span><span class="sxs-lookup"><span data-stu-id="4309e-178">For more information on identifying appropriate tags for various image formats and metadata formats, see [Native Image Format Metadata Queries](-wic-native-image-format-metadata-queries.md).</span></span>

### <a name="additional-query-reader-methods"></a><span data-ttu-id="4309e-179">Méthodes de lecteur de requête supplémentaires</span><span class="sxs-lookup"><span data-stu-id="4309e-179">Additional Query Reader Methods</span></span>

<span data-ttu-id="4309e-180">Outre la lecture des métadonnées, vous pouvez également obtenir des informations supplémentaires sur le lecteur de requête et obtenir des métadonnées par d’autres moyens.</span><span class="sxs-lookup"><span data-stu-id="4309e-180">In addition to reading metadata, you can also obtain additional information about the query reader and obtain metadata through other means.</span></span> <span data-ttu-id="4309e-181">Le lecteur de requête fournit deux méthodes qui fournissent des informations sur le lecteur de requêtes, **GetContainerFormat** et **GetLocation**.</span><span class="sxs-lookup"><span data-stu-id="4309e-181">The query reader provides two methods that provide information about the query reader, **GetContainerFormat** and **GetLocation**.</span></span>

<span data-ttu-id="4309e-182">Avec le lecteur de requête incorporé, vous pouvez utiliser **GetContainerFormat** pour déterminer le type de bloc de métadonnées, et vous pouvez appeler **GetLocation** pour obtenir le chemin d’accès relatif au bloc de métadonnées racine.</span><span class="sxs-lookup"><span data-stu-id="4309e-182">With the embedded query reader, you can use **GetContainerFormat** to determine the type of metadata block, and you can call **GetLocation** to obtain the path relative to the root metadata block.</span></span> <span data-ttu-id="4309e-183">Le code suivant interroge le lecteur de requête incorporé pour obtenir son emplacement.</span><span class="sxs-lookup"><span data-stu-id="4309e-183">The following code queries the embedded query reader for its location.</span></span>


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



<span data-ttu-id="4309e-184">L’appel à **GetContainerFormat** pour le lecteur de requêtes incorporées retourne le GUID du format de métadonnées IFD.</span><span class="sxs-lookup"><span data-stu-id="4309e-184">The call to **GetContainerFormat** for the embedded query reader returns the IFD metadata format GUID.</span></span> <span data-ttu-id="4309e-185">L’appel à **GetLocation** retourne un espace de noms de « /App1/IFD »; fournir le chemin d’accès relatif à partir duquel les requêtes suivantes au nouveau lecteur de requête seront exécutées.</span><span class="sxs-lookup"><span data-stu-id="4309e-185">The call to **GetLocation** returns a namespace of "/app1/ifd"; providing you with the relative path from which subsequent queries to the new query reader will be executed.</span></span> <span data-ttu-id="4309e-186">Bien entendu, le code précédent n’est pas très utile, mais il montre comment utiliser la méthode **GetLocation** pour rechercher des blocs de métadonnées imbriqués.</span><span class="sxs-lookup"><span data-stu-id="4309e-186">Of course, the preceding code isn't very useful, but it does demonstrate how to use the **GetLocation** method for finding nested metadata blocks.</span></span>

## <a name="writing-metadata-using-a-query-writer"></a><span data-ttu-id="4309e-187">Écriture de métadonnées à l’aide d’un générateur de requêtes</span><span class="sxs-lookup"><span data-stu-id="4309e-187">Writing Metadata Using a Query Writer</span></span>

> [!Note]  
> <span data-ttu-id="4309e-188">Certains des exemples de code fournis dans cette section ne sont pas affichés dans le contexte des étapes réelles requises pour écrire des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="4309e-188">Some of the code examples provided in this section are not shown in the context of the actual steps required to write metadata.</span></span> <span data-ttu-id="4309e-189">Pour afficher les exemples de code dans le contexte d’un exemple fonctionnel, consultez le didacticiel Comment : recoder une image avec des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="4309e-189">To view the code examples in the context of a working sample, see the How-to: Re-encode an Image with Metadata tutorial.</span></span>

 

<span data-ttu-id="4309e-190">Le principal composant pour écrire des métadonnées est le générateur de requêtes ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span><span class="sxs-lookup"><span data-stu-id="4309e-190">The main component for writing metadata is the query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span></span> <span data-ttu-id="4309e-191">Le générateur de requêtes vous permet de définir et de supprimer des blocs de métadonnées et des éléments au sein d’un bloc de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="4309e-191">The query writer enables you to set and remove metadata blocks and items within a metadata block.</span></span>

<span data-ttu-id="4309e-192">À l’instar du lecteur de requêtes, il existe trois façons d’obtenir un générateur de requêtes : par le biais d’un encodeur bitmap ([**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)), par le biais de ses propres frames ([**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)) ou par l’intermédiaire d’un encodeur de métadonnées rapide ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)).</span><span class="sxs-lookup"><span data-stu-id="4309e-192">Like the query reader, there are three ways to obtain a query writer: through a bitmap encoder ([**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)), through its individual frames ([**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)), or through a fast metadata encoder ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)).</span></span>

### <a name="obtaining-a-query-writer"></a><span data-ttu-id="4309e-193">Obtention d’un générateur de requêtes</span><span class="sxs-lookup"><span data-stu-id="4309e-193">Obtaining a Query Writer</span></span>

<span data-ttu-id="4309e-194">Le générateur de requêtes le plus courant concerne un frame individuel d’une image bitmap.</span><span class="sxs-lookup"><span data-stu-id="4309e-194">The most common query writer is for an individual frame of a bitmap.</span></span> <span data-ttu-id="4309e-195">Cet enregistreur de requêtes définit et supprime les éléments et les blocs de métadonnées d’un frame d’image.</span><span class="sxs-lookup"><span data-stu-id="4309e-195">This query writer sets and removes an image frame's metadata blocks and items.</span></span> <span data-ttu-id="4309e-196">Pour obtenir le générateur de requêtes d’un frame d’image, appelez la méthode **GetMetadataQueryWriter** du frame.</span><span class="sxs-lookup"><span data-stu-id="4309e-196">To obtain an image frame's query writer, call the frame's **GetMetadataQueryWriter** method.</span></span> <span data-ttu-id="4309e-197">Le code suivant illustre l’appel de méthode simple pour obtenir le générateur de requêtes d’un frame.</span><span class="sxs-lookup"><span data-stu-id="4309e-197">The following code demonstrates the simple method call to obtain a frame's query writer.</span></span>


```
IWICMetadataQueryWriter &pFrameQWriter = NULL;

//Obtain a query writer from the frame.
hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
```



<span data-ttu-id="4309e-198">De même, un enregistreur de requête peut également être obtenu pour le niveau de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="4309e-198">Similarly, a query writer can also be obtained for the encoder level.</span></span> <span data-ttu-id="4309e-199">Un simple appel à la méthode **GetMetadataQueryWriter** de l’encodeur obtient le générateur de requêtes de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="4309e-199">A simple call to the encoder's **GetMetadataQueryWriter** method gets the encoder's query writer.</span></span> <span data-ttu-id="4309e-200">Le générateur de requêtes d’un encodeur, à la différence du writer de requête d’un frame, écrit les métadonnées d’une image en dehors du frame individuel.</span><span class="sxs-lookup"><span data-stu-id="4309e-200">An encoder's query writer, unlike a frame's query writer, writes metadata for an image outside of the individual frame.</span></span> <span data-ttu-id="4309e-201">Toutefois, ce scénario n’est pas courant et les formats d’images natives ne prennent pas en charge cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="4309e-201">However, this scenario is not common, and the native image formats do not support this capability.</span></span> <span data-ttu-id="4309e-202">Les codecs d’image native fournis par le WIC lisent et écrivent les métadonnées au niveau de la trame, même pour les formats à image unique, tels que JPEG.</span><span class="sxs-lookup"><span data-stu-id="4309e-202">The native image codecs provided by WIC read and write metadata at the frame level even for single-frame formats such as JPEG.</span></span>

<span data-ttu-id="4309e-203">Vous pouvez également obtenir un enregistreur de requête directement à partir de la fabrique d’images ([**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)).</span><span class="sxs-lookup"><span data-stu-id="4309e-203">You can also obtain a query writer directly from the imaging factory ([**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)).</span></span> <span data-ttu-id="4309e-204">Deux méthodes de fabrique d’images renvoient un générateur de requêtes : **CreateQueryWriter** et **CreateQueryWriterFromReader**.</span><span class="sxs-lookup"><span data-stu-id="4309e-204">There are two imaging factory methods that return a query writer: **CreateQueryWriter** and **CreateQueryWriterFromReader**.</span></span>

<span data-ttu-id="4309e-205">**CreateQueryWriter** crée un enregistreur de requête pour le format de métadonnées et le fournisseur spécifiés.</span><span class="sxs-lookup"><span data-stu-id="4309e-205">**CreateQueryWriter** creates a query writer for the specified metadata format and vendor.</span></span> <span data-ttu-id="4309e-206">Ce writer de requête vous permet d’écrire des métadonnées pour un format de métadonnées spécifique et de les ajouter à l’image.</span><span class="sxs-lookup"><span data-stu-id="4309e-206">This query writer enables you to write metadata for a specific metadata format and add it to the image.</span></span> <span data-ttu-id="4309e-207">Le code suivant illustre un appel **CreateQueryWriter** pour créer un générateur de requêtes XMP.</span><span class="sxs-lookup"><span data-stu-id="4309e-207">The following code demonstrates a **CreateQueryWriter** call to create an XMP query writer.</span></span>


```
IWICMetadataQueryWriter *pXMPWriter = NULL;

// Create XMP block
GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriter(
        GUID_MetadataFormatXMP,
        &vendor,
        &pXMPWriter);
```



<span data-ttu-id="4309e-208">Dans cet exemple, le nom convivial `GUID_MetadataFormatXMP` est utilisé comme paramètre *guidMetadataFormat* .</span><span class="sxs-lookup"><span data-stu-id="4309e-208">In this example, the friendly name `GUID_MetadataFormatXMP` is used as the *guidMetadataFormat* parameter.</span></span> <span data-ttu-id="4309e-209">Il représente le GUID du format de métadonnées XMP et le fournisseur représente le gestionnaire créé par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4309e-209">It represents the XMP metadata format GUID, and vendor represents the Microsoft created handler.</span></span> <span data-ttu-id="4309e-210">Sinon, la **valeur null** peut être transmise en tant que paramètre *pGuidVendor* avec les mêmes résultats si aucun autre gestionnaire XMP n’existe.</span><span class="sxs-lookup"><span data-stu-id="4309e-210">Alternatively, **NULL** can be passed as the *pguidVendor* parameter with the same results if no other XMP handler exists.</span></span> <span data-ttu-id="4309e-211">Si un gestionnaire XMP personnalisé est installé en même temps que le gestionnaire XMP natif, le passage de la **valeur null** pour le fournisseur entraînera le renvoi du GUID le plus bas dans le générateur de requêtes.</span><span class="sxs-lookup"><span data-stu-id="4309e-211">If a custom XMP handler is installed alongside the native XMP handler, passing **NULL** for the vendor will result in the query writer with the lowest GUID being returned.</span></span>

<span data-ttu-id="4309e-212">**CreateQueryWriterFromReader** est similaire à la méthode **CreateQueryWriter** , à ceci près qu’elle préremplit le nouvel enregistreur de requête avec les données fournies par le lecteur de requête.</span><span class="sxs-lookup"><span data-stu-id="4309e-212">**CreateQueryWriterFromReader** is similar to the **CreateQueryWriter** method except that it prepopulates the new query writer with the data provided by the query reader.</span></span> <span data-ttu-id="4309e-213">Cela est utile pour recoder une image tout en conservant les métadonnées existantes ou pour supprimer les métadonnées indésirables.</span><span class="sxs-lookup"><span data-stu-id="4309e-213">This is useful for re-encoding an image while maintaining the existing metadata, or for removing unwanted metadata.</span></span> <span data-ttu-id="4309e-214">Le code suivant illustre un appel **CreateQueryWriterFromReader** .</span><span class="sxs-lookup"><span data-stu-id="4309e-214">The following code demonstrates a **CreateQueryWriterFromReader** call.</span></span>


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



### <a name="adding-metadata"></a><span data-ttu-id="4309e-215">Ajout de métadonnées</span><span class="sxs-lookup"><span data-stu-id="4309e-215">Adding Metadata</span></span>

<span data-ttu-id="4309e-216">Une fois que vous avez obtenu un générateur de requêtes, vous pouvez l’utiliser pour ajouter des blocs de métadonnées et des éléments.</span><span class="sxs-lookup"><span data-stu-id="4309e-216">After you obtain a query writer, you can use it to add metadata blocks and items.</span></span> <span data-ttu-id="4309e-217">Pour écrire des métadonnées, vous utilisez la méthode **SetMetadataByName** du générateur de requêtes.</span><span class="sxs-lookup"><span data-stu-id="4309e-217">To write metadata, you use the query writer's **SetMetadataByName** method.</span></span> <span data-ttu-id="4309e-218">**SetMetadataByName** accepte deux paramètres : une expression de requête (*wzName*) et un pointeur vers [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*pvarValue*).</span><span class="sxs-lookup"><span data-stu-id="4309e-218">**SetMetadataByName** takes two parameters: a query expression (*wzName*) and a pointer to a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*pvarValue*).</span></span> <span data-ttu-id="4309e-219">L’expression de requête définit le bloc ou l’élément à définir lorsque le PROPVARIANT fournit la valeur de données réelle à définir.</span><span class="sxs-lookup"><span data-stu-id="4309e-219">The query expression defines the block or item to set while the PROPVARIANT provides the actual data value to set.</span></span>

<span data-ttu-id="4309e-220">L’exemple suivant montre comment ajouter un titre à l’aide du writer de requête XMP obtenu précédemment à l’aide de la méthode **CreateQueryWriter** .</span><span class="sxs-lookup"><span data-stu-id="4309e-220">The following example demonstrates how to add a title by using the XMP query writer previously obtained by using the **CreateQueryWriter** method.</span></span>


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



<span data-ttu-id="4309e-221">Dans cet exemple, le type de la valeur (VT) a `VT_LPWSTR` la valeur, ce qui indique qu’une chaîne sera utilisée comme valeur de données.</span><span class="sxs-lookup"><span data-stu-id="4309e-221">In this example, value's type (vt) is set to `VT_LPWSTR`, indicating that a string will be used as the data value.</span></span> <span data-ttu-id="4309e-222">Étant donné que le type de la *valeur* est une chaîne, *pwszVal* est utilisé pour définir le titre à utiliser.</span><span class="sxs-lookup"><span data-stu-id="4309e-222">Because *value*'s type is a string, *pwszVal* is used to set the title to use.</span></span> <span data-ttu-id="4309e-223">**SetMetadataByName** est ensuite appelée à l’aide de l’expression de requête « /DC : title » et du [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)nouvellement défini.</span><span class="sxs-lookup"><span data-stu-id="4309e-223">**SetMetadataByName** is then called using the query expression "/dc:title" and the newly set [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span> <span data-ttu-id="4309e-224">L’expression de requête utilisée indique que la propriété titre du schéma de l’appareil photo numérique (DC) doit être définie.</span><span class="sxs-lookup"><span data-stu-id="4309e-224">The query expression used indicates that the title property in the digital camera (dc) schema should be set.</span></span> <span data-ttu-id="4309e-225">Notez que l’expression n’est pas « /XMP/DC : title »; Cela est dû au fait que le générateur de requêtes est déjà spécifique à XMP et qu’il ne contient pas de bloc XMP incorporé, que « /XMP/DC : title » suggère.</span><span class="sxs-lookup"><span data-stu-id="4309e-225">Note that the expression is not "/xmp/dc:title"; this is because the query writer is already specific to XMP and does not contain an embedded XMP block, which "/xmp/dc:title" would suggest.</span></span>

<span data-ttu-id="4309e-226">Jusqu’à présent, vous n’avez pas ajouté de métadonnées à une image.</span><span class="sxs-lookup"><span data-stu-id="4309e-226">Up to this point you haven't actually added any metadata to an image frame.</span></span> <span data-ttu-id="4309e-227">Vous avez simplement renseigné un générateur de requêtes avec des données.</span><span class="sxs-lookup"><span data-stu-id="4309e-227">You've simply populated a query writer with data.</span></span> <span data-ttu-id="4309e-228">Pour ajouter à un frame un bloc de métadonnées représenté par le générateur de requêtes, vous appelez à nouveau **SetMetadataByName** à l’aide du générateur de requêtes comme valeur de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span><span class="sxs-lookup"><span data-stu-id="4309e-228">To add to a frame a metadata block represented by the query writer, you again call **SetMetadataByName** using the query writer as the value of the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span> <span data-ttu-id="4309e-229">Cela copie efficacement les métadonnées dans le générateur de requêtes dans le frame d’image.</span><span class="sxs-lookup"><span data-stu-id="4309e-229">This effectively copies the metadata in the query writer to the image frame.</span></span> <span data-ttu-id="4309e-230">Le code suivant montre comment ajouter les métadonnées dans le générateur de requêtes XMP précédemment obtenues dans le bloc de métadonnées racine d’un frame.</span><span class="sxs-lookup"><span data-stu-id="4309e-230">The following code demonstrates how to add the metadata in the XMP query writer previously obtained to a frame's root metadata block.</span></span>


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



<span data-ttu-id="4309e-231">Dans cet exemple, un type valeur (VT) de `VT_UNKOWN` est utilisé, ce qui indique un type valeur d’interface com.</span><span class="sxs-lookup"><span data-stu-id="4309e-231">In this example, a value type (vt) of `VT_UNKOWN` is used; indicating a COM interface value type.</span></span> <span data-ttu-id="4309e-232">Le générateur de requêtes XMP (piXMPWriter) est ensuite utilisé comme valeur du [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), en y ajoutant une référence à l’aide de la méthode AddRef.</span><span class="sxs-lookup"><span data-stu-id="4309e-232">The XMP query writer (piXMPWriter) is then used as the value of the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), adding a reference to it by using the AddRef method.</span></span> <span data-ttu-id="4309e-233">Enfin, le générateur de requêtes XMP est défini en appelant la méthode **SetMetadataByName** du frame et en passant l’expression de requête « / », en indiquant le bloc racine et le PROPVARIANT nouvellement défini.</span><span class="sxs-lookup"><span data-stu-id="4309e-233">Finally, the XMP query writer is set by calling the frame's **SetMetadataByName** method and passing the query expression "/", indicating the root block, and the newly set PROPVARIANT.</span></span>

> [!Note]  
> <span data-ttu-id="4309e-234">Si le frame contient déjà le bloc de métadonnées que vous essayez d’ajouter, les métadonnées que vous ajoutez seront ajoutées et les métadonnées existantes seront remplacées.</span><span class="sxs-lookup"><span data-stu-id="4309e-234">If the frame already contains the metadata block you are trying to add, the metadata you are adding will be added and existing metadata overwritten.</span></span>

 

### <a name="removing-metadata"></a><span data-ttu-id="4309e-235">Suppression de métadonnées</span><span class="sxs-lookup"><span data-stu-id="4309e-235">Removing Metadata</span></span>

<span data-ttu-id="4309e-236">Un générateur de requêtes vous permet également de supprimer des métadonnées en appelant la méthode **RemoveMetadataByName** .</span><span class="sxs-lookup"><span data-stu-id="4309e-236">A query writer also enables you to remove metadata by calling the **RemoveMetadataByName** method.</span></span> <span data-ttu-id="4309e-237">**RemoveMetadataByName** prend une expression de requête et supprime le bloc de métadonnées ou l’élément s’il existe.</span><span class="sxs-lookup"><span data-stu-id="4309e-237">**RemoveMetadataByName** takes a query expression and removes the metadata block or item if it exists.</span></span> <span data-ttu-id="4309e-238">Le code suivant montre comment supprimer le titre précédemment ajouté.</span><span class="sxs-lookup"><span data-stu-id="4309e-238">The following code demonstrates how to remove the title that was previously added.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp/dc:title");
}
```



<span data-ttu-id="4309e-239">Le code suivant montre comment supprimer l’intégralité du bloc de métadonnées XMP.</span><span class="sxs-lookup"><span data-stu-id="4309e-239">The following code demonstrates how to remove the entire XMP metadata block.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp");
}
```



### <a name="copying-metadata-for-re-encoding"></a><span data-ttu-id="4309e-240">Copie des métadonnées pour le ré-encodage</span><span class="sxs-lookup"><span data-stu-id="4309e-240">Copying Metadata for Re-encoding</span></span>

> [!Note]  
> <span data-ttu-id="4309e-241">Le code de cette section est valide uniquement lorsque les formats d’image source et de destination sont identiques.</span><span class="sxs-lookup"><span data-stu-id="4309e-241">The code in this section is valid only when the source and destination image formats are the same.</span></span> <span data-ttu-id="4309e-242">Vous ne pouvez pas copier toutes les métadonnées d’une image en une seule opération lors de l’encodage dans un format d’image différent.</span><span class="sxs-lookup"><span data-stu-id="4309e-242">You cannot copy all of an image's metadata in a single operation when encoding to a different image format.</span></span>

 

<span data-ttu-id="4309e-243">Pour conserver les métadonnées tout en recodant une image au même format d’image, il existe des méthodes permettant de copier toutes les métadonnées en une seule opération.</span><span class="sxs-lookup"><span data-stu-id="4309e-243">To preserve metadata while re-encoding an image to the same image format, there are methods available for copying all the metadata in a single operation.</span></span> <span data-ttu-id="4309e-244">Chacune de ces opérations suit un modèle similaire. chaque définit les métadonnées de l’image décodée directement dans le nouveau Frame encodé.</span><span class="sxs-lookup"><span data-stu-id="4309e-244">Each of these operations follows a similar pattern; each sets the decoded frame's metadata directly into the new frame being encoded.</span></span>

<span data-ttu-id="4309e-245">La méthode recommandée pour copier les métadonnées consiste à initialiser le writer de bloc du nouveau Frame avec le lecteur de bloc du frame décodé.</span><span class="sxs-lookup"><span data-stu-id="4309e-245">The preferred method to copy metadata is to initialize the new frame's block writer with the decoded frame's block reader.</span></span> <span data-ttu-id="4309e-246">L’exemple de code suivant illustre cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4309e-246">The following code demonstrates this method.</span></span>


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



<span data-ttu-id="4309e-247">Dans cet exemple, le lecteur de bloc et le writer de bloc sont obtenus à partir de l’image source et du frame de destination, respectivement.</span><span class="sxs-lookup"><span data-stu-id="4309e-247">In this example, the block reader and the block writer are obtained from the source frame and destination frame, respectively.</span></span> <span data-ttu-id="4309e-248">Le writer de bloc est ensuite initialisé à partir du lecteur de bloc.</span><span class="sxs-lookup"><span data-stu-id="4309e-248">The block writer is then initialized from the block reader.</span></span> <span data-ttu-id="4309e-249">Cela initialise le lecteur de bloc avec les métadonnées préremplies du lecteur de bloc.</span><span class="sxs-lookup"><span data-stu-id="4309e-249">This initializes the block reader with the pre-populated metadata of the block reader.</span></span>

<span data-ttu-id="4309e-250">Une autre méthode pour copier les métadonnées consiste à écrire le bloc de métadonnées référencé par le lecteur de requête à l’aide du générateur de requêtes de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="4309e-250">Another method to copy metadata is to write the metadata block referenced by the query reader using the encoder's query writer.</span></span> <span data-ttu-id="4309e-251">L’exemple de code suivant illustre cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4309e-251">The following code demonstrates this method.</span></span>


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



<span data-ttu-id="4309e-252">Ici, un lecteur de requête est obtenu à partir de l’image décodée, puis utilisé en tant que valeur de propriété du [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) avec un type valeur défini sur VT \_ inconnu.</span><span class="sxs-lookup"><span data-stu-id="4309e-252">Here, a query reader is obtained from the decoded frame and then used as the property value of the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) with a value type set to VT\_UNKNOWN.</span></span> <span data-ttu-id="4309e-253">Le générateur de requêtes pour l’encodeur est obtenu et l’expression de requête « / » est utilisée pour définir les métadonnées au niveau du chemin de navigation racine.</span><span class="sxs-lookup"><span data-stu-id="4309e-253">The query writer for the encoder is obtained and the query expression "/" is used to set the metadata at the root navigation path.</span></span> <span data-ttu-id="4309e-254">Vous pouvez également utiliser cette méthode lors de la définition de blocs de métadonnées imbriqués, en ajustant l’expression de requête à l’emplacement souhaité.</span><span class="sxs-lookup"><span data-stu-id="4309e-254">You can also use this method when setting nested metadata blocks, by adjusting the query expression to the desired location.</span></span>

<span data-ttu-id="4309e-255">De même, vous pouvez créer un writer de requête basé sur le lecteur de requêtes de l’image décodée à l’aide de la méthode **CreateQueryWriterFromReader** de la fabrique d’images.</span><span class="sxs-lookup"><span data-stu-id="4309e-255">Similarly, you can create a query writer based on the decoded frame's query reader by using the imaging factory's **CreateQueryWriterFromReader** method.</span></span> <span data-ttu-id="4309e-256">Le générateur de requêtes créé dans cette opération est prérempli avec les métadonnées du lecteur de requêtes et peut ensuite être défini dans le frame.</span><span class="sxs-lookup"><span data-stu-id="4309e-256">The query writer created in this operation will be prepopulated with the metadata from the query reader and can then be set in the frame.</span></span> <span data-ttu-id="4309e-257">Le code suivant illustre l’opération de copie **CreateQueryWriterFromReader** .</span><span class="sxs-lookup"><span data-stu-id="4309e-257">The following code demonstrates the **CreateQueryWriterFromReader** copy operation.</span></span>


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



<span data-ttu-id="4309e-258">Cette méthode utilise un writer de requête distinct créé en fonction des données du lecteur de requête.</span><span class="sxs-lookup"><span data-stu-id="4309e-258">This method uses a separate query writer is created that is based on the data of the query reader.</span></span> <span data-ttu-id="4309e-259">Ce nouvel enregistreur de requête est ensuite défini dans le frame.</span><span class="sxs-lookup"><span data-stu-id="4309e-259">This new query writer then set in the frame.</span></span>

<span data-ttu-id="4309e-260">Là encore, ces opérations de copie des métadonnées fonctionnent uniquement lorsque les images source et de destination ont le même format.</span><span class="sxs-lookup"><span data-stu-id="4309e-260">Again, these operations to copy metadata only work when the source and destination images have the same format.</span></span> <span data-ttu-id="4309e-261">Cela est dû au fait que différents formats d’image stockent les blocs de métadonnées à différents emplacements.</span><span class="sxs-lookup"><span data-stu-id="4309e-261">This is because different image formats store the metadata blocks in different locations.</span></span> <span data-ttu-id="4309e-262">Par exemple, les fichiers JPEG et TIFF prennent en charge les blocs de métadonnées XMP.</span><span class="sxs-lookup"><span data-stu-id="4309e-262">For instance, both JPEG and TIFF support XMP metadata blocks.</span></span> <span data-ttu-id="4309e-263">Dans les images JPEG, le bloc XMP se trouve dans le bloc de métadonnées racine, comme illustré dans la [vue d’ensemble des métadonnées WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="4309e-263">In JPEG images, the XMP block is at the root metadata block as illustrated in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="4309e-264">Toutefois, dans une image TIFF, le bloc XMP est imbriqué dans un bloc IFD racine.</span><span class="sxs-lookup"><span data-stu-id="4309e-264">However, in a TIFF image, the XMP block is nested in a root IFD block.</span></span> <span data-ttu-id="4309e-265">Le diagramme suivant illustre les différences entre une image JPEG et une image TIFF avec les mêmes métadonnées d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="4309e-265">The following diagram illustrates the differences between a JPEG image and a TIFF image with the same rating metadata.</span></span>

![comparaison JPEG et TIFF.](graphics/jpgvstiff.png)

## <a name="fast-metadata-encoding"></a><span data-ttu-id="4309e-267">Encodage de métadonnées rapide</span><span class="sxs-lookup"><span data-stu-id="4309e-267">Fast Metadata Encoding</span></span>

<span data-ttu-id="4309e-268">Il n’est pas toujours nécessaire de recoder une image pour y écrire de nouvelles métadonnées.</span><span class="sxs-lookup"><span data-stu-id="4309e-268">It is not always necessary to re-encode an image to write new metadata to it.</span></span> <span data-ttu-id="4309e-269">Les métadonnées peuvent également être écrites à l’aide d’un encodeur de métadonnées rapide.</span><span class="sxs-lookup"><span data-stu-id="4309e-269">Metadata can also be written by using a fast metadata encoder.</span></span> <span data-ttu-id="4309e-270">Un encodeur de métadonnées rapide peut écrire une quantité limitée de métadonnées dans une image sans recodage de l’image.</span><span class="sxs-lookup"><span data-stu-id="4309e-270">A fast metadata encoder can write a limited amount of metadata to an image without re-encoding the image.</span></span> <span data-ttu-id="4309e-271">Pour ce faire, vous devez écrire les nouvelles métadonnées dans le remplissage vide fourni par certains formats de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="4309e-271">This is accomplished by writing the new metadata within the empty padding provided by some metadata formats.</span></span> <span data-ttu-id="4309e-272">Les formats de métadonnées natifs qui prennent en charge le remplissage des métadonnées sont EXIF, IFD, GPS et XMP.</span><span class="sxs-lookup"><span data-stu-id="4309e-272">The native metadata formats that support metadata padding are Exif, IFD, GPS and XMP.</span></span>

### <a name="adding-padding-to-metadata-blocks"></a><span data-ttu-id="4309e-273">Ajout d’un remplissage à des blocs de métadonnées</span><span class="sxs-lookup"><span data-stu-id="4309e-273">Adding Padding to Metadata Blocks</span></span>

<span data-ttu-id="4309e-274">Avant de pouvoir effectuer un encodage de métadonnées rapide, il doit y avoir de l’espace dans le bloc de métadonnées pour écrire davantage de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="4309e-274">Before you can perform fast metadata encoding, there must be room within the metadata block to write more metadata.</span></span> <span data-ttu-id="4309e-275">S’il n’y a pas assez de place dans le remplissage existant pour écrire les nouvelles métadonnées, l’encodage de métadonnées rapide échoue.</span><span class="sxs-lookup"><span data-stu-id="4309e-275">If there is not enough room within the existing padding to write the new metadata, the fast metadata encoding will fail.</span></span> <span data-ttu-id="4309e-276">Pour ajouter une marge intérieure des métadonnées à une image, l’image doit être à nouveau codée.</span><span class="sxs-lookup"><span data-stu-id="4309e-276">To add metadata padding to an image, the image must be re-encoded.</span></span> <span data-ttu-id="4309e-277">Vous pouvez ajouter un remplissage de la même façon que vous ajoutez tout autre élément de métadonnées, à l’aide d’une expression de requête, si le bloc de métadonnées que vous complétez le prend en charge.</span><span class="sxs-lookup"><span data-stu-id="4309e-277">You can add padding the same way you would add any other metadata item, by using a query expression, if the metadata block you are padding supports it.</span></span> <span data-ttu-id="4309e-278">L’exemple suivant montre comment ajouter un remplissage à un bloc IFD incorporé dans un bloc App1.</span><span class="sxs-lookup"><span data-stu-id="4309e-278">The following example demonstrates how to add padding to an IFD block embedded in an App1 block.</span></span>


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



<span data-ttu-id="4309e-279">Pour ajouter le remplissage, créez un PROPVARIANT de type VT \_ UI4 et une valeur correspondant au nombre d’octets de remplissage à ajouter.</span><span class="sxs-lookup"><span data-stu-id="4309e-279">To add padding, create a PROPVARIANT of type VT\_UI4 and a value corresponding to the number of bytes of padding to add.</span></span> <span data-ttu-id="4309e-280">Une valeur typique est 4096 octets.</span><span class="sxs-lookup"><span data-stu-id="4309e-280">A typical value is 4096 bytes.</span></span> <span data-ttu-id="4309e-281">Les requêtes de métadonnées pour JPEG, TIFF et JPEG-XR sont répertoriées dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="4309e-281">The metadata queries for JPEG, TIFF, and JPEG-XR are in this table.</span></span>



| <span data-ttu-id="4309e-282">Format de métadonnées</span><span class="sxs-lookup"><span data-stu-id="4309e-282">Metadata format</span></span> | <span data-ttu-id="4309e-283">Requête de métadonnées JPEG</span><span class="sxs-lookup"><span data-stu-id="4309e-283">JPEG metadata query</span></span>                  | <span data-ttu-id="4309e-284">TIFF, JPEG-requête de métadonnées XR</span><span class="sxs-lookup"><span data-stu-id="4309e-284">TIFF, JPEG-XR metadata query</span></span>    |
|-----------------|--------------------------------------|---------------------------------|
| <span data-ttu-id="4309e-285">IFD</span><span class="sxs-lookup"><span data-stu-id="4309e-285">IFD</span></span>             | <span data-ttu-id="4309e-286">/app1/ifd/PaddingSchema : remplissage</span><span class="sxs-lookup"><span data-stu-id="4309e-286">/app1/ifd/PaddingSchema:Padding</span></span>      | <span data-ttu-id="4309e-287">/ifd/PaddingSchema : remplissage</span><span class="sxs-lookup"><span data-stu-id="4309e-287">/ifd/PaddingSchema:Padding</span></span>      |
| <span data-ttu-id="4309e-288">EXIF</span><span class="sxs-lookup"><span data-stu-id="4309e-288">EXIF</span></span>            | <span data-ttu-id="4309e-289">/app1/ifd/exif/PaddingSchema : remplissage</span><span class="sxs-lookup"><span data-stu-id="4309e-289">/app1/ifd/exif/PaddingSchema:Padding</span></span> | <span data-ttu-id="4309e-290">/ifd/exif/PaddingSchema : remplissage</span><span class="sxs-lookup"><span data-stu-id="4309e-290">/ifd/exif/PaddingSchema:Padding</span></span> |
| <span data-ttu-id="4309e-291">XMP</span><span class="sxs-lookup"><span data-stu-id="4309e-291">XMP</span></span>             | <span data-ttu-id="4309e-292">/xmp/PaddingSchema : remplissage</span><span class="sxs-lookup"><span data-stu-id="4309e-292">/xmp/PaddingSchema:Padding</span></span>           | <span data-ttu-id="4309e-293">/ifd/xmp/PaddingSchema : remplissage</span><span class="sxs-lookup"><span data-stu-id="4309e-293">/ifd/xmp/PaddingSchema:Padding</span></span>  |
| <span data-ttu-id="4309e-294">GPS</span><span class="sxs-lookup"><span data-stu-id="4309e-294">GPS</span></span>             | <span data-ttu-id="4309e-295">/app1/ifd/gps/PaddingSchema : remplissage</span><span class="sxs-lookup"><span data-stu-id="4309e-295">/app1/ifd/gps/PaddingSchema:Padding</span></span>  | <span data-ttu-id="4309e-296">/ifd/gps/PaddingSchema : remplissage</span><span class="sxs-lookup"><span data-stu-id="4309e-296">/ifd/gps/PaddingSchema:Padding</span></span>  |



 

### <a name="obtaining-a-fast-metadata-encoder"></a><span data-ttu-id="4309e-297">Obtention d’un encodeur de métadonnées rapide</span><span class="sxs-lookup"><span data-stu-id="4309e-297">Obtaining a Fast Metadata Encoder</span></span>

<span data-ttu-id="4309e-298">Lorsque vous disposez d’une image avec remplissage des métadonnées, un encodeur de métadonnées rapide peut être obtenu à l’aide des méthodes de fabrique d’images **CreateFastMetadataEncoderFromDecoder** et **CreateFastMetadataEncoderFromFrameDecode**.</span><span class="sxs-lookup"><span data-stu-id="4309e-298">When you have an image with metadata padding, a fast metadata encoder can be obtained by using the imaging factory methods **CreateFastMetadataEncoderFromDecoder** and **CreateFastMetadataEncoderFromFrameDecode**.</span></span>

<span data-ttu-id="4309e-299">Comme son nom l’indique, **CreateFastMetadataEncoderFromDecoder** crée un encodeur de métadonnées rapide pour les métadonnées au niveau du décodeur.</span><span class="sxs-lookup"><span data-stu-id="4309e-299">As the name implies, **CreateFastMetadataEncoderFromDecoder** creates a fast metadata encoder for decoder-level metadata.</span></span> <span data-ttu-id="4309e-300">Les formats d’images natifs fournis par WIC ne prennent pas en charge les métadonnées au niveau du décodeur, mais cette méthode est fournie au cas où un tel format d’image serait développé à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="4309e-300">The native image formats provided by WIC do not support decoder-level metadata but this method is provided in case such an image format is developed in the future.</span></span>

<span data-ttu-id="4309e-301">Le scénario le plus courant consiste à obtenir un encodeur de métadonnées rapide à partir d’une image à l’aide de **CreateFastMetadataEncoderFromFrameDecode**.</span><span class="sxs-lookup"><span data-stu-id="4309e-301">The more common scenario is to obtain a fast metadata encoder from an image frame by using **CreateFastMetadataEncoderFromFrameDecode**.</span></span> <span data-ttu-id="4309e-302">Le code suivant obtient l’encodeur des métadonnées rapides d’un frame décodé et modifie la valeur d’évaluation dans le bloc App1.</span><span class="sxs-lookup"><span data-stu-id="4309e-302">The following code obtains a decoded frame's fast metadata encoder and changes the rating value in the App1 block.</span></span>


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



### <a name="using-the-fast-metadata-encoder"></a><span data-ttu-id="4309e-303">Utilisation de l’encodeur de métadonnées rapide</span><span class="sxs-lookup"><span data-stu-id="4309e-303">Using the Fast Metadata Encoder</span></span>

<span data-ttu-id="4309e-304">À partir de l’encodeur de métadonnées rapide, vous pouvez obtenir un générateur de requêtes.</span><span class="sxs-lookup"><span data-stu-id="4309e-304">From the fast metadata encoder, you can obtain a query writer.</span></span> <span data-ttu-id="4309e-305">Cela vous permet d’écrire des métadonnées à l’aide d’une expression de requête comme indiqué précédemment.</span><span class="sxs-lookup"><span data-stu-id="4309e-305">This enables you to write metadata by using a query expression as previously demonstrated.</span></span> <span data-ttu-id="4309e-306">Une fois les métadonnées définies dans le générateur de requêtes, validez l’encodeur de métadonnées rapide pour finaliser la mise à jour des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="4309e-306">After metadata has been set in the query writer, commit the fast metadata encoder to finalize the metadata update.</span></span> <span data-ttu-id="4309e-307">Le code suivant illustre la définition et la validation des modifications de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="4309e-307">The following code demonstrates setting and committing the metadata changes</span></span>


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



<span data-ttu-id="4309e-308">Si la **validation** échoue pour une raison quelconque, vous devrez recoder l’image pour vous assurer que les nouvelles métadonnées sont ajoutées à l’image.</span><span class="sxs-lookup"><span data-stu-id="4309e-308">If **Commit** fails for any reason, you will need to re-encode the image to ensure the new metadata is added to the image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4309e-309">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4309e-309">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4309e-310">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="4309e-310">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4309e-311">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="4309e-311">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="4309e-312">Vue d’ensemble des métadonnées WIC</span><span class="sxs-lookup"><span data-stu-id="4309e-312">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="4309e-313">Vue d’ensemble du langage de requête de métadonnées</span><span class="sxs-lookup"><span data-stu-id="4309e-313">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="4309e-314">Vue d’ensemble de l’extensibilité des métadonnées</span><span class="sxs-lookup"><span data-stu-id="4309e-314">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)
</dt> <dt>

[<span data-ttu-id="4309e-315">Comment : recoder une image JPEG avec des métadonnées</span><span class="sxs-lookup"><span data-stu-id="4309e-315">How-to: Re-encode a JPEG Image with Metadata</span></span>](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 
