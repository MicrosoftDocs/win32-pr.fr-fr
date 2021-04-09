---
description: Implémentation de IWICMetadataBlockReader
ms.assetid: 80ad8e20-a9d4-4503-94ba-1b7699e36111
title: Implémentation de IWICMetadataBlockReader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bfe53e87dae52d004fa90d1104fb60f252085d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865549"
---
# <a name="implementing-iwicmetadatablockreader"></a><span data-ttu-id="45a5f-103">Implémentation de IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="45a5f-103">Implementing IWICMetadataBlockReader</span></span>

## <a name="iwicmetadatablockreader"></a><span data-ttu-id="45a5f-104">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="45a5f-104">IWICMetadataBlockReader</span></span>

<span data-ttu-id="45a5f-105">Plusieurs blocs de métadonnées existent souvent dans une image, chacun exposant différents types d’informations dans différents formats.</span><span class="sxs-lookup"><span data-stu-id="45a5f-105">Multiple blocks of metadata often exist within an image, each exposing different types of information in different formats.</span></span> <span data-ttu-id="45a5f-106">Dans le modèle WIC (Windows Imaging Component), les gestionnaires de métadonnées sont des composants distincts qui, comme les décodeurs, sont détectables au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="45a5f-106">In the Windows Imaging Component (WIC) model, metadata handlers are distinct components that, like decoders, are discoverable at run time.</span></span> <span data-ttu-id="45a5f-107">Chaque format de métadonnées a un gestionnaire distinct, et chacun de ces gestionnaires de métadonnées peut être utilisé avec tout format d’image qui prend en charge le format de métadonnées qu’il gère.</span><span class="sxs-lookup"><span data-stu-id="45a5f-107">Each metadata format has a separate handler, and each of these metadata handlers can be used with any image format that supports the metadata format it handles.</span></span> <span data-ttu-id="45a5f-108">Par conséquent, si votre format d’image prend en charge EXIF, XMP, IPTC ou un autre format, vous pouvez tirer parti des gestionnaires de métadonnées standard pour ces formats fournis avec WIC, et vous n’avez pas besoin d’écrire le vôtre.</span><span class="sxs-lookup"><span data-stu-id="45a5f-108">Therefore, if your image format supports EXIF, XMP, IPTC, or another format, you can take advantage of the standard metadata handlers for these formats that ship with WIC, and you do not need to write your own.</span></span> <span data-ttu-id="45a5f-109">Bien entendu, si vous créez un nouveau format de métadonnées, vous devez écrire un gestionnaire de métadonnées pour celui-ci, qui sera découvert et appelé au moment de l’exécution comme les valeurs standard.</span><span class="sxs-lookup"><span data-stu-id="45a5f-109">Of course, if you create a new metadata format, you must write a metadata handler for it, which will be discovered and invoked at run time just as the standard ones are.</span></span>

> [!Note]  
> <span data-ttu-id="45a5f-110">Si votre format d’image est basé sur un conteneur TIFF (Tagged Image File Format) ou JPEG, vous n’avez pas besoin d’écrire de gestionnaires de métadonnées (sauf si vous développez un nouveau format de métadonnées propriétaire).</span><span class="sxs-lookup"><span data-stu-id="45a5f-110">If your image format is based on a Tagged Image File Format (TIFF) or JPEG container, you won’t need to write any metadata handlers (unless you develop a new or proprietary metadata format).</span></span> <span data-ttu-id="45a5f-111">Dans les conteneurs TIFF et JPEG, les blocs de métadonnées se trouvent dans IFD, et chaque conteneur a une structure IFD différente.</span><span class="sxs-lookup"><span data-stu-id="45a5f-111">In TIFF and JPEG containers, blocks of metadata are located within IFDs, and each container has a different IFD structure.</span></span> <span data-ttu-id="45a5f-112">WIC fournit des gestionnaires IFD pour ces deux formats de conteneur qui parcourent la structure IFD et délèguent aux gestionnaires de métadonnées standard pour accéder aux métadonnées qu’ils contiennent.</span><span class="sxs-lookup"><span data-stu-id="45a5f-112">WIC provides IFD handlers for both of these container formats that navigate the IFD structure and delegate to the standard metadata handlers to access the metadata within them.</span></span> <span data-ttu-id="45a5f-113">Par conséquent, si votre format d’image est basé sur l’un de ces conteneurs, vous pouvez automatiquement tirer parti des gestionnaires IFD du WIC.</span><span class="sxs-lookup"><span data-stu-id="45a5f-113">So, if your image format is based on either of these containers, you can automatically take advantage of the WIC IFD handlers.</span></span> <span data-ttu-id="45a5f-114">Toutefois, si vous avez un format de conteneur propriétaire qui a sa propre structure de métadonnées de niveau supérieur unique, vous devez écrire un gestionnaire qui peut naviguer dans cette structure de niveau supérieur et déléguer aux gestionnaires de métadonnées appropriés, tout comme les gestionnaires IFD.)</span><span class="sxs-lookup"><span data-stu-id="45a5f-114">However, if you have a proprietary container format that has its own unique top-level metadata structure, you must write a handler that can navigate that top-level structure and delegate to the appropriate metadata handlers, just like the IFD handlers do.)</span></span>

 

<span data-ttu-id="45a5f-115">De la même façon, WIC fournit une couche d’abstraction pour les applications qui leur permet de fonctionner avec tous les formats d’image de la même façon via un ensemble cohérent d’interfaces, WIC fournit une couche d’abstraction pour les auteurs de codec en ce qui concerne les formats de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="45a5f-115">The same way WIC provides a layer of abstraction for applications that allows them to work with all image formats in the same way through a consistent set of interfaces, WIC provides a layer of abstraction for codec authors with regard to metadata formats.</span></span> <span data-ttu-id="45a5f-116">Comme indiqué précédemment, les auteurs de codec n’ont généralement pas besoin de travailler directement avec les différents formats de métadonnées qui peuvent être présents dans une image.</span><span class="sxs-lookup"><span data-stu-id="45a5f-116">As noted previously, codec authors generally do not need to work directly with the various metadata formats that may be present in an image.</span></span> <span data-ttu-id="45a5f-117">Toutefois, chaque auteur de codec est chargé de fournir un moyen d’énumérer les blocs de métadonnées afin qu’un gestionnaire de métadonnées approprié puisse être découvert et instancié pour chaque bloc.</span><span class="sxs-lookup"><span data-stu-id="45a5f-117">However, every codec author is responsible for providing a way to enumerate the blocks of metadata so an appropriate metadata handler can be discovered and instantiated for each block.</span></span>

<span data-ttu-id="45a5f-118">Vous devez implémenter cette interface sur votre classe de décodage au niveau de la trame.</span><span class="sxs-lookup"><span data-stu-id="45a5f-118">You must implement this interface on your frame-level decoding class.</span></span> <span data-ttu-id="45a5f-119">Vous devrez peut-être également l’implémenter sur votre classe de décodeur au niveau du conteneur si votre format d’image expose des métadonnées globales en dehors de toutes les trames d’image individuelles.</span><span class="sxs-lookup"><span data-stu-id="45a5f-119">You may also need to implement it on your container-level decoder class if your image format exposes global metadata outside of any individual image frames.</span></span>

``` syntax
interface IWICMetadataBlockReader : IUnknown
{
   // All methods required
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetCount ( UINT *pcCount );
   HRESULT GetEnumerator ( IEnumUnknown **ppIEnumMetadata );
   HRESULT GetReaderByIndex ( UINT nIndex, IWICMetadataReader **ppIMetadataReader );
}
```

-   [<span data-ttu-id="45a5f-120">GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="45a5f-120">GetContainerFormat</span></span>](#getcontainerformat)
-   [<span data-ttu-id="45a5f-121">GetCount</span><span class="sxs-lookup"><span data-stu-id="45a5f-121">GetCount</span></span>](#getcount)
-   [<span data-ttu-id="45a5f-122">GetEnumerator</span><span class="sxs-lookup"><span data-stu-id="45a5f-122">GetEnumerator</span></span>](#getenumerator)
-   [<span data-ttu-id="45a5f-123">GetReaderByIndex</span><span class="sxs-lookup"><span data-stu-id="45a5f-123">GetReaderByIndex</span></span>](#getreaderbyindex)

### <a name="getcontainerformat"></a><span data-ttu-id="45a5f-124">GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="45a5f-124">GetContainerFormat</span></span>

<span data-ttu-id="45a5f-125">[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat) est identique à la méthode [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) lors de l' [implémentation de IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).</span><span class="sxs-lookup"><span data-stu-id="45a5f-125">[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat) is the same as the [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) method on [Implementing IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).</span></span>

### <a name="getcount"></a><span data-ttu-id="45a5f-126">GetCount</span><span class="sxs-lookup"><span data-stu-id="45a5f-126">GetCount</span></span>

<span data-ttu-id="45a5f-127">[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) retourne le nombre de blocs de métadonnées de niveau supérieur associés au frame.</span><span class="sxs-lookup"><span data-stu-id="45a5f-127">[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) returns the number of top-level metadata blocks associated with the frame.</span></span>

### <a name="getenumerator"></a><span data-ttu-id="45a5f-128">GetEnumerator</span><span class="sxs-lookup"><span data-stu-id="45a5f-128">GetEnumerator</span></span>

<span data-ttu-id="45a5f-129">[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) retourne un énumérateur que l’appelant peut utiliser pour énumérer les blocs de métadonnées dans le frame et lire leurs métadonnées.</span><span class="sxs-lookup"><span data-stu-id="45a5f-129">[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) returns an enumerator that the caller can use to enumerate over the metadata blocks in the frame and read their metadata.</span></span> <span data-ttu-id="45a5f-130">Pour implémenter cette méthode, vous devez créer un lecteur de métadonnées pour chaque bloc de métadonnées et implémenter un objet d’énumération qui énumère la collection de lecteurs de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="45a5f-130">To implement this method, you need to create a metadata reader for each block of metadata, and implement an enumeration object that enumerates over the collection of metadata readers.</span></span> <span data-ttu-id="45a5f-131">L’objet d’énumération doit implémenter [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) afin que vous puissiez le convertir en IEnumUnknown lorsque vous le retournez dans le paramètre *ppIEnumMetadata* .</span><span class="sxs-lookup"><span data-stu-id="45a5f-131">The enumeration object must implement [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) so you can cast it to IEnumUnknown when you return it in the *ppIEnumMetadata* parameter.</span></span>

<span data-ttu-id="45a5f-132">Lors de l’implémentation de l’objet d’énumération, vous pouvez créer tous les lecteurs de métadonnées lorsque vous créez pour la première fois l’objet [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) ou lorsque vous créez l’objet d’énumération pour la première fois, ou vous pouvez les créer de manière différée à l’intérieur de l’implémentation de la méthode [IEnumUnknown :: Next](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) .</span><span class="sxs-lookup"><span data-stu-id="45a5f-132">When implementing the enumeration object, you can create all the metadata readers when you first create the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) object or when you first create the enumeration object, or you can create them lazily inside the implementation of the [IEnumUnknown::Next](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) method.</span></span> <span data-ttu-id="45a5f-133">Dans de nombreux cas, il est plus efficace de les créer tardivement, mais dans l’exemple suivant, les lecteurs de bloc sont tous créés dans le constructeur pour économiser de l’espace.</span><span class="sxs-lookup"><span data-stu-id="45a5f-133">In many cases, it’s more efficient to create them lazily but, in the following example, the block readers are all created in the constructor to save space.</span></span>


```C++
public class MetadataReaderEnumerator : public IEnumUnknown
{
   UINT m_current;
   UINT m_blockCount;
   IWICMetadataReader** m_ppMetadataReader;
   IStream* m_pStream;

   MetadataReaderEnumerator() 
   {
       // Set m_blockCount to the number of metadata blocks in the frame. 
      ...
      m_ppMetadataReader = IWICMetadataReader*[m_blockCount];
       m_current = 0;

      for (UINT x=0; x < m_blockCount; x++) 
      {
         // Find the position in the file where the xth
         // block of metadata lives and seek m_piStream 
         // to that position.
         ...

         m_pComponentFactory->CreateMetadataReaderFromContainer(
            GUID_ContainerFormatTiff,
                        NULL,
                        WICPersistOptions.WICPersistOptionsDefault | 
            WICMetadataCreationOptions.WICMetadataCreationDefault, 
                        m_pStream, &m_ppMetadataReader[x]);
        }
    }

    // Implementation of IEnumUnknown and IUnknown interfaces
    ...
}
```



<span data-ttu-id="45a5f-134">Pour créer les lecteurs de métadonnées, vous utilisez la méthode [**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) .</span><span class="sxs-lookup"><span data-stu-id="45a5f-134">To create the metadata readers, you use the [**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) method.</span></span> <span data-ttu-id="45a5f-135">Lors de l’appel de cette méthode, vous transmettez le GUID du format de conteneur dans le paramètre *guidContainerFormat* .</span><span class="sxs-lookup"><span data-stu-id="45a5f-135">When invoking this method, you pass in the GUID of the container format in the *guidContainerFormat* parameter.</span></span> <span data-ttu-id="45a5f-136">Si vous avez une préférence de fournisseur pour un lecteur de métadonnées, vous pouvez transmettre le GUID de votre fournisseur préféré dans le paramètre *pGuidVendor* .</span><span class="sxs-lookup"><span data-stu-id="45a5f-136">If you have a preference of vendor for a metadata reader, you can pass the GUID of your preferred vendor in the *pGuidVendor* parameter.</span></span> <span data-ttu-id="45a5f-137">Par exemple, si votre entreprise écrit des gestionnaires de métadonnées et que vous souhaitez utiliser la vôtre si elle est présente, vous pouvez transmettre le GUID de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="45a5f-137">For example, if your company writes metadata handlers, and you want to use your own if present, you can pass in your vendor GUID.</span></span> <span data-ttu-id="45a5f-138">Dans la plupart des cas, vous devez simplement passer la **valeur null** et laisser le système sélectionner le lecteur de métadonnées approprié.</span><span class="sxs-lookup"><span data-stu-id="45a5f-138">In most cases, you would just pass **NULL**, and let the system select the appropriate metadata reader.</span></span> <span data-ttu-id="45a5f-139">Si vous demandez un fournisseur spécifique et que celui-ci dispose d’un lecteur de métadonnées installé sur l’ordinateur, WIC retourne le lecteur de ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="45a5f-139">If you do request a specific vendor, and that vendor does have a metadata reader installed on the computer, WIC will return that vendor’s reader.</span></span> <span data-ttu-id="45a5f-140">Toutefois, si le fournisseur demandé ne dispose pas d’un lecteur de métadonnées installé sur l’ordinateur et si un lecteur de métadonnées approprié est disponible, ce lecteur est retourné même s’il ne provient pas du fournisseur préféré.</span><span class="sxs-lookup"><span data-stu-id="45a5f-140">However, if the requested vendor does not have a metadata reader installed on the computer, and if there is an appropriate metadata reader available, that reader will be returned even though it is not from the preferred vendor.</span></span> <span data-ttu-id="45a5f-141">S’il n’existe aucun lecteur de métadonnées sur l’ordinateur pour le type de métadonnées dans le bloc, la fabrique de composants retourne le gestionnaire de métadonnées inconnu, qui traite le bloc de métadonnées comme un objet BLOB (Binary Large Object) et désérialise le bloc de métadonnées du fichier sans aucune tentative d’analyse.</span><span class="sxs-lookup"><span data-stu-id="45a5f-141">If there is no metadata reader on the computer for the type of metadata in the block, the component factory will return the Unknown Metadata Handler, which will treat the block of metadata as a binary large object (BLOB), and will deserialize the block of metadata from the file without any attempt at parsing it.</span></span>

<span data-ttu-id="45a5f-142">Pour le paramètre *dwOptions* , effectuez une opération or entre le [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) approprié et le [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions)approprié.</span><span class="sxs-lookup"><span data-stu-id="45a5f-142">For the *dwOptions* parameter, perform an OR operation between the appropriate [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) with the appropriate [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions).</span></span> <span data-ttu-id="45a5f-143">Le **WICPersistOptions** décrit comment votre conteneur est disposé. La valeur par défaut est Little endian.</span><span class="sxs-lookup"><span data-stu-id="45a5f-143">The **WICPersistOptions** describe how your container is laid out. Little-endian is the default.</span></span>

``` syntax
enum WICPersistOptions
{   
   WICPersistOptionDefault,
   WICPersistOptionLittleEndian,
   WICPersistOptionBigEndian,
   WICPersistOptionStrictFormat,
   WICPersistOptionNoCacheStream,
   WICPersistOptionPreferUTF8
};
```

<span data-ttu-id="45a5f-144">Le [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) spécifie si vous souhaitez récupérer le UnknownMetadataHandler si aucun lecteur de métadonnées n’est trouvé sur l’ordinateur qui peut lire le format de métadonnées d’un bloc particulier.</span><span class="sxs-lookup"><span data-stu-id="45a5f-144">The [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) specify whether you want to get back the UnknownMetadataHandler if no metadata reader is found on the machine that can read the metadata format of a particular block.</span></span> <span data-ttu-id="45a5f-145">**WICMetadataCreationAllowUnknown** est la valeur par défaut, et vous devez toujours autoriser la création du UnknownMetadtataHandler.</span><span class="sxs-lookup"><span data-stu-id="45a5f-145">**WICMetadataCreationAllowUnknown** is the default, and you should always allow creation of the UnknownMetadtataHandler.</span></span> <span data-ttu-id="45a5f-146">UnknownMetadataHandler traite les métadonnées non reconnues comme un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="45a5f-146">The UnknownMetadataHandler treats unrecognized metadata as a BLOB.</span></span> <span data-ttu-id="45a5f-147">Il ne peut pas l’analyser, mais il l’écrit dans le flux en tant qu’objet BLOB et le rend intact quand il est réécrit dans le flux pendant l’encodage.</span><span class="sxs-lookup"><span data-stu-id="45a5f-147">It cannot parse it, but it writes it out into the stream as a BLOB, and persists it intact when it’s written back to the stream during encoding.</span></span> <span data-ttu-id="45a5f-148">Cela permet de créer en toute sécurité des gestionnaires de métadonnées pour les formats de métadonnées propriétaires ou de métadonnées qui ne sont pas fournis avec le système.</span><span class="sxs-lookup"><span data-stu-id="45a5f-148">This makes it safe to create metadata handlers for proprietary metadata or metadata formats that don’t ship with the system.</span></span> <span data-ttu-id="45a5f-149">Étant donné que les métadonnées sont conservées intactes, même si aucun gestionnaire n’est présent sur l’ordinateur qui les reconnaît, lorsqu’un gestionnaire de métadonnées approprié est installé ultérieurement, les métadonnées sont toujours présentes et peuvent être lues.</span><span class="sxs-lookup"><span data-stu-id="45a5f-149">Because metadata is preserved intact, even if no handler is present on the computer that recognizes it, when an appropriate metadata handler is later installed, the metadata will still be there and can be read.</span></span> <span data-ttu-id="45a5f-150">Si vous n’autorisez pas la création du UnknownMetadataHandler, l’alternative ignore ou remplace les métadonnées non reconnues.</span><span class="sxs-lookup"><span data-stu-id="45a5f-150">If you don’t allow creation of the UnknownMetadataHandler, the alternative is discarding or overwriting unrecognized metadata.</span></span> <span data-ttu-id="45a5f-151">Il s’agit d’une forme de perte de données.</span><span class="sxs-lookup"><span data-stu-id="45a5f-151">This is a form of data loss.</span></span>

> [!Note]  
> <span data-ttu-id="45a5f-152">Si vous écrivez votre propre gestionnaire de métadonnées pour les métadonnées propriétaires, vous ne devez jamais inclure de références à ce qui se trouve en dehors du bloc de métadonnées lui-même.</span><span class="sxs-lookup"><span data-stu-id="45a5f-152">If you write your own metadata handler for proprietary metadata, you should never include references to anything outside the metadata block itself.</span></span> <span data-ttu-id="45a5f-153">Même si le UnknownMetadataHandler conserve les métadonnées intactes, les métadonnées sont déplacées lors de la modification des fichiers et toutes les références à des éléments en dehors de son propre bloc ne seront plus valides lorsque cela se produit.</span><span class="sxs-lookup"><span data-stu-id="45a5f-153">Even though the UnknownMetadataHandler preserves metadata intact, metadata does get moved when files are edited, and any references to anything outside its own block will no longer be valid when this happens.</span></span>

 

``` syntax
enum WICMetadataCreationOptions
{
   WICMetadataCreationDefault = 0x00000000,
   WICMetadataCreationAllowUnknown = WICMetadataCreationDefault,
   WICMetadataCreationFailUnknown = 0x00010000,
   WICMetadataCreationMask = 0xFFFF0000
};
```

<span data-ttu-id="45a5f-154">Le paramètre *pIStream* est le flux réel que vous décodez.</span><span class="sxs-lookup"><span data-stu-id="45a5f-154">The *pIStream* parameter is the actual stream that you are decoding.</span></span> <span data-ttu-id="45a5f-155">Avant de passer le flux, vous devez rechercher le début du bloc de métadonnées pour lequel vous demandez un lecteur.</span><span class="sxs-lookup"><span data-stu-id="45a5f-155">Before passing in the stream, you should seek to the beginning of the metadata block for which you’re requesting a reader.</span></span> <span data-ttu-id="45a5f-156">Le lecteur de métadonnées approprié pour le bloc de métadonnées à la position actuelle dans l' [IStream](/windows/desktop/api/objidl/nn-objidl-istream) est retourné dans le paramètre *ppiReader* .</span><span class="sxs-lookup"><span data-stu-id="45a5f-156">The appropriate metadata reader for the metadata block at the current position in the [IStream](/windows/desktop/api/objidl/nn-objidl-istream) will be returned in the *ppiReader* parameter.</span></span>

### <a name="getreaderbyindex"></a><span data-ttu-id="45a5f-157">GetReaderByIndex</span><span class="sxs-lookup"><span data-stu-id="45a5f-157">GetReaderByIndex</span></span>

<span data-ttu-id="45a5f-158">[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) retourne le lecteur de métadonnées à l’index demandé dans la collection.</span><span class="sxs-lookup"><span data-stu-id="45a5f-158">[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) returns the metadata reader at the requested index in the collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="45a5f-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="45a5f-159">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="45a5f-160">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="45a5f-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="45a5f-161">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="45a5f-161">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

<span data-ttu-id="45a5f-162">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="45a5f-162">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="45a5f-163">Implémentation de IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="45a5f-163">Implementing IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[<span data-ttu-id="45a5f-164">Implémentation de IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="45a5f-164">Implementing IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[<span data-ttu-id="45a5f-165">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="45a5f-165">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="45a5f-166">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="45a5f-166">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
