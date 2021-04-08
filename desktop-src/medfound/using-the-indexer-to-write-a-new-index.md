---
description: Cette rubrique montre comment écrire un index pour un fichier ASF (Advanced Systems Format).
ms.assetid: a14e3bef-0232-4259-930a-d860ed9230fd
title: Utilisation de l’indexeur pour écrire un nouvel index
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d37922b693c83a8417dea4006fc38397b805fb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753836"
---
# <a name="using-the-indexer-to-write-a-new-index"></a><span data-ttu-id="1957f-103">Utilisation de l’indexeur pour écrire un nouvel index</span><span class="sxs-lookup"><span data-stu-id="1957f-103">Using the Indexer to Write a New Index</span></span>

<span data-ttu-id="1957f-104">Cette rubrique montre comment écrire un index pour un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="1957f-104">This topic shows how to write an index for an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="1957f-105">Voici la procédure générale pour créer un index ASF :</span><span class="sxs-lookup"><span data-stu-id="1957f-105">Here is the general procedure for creating an ASF index:</span></span>

1.  <span data-ttu-id="1957f-106">Initialisez une nouvelle instance de l’objet d’indexeur ASF, comme décrit dans [création et configuration de l’indexeur](indexer-creation-and-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="1957f-106">Initialize a new instance of the ASF indexer object, as described in [Indexer Creation and Configuration](indexer-creation-and-configuration.md).</span></span>
2.  <span data-ttu-id="1957f-107">Éventuellement, configurez l’indexeur.</span><span class="sxs-lookup"><span data-stu-id="1957f-107">Optionally, configure the indexer.</span></span>
3.  <span data-ttu-id="1957f-108">Envoyer des paquets de données ASF à l’indexeur.</span><span class="sxs-lookup"><span data-stu-id="1957f-108">Send ASF data packets to the indexer.</span></span>
4.  <span data-ttu-id="1957f-109">Validez l’index.</span><span class="sxs-lookup"><span data-stu-id="1957f-109">Commit the index.</span></span>
5.  <span data-ttu-id="1957f-110">Obtient l’index terminé de l’indexeur et l’écrit dans un flux.</span><span class="sxs-lookup"><span data-stu-id="1957f-110">Get the completed index from the indexer, and write it to a stream.</span></span>

## <a name="configure-the-indexer"></a><span data-ttu-id="1957f-111">Configurer l’indexeur</span><span class="sxs-lookup"><span data-stu-id="1957f-111">Configure the Indexer</span></span>

<span data-ttu-id="1957f-112">Pour utiliser l’indexeur afin d’écrire un nouvel objet d’index, l’objet indexeur doit avoir l’indexeur d’index MFASF \_ \_ écrire un \_ nouveau jeu d' \_ index avec un appel à [**IMFASFIndexer :: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) avant qu’il ne soit initialisé avec [**IMFASFIndexer :: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize).</span><span class="sxs-lookup"><span data-stu-id="1957f-112">To use the indexer to write a new index object, the indexer object must have the flag MFASF\_INDEXER\_WRITE\_NEW\_INDEX set with a call to [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) before it is initialized with [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize).</span></span>

<span data-ttu-id="1957f-113">Lorsque l’indexeur est configuré pour l’écriture d’un index, l’appelant choisit les flux à indexer.</span><span class="sxs-lookup"><span data-stu-id="1957f-113">When the indexer is configured for writing an index, the caller chooses the streams to be indexed.</span></span> <span data-ttu-id="1957f-114">Par défaut, l’indexeur tente de créer un objet index pour tous les flux.</span><span class="sxs-lookup"><span data-stu-id="1957f-114">By default, the indexer attempts to create an Index Object for all streams.</span></span> <span data-ttu-id="1957f-115">L’intervalle de temps par défaut est d’une seconde.</span><span class="sxs-lookup"><span data-stu-id="1957f-115">The default time interval is one second.</span></span>

<span data-ttu-id="1957f-116">[**IMFASFIndexer :: SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) peut être utilisé pour substituer le choix par défaut des flux et des types d’index de l’objet indexeur.</span><span class="sxs-lookup"><span data-stu-id="1957f-116">[**IMFASFIndexer::SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) can be used to override the indexer object's default choice of streams and index types.</span></span>

<span data-ttu-id="1957f-117">L’exemple de code suivant illustre l’initialisation d’un \_ \_ descripteur d’index ASF et d’un \_ identificateur d’index ASF \_ avant un appel à [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span><span class="sxs-lookup"><span data-stu-id="1957f-117">The following example code shows the initialization of an ASF\_INDEX\_DESCRIPTOR and an ASF\_INDEX\_IDENTIFIER before a call to [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span></span>


```
ASF_INDEX_DESCRIPTOR IndexerType;
ZeroMemory(&IndexerType, sizeof(ASF_INDEX_DESCRIPTOR));

ASF_INDEX_IDENTIFIER IndexIdentifier;
ZeroMemory(&IndexIdentifier, sizeof(ASF_INDEX_IDENTIFIER));

IndexIdentifier.guidIndexType = GUID_NULL;
IndexIdentifier.wStreamNumber = 1;

IndexerType.Identifier = IndexIdentifier;
IndexerType.cPerEntryBytes  = MFASFINDEXER_PER_ENTRY_BYTES_DYNAMIC;
IndexerType.dwInterval  = MFASFINDEXER_NO_FIXED_INTERVAL;

hr = pIndexer->SetIndexStatus((BYTE*)&IndexerType, sizeof(ASF_INDEX_DESCRIPTOR), TRUE);
```



<span data-ttu-id="1957f-118">Le type d’index GUID de l’identificateur d’index doit être défini sur GUID \_ null pour indiquer que le type d’index sera basé sur la durée de la présentation.</span><span class="sxs-lookup"><span data-stu-id="1957f-118">The index identifier must have its GUID index type set to GUID\_NULL to indicate that the index type will be presentation time-based.</span></span> <span data-ttu-id="1957f-119">L’identificateur d’index doit également être initialisé avec le numéro de flux du flux ASF à indexer.</span><span class="sxs-lookup"><span data-stu-id="1957f-119">The index identifier must also be initialized with the stream number of the ASF stream to be indexed.</span></span> <span data-ttu-id="1957f-120">Une fois l’identificateur d’index défini, utilisez-le pour initialiser le descripteur d’index.</span><span class="sxs-lookup"><span data-stu-id="1957f-120">After the index identifier is set, use it to initialize the index descriptor.</span></span>

<span data-ttu-id="1957f-121">La structure du descripteur d’index a des membres qui doivent être définis avant l’appel à [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span><span class="sxs-lookup"><span data-stu-id="1957f-121">The index descriptor structure has members which must be set before the call to [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span></span> <span data-ttu-id="1957f-122">**Identificateur** est une structure [**d' \_ \_ identificateur d’index ASF**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) qui identifie le numéro de flux et le type d’index.</span><span class="sxs-lookup"><span data-stu-id="1957f-122">**Identifier** is an [**ASF\_INDEX\_IDENTIFIER**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) structure that identifies the stream number and the type of index.</span></span> <span data-ttu-id="1957f-123">**cPerEntryBytes** est le nombre d’octets utilisés pour chaque entrée d’index.</span><span class="sxs-lookup"><span data-stu-id="1957f-123">**cPerEntryBytes** is the number of bytes used for each index entry.</span></span> <span data-ttu-id="1957f-124">Si la valeur est MFASFINDEXER \_ par \_ octet d’entrée \_ \_ dynamique, les entrées d’index ont une taille variable.</span><span class="sxs-lookup"><span data-stu-id="1957f-124">If the value is MFASFINDEXER\_PER\_ENTRY\_BYTES\_DYNAMIC, the index entries have variable size.</span></span> <span data-ttu-id="1957f-125">**dwInterval** est l’intervalle d’indexation.</span><span class="sxs-lookup"><span data-stu-id="1957f-125">**dwInterval** is the indexing interval.</span></span> <span data-ttu-id="1957f-126">La valeur MFASFINDEXER \_ aucun \_ intervalle fixe \_ indique qu’il n’y a pas d’intervalle d’indexation fixe.</span><span class="sxs-lookup"><span data-stu-id="1957f-126">A value of MFASFINDEXER\_NO\_FIXED\_INTERVAL indicates that there is no fixed indexing interval.</span></span>

## <a name="send-asf-data-packets-to-the-indexer"></a><span data-ttu-id="1957f-127">Envoyer des paquets de données ASF à l’indexeur</span><span class="sxs-lookup"><span data-stu-id="1957f-127">Send ASF Data Packets to the Indexer</span></span>

<span data-ttu-id="1957f-128">Étant donné que l’indexeur est un objet de niveau WMContainer, il doit être utilisé conjointement avec le multiplexeur lors de la génération de paquets.</span><span class="sxs-lookup"><span data-stu-id="1957f-128">Because the indexer is a WMContainer level object, it must be used in conjunction with the multiplexer during packet generation.</span></span>

<span data-ttu-id="1957f-129">Les paquets renvoyés à partir de [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) peuvent être envoyés à l’objet indexeur par le biais d’appels à [**GenerateIndexEntries**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries) où il crée des entrées d’index pour chaque paquet envoyé.</span><span class="sxs-lookup"><span data-stu-id="1957f-129">Packets returned from [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) can be sent to the indexer object through calls to [**GenerateIndexEntries**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries) where it creates index entries for each packet sent.</span></span>

<span data-ttu-id="1957f-130">Le code suivant illustre cette opération :</span><span class="sxs-lookup"><span data-stu-id="1957f-130">The following code demonstrates how this may be done:</span></span>


```C++
HRESULT SendSampleToMux(
    IMFASFMultiplexer *pMux,
    IMFASFIndexer *pIndex,
    IMFSample *pSample,
    WORD wStream,
    IMFByteStream *pDestStream
    )
{
    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacket = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    HRESULT hr = pMux->ProcessSample(wStream, pSample, 0);
    if (FAILED(hr))
    {
        goto done;
    }

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pOutputSample)
        {
            // Send the data packet to the indexer
            hr = pIndex->GenerateIndexEntries(pOutputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            // Convert the sample to a contiguous buffer.
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacket);
            if (FAILED(hr))
            {
                goto done;
            }

            // Write the buffer to the byte stream.
            hr = WriteBufferToByteStream(pDestStream, pDataPacket, NULL);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        SafeRelease(&pOutputSample);
        SafeRelease(&pDataPacket);
    }

done:
    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacket);
    return hr;
}
```



<span data-ttu-id="1957f-131">Pour plus d’informations, consultez [génération de nouveaux paquets de données ASF](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="1957f-131">For more information, see [Generating New ASF Data Packets](generating-new-asf-data-packets.md).</span></span>

## <a name="commit-the-index"></a><span data-ttu-id="1957f-132">Valider l’index</span><span class="sxs-lookup"><span data-stu-id="1957f-132">Commit the Index</span></span>

<span data-ttu-id="1957f-133">Une fois que le dernier paquet a créé une entrée d’index, l’index doit être validé.</span><span class="sxs-lookup"><span data-stu-id="1957f-133">After the last packet has had an index entry created for it, the index must be committed.</span></span> <span data-ttu-id="1957f-134">Pour ce faire, appelez [**IMFASFIndexer :: CommitIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex).</span><span class="sxs-lookup"><span data-stu-id="1957f-134">This is done with a call to [**IMFASFIndexer::CommitIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex).</span></span> <span data-ttu-id="1957f-135">**CommitIndex** prend un pointeur vers l’objet ContentInfo qui décrit le contenu du fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="1957f-135">**CommitIndex** takes a pointer to the ContentInfo object which describes the content of the ASF file.</span></span> <span data-ttu-id="1957f-136">La validation de l’index termine l’indexation et met à jour l’en-tête avec de nouvelles informations sur la taille de fichier et la capacité de recherche.</span><span class="sxs-lookup"><span data-stu-id="1957f-136">Committing the index finishes the indexing and updates the header with new information about file size and seekability.</span></span>

## <a name="get-the-completed-index"></a><span data-ttu-id="1957f-137">Obtient l’index terminé</span><span class="sxs-lookup"><span data-stu-id="1957f-137">Get the Completed Index</span></span>

<span data-ttu-id="1957f-138">Pour récupérer l’index terminé à partir de l’indexeur, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1957f-138">To get the completed index from the indexer, perform the following steps:</span></span>

1.  <span data-ttu-id="1957f-139">Appelez [**IMFASFIndexer :: GetIndexWriteSpace**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace) pour connaître la taille de l’index.</span><span class="sxs-lookup"><span data-stu-id="1957f-139">Call [**IMFASFIndexer::GetIndexWriteSpace**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace) to get the size of the index.</span></span>
2.  <span data-ttu-id="1957f-140">Appelez [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) pour créer une mémoire tampon de support.</span><span class="sxs-lookup"><span data-stu-id="1957f-140">Call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) to create a media buffer.</span></span> <span data-ttu-id="1957f-141">Vous pouvez allouer une mémoire tampon suffisamment grande pour contenir la totalité de l’index, d’allouer une mémoire tampon plus petite et d’obtenir l’index en segments.</span><span class="sxs-lookup"><span data-stu-id="1957f-141">You can either allocate an buffer that is large enough to hold the entire index, of allocate a smaller buffer and get the index in chunks.</span></span>
3.  <span data-ttu-id="1957f-142">Appelez [**IMFASFIndexer :: GetCompletedIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex) pour récupérer les données d’index.</span><span class="sxs-lookup"><span data-stu-id="1957f-142">Call [**IMFASFIndexer::GetCompletedIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex) to get the index data.</span></span> <span data-ttu-id="1957f-143">Lors du premier appel, définissez le paramètre *cbOffsetWithinIndex* sur zéro.</span><span class="sxs-lookup"><span data-stu-id="1957f-143">On the first call, set the *cbOffsetWithinIndex* parameter to zero.</span></span> <span data-ttu-id="1957f-144">Si vous récupérez l’index en segments, incrémentez les *cbOffsetWithinIndex* à chaque fois par la taille des données de l’appel précédent.</span><span class="sxs-lookup"><span data-stu-id="1957f-144">If you get the index in chunks, increment *cbOffsetWithinIndex* each time by the size of the data from the previous call.</span></span>
4.  <span data-ttu-id="1957f-145">Appelez [**IMFMediaBuffer :: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) pour obtenir un pointeur vers les données d’index et la taille des données.</span><span class="sxs-lookup"><span data-stu-id="1957f-145">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the index data and the size of the data.</span></span>
5.  <span data-ttu-id="1957f-146">Écrire les données d’index dans le fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="1957f-146">Write the index data to the ASF file.</span></span>
6.  <span data-ttu-id="1957f-147">Appelez [**IMFMediaBuffer :: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) pour déverrouiller la mémoire tampon du média.</span><span class="sxs-lookup"><span data-stu-id="1957f-147">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the media buffer.</span></span>
7.  <span data-ttu-id="1957f-148">Répétez les étapes 3 à 6 jusqu’à ce que vous ayez écrit la totalité de l’index.</span><span class="sxs-lookup"><span data-stu-id="1957f-148">Repeat steps 3–6 until you have written the entire index.</span></span>

<span data-ttu-id="1957f-149">Le code suivant illustre ces étapes :</span><span class="sxs-lookup"><span data-stu-id="1957f-149">The following code shows these steps:</span></span>


```C++
HRESULT WriteASFIndex(IMFASFIndexer *pIndex,IMFByteStream *pStream)
{
    const DWORD cbChunkSize = 4096;

    IMFMediaBuffer *pBuffer = NULL;

    QWORD cbIndex = 0;
    DWORD cbIndexWritten = 0;

    HRESULT hr = pIndex->GetIndexWriteSpace(&cbIndex);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateMemoryBuffer(cbChunkSize, &pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    while (cbIndexWritten < cbIndex)
    {
        BYTE *pData = NULL;
        DWORD cbData = 0;
        DWORD cbWritten = 0;

        hr = pIndex->GetCompletedIndex(pBuffer, cbIndexWritten);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pBuffer->Lock(&pData, NULL, &cbData);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStream->Write(pData, cbData, &cbWritten);

        (void)pBuffer->Unlock();

        if (FAILED(hr))
        {
            goto done;
        }

        cbIndexWritten += cbData;
    }

done:
    SafeRelease(&pBuffer);
    return hr;
};
```



## <a name="related-topics"></a><span data-ttu-id="1957f-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1957f-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1957f-151">Indexeur ASF</span><span class="sxs-lookup"><span data-stu-id="1957f-151">ASF Indexer</span></span>](asf-index-object.md)
</dt> </dl>

 

 



