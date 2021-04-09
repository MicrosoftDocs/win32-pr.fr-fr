---
description: Cette rubrique présente le nouveau schéma XMP (Extensible Metadata Platform) et la propriété photo Windows 7 System. photo. PeopleNames qui permet d’étiqueter des individus dans une photo numérique.
ms.assetid: 557c3e9a-1756-4abb-8465-b12195ecbc91
title: Vue d’ensemble du balisage des personnes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64f2080e51d4d340474e0610fcce9512fc72429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115778"
---
# <a name="people-tagging-overview"></a><span data-ttu-id="df7f4-103">Vue d’ensemble du balisage des personnes</span><span class="sxs-lookup"><span data-stu-id="df7f4-103">People Tagging Overview</span></span>

<span data-ttu-id="df7f4-104">Cette rubrique présente le nouveau schéma XMP (Extensible Metadata Platform) et la propriété photo Windows 7 [System. photo. PeopleNames](../properties/props-system-photo-peoplenames.md) qui permet d’étiqueter des individus dans une photo numérique.</span><span class="sxs-lookup"><span data-stu-id="df7f4-104">This topic introduces the new Extensible Metadata Platform (XMP) schema and the Windows 7 photo property [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) that enables the tagging of individuals in a digital photo.</span></span> <span data-ttu-id="df7f4-105">Cette rubrique explique également comment utiliser l’API WIC (Windows Imaging Component) pour lire et écrire les métadonnées nécessaires au balisage des personnes.</span><span class="sxs-lookup"><span data-stu-id="df7f4-105">This topic also discusses how to use the Windows Imaging Component (WIC) API to both read and write the metadata needed for people tagging.</span></span>

<span data-ttu-id="df7f4-106">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="df7f4-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="df7f4-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="df7f4-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="df7f4-108">Introduction</span><span class="sxs-lookup"><span data-stu-id="df7f4-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="df7f4-109">Balisage de personnes</span><span class="sxs-lookup"><span data-stu-id="df7f4-109">People Tagging</span></span>](#people-tagging-overview)
    -   [<span data-ttu-id="df7f4-110">Noms de personnes</span><span class="sxs-lookup"><span data-stu-id="df7f4-110">People Names</span></span>](#people-names)
    -   [<span data-ttu-id="df7f4-111">Rectangles de personnes</span><span class="sxs-lookup"><span data-stu-id="df7f4-111">People Rectangles</span></span>](#people-rectangles)
-   [<span data-ttu-id="df7f4-112">Référence du schéma</span><span class="sxs-lookup"><span data-stu-id="df7f4-112">Schema Reference</span></span>](#schema-reference)
    -   [<span data-ttu-id="df7f4-113">Schéma Microsoft Photo 1,2</span><span class="sxs-lookup"><span data-stu-id="df7f4-113">Microsoft Photo 1.2 Schema</span></span>](#microsoft-photo-12-schema)
    -   [<span data-ttu-id="df7f4-114">Schéma de l’RegionInfo Microsoft Photo</span><span class="sxs-lookup"><span data-stu-id="df7f4-114">Microsoft Photo RegionInfo Schema</span></span>](#microsoft-photo-regioninfo-schema)
    -   [<span data-ttu-id="df7f4-115">Schéma de la région de photo Microsoft</span><span class="sxs-lookup"><span data-stu-id="df7f4-115">Microsoft Photo Region Schema</span></span>](#microsoft-photo-regioninfo-schema)
    -   [<span data-ttu-id="df7f4-116">Exemples de métadonnées</span><span class="sxs-lookup"><span data-stu-id="df7f4-116">Sample Metadata</span></span>](#sample-metadata)
-   [<span data-ttu-id="df7f4-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="df7f4-117">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="df7f4-118">Prérequis</span><span class="sxs-lookup"><span data-stu-id="df7f4-118">Prerequisites</span></span>

<span data-ttu-id="df7f4-119">Pour comprendre cette rubrique, vous devez être familiarisé avec les interfaces de décodeur WIC et les composants COM (Component Object Model) associés, comme décrit dans la [vue d’ensemble du composant de création d’images Windows](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="df7f4-119">To understand this topic, you should be familiar with the WIC decoder interfaces and its related Component Object Model (COM) components, as described in the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span> <span data-ttu-id="df7f4-120">Il permet également d’avoir une connaissance générale des métadonnées d’acquisition d’images, en particulier XMP.</span><span class="sxs-lookup"><span data-stu-id="df7f4-120">It also helps to have a general familiarity with imaging metadata, especially XMP.</span></span>

## <a name="introduction"></a><span data-ttu-id="df7f4-121">Introduction</span><span class="sxs-lookup"><span data-stu-id="df7f4-121">Introduction</span></span>

<span data-ttu-id="df7f4-122">Microsoft a créé un nouveau schéma XMP pour baliser les personnes au sein d’une image numérique.</span><span class="sxs-lookup"><span data-stu-id="df7f4-122">Microsoft has created a new XMP schema for tagging people within a digital image.</span></span> <span data-ttu-id="df7f4-123">Ce schéma permet aux applications de stocker les noms et les emplacements des individus qui se trouvent dans l’image en tant que métadonnées dans l’image.</span><span class="sxs-lookup"><span data-stu-id="df7f4-123">This schema enables applications to store the names and locations of individuals who are in the image as metadata within the image.</span></span> <span data-ttu-id="df7f4-124">Outre le nouveau schéma, la nouvelle propriété photo [System. photo. PeopleNames](../properties/props-system-photo-peoplenames.md) est disponible dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="df7f4-124">In addition to the new schema, the new photo property [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) is available in Windows 7.</span></span> <span data-ttu-id="df7f4-125">Cette nouvelle propriété permet aux applications de lire les noms individuels stockés dans les métadonnées de l’image.</span><span class="sxs-lookup"><span data-stu-id="df7f4-125">This new property enables applications to read the individual's names stored in the image metadata.</span></span> <span data-ttu-id="df7f4-126">WIC utilise ces nouvelles fonctionnalités en permettant aux applications de lire et d’écrire facilement des métadonnées de balisage sur des photos numériques.</span><span class="sxs-lookup"><span data-stu-id="df7f4-126">WIC utilizes these new features by enabling applications to easily read and write people tagging metadata to digital photos.</span></span>

## <a name="people-tagging"></a><span data-ttu-id="df7f4-127">Balisage de personnes</span><span class="sxs-lookup"><span data-stu-id="df7f4-127">People Tagging</span></span>

<span data-ttu-id="df7f4-128">WIC fournit aux développeurs d’applications des composants COM qui lisent les données d’image, ainsi que les métadonnées d’image.</span><span class="sxs-lookup"><span data-stu-id="df7f4-128">WIC provides application developers with COM components which read image data as well as image metadata.</span></span> <span data-ttu-id="df7f4-129">Pour la lecture et l’écriture de métadonnées, telles que la nouvelle fonctionnalité de balisage de personnes, WIC fournit les interfaces [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) et [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="df7f4-129">For reading and writing metadata, such as the new people tagging feature, WIC provides the [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) and [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) interfaces.</span></span> <span data-ttu-id="df7f4-130">Ces interfaces permettent aux applications d’utiliser le [langage de requête de métadonnées](-wic-codec-metadataquerylanguage.md) pour écrire des métadonnées dans les frames individuels d’une image.</span><span class="sxs-lookup"><span data-stu-id="df7f4-130">These interfaces enable applications to use the [metadata query language](-wic-codec-metadataquerylanguage.md) to write metadata to the individual frames of an image.</span></span> <span data-ttu-id="df7f4-131">La section suivante montre comment lire et écrire les métadonnées de balisage des personnes dans les métadonnées d’une image à l’aide de lecteurs et de Writers de requêtes WIC.</span><span class="sxs-lookup"><span data-stu-id="df7f4-131">The following section demonstrates how to read and write the people-tagging metadata into an image's metadata by using WIC query readers and writers.</span></span>

### <a name="people-names"></a><span data-ttu-id="df7f4-132">Noms de personnes</span><span class="sxs-lookup"><span data-stu-id="df7f4-132">People Names</span></span>

<span data-ttu-id="df7f4-133">Une partie de la fonctionnalité de balisage des personnes est la possibilité de simplement obtenir une liste des noms des personnes marquées dans l’image.</span><span class="sxs-lookup"><span data-stu-id="df7f4-133">Part of the people-tagging feature is the ability to simply get a list the names of the people tagged within the image.</span></span> <span data-ttu-id="df7f4-134">Cette partie de la fonctionnalité est prise en charge par les gestionnaires de métadonnées [System. photo. PeopleNames](../properties/props-system-photo-peoplenames.md) et WIC.</span><span class="sxs-lookup"><span data-stu-id="df7f4-134">This part of the feature is supported by the [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) and WIC's metadata handlers.</span></span> <span data-ttu-id="df7f4-135">L’interface [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) , conjointement à la propriété System. photo. PeopleNames, est utilisée pour lire les noms des personnes identifiées dans une image et stockées dans les métadonnées de l’image.</span><span class="sxs-lookup"><span data-stu-id="df7f4-135">The [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) interface, in conjunction with the System.Photo.PeopleNames property, are used to read the names of people identified in an image and stored in the image metadata.</span></span>

<span data-ttu-id="df7f4-136">L’exemple de code suivant montre un lecteur de requête obtenu à partir d’un frame d’image pour interroger les métadonnées d’une image pour les noms avec balises de la propriété [System. photo. PeopleNames](../properties/props-system-photo-peoplenames.md) .</span><span class="sxs-lookup"><span data-stu-id="df7f4-136">The following code example demonstrates a query reader obtained from an image frame to query an image's metadata for tagged names of the [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) property.</span></span>


```C++
// Not shown: image decoding, retrieving an image frame. 
...
PROPVARIANT value;
IWICMetadataQueryReader *pQueryReader = NULL;
...
// Get the query reader.
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}

// Query for the System.Photo.PeopleNames property.
if (SUCCEEDED(hr))
{
    // Get the property metadata by property name.
    hr = pQueryReader->GetMetadataByName(L"System.Photo.PeopleNames", &value);
}
```



<span data-ttu-id="df7f4-137">L’expression de requête « System. photo. PeopleNames » interroge le frame pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="df7f4-137">The query expression "System.Photo.PeopleNames" queries the frame for the property.</span></span> <span data-ttu-id="df7f4-138">Si les métadonnées de balisage de personnes existent et contiennent des noms de personnes, la valeur [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) est définie sur VT \_ LPWStr et la valeur des données contient la liste des noms avec balises.</span><span class="sxs-lookup"><span data-stu-id="df7f4-138">If the people-tagging metadata exists and contains people's names, the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) value will be set to VT\_LPWSTR and the data value will contain the list of tagged names.</span></span> <span data-ttu-id="df7f4-139">Pour plus d’informations sur la lecture des métadonnées d’image, consultez [vue d’ensemble de la lecture et de l’écriture de métadonnées d’image](-wic-codec-readingwritingmetadata.md).</span><span class="sxs-lookup"><span data-stu-id="df7f4-139">For more information on reading image metadata, see [Overview of Reading and Writing Image Metadata](-wic-codec-readingwritingmetadata.md).</span></span>

<span data-ttu-id="df7f4-140">L’interrogation de la balise People Names n’est utile que si l’image contient réellement les métadonnées de balisage.</span><span class="sxs-lookup"><span data-stu-id="df7f4-140">Querying for the people names tag is only useful if the image actually contains the people-tagging metadata.</span></span> <span data-ttu-id="df7f4-141">Pour que cela se produise, une application doit d’abord l’avoir écrite.</span><span class="sxs-lookup"><span data-stu-id="df7f4-141">For this to occur, an application must first have written it.</span></span> <span data-ttu-id="df7f4-142">Pour écrire les métadonnées de noms de personnes, utilisez un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) et le chemin d’accès XMP explicite des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="df7f4-142">To write the people names metadata, use an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) and the explicit XMP path of the metadata.</span></span> <span data-ttu-id="df7f4-143">L’exemple de code suivant illustre l’utilisation d’un générateur de requêtes pour écrire un nom dans le chemin d’accès de la requête.</span><span class="sxs-lookup"><span data-stu-id="df7f4-143">The following code example demonstrates using a query writer to write a name to the query path.</span></span>


```C++
// Not shown: image encoding, retrieving/creating the image frame,
// creating the IWICImagingFactory 
...
IWICImagingFactory *pFactory = NULL;
IWICMetadataQueryWriter *pQueryWriter = NULL;
...
// Get the query writer from the image frame.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pQueryWriter);
}

// A query writer specifically for this person's XMP struct
IWICMetadataQueryWriter *pXMPStructQueryWriter = NULL;

// Create a query writer specifically for an XMP Struct
hr = pFactory->CreateQueryWriter(
    GUID_MetadataFormatXMPStruct,
    NULL,
    &pXMPStructQueryWriter
    );

// Create a variant representing the structure created above
PROPVARIANT xmpStruct;
PropVariantInit(&xmpStruct);

// VT_UNKNOWN indicates that we're setting a COM object, in this case a XMPStruct
// which will hold the name and rectangle
xmpStruct.vt = VT_UNKNOWN; 
xmpStruct.punkVal = pXMPStructQueryWriter;

if(SUCCEEDED(hr))
{
    // WIC will automatically create the xmp base, the RegionInfo struct, and the Regions
    // bag (an unordered array) but structs within that bag need to be explicitly created.
    // The {ulong=0} in the query means to insert the new struct at the start of the bag,
    // {} could also be used to insert at the end of the bag.
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions/{ulong=0}",
        &xmpStruct
        );
}

// Set up the PROPVARIANT with the name information
PROPVARIANT personName;
PropVariantInit(&personName);
personName.vt = VT_LPWSTR;
personName.pwszVal = L"John Doe";

if(SUCCEEDED(hr))
{
    // Set the name metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:PersonDisplayName",
        &personName
        );  
}
```



<span data-ttu-id="df7f4-144">Notez l’étape qui consiste à construire la structure XMP et à la définir sous `MPRI:Regions/{ulong=0}` .</span><span class="sxs-lookup"><span data-stu-id="df7f4-144">Note the step constructing the XMP structure and setting it under `MPRI:Regions/{ulong=0}`.</span></span> <span data-ttu-id="df7f4-145">Sans cette étape, le WIC ne peut pas identifier où placer `PersonDisplayName` ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="df7f4-145">Without this step, the WIC can't identify where to place the `PersonDisplayName` later on.</span></span> <span data-ttu-id="df7f4-146">Notez également que le chemin de requête explicite est utilisé à la place de [System. photo. PeopleNames](-wic-photoprop-system-photo-peoplenames.md), dont la stratégie de métadonnées ne prend pas en charge l’écriture de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="df7f4-146">Also note that the explicit query path is used instead of [System.Photo.PeopleNames](-wic-photoprop-system-photo-peoplenames.md), whose metadata policy does not support writing metadata.</span></span>

### <a name="people-rectangles"></a><span data-ttu-id="df7f4-147">Rectangles de personnes</span><span class="sxs-lookup"><span data-stu-id="df7f4-147">People Rectangles</span></span>

<span data-ttu-id="df7f4-148">Toutefois, les noms des personnes font uniquement partie de la fonctionnalité de balisage des personnes.</span><span class="sxs-lookup"><span data-stu-id="df7f4-148">People's names however, are only part of the people-tagging feature.</span></span> <span data-ttu-id="df7f4-149">Outre le stockage des noms des personnes dans les métadonnées, le schéma prend également en charge les informations de région qui identifient la zone spécifique (un rectangle) que la personne affiche dans l’image.</span><span class="sxs-lookup"><span data-stu-id="df7f4-149">In addition to storing people's names in the metadata, the schema also supports region information that identifies the specific area (a rectangle) the person is shown in the image.</span></span>

<span data-ttu-id="df7f4-150">Les informations de rectangle sont représentées par quatre valeurs décimales délimitées par des virgules, telles que « 0,25, 0,25, 0,25, 0,25 ».</span><span class="sxs-lookup"><span data-stu-id="df7f4-150">The rectangle information is represented by four comma-delimited decimal values, such as "0.25, 0.25, 0.25, 0.25".</span></span> <span data-ttu-id="df7f4-151">Les deux premières valeurs spécifient la coordonnée supérieure gauche ; les deux derniers spécifient la hauteur et la largeur du rectangle.</span><span class="sxs-lookup"><span data-stu-id="df7f4-151">The first two values specify the top-left coordinate; the final two specify the height and width of the rectangle.</span></span> <span data-ttu-id="df7f4-152">Les dimensions de l’image dans le cadre de la définition des rectangles de personnes sont normalisées à 1, ce qui signifie que dans l’exemple « 0,25, 0,25, 0,25, 0,25 », le rectangle démarre 1/4 de la distance à partir du haut et de 1/4 de la distance à partir de la gauche de l’image.</span><span class="sxs-lookup"><span data-stu-id="df7f4-152">The dimensions of the image for the purposes of defining people rectangles are normalized to 1, which means that in the "0.25, 0.25, 0.25, 0.25" example, the rectangle starts 1/4 of the distance from the top and 1/4 of the distance from the left of the image.</span></span> <span data-ttu-id="df7f4-153">La hauteur et la largeur du rectangle sont 1/4 de la taille de leurs dimensions d’image respectives.</span><span class="sxs-lookup"><span data-stu-id="df7f4-153">Both the height and width of the rectangle are 1/4 of the size of their respective image dimensions.</span></span>

<span data-ttu-id="df7f4-154">Les informations de rectangle qui identifient les individus sont écrites de la même façon que les noms des personnes, au sein de la même structure.</span><span class="sxs-lookup"><span data-stu-id="df7f4-154">The rectangle information that identifies individuals is written in the same way people's names are written, within the same structure.</span></span> <span data-ttu-id="df7f4-155">Pour écrire les métadonnées de rectangle, utilisez un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) et le chemin d’accès XMP explicite des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="df7f4-155">To write the rectangle metadata, use an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) and the explicit XMP path of the metadata.</span></span> <span data-ttu-id="df7f4-156">L’exemple de code suivant poursuit l’exemple précédent et ajoute un rectangle représentant « John Doe » aux métadonnées de l’image.</span><span class="sxs-lookup"><span data-stu-id="df7f4-156">The following code example continues the previous example and adds a rectangle representing 'John Doe' to the image's metadata.</span></span> <span data-ttu-id="df7f4-157">Notez qu’il utilise le même `{ulong=0}` index pour associer ce rectangle à « John Doe ».</span><span class="sxs-lookup"><span data-stu-id="df7f4-157">Note that it uses the same `{ulong=0}` index to associate this rectangle with 'John Doe'.</span></span>


```C++
// Set up the PROPVARIANT with the rectangle information
PROPVARIANT rectangle;
PropVariantInit(&rectangle);
rectangle.vt = VT_LPWSTR;
rectangle.pwszVal = L"0.0,0.0,0.25,0.25";

if(SUCCEEDED(hr))
{
    // Set the rectangle metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:Rectangle",
        &rectangle
        );
}
```



## <a name="schema-reference"></a><span data-ttu-id="df7f4-158">Référence du schéma</span><span class="sxs-lookup"><span data-stu-id="df7f4-158">Schema Reference</span></span>

<span data-ttu-id="df7f4-159">Les schémas XMP Microsoft pour les balises de personnes définissent un ensemble de propriétés pour baliser des personnes dans des photos numériques.</span><span class="sxs-lookup"><span data-stu-id="df7f4-159">The Microsoft XMP schemas for people tagging define a set of properties to tag individuals in digital photos.</span></span>

<span data-ttu-id="df7f4-160">Les sections suivantes fournissent les définitions de schéma nécessaires pour le balisage des personnes.</span><span class="sxs-lookup"><span data-stu-id="df7f4-160">The following sections provide the schema definitions needed for people tagging.</span></span> <span data-ttu-id="df7f4-161">Dans la mesure du possible, les définitions de schéma utilisent les conventions fournies par les [spécifications XMP (Extensible Metadata Platform) d’Adobe](https://www.adobe.com/devnet/xmp/).</span><span class="sxs-lookup"><span data-stu-id="df7f4-161">Wherever possible, the schema definitions use the conventions provided by [Adobe's Extensible Metadata Platform (XMP) Specifications](https://www.adobe.com/devnet/xmp/).</span></span> <span data-ttu-id="df7f4-162">Les définitions de schéma de cette rubrique indiquent l’espace de noms XML Uniform Resource Identifier (URI) qui identifie le schéma et le préfixe d’espace de noms de schéma par défaut, suivis d’un tableau qui répertorie toutes les propriétés définies pour le schéma.</span><span class="sxs-lookup"><span data-stu-id="df7f4-162">The schema definitions in this topic show the XML namespace Uniform Resource Identifier (URI) that identifies the schema and the preferred schema namespace prefix, followed by a table that lists all properties defined for the schema.</span></span> <span data-ttu-id="df7f4-163">Chaque table contient les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="df7f4-163">Each table has the following columns:</span></span>

-   <span data-ttu-id="df7f4-164">**Property** -le nom de la propriété, y compris le préfixe d’espace de noms préféré.</span><span class="sxs-lookup"><span data-stu-id="df7f4-164">**Property** - The name of the property, including the preferred namespace prefix.</span></span>

-   <span data-ttu-id="df7f4-165">**Type de valeur** : type de valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="df7f4-165">**Value type** - The value type of the property.</span></span> <span data-ttu-id="df7f4-166">Les schémas de prise en charge du balisage des personnes utilisent les types de valeur XMP chaque fois que cela est possible, y compris la date et le texte.</span><span class="sxs-lookup"><span data-stu-id="df7f4-166">The people-tagging support schemas use the XMP value types whenever possible, including Date and Text.</span></span> <span data-ttu-id="df7f4-167">Les types de tableau sont précédés du type de conteneur : `alt` , `bag` ou `seq` .</span><span class="sxs-lookup"><span data-stu-id="df7f4-167">Array types are preceded by the container type: `alt`, `bag`, or `seq`.</span></span>

-   <span data-ttu-id="df7f4-168">**Category** -les propriétés de schéma sont internes ou externes :</span><span class="sxs-lookup"><span data-stu-id="df7f4-168">**Category** - Schema properties are internal or external:</span></span>

    -   <span data-ttu-id="df7f4-169">Les métadonnées internes doivent être définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="df7f4-169">Internal metadata must be set by the application.</span></span>

    -   <span data-ttu-id="df7f4-170">Les métadonnées externes doivent être définies par l’utilisateur et sont indépendantes du contenu du document.</span><span class="sxs-lookup"><span data-stu-id="df7f4-170">External metadata must be set by the user and is independent of the contents of the document.</span></span>

-   <span data-ttu-id="df7f4-171">**Description** : description de la propriété.</span><span class="sxs-lookup"><span data-stu-id="df7f4-171">**Description** - The description of the property.</span></span>

### <a name="microsoft-photo-12-schema"></a><span data-ttu-id="df7f4-172">Schéma Microsoft Photo 1,2</span><span class="sxs-lookup"><span data-stu-id="df7f4-172">Microsoft Photo 1.2 Schema</span></span>

<span data-ttu-id="df7f4-173">Le schéma Microsoft Photo 1,2 fournit un ensemble de propriétés pour les zones d’image.</span><span class="sxs-lookup"><span data-stu-id="df7f4-173">The Microsoft Photo 1.2 schema provides a set of properties for image regions.</span></span>

-   <span data-ttu-id="df7f4-174">L’URI de l’espace de noms du schéma est `https://ns.microsoft.com/photo/1.2/` .</span><span class="sxs-lookup"><span data-stu-id="df7f4-174">The schema namespace URI is `https://ns.microsoft.com/photo/1.2/`.</span></span>
-   <span data-ttu-id="df7f4-175">Le préfixe de l’espace de noms du schéma par défaut est `MP` .</span><span class="sxs-lookup"><span data-stu-id="df7f4-175">The preferred schema namespace prefix is `MP`.</span></span>



| <span data-ttu-id="df7f4-176">Propriété</span><span class="sxs-lookup"><span data-stu-id="df7f4-176">Property</span></span>      | <span data-ttu-id="df7f4-177">Type de valeur</span><span class="sxs-lookup"><span data-stu-id="df7f4-177">Value type</span></span> | <span data-ttu-id="df7f4-178">Category</span><span class="sxs-lookup"><span data-stu-id="df7f4-178">Category</span></span> | <span data-ttu-id="df7f4-179">Description</span><span class="sxs-lookup"><span data-stu-id="df7f4-179">Description</span></span>                                                                                                                     |
|---------------|------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df7f4-180">MP : RegionInfo</span><span class="sxs-lookup"><span data-stu-id="df7f4-180">MP:RegionInfo</span></span> | <span data-ttu-id="df7f4-181">RegionInfo</span><span class="sxs-lookup"><span data-stu-id="df7f4-181">RegionInfo</span></span> | <span data-ttu-id="df7f4-182">Interne</span><span class="sxs-lookup"><span data-stu-id="df7f4-182">Internal</span></span> | <span data-ttu-id="df7f4-183">**obligatoire** : stocke la racine des métadonnées de balisage des personnes.</span><span class="sxs-lookup"><span data-stu-id="df7f4-183">**required** : Stores the root of the people-tagging metadata.</span></span> <span data-ttu-id="df7f4-184">Consultez la section relative au schéma Microsoft Photo RegionInfo qui suit.</span><span class="sxs-lookup"><span data-stu-id="df7f4-184">See the Microsoft Photo RegionInfo Schema section which follows.</span></span> |



 

### <a name="microsoft-photo-regioninfo-schema"></a><span data-ttu-id="df7f4-185">Schéma de l’RegionInfo Microsoft Photo</span><span class="sxs-lookup"><span data-stu-id="df7f4-185">Microsoft Photo RegionInfo Schema</span></span>

<span data-ttu-id="df7f4-186">Le schéma Microsoft Photo RegionInfo 1,2 fournit un ensemble de propriétés pour les informations de région.</span><span class="sxs-lookup"><span data-stu-id="df7f4-186">The Microsoft Photo RegionInfo 1.2 schema provides a set of properties for region info.</span></span>

-   <span data-ttu-id="df7f4-187">L’URI de l’espace de noms du schéma est `https://ns.microsoft.com/photo/1.2/t/RegionInfo#` .</span><span class="sxs-lookup"><span data-stu-id="df7f4-187">The schema namespace URI is `https://ns.microsoft.com/photo/1.2/t/RegionInfo#`.</span></span>
-   <span data-ttu-id="df7f4-188">Le préfixe de l’espace de noms du schéma par défaut est `MPRI` .</span><span class="sxs-lookup"><span data-stu-id="df7f4-188">The preferred schema namespace prefix is `MPRI`.</span></span>



| <span data-ttu-id="df7f4-189">Propriété</span><span class="sxs-lookup"><span data-stu-id="df7f4-189">Property</span></span>              | <span data-ttu-id="df7f4-190">Type de valeur</span><span class="sxs-lookup"><span data-stu-id="df7f4-190">Value type</span></span> | <span data-ttu-id="df7f4-191">Category</span><span class="sxs-lookup"><span data-stu-id="df7f4-191">Category</span></span> | <span data-ttu-id="df7f4-192">Description</span><span class="sxs-lookup"><span data-stu-id="df7f4-192">Description</span></span>                                                                                                    |
|-----------------------|------------|----------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df7f4-193">MPRI:DateRegionsValid</span><span class="sxs-lookup"><span data-stu-id="df7f4-193">MPRI:DateRegionsValid</span></span> | <span data-ttu-id="df7f4-194">Date</span><span class="sxs-lookup"><span data-stu-id="df7f4-194">Date</span></span>       | <span data-ttu-id="df7f4-195">Externe</span><span class="sxs-lookup"><span data-stu-id="df7f4-195">External</span></span> | <span data-ttu-id="df7f4-196">**facultatif** : date de création de la dernière région.</span><span class="sxs-lookup"><span data-stu-id="df7f4-196">**optional** : Date that the last region was created.</span></span>                                                          |
| <span data-ttu-id="df7f4-197">MPRI : régions</span><span class="sxs-lookup"><span data-stu-id="df7f4-197">MPRI:Regions</span></span>          | <span data-ttu-id="df7f4-198">Région de sac</span><span class="sxs-lookup"><span data-stu-id="df7f4-198">bag Region</span></span> | <span data-ttu-id="df7f4-199">Externe</span><span class="sxs-lookup"><span data-stu-id="df7f4-199">External</span></span> | <span data-ttu-id="df7f4-200">**obligatoire** : stocke les régions de marquage des personnes.</span><span class="sxs-lookup"><span data-stu-id="df7f4-200">**required** : Stores the people tagging regions.</span></span> <span data-ttu-id="df7f4-201">Consultez la section schéma de la zone de photo Microsoft qui suit.</span><span class="sxs-lookup"><span data-stu-id="df7f4-201">See the Microsoft Photo Region Schema section which follows.</span></span> |



 

### <a name="microsoft-photo-region-schema"></a><span data-ttu-id="df7f4-202">Schéma de la région de photo Microsoft</span><span class="sxs-lookup"><span data-stu-id="df7f4-202">Microsoft Photo Region Schema</span></span>

<span data-ttu-id="df7f4-203">Le schéma de la zone de photo Microsoft 1,2 fournit un ensemble de propriétés pour les régions d’image.</span><span class="sxs-lookup"><span data-stu-id="df7f4-203">The Microsoft Photo Region 1.2 schema provides a set of properties for image regions.</span></span>

-   <span data-ttu-id="df7f4-204">L’URI de l’espace de noms du schéma est `https://ns.microsoft.com/photo/1.2/t/Region#` .</span><span class="sxs-lookup"><span data-stu-id="df7f4-204">The schema namespace URI is `https://ns.microsoft.com/photo/1.2/t/Region#`.</span></span>
-   <span data-ttu-id="df7f4-205">Le préfixe de l’espace de noms du schéma par défaut est `MPReg` .</span><span class="sxs-lookup"><span data-stu-id="df7f4-205">The preferred schema namespace prefix is `MPReg`.</span></span>



| <span data-ttu-id="df7f4-206">MPReg : propriété</span><span class="sxs-lookup"><span data-stu-id="df7f4-206">MPReg:Property</span></span>          | <span data-ttu-id="df7f4-207">Type de valeur</span><span class="sxs-lookup"><span data-stu-id="df7f4-207">Value type</span></span> | <span data-ttu-id="df7f4-208">Category</span><span class="sxs-lookup"><span data-stu-id="df7f4-208">Category</span></span> | <span data-ttu-id="df7f4-209">Description</span><span class="sxs-lookup"><span data-stu-id="df7f4-209">Description</span></span>                                                                                                                                                                                                                                                                                                     |
|-------------------------|------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df7f4-210">MPReg:PersonDisplayName</span><span class="sxs-lookup"><span data-stu-id="df7f4-210">MPReg:PersonDisplayName</span></span> | <span data-ttu-id="df7f4-211">Texte</span><span class="sxs-lookup"><span data-stu-id="df7f4-211">Text</span></span>       | <span data-ttu-id="df7f4-212">Externe</span><span class="sxs-lookup"><span data-stu-id="df7f4-212">External</span></span> | <span data-ttu-id="df7f4-213">**Required** : stocke le nom de la personne dans le rectangle donné.</span><span class="sxs-lookup"><span data-stu-id="df7f4-213">**required** : Stores the name of the person in the given rectangle.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="df7f4-214">MPReg : rectangle</span><span class="sxs-lookup"><span data-stu-id="df7f4-214">MPReg:Rectangle</span></span>         | <span data-ttu-id="df7f4-215">Texte</span><span class="sxs-lookup"><span data-stu-id="df7f4-215">Text</span></span>       | <span data-ttu-id="df7f4-216">Externe</span><span class="sxs-lookup"><span data-stu-id="df7f4-216">External</span></span> | <span data-ttu-id="df7f4-217">**facultatif** : stocke le rectangle qui identifie la personne au sein de la photo.</span><span class="sxs-lookup"><span data-stu-id="df7f4-217">**optional** : Stores the rectangle that identifies the person within the photo.</span></span> <span data-ttu-id="df7f4-218">Le rectangle est stocké sous la forme de quatre valeurs décimales délimitées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="df7f4-218">The rectangle is stored as four comma-delimited decimal values.</span></span> <span data-ttu-id="df7f4-219">Les deux premières valeurs spécifient la coordonnée supérieure gauche ; les deux derniers spécifient la hauteur et la largeur du rectangle.</span><span class="sxs-lookup"><span data-stu-id="df7f4-219">The first two values specify the top left coordinate; the final two specify the height and width of the rectangle.</span></span> <span data-ttu-id="df7f4-220">Les valeurs décimales doivent être normalisées en 1.</span><span class="sxs-lookup"><span data-stu-id="df7f4-220">The decimal values must be normalized to 1.</span></span> |
| <span data-ttu-id="df7f4-221">MPReg:PersonEmailDigest</span><span class="sxs-lookup"><span data-stu-id="df7f4-221">MPReg:PersonEmailDigest</span></span> | <span data-ttu-id="df7f4-222">Texte</span><span class="sxs-lookup"><span data-stu-id="df7f4-222">Text</span></span>       | <span data-ttu-id="df7f4-223">Externe</span><span class="sxs-lookup"><span data-stu-id="df7f4-223">External</span></span> | <span data-ttu-id="df7f4-224">**facultatif** : stocke le hachage de message SHA-1 chiffré de l’adresse de messagerie en direct de la personne.</span><span class="sxs-lookup"><span data-stu-id="df7f4-224">**optional** : Stores the SHA-1 encrypted message hash of the person's Live e-mail address.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="df7f4-225">MPReg:PersonLiveIdCID</span><span class="sxs-lookup"><span data-stu-id="df7f4-225">MPReg:PersonLiveIdCID</span></span>   | <span data-ttu-id="df7f4-226">Texte</span><span class="sxs-lookup"><span data-stu-id="df7f4-226">Text</span></span>       | <span data-ttu-id="df7f4-227">Externe</span><span class="sxs-lookup"><span data-stu-id="df7f4-227">External</span></span> | <span data-ttu-id="df7f4-228">**facultatif** : stocke la représentation décimale signée du CID actif de la personne, un entier 64 bits qui identifie publiquement une identité active.</span><span class="sxs-lookup"><span data-stu-id="df7f4-228">**optional** :Stores the signed decimal representation of the person's Live CID, a 64-bit integer that publicly identifies a Live identity.</span></span>                                                                                                                                                                     |



 

### <a name="sample-metadata"></a><span data-ttu-id="df7f4-229">Exemples de métadonnées</span><span class="sxs-lookup"><span data-stu-id="df7f4-229">Sample Metadata</span></span>

<span data-ttu-id="df7f4-230">Voici une représentation des métadonnées XMP pour le balisage des personnes.</span><span class="sxs-lookup"><span data-stu-id="df7f4-230">The following is a representation of the XMP metadata for people tagging.</span></span>

``` syntax
<rdf:Description rdf:about="" xmlns:MP="https://ns.microsoft.com/photo/1.2/">
<MP:RegionInfo> 
<rdf:Description xmlns:MPRI="https://ns.microsoft.com/photo/1.2/t/RegionInfo#">
   <MPRI:Regions> 
       <rdf:Bag> 
          <rdf:li> 
       <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#"> 
           <MPReg:Rectangle>0.790650, 0.441734, 0.209350, 0.279133
           </MPReg:Rectangle>
           <MPReg:PersonDisplayName>John Doe</MPReg:PersonDisplayName> 
           <MPReg:PersonEmailDigest>2FD4E1C67A2D28FCED849EE1BB76E7391B93EB13</MPReg:PersonEmailDigest> 
           <MPReg:PersonLiveIdCID>1234567890123456789</MPReg:PersonLiveIdCID> 
       </rdf:Description> 
         </rdf:li> 
         <rdf:li>
             <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#">
                  <MPReg:Rectangle>0.222656, 0.302083, 0.378906, 0.505208</MPReg:Rectangle> 
                  <MPReg:PersonDisplayName>Jane Doe</MPReg:PersonDisplayName> 
              </rdf:Description> 
         </rdf:li> 
<!-- Addition Regions --> ... 
<rdf:li>...
</rdf:li> 
</rdf:Bag> 
</MPRI:Regions> </rdf:Description> </MP:RegionInfo> </rdf:Description>
```

## <a name="related-topics"></a><span data-ttu-id="df7f4-231">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="df7f4-231">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="df7f4-232">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="df7f4-232">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="df7f4-233">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="df7f4-233">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="df7f4-234">Vue d’ensemble des métadonnées WIC</span><span class="sxs-lookup"><span data-stu-id="df7f4-234">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="df7f4-235">Vue d’ensemble de la lecture et de l’écriture des métadonnées d’image</span><span class="sxs-lookup"><span data-stu-id="df7f4-235">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="df7f4-236">Vue d’ensemble du langage de requête de métadonnées</span><span class="sxs-lookup"><span data-stu-id="df7f4-236">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> </dl>

 

 
