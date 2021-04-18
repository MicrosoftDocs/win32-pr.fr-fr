---
description: Déverrouillage du kit de développement logiciel (SDK) Windows Media format
ms.assetid: 7ede8bda-3b26-452d-8ce9-cd2410ffd9f4
title: Déverrouillage du kit de développement logiciel (SDK) Windows Media format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9807794dc7e42c563f2f7d45dcb0b1b684aad1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106527043"
---
# <a name="unlocking-the-windows-media-format-sdk"></a>Déverrouillage du kit de développement logiciel (SDK) Windows Media format

Pour accéder à la version 7 ou 7,1 du kit de développement logiciel (SDK) Windows Media format, une application doit fournir un certificat logiciel, également appelé clé, au moment de l’exécution. Cette clé est contenue dans une bibliothèque statique appelée wmstub. lib, à laquelle l’application établit une liaison au moment de la génération. Une clé individualisée est uniquement nécessaire pour créer ou lire des fichiers protégés par DRM. Les fichiers non DRM peuvent être créés à l’aide de la bibliothèque statique fournie avec le kit de développement logiciel (SDK) Windows Media format. Pour plus d’informations sur l’obtention de la clé DRM, consultez le kit de développement logiciel (SDK) de format Windows Media. Une application DirectShow fournit son certificat à l’enregistreur ASF WM lorsqu’il est ajouté au graphique de filtre. L’application doit s’inscrire en tant que fournisseur de clés à l’aide des interfaces COM **IServiceProvider** et **IObjectWithSite** . À l’aide de cette technique, l’application implémente une classe de fournisseur de clé dérivée de **IServiceProvider**. Cette classe implémente les trois méthodes COM standard (**AddRef**, **QueryInterface** et **Release**), ainsi qu’une autre méthode, **QueryService**, qui est appelée par le gestionnaire de graphique de filtre. **QueryService** appelle la méthode du kit de développement logiciel (SDK) Windows Media format [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) et retourne au gestionnaire du graphique de filtres un pointeur vers le certificat qui a été créé. Si le certificat est valide, le gestionnaire de graphes de filtre permet au processus de création de graphique de continuer.

> [!Note]  
> Pour générer une application, incluez Wmsdkidl. h pour le prototype de [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85))et liez-la à la bibliothèque Wmstub. lib.

 

L’exemple de code suivant illustre les étapes de base de ce processus :


```C++
// Declare and implement a key provider class derived from IServiceProvider.

class CKeyProvider : public IServiceProvider {
public:
    // IUnknown interface
    STDMETHODIMP QueryInterface(REFIID riid, void ** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    CKeyProvider();

    // IServiceProvider
    STDMETHODIMP QueryService(REFIID siid, REFIID riid, void **ppv);
    
private:
    ULONG m_cRef;
};

CKeyProvider::CKeyProvider() : m_cRef(0)
{
}

// IUnknown methods
ULONG CKeyProvider::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

ULONG CKeyProvider::Release()
{
    ASSERT(m_cRef > 0);

    ULONG lCount = InterlockedDecrement(&m_cRef);
    if (m_cRef == 0) 
    {
        delete this;
        return (ULONG)0;
    }
    return (ULONG)lCount;
}

// We only support IUnknown and IServiceProvider.
HRESULT CKeyProvider::QueryInterface(REFIID riid, void ** ppv)
{
    if (!ppv) return E_POINTER;

    if (riid == IID_IUnknown) 
    {
        *ppv = (void *) static_cast<IUnknown *>(this);
        AddRef();
        return S_OK;
    }
    if (riid == IID_IServiceProvider) 
    {
        *ppv = (void *) static_cast<IServiceProvider *>(this);
        AddRef();
        return S_OK;
    }

    return E_NOINTERFACE;
}

STDMETHODIMP CKeyProvider::QueryService(REFIID siid, REFIID riid, void **ppv)
{
    if (!ppv) return E_POINTER;

    if (siid == __uuidof(IWMReader) && riid == IID_IUnknown) 
    {
        IUnknown *punkCert;
        HRESULT hr = WMCreateCertificate(&punkCert);
        if (SUCCEEDED(hr)) 
        {
            *ppv = (void *) punkCert;
        }
        return hr;
    }
    return E_NOINTERFACE;
}

////////////////////////////////////////////////////////////////////
//
// These examples illustrate the sequence of method calls
// in your application. Error checking is omitted for brevity.
//
///////////////////////////////////////////////////////////////////

// Create the filter graph manager, but don't add any filters.
IGraphBuilder *pGraph;
hr = CreateFilterGraph(&pGraph);

...

// Instantiate the key provider class, and AddRef it
// so that COM doesn't try to free our static object.

CKeyProvider prov;
prov.AddRef();  // Don't let COM try to free our static object.

// Give the graph an IObjectWithSite pointer for callbacks and QueryService.
IObjectWithSite* pObjectWithSite = NULL;

hr = pGraph->QueryInterface(IID_IObjectWithSite, (void**)&pObjectWithSite);
if (SUCCEEDED(hr))
{
    // Use the IObjectWithSite pointer to specify our key provider object.
    // The filter graph manager will use this pointer to call
    // QueryService to do the unlocking.
    // If the unlocking succeeds, then we can build our graph.

    pObjectWithSite->SetSite((IUnknown *) (IServiceProvider *) &prov);
    pObjectWithSite->Release();
}

// Now build the graph.
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de fichiers ASF dans DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
