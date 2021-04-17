---
description: Implémentation de IWICMetadataBlockWriter
ms.assetid: 31824f21-04b1-45ca-adfa-15fd348e14a1
title: Implémentation de IWICMetadataBlockWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62044ce9695a45a8fe052d67479158aa9e4baf6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530268"
---
# <a name="implementing-iwicmetadatablockwriter"></a><span data-ttu-id="77293-103">Implémentation de IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="77293-103">Implementing IWICMetadataBlockWriter</span></span>

## <a name="iwicmetadatablockwriter"></a><span data-ttu-id="77293-104">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="77293-104">IWICMetadataBlockWriter</span></span>

-   [<span data-ttu-id="77293-105">InitializeFromBlockReader</span><span class="sxs-lookup"><span data-stu-id="77293-105">InitializeFromBlockReader</span></span>](#initializefromblockreader)
-   [<span data-ttu-id="77293-106">GetWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="77293-106">GetWriterByIndex</span></span>](#getwriterbyindex)
-   [<span data-ttu-id="77293-107">AddWriter</span><span class="sxs-lookup"><span data-stu-id="77293-107">AddWriter</span></span>](#addwriter)
-   [<span data-ttu-id="77293-108">SetWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="77293-108">SetWriterByIndex</span></span>](#setwriterbyindex)
-   [<span data-ttu-id="77293-109">RemoveWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="77293-109">RemoveWriterByIndex</span></span>](#removewriterbyindex)

<span data-ttu-id="77293-110">La classe d’encodage au niveau de la trame implémente cette interface pour exposer tous les blocs de métadonnées et demander le writer de métadonnées approprié pour chaque bloc.</span><span class="sxs-lookup"><span data-stu-id="77293-110">The frame-level encoding class implements this interface to expose all the metadata blocks and request the appropriate metadata writer for each block.</span></span> <span data-ttu-id="77293-111">Si votre format d’image prend en charge les métadonnées globales, en dehors de tout Frame individuel, vous devez également implémenter cette interface sur la classe de codeur au niveau du conteneur.</span><span class="sxs-lookup"><span data-stu-id="77293-111">If your image format supports global metadata, outside of any individual frame, you should also implement this interface on the container-level encoder class.</span></span> <span data-ttu-id="77293-112">Pour une présentation plus détaillée des gestionnaires de métadonnées, reportez-vous à la section du [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) dans la section sur l’implémentation d’un décodeur de WIC-Enabled.</span><span class="sxs-lookup"><span data-stu-id="77293-112">For a more detailed discussion of metadata handlers, refer to the section on the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) in the section on Implementing a WIC-Enabled Decoder.</span></span>

``` syntax
interface IWICMetadataBlockWriter : IWICMetadataBlockReader
{
   // All methods required
   HRESULT InitializeFromBlockReader ( IWICMetadataBlockReader *pIMDBlockReader );
   HRESULT GetWriterByIndex ( UINT nIndex, IWICMetadataWriter **ppIMetadataWriter );
   HRESULT AddWriter (IWICMetadataWriter *pIMetadataWriter );
   HRESULT SetWriterByIndex ( UINT nIndex, IWICMetadataWriter *pIMetadataWriter );
   HRESULT RemoveWriterByIndex ( UINT nIndex );
}
```

### <a name="initializefromblockreader"></a><span data-ttu-id="77293-113">InitializeFromBlockReader</span><span class="sxs-lookup"><span data-stu-id="77293-113">InitializeFromBlockReader</span></span>

<span data-ttu-id="77293-114">[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) utilise un [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) pour initialiser le writer de bloc.</span><span class="sxs-lookup"><span data-stu-id="77293-114">[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) uses an [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) to initialize the block writer.</span></span> <span data-ttu-id="77293-115">Vous pouvez récupérer le **IWICMetadataBlockReader** à partir du décodeur qui a décodé l’image.</span><span class="sxs-lookup"><span data-stu-id="77293-115">You can get the **IWICMetadataBlockReader** from the decoder that decoded the image.</span></span>


```C++
UINT blockCount = 0;
IWICMetadataReader* pMetadataReader = NULL;
IWICMetadataWriter** ppMetadataWriter = NULL;
HRESULT hr;

hr = m_pBlockReader->GetCount(&blockCount);
ppMetadataWriter = IWICMetadataWriter*[blockCount];

for (UINT x=0; x < blockCount; x++)
{
   hr = m_pBlockReader->GetReaderByIndex(&pMetadataReader);
   hr = m_pComponentFactory->CreateMetadataWriterFromReader(
         pMetadataReader, NULL, &ppMetadataWriter[x]);
}
```



<span data-ttu-id="77293-116">Étant donné que l’initialisation du [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) avec un [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) instancie un writer de métadonnées pour chaque lecteur de métadonnées exposé par l’objet **IWICMetadataBlockReader** , l’application n’a pas besoin de demander explicitement un writer pour chaque bloc de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="77293-116">Because initializing the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) with an [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) instantiates a metadata writer for each metadata reader exposed by the **IWICMetadataBlockReader** object, the application doesn’t have to explicitly request a writer for each block of metadata.</span></span>

### <a name="getwriterbyindex"></a><span data-ttu-id="77293-117">GetWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="77293-117">GetWriterByIndex</span></span>

<span data-ttu-id="77293-118">[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) retourne l’objet [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) pour le nième bloc de métadonnées, où n est la valeur passée dans le paramètre *nIndex* .</span><span class="sxs-lookup"><span data-stu-id="77293-118">[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) returns the [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) object for the nth metadata block, where n is the value passed in the *nIndex* parameter.</span></span> <span data-ttu-id="77293-119">Si aucun enregistreur de métadonnées inscrit ne peut gérer le type de métadonnées dans le bloc nième, la fabrique de composants retourne le gestionnaire de métadonnées inconnu, qui traite le bloc de métadonnées comme un objet BLOB (Binary Large Object).</span><span class="sxs-lookup"><span data-stu-id="77293-119">If there is no metadata writer registered that can handle the type of metadata in the nth block, the component factory will return the Unknown Metadata Handler, which will treat the block of metadata as a binary large object (BLOB).</span></span> <span data-ttu-id="77293-120">Il le sérialise comme un flux binaire sans tenter de l’analyser.</span><span class="sxs-lookup"><span data-stu-id="77293-120">It will serialize it out as a bit stream without attempting to parse it.</span></span>

### <a name="addwriter"></a><span data-ttu-id="77293-121">AddWriter</span><span class="sxs-lookup"><span data-stu-id="77293-121">AddWriter</span></span>

<span data-ttu-id="77293-122">[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) permet à un appelant d’ajouter un nouveau générateur de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="77293-122">[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) allows a caller to add a new metadata writer.</span></span> <span data-ttu-id="77293-123">Cela est obligatoire si une application souhaite ajouter des métadonnées d’un format différent de celui des blocs de métadonnées existants.</span><span class="sxs-lookup"><span data-stu-id="77293-123">This is required if an application wants to add metadata of a different format than any of the existing metadata blocks.</span></span> <span data-ttu-id="77293-124">Par exemple, une application peut souhaiter ajouter des métadonnées XMP.</span><span class="sxs-lookup"><span data-stu-id="77293-124">For example, an application may want to add some XMP metadata.</span></span> <span data-ttu-id="77293-125">S’il n’existe aucun bloc de métadonnées XMP existant, l’application doit instancier un enregistreur de métadonnées XMP et utiliser la méthode **AddWriter** pour l’inclure dans la collection de Writers de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="77293-125">If there is no existing XMP metadata block, the application must instantiate an XMP metadata writer and use the **AddWriter** method to include it in the collection of metadata writers.</span></span>

### <a name="setwriterbyindex"></a><span data-ttu-id="77293-126">SetWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="77293-126">SetWriterByIndex</span></span>

<span data-ttu-id="77293-127">[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) est utilisé pour ajouter un enregistreur de métadonnées à un index spécifique dans la collection.</span><span class="sxs-lookup"><span data-stu-id="77293-127">[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) is used to add a metadata writer at a specific index in the collection.</span></span> <span data-ttu-id="77293-128">Si un enregistreur de métadonnées existe actuellement à cet index, le nouveau doit le remplacer.</span><span class="sxs-lookup"><span data-stu-id="77293-128">If a metadata writer is currently exists at that index, the new one should replace it.</span></span>

### <a name="removewriterbyindex"></a><span data-ttu-id="77293-129">RemoveWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="77293-129">RemoveWriterByIndex</span></span>

<span data-ttu-id="77293-130">[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) est utilisé pour supprimer un enregistreur de métadonnées de la collection.</span><span class="sxs-lookup"><span data-stu-id="77293-130">[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) is used to remove a metadata writer from the collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77293-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="77293-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="77293-132">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="77293-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="77293-133">Implémentation de IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="77293-133">Implementing IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[<span data-ttu-id="77293-134">Installation et inscription du CODEC</span><span class="sxs-lookup"><span data-stu-id="77293-134">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="77293-135">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="77293-135">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="77293-136">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="77293-136">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



