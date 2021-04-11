---
description: Cette rubrique présente la configuration requise pour la création de gestionnaires de métadonnées personnalisés pour le composant WIC (Windows Imaging Component), y compris les lecteurs et les enregistreurs de métadonnées.
ms.assetid: 08f1872b-6e4d-44ee-abc7-48685e435acc
title: Vue d’ensemble de l’extensibilité des métadonnées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6576585f7f35628432504086695dd6c64091d3b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203657"
---
# <a name="metadata-extensibility-overview"></a><span data-ttu-id="87b7b-103">Vue d’ensemble de l’extensibilité des métadonnées</span><span class="sxs-lookup"><span data-stu-id="87b7b-103">Metadata Extensibility Overview</span></span>

<span data-ttu-id="87b7b-104">Cette rubrique présente la configuration requise pour la création de gestionnaires de métadonnées personnalisés pour le composant WIC (Windows Imaging Component), y compris les lecteurs et les enregistreurs de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-104">This topic introduces the requirements for creating custom metadata handlers for the Windows Imaging Component (WIC), including both metadata readers and writers.</span></span> <span data-ttu-id="87b7b-105">Il aborde également la configuration requise pour l’extension de la détection des composants runtime WIC pour inclure vos gestionnaires de métadonnées personnalisés.</span><span class="sxs-lookup"><span data-stu-id="87b7b-105">It also discusses the requirements for extending WIC run-time component discovery to include your custom metadata handlers.</span></span>

<span data-ttu-id="87b7b-106">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="87b7b-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="87b7b-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="87b7b-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="87b7b-108">Introduction</span><span class="sxs-lookup"><span data-stu-id="87b7b-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="87b7b-109">Création d’un lecteur de métadonnées</span><span class="sxs-lookup"><span data-stu-id="87b7b-109">Creating a Metadata Reader</span></span>](#creating-a-metadata-reader)
    -   [<span data-ttu-id="87b7b-110">Interface IWICMetadataReader</span><span class="sxs-lookup"><span data-stu-id="87b7b-110">IWICMetadataReader Interface</span></span>](#iwicmetadatareader-interface)
    -   [<span data-ttu-id="87b7b-111">Interface IWICPersistStream</span><span class="sxs-lookup"><span data-stu-id="87b7b-111">IWICPersistStream Interface</span></span>](#iwicpersiststream-interface)
    -   [<span data-ttu-id="87b7b-112">Interface IWICStreamProvider</span><span class="sxs-lookup"><span data-stu-id="87b7b-112">IWICStreamProvider Interface</span></span>](#iwicstreamprovider-interface)
-   [<span data-ttu-id="87b7b-113">Création d’un enregistreur de métadonnées</span><span class="sxs-lookup"><span data-stu-id="87b7b-113">Creating a Metadata Writer</span></span>](#creating-a-metadata-writer)
    -   [<span data-ttu-id="87b7b-114">Interface IWICMetadataWriter</span><span class="sxs-lookup"><span data-stu-id="87b7b-114">IWICMetadataWriter Interface</span></span>](#iwicmetadatawriter-interface)
    -   [<span data-ttu-id="87b7b-115">Interface IWICPersistStream</span><span class="sxs-lookup"><span data-stu-id="87b7b-115">IWICPersistStream Interface</span></span>](#iwicpersiststream-interface)
    -   [<span data-ttu-id="87b7b-116">Interface IWICStreamProvider</span><span class="sxs-lookup"><span data-stu-id="87b7b-116">IWICStreamProvider Interface</span></span>](#iwicstreamprovider-interface)
-   [<span data-ttu-id="87b7b-117">Installation et inscription d’un gestionnaire de métadonnées</span><span class="sxs-lookup"><span data-stu-id="87b7b-117">Installing and Registering a Metadata Handler</span></span>](#installing-and-registering-a-metadata-handler)
    -   [<span data-ttu-id="87b7b-118">Clés de Registre du gestionnaire de métadonnées</span><span class="sxs-lookup"><span data-stu-id="87b7b-118">Metadata Handler Registry Keys</span></span>](#metadata-handler-registry-keys)
    -   [<span data-ttu-id="87b7b-119">Lecteurs de métadonnées</span><span class="sxs-lookup"><span data-stu-id="87b7b-119">Metadata Readers</span></span>](#metadata-readers)
    -   [<span data-ttu-id="87b7b-120">Enregistreurs de métadonnées</span><span class="sxs-lookup"><span data-stu-id="87b7b-120">Metadata Writers</span></span>](#metadata-writers)
    -   [<span data-ttu-id="87b7b-121">Signature d’un gestionnaire de métadonnées</span><span class="sxs-lookup"><span data-stu-id="87b7b-121">Signing a Metadata Handler</span></span>](#signing-a-metadata-handler)
-   [<span data-ttu-id="87b7b-122">Considérations spéciales</span><span class="sxs-lookup"><span data-stu-id="87b7b-122">Special Considerations</span></span>](#special-considerations)
    -   [<span data-ttu-id="87b7b-123">PROPVARIANTS</span><span class="sxs-lookup"><span data-stu-id="87b7b-123">PROPVARIANTS</span></span>](#propvariants)
    -   [<span data-ttu-id="87b7b-124">Gestionnaires 8BIM</span><span class="sxs-lookup"><span data-stu-id="87b7b-124">8BIM Handlers</span></span>](#8bim-handlers)
-   [<span data-ttu-id="87b7b-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="87b7b-125">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="87b7b-126">Prérequis</span><span class="sxs-lookup"><span data-stu-id="87b7b-126">Prerequisites</span></span>

<span data-ttu-id="87b7b-127">Pour comprendre cette rubrique, vous devez avoir une connaissance approfondie de WIC, de ses composants et de ses métadonnées pour les images.</span><span class="sxs-lookup"><span data-stu-id="87b7b-127">To understand this topic you should have an in-depth understanding of WIC, its components, and metadata for images.</span></span> <span data-ttu-id="87b7b-128">Pour plus d’informations sur les métadonnées WIC, consultez [vue d’ensemble des métadonnées WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="87b7b-128">For more information on WIC metadata, see the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="87b7b-129">Pour plus d’informations sur les composants WIC, consultez [vue d’ensemble du composant de création d’images Windows](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="87b7b-129">For more information on WIC components, see the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span>

## <a name="introduction"></a><span data-ttu-id="87b7b-130">Introduction</span><span class="sxs-lookup"><span data-stu-id="87b7b-130">Introduction</span></span>

<span data-ttu-id="87b7b-131">Comme indiqué dans la [vue d’ensemble des métadonnées WIC](-wic-about-metadata.md), il existe souvent plusieurs blocs de métadonnées dans une image, chacun exposant différents types d’informations dans différents formats de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-131">As discussed in the [WIC Metadata Overview](-wic-about-metadata.md), there are often multiple blocks of metadata within an image, each exposing different types of information in different metadata formats.</span></span> <span data-ttu-id="87b7b-132">Pour interagir avec un format de métadonnées incorporé dans une image, une application doit utiliser un gestionnaire de métadonnées approprié.</span><span class="sxs-lookup"><span data-stu-id="87b7b-132">To interact with a metadata format embedded within an image, an application must use an appropriate metadata handler.</span></span> <span data-ttu-id="87b7b-133">WIC fournit plusieurs gestionnaires de métadonnées (les lecteurs et les enregistreurs de métadonnées) qui vous permettent de lire et d’écrire des types de métadonnées spécifiques, tels que EXIF ou XMP.</span><span class="sxs-lookup"><span data-stu-id="87b7b-133">WIC provides several metadata handlers (both metadata readers and writers) that enable you to read and write specific types of metadata such as Exif or XMP.</span></span>

<span data-ttu-id="87b7b-134">Outre les gestionnaires natifs fournis, WIC fournit des API qui vous permettent de créer de nouveaux gestionnaires de métadonnées qui participent à la détection des composants d’exécution de WIC.</span><span class="sxs-lookup"><span data-stu-id="87b7b-134">In addition to the native handlers provided, WIC provides APIs that enable you to create new metadata handlers that participate in WIC's run-time component discovery.</span></span> <span data-ttu-id="87b7b-135">Cela permet aux applications qui utilisent WIC de lire et d’écrire vos formats de métadonnées personnalisés.</span><span class="sxs-lookup"><span data-stu-id="87b7b-135">This enables applications that use WIC to read and write your custom metadata formats.</span></span>

<span data-ttu-id="87b7b-136">Les étapes suivantes permettent à vos gestionnaires de métadonnées de participer à la découverte des métadonnées au moment de l’exécution du WIC.</span><span class="sxs-lookup"><span data-stu-id="87b7b-136">The following steps enable your metadata handlers to participate in WIC's run-time metadata discovery.</span></span>

-   <span data-ttu-id="87b7b-137">Implémentez une classe de gestionnaire de lecteur de métadonnées ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) qui expose les interfaces WIC requises pour lire votre format de métadonnées personnalisé.</span><span class="sxs-lookup"><span data-stu-id="87b7b-137">Implement a metadata-reader handler class ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) that exposes the required WIC interfaces for reading your custom metadata format.</span></span> <span data-ttu-id="87b7b-138">Cela permet aux applications WIC de lire votre format de métadonnées de la même façon qu’elles lisent des formats de métadonnées natifs.</span><span class="sxs-lookup"><span data-stu-id="87b7b-138">This enables WIC-based applications to read your metadata format the same way they read native metadata formats.</span></span>
-   <span data-ttu-id="87b7b-139">Implémentez une classe de gestionnaire d’écriture de métadonnées ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) qui expose les interfaces WIC requises pour l’encodage de votre format de métadonnées personnalisé.</span><span class="sxs-lookup"><span data-stu-id="87b7b-139">Implement a metadata-writer handler class ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) that exposes the required WIC interfaces for encoding your custom metadata format.</span></span> <span data-ttu-id="87b7b-140">Cela permet aux applications basées sur WIC de sérialiser votre format de métadonnées dans des formats d’image pris en charge.</span><span class="sxs-lookup"><span data-stu-id="87b7b-140">This enables WIC-based applications to serialize your metadata format into supported image formats.</span></span>
-   <span data-ttu-id="87b7b-141">Signez et inscrivez numériquement vos gestionnaires de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-141">Digitally sign and register your metadata handlers.</span></span> <span data-ttu-id="87b7b-142">Cela permet de découvrir vos gestionnaires de métadonnées au moment de l’exécution en faisant correspondre le modèle d’identification dans le Registre avec le modèle incorporé dans le fichier image.</span><span class="sxs-lookup"><span data-stu-id="87b7b-142">This enables your metadata handlers to be discovered at run time by matching the identifying pattern in the registry with the pattern embedded in the image file.</span></span>

## <a name="creating-a-metadata-reader"></a><span data-ttu-id="87b7b-143">Création d’un lecteur de métadonnées</span><span class="sxs-lookup"><span data-stu-id="87b7b-143">Creating a Metadata Reader</span></span>

<span data-ttu-id="87b7b-144">Le principal accès aux blocs de métadonnées au sein d’un codec s’effectue via l’interface [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) que chaque codec WIC implémente.</span><span class="sxs-lookup"><span data-stu-id="87b7b-144">The main access to metadata blocks within a codec is through the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) interface that each WIC codec implements.</span></span> <span data-ttu-id="87b7b-145">Cette interface énumère chacun des blocs de métadonnées incorporés dans un format d’image afin que le gestionnaire de métadonnées approprié puisse être découvert et instancié pour chaque bloc.</span><span class="sxs-lookup"><span data-stu-id="87b7b-145">This interface enumerates each of the metadata blocks embedded in an image format so that the appropriate metadata handler can be discovered and instantiated for each block.</span></span> <span data-ttu-id="87b7b-146">Les blocs de métadonnées qui ne sont pas reconnus par WIC sont considérés comme inconnus et sont définis en tant que GUID CLSID \_ WICUnknownMetadataReader.</span><span class="sxs-lookup"><span data-stu-id="87b7b-146">The metadata blocks that are not recognized by WIC are considered unknown and are defined as the GUID CLSID\_WICUnknownMetadataReader.</span></span> <span data-ttu-id="87b7b-147">Pour que votre format de métadonnées soit reconnu par WIC, vous devez créer une classe qui implémente trois interfaces : [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)et [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span><span class="sxs-lookup"><span data-stu-id="87b7b-147">To have your metadata format recognized by WIC, you must create a class that implements three interfaces: [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream), and [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span></span>

> [!Note]  
> <span data-ttu-id="87b7b-148">Si votre format de métadonnées a des restrictions qui rendent certaines méthodes des interfaces requises inappropriées, ces méthodes doivent retourner WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.</span><span class="sxs-lookup"><span data-stu-id="87b7b-148">If your metadata format has restrictions that render some methods of the required interfaces inappropriate, such methods should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

 

### <a name="iwicmetadatareader-interface"></a><span data-ttu-id="87b7b-149">Interface IWICMetadataReader</span><span class="sxs-lookup"><span data-stu-id="87b7b-149">IWICMetadataReader Interface</span></span>

<span data-ttu-id="87b7b-150">L’interface [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) doit être implémentée lors de la création d’un lecteur de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-150">The [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) interface must be implemented when creating a metadata reader.</span></span> <span data-ttu-id="87b7b-151">Cette interface fournit l’accès aux éléments de métadonnées sous-comprises dans le flux de données d’un format de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-151">This interface provides access to the underling metadata items within the data stream of a metadata format.</span></span>

<span data-ttu-id="87b7b-152">Le code suivant illustre la définition de l’interface du lecteur de métadonnées telle que définie dans le fichier wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="87b7b-152">The following code shows the definition of the metadata reader interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICMetadataReader : IUnknown
{
    HRESULT GetMetadataFormat(
        [out] GUID *pguidMetadataFormat
        );

    HRESULT GetMetadataHandlerInfo(
        [out] IWICMetadataHandlerInfo **ppIHandler
        );

    HRESULT GetCount(
        [out] UINT *pcCount
        );

    HRESULT GetValueByIndex(
        [in] UINT nIndex,
        [in, out, unique] PROPVARIANT *pvarSchema,
        [in, out, unique] PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetEnumerator(
        [out] IWICEnumMetadataItem **ppIEnumMetadata
        );
};
```

<span data-ttu-id="87b7b-153">La méthode **GetMetadataFormat** retourne le GUID de votre format de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-153">The **GetMetadataFormat** method returns the GUID of your metadata format.</span></span>

<span data-ttu-id="87b7b-154">La méthode **GetMetadataHandlerInfo** retourne une interface [**IWICMetadataHandlerInfo**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo) qui fournit des informations sur votre gestionnaire de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-154">The **GetMetadataHandlerInfo** method returns an [**IWICMetadataHandlerInfo**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo) interface that provides information about your metadata handler.</span></span> <span data-ttu-id="87b7b-155">Cela comprend des informations telles que les formats d’image qui prennent en charge le format de métadonnées et si votre lecteur de métadonnées requiert l’accès au flux de métadonnées complet.</span><span class="sxs-lookup"><span data-stu-id="87b7b-155">This includes information such as what image formats support the metadata format and whether your metadata reader requires access to the full metadata stream.</span></span>

<span data-ttu-id="87b7b-156">La méthode **GetCount** retourne le nombre d’éléments de métadonnées individuels (y compris les blocs de métadonnées incorporés) trouvés dans le flux de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-156">The **GetCount** method returns the number of individual metadata items (including embedded metadata blocks) found within the metadata stream.</span></span>

<span data-ttu-id="87b7b-157">La méthode **GetValueByIndex** retourne un élément de métadonnées par une valeur d’index.</span><span class="sxs-lookup"><span data-stu-id="87b7b-157">The **GetValueByIndex** method returns a metadata item by an index value.</span></span> <span data-ttu-id="87b7b-158">Cette méthode permet aux applications de parcourir chaque élément de métadonnées dans un bloc de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-158">This method enables applications to loop through each metadata item in a metadata block.</span></span> <span data-ttu-id="87b7b-159">Le code suivant montre comment une application peut utiliser cette méthode pour récupérer chaque élément de métadonnées dans un bloc de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-159">The following code demonstrates how an application can use this method to retrieve each metadata item in a metadata block.</span></span>


```C++
PROPVARIANT readerValue;
IWICMetadataBlockReader *blockReader = NULL;
IWICMetadataReader *reader = NULL;

PropVariantInit(&readerValue);

hr = pFrameDecode->QueryInterface(IID_IWICMetadataBlockReader, (void**)&blockReader);

if (SUCCEEDED(hr))
{
    // Retrieve the third block in the image. This is image specific and
    // ideally you should call this by retrieving the reader count
    // first.
    hr = blockReader->GetReaderByIndex(2, &reader);
}

if (SUCCEEDED(hr))
{
    UINT numValues = 0;

    hr = reader->GetCount(&numValues);

    // Loop through each item and retrieve by index
    for (UINT i = 0; SUCCEEDED(hr) && i < numValues; i++)
    {
        PROPVARIANT id, value;

        PropVariantInit(&id);
        PropVariantInit(&value);

        hr = reader->GetValueByIndex(i, NULL, &id, &value);

        if (SUCCEEDED(hr))
        {
            // Do something with the metadata item.
            //...
        }
        PropVariantClear(&id);
        PropVariantClear(&value);
    }               
}
```



<span data-ttu-id="87b7b-160">La méthode **GetValue** récupère un élément de métadonnées spécifique par schéma et/ou ID.</span><span class="sxs-lookup"><span data-stu-id="87b7b-160">The **GetValue** method retrieves a specific metadata item by schema and/or ID.</span></span> <span data-ttu-id="87b7b-161">Cette méthode est similaire à la méthode **GetValueByIndex** , à ceci près qu’elle récupère un élément de métadonnées ayant un schéma ou un ID spécifique.</span><span class="sxs-lookup"><span data-stu-id="87b7b-161">This method is similar to the **GetValueByIndex** method except that it retrieves a metadata item that has a specific schema or ID.</span></span>

<span data-ttu-id="87b7b-162">La méthode **GetEnumerator** retourne un énumérateur de chaque élément de métadonnées dans le bloc de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-162">The **GetEnumerator** method returns an enumerator of each metadata item in the metadata block.</span></span> <span data-ttu-id="87b7b-163">Cela permet aux applications d’utiliser un énumérateur pour naviguer dans votre format de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-163">This enables applications to use an enumerator to navigate your metadata format.</span></span>

<span data-ttu-id="87b7b-164">Si votre format de métadonnées n’a pas de notion de schémas pour les éléments de métadonnées, le GetValue... les méthodes doivent ignorer cette propriété.</span><span class="sxs-lookup"><span data-stu-id="87b7b-164">If your metadata format does not have a notion of schemas for metadata items, the GetValue... methods should ignore this property.</span></span> <span data-ttu-id="87b7b-165">Toutefois, si votre format prend en charge les noms de schéma, vous devez anticiper une valeur **null** .</span><span class="sxs-lookup"><span data-stu-id="87b7b-165">If, however, your format supports schema naming, you should anticipate a **NULL** value.</span></span>

<span data-ttu-id="87b7b-166">Si un élément de métadonnées est un bloc de métadonnées incorporé, créez un gestionnaire de métadonnées à partir du sous-flux du contenu incorporé et retournez le nouveau gestionnaire de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-166">If a metadata item is an embedded metadata block, create a metadata handler from the substream of the embedded content and return the new metadata handler.</span></span> <span data-ttu-id="87b7b-167">Si aucun lecteur de métadonnées n’est disponible pour le bloc imbriqué, instanciez et retournez un lecteur de métadonnées inconnu.</span><span class="sxs-lookup"><span data-stu-id="87b7b-167">If there is no metadata reader available for the nested block, instantiate and return an unknown metadata reader.</span></span> <span data-ttu-id="87b7b-168">Pour créer un lecteur de métadonnées pour le bloc incorporé, appelez les méthodes **CreateMetadataReaderFromContainer** ou **CreateMetadataReader** de la fabrique de composants, ou appelez la fonction [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent) .</span><span class="sxs-lookup"><span data-stu-id="87b7b-168">To create a new metadata reader for the embedded block, call the component factory's **CreateMetadataReaderFromContainer** or **CreateMetadataReader** methods, or call the [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent) function.</span></span>

<span data-ttu-id="87b7b-169">Si le flux de métadonnées contient du contenu de poids fort (Big-endian), le lecteur de métadonnées est responsable de la permutation des valeurs de données qu’il traite.</span><span class="sxs-lookup"><span data-stu-id="87b7b-169">If the metadata stream contains big-endian content, the metadata reader is responsible for swapping any data values it processes.</span></span> <span data-ttu-id="87b7b-170">Il est également chargé d’informer les lecteurs de métadonnées imbriqués qu’ils utilisent le flux de données Big-endian.</span><span class="sxs-lookup"><span data-stu-id="87b7b-170">It is also responsible for informing any nested metadata readers that they are working with big-endian data stream.</span></span> <span data-ttu-id="87b7b-171">Toutefois, toutes les valeurs doivent être retournées au format Little endian.</span><span class="sxs-lookup"><span data-stu-id="87b7b-171">However, all values should be returned in little-endian format.</span></span>

<span data-ttu-id="87b7b-172">Implémentez la prise en charge de la navigation dans les espaces de noms en prenant en charge les requêtes où l’ID d’élément de métadonnées est un `VT_CLSID` (Guid) correspondant à un format de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-172">Implement support for namespace navigation by supporting queries where the metadata item ID is a `VT_CLSID` (a GUID) corresponding to a metadata format.</span></span> <span data-ttu-id="87b7b-173">Si un lecteur de métadonnées imbriqué pour ce format est identifié lors de l’analyse, il doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="87b7b-173">If a nested metadata reader for that format is identified during parsing, it must be returned.</span></span> <span data-ttu-id="87b7b-174">Cela permet aux applications d’utiliser un lecteur de requêtes de métadonnées pour rechercher votre format de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-174">This enables applications to use a metadata query reader to search your metadata format.</span></span>

<span data-ttu-id="87b7b-175">Lors de l’obtention d’un élément de métadonnées par ID, vous devez utiliser la [fonction PropVariantChangeType](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) pour forcer l’ID dans le type attendu.</span><span class="sxs-lookup"><span data-stu-id="87b7b-175">When getting a metadata item by ID, you should use [PropVariantChangeType Function](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) to coerce the ID into the expected type.</span></span> <span data-ttu-id="87b7b-176">Par exemple, le lecteur IFD convertit un ID en type `VT_UI2` pour qu’il coïncide avec le type de données d’un ID de balise IFD UShort.</span><span class="sxs-lookup"><span data-stu-id="87b7b-176">For example, the IFD reader will coerce an ID to type `VT_UI2` to coincide with the data type of an IFD tag ID USHORT.</span></span> <span data-ttu-id="87b7b-177">Le type d’entrée et le type attendu doivent tous deux être [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) pour ce faire.</span><span class="sxs-lookup"><span data-stu-id="87b7b-177">The input type and expected type must both be [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) to do this.</span></span> <span data-ttu-id="87b7b-178">Ce n’est pas obligatoire, mais cette contrainte simplifie le code qui appelle le lecteur pour rechercher des éléments de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-178">This is not required, but doing this coercion simplifies code that calls the reader to query for metadata items.</span></span>

### <a name="iwicpersiststream-interface"></a><span data-ttu-id="87b7b-179">Interface IWICPersistStream</span><span class="sxs-lookup"><span data-stu-id="87b7b-179">IWICPersistStream Interface</span></span>

<span data-ttu-id="87b7b-180">L’interface [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) hérite de **IPersistStream** et fournit des méthodes supplémentaires pour l’enregistrement et le chargement d’objets à l’aide de l’énumération [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .</span><span class="sxs-lookup"><span data-stu-id="87b7b-180">The [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface inherits from **IPersistStream** and provides additional methods for saving and loading objects by using the [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) enumeration.</span></span>

<span data-ttu-id="87b7b-181">Le code suivant illustre la définition de l’interface [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) comme défini dans le fichier wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="87b7b-181">The following code shows the definition of the [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

<span data-ttu-id="87b7b-182">La méthode **LoadEx** fournit à votre lecteur de métadonnées un flux de données contenant votre bloc de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-182">The **LoadEx** method provides your metadata reader with a data stream containing your metadata block.</span></span> <span data-ttu-id="87b7b-183">Votre lecteur analyse ce flux pour accéder aux éléments de métadonnées sous-jacents.</span><span class="sxs-lookup"><span data-stu-id="87b7b-183">Your reader parses this stream to access the underlying metadata items.</span></span> <span data-ttu-id="87b7b-184">Votre lecteur de métadonnées est initialisé avec un sous-flux positionné au début du contenu de métadonnées brutes.</span><span class="sxs-lookup"><span data-stu-id="87b7b-184">Your metadata reader is initialized with a substream that is positioned at the beginning of the raw metadata content.</span></span> <span data-ttu-id="87b7b-185">Si votre lecteur ne requiert pas le flux complet, le sous-flux est limité dans la plage au contenu du bloc de métadonnées ; dans le cas contraire, le flux de métadonnées complet est fourni avec la position définie au début de votre bloc de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-185">If your reader does not require the full stream, the substream is limited in range to only the content of the metadata block; otherwise, the full metadata stream is provided with the position set at the beginning of your metadata block.</span></span>

<span data-ttu-id="87b7b-186">La méthode **SaveEx** est utilisée par les enregistreurs de métadonnées pour sérialiser votre bloc de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-186">The **SaveEx** method is used by metadata writers to serialize your metadata block.</span></span> <span data-ttu-id="87b7b-187">Quand **SaveEx** est utilisé dans un lecteur de métadonnées, il doit retourner WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.</span><span class="sxs-lookup"><span data-stu-id="87b7b-187">When **SaveEx** is used in a metadata reader, it should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

### <a name="iwicstreamprovider-interface"></a><span data-ttu-id="87b7b-188">Interface IWICStreamProvider</span><span class="sxs-lookup"><span data-stu-id="87b7b-188">IWICStreamProvider Interface</span></span>

<span data-ttu-id="87b7b-189">L’interface [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) permet à votre lecteur de métadonnées de fournir des références à son flux de contenu, de fournir des informations sur le flux et d’actualiser les versions mises en cache du flux.</span><span class="sxs-lookup"><span data-stu-id="87b7b-189">The [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) interface enables your metadata reader to provide references to its content stream, provide information about the stream, and refresh cached versions of the stream.</span></span>

<span data-ttu-id="87b7b-190">Le code suivant illustre la définition de l’interface [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) comme défini dans le fichier wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="87b7b-190">The following code shows the definition of the [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICStreamProvider : IUnknown
{
    HRESULT GetStream(
        [out] IStream **ppIStream
        );

    HRESULT GetPersistOptions(
        [out] DWORD *pdwPersistOptions
        );

    HRESULT GetPreferredVendorGUID(
        [out] GUID *pguidPreferredVendor
        );

    HRESULT RefreshStream(
        );
};
```

<span data-ttu-id="87b7b-191">La méthode **GetStream** récupère une référence à votre flux de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-191">The **GetStream** method retrieves a reference to your metadata stream.</span></span> <span data-ttu-id="87b7b-192">Le point de départ du flux que vous renvoyez doit être réinitialisé à la position de début.</span><span class="sxs-lookup"><span data-stu-id="87b7b-192">The stream you return should have the stream pointer reset to the start position.</span></span> <span data-ttu-id="87b7b-193">Si votre format de métadonnées requiert un accès complet au flux, la position de départ doit être le début de votre bloc de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-193">If your metadata format requires full stream access, the start position should be the start of your metadata block.</span></span>

<span data-ttu-id="87b7b-194">La méthode **GetPersistOptions** retourne les options actuelles du flux à partir de l’énumération [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .</span><span class="sxs-lookup"><span data-stu-id="87b7b-194">The **GetPersistOptions** method returns the stream's current options from the [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) enumeration.</span></span>

<span data-ttu-id="87b7b-195">La méthode **GetPreferredVendorGUID** retourne le GUID du fournisseur du lecteur de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-195">The **GetPreferredVendorGUID** method returns the GUID of the vendor of the metadata reader.</span></span>

<span data-ttu-id="87b7b-196">La méthode **RefreshStream** actualise le flux de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-196">The **RefreshStream** method refreshes the metadata stream.</span></span> <span data-ttu-id="87b7b-197">Cette méthode doit appeler **LoadEx** avec un flux **null** pour tous les blocs de métadonnées imbriqués.</span><span class="sxs-lookup"><span data-stu-id="87b7b-197">This method must call **LoadEx** with a **NULL** stream for any nested metadata blocks.</span></span> <span data-ttu-id="87b7b-198">Cela est nécessaire, car les blocs de métadonnées imbriqués et leurs éléments peuvent ne plus exister, en raison de la modification sur place.</span><span class="sxs-lookup"><span data-stu-id="87b7b-198">This is necessary because nested metadata blocks and their items may no longer exist, due to in-place editing.</span></span>

## <a name="creating-a-metadata-writer"></a><span data-ttu-id="87b7b-199">Création d’un enregistreur de métadonnées</span><span class="sxs-lookup"><span data-stu-id="87b7b-199">Creating a Metadata Writer</span></span>

<span data-ttu-id="87b7b-200">Un enregistreur de métadonnées est un type de gestionnaire de métadonnées qui fournit un moyen de sérialiser un bloc de métadonnées vers une image, ou à l’extérieur d’un frame individuel si le format d’image le prend en charge.</span><span class="sxs-lookup"><span data-stu-id="87b7b-200">A metadata writer is a type of metadata handler that provides a way to serialize a metadata block to an image frame, or outside an individual frame if the image format supports it.</span></span> <span data-ttu-id="87b7b-201">L’accès principal aux enregistreurs de métadonnées au sein d’un codec s’effectue par le biais de l’interface [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) que chaque encodeur WIC implémente.</span><span class="sxs-lookup"><span data-stu-id="87b7b-201">The main access to the metadata writers within a codec is through the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) interface that each WIC encoder implements.</span></span> <span data-ttu-id="87b7b-202">Cette interface permet aux applications d’énumérer chacun des blocs de métadonnées incorporés dans une image afin que le writer de métadonnées approprié puisse être découvert et instancié pour chaque bloc de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-202">This interface enables applications to enumerate each of the metadata blocks embedded in an image so that the appropriate metadata writer can be discovered and instantiated for each metadata block.</span></span> <span data-ttu-id="87b7b-203">Les blocs de métadonnées qui n’ont pas de writer de métadonnées correspondant sont considérés comme inconnus et sont définis en tant que GUID CLSID \_ WICUnknownMetadataReader.</span><span class="sxs-lookup"><span data-stu-id="87b7b-203">Metadata blocks that do not have a corresponding metadata writer are considered unknown, and are defined as the GUID CLSID\_WICUnknownMetadataReader.</span></span> <span data-ttu-id="87b7b-204">Pour permettre aux applications compatibles WIC de sérialiser et d’écrire votre format de métadonnées, vous devez créer une classe qui implémente les interfaces suivantes : [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter), [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)et [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span><span class="sxs-lookup"><span data-stu-id="87b7b-204">To enable WIC enabled applications to serialize and write your metadata format, you must create a class that implements the following interfaces: [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter), [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream), and [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span></span>

> [!Note]  
> <span data-ttu-id="87b7b-205">Si votre format de métadonnées a des restrictions qui rendent certaines méthodes des interfaces requises inappropriées, ces méthodes doivent retourner WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.</span><span class="sxs-lookup"><span data-stu-id="87b7b-205">If your metadata format has restrictions that render some methods of the required interfaces inappropriate, such methods should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

 

### <a name="iwicmetadatawriter-interface"></a><span data-ttu-id="87b7b-206">Interface IWICMetadataWriter</span><span class="sxs-lookup"><span data-stu-id="87b7b-206">IWICMetadataWriter Interface</span></span>

<span data-ttu-id="87b7b-207">L’interface [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) doit être implémentée par votre générateur de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-207">The [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) interface must be implemented by your metadata writer.</span></span> <span data-ttu-id="87b7b-208">En outre, étant donné que **IWICMetadataWriter** hérite de [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), vous devez également implémenter toutes les méthodes de **IWICMetadataReader**.</span><span class="sxs-lookup"><span data-stu-id="87b7b-208">Additionally, because **IWICMetadataWriter** inherits from [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), you must also implement all the methods of **IWICMetadataReader**.</span></span> <span data-ttu-id="87b7b-209">Étant donné que les deux types de gestionnaires nécessitent le même héritage d’interface, vous pouvez créer une seule classe qui fournit des fonctionnalités de lecture et d’écriture.</span><span class="sxs-lookup"><span data-stu-id="87b7b-209">Because both handler types require the same interface inheritance, you might want to create a single class that provides both reading and writing functionality.</span></span>

<span data-ttu-id="87b7b-210">Le code suivant illustre la définition de l’interface du writer de métadonnées telle que définie dans le fichier wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="87b7b-210">The following code shows the definition of the metadata writer interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICMetadataWriter : IWICMetadataReader
{
    HRESULT SetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT SetValueByIndex(
        [in] UINT nIndex,
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT RemoveValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId
        );

    HRESULT RemoveValueByIndex(
        [in] UINT nIndex
        );
};
```

<span data-ttu-id="87b7b-211">La méthode **SetValue** écrit l’élément de métadonnées spécifié dans le flux de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-211">The **SetValue** method writes the specified metadata item to the metadata stream.</span></span>

<span data-ttu-id="87b7b-212">La méthode **SetValueByIndex** écrit l’élément de métadonnées spécifié dans l’index spécifié dans le flux de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-212">The **SetValueByIndex** method writes the specified metadata item to the specified index in the metadata stream.</span></span> <span data-ttu-id="87b7b-213">L’index ne fait pas référence à l’ID, mais à la position de l’élément dans le bloc de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-213">The index does not refer to the ID but to the position of the item within the metadata block.</span></span>

<span data-ttu-id="87b7b-214">La méthode **RemoveValue** supprime l’élément de métadonnées spécifié du flux de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-214">The **RemoveValue** method removes the specified metadata item from the metadata stream.</span></span>

<span data-ttu-id="87b7b-215">La méthode **RemoveValueByIndex** supprime l’élément de métadonnées au niveau de l’index spécifié du flux de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-215">The **RemoveValueByIndex** method removes the metadata item at the specified index from the metadata stream.</span></span> <span data-ttu-id="87b7b-216">Après la suppression d’un élément, il est prévu que les éléments de métadonnées restants occupent l’index libéré si l’index n’est pas le dernier index.</span><span class="sxs-lookup"><span data-stu-id="87b7b-216">After removing an item, it is expected that the remaining metadata items will occupy the vacated index if the index is not the last index.</span></span> <span data-ttu-id="87b7b-217">Il est également prévu que le nombre change une fois que l’élément a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="87b7b-217">It is also expected that the count will change after the item is removed.</span></span>

<span data-ttu-id="87b7b-218">Le générateur de métadonnées est chargé de convertir les éléments [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) en structure sous-jacente requise par votre format.</span><span class="sxs-lookup"><span data-stu-id="87b7b-218">It is the metadata writer's responsibility to convert the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) items to the underlying structure required by your format.</span></span> <span data-ttu-id="87b7b-219">Toutefois, à la différence du lecteur de métadonnées, les types VARIANT ne doivent normalement pas être forcés à des types différents, car l’appelant indique spécifiquement le type de données à utiliser.</span><span class="sxs-lookup"><span data-stu-id="87b7b-219">However, unlike the metadata reader, VARIANT types should not normally be coerced to different types as the caller is specifically indicating what data type to use.</span></span>

<span data-ttu-id="87b7b-220">Votre enregistreur de métadonnées doit valider tous les éléments de métadonnées dans le flux d’image, y compris les valeurs masquées ou non reconnues.</span><span class="sxs-lookup"><span data-stu-id="87b7b-220">Your metadata writer must commit all metadata items to the image stream, including hidden or unrecognized values.</span></span> <span data-ttu-id="87b7b-221">Cela comprend les blocs de métadonnées imbriqués inconnus.</span><span class="sxs-lookup"><span data-stu-id="87b7b-221">This includes unknown nested metadata blocks.</span></span> <span data-ttu-id="87b7b-222">Toutefois, il incombe à l’encodeur de définir tous les éléments de métadonnées critiques avant de lancer l’opération d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="87b7b-222">However, it is the encoder's responsibility to set any critical metadata items prior to initiating the save operation.</span></span>

<span data-ttu-id="87b7b-223">Si le flux de métadonnées contient du contenu de poids fort, le générateur de métadonnées est responsable de la permutation des valeurs de données qu’il traite.</span><span class="sxs-lookup"><span data-stu-id="87b7b-223">If the metadata stream contains big-endian content, the metadata writer is responsible for swapping any data values it processes.</span></span> <span data-ttu-id="87b7b-224">Il est également chargé d’informer tous les enregistreurs de métadonnées imbriqués qu’ils utilisent un flux de données Big-endian lorsqu’ils sont enregistrés.</span><span class="sxs-lookup"><span data-stu-id="87b7b-224">It is also responsible for informing any nested metadata writers that they are working with a big-endian data stream when they save.</span></span>

<span data-ttu-id="87b7b-225">Implémentez la prise en charge de la création et de la suppression des espaces de noms en prenant en charge les opérations Set et Remove sur les éléments de métadonnées avec un type `VT_CLSID` (Guid) correspondant à un format de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-225">Implement support for namespace creation and removal by supporting set and remove operations on metadata items with a type of `VT_CLSID` (a GUID) corresponding to a metadata format.</span></span> <span data-ttu-id="87b7b-226">Le générateur de métadonnées appelle la fonction [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) pour incorporer correctement le contenu du générateur de métadonnées imbriqué dans le writer de métadonnées parent.</span><span class="sxs-lookup"><span data-stu-id="87b7b-226">The metadata writer calls the [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) function to properly embed the nested metadata writer content into the parent metadata writer.</span></span>

<span data-ttu-id="87b7b-227">Si votre format de métadonnées prend en charge l’encodage sur place, vous êtes chargé de gérer le remplissage requis.</span><span class="sxs-lookup"><span data-stu-id="87b7b-227">If your metadata format supports in-place encoding, you are responsible for managing the required padding.</span></span> <span data-ttu-id="87b7b-228">Pour plus d’informations sur l’encodage sur place, consultez [vue d’ensemble des métadonnées WIC](-wic-about-metadata.md) et [vue d’ensemble de la lecture et de l’écriture des métadonnées d’image](-wic-codec-readingwritingmetadata.md).</span><span class="sxs-lookup"><span data-stu-id="87b7b-228">For more information on in-place encoding, see [WIC Metadata Overview](-wic-about-metadata.md) and [Overview of Reading and Writing Image Metadata](-wic-codec-readingwritingmetadata.md).</span></span>

### <a name="iwicpersiststream-interface"></a><span data-ttu-id="87b7b-229">Interface IWICPersistStream</span><span class="sxs-lookup"><span data-stu-id="87b7b-229">IWICPersistStream Interface</span></span>

<span data-ttu-id="87b7b-230">L’interface [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) hérite de **IPersistStream** et fournit des méthodes supplémentaires pour l’enregistrement et le chargement d’objets à l’aide de l’énumération [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .</span><span class="sxs-lookup"><span data-stu-id="87b7b-230">The [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface inherits from **IPersistStream** and provides additional methods for saving and loading objects by using the [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) enumeration.</span></span>

<span data-ttu-id="87b7b-231">Le code suivant illustre la définition de l’interface [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) comme défini dans le fichier wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="87b7b-231">The following code shows the definition of the [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

<span data-ttu-id="87b7b-232">La méthode **LoadEx** fournit votre gestionnaire de métadonnées avec un flux de données contenant votre bloc de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-232">The **LoadEx** method provides your metadata handler with a data stream containing your metadata block.</span></span>

<span data-ttu-id="87b7b-233">La méthode **SaveEx** sérialise les métadonnées dans un flux.</span><span class="sxs-lookup"><span data-stu-id="87b7b-233">The **SaveEx** method serializes the metadata into a stream.</span></span> <span data-ttu-id="87b7b-234">Si le flux fourni est le même que le flux d’initialisation, vous devez effectuer un encodage sur place.</span><span class="sxs-lookup"><span data-stu-id="87b7b-234">If the provided stream is the same as initialization stream, you should perform in-place encoding.</span></span> <span data-ttu-id="87b7b-235">Si l’encodage sur place est pris en charge, cette méthode doit retourner WINCODEC \_ Err \_ TOOMUCHMETADATA lorsque le remplissage est insuffisant pour effectuer un encodage sur place.</span><span class="sxs-lookup"><span data-stu-id="87b7b-235">If in-place encoding is supported, this method should return WINCODEC\_ERR\_TOOMUCHMETADATA when there is insufficient padding to perform in-place encoding.</span></span> <span data-ttu-id="87b7b-236">Si l’encodage sur place n’est pas pris en charge, cette méthode doit retourner WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.</span><span class="sxs-lookup"><span data-stu-id="87b7b-236">If in-place encoding is not supported, this method should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

<span data-ttu-id="87b7b-237">La méthode **IPersistStream :: GetSizeMax** doit être implémentée et doit retourner la taille exacte du contenu des métadonnées qui serait écrit lors de l’enregistrement suivant.</span><span class="sxs-lookup"><span data-stu-id="87b7b-237">The **IPersistStream::GetSizeMax** method must be implemented and must return the exact size of the metadata content that would be written in subsequent save.</span></span>

<span data-ttu-id="87b7b-238">La méthode **IPersistStream :: IsDirty** doit être implémentée si le writer de métadonnées est initialisé par le biais d’un flux, afin qu’une image puisse déterminer de manière fiable si son contenu a changé.</span><span class="sxs-lookup"><span data-stu-id="87b7b-238">The **IPersistStream::IsDirty** method should be implemented if the metadata writer is initialized through a stream, so that an image can reliably determine whether its content has changed.</span></span>

<span data-ttu-id="87b7b-239">Si votre format de métadonnées prend en charge les blocs de métadonnées imbriqués, votre générateur de métadonnées doit déléguer aux rédacteurs de métadonnées imbriqués la sérialisation de son contenu lors de l’enregistrement dans un flux.</span><span class="sxs-lookup"><span data-stu-id="87b7b-239">If your metadata format supports nested metadata blocks, your metadata writer should delegate to the nested metadata writers the serializing of its content when saving to a stream.</span></span>

### <a name="iwicstreamprovider-interface"></a><span data-ttu-id="87b7b-240">Interface IWICStreamProvider</span><span class="sxs-lookup"><span data-stu-id="87b7b-240">IWICStreamProvider Interface</span></span>

<span data-ttu-id="87b7b-241">L’implémentation de l’interface [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) pour un générateur de métadonnées est identique à celle d’un lecteur de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-241">The implementation of the [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) interface for a metadata writer is the same as that of a metadata reader.</span></span> <span data-ttu-id="87b7b-242">Pour plus d’informations, consultez la section création d’un lecteur de métadonnées dans ce document.</span><span class="sxs-lookup"><span data-stu-id="87b7b-242">For more information, see Creating a Metadata Reader section in this document.</span></span>

## <a name="installing-and-registering-a-metadata-handler"></a><span data-ttu-id="87b7b-243">Installation et inscription d’un gestionnaire de métadonnées</span><span class="sxs-lookup"><span data-stu-id="87b7b-243">Installing and Registering a Metadata Handler</span></span>

<span data-ttu-id="87b7b-244">Pour installer un gestionnaire de métadonnées, vous devez fournir l’assembly du gestionnaire et l’inscrire dans le registre système.</span><span class="sxs-lookup"><span data-stu-id="87b7b-244">To install a metadata handler, you must provide the handler assembly and register it in the system registry.</span></span> <span data-ttu-id="87b7b-245">Vous pouvez choisir le mode et le moment de remplissage des clés de registre.</span><span class="sxs-lookup"><span data-stu-id="87b7b-245">You can decide how and when the registry keys are populated.</span></span>

> [!Note]  
> <span data-ttu-id="87b7b-246">Pour des raisons de lisibilité, les GUID hexadécimaux réels ne sont pas affichés dans les clés de registre indiquées dans les sections suivantes de ce document.</span><span class="sxs-lookup"><span data-stu-id="87b7b-246">For readability, the actual hexadecimal GUIDs are not shown in the registry keys shown in the following sections of this document.</span></span> <span data-ttu-id="87b7b-247">Pour rechercher la valeur hexadécimale d’un nom convivial spécifié, consultez les fichiers wincodec. idl et wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="87b7b-247">To find the hexadecimal value for a specified friendly name, see the wincodec.idl and wincodecsdk.idl files.</span></span>

 

### <a name="metadata-handler-registry-keys"></a><span data-ttu-id="87b7b-248">Clés de Registre du gestionnaire de métadonnées</span><span class="sxs-lookup"><span data-stu-id="87b7b-248">Metadata Handler Registry Keys</span></span>

<span data-ttu-id="87b7b-249">Chaque gestionnaire de métadonnées est identifié par un CLSID unique, et chaque gestionnaire est requis pour inscrire son CLSID sous le GUID de l’ID de catégorie du gestionnaire de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-249">Each metadata handler is identified by a unique CLSID, and each handler is required to register its CLSID under the metadata handler's category ID GUID.</span></span> <span data-ttu-id="87b7b-250">L’ID de catégorie de chaque type de gestionnaire est défini dans wincodec. idl ; le nom d’ID de catégorie pour Readers est CATID \_ WICMetadataReader et le nom d’ID de catégorie pour les Writers est CATID \_ WICMetadataWriter.</span><span class="sxs-lookup"><span data-stu-id="87b7b-250">Each handler type's category ID is defined in the wincodec.idl; the category ID name for readers is CATID\_WICMetadataReader, and the category ID name for writers is CATID\_WICMetadataWriter.</span></span>

<span data-ttu-id="87b7b-251">Chaque gestionnaire de métadonnées est identifié par un CLSID unique, et chaque gestionnaire est requis pour inscrire son CLSID sous le GUID de l’ID de catégorie du gestionnaire de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-251">Each metadata handler is identified by a unique CLSID, and each handler is required to register its CLSID under the metadata handler's category ID GUID.</span></span> <span data-ttu-id="87b7b-252">L’ID de catégorie de chaque type de gestionnaire est défini dans wincodec. idl ; le nom d’ID de catégorie pour Readers est CATID \_ WICMetadataReader et le nom d’ID de catégorie pour les Writers est CATID \_ WICMetadataWriter.</span><span class="sxs-lookup"><span data-stu-id="87b7b-252">Each handler type's category ID is defined in the wincodec.idl; the category ID name for readers is CATID\_WICMetadataReader, and the category ID name for writers is CATID\_WICMetadataWriter.</span></span>

> [!Note]  
> <span data-ttu-id="87b7b-253">Dans les listes de clés de Registre suivantes, {Reader CLSID} fait référence au CLSID unique que vous fournissez pour votre lecteur de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-253">In the following registry key listings, {Reader CLSID} refers to the unique CLSID that you provide for your metadata reader.</span></span> <span data-ttu-id="87b7b-254">{Writer CLSID} fait référence au CLSID unique que vous fournissez pour votre générateur de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-254">{Writer CLSID} refers to the unique CLSID that you provide for your metadata writer.</span></span> <span data-ttu-id="87b7b-255">{Handler CLSID} fait référence au CLSID du lecteur, au CLSID du writer, ou aux deux, selon les gestionnaires que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="87b7b-255">{Handler CLSID} refers to the reader's CLSID, the writer's CLSID, or both, depending on which handlers you are providing.</span></span> <span data-ttu-id="87b7b-256">{Container GUID} fait référence à l’objet conteneur (format d’image ou format de métadonnées) qui peut contenir le bloc de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-256">{Container GUID} refers to the container object (image format or metadata format) that can contain the metadata block.</span></span>

 

<span data-ttu-id="87b7b-257">Les clés de Registre suivantes inscrivent votre gestionnaire de métadonnées avec les autres gestionnaires de métadonnées disponibles :</span><span class="sxs-lookup"><span data-stu-id="87b7b-257">The following registry keys register your metadata handler with the other metadata handlers available:</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CATID_WICMetadataReaders}\Instance\{Reader CLSID}]
CLSID={Reader CLSID}
Friendly Name="Reader Name"

[HKEY_CLASSES_ROOT\CLSID\{CATID_ WICMetadataWriters}\Instance\{Writer CLSID}]
CLSID={Writer CLSID}
Friendly Name="Writer Name"
```

<span data-ttu-id="87b7b-258">En plus d’inscrire vos gestionnaires dans leurs catégories respectives, vous devez également inscrire des clés supplémentaires qui fournissent des informations spécifiques au gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="87b7b-258">In addition to registering your handlers in their respective categories, you must also register additional keys that provide information specific to the handler.</span></span> <span data-ttu-id="87b7b-259">Les lecteurs et les enregistreurs partagent des exigences de clé de Registre similaires.</span><span class="sxs-lookup"><span data-stu-id="87b7b-259">Readers and writers share similar registry key requirements.</span></span> <span data-ttu-id="87b7b-260">La syntaxe suivante montre comment inscrire un gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="87b7b-260">The following syntax shows how to register a handler.</span></span> <span data-ttu-id="87b7b-261">Le gestionnaire de lecteur et le gestionnaire d’écriture doivent être enregistrés de cette manière, à l’aide de leurs CLSID respectifs :</span><span class="sxs-lookup"><span data-stu-id="87b7b-261">Both the reader handler and writer handler must be registered in this way, using their respective CLSIDs:</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CLSID}]
"Vendor"={VendorGUID}
"Date"="yyyy-mm-dd"
"Version"="Major.Minor.Build.Number"
"SpecVersion"="Major.Minor.Build.Number"
"MetadataFormat"={MetadataFormatGUID}
"RequiresFullStream"=dword:1|0
"SupportsPadding"= dword:1|0
"FixedSize"=0

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\InProcServer32]
@="drive:\path\yourdll.dll"
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\{LCID}]
Author="Author's Name"
Description = " Metadata Description"
DeviceManufacturer ="Manufacturer Name"
DeviceModels="Device,Device"
FriendlyName="Friendly Name"
```

### <a name="metadata-readers"></a><span data-ttu-id="87b7b-262">Lecteurs de métadonnées</span><span class="sxs-lookup"><span data-stu-id="87b7b-262">Metadata Readers</span></span>

<span data-ttu-id="87b7b-263">L’inscription des lecteurs de métadonnées comprend également des clés qui décrivent comment le lecteur peut être incorporé dans un format de conteneur.</span><span class="sxs-lookup"><span data-stu-id="87b7b-263">The metadata reader registration also includes keys that describe how the reader can be embedded in a container format.</span></span> <span data-ttu-id="87b7b-264">Un format de conteneur peut être un format d’image tel que TIFF ou JPEG. Il peut également s’agir d’un autre format de métadonnées, tel qu’un bloc de métadonnées IFD.</span><span class="sxs-lookup"><span data-stu-id="87b7b-264">A container format can be an image format such as TIFF or JPEG; it can also be another metadata format such as an IFD metadata block.</span></span> <span data-ttu-id="87b7b-265">Les formats de conteneur d’images pris en charge en mode natif sont répertoriés dans wincodec. idl. chaque format de conteneur d’images est défini en tant que GUID avec un nom commençant par le GUID \_ ContainerFormat.</span><span class="sxs-lookup"><span data-stu-id="87b7b-265">Natively supported image container formats are listed in wincodec.idl; each image container format is defined as a GUID with a name that begins with GUID\_ContainerFormat.</span></span> <span data-ttu-id="87b7b-266">Les formats de conteneur de métadonnées pris en charge en mode natif sont répertoriés dans wincodecsdk. idl. chaque format de conteneur de métadonnées est défini en tant que GUID avec un nom commençant par le GUID \_ MetadataFormat.</span><span class="sxs-lookup"><span data-stu-id="87b7b-266">Natively supported metadata container formats are listed in wincodecsdk.idl; each metadata container format is defined as a GUID with a name that begins with GUID\_MetadataFormat.</span></span>

<span data-ttu-id="87b7b-267">Les clés suivantes inscrivent un conteneur que le lecteur de métadonnées prend en charge, ainsi que les données nécessaires à la lecture de ce conteneur.</span><span class="sxs-lookup"><span data-stu-id="87b7b-267">The following keys register a container that the metadata reader supports, and the data needed to read from that container.</span></span> <span data-ttu-id="87b7b-268">Chaque conteneur pris en charge par le lecteur doit être inscrit de cette façon.</span><span class="sxs-lookup"><span data-stu-id="87b7b-268">Each container supported by the reader must be registered in this way.</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Reader CLSID}\Containers\{Container GUID}\0]
"Position"=dword:00000000
"Pattern"=hex:ff,ff,ff,...
"Mask"=hex:ff,ff,ff,...
"DataOffset"=dword:00000006
```

<span data-ttu-id="87b7b-269">La clé de modèle décrit le modèle binaire qui est utilisé pour faire correspondre le bloc de métadonnées au lecteur.</span><span class="sxs-lookup"><span data-stu-id="87b7b-269">The Pattern key describes the binary pattern that is used to match the metadata block to the reader.</span></span> <span data-ttu-id="87b7b-270">Lors de la définition d’un modèle pour votre lecteur de métadonnées, il doit être suffisamment fiable pour qu’une correspondance positive signifie que le lecteur de métadonnées peut comprendre les métadonnées du bloc de métadonnées en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="87b7b-270">When defining a pattern for your metadata reader, it should be reliable enough that a positive match means the metadata reader can understand the metadata in the metadata block being processed.</span></span>

<span data-ttu-id="87b7b-271">La clé DataOffset décrit l’offset fixe des métadonnées à partir de l’en-tête de bloc.</span><span class="sxs-lookup"><span data-stu-id="87b7b-271">The DataOffset key describes the fixed offset of the metadata from the block header.</span></span> <span data-ttu-id="87b7b-272">Cette clé est facultative et, si elle n’est pas spécifiée, signifie que les métadonnées réelles ne peuvent pas être localisées à l’aide d’un décalage fixe par rapport à l’en-tête de bloc.</span><span class="sxs-lookup"><span data-stu-id="87b7b-272">This key is optional and, if not specified, means that the actual metadata cannot be located using a fixed offset from the block header.</span></span>

### <a name="metadata-writers"></a><span data-ttu-id="87b7b-273">Enregistreurs de métadonnées</span><span class="sxs-lookup"><span data-stu-id="87b7b-273">Metadata Writers</span></span>

<span data-ttu-id="87b7b-274">L’inscription de l’enregistreur de métadonnées comprend également des clés qui décrivent comment écrire l’en-tête précédant le contenu de métadonnées incorporé dans un format de conteneur.</span><span class="sxs-lookup"><span data-stu-id="87b7b-274">The metadata writer registration also includes keys that describe how to write out the header preceding the metadata content embedded in a container format.</span></span> <span data-ttu-id="87b7b-275">Comme avec le lecteur, un format de conteneur peut être un format d’image ou un autre bloc de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-275">As with the reader, a container format can be an image format or another metadata block.</span></span>

<span data-ttu-id="87b7b-276">Les clés suivantes inscrivent un conteneur pris en charge par le writer de métadonnées, ainsi que les données nécessaires à l’écriture de l’en-tête et des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-276">The following keys register a container that the metadata writer supports, and the data needed to write the header and metadata.</span></span> <span data-ttu-id="87b7b-277">Chaque conteneur pris en charge par le writer doit être inscrit de cette façon.</span><span class="sxs-lookup"><span data-stu-id="87b7b-277">Each container supported by the writer must be registered in this way.</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Writer CLSID}\Containers\{Container GUID}]
"WritePosition"=dword:00000000
"WriteHeader"=hex:ff,ff,ff,...
"WriteOffset"=dword:00000000
```

<span data-ttu-id="87b7b-278">La clé WriteHeader décrit le modèle binaire de l’en-tête de bloc de métadonnées à écrire.</span><span class="sxs-lookup"><span data-stu-id="87b7b-278">The WriteHeader key describes the binary pattern of the metadata block header to be written.</span></span> <span data-ttu-id="87b7b-279">Ce modèle binaire coïncide avec la clé de modèle de lecteur du format de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-279">This binary pattern coincides with the metadata format's reader Pattern key.</span></span>

<span data-ttu-id="87b7b-280">La clé WriteOffset décrit l’offset fixe à partir de l’en-tête de bloc auquel les métadonnées doivent être écrites.</span><span class="sxs-lookup"><span data-stu-id="87b7b-280">The WriteOffset key describes the fixed offset from the block header at which the metadata should be written.</span></span> <span data-ttu-id="87b7b-281">Cette clé est facultative et, si elle n’est pas spécifiée, signifie que les métadonnées réelles ne doivent pas être écrites avec l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="87b7b-281">This key is optional and, if not specified, means that the actual metadata should not be written out with the header.</span></span>

### <a name="signing-a-metadata-handler"></a><span data-ttu-id="87b7b-282">Signature d’un gestionnaire de métadonnées</span><span class="sxs-lookup"><span data-stu-id="87b7b-282">Signing a Metadata Handler</span></span>

<span data-ttu-id="87b7b-283">Tous les gestionnaires de métadonnées doivent être signés numériquement pour participer au processus de découverte du WIC.</span><span class="sxs-lookup"><span data-stu-id="87b7b-283">All metadata handlers must be digitally signed to participate in the WIC discovery process.</span></span> <span data-ttu-id="87b7b-284">WIC ne chargera aucun gestionnaire qui n’est pas signé par une autorité de certification approuvée.</span><span class="sxs-lookup"><span data-stu-id="87b7b-284">WIC will not load any handler that is not signed by a trusted certificate authority.</span></span> <span data-ttu-id="87b7b-285">Pour plus d’informations sur la signature numérique, consultez [Présentation de la signature de code](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="87b7b-285">For more information on digital signing, see [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span></span>

## <a name="special-considerations"></a><span data-ttu-id="87b7b-286">Considérations spéciales</span><span class="sxs-lookup"><span data-stu-id="87b7b-286">Special Considerations</span></span>

<span data-ttu-id="87b7b-287">Les sections suivantes incluent des informations supplémentaires que vous devez prendre en compte lors de la création de vos propres gestionnaires de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-287">The following sections include additional information you must consider when creating your own metadata handlers.</span></span>

### <a name="propvariants"></a><span data-ttu-id="87b7b-288">PROPVARIANTS</span><span class="sxs-lookup"><span data-stu-id="87b7b-288">PROPVARIANTS</span></span>

<span data-ttu-id="87b7b-289">WIC utilise un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) pour représenter un élément de métadonnées à la fois pour la lecture et l’écriture.</span><span class="sxs-lookup"><span data-stu-id="87b7b-289">WIC uses a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) to represent a metadata item for both reading and writing.</span></span> <span data-ttu-id="87b7b-290">Un PROPVARIANT fournit un type de données et une valeur de données pour un élément de métadonnées utilisé dans un format de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-290">A PROPVARIANT provides a data type and data value for a metadata item used within a metadata format.</span></span> <span data-ttu-id="87b7b-291">En tant qu’auteur d’un gestionnaire de métadonnées, vous disposez d’une grande flexibilité sur la façon dont les données sont stockées dans le format de métadonnées et sur la façon dont les données sont représentées dans un bloc de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-291">As the writer of a metadata handler, you have a lot of flexibility on how data is stored in the metadata format and how data is represented within a metadata block.</span></span> <span data-ttu-id="87b7b-292">Le tableau suivant fournit des instructions pour vous aider à déterminer le type de PROPVARIANT approprié à utiliser dans différentes situations.</span><span class="sxs-lookup"><span data-stu-id="87b7b-292">The following table provides guidelines to help you decide on the appropriate PROPVARIANT type to use in different situations.</span></span>



| <span data-ttu-id="87b7b-293">Le type de métadonnées est...</span><span class="sxs-lookup"><span data-stu-id="87b7b-293">Metadata type is...</span></span>          | <span data-ttu-id="87b7b-294">Utiliser le type PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="87b7b-294">Use PROPVARIANT type</span></span>      | <span data-ttu-id="87b7b-295">Propriété PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="87b7b-295">PROPVARIANT Property</span></span>                                                                                                                                                                                                                                                           |
|------------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87b7b-296">Vide ou inexistant.</span><span class="sxs-lookup"><span data-stu-id="87b7b-296">Empty or non-existent.</span></span>       | <span data-ttu-id="87b7b-297">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="87b7b-297">VT\_EMPTY</span></span>                 | <span data-ttu-id="87b7b-298">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="87b7b-298">Not applicable.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="87b7b-299">Non défini.</span><span class="sxs-lookup"><span data-stu-id="87b7b-299">Undefined.</span></span>                   | <span data-ttu-id="87b7b-300">\_objet BLOB VT</span><span class="sxs-lookup"><span data-stu-id="87b7b-300">VT\_BLOB</span></span>                  | <span data-ttu-id="87b7b-301">Utilisez la propriété BLOB pour définir la taille et le pointeur sur l’objet BLOB alloué à l’aide de CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="87b7b-301">Use the blob property to set the size and pointer to the BLOB object allocated using CoTaskMemAlloc.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="87b7b-302">Bloc de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-302">A metadata block.</span></span>            | <span data-ttu-id="87b7b-303">VT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="87b7b-303">VT\_UNKNOWN</span></span>               | <span data-ttu-id="87b7b-304">Ce type utilise la propriété punkVal.</span><span class="sxs-lookup"><span data-stu-id="87b7b-304">This type uses the punkVal property.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="87b7b-305">Tableau de types.</span><span class="sxs-lookup"><span data-stu-id="87b7b-305">An array of types.</span></span>           | <span data-ttu-id="87b7b-306">VT \_ Vector \| VT \_ {type}</span><span class="sxs-lookup"><span data-stu-id="87b7b-306">VT\_VECTOR \| VT\_{type}</span></span>  | <span data-ttu-id="87b7b-307">Utilisez la propriété ca {type} pour définir le nombre et le pointeur sur le tableau alloué à l’aide de CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="87b7b-307">Use the ca{type} property to set the count and pointer to the array allocated using CoTaskMemAlloc.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="87b7b-308">Tableau de blocs de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87b7b-308">An array of metadata blocks.</span></span> | <span data-ttu-id="87b7b-309">\_variante VT Vector \| VT \_</span><span class="sxs-lookup"><span data-stu-id="87b7b-309">VT\_VECTOR \| VT\_VARIANT</span></span> | <span data-ttu-id="87b7b-310">Utilisez la propriété capropvar pour définir le tableau de variants.</span><span class="sxs-lookup"><span data-stu-id="87b7b-310">Use the capropvar property to set the array of variants.</span></span>                                                                                                                                                                                                                       |
| <span data-ttu-id="87b7b-311">Valeur rationnelle signée.</span><span class="sxs-lookup"><span data-stu-id="87b7b-311">A signed rational value.</span></span>     | <span data-ttu-id="87b7b-312">Le \_ i8 VT</span><span class="sxs-lookup"><span data-stu-id="87b7b-312">VT\_I8</span></span>                    | <span data-ttu-id="87b7b-313">Utilisez la propriété hVal pour définir la valeur.</span><span class="sxs-lookup"><span data-stu-id="87b7b-313">Use the hVal property to set the value.</span></span> <span data-ttu-id="87b7b-314">Définissez le mot de poids fort sur le dénominateur et le mot de poids faible sur le numérateur.</span><span class="sxs-lookup"><span data-stu-id="87b7b-314">Set the high word to the denominator and the low word to the numerator.</span></span>                                                                                                                                                                |
| <span data-ttu-id="87b7b-315">Valeur rationnelle.</span><span class="sxs-lookup"><span data-stu-id="87b7b-315">A rational value.</span></span>            | <span data-ttu-id="87b7b-316">\_UI8 VT</span><span class="sxs-lookup"><span data-stu-id="87b7b-316">VT\_UI8</span></span>                   | <span data-ttu-id="87b7b-317">Utilisez la propriété uhVal pour définir la valeur.</span><span class="sxs-lookup"><span data-stu-id="87b7b-317">Use the uhVal property to set the value.</span></span> <span data-ttu-id="87b7b-318">Définissez HighPart sur le dénominateur et LowPart sur le numérateur.</span><span class="sxs-lookup"><span data-stu-id="87b7b-318">Set the HighPart to the denominator and the LowPart to the numerator.</span></span> <span data-ttu-id="87b7b-319">Notez que LowPart est un entier non signé. Le numérateur doit être converti d’un int non signé en int pour garantir que le bit de signe est préservé s’il est présent.</span><span class="sxs-lookup"><span data-stu-id="87b7b-319">Note that the LowPart is an unsigned int. The numerator should be converted from an unsigned int to an int to ensure that the sign bit is preserved if present.</span></span> |



 

<span data-ttu-id="87b7b-320">Pour éviter la redondance dans la représentation d’éléments de tableau, n’utilisez pas de tableaux sécurisés ; Utilisez uniquement des tableaux simples.</span><span class="sxs-lookup"><span data-stu-id="87b7b-320">To avoid redundancy in representing array items, do not use safe arrays; use only simple arrays.</span></span> <span data-ttu-id="87b7b-321">Cela réduit le travail qu’une application doit effectuer lors de l’interprétation des types [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="87b7b-321">This reduces the work an application needs to perform when interpreting [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) types.</span></span>

<span data-ttu-id="87b7b-322">Évitez d’utiliser `VT_BYREF` et de stocker les valeurs inline dans la mesure du possible.</span><span class="sxs-lookup"><span data-stu-id="87b7b-322">Avoid using `VT_BYREF` and store values inline whenever possible.</span></span> <span data-ttu-id="87b7b-323">`VT_BYREF` est inefficace pour les petits types (communs aux éléments de métadonnées) et ne fournit pas d’informations sur la taille.</span><span class="sxs-lookup"><span data-stu-id="87b7b-323">`VT_BYREF` is inefficient for small types (common for metadata items) and does not provide size information.</span></span>

<span data-ttu-id="87b7b-324">Avant d’utiliser un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), appelez toujours **PropVariantInit** pour initialiser la valeur.</span><span class="sxs-lookup"><span data-stu-id="87b7b-324">Before using a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), always call **PropVariantInit** to initialize the value.</span></span> <span data-ttu-id="87b7b-325">Lorsque vous avez terminé avec le PROPVARIANT, appelez toujours **PropVariantClear** pour libérer toute mémoire allouée pour la variable.</span><span class="sxs-lookup"><span data-stu-id="87b7b-325">When you are finished with the PROPVARIANT, always call **PropVariantClear** to release any memory allocated for the variable.</span></span>

### <a name="8bim-handlers"></a><span data-ttu-id="87b7b-326">Gestionnaires 8BIM</span><span class="sxs-lookup"><span data-stu-id="87b7b-326">8BIM Handlers</span></span>

<span data-ttu-id="87b7b-327">Lors de l’écriture d’un gestionnaire de métadonnées pour un bloc de métadonnées 8BIM, vous devez utiliser une signature qui encapsule la signature 8BIM et l’ID.</span><span class="sxs-lookup"><span data-stu-id="87b7b-327">When writing a metadata handler for an 8BIM metadata block, you must use a signature that encapsulates both the 8BIM signature and the ID.</span></span> <span data-ttu-id="87b7b-328">Par exemple, le lecteur de métadonnées 8BIMIPTC natif fournit les informations de Registre suivantes pour la découverte des lecteurs :</span><span class="sxs-lookup"><span data-stu-id="87b7b-328">For example, the native 8BIMIPTC metadata reader provides the following registry information for reader discovery:</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{0010668C-0801-4DA6-A4A4-826522B6D28F}\Containers\{16100D66-8570-4BB9-B92D-FDA4B23ECE67}\0]
"Position"=dword:00000000
"Pattern"=hex:38,42,49,4d,04,04
"Mask"=hex:ff,ff,ff,ff,ff,ff
"DataOffset"=dword:00000006
```

<span data-ttu-id="87b7b-329">Le lecteur 8BIMIPTC a un modèle inscrit de 0x38, 0x42, 0x49, 0x4D, 0x04, 0x04.</span><span class="sxs-lookup"><span data-stu-id="87b7b-329">The 8BIMIPTC reader has a registered pattern of 0x38, 0x42, 0x49, 0x4D, 0x04, 0x04.</span></span> <span data-ttu-id="87b7b-330">Les quatre premiers octets (0x38, 0x42, 0x49, 0x4D) sont la signature 8BIM, et les deux derniers octets (0x04, 0x04) sont l’ID de l’enregistrement IPTC.</span><span class="sxs-lookup"><span data-stu-id="87b7b-330">The first four bytes (0x38, 0x42, 0x49, 0x4D) are the 8BIM signature, and the last two bytes (0x04, 0x04) are the ID for the IPTC record.</span></span>

<span data-ttu-id="87b7b-331">Ainsi, pour écrire un lecteur de métadonnées 8BIM pour les informations de résolution, vous avez besoin d’un modèle inscrit de 0x38, 0x42, 0x49, 0x4D, 0x03, 0xED.</span><span class="sxs-lookup"><span data-stu-id="87b7b-331">So, to write an 8BIM metadata reader for resolution information, you would need a registered pattern of 0x38, 0x42, 0x49, 0x4D, 0x03, 0xED.</span></span> <span data-ttu-id="87b7b-332">Là encore, les quatre premiers octets (0x38, 0x42, 0x49, 0x4D) sont la signature 8BIM.</span><span class="sxs-lookup"><span data-stu-id="87b7b-332">Again, the first four bytes (0x38, 0x42, 0x49, 0x4D) are the 8BIM signature.</span></span> <span data-ttu-id="87b7b-333">Toutefois, les deux derniers octets (0x03, 0xED) sont l’ID des informations de résolution tel que défini par le format PSD.</span><span class="sxs-lookup"><span data-stu-id="87b7b-333">The last two bytes (0x03, 0xED), however, are the resolution information ID as defined by the PSD format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87b7b-334">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="87b7b-334">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="87b7b-335">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="87b7b-335">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="87b7b-336">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="87b7b-336">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="87b7b-337">Vue d’ensemble des métadonnées WIC</span><span class="sxs-lookup"><span data-stu-id="87b7b-337">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="87b7b-338">Vue d’ensemble du langage de requête de métadonnées</span><span class="sxs-lookup"><span data-stu-id="87b7b-338">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="87b7b-339">Vue d’ensemble de la lecture et de l’écriture des métadonnées d’image</span><span class="sxs-lookup"><span data-stu-id="87b7b-339">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="87b7b-340">Comment : recoder une image JPEG avec des métadonnées</span><span class="sxs-lookup"><span data-stu-id="87b7b-340">How-to: Re-encode a JPEG Image with Metadata</span></span>](-wic-codec-jpegmetadataencoding.md)
</dt> <dt>

<span data-ttu-id="87b7b-341">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="87b7b-341">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="87b7b-342">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="87b7b-342">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
