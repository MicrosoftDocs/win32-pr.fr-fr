---
description: Cette rubrique explique comment utiliser le lecteur source en mode asynchrone.
ms.assetid: 9D3C2780-D7DB-4151-8474-9A19EC94F6BE
title: Utilisation du lecteur source en mode asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357d0405cb3e594d059b7c93e793250e0be88562
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313674"
---
# <a name="using-the-source-reader-in-asynchronous-mode"></a>Utilisation du lecteur source en mode asynchrone

Cette rubrique explique comment utiliser le [lecteur source](source-reader.md) en mode asynchrone. En mode asynchrone, l’application fournit une interface de rappel, qui est utilisée pour informer l’application que les données sont disponibles.

Cette rubrique part du principe que vous avez déjà lu la rubrique [à l’aide du lecteur source pour traiter les données multimédias](processing-media-data-with-the-source-reader.md).

## <a name="using-asynchronous-mode"></a>Utilisation du mode asynchrone

Le lecteur source fonctionne soit en mode synchrone, soit en mode asynchrone. L’exemple de code présenté dans la section précédente suppose que le lecteur source utilise le mode synchrone, qui est la valeur par défaut. En mode synchrone, la méthode [**IMFSourceReader :: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) est bloquée pendant que la source du média produit l’exemple suivant. Une source de média acquiert généralement des données à partir d’une source externe (par exemple, un fichier local ou une connexion réseau), de sorte que la méthode peut bloquer le thread appelant pour une durée perceptible.

En mode asynchrone, le [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) retourne immédiatement et le travail est effectué sur un autre thread. Une fois l’opération terminée, le lecteur source appelle l’application par le biais de l’interface de rappel [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) . Pour utiliser le mode asynchrone, vous devez fournir un pointeur de rappel lorsque vous créez le lecteur source pour la première fois, comme suit :

1.  Créez un magasin d’attributs en appelant la fonction [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) .
2.  Définissez l’attribut de [ \_ \_ \_ \_ rappel asynchrone du lecteur source MF](mf-source-reader-async-callback.md) sur le magasin d’attributs. La valeur de l’attribut est un pointeur vers votre objet de rappel.
3.  Lorsque vous créez le lecteur source, transmettez le magasin d’attributs à la fonction de création dans le paramètre *pAttributes* . Toutes les fonctions permettant de créer le lecteur source ont ce paramètre.

L'exemple suivant affiche ces étapes.


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



Après avoir créé le lecteur source, vous ne pouvez pas basculer entre les modes synchrone et asynchrone.

Pour récupérer des données en mode asynchrone, appelez la méthode [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) , mais affectez aux quatre derniers paramètres la **valeur null**, comme illustré dans l’exemple suivant.


```C++
    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
```



Lorsque la méthode [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) se termine de façon asynchrone, le lecteur source appelle votre méthode [**IMFSourceReaderCallback :: OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) . Cette méthode a cinq paramètres :

-   *hrStatus*: contient une valeur **HRESULT** . Il s’agit de la même valeur que [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) retournerait en mode synchrone. Si *hrStatus* contient un code d’erreur, vous pouvez ignorer les paramètres restants.
-   *dwStreamIndex*, *dwStreamFlags*, llTimestamp et *pSample*: ces trois paramètres sont équivalents aux trois derniers paramètres dans [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample). Ils contiennent respectivement le numéro de flux, les indicateurs d’État et le pointeur [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .


```C++
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);
```



En outre, l’interface de rappel définit deux autres méthodes :

-   [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent). Avertit l’application lorsque certains événements se produisent dans la source du média, tels que les événements de mise en mémoire tampon ou de connexion réseau.
-   [**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush). Appelé lorsque la méthode [**flush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush) est terminée.

## <a name="implementing-the-callback-interface"></a>Implémentation de l’interface de rappel

L’interface de rappel doit être thread-safe, car [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) et les autres méthodes de rappel sont appelées à partir de threads de travail.

Lorsque vous implémentez le rappel, vous pouvez adopter plusieurs approches différentes. Par exemple, vous pouvez effectuer tout le travail à l’intérieur du rappel, ou vous pouvez utiliser le rappel pour notifier l’application (par exemple, en signalant un handle d’événement), puis effectuer le travail à partir du thread d’application.

La méthode [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) sera appelée une fois pour chaque appel que vous apportez à la méthode [**IMFSourceReader :: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) . Pour accéder à l’exemple suivant, appelez à nouveau **ReadSample** . Si une erreur se produit, **OnReadSample** est appelé avec un code d’erreur pour le paramètre *hrStatus* .

L’exemple suivant montre une implémentation minimale de l’interface de rappel. Tout d’abord, voici la déclaration d’une classe qui implémente l’interface.


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



Dans cet exemple, nous ne sommes pas intéressés par les méthodes [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent) et [**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) . ils renvoient simplement **S \_ OK**. La classe utilise un handle d’événement pour signaler l’application ; ce handle est fourni par le biais du constructeur.

Dans cet exemple minimal, la méthode [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) imprime simplement l’horodatage dans la fenêtre de console. Elle stocke ensuite le code d’État et l’indicateur de fin de flux, et signale le descripteur d’événement :


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



Le code suivant montre que l’application utilise cette classe de rappel pour lire toutes les images vidéo d’un fichier multimédia :


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecteur source](source-reader.md)
</dt> </dl>

 

 



