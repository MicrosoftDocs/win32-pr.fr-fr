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
# <a name="unlocking-the-windows-media-format-sdk"></a><span data-ttu-id="c7346-103">Déverrouillage du kit de développement logiciel (SDK) Windows Media format</span><span class="sxs-lookup"><span data-stu-id="c7346-103">Unlocking the Windows Media Format SDK</span></span>

<span data-ttu-id="c7346-104">Pour accéder à la version 7 ou 7,1 du kit de développement logiciel (SDK) Windows Media format, une application doit fournir un certificat logiciel, également appelé clé, au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="c7346-104">To access version 7 or 7.1 of the Windows Media Format SDK, an application must provide a software certificate, also called a key, at run time.</span></span> <span data-ttu-id="c7346-105">Cette clé est contenue dans une bibliothèque statique appelée wmstub. lib, à laquelle l’application établit une liaison au moment de la génération.</span><span class="sxs-lookup"><span data-stu-id="c7346-105">This key is contained in a static library called wmstub.lib to which the application links at build time.</span></span> <span data-ttu-id="c7346-106">Une clé individualisée est uniquement nécessaire pour créer ou lire des fichiers protégés par DRM.</span><span class="sxs-lookup"><span data-stu-id="c7346-106">An individualized key is only required for creating or reading DRM-protected files.</span></span> <span data-ttu-id="c7346-107">Les fichiers non DRM peuvent être créés à l’aide de la bibliothèque statique fournie avec le kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="c7346-107">Non-DRM files can be created using the static library provided with the Windows Media Format SDK.</span></span> <span data-ttu-id="c7346-108">Pour plus d’informations sur l’obtention de la clé DRM, consultez le kit de développement logiciel (SDK) de format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c7346-108">For details on obtaining the DRM key, see the Windows Media Format SDK.</span></span> <span data-ttu-id="c7346-109">Une application DirectShow fournit son certificat à l’enregistreur ASF WM lorsqu’il est ajouté au graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="c7346-109">A DirectShow application provides its certificate to the WM ASF Writer when it is added to the filter graph.</span></span> <span data-ttu-id="c7346-110">L’application doit s’inscrire en tant que fournisseur de clés à l’aide des interfaces COM **IServiceProvider** et **IObjectWithSite** .</span><span class="sxs-lookup"><span data-stu-id="c7346-110">The application must register as a key provider using the COM **IServiceProvider** and **IObjectWithSite** interfaces.</span></span> <span data-ttu-id="c7346-111">À l’aide de cette technique, l’application implémente une classe de fournisseur de clé dérivée de **IServiceProvider**.</span><span class="sxs-lookup"><span data-stu-id="c7346-111">Using this technique, the application implements a key provider class derived from **IServiceProvider**.</span></span> <span data-ttu-id="c7346-112">Cette classe implémente les trois méthodes COM standard (**AddRef**, **QueryInterface** et **Release**), ainsi qu’une autre méthode, **QueryService**, qui est appelée par le gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="c7346-112">This class implements the three standard COM methods—**AddRef**, **QueryInterface**, and **Release**—along with one additional method, **QueryService**, which is called by the filter graph manager.</span></span> <span data-ttu-id="c7346-113">**QueryService** appelle la méthode du kit de développement logiciel (SDK) Windows Media format [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) et retourne au gestionnaire du graphique de filtres un pointeur vers le certificat qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="c7346-113">**QueryService** calls the Windows Media Format SDK method [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) and returns to the filter graph manager a pointer to the certificate that was created.</span></span> <span data-ttu-id="c7346-114">Si le certificat est valide, le gestionnaire de graphes de filtre permet au processus de création de graphique de continuer.</span><span class="sxs-lookup"><span data-stu-id="c7346-114">If the certificate is valid, the filter graph manager allows the graph-building process to proceed.</span></span>

> [!Note]  
> <span data-ttu-id="c7346-115">Pour générer une application, incluez Wmsdkidl. h pour le prototype de [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85))et liez-la à la bibliothèque Wmstub. lib.</span><span class="sxs-lookup"><span data-stu-id="c7346-115">To build an application, include Wmsdkidl.h for the prototype for [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)), and link to the Wmstub.lib library.</span></span>

 

<span data-ttu-id="c7346-116">L’exemple de code suivant illustre les étapes de base de ce processus :</span><span class="sxs-lookup"><span data-stu-id="c7346-116">The following code example illustrates the basic steps in this process:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c7346-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c7346-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7346-118">Création de fichiers ASF dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="c7346-118">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
