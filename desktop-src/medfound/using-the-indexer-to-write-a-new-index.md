---
description: Cette rubrique montre comment écrire un index pour un fichier ASF (Advanced Systems Format).
ms.assetid: a14e3bef-0232-4259-930a-d860ed9230fd
title: Utilisation de l’indexeur pour écrire un nouvel index
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d37922b693c83a8417dea4006fc38397b805fb71
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530633"
---
# <a name="using-the-indexer-to-write-a-new-index"></a>Utilisation de l’indexeur pour écrire un nouvel index

Cette rubrique montre comment écrire un index pour un fichier ASF (Advanced Systems Format).

Voici la procédure générale pour créer un index ASF :

1.  Initialisez une nouvelle instance de l’objet d’indexeur ASF, comme décrit dans [création et configuration de l’indexeur](indexer-creation-and-configuration.md).
2.  Éventuellement, configurez l’indexeur.
3.  Envoyer des paquets de données ASF à l’indexeur.
4.  Validez l’index.
5.  Obtient l’index terminé de l’indexeur et l’écrit dans un flux.

## <a name="configure-the-indexer"></a>Configurer l’indexeur

Pour utiliser l’indexeur afin d’écrire un nouvel objet d’index, l’objet indexeur doit avoir l’indexeur d’index MFASF \_ \_ écrire un \_ nouveau jeu d' \_ index avec un appel à [**IMFASFIndexer :: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) avant qu’il ne soit initialisé avec [**IMFASFIndexer :: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize).

Lorsque l’indexeur est configuré pour l’écriture d’un index, l’appelant choisit les flux à indexer. Par défaut, l’indexeur tente de créer un objet index pour tous les flux. L’intervalle de temps par défaut est d’une seconde.

[**IMFASFIndexer :: SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) peut être utilisé pour substituer le choix par défaut des flux et des types d’index de l’objet indexeur.

L’exemple de code suivant illustre l’initialisation d’un \_ \_ descripteur d’index ASF et d’un \_ identificateur d’index ASF \_ avant un appel à [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).


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



Le type d’index GUID de l’identificateur d’index doit être défini sur GUID \_ null pour indiquer que le type d’index sera basé sur la durée de la présentation. L’identificateur d’index doit également être initialisé avec le numéro de flux du flux ASF à indexer. Une fois l’identificateur d’index défini, utilisez-le pour initialiser le descripteur d’index.

La structure du descripteur d’index a des membres qui doivent être définis avant l’appel à [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus). **Identificateur** est une structure [**d' \_ \_ identificateur d’index ASF**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) qui identifie le numéro de flux et le type d’index. **cPerEntryBytes** est le nombre d’octets utilisés pour chaque entrée d’index. Si la valeur est MFASFINDEXER \_ par \_ octet d’entrée \_ \_ dynamique, les entrées d’index ont une taille variable. **dwInterval** est l’intervalle d’indexation. La valeur MFASFINDEXER \_ aucun \_ intervalle fixe \_ indique qu’il n’y a pas d’intervalle d’indexation fixe.

## <a name="send-asf-data-packets-to-the-indexer"></a>Envoyer des paquets de données ASF à l’indexeur

Étant donné que l’indexeur est un objet de niveau WMContainer, il doit être utilisé conjointement avec le multiplexeur lors de la génération de paquets.

Les paquets renvoyés à partir de [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) peuvent être envoyés à l’objet indexeur par le biais d’appels à [**GenerateIndexEntries**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries) où il crée des entrées d’index pour chaque paquet envoyé.

Le code suivant illustre cette opération :


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



Pour plus d’informations, consultez [génération de nouveaux paquets de données ASF](generating-new-asf-data-packets.md).

## <a name="commit-the-index"></a>Valider l’index

Une fois que le dernier paquet a créé une entrée d’index, l’index doit être validé. Pour ce faire, appelez [**IMFASFIndexer :: CommitIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex). **CommitIndex** prend un pointeur vers l’objet ContentInfo qui décrit le contenu du fichier ASF. La validation de l’index termine l’indexation et met à jour l’en-tête avec de nouvelles informations sur la taille de fichier et la capacité de recherche.

## <a name="get-the-completed-index"></a>Obtient l’index terminé

Pour récupérer l’index terminé à partir de l’indexeur, procédez comme suit :

1.  Appelez [**IMFASFIndexer :: GetIndexWriteSpace**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace) pour connaître la taille de l’index.
2.  Appelez [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) pour créer une mémoire tampon de support. Vous pouvez allouer une mémoire tampon suffisamment grande pour contenir la totalité de l’index, d’allouer une mémoire tampon plus petite et d’obtenir l’index en segments.
3.  Appelez [**IMFASFIndexer :: GetCompletedIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex) pour récupérer les données d’index. Lors du premier appel, définissez le paramètre *cbOffsetWithinIndex* sur zéro. Si vous récupérez l’index en segments, incrémentez les *cbOffsetWithinIndex* à chaque fois par la taille des données de l’appel précédent.
4.  Appelez [**IMFMediaBuffer :: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) pour obtenir un pointeur vers les données d’index et la taille des données.
5.  Écrire les données d’index dans le fichier ASF.
6.  Appelez [**IMFMediaBuffer :: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) pour déverrouiller la mémoire tampon du média.
7.  Répétez les étapes 3 à 6 jusqu’à ce que vous ayez écrit la totalité de l’index.

Le code suivant illustre ces étapes :


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Indexeur ASF](asf-index-object.md)
</dt> </dl>

 

 



