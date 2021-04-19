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
# <a name="custom-topology-loaders"></a><span data-ttu-id="91ecd-103">Chargeurs de topologie personnalisés</span><span class="sxs-lookup"><span data-stu-id="91ecd-103">Custom Topology Loaders</span></span>

<span data-ttu-id="91ecd-104">Lorsqu’une application met en file d’attente une topologie partielle sur la session multimédia, la session multimédia utilise un chargeur de topologie pour résoudre la topologie.</span><span class="sxs-lookup"><span data-stu-id="91ecd-104">When an application queues a partial topology on the Media Session, the Media Session uses a topology loader to resolve the topology.</span></span> <span data-ttu-id="91ecd-105">Par défaut, la session multimédia utilise l’implémentation standard Media Foundation du chargeur de topologie, mais vous pouvez également fournir une implémentation personnalisée.</span><span class="sxs-lookup"><span data-stu-id="91ecd-105">By default, the Media Session uses the standard Media Foundation implementation of the topology loader, but you can also provide a custom implementation.</span></span> <span data-ttu-id="91ecd-106">Cela vous donne davantage de contrôle sur la topologie finale.</span><span class="sxs-lookup"><span data-stu-id="91ecd-106">This gives you more control over the final topology.</span></span> <span data-ttu-id="91ecd-107">Un chargeur de topologie personnalisé doit implémenter l’interface [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) .</span><span class="sxs-lookup"><span data-stu-id="91ecd-107">A custom topology loader must implement the [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) interface.</span></span>

<span data-ttu-id="91ecd-108">Pour définir un chargeur de topologie personnalisé sur la session multimédia, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="91ecd-108">To set a custom topology loader on the Media Session, do the following:</span></span>

1.  <span data-ttu-id="91ecd-109">Créez un magasin d’attributs vide en appelant [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span><span class="sxs-lookup"><span data-stu-id="91ecd-109">Create an empty attribute store by calling [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>
2.  <span data-ttu-id="91ecd-110">Définissez l' [**attribut \_ \_ TOPOLOADER de session MF**](mf-session-topoloader-attribute.md) sur le magasin d’attributs.</span><span class="sxs-lookup"><span data-stu-id="91ecd-110">Set the [**MF\_SESSION\_TOPOLOADER**](mf-session-topoloader-attribute.md) attribute on the attribute store.</span></span> <span data-ttu-id="91ecd-111">La valeur de l’attribut est le CLSID de votre chargeur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="91ecd-111">The value of the attribute is the CLSID of your custom loader.</span></span>
3.  <span data-ttu-id="91ecd-112">Appelez [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) pour créer la session multimédia pour du contenu non protégé ou [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) pour créer la session multimédia à l’intérieur du chemin d’accès de média protégé (PMP).</span><span class="sxs-lookup"><span data-stu-id="91ecd-112">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create the Media Session for unprotected content, or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) to create the Media Session inside the protected media path (PMP).</span></span>

> [!Note]  
> <span data-ttu-id="91ecd-113">Pour utiliser un chargeur de topologie personnalisé à l’intérieur du PMP, le chargeur de topologie doit être un composant approuvé.</span><span class="sxs-lookup"><span data-stu-id="91ecd-113">To use a custom topology loader inside the PMP, the topology loader must be a trusted component.</span></span> <span data-ttu-id="91ecd-114">Pour plus d’informations, consultez [chemin d’accès au média protégé](protected-media-path.md).</span><span class="sxs-lookup"><span data-stu-id="91ecd-114">For more information, see [Protected Media Path](protected-media-path.md).</span></span>

 

<span data-ttu-id="91ecd-115">Le code suivant montre comment définir un chargeur de topologie personnalisé sur la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="91ecd-115">The following code shows how to set a custom topology loader on the Media Session.</span></span>


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



<span data-ttu-id="91ecd-116">Il n’est pas nécessaire d’implémenter l’intégralité de l’algorithme de chargement de topologie dans le chargeur de topologie.</span><span class="sxs-lookup"><span data-stu-id="91ecd-116">It is not necessary to implement the entire topology-loading algorithm in your topology loader.</span></span> <span data-ttu-id="91ecd-117">Vous pouvez également encapsuler le chargeur de topologie Media Foundation standard.</span><span class="sxs-lookup"><span data-stu-id="91ecd-117">As an alternative, you can wrap the standard Media Foundation topology loader.</span></span> <span data-ttu-id="91ecd-118">Dans votre implémentation de la méthode [**IMFTopoLoader :: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) , modifiez la topologie en fonction des besoins et transmettez la topologie modifiée au chargeur de topologie standard.</span><span class="sxs-lookup"><span data-stu-id="91ecd-118">In your implementation of the [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method, modify the topology as needed and pass the modified topology to the standard topology loader.</span></span> <span data-ttu-id="91ecd-119">Le chargeur de topologie standard termine la topologie.</span><span class="sxs-lookup"><span data-stu-id="91ecd-119">Then the standard topology loader completes the topology.</span></span> <span data-ttu-id="91ecd-120">Vous pouvez également modifier la topologie terminée avant de la retransmettre à la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="91ecd-120">You can also modify the completed topology before passing it back to the Media Session.</span></span>

<span data-ttu-id="91ecd-121">Le code suivant illustre la structure générale de cette approche.</span><span class="sxs-lookup"><span data-stu-id="91ecd-121">The following code shows the general outline of this approach.</span></span> <span data-ttu-id="91ecd-122">Il n’affiche aucun détail de la méthode [**Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) , car ceux-ci dépendent des besoins particuliers de votre application.</span><span class="sxs-lookup"><span data-stu-id="91ecd-122">It does not show any details of the [**Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method, because these will depend on the particular requirements of your application.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="91ecd-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="91ecd-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91ecd-124">**MFCreateTopoLoader**</span><span class="sxs-lookup"><span data-stu-id="91ecd-124">**MFCreateTopoLoader**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader)
</dt> <dt>

[<span data-ttu-id="91ecd-125">Génération de topologie avancée</span><span class="sxs-lookup"><span data-stu-id="91ecd-125">Advanced Topology Building</span></span>](advanced-topology-building.md)
</dt> </dl>

 

 



