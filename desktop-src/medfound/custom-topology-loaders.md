---
description: Chargeurs de topologie personnalisés
ms.assetid: 3982b07e-3179-45c1-9f17-f2114363f53d
title: Chargeurs de topologie personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a8f9e24b207d43620e7b2d09080d244b0a9e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513959"
---
# <a name="custom-topology-loaders"></a>Chargeurs de topologie personnalisés

Lorsqu’une application met en file d’attente une topologie partielle sur la session multimédia, la session multimédia utilise un chargeur de topologie pour résoudre la topologie. Par défaut, la session multimédia utilise l’implémentation standard Media Foundation du chargeur de topologie, mais vous pouvez également fournir une implémentation personnalisée. Cela vous donne davantage de contrôle sur la topologie finale. Un chargeur de topologie personnalisé doit implémenter l’interface [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) .

Pour définir un chargeur de topologie personnalisé sur la session multimédia, procédez comme suit :

1.  Créez un magasin d’attributs vide en appelant [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).
2.  Définissez l' [**attribut \_ \_ TOPOLOADER de session MF**](mf-session-topoloader-attribute.md) sur le magasin d’attributs. La valeur de l’attribut est le CLSID de votre chargeur personnalisé.
3.  Appelez [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) pour créer la session multimédia pour du contenu non protégé ou [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) pour créer la session multimédia à l’intérieur du chemin d’accès de média protégé (PMP).

> [!Note]  
> Pour utiliser un chargeur de topologie personnalisé à l’intérieur du PMP, le chargeur de topologie doit être un composant approuvé. Pour plus d’informations, consultez [chemin d’accès au média protégé](protected-media-path.md).

 

Le code suivant montre comment définir un chargeur de topologie personnalisé sur la session multimédia.


```C++
HRESULT CreateSession_CustomTopoLoader(REFCLSID clsid, IMFMediaSession **ppSession)
{
    *ppSession = NULL;

    IMFMediaSession *pSession = NULL;
    IMFAttributes *pConfig = NULL;

    // Create an attribute store to configure the media session.
    HRESULT hr = MFCreateAttributes(&pConfig, 1);

    // Set the CLSID of the custom topology loader.
    if (SUCCEEDED(hr))
    {
        hr = pConfig->SetGUID(MF_SESSION_TOPOLOADER, clsid);
    }

    // Create the media session.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaSession(pConfig, &pSession);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppSession = pSession;
        (*ppSession)->AddRef();
    }

    SafeRelease(&pSession);
    SafeRelease(&pConfig);

    return hr;
}
```



Il n’est pas nécessaire d’implémenter l’intégralité de l’algorithme de chargement de topologie dans le chargeur de topologie. Vous pouvez également encapsuler le chargeur de topologie Media Foundation standard. Dans votre implémentation de la méthode [**IMFTopoLoader :: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) , modifiez la topologie en fonction des besoins et transmettez la topologie modifiée au chargeur de topologie standard. Le chargeur de topologie standard termine la topologie. Vous pouvez également modifier la topologie terminée avant de la retransmettre à la session multimédia.

Le code suivant illustre la structure générale de cette approche. Il n’affiche aucun détail de la méthode [**Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) , car ceux-ci dépendent des besoins particuliers de votre application.


```C++
class CTopoLoader : public IMFTopoLoader
{
public:

    static HRESULT CreateInstance(REFIID iid, void **ppv)
    {
        HRESULT hr = S_OK;

        CTopoLoader *pTopoLoader = new (std::nothrow) CTopoLoader(&hr);
        
        if (pTopoLoader == NULL)
        {
            return E_OUTOFMEMORY;
        }

        if (SUCCEEDED(hr))
        {
            hr = pTopoLoader->QueryInterface(iid, ppv);
        }

        SafeRelease(&pTopoLoader);
        return hr;
    }

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CTopoLoader, IMFTopoLoader),
            { 0 },
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        long cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    // IMTopoLoader methods.
    STDMETHODIMP Load(
        IMFTopology *pInput, 
        IMFTopology **ppOutput, 
        IMFTopology *pCurrent
        )
    {
        HRESULT hr = S_OK;

        // TODO: Add custom topology-building code here.
        //       Modify pInput as needed.

        if (SUCCEEDED(hr))
        {
            hr = m_pTopoLoader->Load(pInput, ppOutput, pCurrent);
        }

        // TODO: Add custom topology-building code here.
        //       Modify ppOutput as needed.

        return hr;
    }

private:
    CTopoLoader(HRESULT *phr) : m_cRef(1), m_pTopoLoader(NULL)
    {
        *phr = MFCreateTopoLoader(&m_pTopoLoader);
    }

    virtual ~CTopoLoader()
    {
        SafeRelease(&m_pTopoLoader);
    }

private:
    long            m_cRef;          // Reference count.
    IMFTopoLoader   *m_pTopoLoader;  // Standard topoloader.
};
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**MFCreateTopoLoader**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader)
</dt> <dt>

[Génération de topologie avancée](advanced-topology-building.md)
</dt> </dl>

 

 



