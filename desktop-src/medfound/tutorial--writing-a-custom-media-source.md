---
description: Cette rubrique présente en détail l’exemple du kit de développement logiciel (SDK) source de média MPEG-1.
ms.assetid: d392f30c-c963-4eb3-add2-1bb986919c0b
title: 'Étude de cas : source de média MPEG-1'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e1f72cc6ae6df119439bdae1942732bf8d2fa2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104042926"
---
# <a name="case-study-mpeg-1-media-source"></a>Étude de cas : source de média MPEG-1

Dans Microsoft Media Foundation, l’objet qui introduit les données multimédias dans le pipeline de données est appelé une *source de média*. Cette rubrique présente en détail l’exemple du kit de développement logiciel (SDK) [source de média MPEG-1](mpeg1source-sample.md) .

-   [Conditions préalables](#prerequisites)
-   [Classes C++ utilisées dans la source MPEG-1](#c-classes-used-in-the-mpeg-1-source)
-   [Gestionnaire de flux d’octets](#byte-stream-handler)
-   [Descripteur de présentation](#presentation-descriptor)
-   [États de streaming](#streaming-states)
    -   [Start](#start)
    -   [Pause](#pause)
    -   [Stop](#stop)
-   [Exemples de demandes](#sample-requests)
-   [Fin de flux](#end-of-stream)
-   [Opérations asynchrones](#asynchronous-operations)
    -   [File d’attente des opérations](#operation-queue)
-   [Rubriques connexes](#related-topics)

## <a name="prerequisites"></a>Prérequis

Avant de lire cette rubrique, vous devez comprendre les concepts de Media Foundation suivants :

-   [Modèle d’objet de source multimédia](media-source-object-model.md)
-   [Méthodes de rappel asynchrones](asynchronous-callback-methods.md).
-   [Files d’attente de travail](work-queues.md)
-   [Générateurs d’événements de média](media-event-generators.md)
-   [Mémoires tampons de média](media-buffers.md)
-   [Exemples de supports](media-samples.md)
-   [Types de médias](media-types.md)

Vous devez également avoir une compréhension de base de l’architecture Media Foundation, en particulier le rôle des sources multimédias dans le pipeline. (Pour plus d’informations, consultez [sources multimédias](media-sources.md).)

En outre, vous souhaiterez peut-être lire la rubrique [écriture d’une source de média personnalisée](writing-a-custom-media-source.md), qui donne une vue d’ensemble plus générale des étapes décrites ici.

Cette rubrique ne reproduit pas l’intégralité du code de l’exemple du kit de développement logiciel (SDK), car l’exemple est relativement volumineux.

## <a name="c-classes-used-in-the-mpeg-1-source"></a>Classes C++ utilisées dans la source MPEG-1

L’exemple de source MPEG-1 est implémenté avec les classes C++ suivantes :

-   `MPEG1ByteStreamHandler`. Implémente le gestionnaire de flux d’octets pour la source du média. Pour un flux d’octets donné, le gestionnaire de flux d’octets crée une instance de la source.
-   `MPEG1Source`. Implémente la source du média.
-   `MPEG1Stream`. Implémente les objets de flux de média. La source du média crée un `MPEG1Stream` objet pour chaque flux audio ou vidéo dans le flux de données MPEG-1.
-   `Parser`. Analyse le flux de bits MPEG-1. Pour l’essentiel, les détails de cette classe ne sont pas pertinents pour les API Media Foundation.
-   SourceOp, OpQueue : ces deux classes gèrent les opérations asynchrones dans la source du média. (Voir [opérations asynchrones](#asynchronous-operations)).

D’autres classes d’assistance diverses sont décrites plus loin dans cette rubrique.

## <a name="byte-stream-handler"></a>Gestionnaire de Byte-Stream

Le gestionnaire *de flux d’octets* est l’objet qui crée la source du média. Le gestionnaire de flux d’octets est créé par le programme de résolution source ; les applications n’interagissent pas directement avec le gestionnaire de flux d’octets. Le programme de résolution source Découvre le gestionnaire de flux d’octets en recherchant dans le registre. Le gestionnaire est inscrit par une extension de nom de fichier ou un type MIME. Pour la source MPEG-1, le gestionnaire de flux d’octets est inscrit pour l’extension de nom de fichier « . mpg ».

> [!Note]  
> Si vous souhaitez prendre en charge des schémas d’URL personnalisés, vous pouvez également écrire un *Gestionnaire de schéma*. La source MPEG-1 est conçue pour les fichiers locaux et Media Foundation fournit déjà un gestionnaire de schéma pour les URL « file:// ».

 

Le gestionnaire de flux d’octets implémente l’interface [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) . Cette interface a deux méthodes les plus importantes qui doivent être implémentées :

-   [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject). Démarre une opération asynchrone pour créer la source du média.
-   [**EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject). Termine l’appel asynchrone.

Deux autres méthodes sont facultatives et ne sont pas implémentées dans l’exemple du kit de développement logiciel (SDK) :

-   [**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation). Annule la méthode [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) . Cette méthode est utile pour une source réseau qui peut avoir une latence élevée au démarrage.
-   [**GetMaxNumberOfBytesRequiredForResolution**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-getmaxnumberofbytesrequiredforresolution). Obtient le nombre maximal d’octets que le gestionnaire lira à partir du flux source. Implémentez cette méthode si vous savez combien de données le gestionnaire de flux d’octets avant de pouvoir créer la source du média. Dans le cas contraire, renvoyez simplement **E \_ NOTIMPL**.

Voici l’implémentation de la méthode [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) :


```C++
HRESULT MPEG1ByteStreamHandler::BeginCreateObject(
        /* [in] */ IMFByteStream *pByteStream,
        /* [in] */ LPCWSTR pwszURL,
        /* [in] */ DWORD dwFlags,
        /* [in] */ IPropertyStore *pProps,
        /* [out] */ IUnknown **ppIUnknownCancelCookie,  // Can be NULL
        /* [in] */ IMFAsyncCallback *pCallback,
        /* [in] */ IUnknown *punkState                  // Can be NULL
        )
{
    if (pByteStream == NULL)
    {
        return E_POINTER;
    }

    if (pCallback == NULL)
    {
        return E_POINTER;
    }

    if ((dwFlags & MF_RESOLUTION_MEDIASOURCE) == 0)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFAsyncResult *pResult = NULL;
    MPEG1Source    *pSource = NULL;

    // Create an instance of the media source.
    hr = MPEG1Source::CreateInstance(&pSource);

    // Create a result object for the caller's async callback.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateAsyncResult(NULL, pCallback, punkState, &pResult);
    }

    // Start opening the source. This is an async operation.
    // When it completes, the source will invoke our callback
    // and then we will invoke the caller's callback.
    if (SUCCEEDED(hr))
    {
        hr = pSource->BeginOpen(pByteStream, this, NULL);
    }

    if (SUCCEEDED(hr))
    {
        if (ppIUnknownCancelCookie)
        {
            *ppIUnknownCancelCookie = NULL;
        }

        m_pSource = pSource;
        m_pSource->AddRef();

        m_pResult = pResult;
        m_pResult->AddRef();
    }

// cleanup
    SafeRelease(&pSource);
    SafeRelease(&pResult);
    return hr;
}
```



La méthode effectue les étapes suivantes :

1.  Crée une nouvelle instance de l'objet `MPEG1Source`.
2.  Créez un objet de résultat asynchrone. Cet objet est utilisé ultérieurement pour appeler la méthode de rappel de l’outil de résolution source.
3.  Appelle `MPEG1Source::BeginOpen` , une méthode asynchrone définie dans la `MPEG1Source` classe.
4.  Affecte la **valeur null** à *ppIUnknownCancelCookie* , ce qui indique à l’appelant que [**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation) n’est pas pris en charge.

La `MPEG1Source::BeginOpen` méthode effectue le travail réel de lecture du flux d’octets et d’initialisation de l' `MPEG1Source` objet. Cette méthode ne fait pas partie de l’API publique. Vous pouvez définir n’importe quel mécanisme entre le gestionnaire et la source du média qui répond à vos besoins. Le fait de placer la majeure partie de la logique dans la source du média permet de conserver un gestionnaire de flux d’octets relativement simple.

En bref, `BeginOpen` effectue les opérations suivantes :

1.  Appelle [**IMFByteStream :: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) pour vérifier que le flux d’octets source est à la fois lisible et pouvant être recherché.
2.  Appelle [**IMFByteStream :: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) pour démarrer une requête d’e/s asynchrone.

Le reste de l’initialisation se produit de façon asynchrone. La source du média lit suffisamment de données à partir du flux pour analyser les en-têtes de séquence MPEG-1. Ensuite, il crée un *descripteur de présentation*, qui est l’objet utilisé pour décrire les flux audio et vidéo dans le fichier. (Pour plus d’informations, consultez [descripteur de présentation](#presentation-descriptor).) Lorsque l' `BeginOpen` opération est terminée, le gestionnaire de flux d’octets appelle la méthode de rappel de l’outil de résolution source. À ce stade, le programme de résolution source appelle [**IMFByteStreamHandler :: EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject). La méthode **EndCreateObject** retourne l’état de l’opération.


```C++
HRESULT MPEG1ByteStreamHandler::EndCreateObject(
        /* [in] */ IMFAsyncResult *pResult,
        /* [out] */ MF_OBJECT_TYPE *pObjectType,
        /* [out] */ IUnknown **ppObject)
{
    if (pResult == NULL || pObjectType == NULL || ppObject == NULL)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    *pObjectType = MF_OBJECT_INVALID;
    *ppObject = NULL;

    hr = pResult->GetStatus();

    if (SUCCEEDED(hr))
    {
        *pObjectType = MF_OBJECT_MEDIASOURCE;

        assert(m_pSource != NULL);

        hr = m_pSource->QueryInterface(IID_PPV_ARGS(ppObject));
    }

    SafeRelease(&m_pSource);
    SafeRelease(&m_pResult);
    return hr;
}
```



Si une erreur se produit à tout moment pendant ce processus, le rappel est appelé avec un code d’état d’erreur.

## <a name="presentation-descriptor"></a>Descripteur de présentation

Le descripteur de présentation décrit le contenu du fichier MPEG-1, y compris les informations suivantes :

-   Nombre de flux.
-   Format de chaque flux.
-   Identificateurs de flux.
-   État de sélection de chaque flux (sélectionné ou désélectionné).

En termes d’architecture Media Foundation, le descripteur de présentation contient un ou plusieurs *descripteurs de flux*. Chaque descripteur de flux contient un *Gestionnaire de type de média* qui est utilisé pour obtenir ou définir des types de média sur le flux. Media Foundation fournit des implémentations de stock pour le descripteur de présentation et le descripteur de flux ; celles-ci conviennent à la plupart des sources multimédias.

Pour créer un descripteur de présentation, procédez comme suit :

1.  Pour chaque flux :
    1.  Fournissez un ID de flux et un tableau de types de média possibles. Si le flux prend en charge plusieurs types de média, classez la liste des types de médias par préférence, le cas échéant. (Placez d’abord le type optimal et le type le moins optimal).
    2.  Appelez [**MFCreateStreamDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) pour créer le descripteur de flux.
    3.  Appelez [**IMFStreamDescriptor :: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) sur le descripteur de flux que vous venez de créer.
    4.  Appelez [**IMFMediaTypeHandler :: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) pour définir le format par défaut du flux. S’il existe plusieurs types de média, vous devez généralement définir le premier type dans la liste.
2.  Appelez [**MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) et transmettez le tableau de pointeurs de descripteur de flux.
3.  Pour chaque flux, appelez [**IMFPresentationDescriptor :: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) ou [**DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) pour définir l’état de sélection par défaut. S’il existe plusieurs flux du même type (audio ou vidéo), un seul doit être sélectionné par défaut.

L' `MPEG1Source` objet crée le descripteur de présentation dans sa `InitPresentationDescriptor` méthode :


```C++
HRESULT MPEG1Source::InitPresentationDescriptor()
{
    HRESULT hr = S_OK;
    DWORD cStreams = 0;

    assert(m_pPresentationDescriptor == NULL);
    assert(m_state == STATE_OPENING);

    if (m_pHeader == NULL)
    {
        return E_FAIL;
    }

    // Get the number of streams, as declared in the MPEG-1 header, skipping
    // any streams with an unsupported format.
    for (DWORD i = 0; i < m_pHeader->cStreams; i++)
    {
        if (IsStreamTypeSupported(m_pHeader->streams[i].type))
        {
            cStreams++;
        }
    }

    // How many streams do we actually have?
    if (cStreams > m_streams.GetCount())
    {
        // Keep reading data until we have seen a packet for each stream.
        return S_OK;
    }

    // We should never create a stream we don't support.
    assert(cStreams == m_streams.GetCount());

    // Ready to create the presentation descriptor.

    // Create an array of IMFStreamDescriptor pointers.
    IMFStreamDescriptor **ppSD =
            new (std::nothrow) IMFStreamDescriptor*[cStreams];

    if (ppSD == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    ZeroMemory(ppSD, cStreams * sizeof(IMFStreamDescriptor*));

    // Fill the array by getting the stream descriptors from the streams.
    for (DWORD i = 0; i < cStreams; i++)
    {
        hr = m_streams[i]->GetStreamDescriptor(&ppSD[i]);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Create the presentation descriptor.
    hr = MFCreatePresentationDescriptor(cStreams, ppSD,
        &m_pPresentationDescriptor);

    if (FAILED(hr))
    {
        goto done;
    }

    // Select the first video stream (if any).
    for (DWORD i = 0; i < cStreams; i++)
    {
        GUID majorType = GUID_NULL;

        hr = GetStreamMajorType(ppSD[i], &majorType);
        if (FAILED(hr))
        {
            goto done;
        }

        if (majorType == MFMediaType_Video)
        {
            hr = m_pPresentationDescriptor->SelectStream(i);
            if (FAILED(hr))
            {
                goto done;
            }
            break;
        }
    }

    // Switch state from "opening" to stopped.
    m_state = STATE_STOPPED;

    // Invoke the async callback to complete the BeginOpen operation.
    hr = CompleteOpen(S_OK);

done:
    // clean up:
    if (ppSD)
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            SafeRelease(&ppSD[i]);
        }
        delete [] ppSD;
    }
    return hr;
}
```



L’application obtient le descripteur de présentation en appelant [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). Cette méthode crée une copie superficielle du descripteur de présentation en appelant [**IMFPresentationDescriptor :: Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone). (La copie contient des pointeurs vers les descripteurs de flux d’origine.) L’application peut utiliser le descripteur de présentation pour définir le type de média, sélectionner un flux ou désélectionner un flux.

Si vous le souhaitez, les descripteurs de présentation et les descripteurs de flux peuvent contenir des attributs qui fournissent des informations supplémentaires sur la source. Pour obtenir la liste de ces attributs, consultez les rubriques suivantes :

-   [Attributs du descripteur de présentation](presentation-descriptor-attributes.md)
-   [Attributs du descripteur de flux](stream-descriptor-attributes.md)

Un attribut mérite une mention spéciale : l’attribut de [**\_ \_ durée MF PD**](mf-pd-duration-attribute.md) contient la durée totale de la source. Définissez cet attribut si vous connaissez la durée en amont ; par exemple, la durée peut être spécifiée dans les en-têtes de fichier, selon le format de fichier. L’application peut afficher cette valeur ou l’utiliser pour définir une barre de progression ou une barre de recherche.

## <a name="streaming-states"></a>États de streaming

Une source de média définit les États suivants :



| State    | Description                                                                                                     |
|----------|-----------------------------------------------------------------------------------------------------------------|
| Démarré  | La source accepte et traite les exemples de demandes.                                                               |
| Suspendu   | La source accepte les exemples de demandes, mais ne les traite pas. Les demandes sont mises en file d’attente jusqu’au démarrage de la source. |
| Arrêté. | La source rejette les exemples de demandes.                                                                             |



 

### <a name="start"></a>Démarrer

La méthode [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) démarre la source du média. Les paramètres suivants sont pris en compte :

-   Descripteur de présentation.
-   GUID de format d’heure.
-   Position de départ.

L’application doit obtenir le descripteur de présentation en appelant [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) sur la source. Il n’existe aucun mécanisme défini pour valider un descripteur de présentation. Si l’application spécifie un descripteur de présentation incorrect, les résultats ne sont pas définis.

Le GUID de format de temps spécifie comment interpréter la position de départ. Le format standard est de 100-nanosecondes (NS) unités, indiquées par la \_ valeur Guid null. Chaque source de média doit prendre en charge les unités 100-ns. Éventuellement, une source peut prendre en charge d’autres unités de temps, telles que le nombre d’images ou le code de temps. Toutefois, il n’existe pas de méthode standard pour interroger une source de média pour obtenir la liste des formats de temps qu’elle prend en charge.

La position de début est fournie en tant que **PROPVARIANT**, ce qui permet d’obtenir des types de données différents en fonction du format d’heure. Pour 100-ns, le type **PROPVARIANT** est à la fois **VT \_ i8** ou **VT \_ vide**. Si **VT \_ i8**, **PROPVARIANT** contient la position de début dans les unités 100-ns. La valeur « **VT \_ vide** » a la signification spéciale « démarrer à la position actuelle ».

Implémentez la méthode [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) comme suit :

1.  Valider les paramètres et l’État :
    -   Recherchez les paramètres **null** .
    -   Vérifiez le GUID de format de l’heure. Si la valeur n’est pas valide, retourne le **\_ format d’heure MF E non \_ pris en \_ \_ charge**.
    -   Vérifiez le type de données du **PROPVARIANT** qui contient la position de début.
    -   Validez la position de départ. Si ce n’est pas le cas, retournez **MF \_ E \_ INVALIDREQUEST**.
    -   Si la source a été arrêtée, retourne **MF \_ E \_ Shutdown**.
2.  Si aucune erreur ne se produit à l’étape 1, met en file d’attente une opération asynchrone. Tout après cette étape se produit sur un thread de file d’attente de travail.
3.  Pour chaque flux :
    1.  Vérifiez si le flux est déjà actif à partir d’une demande de [**démarrage**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) précédente.
    2.  Appelez [**IMFPresentationDescriptor :: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) pour vérifier si l’application a sélectionné ou désélectionné le flux.
    3.  Si un flux précédemment sélectionné est désélectionné, videz les exemples non remis pour ce flux.
    4.  Si le flux est actif, la source du média (pas le flux) envoie l’un des événements suivants :
        -   Elle envoie [MEUpdatedStream](meupdatedstream.md) si le flux était précédemment actif.
        -   Sinon, elle envoie [MENewStream](menewstream.md).

        Pour les deux événements, les données d’événement sont le pointeur [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) pour le flux.
    5.  Si la source redémarre à partir de l’état suspendu, des exemples de demandes sont peut-être en attente. Si c’est le cas, fournissez-les maintenant.
    6.  Si la source recherche une nouvelle position, chaque objet de flux envoie un événement [MEStreamSeeked](mestreamseeked.md) . Dans le cas contraire, chaque flux envoie un événement [MEStreamStarted](mestreamstarted.md) .
4.  Si la source recherche une nouvelle position, la source du média envoie un événement [MESourceSeeked](mesourceseeked.md) . Sinon, elle envoie un événement [MESourceStarted](mesourcestarted.md) .

Si une erreur se produit à tout moment après l’étape 2, la source envoie un événement [MESourceStarted](mesourcestarted.md) avec un code d’erreur. Cette alerte signale à l’application que la méthode [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) a échoué de manière asynchrone.

Le code suivant illustre les étapes 1 à 2 :


```C++
HRESULT MPEG1Source::Start(
        IMFPresentationDescriptor* pPresentationDescriptor,
        const GUID* pguidTimeFormat,
        const PROPVARIANT* pvarStartPos
    )
{

    HRESULT hr = S_OK;
    SourceOp *pAsyncOp = NULL;

    // Check parameters.

    // Start position and presentation descriptor cannot be NULL.
    if (pvarStartPos == NULL || pPresentationDescriptor == NULL)
    {
        return E_INVALIDARG;
    }

    // Check the time format.
    if ((pguidTimeFormat != NULL) && (*pguidTimeFormat != GUID_NULL))
    {
        // Unrecognized time format GUID.
        return MF_E_UNSUPPORTED_TIME_FORMAT;
    }

    // Check the data type of the start position.
    if ((pvarStartPos->vt != VT_I8) && (pvarStartPos->vt != VT_EMPTY))
    {
        return MF_E_UNSUPPORTED_TIME_FORMAT;
    }

    EnterCriticalSection(&m_critSec);

    // Check if this is a seek request. This sample does not support seeking.

    if (pvarStartPos->vt == VT_I8)
    {
        // If the current state is STOPPED, then position 0 is valid.
        // Otherwise, the start position must be VT_EMPTY (current position).

        if ((m_state != STATE_STOPPED) || (pvarStartPos->hVal.QuadPart != 0))
        {
            hr = MF_E_INVALIDREQUEST;
            goto done;
        }
    }

    // Fail if the source is shut down.
    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Fail if the source was not initialized yet.
    hr = IsInitialized();
    if (FAILED(hr))
    {
        goto done;
    }

    // Perform a basic check on the caller's presentation descriptor.
    hr = ValidatePresentationDescriptor(pPresentationDescriptor);
    if (FAILED(hr))
    {
        goto done;
    }

    // The operation looks OK. Complete the operation asynchronously.
    hr = SourceOp::CreateStartOp(pPresentationDescriptor, &pAsyncOp);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAsyncOp->SetData(*pvarStartPos);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = QueueOperation(pAsyncOp);

done:
    SafeRelease(&pAsyncOp);
    LeaveCriticalSection(&m_critSec);
    return hr;
}
```



Les étapes restantes sont présentées dans l’exemple suivant :


```C++
HRESULT MPEG1Source::DoStart(StartOp *pOp)
{
    assert(pOp->Op() == SourceOp::OP_START);

    IMFPresentationDescriptor *pPD = NULL;
    IMFMediaEvent  *pEvent = NULL;

    HRESULT     hr = S_OK;
    LONGLONG    llStartOffset = 0;
    BOOL        bRestartFromCurrentPosition = FALSE;
    BOOL        bSentEvents = FALSE;

    hr = BeginAsyncOp(pOp);

    // Get the presentation descriptor from the SourceOp object.
    // This is the PD that the caller passed into the Start() method.
    // The PD has already been validated.
    if (SUCCEEDED(hr))
    {
        hr = pOp->GetPresentationDescriptor(&pPD);
    }

    // Because this sample does not support seeking, the start
    // position must be 0 (from stopped) or "current position."

    // If the sample supported seeking, we would need to get the
    // start position from the PROPVARIANT data contained in pOp.

    if (SUCCEEDED(hr))
    {
        // Select/deselect streams, based on what the caller set in the PD.
        // This method also sends the MENewStream/MEUpdatedStream events.
        hr = SelectStreams(pPD, pOp->Data());
    }

    if (SUCCEEDED(hr))
    {
        m_state = STATE_STARTED;

        // Queue the "started" event. The event data is the start position.
        hr = m_pEventQueue->QueueEventParamVar(
            MESourceStarted,
            GUID_NULL,
            S_OK,
            &pOp->Data()
            );
    }

    if (FAILED(hr))
    {
        // Failure. Send the error code to the application.

        // Note: It's possible that QueueEvent itself failed, in which case it
        // is likely to fail again. But there is no good way to recover in
        // that case.

        (void)m_pEventQueue->QueueEventParamVar(
            MESourceStarted, GUID_NULL, hr, NULL);
    }

    CompleteAsyncOp(pOp);

    SafeRelease(&pEvent);
    SafeRelease(&pPD);
    return hr;
}
```



### <a name="pause"></a>Suspendre

La méthode [**IMFMediaSource ::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) interrompt la source du média. Implémentez cette méthode comme suit :

1.  Met en file d’attente une opération asynchrone.
2.  Chaque flux actif envoie un événement [MEStreamPaused](mestreampaused.md) .
3.  La source du média envoie un événement [MESourcePaused](mesourcepaused.md) .

Pendant la suspension, la source met en file d’attente les exemples de demandes sans les traiter. (Consultez [exemples de demandes](#sample-requests).)

### <a name="stop"></a>Arrêter

La méthode [**IMFMediaSource :: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) arrête la source du média. Implémentez cette méthode comme suit :

1.  Met en file d’attente une opération asynchrone.
2.  Chaque flux actif envoie un événement [MEStreamStopped](mestreamstopped.md) .
3.  Effacez tous les échantillons en file d’attente et les exemples de demandes.
4.  La source du média envoie un événement [MESourceStopped](mesourcestopped.md) .

Lorsqu’il est arrêté, la source rejette toutes les demandes pour les exemples.

Si la source est arrêtée alors qu’une demande d’e/s est en cours, la requête d’e/s peut se terminer une fois que la source passe à l’état arrêté. Dans ce cas, la source doit ignorer le résultat de cette requête d’e/s.

## <a name="sample-requests"></a>Exemple de demande

Media Foundation utiliser un modèle d' *extraction* , dans lequel le pipeline demande des exemples à partir de la source du média. Cela diffère du modèle utilisé par DirectShow, dans lequel les « push » sont des exemples.

Pour demander un nouvel exemple, le pipeline Media Foundation appelle [**IMFMediaStream :: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample). Cette méthode prend un pointeur **IUnknown** qui représente un objet de *jeton* . L’implémentation de l’objet de jeton est jusqu’à l’appelant ; Il permet simplement à l’appelant de suivre les exemples de demandes. Le paramètre token peut également avoir la **valeur null**.

En supposant que la source utilise des demandes d’e/s asynchrones pour lire les données, l’exemple de génération ne sera pas synchronisé avec les exemples de demandes. Pour synchroniser les exemples de demandes avec l’exemple de génération, une source de média effectue les opérations suivantes :

1.  Les jetons de demande sont placés dans une file d’attente.
2.  À mesure que des exemples sont générés, ils sont placés sur une deuxième file d’attente.
3.  La source du média termine un exemple de demande en extrayant un jeton de demande de la première file d’attente et un échantillon de la deuxième file d’attente.
4.  La source du média envoie un événement MEMediaSample. L’événement contient un pointeur vers l’exemple et l’exemple contient un pointeur vers le jeton.

Le diagramme suivant montre la relation entre l’événement [MEMediaSample](memediasample.md) , l’exemple et le jeton de demande.

![Diagramme montrant memediasample et un exemple de file d’attente pointant vers imfsample ; imfsample et la file d’attente de demandes pointent vers IUnknown](images/mediasourceimpl01.png)

L’exemple de source MPEG-1 implémente ce processus comme suit :

1.  La méthode [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) place la demande sur une file d’attente FIFO.
2.  À mesure que les demandes d’e/s sont terminées, la source du média crée de nouveaux exemples et les place dans une deuxième file d’attente FIFO. (Cette file d’attente a une taille maximale, afin d’éviter que la source ne lise trop loin.)
3.  Lorsque ces deux files d’attente ont au moins un élément (une demande et un exemple), la source du média termine la première requête de la file d’attente de demandes en envoyant le premier échantillon de la file d’attente de l’exemple.
4.  Pour remettre un exemple, l’objet de flux (et non l’objet source) envoie un événement [MEMediaSample](memediasample.md) .
    -   Les données d’événement sont un pointeur vers l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) de l’exemple.
    -   Si la demande incluait un jeton, attachez le jeton à l’exemple en définissant l’attribut de [**\_ jeton MFSampleExtension**](mfsampleextension-token-attribute.md) sur l’exemple.

À ce stade, il existe trois possibilités :

-   Il existe un autre échantillon dans la file d’attente de l’exemple, mais aucune demande correspondante.
-   Il existe une demande, mais pas d’exemple.
-   Les deux files d’attente sont vides ; Il n’y a aucun échantillon et aucune demande.

Si la file d’attente de l’exemple est vide, la source vérifie la fin du flux (voir la [fin du flux](#end-of-stream)). Dans le cas contraire, elle démarre une autre demande d’e/s de données. Si une erreur se produit pendant ce processus, le flux envoie un événement [MEError](meerror.md) .

Le code suivant implémente la méthode [**IMFMediaStream :: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) :


```C++
HRESULT MPEG1Stream::RequestSample(IUnknown* pToken)
{
    HRESULT hr = S_OK;
    IMFMediaSource *pSource = NULL;

    // Hold the media source object's critical section.
    SourceLock lock(m_pSource);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_state == STATE_STOPPED)
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    if (!m_bActive)
    {
        // If the stream is not active, it should not get sample requests.
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    if (m_bEOS && m_Samples.IsEmpty())
    {
        // This stream has already reached the end of the stream, and the
        // sample queue is empty.
        hr = MF_E_END_OF_STREAM;
        goto done;
    }

    hr = m_Requests.InsertBack(pToken);
    if (FAILED(hr))
    {
        goto done;
    }

    // Dispatch the request.
    hr = DispatchSamples();
    if (FAILED(hr))
    {
        goto done;
    }

done:
    if (FAILED(hr) && (m_state != STATE_SHUTDOWN))
    {
        // An error occurred. Send an MEError even from the source,
        // unless the source is already shut down.
        hr = m_pSource->QueueEvent(MEError, GUID_NULL, hr, NULL);
    }
    return hr;
}
```



La `DispatchSamples` méthode extrait des exemples de la file d’attente de l’exemple, les met en correspondance avec des exemples de demandes en attente et met en file d’attente les événements [MEMediaSample](memediasample.md) :


```C++
HRESULT MPEG1Stream::DispatchSamples()
{
    HRESULT hr = S_OK;
    BOOL bNeedData = FALSE;
    BOOL bEOS = FALSE;

    SourceLock lock(m_pSource);

    // An I/O request can complete after the source is paused, stopped, or
    // shut down. Do not deliver samples unless the source is running.
    if (m_state != STATE_STARTED)
    {
        return S_OK;
    }

    IMFSample *pSample = NULL;
    IUnknown  *pToken = NULL;

    // Deliver as many samples as we can.
    while (!m_Samples.IsEmpty() && !m_Requests.IsEmpty())
    {
        // Pull the next sample from the queue.
        hr = m_Samples.RemoveFront(&pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Pull the next request token from the queue. Tokens can be NULL.
        hr = m_Requests.RemoveFront(&pToken);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pToken)
        {
            // Set the token on the sample.
            hr = pSample->SetUnknown(MFSampleExtension_Token, pToken);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Send an MEMediaSample event with the sample.
        hr = m_pEventQueue->QueueEventParamUnk(
            MEMediaSample, GUID_NULL, S_OK, pSample);

        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pSample);
        SafeRelease(&pToken);
    }

    if (m_Samples.IsEmpty() && m_bEOS)
    {
        // The sample queue is empty AND we have reached the end of the source
        // stream. Notify the pipeline by sending the end-of-stream event.

        hr = m_pEventQueue->QueueEventParamVar(
            MEEndOfStream, GUID_NULL, S_OK, NULL);

        if (FAILED(hr))
        {
            goto done;
        }

        // Notify the source. It will send the end-of-presentation event.
        hr = m_pSource->QueueAsyncOperation(SourceOp::OP_END_OF_STREAM);
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (NeedsData())
    {
        // The sample queue is empty; the request queue is not empty; and we
        // have not reached the end of the stream. Ask for more data.
        hr = m_pSource->QueueAsyncOperation(SourceOp::OP_REQUEST_DATA);
        if (FAILED(hr))
        {
            goto done;
        }
    }

done:
    if (FAILED(hr) && (m_state != STATE_SHUTDOWN))
    {
        // An error occurred. Send an MEError even from the source,
        // unless the source is already shut down.
        m_pSource->QueueEvent(MEError, GUID_NULL, hr, NULL);
    }

    SafeRelease(&pSample);
    SafeRelease(&pToken);
    return S_OK;
}
```



La `DispatchSamples` méthode est appelée dans les circonstances suivantes :

-   À l’intérieur de la méthode [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .
-   Lorsque la source du média redémarre à partir de l’état suspendu.
-   Quand une demande d’e/s se termine.

## <a name="end-of-stream"></a>Fin de flux

Lorsqu’un flux ne contient plus de données et que tous les exemples de ce flux ont été remis, les objets de flux envoient un événement [MEEndOfStream](meendofstream.md) .

Lorsque tous les flux actifs sont terminés, la source du média envoie un événement [MEEndOfPresentation](meendofpresentation.md) .

## <a name="asynchronous-operations"></a>Opérations asynchrones

La partie la plus difficile de l’écriture d’une source de média est peut-être la compréhension du modèle asynchrone Media Foundation.

Toutes les méthodes sur une source multimédia qui contrôlent la diffusion en continu sont asynchrones. Dans chaque cas, la méthode effectue une validation initiale, telle que la vérification des paramètres. La source distribue ensuite le reste du travail à une file d’attente de travail. Une fois l’opération terminée, la source du média renvoie un événement à l’appelant, via l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) de la source du média. Il est donc important de comprendre les files d’attente de travail.

Pour placer un élément dans une file d’attente de travail, vous pouvez appeler [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) ou [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex). La source MPEG-1 utilise **MFPutWorkItem**, mais les deux fonctions font la même chose. La fonction **MFPutWorkItem** accepte les paramètres suivants :

-   Valeur **DWORD** qui identifie la file d’attente de travail. Vous pouvez créer une file d’attente de travail privée ou utiliser la **\_ \_ \_ norme de file d’attente de rappel MFASYNC**.
-   Pointeur vers l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . Cette interface de rappel est appelée pour effectuer le travail.
-   Objet d’État facultatif, qui doit implémenter **IUnknown**.

La file d’attente de travail est desservie par un ou plusieurs threads de travail qui extraient en permanence l’élément de travail suivant de la file d’attente et appellent la méthode [**IMFAsyncCallback :: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) de l’interface de rappel.

Il n’est pas garanti que les éléments de travail s’exécutent dans le même ordre que celui dans lequel ils sont placés dans la file d’attente. N’oubliez pas que plusieurs threads peuvent traiter la même file d’attente de travail, de sorte que les appels [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) peuvent se chevaucher ou se produire dans le désordre. Par conséquent, il revient à la source du média de conserver l’état interne correct, en envoyant les éléments de la file d’attente de travail dans le bon ordre. La source démarre l’opération suivante uniquement lorsque l’opération précédente est terminée.

Pour représenter des opérations en attente, la source MPEG-1 définit une classe nommée `SourceOp` :


```C++
// Represents a request for an asynchronous operation.

class SourceOp : public IUnknown
{
public:

    enum Operation
    {
        OP_START,
        OP_PAUSE,
        OP_STOP,
        OP_REQUEST_DATA,
        OP_END_OF_STREAM
    };

    static HRESULT CreateOp(Operation op, SourceOp **ppOp);
    static HRESULT CreateStartOp(IMFPresentationDescriptor *pPD, SourceOp **ppOp);

    // IUnknown
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    SourceOp(Operation op);
    virtual ~SourceOp();

    HRESULT SetData(const PROPVARIANT& var);

    Operation Op() const { return m_op; }
    const PROPVARIANT& Data() { return m_data;}

protected:
    long        m_cRef;     // Reference count.
    Operation   m_op;
    PROPVARIANT m_data;     // Data for the operation.
};
```



L' `Operation` énumération identifie l’opération en attente. La classe contient également un **PROPVARIANT** pour transmettre des données supplémentaires pour l’opération.

### <a name="operation-queue"></a>File d’attente des opérations

Pour sérialiser des opérations, la source du média gère une file d’attente d' `SourceOp` objets. Elle utilise une classe d’assistance pour gérer la file d’attente :


```C++
template <class OP_TYPE>
class OpQueue : public IUnknown
{
public:

    typedef ComPtrList<OP_TYPE>   OpList;

    HRESULT QueueOperation(OP_TYPE *pOp);

protected:

    HRESULT ProcessQueue();
    HRESULT ProcessQueueAsync(IMFAsyncResult *pResult);

    virtual HRESULT DispatchOperation(OP_TYPE *pOp) = 0;
    virtual HRESULT ValidateOperation(OP_TYPE *pOp) = 0;

    OpQueue(CRITICAL_SECTION& critsec)
        : m_OnProcessQueue(this, &OpQueue::ProcessQueueAsync),
          m_critsec(critsec)
    {
    }

    virtual ~OpQueue()
    {
    }

protected:
    OpList                  m_OpQueue;         // Queue of operations.
    CRITICAL_SECTION&       m_critsec;         // Protects the queue state.
    AsyncCallback<OpQueue>  m_OnProcessQueue;  // ProcessQueueAsync callback.
};
```



La `OpQueue` classe est conçue pour être héritée par le composant qui exécute des éléments de travail asynchrones. Le paramètre de modèle de *\_ type op* est le type d’objet utilisé pour représenter les éléments de travail dans la file d’attente. dans ce cas, le *\_ type d’opération* est `SourceOp` . La `OpQueue` classe implémente les méthodes suivantes :

-   `QueueOperation` place un nouvel élément dans la file d’attente.
-   `ProcessQueue` distribue l’opération suivante à partir de la file d’attente. Cette méthode est asynchrone.
-   `ProcessQueueAsync` termine la `ProcessQueue` méthode asynchrone.

Les deux autres méthodes doivent être implémentées par la classe dérivée :

-   `ValidateOperation` vérifie s’il est valide d’effectuer une opération spécifiée, en fonction de l’état actuel de la source du média.
-   `DispatchOperation` exécute l’élément de travail asynchrone.

La file d’attente des opérations est utilisée comme suit :

1.  Le pipeline Media Foundation appelle une méthode asynchrone sur la source du média, par exemple [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).
2.  La méthode asynchrone appelle `QueueOperation` , qui place l’opération [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) sur la file d’attente et appelle `ProcessQueue` (sous la forme d’un `SourceOp` objet).
3.  `ProcessQueue` appelle [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).
4.  Le thread de file d’attente de travail appelle `ProcessQueueAsync` .
5.  La `ProcessQueueAsync` méthode appelle `ValidateOperation` et `DispatchOperation` .

Le code suivant met en file d’attente une nouvelle opération sur la source MPEG-1 :


```C++
template <class OP_TYPE>
HRESULT OpQueue<OP_TYPE>::QueueOperation(OP_TYPE *pOp)
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_critsec);

    hr = m_OpQueue.InsertBack(pOp);
    if (SUCCEEDED(hr))
    {
        hr = ProcessQueue();
    }

    LeaveCriticalSection(&m_critsec);
    return hr;
}
```



Le code suivant traite la file d’attente :


```C++
template <class OP_TYPE>
HRESULT OpQueue<OP_TYPE>::ProcessQueue()
{
    HRESULT hr = S_OK;
    if (m_OpQueue.GetCount() > 0)
    {
        hr = MFPutWorkItem(
            MFASYNC_CALLBACK_QUEUE_STANDARD,    // Use the standard work queue.
            &m_OnProcessQueue,                  // Callback method.
            NULL                                // State object.
            );
    }
    return hr;
}
```



La `ValidateOperation` méthode vérifie si la source MPEG-1 peut distribuer la prochaine opération dans la file d’attente. Si une autre opération est en cours, `ValidateOperation` retourne **MF \_ E \_ NOTACCEPTING**. Cela permet de `DispatchOperation` s’assurer que n’est pas appelé alors qu’une autre opération est en attente.


```C++
HRESULT MPEG1Source::ValidateOperation(SourceOp *pOp)
{
    if (m_pCurrentOp != NULL)
    {
        return MF_E_NOTACCEPTING;
    }
    return S_OK;
}
```



La méthode DispatchOperation bascule sur le type d’opération :


```C++
//-------------------------------------------------------------------
// DispatchOperation
//
// Performs the asynchronous operation indicated by pOp.
//
// NOTE:
// This method implements the pure-virtual OpQueue::DispatchOperation
// method. It is always called from a work-queue thread.
//-------------------------------------------------------------------

HRESULT MPEG1Source::DispatchOperation(SourceOp *pOp)
{
    EnterCriticalSection(&m_critSec);

    HRESULT hr = S_OK;

    if (m_state == STATE_SHUTDOWN)
    {
        LeaveCriticalSection(&m_critSec);

        return S_OK; // Already shut down, ignore the request.
    }

    switch (pOp->Op())
    {

    // IMFMediaSource methods:

    case SourceOp::OP_START:
        hr = DoStart((StartOp*)pOp);
        break;

    case SourceOp::OP_STOP:
        hr = DoStop(pOp);
        break;

    case SourceOp::OP_PAUSE:
        hr = DoPause(pOp);
        break;

    // Operations requested by the streams:

    case SourceOp::OP_REQUEST_DATA:
        hr = OnStreamRequestSample(pOp);
        break;

    case SourceOp::OP_END_OF_STREAM:
        hr = OnEndOfStream(pOp);
        break;

    default:
        hr = E_UNEXPECTED;
    }

    if (FAILED(hr))
    {
        StreamingError(hr);
    }

    LeaveCriticalSection(&m_critSec);
    return hr;
}
```



Pour récapituler :

1.  Le pipeline appelle une méthode asynchrone, telle que [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).
2.  La méthode asynchrone appelle `OpQueue::QueueOperation` , en passant un pointeur vers un `SourceOp` objet.
3.  La `QueueOperation` méthode place l’opération sur la file d’attente *m \_ OpQueue* et appelle `OpQueue::ProcessQueue` .
4.  La `ProcessQueue` méthode appelle [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem). À partir de ce stade, tout se produit sur un thread de file d’attente de travail Media Foundation. La méthode asynchrone retourne à l’appelant.
5.  Le thread de file d’attente de travail appelle la `OpQueue::ProcessQueueAsync` méthode.
6.  La `ProcessQueueAsync` méthode appelle `MPEG1Source:ValidateOperation` pour valider l’opération.
7.  La `ProcessQueueAsync` méthode appelle `MPEG1Source::DispatchOperation` pour traiter l’opération.

Cette conception présente plusieurs avantages :

-   Les méthodes étant asynchrones, elles ne bloquent pas le thread de l’application appelante.
-   Les opérations sont distribuées sur un thread de file d’attente de travail Media Foundation, qui est partagé entre les composants de pipeline. Par conséquent, la source du média ne crée pas son propre thread, ce qui réduit le nombre total de threads créés.
-   La source du média n’est pas bloquée en attendant la fin des opérations. Cela réduit le risque qu’une source de média provoque accidentellement un blocage et contribue à réduire le basculement de contexte.
-   La source du média peut utiliser des e/s asynchrones pour lire le fichier source (en appelant [**IMFByteStream :: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread)). La source du média n’a pas besoin d’être bloquée en attendant la fin de la routine d’e/s.

Si vous suivez le modèle présenté dans l’exemple du kit de développement logiciel (SDK), vous pouvez vous concentrer sur les détails spécifiques de la source du média.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sources multimédias](media-sources.md)
</dt> <dt>

[Écriture d’une source de média personnalisée](writing-a-custom-media-source.md)
</dt> </dl>

 

 



