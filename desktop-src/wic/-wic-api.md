---
description: Le composant WIC (Windows Imaging Component) fournit une API COM (Component Object Model) à utiliser en C et C++.
ms.assetid: 74b14b5e-70e9-410f-a6e6-d8873a5f4fa4
title: Vue d’ensemble de l’API WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86e5a876010e52489adac9baa7ce57fdfdf80f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536681"
---
# <a name="wic-api-overview"></a><span data-ttu-id="80b28-103">Vue d’ensemble de l’API WIC</span><span class="sxs-lookup"><span data-stu-id="80b28-103">WIC API Overview</span></span>

<span data-ttu-id="80b28-104">Le composant WIC (Windows Imaging Component) fournit une API COM (Component Object Model) à utiliser en C et C++.</span><span class="sxs-lookup"><span data-stu-id="80b28-104">The Windows Imaging Component (WIC) provides a Component Object Model (COM) based API for use in C and C++.</span></span> <span data-ttu-id="80b28-105">L’API WIC expose une variété de fonctionnalités liées aux images, notamment :</span><span class="sxs-lookup"><span data-stu-id="80b28-105">The WIC API exposes a variety of image-related functionality, including:</span></span>

-   <span data-ttu-id="80b28-106">Codecs intégrés pour les formats d’image Web standard.</span><span class="sxs-lookup"><span data-stu-id="80b28-106">Built-in codecs for the standard web image formats.</span></span>
-   <span data-ttu-id="80b28-107">Prise en charge intégrée des formats de métadonnées standard.</span><span class="sxs-lookup"><span data-stu-id="80b28-107">Built-in support for standard metadata formats.</span></span>
-   <span data-ttu-id="80b28-108">Large éventail de prise en charge du format de pixel.</span><span class="sxs-lookup"><span data-stu-id="80b28-108">Wide range of pixel format support.</span></span>
-   <span data-ttu-id="80b28-109">Prise en charge des couleurs élevées ; y compris les formats de pixels étendus 30 bits, haute précision 30 bits et haute précision 48 bits et à large gamme.</span><span class="sxs-lookup"><span data-stu-id="80b28-109">High-color support; including 30-bit extended range, 30-bit high precision, and 48-bit high precision and wide gamut pixel formats.</span></span>
-   <span data-ttu-id="80b28-110">Framework extensible pour les codecs d’image, les formats de pixel et les formats de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="80b28-110">Extensible framework for image codecs, pixel formats, and metadata formats.</span></span>

<span data-ttu-id="80b28-111">Cette rubrique contient les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="80b28-111">This topic contains the following topics.</span></span>

-   [<span data-ttu-id="80b28-112">Fichiers d’en-tête WIC</span><span class="sxs-lookup"><span data-stu-id="80b28-112">WIC Header Files</span></span>](#wic-header-files)
-   [<span data-ttu-id="80b28-113">Fichiers de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="80b28-113">Library Files</span></span>](#library-files)
-   [<span data-ttu-id="80b28-114">Fabriques de classes</span><span class="sxs-lookup"><span data-stu-id="80b28-114">Class Factories</span></span>](#class-factories)
-   [<span data-ttu-id="80b28-115">Composants de création d’images</span><span class="sxs-lookup"><span data-stu-id="80b28-115">Imaging Components</span></span>](#imaging-components)
-   [<span data-ttu-id="80b28-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80b28-116">See Also</span></span>](#see-also)

## <a name="wic-header-files"></a><span data-ttu-id="80b28-117">Fichiers d’en-tête WIC</span><span class="sxs-lookup"><span data-stu-id="80b28-117">WIC Header Files</span></span>

<span data-ttu-id="80b28-118">Les API WIC sont définies dans les fichiers d’en-tête et IDL (Interface Definition Language) suivants :</span><span class="sxs-lookup"><span data-stu-id="80b28-118">The WIC APIs are defined in the following header and Interface Definition Language (IDL) files:</span></span>



| <span data-ttu-id="80b28-119">Fichier</span><span class="sxs-lookup"><span data-stu-id="80b28-119">File</span></span>              | <span data-ttu-id="80b28-120">Description</span><span class="sxs-lookup"><span data-stu-id="80b28-120">Description</span></span>                                          |
|-------------------|------------------------------------------------------|
| <span data-ttu-id="80b28-121">wincodec. h</span><span class="sxs-lookup"><span data-stu-id="80b28-121">wincodec.h</span></span>        | <span data-ttu-id="80b28-122">Définit les versions C et C++ des API WIC principales.</span><span class="sxs-lookup"><span data-stu-id="80b28-122">Defines C and C++ versions of the primary WIC APIs.</span></span>  |
| <span data-ttu-id="80b28-123">wincodec. idl</span><span class="sxs-lookup"><span data-stu-id="80b28-123">wincodec.idl</span></span>      | <span data-ttu-id="80b28-124">Définit les interfaces WIC principales.</span><span class="sxs-lookup"><span data-stu-id="80b28-124">Defines the primary WIC interfaces.</span></span>                  |
| <span data-ttu-id="80b28-125">wincodecsdk. h</span><span class="sxs-lookup"><span data-stu-id="80b28-125">wincodecsdk.h</span></span>     | <span data-ttu-id="80b28-126">Définit les versions C et C++ des API WIC de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="80b28-126">Defines C and C++ versions of the metadata WIC APIs.</span></span> |
| <span data-ttu-id="80b28-127">wincodecsdk. idl</span><span class="sxs-lookup"><span data-stu-id="80b28-127">wincodecsdk.idl</span></span>   | <span data-ttu-id="80b28-128">Définit les interfaces de métadonnées WIC.</span><span class="sxs-lookup"><span data-stu-id="80b28-128">Defines the WIC metadata interfaces.</span></span>                 |
| <span data-ttu-id="80b28-129">wincodec \_ proxy. h</span><span class="sxs-lookup"><span data-stu-id="80b28-129">wincodec\_proxy.h</span></span> | <span data-ttu-id="80b28-130">Définit les exportations du proxy WIC.</span><span class="sxs-lookup"><span data-stu-id="80b28-130">Defines the WIC proxy exports.</span></span>                       |



 

<span data-ttu-id="80b28-131">Pour utiliser le WIC, vos applications doivent inclure wincodec. h et/ou wincodecsdk. h, en fonction de l’API dont votre application a besoin.</span><span class="sxs-lookup"><span data-stu-id="80b28-131">To use WIC, your applications must include wincodec.h and/or wincodecsdk.h, depending on the API your application needs.</span></span>

## <a name="library-files"></a><span data-ttu-id="80b28-132">Fichiers de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="80b28-132">Library Files</span></span>

<span data-ttu-id="80b28-133">Fichiers de bibliothèque WIC :</span><span class="sxs-lookup"><span data-stu-id="80b28-133">The WIC library files:</span></span>



| <span data-ttu-id="80b28-134">Fichier</span><span class="sxs-lookup"><span data-stu-id="80b28-134">File</span></span>              | <span data-ttu-id="80b28-135">Description</span><span class="sxs-lookup"><span data-stu-id="80b28-135">Description</span></span>                                                            |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="80b28-136">windowscodecs. lib</span><span class="sxs-lookup"><span data-stu-id="80b28-136">windowscodecs.lib</span></span> | <span data-ttu-id="80b28-137">Bibliothèque d’importation fournie par le kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="80b28-137">Import library provided by the Windows Software Development Kit (SDK).</span></span> |
| <span data-ttu-id="80b28-138">windowscodecs.dll</span><span class="sxs-lookup"><span data-stu-id="80b28-138">windowscodecs.dll</span></span> | <span data-ttu-id="80b28-139">Bibliothèque d’implémentation stock fournie par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="80b28-139">Stock implementation library provided by the operating system.</span></span>         |



 

<span data-ttu-id="80b28-140">Pour créer un lien vers des API WIC, votre application doit inclure windowscodec. lib comme dépendance supplémentaire de l’éditeur de liens.</span><span class="sxs-lookup"><span data-stu-id="80b28-140">To link to WIC APIs, your application must include windowscodec.lib as an additional linker dependency.</span></span>

## <a name="class-factories"></a><span data-ttu-id="80b28-141">Fabriques de classes</span><span class="sxs-lookup"><span data-stu-id="80b28-141">Class Factories</span></span>

<span data-ttu-id="80b28-142">Le tableau suivant décrit les deux fabriques de classes COM fournies par les API WIC pour la création de composants WIC.</span><span class="sxs-lookup"><span data-stu-id="80b28-142">The following table describes the two COM class factories the WIC APIs provide for creating WIC components.</span></span>



| <span data-ttu-id="80b28-143">Interface de fabrique</span><span class="sxs-lookup"><span data-stu-id="80b28-143">Factory Interface</span></span>                                               | <span data-ttu-id="80b28-144">Description</span><span class="sxs-lookup"><span data-stu-id="80b28-144">Description</span></span>                                                                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="80b28-145">**IWICImagingFactory**</span><span class="sxs-lookup"><span data-stu-id="80b28-145">**IWICImagingFactory**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)     | <span data-ttu-id="80b28-146">Fabrique de classe principale pour le développement d’applications à l’aide de composants WIC.</span><span class="sxs-lookup"><span data-stu-id="80b28-146">Primary class factory for application development using WIC components.</span></span> <span data-ttu-id="80b28-147">Cette fabrique crée des composants tels que les décodeurs d’images, les encodeurs et les flux.</span><span class="sxs-lookup"><span data-stu-id="80b28-147">This factory creates components such as image decoders, encoders and streams.</span></span>   |
| [<span data-ttu-id="80b28-148">**IWICComponentFactory**</span><span class="sxs-lookup"><span data-stu-id="80b28-148">**IWICComponentFactory**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) | <span data-ttu-id="80b28-149">Fabrique de classe ciblée pour les développeurs de composants WIC.</span><span class="sxs-lookup"><span data-stu-id="80b28-149">Class factory targeted for WIC component developers.</span></span> <span data-ttu-id="80b28-150">Les composants créés à partir de cette fabrique sont principalement utilisés dans le codec et le développement du gestionnaire de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="80b28-150">Components created from this factory are primarily used in codec and metadata handler development.</span></span> |



 

<span data-ttu-id="80b28-151">Pour créer une fabrique de classes, utilisez la fonction com [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="80b28-151">To create either class factory, use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) COM function.</span></span> <span data-ttu-id="80b28-152">L’exemple suivant illustre la création de la fabrique d’images WIC.</span><span class="sxs-lookup"><span data-stu-id="80b28-152">The following example demonstrates the creation of the WIC imaging factory.</span></span>


```C++
// Initialize COM
CoInitialize(NULL);

// The factory pointer
IWICImagingFactory *pFactory = NULL;

// Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_PPV_ARGS(&pFactory)
);
```



## <a name="imaging-components"></a><span data-ttu-id="80b28-153">Composants de création d’images</span><span class="sxs-lookup"><span data-stu-id="80b28-153">Imaging Components</span></span>

<span data-ttu-id="80b28-154">Les API WIC fournissent plusieurs types de composants d’image.</span><span class="sxs-lookup"><span data-stu-id="80b28-154">The WIC APIs provide several types of imaging components.</span></span> <span data-ttu-id="80b28-155">Le tableau suivant décrit certains des composants de WIC courants.</span><span class="sxs-lookup"><span data-stu-id="80b28-155">The following table describes some of the common WIC components.</span></span> <span data-ttu-id="80b28-156">Pour obtenir la liste complète des composants disponibles, consultez [interfaces WIC](-wic-codec-ifaces.md).</span><span class="sxs-lookup"><span data-stu-id="80b28-156">For a full list of available components, see [WIC interfaces](-wic-codec-ifaces.md).</span></span>



| <span data-ttu-id="80b28-157">Type de composant</span><span class="sxs-lookup"><span data-stu-id="80b28-157">Component Type</span></span>                                                      | <span data-ttu-id="80b28-158">Description</span><span class="sxs-lookup"><span data-stu-id="80b28-158">Description</span></span>                                                                                                   |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="80b28-159">**Bitmap**</span><span class="sxs-lookup"><span data-stu-id="80b28-159">**Bitmap**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)                             | <span data-ttu-id="80b28-160">Représente une représentation en mémoire accessible en écriture d’un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource).</span><span class="sxs-lookup"><span data-stu-id="80b28-160">Represents a writable in-memory representation of an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource).</span></span> |
| [<span data-ttu-id="80b28-161">**Décodeur**</span><span class="sxs-lookup"><span data-stu-id="80b28-161">**Decoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)                     | <span data-ttu-id="80b28-162">Utilisé pour décoder les données d’image d’un flux dans un format utile pour le traitement d’image.</span><span class="sxs-lookup"><span data-stu-id="80b28-162">Used to decode image data from a stream into a format that is useful for image processing.</span></span>                    |
| [<span data-ttu-id="80b28-163">**Codeur**</span><span class="sxs-lookup"><span data-stu-id="80b28-163">**Encoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)                     | <span data-ttu-id="80b28-164">Écrit des données d’image dans un flux.</span><span class="sxs-lookup"><span data-stu-id="80b28-164">Writes image data to a stream.</span></span>                                                                                |
| [<span data-ttu-id="80b28-165">**Stream**</span><span class="sxs-lookup"><span data-stu-id="80b28-165">**Stream**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)                             | <span data-ttu-id="80b28-166">Utilisé pour lire et écrire des données à partir d’un fichier, d’une ressource réseau, d’un bloc de mémoire, etc.</span><span class="sxs-lookup"><span data-stu-id="80b28-166">Used to read and write data from a file, network resource, a block of memory, and so on.</span></span>                      |
| [<span data-ttu-id="80b28-167">**Convertisseur de format**</span><span class="sxs-lookup"><span data-stu-id="80b28-167">**Format Converter**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)          | <span data-ttu-id="80b28-168">Utilisé pour convertir d’un format de pixel à un autre.</span><span class="sxs-lookup"><span data-stu-id="80b28-168">Used to convert from one pixel format to another.</span></span>                                                             |
| [<span data-ttu-id="80b28-169">**Lecteur de requêtes de métadonnées**</span><span class="sxs-lookup"><span data-stu-id="80b28-169">**Metadata Query Reader**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) | <span data-ttu-id="80b28-170">Utilisé pour lire les métadonnées d’une image ou d’un frame d’image.</span><span class="sxs-lookup"><span data-stu-id="80b28-170">Used to read metadata of an image or image frame.</span></span>                                                             |
| [<span data-ttu-id="80b28-171">**Générateur de requêtes de métadonnées**</span><span class="sxs-lookup"><span data-stu-id="80b28-171">**Metadata Query Writer**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) | <span data-ttu-id="80b28-172">Utilisé pour écrire des métadonnées dans une image ou un frame d’image.</span><span class="sxs-lookup"><span data-stu-id="80b28-172">Used to write metadata to an image or image frame.</span></span>                                                            |



 

## <a name="see-also"></a><span data-ttu-id="80b28-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80b28-173">See Also</span></span>

[<span data-ttu-id="80b28-174">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="80b28-174">References</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="80b28-175">Exemples et exemples de code</span><span class="sxs-lookup"><span data-stu-id="80b28-175">Samples and Code Examples</span></span>](-wic-samples.md)


 

 
