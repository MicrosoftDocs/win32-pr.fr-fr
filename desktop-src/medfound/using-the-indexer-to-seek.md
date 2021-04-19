---
description: L’indexeur ASF est un composant de couche WMContainer utilisé pour lire ou écrire des objets index dans un fichier ASF (Advanced Systems Format). Cette rubrique fournit des informations sur l’utilisation de l’indexeur ASF pour effectuer une recherche dans un fichier ASF.
ms.assetid: 9c501d33-847e-448e-a19c-39dfbc7757ca
title: Utilisation de l’indexeur pour rechercher dans un fichier ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c40c35f876fdc5452c596048d121fb0c2933094a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517777"
---
# <a name="using-the-indexer-to-seek-within-an-asf-file"></a><span data-ttu-id="2a9dd-104">Utilisation de l’indexeur pour rechercher dans un fichier ASF</span><span class="sxs-lookup"><span data-stu-id="2a9dd-104">Using the Indexer to Seek Within an ASF File</span></span>

<span data-ttu-id="2a9dd-105">L' *indexeur* ASF est un composant de couche WMContainer utilisé pour lire ou écrire des objets index dans un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="2a9dd-105">The ASF *indexer* is a WMContainer layer component that is used to read or write Index Objects in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="2a9dd-106">Cette rubrique fournit des informations sur l’utilisation de l’indexeur ASF pour effectuer une recherche dans un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-106">This topic provides information about using the ASF indexer to seek within an ASF file.</span></span>

-   [<span data-ttu-id="2a9dd-107">Initialisation de l’indexeur pour la recherche</span><span class="sxs-lookup"><span data-stu-id="2a9dd-107">Initializing the Indexer for Seeking</span></span>](#initializing-the-indexer-for-seeking)
-   [<span data-ttu-id="2a9dd-108">Obtention de la position de recherche.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-108">Getting the Seek Position.</span></span>](#getting-the-seek-position)
-   [<span data-ttu-id="2a9dd-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2a9dd-109">Related topics</span></span>](#related-topics)

<span data-ttu-id="2a9dd-110">Pour plus d’informations sur la structure d’un fichier ASF, consultez [structure des fichiers ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="2a9dd-110">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

## <a name="initializing-the-indexer-for-seeking"></a><span data-ttu-id="2a9dd-111">Initialisation de l’indexeur pour la recherche</span><span class="sxs-lookup"><span data-stu-id="2a9dd-111">Initializing the Indexer for Seeking</span></span>

<span data-ttu-id="2a9dd-112">Pour initialiser l’indexeur ASF pour la recherche :</span><span class="sxs-lookup"><span data-stu-id="2a9dd-112">To initialize the ASF indexer for seeking:</span></span>

1.  <span data-ttu-id="2a9dd-113">Appelez [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) pour créer une nouvelle instance de l’indexeur ASF.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-113">Call [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) to create a new instance of the ASF indexer.</span></span>
2.  <span data-ttu-id="2a9dd-114">Appelez [**IMFASFIndexer :: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) pour initialiser l’indexeur.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-114">Call [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) to initialize the indexer.</span></span> <span data-ttu-id="2a9dd-115">Cette méthode obtient les informations de l’en-tête ASF pour déterminer les flux ASF indexés.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-115">This method gets information from the ASF header to determine which ASF streams are indexed.</span></span> <span data-ttu-id="2a9dd-116">Par défaut, l’objet indexeur est configuré pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-116">By default, the indexer object is configured for seeking.</span></span>
3.  <span data-ttu-id="2a9dd-117">Appelez [**IMFASFIndexer :: GetIndexPosition**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition) pour rechercher le décalage de l’index dans le fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-117">Call [**IMFASFIndexer::GetIndexPosition**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition) to find the offset of the index within the ASF file.</span></span>
4.  <span data-ttu-id="2a9dd-118">Appelez la fonction [**MFCreateASFIndexerByteStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexerbytestream) pour créer un flux d’octets pour la lecture de l’index.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-118">Call the [**MFCreateASFIndexerByteStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexerbytestream) function to create a byte stream for reading the index.</span></span> <span data-ttu-id="2a9dd-119">L’entrée de cette fonction est un pointeur vers un flux d’octets qui contient le fichier ASF et le décalage de l’index (à partir de l’étape précédente).</span><span class="sxs-lookup"><span data-stu-id="2a9dd-119">The input to this function is a pointer to a byte stream that contains the ASF file, and the offset of the index (from the previous step).</span></span>
5.  <span data-ttu-id="2a9dd-120">Appelez [**IMFASFIndexer :: SetIndexByteStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams) pour définir le flux d’octets d’index sur l’indexeur.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-120">Call [**IMFASFIndexer::SetIndexByteStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams) to set the index byte stream on the indexer.</span></span>

<span data-ttu-id="2a9dd-121">Le code suivant illustre ces étapes :</span><span class="sxs-lookup"><span data-stu-id="2a9dd-121">The following code shows these steps:</span></span>


```C++
HRESULT CreateASFIndexer(
    IMFByteStream *pContentByteStream,  // Pointer to the content byte stream
    IMFASFContentInfo *pContentInfo,
    IMFASFIndexer **ppIndexer
    )
{
    IMFASFIndexer *pIndexer = NULL;
    IMFByteStream *pIndexerByteStream = NULL;

    QWORD qwLength = 0, qwIndexOffset = 0, qwBytestreamLength = 0;

    // Create the indexer.
    HRESULT hr = MFCreateASFIndexer(&pIndexer);
    if (FAILED(hr))
    {
        goto done;
    }

    //Initialize the indexer to work with this ASF library
    hr =  pIndexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //Check if the index exists. You can only do this after creating the indexer

    //Get byte stream length
    hr = pContentByteStream->GetLength(&qwLength);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get index offset
    hr = pIndexer->GetIndexPosition(pContentInfo, &qwIndexOffset);
    if (FAILED(hr))
    {
        goto done;
    }

    if ( qwIndexOffset >= qwLength)
    {
        //index object does not exist, release the indexer
        goto done;
    }
    else
    {
        // initialize the indexer
        // Create a byte stream that the Indexer will use to read in
        // and parse the indexers.
         hr = MFCreateASFIndexerByteStream(
             pContentByteStream,
             qwIndexOffset,
             &pIndexerByteStream
             );

        if (FAILED(hr))
        {
            goto done;
        }
   }

    hr = pIndexer->SetIndexByteStreams(&pIndexerByteStream, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppIndexer = pIndexer;
    (*ppIndexer)->AddRef();

done:
    SafeRelease(&pIndexer);
    SafeRelease(&pIndexerByteStream);
    return hr;
}
```



## <a name="getting-the-seek-position"></a><span data-ttu-id="2a9dd-122">Obtention de la position de recherche.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-122">Getting the Seek Position.</span></span>

1.  <span data-ttu-id="2a9dd-123">Pour déterminer si un flux de données particulier est indexé, appelez [**IMFASFIndexer :: GetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus).</span><span class="sxs-lookup"><span data-stu-id="2a9dd-123">To find out if a particular stream is indexed, call [**IMFASFIndexer::GetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus).</span></span> <span data-ttu-id="2a9dd-124">Si le flux est indexé, le paramètre *pfIsIndexed* reçoit la valeur **true**; dans le cas contraire, elle reçoit la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-124">If the stream is indexed, the *pfIsIndexed* parameter receives the value **TRUE**; otherwise it receives the value **FALSE**.</span></span>
2.  <span data-ttu-id="2a9dd-125">Par défaut, l’indexeur utilise la recherche vers l’avant.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-125">By default, the indexer uses forward seeking.</span></span> <span data-ttu-id="2a9dd-126">Pour la recherche inversée (autrement dit, la recherche à partir de la fin du fichier), appelez [**IMFASFIndexer :: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) et définissez la valeur de l’indicateur **\_ de lecture de l’indexeur MFASF \_ \_ pour \_ REVERSEPLAYBACK** .</span><span class="sxs-lookup"><span data-stu-id="2a9dd-126">For reverse seeking (that is, seeking from the end of the file), call [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) and set the **MFASF\_INDEXER\_READ\_FOR\_REVERSEPLAYBACK** flag.</span></span> <span data-ttu-id="2a9dd-127">Sinon, ignorez cette étape.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-127">Otherwise, skip this step.</span></span>
3.  <span data-ttu-id="2a9dd-128">Si le flux est indexé, obtenez la position de recherche pour une durée de présentation spécifiée en appelant [**IMFASFIndexer :: GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue).</span><span class="sxs-lookup"><span data-stu-id="2a9dd-128">If the stream is indexed, get the seek position for a specified presentation time by calling [**IMFASFIndexer::GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue).</span></span> <span data-ttu-id="2a9dd-129">Cette méthode lit l’index ASF et recherche l’entrée d’index la plus proche de l’heure demandée.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-129">This method reads the ASF index and finds the index entry that is closest to the requested time.</span></span> <span data-ttu-id="2a9dd-130">La méthode retourne l’offset d’octet du paquet de données spécifié par l’entrée d’index.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-130">The method returns the byte offset of the data packet specified by the index entry.</span></span> <span data-ttu-id="2a9dd-131">L’offset d’octet est relatif au début de l’objet de données ASF.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-131">The byte offset is relative to the start of the ASF Data Object.</span></span>

<span data-ttu-id="2a9dd-132">La méthode [**GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue) prend un pointeur vers la structure de l' [**\_ \_ identificateur d’index ASF**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) .</span><span class="sxs-lookup"><span data-stu-id="2a9dd-132">The [**GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue) method takes a pointer to the [**ASF\_INDEX\_IDENTIFIER**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) structure.</span></span> <span data-ttu-id="2a9dd-133">Cette structure spécifie un type d’index et un identificateur de flux.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-133">This structure specifies an index type and a stream identifier.</span></span> <span data-ttu-id="2a9dd-134">Actuellement, le type d’index doit être un GUID \_ null, qui spécifie l’indexation basée sur le temps.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-134">Currently, the index type must be GUID\_NULL, which specifies time-based indexing.</span></span>

<span data-ttu-id="2a9dd-135">Le code suivant obtient une position de recherche, en fonction d’un identificateur de flux et de l’heure de présentation cible.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-135">The following code gets a seek position, given a stream identifier and target presentation time.</span></span> <span data-ttu-id="2a9dd-136">Si l’appel est effectué, il retourne l’offset de données dans le paramètre *pcbDataOffset* et le temps de recherche réel approximatif dans *phnsApproxSeekTime*.</span><span class="sxs-lookup"><span data-stu-id="2a9dd-136">If the call succeeds, it returns the data offset in the *pcbDataOffset* parameter and the approximate actual seek time in *phnsApproxSeekTime*.</span></span>


```C++
HRESULT GetSeekPositionWithIndexer(
    IMFASFIndexer *pIndexer,
    WORD          wStreamNumber,
    MFTIME        hnsSeekTime,          // Desired seek time, in 100-nsec.
    BOOL          bReverse,
    QWORD         *pcbDataOffset,       // Receives the offset in bytes.
    MFTIME        *phnsApproxSeekTime   // Receives the approximate seek time.
    )
{
    // Query whether the stream is indexed.

    ASF_INDEX_IDENTIFIER IndexIdentifier = { GUID_NULL, wStreamNumber };

    BOOL fIsIndexed = FALSE;

    ASF_INDEX_DESCRIPTOR descriptor;

    DWORD cbIndexDescriptor = sizeof(descriptor);

    HRESULT hr = pIndexer->GetIndexStatus(
        &IndexIdentifier,
        &fIsIndexed,
        (BYTE*)&descriptor,
        &cbIndexDescriptor
        );

    if (hr == MF_E_BUFFERTOOSMALL)
    {
        hr = S_OK;
    }
    else if (FAILED(hr))
    {
        goto done;
    }

    if (!fIsIndexed)
    {
        hr = MF_E_ASF_NOINDEX;
        goto done;
    }

    if (bReverse)
    {
        hr = pIndexer->SetFlags(MFASF_INDEXER_READ_FOR_REVERSEPLAYBACK);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Get the offset from the indexer.

    PROPVARIANT var;

    var.vt = VT_I8;
    var.hVal.QuadPart = hnsSeekTime;

    hr = pIndexer->GetSeekPositionForValue(
        &var,
        &IndexIdentifier,
        pcbDataOffset,
        phnsApproxSeekTime,
        0
        );

done:
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="2a9dd-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2a9dd-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a9dd-138">Indexeur ASF</span><span class="sxs-lookup"><span data-stu-id="2a9dd-138">ASF Indexer</span></span>](asf-index-object.md)
</dt> </dl>

 

 



