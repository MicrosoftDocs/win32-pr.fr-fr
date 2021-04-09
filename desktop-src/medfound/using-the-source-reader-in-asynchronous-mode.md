---
description: Cette rubrique explique comment utiliser le lecteur source en mode asynchrone.
ms.assetid: 9D3C2780-D7DB-4151-8474-9A19EC94F6BE
title: Utilisation du lecteur source en mode asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357d0405cb3e594d059b7c93e793250e0be88562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034151"
---
# <a name="using-the-source-reader-in-asynchronous-mode"></a><span data-ttu-id="273dd-103">Utilisation du lecteur source en mode asynchrone</span><span class="sxs-lookup"><span data-stu-id="273dd-103">Using the Source Reader in Asynchronous Mode</span></span>

<span data-ttu-id="273dd-104">Cette rubrique explique comment utiliser le [lecteur source](source-reader.md) en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="273dd-104">This topic describes how to use the [Source Reader](source-reader.md) in asynchronous mode.</span></span> <span data-ttu-id="273dd-105">En mode asynchrone, l’application fournit une interface de rappel, qui est utilisée pour informer l’application que les données sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="273dd-105">In asynchronous mode, the application provides a callback interface, which is used to notify the application that data is available.</span></span>

<span data-ttu-id="273dd-106">Cette rubrique part du principe que vous avez déjà lu la rubrique [à l’aide du lecteur source pour traiter les données multimédias](processing-media-data-with-the-source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="273dd-106">This topic assumes that you have already read the topic [Using the Source Reader to Process Media Data](processing-media-data-with-the-source-reader.md).</span></span>

## <a name="using-asynchronous-mode"></a><span data-ttu-id="273dd-107">Utilisation du mode asynchrone</span><span class="sxs-lookup"><span data-stu-id="273dd-107">Using Asynchronous Mode</span></span>

<span data-ttu-id="273dd-108">Le lecteur source fonctionne soit en mode synchrone, soit en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="273dd-108">The Source Reader operates either in synchronous mode or asynchronous mode.</span></span> <span data-ttu-id="273dd-109">L’exemple de code présenté dans la section précédente suppose que le lecteur source utilise le mode synchrone, qui est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="273dd-109">The code example shown in the previous section assumes that the Source Reader is using synchronous mode, which is the default.</span></span> <span data-ttu-id="273dd-110">En mode synchrone, la méthode [**IMFSourceReader :: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) est bloquée pendant que la source du média produit l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="273dd-110">In synchronous mode, the [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method blocks while the media source produces the next sample.</span></span> <span data-ttu-id="273dd-111">Une source de média acquiert généralement des données à partir d’une source externe (par exemple, un fichier local ou une connexion réseau), de sorte que la méthode peut bloquer le thread appelant pour une durée perceptible.</span><span class="sxs-lookup"><span data-stu-id="273dd-111">A media source typically acquires data from some external source (such as a local file or a network connection), so the method can block the calling thread for a noticeable amount of time.</span></span>

<span data-ttu-id="273dd-112">En mode asynchrone, le [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) retourne immédiatement et le travail est effectué sur un autre thread.</span><span class="sxs-lookup"><span data-stu-id="273dd-112">In asynchronous mode, the [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) returns immediately and the work is performed on another thread.</span></span> <span data-ttu-id="273dd-113">Une fois l’opération terminée, le lecteur source appelle l’application par le biais de l’interface de rappel [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) .</span><span class="sxs-lookup"><span data-stu-id="273dd-113">After the operation is complete, the Source Reader calls the application through the [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) callback interface.</span></span> <span data-ttu-id="273dd-114">Pour utiliser le mode asynchrone, vous devez fournir un pointeur de rappel lorsque vous créez le lecteur source pour la première fois, comme suit :</span><span class="sxs-lookup"><span data-stu-id="273dd-114">To use asynchronous mode, you must provide a callback pointer when you first create the Source Reader, as follows:</span></span>

1.  <span data-ttu-id="273dd-115">Créez un magasin d’attributs en appelant la fonction [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) .</span><span class="sxs-lookup"><span data-stu-id="273dd-115">Create an attribute store by calling the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function.</span></span>
2.  <span data-ttu-id="273dd-116">Définissez l’attribut de [ \_ \_ \_ \_ rappel asynchrone du lecteur source MF](mf-source-reader-async-callback.md) sur le magasin d’attributs.</span><span class="sxs-lookup"><span data-stu-id="273dd-116">Set the [MF\_SOURCE\_READER\_ASYNC\_CALLBACK](mf-source-reader-async-callback.md) attribute on the attribute store.</span></span> <span data-ttu-id="273dd-117">La valeur de l’attribut est un pointeur vers votre objet de rappel.</span><span class="sxs-lookup"><span data-stu-id="273dd-117">The attribute value is a pointer to your callback object.</span></span>
3.  <span data-ttu-id="273dd-118">Lorsque vous créez le lecteur source, transmettez le magasin d’attributs à la fonction de création dans le paramètre *pAttributes* .</span><span class="sxs-lookup"><span data-stu-id="273dd-118">When you create the Source Reader, pass the attribute store to the creation function in the *pAttributes* parameter.</span></span> <span data-ttu-id="273dd-119">Toutes les fonctions permettant de créer le lecteur source ont ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="273dd-119">All of the functions to create the Source Reader have this parameter.</span></span>

<span data-ttu-id="273dd-120">L'exemple suivant affiche ces étapes.</span><span class="sxs-lookup"><span data-stu-id="273dd-120">The following example shows these steps.</span></span>


```C++
HRESULT CreateSourceReaderAsync(
    PCWSTR pszURL, 
    IMFSourceReaderCallback *pCallback, 
    IMFSourceReader **ppReader)
{
    HRESULT hr = S_OK;
    IMFAttributes *pAttributes = NULL;

    hr = MFCreateAttributes(&pAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAttributes->SetUnknown(MF_SOURCE_READER_ASYNC_CALLBACK, pCallback);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateSourceReaderFromURL(pszURL, pAttributes, ppReader);

done:
    SafeRelease(&pAttributes);
    return hr;
}
```



<span data-ttu-id="273dd-121">Après avoir créé le lecteur source, vous ne pouvez pas basculer entre les modes synchrone et asynchrone.</span><span class="sxs-lookup"><span data-stu-id="273dd-121">After you create the Source Reader, you cannot switch modes between synchronous and asynchronous.</span></span>

<span data-ttu-id="273dd-122">Pour récupérer des données en mode asynchrone, appelez la méthode [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) , mais affectez aux quatre derniers paramètres la **valeur null**, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="273dd-122">To get data in asynchronous mode, call the [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method but set the last four parameters to **NULL**, as shown in the following example.</span></span>


```C++
    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
```



<span data-ttu-id="273dd-123">Lorsque la méthode [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) se termine de façon asynchrone, le lecteur source appelle votre méthode [**IMFSourceReaderCallback :: OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) .</span><span class="sxs-lookup"><span data-stu-id="273dd-123">When the [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method completes asynchronously, the Source Reader calls your [**IMFSourceReaderCallback::OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) method.</span></span> <span data-ttu-id="273dd-124">Cette méthode a cinq paramètres :</span><span class="sxs-lookup"><span data-stu-id="273dd-124">This method has five parameters:</span></span>

-   <span data-ttu-id="273dd-125">*hrStatus*: contient une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="273dd-125">*hrStatus*: Contains an **HRESULT** value.</span></span> <span data-ttu-id="273dd-126">Il s’agit de la même valeur que [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) retournerait en mode synchrone.</span><span class="sxs-lookup"><span data-stu-id="273dd-126">This is the same value that [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) would return in synchronous mode.</span></span> <span data-ttu-id="273dd-127">Si *hrStatus* contient un code d’erreur, vous pouvez ignorer les paramètres restants.</span><span class="sxs-lookup"><span data-stu-id="273dd-127">If *hrStatus* contains an error code, you can ignore the remaining parameters.</span></span>
-   <span data-ttu-id="273dd-128">*dwStreamIndex*, *dwStreamFlags*, llTimestamp et *pSample*: ces trois paramètres sont équivalents aux trois derniers paramètres dans [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span><span class="sxs-lookup"><span data-stu-id="273dd-128">*dwStreamIndex*, *dwStreamFlags*, llTimestamp, and *pSample*: These three parameters are equivalent to the last three parameters in [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span></span> <span data-ttu-id="273dd-129">Ils contiennent respectivement le numéro de flux, les indicateurs d’État et le pointeur [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .</span><span class="sxs-lookup"><span data-stu-id="273dd-129">They contain the stream number, status flags, and [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer, respectively.</span></span>


```C++
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);
```



<span data-ttu-id="273dd-130">En outre, l’interface de rappel définit deux autres méthodes :</span><span class="sxs-lookup"><span data-stu-id="273dd-130">In addition, the callback interface defines two other methods:</span></span>

-   <span data-ttu-id="273dd-131">[**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent).</span><span class="sxs-lookup"><span data-stu-id="273dd-131">[**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent).</span></span> <span data-ttu-id="273dd-132">Avertit l’application lorsque certains événements se produisent dans la source du média, tels que les événements de mise en mémoire tampon ou de connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="273dd-132">Notifies the application when certain events occur in media source, such as buffering or network connection events.</span></span>
-   <span data-ttu-id="273dd-133">[**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush).</span><span class="sxs-lookup"><span data-stu-id="273dd-133">[**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush).</span></span> <span data-ttu-id="273dd-134">Appelé lorsque la méthode [**flush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush) est terminée.</span><span class="sxs-lookup"><span data-stu-id="273dd-134">Called when the [**Flush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush) method completes.</span></span>

## <a name="implementing-the-callback-interface"></a><span data-ttu-id="273dd-135">Implémentation de l’interface de rappel</span><span class="sxs-lookup"><span data-stu-id="273dd-135">Implementing the Callback Interface</span></span>

<span data-ttu-id="273dd-136">L’interface de rappel doit être thread-safe, car [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) et les autres méthodes de rappel sont appelées à partir de threads de travail.</span><span class="sxs-lookup"><span data-stu-id="273dd-136">The callback interface must be thread-safe, because [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) and the other callback methods are called from worker threads.</span></span>

<span data-ttu-id="273dd-137">Lorsque vous implémentez le rappel, vous pouvez adopter plusieurs approches différentes.</span><span class="sxs-lookup"><span data-stu-id="273dd-137">There are several different approaches you can take when you implement the callback.</span></span> <span data-ttu-id="273dd-138">Par exemple, vous pouvez effectuer tout le travail à l’intérieur du rappel, ou vous pouvez utiliser le rappel pour notifier l’application (par exemple, en signalant un handle d’événement), puis effectuer le travail à partir du thread d’application.</span><span class="sxs-lookup"><span data-stu-id="273dd-138">For example, you can do all of the work inside the callback, or you can use the callback to notify the application (for example, by signaling an event handle) and then do work from the application thread.</span></span>

<span data-ttu-id="273dd-139">La méthode [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) sera appelée une fois pour chaque appel que vous apportez à la méthode [**IMFSourceReader :: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) .</span><span class="sxs-lookup"><span data-stu-id="273dd-139">The [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) method will be called once for every call that you make to the [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method.</span></span> <span data-ttu-id="273dd-140">Pour accéder à l’exemple suivant, appelez à nouveau **ReadSample** .</span><span class="sxs-lookup"><span data-stu-id="273dd-140">To get the next sample, call **ReadSample** again.</span></span> <span data-ttu-id="273dd-141">Si une erreur se produit, **OnReadSample** est appelé avec un code d’erreur pour le paramètre *hrStatus* .</span><span class="sxs-lookup"><span data-stu-id="273dd-141">If an error occurs, **OnReadSample** is called with an error code for the *hrStatus* parameter.</span></span>

<span data-ttu-id="273dd-142">L’exemple suivant montre une implémentation minimale de l’interface de rappel.</span><span class="sxs-lookup"><span data-stu-id="273dd-142">The following example shows a minimal implementation of the callback interface.</span></span> <span data-ttu-id="273dd-143">Tout d’abord, voici la déclaration d’une classe qui implémente l’interface.</span><span class="sxs-lookup"><span data-stu-id="273dd-143">First, here is the declaration of a class that implements the interface.</span></span>


```C++
#include <shlwapi.h>

class SourceReaderCB : public IMFSourceReaderCallback
{
public:
    SourceReaderCB(HANDLE hEvent) : 
      m_nRefCount(1), m_hEvent(hEvent), m_bEOS(FALSE), m_hrStatus(S_OK)
    {
        InitializeCriticalSection(&m_critsec);
    }

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(SourceReaderCB, IMFSourceReaderCallback),
            { 0 },
        };
        return QISearch(this, qit, iid, ppv);
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_nRefCount);
    }
    STDMETHODIMP_(ULONG) Release()
    {
        ULONG uCount = InterlockedDecrement(&m_nRefCount);
        if (uCount == 0)
        {
            delete this;
        }
        return uCount;
    }

    // IMFSourceReaderCallback methods
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);

    STDMETHODIMP OnEvent(DWORD, IMFMediaEvent *)
    {
        return S_OK;
    }

    STDMETHODIMP OnFlush(DWORD)
    {
        return S_OK;
    }

public:
    HRESULT Wait(DWORD dwMilliseconds, BOOL *pbEOS)
    {
        *pbEOS = FALSE;

        DWORD dwResult = WaitForSingleObject(m_hEvent, dwMilliseconds);
        if (dwResult == WAIT_TIMEOUT)
        {
            return E_PENDING;
        }
        else if (dwResult != WAIT_OBJECT_0)
        {
            return HRESULT_FROM_WIN32(GetLastError());
        }

        *pbEOS = m_bEOS;
        return m_hrStatus;
    }
    
private:
    
    // Destructor is private. Caller should call Release.
    virtual ~SourceReaderCB() 
    {
    }

    void NotifyError(HRESULT hr)
    {
        wprintf(L"Source Reader error: 0x%X\n", hr);
    }

private:
    long                m_nRefCount;        // Reference count.
    CRITICAL_SECTION    m_critsec;
    HANDLE              m_hEvent;
    BOOL                m_bEOS;
    HRESULT             m_hrStatus;

};
```



<span data-ttu-id="273dd-144">Dans cet exemple, nous ne sommes pas intéressés par les méthodes [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent) et [**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) . ils renvoient simplement **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="273dd-144">In this example, we are not interested in the [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent) and [**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) methods, so they simply return **S\_OK**.</span></span> <span data-ttu-id="273dd-145">La classe utilise un handle d’événement pour signaler l’application ; ce handle est fourni par le biais du constructeur.</span><span class="sxs-lookup"><span data-stu-id="273dd-145">The class uses an event handle to signal the application; this handle is provided through the constructor.</span></span>

<span data-ttu-id="273dd-146">Dans cet exemple minimal, la méthode [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) imprime simplement l’horodatage dans la fenêtre de console.</span><span class="sxs-lookup"><span data-stu-id="273dd-146">In this minimal example, the [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) method just prints the time stamp to the console window.</span></span> <span data-ttu-id="273dd-147">Elle stocke ensuite le code d’État et l’indicateur de fin de flux, et signale le descripteur d’événement :</span><span class="sxs-lookup"><span data-stu-id="273dd-147">Then it stores the status code and the end-of-stream flag, and signals the event handle:</span></span>


```C++
HRESULT SourceReaderCB::OnReadSample(
    HRESULT hrStatus,
    DWORD /* dwStreamIndex */,
    DWORD dwStreamFlags,
    LONGLONG llTimestamp,
    IMFSample *pSample      // Can be NULL
    )
{
    EnterCriticalSection(&m_critsec);

    if (SUCCEEDED(hrStatus))
    {
        if (pSample)
        {
            // Do something with the sample.
            wprintf(L"Frame @ %I64d\n", llTimestamp);
        }
    }
    else
    {
        // Streaming error.
        NotifyError(hrStatus);
    }

    if (MF_SOURCE_READERF_ENDOFSTREAM & dwStreamFlags)
    {
        // Reached the end of the stream.
        m_bEOS = TRUE;
    }
    m_hrStatus = hrStatus;

    LeaveCriticalSection(&m_critsec);
    SetEvent(m_hEvent);
    return S_OK;
}
```



<span data-ttu-id="273dd-148">Le code suivant montre que l’application utilise cette classe de rappel pour lire toutes les images vidéo d’un fichier multimédia :</span><span class="sxs-lookup"><span data-stu-id="273dd-148">The following code shows the application would use this callback class to read all of the video frames from a media file:</span></span>


```C++
HRESULT ReadMediaFile(PCWSTR pszURL)
{
    HRESULT hr = S_OK;

    IMFSourceReader *pReader = NULL;
    SourceReaderCB *pCallback = NULL;

    HANDLE hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (hEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        goto done;
    }

    // Create an instance of the callback object.
    pCallback = new (std::nothrow) SourceReaderCB(hEvent);
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    // Create the Source Reader.
    hr = CreateSourceReaderAsync(pszURL, pCallback, &pReader);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConfigureDecoder(pReader, MF_SOURCE_READER_FIRST_VIDEO_STREAM);
    if (FAILED(hr))
    {
        goto done;
    }

    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    while (SUCCEEDED(hr))
    {
        BOOL bEOS;
        hr = pCallback->Wait(INFINITE, &bEOS);
        if (FAILED(hr) || bEOS)
        {
            break;
        }
        hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM,
            0, NULL, NULL, NULL, NULL);
    }

done:
    SafeRelease(&pReader);
    SafeRelease(&pCallback);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="273dd-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="273dd-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="273dd-150">Lecteur source</span><span class="sxs-lookup"><span data-stu-id="273dd-150">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 



