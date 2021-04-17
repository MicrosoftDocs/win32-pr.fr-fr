---
description: Cette rubrique présente la prise en charge des métadonnées de création d’images fournie par le WIC (Windows Imaging Component).
ms.assetid: 35727810-3c4c-4c11-a4a2-3ae2cf3b8142
title: Vue d’ensemble des métadonnées WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f00e3a77eb74a3fb4a00db05ef9e00028f02ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556412"
---
# <a name="wic-metadata-overview"></a><span data-ttu-id="3ed35-103">Vue d’ensemble des métadonnées WIC</span><span class="sxs-lookup"><span data-stu-id="3ed35-103">WIC Metadata Overview</span></span>

<span data-ttu-id="3ed35-104">Cette rubrique présente la prise en charge des métadonnées de création d’images fournie par le WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="3ed35-104">This topic introduces the imaging metadata support provided by the Windows Imaging Component (WIC).</span></span> <span data-ttu-id="3ed35-105">Il fournit une présentation de la lecture et de l’écriture des métadonnées d’image, du langage de requête de métadonnées et de l’extensibilité du gestionnaire de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3ed35-105">It provides an introduction to reading and writing image metadata, the metadata query language, and metadata handler extensibility.</span></span>

<span data-ttu-id="3ed35-106">Les métadonnées d’image sont des données incorporées dans un fichier image qui fournit des informations supplémentaires sur l’image, telles que l’appareil utilisé pour capturer l’image ou les dimensions de l’image.</span><span class="sxs-lookup"><span data-stu-id="3ed35-106">Image metadata is data embedded inside an image file that provides additional information about the image, such as the device used to capture the image or the dimensions of the image.</span></span> <span data-ttu-id="3ed35-107">Bien qu’elle soit contenue dans le fichier image lui-même, ces métadonnées ne font pas partie des données de rendu.</span><span class="sxs-lookup"><span data-stu-id="3ed35-107">Although it is contained within the image file itself, this metadata is not part of the rendering data.</span></span> <span data-ttu-id="3ed35-108">WIC fournit des interfaces qui vous permettent de lire et d’écrire ces métadonnées pour plusieurs formats de métadonnées courants, notamment les formats de métadonnées XMP (Extensible Metadata Platform), EXIF (échanged image file) et png (texte).</span><span class="sxs-lookup"><span data-stu-id="3ed35-108">WIC provides interfaces that enable you to read and write this metadata for several common metadata formats including Extensible Metadata Platform (XMP), Exchangeable Image File (EXIF), and Png Textual Data (tEXt).</span></span>

<span data-ttu-id="3ed35-109">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="3ed35-109">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3ed35-110">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="3ed35-110">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="3ed35-111">Introduction</span><span class="sxs-lookup"><span data-stu-id="3ed35-111">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="3ed35-112">Lecture des métadonnées de l’image</span><span class="sxs-lookup"><span data-stu-id="3ed35-112">Reading Image Metadata</span></span>](#reading-image-metadata)
-   [<span data-ttu-id="3ed35-113">Écriture de métadonnées d’image</span><span class="sxs-lookup"><span data-stu-id="3ed35-113">Writing Image Metadata</span></span>](#writing-image-metadata)
-   [<span data-ttu-id="3ed35-114">Extensibilité des métadonnées</span><span class="sxs-lookup"><span data-stu-id="3ed35-114">Metadata Extensibility</span></span>](#metadata-extensibility)
-   [<span data-ttu-id="3ed35-115">Formats de métadonnées pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ed35-115">Supported Metadata Formats</span></span>](#supported-metadata-formats)
-   [<span data-ttu-id="3ed35-116">Résumé du composant de métadonnées</span><span class="sxs-lookup"><span data-stu-id="3ed35-116">Metadata Component Summary</span></span>](#metadata-component-summary)
-   [<span data-ttu-id="3ed35-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3ed35-117">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="3ed35-118">Prérequis</span><span class="sxs-lookup"><span data-stu-id="3ed35-118">Prerequisites</span></span>

<span data-ttu-id="3ed35-119">Pour comprendre cette rubrique, vous devez être familiarisé avec l’encodeur et les interfaces de décodeur WIC et leurs composants COM (Component Object Model) associés, comme décrit dans [vue d’ensemble du composant de création d’images Windows](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="3ed35-119">To understand this topic, you should be familiar with the WIC encoder and decoder interfaces and their related Component Object Model (COM) components, as described in the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span> <span data-ttu-id="3ed35-120">Il permet également d’avoir une connaissance générale de certains des formats de métadonnées de création d’images actuellement utilisés.</span><span class="sxs-lookup"><span data-stu-id="3ed35-120">It also helps to have a general familiarity with some of the imaging metadata formats in use today.</span></span>

## <a name="introduction"></a><span data-ttu-id="3ed35-121">Introduction</span><span class="sxs-lookup"><span data-stu-id="3ed35-121">Introduction</span></span>

<span data-ttu-id="3ed35-122">Les métadonnées fournissent des informations étendues sur une image.</span><span class="sxs-lookup"><span data-stu-id="3ed35-122">Metadata provides extended information about an image.</span></span> <span data-ttu-id="3ed35-123">Ces informations peuvent être utilisées de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="3ed35-123">This information can be used in several ways.</span></span> <span data-ttu-id="3ed35-124">Une image peut contenir des métadonnées telles qu’une description, une évaluation, des balises de catégorie et des informations de copyright.</span><span class="sxs-lookup"><span data-stu-id="3ed35-124">An image might contain metadata such as a description, rating, category tags, and copyright information.</span></span> <span data-ttu-id="3ed35-125">L’accès aux métadonnées facilite l’exécution de tâches telles que la gestion des ressources, l’emplacement des fichiers ou la détermination des informations de copyright.</span><span class="sxs-lookup"><span data-stu-id="3ed35-125">Accessing the metadata makes it easier to perform tasks such as asset management, file location, or determining copyright information.</span></span> <span data-ttu-id="3ed35-126">Par exemple, la Galerie de photos Windows dans Windows Vista vous permet d’ajouter des descriptions et des balises de catégorie aux images.</span><span class="sxs-lookup"><span data-stu-id="3ed35-126">For example, the Windows Photo Gallery in Windows Vista enables you to add descriptions and category tags to images.</span></span> <span data-ttu-id="3ed35-127">Cela permet une meilleure détectabilité des images et un moyen pratique de classer les images.</span><span class="sxs-lookup"><span data-stu-id="3ed35-127">This allows for better discoverability of images and a convenient way to categorize images.</span></span> <span data-ttu-id="3ed35-128">À l’aide des API WIC et des formats de métadonnées courants, les applications peuvent facilement écrire ou lire ce type de métadonnées vers ou à partir d’images.</span><span class="sxs-lookup"><span data-stu-id="3ed35-128">Using the WIC APIs and common metadata formats, applications can easily write or read this type of metadata to or from images.</span></span>

<span data-ttu-id="3ed35-129">Le diagramme suivant illustre le contenu d’un fichier JPEG qui comprend des blocs de métadonnées incorporés et des éléments de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3ed35-129">The following diagram illustrates the contents of a JPEG file that includes embedded metadata blocks and metadata items.</span></span>

![image JPEG avec les métadonnées d’évaluation](graphics/jpeg.png)

<span data-ttu-id="3ed35-131">Dans cet exemple d’image, les métadonnées sont incorporées dans le fichier image au sein d’une image.</span><span class="sxs-lookup"><span data-stu-id="3ed35-131">In this example image, the metadata is embedded in the image file within an image frame.</span></span> <span data-ttu-id="3ed35-132">Le format JPEG ne prenant pas en charge plusieurs trames d’image, les métadonnées sont attachées de manière conceptuelle à ce frame unique.</span><span class="sxs-lookup"><span data-stu-id="3ed35-132">The JPEG format does not support multiple image frames, so the metadata is conceptually attached to this single frame.</span></span> <span data-ttu-id="3ed35-133">Les formats qui prennent en charge plusieurs frames, tels que TIFF, peuvent avoir des métadonnées attachées à chaque frame d’image comme le montre ce diagramme.</span><span class="sxs-lookup"><span data-stu-id="3ed35-133">Formats that support multiple frames, such as TIFF, may have metadata attached to each image frame as this diagram shows.</span></span> <span data-ttu-id="3ed35-134">Bien qu’il ne soit pas courant aujourd’hui ni pris en charge par les codecs d’image native, certains formats d’image peuvent également prendre en charge les métadonnées en dehors d’une image.</span><span class="sxs-lookup"><span data-stu-id="3ed35-134">Though not common today and not supported by the native image codecs, some image formats may also support metadata outside of an image frame.</span></span> <span data-ttu-id="3ed35-135">WIC est suffisamment flexible pour gérer les métadonnées de niveau image et les métadonnées en dehors du frame individuel d’une image.</span><span class="sxs-lookup"><span data-stu-id="3ed35-135">WIC is flexible enough to handle both frame-level metadata and metadata outside of an image's individual frame.</span></span>

## <a name="reading-image-metadata"></a><span data-ttu-id="3ed35-136">Lecture des métadonnées de l’image</span><span class="sxs-lookup"><span data-stu-id="3ed35-136">Reading Image Metadata</span></span>

<span data-ttu-id="3ed35-137">Les API WIC fournissent des composants COM qui permettent aux applications de lire et d’écrire facilement des métadonnées d’image.</span><span class="sxs-lookup"><span data-stu-id="3ed35-137">The WIC APIs provide COM components that make it easy for applications to read and write image metadata.</span></span>

<span data-ttu-id="3ed35-138">Le principal moyen de lire les métadonnées consiste à utiliser un lecteur de requêtes de métadonnées ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) pour accéder à des éléments de métadonnées spécifiques.</span><span class="sxs-lookup"><span data-stu-id="3ed35-138">The primary way to read metadata is to use a metadata query reader ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) to access specific metadata items.</span></span> <span data-ttu-id="3ed35-139">Le composant lecteur de requêtes de métadonnées est implémenté par le codec et est accessible au niveau du décodeur ou via des trames d’image individuelles, qui est la méthode la plus courante.</span><span class="sxs-lookup"><span data-stu-id="3ed35-139">The metadata query reader component is implemented by the codec and can be accessed at the decoder level or through individual image frames, which is the more common method.</span></span> <span data-ttu-id="3ed35-140">Le code suivant montre comment accéder à un lecteur de requêtes pour un frame individuel à l’aide de la méthode **GetMetadataQueryReader** du lecteur de requête.</span><span class="sxs-lookup"><span data-stu-id="3ed35-140">The following code demonstrates how to access a query reader for an individual frame by using the query reader's **GetMetadataQueryReader** method.</span></span>


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



<span data-ttu-id="3ed35-141">Un lecteur de requête fournit des méthodes pour obtenir des informations sur des métadonnées spécifiques et un moyen de spécifier un élément de métadonnées à récupérer.</span><span class="sxs-lookup"><span data-stu-id="3ed35-141">A query reader provides methods to obtain information about specific metadata, and a means to specify a metadata item to retrieve.</span></span> <span data-ttu-id="3ed35-142">Le code suivant utilise une expression de requête pour demander un élément de métadonnées spécifique dans le bloc répertoire du fichier d’image imbriquée App1 (IFD).</span><span class="sxs-lookup"><span data-stu-id="3ed35-142">The following code uses a query expression to request a specific metadata item within the App1 nested image file directory (IFD) block.</span></span> <span data-ttu-id="3ed35-143">Pour ce faire, utilisez la méthode **GetMetadataByName** du lecteur de requête.</span><span class="sxs-lookup"><span data-stu-id="3ed35-143">This is done by using the query reader's **GetMetadataByName** method.</span></span> <span data-ttu-id="3ed35-144">Le code suivant illustre l’utilisation du lecteur de requête pour obtenir la valeur d’évaluation MicrosoftPhoto.</span><span class="sxs-lookup"><span data-stu-id="3ed35-144">The following code demonstrates using the query reader to obtain the MicrosoftPhoto rating value.</span></span>


```
PROPVARIANT value;
PropVariantInit(&value);

LPCWSTR pwzRatingQuery = L"/app1/ifd/{ushort=18249}";

if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(pwzRatingQuery, &value);
}
```



<span data-ttu-id="3ed35-145">La variable pwzRatingQuery dans l’exemple précédent est la chaîne de requête pour accéder à l’évaluation de MicrosoftPhoto de l’élément de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3ed35-145">The pwzRatingQuery variable in the preceding example is the query string to access the metadata item MicrosoftPhoto rating.</span></span> <span data-ttu-id="3ed35-146">Cette chaîne est créée à l’aide du langage de requête de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3ed35-146">This string is created by using the metadata query language.</span></span> <span data-ttu-id="3ed35-147">Pour créer cette chaîne, il est nécessaire de connaître le format des métadonnées et le langage de requête des métadonnées pour récupérer des éléments de métadonnées individuels.</span><span class="sxs-lookup"><span data-stu-id="3ed35-147">To create this string, knowledge of the metadata format and the metadata query language is needed to retrieve individual metadata items.</span></span> <span data-ttu-id="3ed35-148">Pour plus d’informations sur le langage de requête de métadonnées, consultez la [vue d’ensemble du langage de requête de métadonnées](-wic-codec-metadataquerylanguage.md).</span><span class="sxs-lookup"><span data-stu-id="3ed35-148">For more information about the metadata query language, see the [Metadata Query Language Overview](-wic-codec-metadataquerylanguage.md).</span></span>

<span data-ttu-id="3ed35-149">En arrière-plan, un lecteur de requête utilise un lecteur de métadonnées ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) pour accéder aux métadonnées décrites par l’expression de requête.</span><span class="sxs-lookup"><span data-stu-id="3ed35-149">Behind the scenes, a query reader uses a metadata reader ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) to access the metadata described by the query expression.</span></span> <span data-ttu-id="3ed35-150">En plus d’utiliser un lecteur de requêtes, vous pouvez également accéder directement à un lecteur de métadonnées pour lire les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3ed35-150">In addition to using a query reader, you can also access a metadata reader directly to read metadata.</span></span> <span data-ttu-id="3ed35-151">Vous pouvez obtenir un lecteur de métadonnées à partir du décodeur ou des frames individuels en interrogeant une interface de lecteur de bloc ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)).</span><span class="sxs-lookup"><span data-stu-id="3ed35-151">You can obtain a metadata reader from the decoder or individual frames by querying for a block reader ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) interface.</span></span>

## <a name="writing-image-metadata"></a><span data-ttu-id="3ed35-152">Écriture de métadonnées d’image</span><span class="sxs-lookup"><span data-stu-id="3ed35-152">Writing Image Metadata</span></span>

<span data-ttu-id="3ed35-153">Le processus d’écriture des métadonnées est similaire à la façon dont il est lu, sauf qu’un enregistreur de requêtes de métadonnées ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="3ed35-153">The process of writing metadata is similar to the way it is read except that a metadata query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) is used.</span></span> <span data-ttu-id="3ed35-154">L’interface du writer de requête est implémentée par l’encodeur d’image et, comme dans le lecteur de requête, les métadonnées sont accessibles à la fois sur l’encodeur et sur des frames individuels (en fonction de la prise en charge du format d’image).</span><span class="sxs-lookup"><span data-stu-id="3ed35-154">The query writer interface is implemented by the image encoder and, as in the query reader, metadata is accessed both on the encoder and on individual frames (depending on image format support).</span></span>

<span data-ttu-id="3ed35-155">Le code suivant montre comment obtenir un enregistreur de requête à partir d’un frame d’encodeur et supprimer la valeur d’évaluation précédemment lue.</span><span class="sxs-lookup"><span data-stu-id="3ed35-155">The following code demonstrates how to obtain a query writer from an encoder frame and remove the rating value that was previously read.</span></span>


```
// Get the frame's query writer
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/app1/ifd/{ushort=18249}");
}
```



<span data-ttu-id="3ed35-156">Une autre façon d’écrire des métadonnées consiste à utiliser des mises à jour de métadonnées rapides.</span><span class="sxs-lookup"><span data-stu-id="3ed35-156">Another way to write metadata is through fast metadata updates.</span></span> <span data-ttu-id="3ed35-157">L’encodage de métadonnées rapide est un moyen d’écrire des métadonnées d’image sans avoir à recoder un fichier image.</span><span class="sxs-lookup"><span data-stu-id="3ed35-157">Fast metadata encoding is a way to write image metadata without having to re-encode an image file.</span></span> <span data-ttu-id="3ed35-158">Cela s’effectue en écrivant de nouvelles métadonnées dans une zone rembourrée du format de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3ed35-158">This is done by writing new metadata information to a padded region of the metadata format.</span></span> <span data-ttu-id="3ed35-159">L’encodeur de métadonnées rapide ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) est obtenu à partir de la fabrique de composants, en fonction du décodeur d’image.</span><span class="sxs-lookup"><span data-stu-id="3ed35-159">The fast metadata encoder ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) is obtained from the component factory, based on the image decoder.</span></span> <span data-ttu-id="3ed35-160">L’encodeur de métadonnées rapide obtient alors un générateur de requêtes qui est utilisé pour écrire les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3ed35-160">The fast metadata encoder then obtains a query writer that is used to write the metadata.</span></span> <span data-ttu-id="3ed35-161">Enfin, l’encodeur rapide valide la modification.</span><span class="sxs-lookup"><span data-stu-id="3ed35-161">Finally, the fast encoder commits the change.</span></span>

<span data-ttu-id="3ed35-162">Le code suivant montre comment obtenir un encodeur de métadonnées rapide et l’utiliser pour écrire la valeur MicrosoftRating.</span><span class="sxs-lookup"><span data-stu-id="3ed35-162">The following code demonstrates how to obtain a fast metadata encoder and use it to write the MicrosoftRating value.</span></span>


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode,
        &pFME);

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



<span data-ttu-id="3ed35-163">Tous les formats de métadonnées ne prennent pas en charge les métadonnées rapides.</span><span class="sxs-lookup"><span data-stu-id="3ed35-163">Not all metadata formats support fast metadata.</span></span> <span data-ttu-id="3ed35-164">Pour savoir quels formats pris en charge en mode natif prennent en charge l’encodage de métadonnées rapide, consultez le tableau dans la section [formats de métadonnées pris en charge](#supported-metadata-formats) plus loin dans ce document.</span><span class="sxs-lookup"><span data-stu-id="3ed35-164">To see which natively supported formats support fast metadata encoding, see the table in the [Supported Metadata Formats](#supported-metadata-formats) section later in this document.</span></span>

<span data-ttu-id="3ed35-165">En arrière-plan, un writer de requête utilise un enregistreur de métadonnées ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) pour écrire les métadonnées décrites par l’expression de requête.</span><span class="sxs-lookup"><span data-stu-id="3ed35-165">Behind the scenes, a query writer uses a metadata writer ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) to write the metadata described by the query expression.</span></span> <span data-ttu-id="3ed35-166">En plus d’utiliser un lecteur de requêtes, vous pouvez également accéder directement à un enregistreur de métadonnées pour écrire des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3ed35-166">In addition to using a query reader, you can also access a metadata writer directly to write metadata.</span></span> <span data-ttu-id="3ed35-167">Vous pouvez obtenir un générateur de métadonnées à partir du décodeur ou des frames individuels à l’aide de l’interrogation d’une interface de writer de bloc ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)).</span><span class="sxs-lookup"><span data-stu-id="3ed35-167">You can obtain a metadata writer from the decoder or individual frames using querying for a block writer ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)) interface.</span></span>

## <a name="metadata-extensibility"></a><span data-ttu-id="3ed35-168">Extensibilité des métadonnées</span><span class="sxs-lookup"><span data-stu-id="3ed35-168">Metadata Extensibility</span></span>

<span data-ttu-id="3ed35-169">Comme mentionné précédemment, WIC fournit plusieurs gestionnaires de métadonnées pour lire et écrire des métadonnées pour les formats de métadonnées courants.</span><span class="sxs-lookup"><span data-stu-id="3ed35-169">As mentioned previously, WIC provides several metadata handlers to read and write metadata for common metadata formats.</span></span> <span data-ttu-id="3ed35-170">Toutefois, certains formats de métadonnées ne sont pas pris en charge en mode natif.</span><span class="sxs-lookup"><span data-stu-id="3ed35-170">However, there are some metadata formats that are not natively supported.</span></span> <span data-ttu-id="3ed35-171">Par conséquent, WIC fournit des API pour créer des gestionnaires de métadonnées supplémentaires qui peuvent étendre la prise en charge des métadonnées à d’autres formats.</span><span class="sxs-lookup"><span data-stu-id="3ed35-171">Therefore, WIC provides APIs for creating additional metadata handlers that can extend metadata support to other formats.</span></span>

<span data-ttu-id="3ed35-172">Pour prendre entièrement en charge d’autres formats de métadonnées, deux types de gestionnaires doivent être développés : un lecteur de métadonnées pour lire les métadonnées et un générateur de métadonnées pour écrire des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3ed35-172">To fully support other metadata formats, two types of handlers must be developed — a metadata reader to read metadata and a metadata writer to write metadata.</span></span> <span data-ttu-id="3ed35-173">Bien que ces deux gestionnaires soient généralement implémentés par paires pour un format spécifique, ce n’est pas une exigence.</span><span class="sxs-lookup"><span data-stu-id="3ed35-173">Although these two handlers are usually implemented in pairs for a specific format, that is not a requirement.</span></span> <span data-ttu-id="3ed35-174">Dans certains cas, seule la capacité de lecture ou uniquement la capacité d’écriture est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3ed35-174">There might be some cases in which only the read ability or only the write ability is needed.</span></span>

<span data-ttu-id="3ed35-175">Pour plus d’informations sur l’extensibilité des métadonnées à l’aide des API WIC, consultez [vue d’ensemble de l’extensibilité des métadonnées](-wic-codec-metadatahandlers.md).</span><span class="sxs-lookup"><span data-stu-id="3ed35-175">For more information on metadata extensibility using the WIC APIs, see the [Metadata Extensibility Overview](-wic-codec-metadatahandlers.md).</span></span>

## <a name="supported-metadata-formats"></a><span data-ttu-id="3ed35-176">Formats de métadonnées pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ed35-176">Supported Metadata Formats</span></span>

<span data-ttu-id="3ed35-177">WIC prend en charge plusieurs formats de métadonnées courants.</span><span class="sxs-lookup"><span data-stu-id="3ed35-177">WIC provides support for several common metadata formats.</span></span> <span data-ttu-id="3ed35-178">Le tableau suivant répertorie les formats de métadonnées pris en charge, leurs versions, les formats d’image qui prennent en charge le format de métadonnées, et indique si le format de métadonnées prend en charge l’encodage de métadonnées rapide.</span><span class="sxs-lookup"><span data-stu-id="3ed35-178">The following table lists the supported metadata formats, their versions, the image formats that support the metadata format, and whether the metadata format supports fast metadata encoding.</span></span> <span data-ttu-id="3ed35-179">Pour plus d’informations sur l’encodage des métadonnées rapide, consultez la section [écriture de métadonnées d’image](#writing-image-metadata) plus haut dans ce document.</span><span class="sxs-lookup"><span data-stu-id="3ed35-179">For more information about fast metadata encoding, see the [Writing Image Metadata](#writing-image-metadata) section earlier in this document.</span></span>



| <span data-ttu-id="3ed35-180">Formats de métadonnées pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ed35-180">Supported metadata formats</span></span> | <span data-ttu-id="3ed35-181">Version de la spécification de métadonnées</span><span class="sxs-lookup"><span data-stu-id="3ed35-181">Metadata specification version</span></span> | <span data-ttu-id="3ed35-182">Prise en charge du format d’image</span><span class="sxs-lookup"><span data-stu-id="3ed35-182">Image format support</span></span> | <span data-ttu-id="3ed35-183">Prend en charge l’encodage de métadonnées rapide</span><span class="sxs-lookup"><span data-stu-id="3ed35-183">Supports fast metadata encoding</span></span> |
|----------------------------|--------------------------------|----------------------|---------------------------------|
| <span data-ttu-id="3ed35-184">App0</span><span class="sxs-lookup"><span data-stu-id="3ed35-184">App0</span></span>                       | <span data-ttu-id="3ed35-185">JFIF 1,02</span><span class="sxs-lookup"><span data-stu-id="3ed35-185">JFIF 1.02</span></span>                      | <span data-ttu-id="3ed35-186">JPEG</span><span class="sxs-lookup"><span data-stu-id="3ed35-186">JPEG</span></span>                 | <span data-ttu-id="3ed35-187">Non</span><span class="sxs-lookup"><span data-stu-id="3ed35-187">No</span></span>                              |
| <span data-ttu-id="3ed35-188">App1</span><span class="sxs-lookup"><span data-stu-id="3ed35-188">App1</span></span>                       | <span data-ttu-id="3ed35-189">JFIF 1,02</span><span class="sxs-lookup"><span data-stu-id="3ed35-189">JFIF 1.02</span></span>                      | <span data-ttu-id="3ed35-190">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="3ed35-190">JPEG, TIFF</span></span>           | <span data-ttu-id="3ed35-191">Non</span><span class="sxs-lookup"><span data-stu-id="3ed35-191">No</span></span>                              |
| <span data-ttu-id="3ed35-192">App13</span><span class="sxs-lookup"><span data-stu-id="3ed35-192">App13</span></span>                      | <span data-ttu-id="3ed35-193">Unknown</span><span class="sxs-lookup"><span data-stu-id="3ed35-193">Unknown</span></span>                        | <span data-ttu-id="3ed35-194">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="3ed35-194">JPEG, TIFF</span></span>           | <span data-ttu-id="3ed35-195">Non</span><span class="sxs-lookup"><span data-stu-id="3ed35-195">No</span></span>                              |
| <span data-ttu-id="3ed35-196">IFD</span><span class="sxs-lookup"><span data-stu-id="3ed35-196">IFD</span></span>                        | <span data-ttu-id="3ed35-197">TIFF 6,0</span><span class="sxs-lookup"><span data-stu-id="3ed35-197">TIFF 6.0</span></span>                       | <span data-ttu-id="3ed35-198">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="3ed35-198">JPEG, TIFF</span></span>           | <span data-ttu-id="3ed35-199">Oui</span><span class="sxs-lookup"><span data-stu-id="3ed35-199">Yes</span></span>                             |
| <span data-ttu-id="3ed35-200">IRB</span><span class="sxs-lookup"><span data-stu-id="3ed35-200">IRB</span></span>                        | <span data-ttu-id="3ed35-201">Unknown</span><span class="sxs-lookup"><span data-stu-id="3ed35-201">Unknown</span></span>                        | <span data-ttu-id="3ed35-202">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="3ed35-202">JPEG, TIFF</span></span>           | <span data-ttu-id="3ed35-203">Non</span><span class="sxs-lookup"><span data-stu-id="3ed35-203">No</span></span>                              |
| <span data-ttu-id="3ed35-204">Exif</span><span class="sxs-lookup"><span data-stu-id="3ed35-204">Exif</span></span>                       | <span data-ttu-id="3ed35-205">EXIF 2,2</span><span class="sxs-lookup"><span data-stu-id="3ed35-205">Exif 2.2</span></span>                       | <span data-ttu-id="3ed35-206">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="3ed35-206">JPEG, TIFF</span></span>           | <span data-ttu-id="3ed35-207">Oui</span><span class="sxs-lookup"><span data-stu-id="3ed35-207">Yes</span></span>                             |
| <span data-ttu-id="3ed35-208">XMP</span><span class="sxs-lookup"><span data-stu-id="3ed35-208">XMP</span></span>                        | <span data-ttu-id="3ed35-209">XMP 1,0 (septembre 2005)</span><span class="sxs-lookup"><span data-stu-id="3ed35-209">XMP 1.0 (Sept 2005)</span></span>            | <span data-ttu-id="3ed35-210">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="3ed35-210">JPEG, TIFF</span></span>           | <span data-ttu-id="3ed35-211">Oui</span><span class="sxs-lookup"><span data-stu-id="3ed35-211">Yes</span></span>                             |
| <span data-ttu-id="3ed35-212">GPS</span><span class="sxs-lookup"><span data-stu-id="3ed35-212">GPS</span></span>                        | <span data-ttu-id="3ed35-213">EXIF 2,2</span><span class="sxs-lookup"><span data-stu-id="3ed35-213">Exif 2.2</span></span>                       | <span data-ttu-id="3ed35-214">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="3ed35-214">JPEG, TIFF</span></span>           | <span data-ttu-id="3ed35-215">Oui</span><span class="sxs-lookup"><span data-stu-id="3ed35-215">Yes</span></span>                             |
| <span data-ttu-id="3ed35-216">IPTC</span><span class="sxs-lookup"><span data-stu-id="3ed35-216">IPTC</span></span>                       | <span data-ttu-id="3ed35-217">IPTC 4,0</span><span class="sxs-lookup"><span data-stu-id="3ed35-217">IPTC 4.0</span></span>                       | <span data-ttu-id="3ed35-218">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="3ed35-218">JPEG, TIFF</span></span>           | <span data-ttu-id="3ed35-219">Oui</span><span class="sxs-lookup"><span data-stu-id="3ed35-219">Yes</span></span>                             |
| <span data-ttu-id="3ed35-220">Financière</span><span class="sxs-lookup"><span data-stu-id="3ed35-220">tEXt</span></span>                       | <span data-ttu-id="3ed35-221">PNG 1,2</span><span class="sxs-lookup"><span data-stu-id="3ed35-221">PNG 1.2</span></span>                        | <span data-ttu-id="3ed35-222">PNG</span><span class="sxs-lookup"><span data-stu-id="3ed35-222">PNG</span></span>                  | <span data-ttu-id="3ed35-223">Non</span><span class="sxs-lookup"><span data-stu-id="3ed35-223">No</span></span>                              |



 

> [!Note]  
> <span data-ttu-id="3ed35-224">IPTC prend en charge uniquement FME si la taille des blocs augmente, car IPTC ne prend pas en charge le remplissage.</span><span class="sxs-lookup"><span data-stu-id="3ed35-224">IPTC only supports FME if the blocks grow in size, as IPTC does not support padding.</span></span>

 

## <a name="metadata-component-summary"></a><span data-ttu-id="3ed35-225">Résumé du composant de métadonnées</span><span class="sxs-lookup"><span data-stu-id="3ed35-225">Metadata Component Summary</span></span>

<span data-ttu-id="3ed35-226">Le tableau suivant décrit les interfaces WIC qui prennent en charge les métadonnées et leurs composants correspondants.</span><span class="sxs-lookup"><span data-stu-id="3ed35-226">The following table describes the WIC interfaces that support metadata, and their corresponding components.</span></span> <span data-ttu-id="3ed35-227">Ces composants fournissent l’accès aux métadonnées d’une image.</span><span class="sxs-lookup"><span data-stu-id="3ed35-227">These components provide the access to an image's metadata.</span></span> <span data-ttu-id="3ed35-228">Pour plus d’informations sur ces composants, consultez [vue d’ensemble du composant de création d’images Windows](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="3ed35-228">For more information about these components, see the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3ed35-229">Composant</span><span class="sxs-lookup"><span data-stu-id="3ed35-229">Component</span></span></th>
<th><span data-ttu-id="3ed35-230">Description</span><span class="sxs-lookup"><span data-stu-id="3ed35-230">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ed35-231">Décodeur bitmap (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="3ed35-231">Bitmap Decoder (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="3ed35-232">Lit un flux d’image et produit une source bitmap utilisable.</span><span class="sxs-lookup"><span data-stu-id="3ed35-232">Reads an image stream and produces a usable bitmap source.</span></span> <span data-ttu-id="3ed35-233">Associé à un format de conteneur tel que TIFF (Tagged Image File Format) ou JPEG (Joint Photographic Experts Group).</span><span class="sxs-lookup"><span data-stu-id="3ed35-233">Associated with a container format such as Tagged Image File Format (TIFF) or Joint Photographic Experts Group (JPEG).</span></span></li>
<li><span data-ttu-id="3ed35-234">Implémente une interface <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> pour énumérer tous les blocs de métadonnées dans le flux de données du décodeur qui ne se trouvent pas à l’intérieur d’un frame.</span><span class="sxs-lookup"><span data-stu-id="3ed35-234">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> interface to enumerate all of the metadata blocks in the decoder's data stream that are not inside a frame.</span></span></li>
<li><span data-ttu-id="3ed35-235">Expose un lecteur de requêtes pour lire les métadonnées associées à l’image qui ne se trouve pas à l’intérieur d’un frame.</span><span class="sxs-lookup"><span data-stu-id="3ed35-235">Exposes a query reader to read the metadata associated with the image that is not inside a frame.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ed35-236">Décodage de cadre bitmap (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="3ed35-236">Bitmap Frame Decode (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="3ed35-237">Accède à des frames individuels à partir du flux d’images détenu par le décodeur.</span><span class="sxs-lookup"><span data-stu-id="3ed35-237">Accesses individual frames from the image stream held by the decoder.</span></span></li>
<li><span data-ttu-id="3ed35-238">Implémente une interface <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> pour énumérer tous les blocs de métadonnées dans le flux de données du frame.</span><span class="sxs-lookup"><span data-stu-id="3ed35-238">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> interface to enumerate all of the metadata blocks in the frame's data stream.</span></span></li>
<li><span data-ttu-id="3ed35-239">Expose un lecteur de requêtes pour lire les métadonnées associées au frame, à l’aide d’expressions de requête.</span><span class="sxs-lookup"><span data-stu-id="3ed35-239">Exposes a query reader to read the metadata associated with the frame, using query expressions.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ed35-240">Encodeur bitmap (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="3ed35-240">Bitmap Encoder (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="3ed35-241">Écrit une source bitmap dans un flux d’image.</span><span class="sxs-lookup"><span data-stu-id="3ed35-241">Writes a bitmap source to an image stream.</span></span> <span data-ttu-id="3ed35-242">Associé à un format de conteneur tel que TIFF ou JPEG.</span><span class="sxs-lookup"><span data-stu-id="3ed35-242">Associated with a container format such as TIFF or JPEG.</span></span></li>
<li><span data-ttu-id="3ed35-243">Implémente une interface <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> pour générer une liste de blocs de métadonnées à écrire dans le flux de données de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="3ed35-243">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> interface to build up a list of metadata blocks to write into the data stream of the encoder.</span></span></li>
<li><span data-ttu-id="3ed35-244">Expose un générateur de requêtes pour écrire les métadonnées associées à l’image, à l’aide d’expressions de requête.</span><span class="sxs-lookup"><span data-stu-id="3ed35-244">Exposes a query writer to write the metadata associated with the image, using query expressions.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ed35-245">Encodage de trame Bitma (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="3ed35-245">Bitma Frame Encode (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="3ed35-246">Crée un frame qui sera encodé dans le flux détenu par l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="3ed35-246">Creates a frame that will be encoded into the stream held by the encoder.</span></span></li>
<li><span data-ttu-id="3ed35-247">Implémente une interface <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> pour générer une liste de blocs de métadonnées à écrire dans le flux de données du frame.</span><span class="sxs-lookup"><span data-stu-id="3ed35-247">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> interface to build up a list of metadata blocks to write into the frame's data stream.</span></span></li>
<li><span data-ttu-id="3ed35-248">Expose un générateur de requêtes pour écrire les métadonnées associées au frame, à l’aide d’expressions de requête.</span><span class="sxs-lookup"><span data-stu-id="3ed35-248">Exposes a query writer to write the metadata associated with the frame, using query expressions.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3ed35-249">Le tableau suivant décrit les composants de métadonnées WIC.</span><span class="sxs-lookup"><span data-stu-id="3ed35-249">The following table describes the WIC metadata components.</span></span> <span data-ttu-id="3ed35-250">Ces composants vous permettent de lire et d’écrire les métadonnées dans une image exposée par les composants répertoriés dans le tableau précédent.</span><span class="sxs-lookup"><span data-stu-id="3ed35-250">These components enable you to read and write the metadata in an image exposed by the components listed in the previous table.</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3ed35-251">Composant</span><span class="sxs-lookup"><span data-stu-id="3ed35-251">Component</span></span></th>
<th><span data-ttu-id="3ed35-252">Description</span><span class="sxs-lookup"><span data-stu-id="3ed35-252">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ed35-253">Lecteur de requêtes de métadonnées (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="3ed35-253">Metadata Query Reader (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="3ed35-254">Prend une chaîne de requête et parcourt la hiérarchie de métadonnées sous-jacente pour obtenir les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3ed35-254">Takes a query string and navigates the underlying metadata hierarchy to get metadata.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ed35-255">Générateur de requêtes de métadonnées (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="3ed35-255">Metadata Query Writer (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="3ed35-256">Prend une chaîne de requête et parcourt la hiérarchie de métadonnées sous-jacente pour obtenir, définir et supprimer des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3ed35-256">Takes a query string and navigates the underlying metadata hierarchy to get, set, and remove metadata.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ed35-257">Lecteur de bloc de métadonnées (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="3ed35-257">Metadata Block Reader (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="3ed35-258">Gère une collection en lecture seule d’objets <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a> en haut de la hiérarchie de métadonnées et permet l’énumération de tous les blocs de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3ed35-258">Manages a read-only collection of <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a> objects at the top of the metadata hierarchy and enables enumeration of all metadata blocks.</span></span></li>
<li><span data-ttu-id="3ed35-259">Implémenté par un décodeur bitmap et un frame bitmap décodé.</span><span class="sxs-lookup"><span data-stu-id="3ed35-259">Implemented by a bitmap decoder and a decoded bitmap frame.</span></span></li>
<li><span data-ttu-id="3ed35-260">Implémenté par les développeurs de composants tiers pour les codecs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="3ed35-260">Implemented by third-party component developers for custom codecs.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ed35-261">Enregistreur de bloc de métadonnées (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="3ed35-261">Metadata Block Writer (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="3ed35-262">Gère une collection de lecture et d’écriture d’objets <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a> en haut de la hiérarchie de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3ed35-262">Manages a read and write collection of <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a> objects at the top of the metadata hierarchy.</span></span></li>
<li><span data-ttu-id="3ed35-263">Implémenté par un encodeur bitmap et un encodage de frame bitmap.</span><span class="sxs-lookup"><span data-stu-id="3ed35-263">Implemented by a bitmap encoder and a bitmap frame encode.</span></span></li>
<li><span data-ttu-id="3ed35-264">Implémenté par les développeurs de composants tiers pour les codecs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="3ed35-264">Implemented by third-party component developers for custom codecs.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ed35-265">Lecteur de métadonnées (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="3ed35-265">Metadata Reader (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="3ed35-266">Analyse un flux de métadonnées et gère une collection en lecture seule des éléments de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3ed35-266">Parses a stream of metadata and manages a read-only collection of the metadata items.</span></span> <span data-ttu-id="3ed35-267">Associé à un format de métadonnées tel que EXIF, IFD et XMP.</span><span class="sxs-lookup"><span data-stu-id="3ed35-267">Associated with a metadata format such as EXIF, IFD, and XMP.</span></span></li>
<li><span data-ttu-id="3ed35-268">Agit comme un dictionnaire, en retournant une valeur lorsqu’une paire format-ID est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3ed35-268">Acts as a dictionary, returning a value when given a format and ID pair.</span></span></li>
<li><span data-ttu-id="3ed35-269">Implémenté par les développeurs de composants tiers pour les types de métadonnées personnalisés.</span><span class="sxs-lookup"><span data-stu-id="3ed35-269">Implemented by third-party component developers for custom metadata types.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ed35-270">Enregistreur de métadonnées (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="3ed35-270">Metadata Writer (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="3ed35-271">Analyse et sérialise un flux de métadonnées et gère une collection en lecture/écriture d’éléments de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3ed35-271">Parses and serializes a stream of metadata and manages a read/write collection of metadata items.</span></span></li>
<li><span data-ttu-id="3ed35-272">Implémenté par les développeurs de composants tiers pour les types de métadonnées personnalisés.</span><span class="sxs-lookup"><span data-stu-id="3ed35-272">Implemented by third-party component developers for custom metadata types.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ed35-273">IWICFastMetadataEncoder rapide de l’encodeur de métadonnées<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong></strong></a></span><span class="sxs-lookup"><span data-stu-id="3ed35-273">Fast Metadata Encoder<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong>IWICFastMetadataEncoder</strong></a></span></span></td>
<td><ul>
<li><span data-ttu-id="3ed35-274">Expose la sémantique pour l’écriture dans une hiérarchie de métadonnées qui met à jour les métadonnées en place sans recoder l’image.</span><span class="sxs-lookup"><span data-stu-id="3ed35-274">Exposes semantics for writing on a metadata hierarchy that will update metadata in place without re-encoding the image.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="3ed35-275">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3ed35-275">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3ed35-276">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="3ed35-276">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3ed35-277">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="3ed35-277">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="3ed35-278">Vue d’ensemble du langage de requête de métadonnées</span><span class="sxs-lookup"><span data-stu-id="3ed35-278">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="3ed35-279">Vue d’ensemble de la lecture et de l’écriture des métadonnées d’image</span><span class="sxs-lookup"><span data-stu-id="3ed35-279">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="3ed35-280">Vue d’ensemble de l’extensibilité des métadonnées</span><span class="sxs-lookup"><span data-stu-id="3ed35-280">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)
</dt> <dt>

[<span data-ttu-id="3ed35-281">Comment : recoder une image JPEG avec des métadonnées</span><span class="sxs-lookup"><span data-stu-id="3ed35-281">How-to: Re-encode a JPEG Image with Metadata</span></span>](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



