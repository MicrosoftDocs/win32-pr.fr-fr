---
description: L’indexeur ASF est un composant de couche WMContainer utilisé pour lire ou écrire des objets index dans un fichier ASF (Advanced Systems Format). Cette rubrique fournit des informations sur l’utilisation de l’indexeur ASF pour effectuer une recherche dans un fichier ASF.
ms.assetid: 9c501d33-847e-448e-a19c-39dfbc7757ca
title: Utilisation de l’indexeur pour rechercher dans un fichier ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c40c35f876fdc5452c596048d121fb0c2933094a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530636"
---
# <a name="using-the-indexer-to-seek-within-an-asf-file"></a>Utilisation de l’indexeur pour rechercher dans un fichier ASF

L' *indexeur* ASF est un composant de couche WMContainer utilisé pour lire ou écrire des objets index dans un fichier ASF (Advanced Systems Format). Cette rubrique fournit des informations sur l’utilisation de l’indexeur ASF pour effectuer une recherche dans un fichier ASF.

-   [Initialisation de l’indexeur pour la recherche](#initializing-the-indexer-for-seeking)
-   [Obtention de la position de recherche.](#getting-the-seek-position)
-   [Rubriques connexes](#related-topics)

Pour plus d’informations sur la structure d’un fichier ASF, consultez [structure des fichiers ASF](asf-file-structure.md).

## <a name="initializing-the-indexer-for-seeking"></a>Initialisation de l’indexeur pour la recherche

Pour initialiser l’indexeur ASF pour la recherche :

1.  Appelez [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) pour créer une nouvelle instance de l’indexeur ASF.
2.  Appelez [**IMFASFIndexer :: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) pour initialiser l’indexeur. Cette méthode obtient les informations de l’en-tête ASF pour déterminer les flux ASF indexés. Par défaut, l’objet indexeur est configuré pour la recherche.
3.  Appelez [**IMFASFIndexer :: GetIndexPosition**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition) pour rechercher le décalage de l’index dans le fichier ASF.
4.  Appelez la fonction [**MFCreateASFIndexerByteStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexerbytestream) pour créer un flux d’octets pour la lecture de l’index. L’entrée de cette fonction est un pointeur vers un flux d’octets qui contient le fichier ASF et le décalage de l’index (à partir de l’étape précédente).
5.  Appelez [**IMFASFIndexer :: SetIndexByteStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams) pour définir le flux d’octets d’index sur l’indexeur.

Le code suivant illustre ces étapes :


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



## <a name="getting-the-seek-position"></a>Obtention de la position de recherche.

1.  Pour déterminer si un flux de données particulier est indexé, appelez [**IMFASFIndexer :: GetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus). Si le flux est indexé, le paramètre *pfIsIndexed* reçoit la valeur **true**; dans le cas contraire, elle reçoit la valeur **false**.
2.  Par défaut, l’indexeur utilise la recherche vers l’avant. Pour la recherche inversée (autrement dit, la recherche à partir de la fin du fichier), appelez [**IMFASFIndexer :: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) et définissez la valeur de l’indicateur **\_ de lecture de l’indexeur MFASF \_ \_ pour \_ REVERSEPLAYBACK** . Sinon, ignorez cette étape.
3.  Si le flux est indexé, obtenez la position de recherche pour une durée de présentation spécifiée en appelant [**IMFASFIndexer :: GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue). Cette méthode lit l’index ASF et recherche l’entrée d’index la plus proche de l’heure demandée. La méthode retourne l’offset d’octet du paquet de données spécifié par l’entrée d’index. L’offset d’octet est relatif au début de l’objet de données ASF.

La méthode [**GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue) prend un pointeur vers la structure de l' [**\_ \_ identificateur d’index ASF**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) . Cette structure spécifie un type d’index et un identificateur de flux. Actuellement, le type d’index doit être un GUID \_ null, qui spécifie l’indexation basée sur le temps.

Le code suivant obtient une position de recherche, en fonction d’un identificateur de flux et de l’heure de présentation cible. Si l’appel est effectué, il retourne l’offset de données dans le paramètre *pcbDataOffset* et le temps de recherche réel approximatif dans *phnsApproxSeekTime*.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Indexeur ASF](asf-index-object.md)
</dt> </dl>

 

 



