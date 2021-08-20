---
description: Implémentation de IMediaBuffer
ms.assetid: bde7cef8-f43e-4a11-8b77-fed5585d390a
title: Implémentation de IMediaBuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5033fcf18812f2a31e175c05b0d4d8eeee18484d0cc20e640ae30f9390a68f76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154117"
---
# <a name="implementing-imediabuffer"></a>Implémentation de IMediaBuffer

dans le modèle de diffusion en continu DMO par défaut, les mémoires tampons sont gérées via l’interface [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) . le client du DMO est chargé d’implémenter un objet qui expose cette interface. L’interface **IMediaBuffer** a trois méthodes :

-   **GetBufferAndLength** retourne l’adresse de la mémoire tampon (autrement dit, le bloc réel de mémoire qui contient les données) et la taille des données valides dans la mémoire tampon.
-   **GetMaxLength** retourne la taille de la mémoire tampon.
-   **SetLength** spécifie la longueur des données valides dans la mémoire tampon.

Le traitement sur place ne requiert pas l’interface **IMediaBuffer** . Le code suivant illustre une implémentation minimale de **IMediaBuffer**:


```C++
//  CMediaBuffer class.
#include <dmo.h>
class CMediaBuffer : public IMediaBuffer
{
private:
    DWORD        m_cbLength;
    const DWORD  m_cbMaxLength;
    LONG         m_nRefCount;  // Reference count
    BYTE         *m_pbData;


    CMediaBuffer(DWORD cbMaxLength, HRESULT& hr) :
        m_nRefCount(1),
        m_cbMaxLength(cbMaxLength),
        m_cbLength(0),
        m_pbData(NULL)
    {
        m_pbData = new BYTE[cbMaxLength];
        if (!m_pbData) 
        {
            hr = E_OUTOFMEMORY;
        }
    }

    ~CMediaBuffer()
    {
        if (m_pbData) 
        {
            delete [] m_pbData;
        }
    }

public:

    // Function to create a new IMediaBuffer object and return 
    // an AddRef'd interface pointer.
    static HRESULT Create(long cbMaxLen, IMediaBuffer **ppBuffer)
    {
        HRESULT hr = S_OK;
        CMediaBuffer *pBuffer = NULL;

        if (ppBuffer == NULL)
        {
            return E_POINTER;
        }

        pBuffer = new CMediaBuffer(cbMaxLen, hr);

        if (pBuffer == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        if (SUCCEEDED(hr))
        {
           *ppBuffer = pBuffer;
           (*ppBuffer)->AddRef();
        }

        if (pBuffer)
        {
            pBuffer->Release();
        }
        return hr;
    }

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        if (ppv == NULL) 
        {
            return E_POINTER;
        }
        else if (riid == IID_IMediaBuffer || riid == IID_IUnknown) 
        {
            *ppv = static_cast<IMediaBuffer *>(this);
            AddRef();
            return S_OK;
        }
        else
        {
            *ppv = NULL;
            return E_NOINTERFACE;
        }
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_nRefCount);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG lRef = InterlockedDecrement(&m_nRefCount);
        if (lRef == 0) 
        {
            delete this;
            // m_cRef is no longer valid! Return lRef.
        }
        return lRef;  
    }

    // IMediaBuffer methods.
    STDMETHODIMP SetLength(DWORD cbLength)
    {
        if (cbLength > m_cbMaxLength) 
        {
            return E_INVALIDARG;
        }
        m_cbLength = cbLength;
        return S_OK;
    }

    STDMETHODIMP GetMaxLength(DWORD *pcbMaxLength)
    {
        if (pcbMaxLength == NULL) 
        {
            return E_POINTER;
        }
        *pcbMaxLength = m_cbMaxLength;
        return S_OK;
    }

    STDMETHODIMP GetBufferAndLength(BYTE **ppbBuffer, DWORD *pcbLength)
    {
        // Either parameter can be NULL, but not both.
        if (ppbBuffer == NULL && pcbLength == NULL) 
        {
            return E_POINTER;
        }
        if (ppbBuffer) 
        {
            *ppbBuffer = m_pbData;
        }
        if (pcbLength) 
        {
            *pcbLength = m_cbLength;
        }
        return S_OK;
    }
};

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Hébergement direct d’un DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



