---
description: Microsoft Media Foundation utilise une combinaison de constructions COM, mais n’est pas une API entièrement basée sur COM.
ms.assetid: d58ca46f-8f3a-4a12-b948-1ea7ab568788
title: Media Foundation et COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb7d05bac6a3f4deef2c004c6980ef1351c3823
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106529535"
---
# <a name="media-foundation-and-com"></a><span data-ttu-id="6ef70-103">Media Foundation et COM</span><span class="sxs-lookup"><span data-stu-id="6ef70-103">Media Foundation and COM</span></span>

<span data-ttu-id="6ef70-104">Microsoft Media Foundation utilise une combinaison de constructions COM, mais n’est pas une API entièrement basée sur COM.</span><span class="sxs-lookup"><span data-stu-id="6ef70-104">Microsoft Media Foundation uses a mix of COM constructs, but is not a fully COM-based API.</span></span> <span data-ttu-id="6ef70-105">Cette rubrique décrit l’interaction entre COM et Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6ef70-105">This topic describes the interaction between COM and Media Foundation.</span></span> <span data-ttu-id="6ef70-106">Il définit également quelques pratiques recommandées pour le développement de composants de plug-in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6ef70-106">It also defines some best practices for developing Media Foundation plug-in components.</span></span> <span data-ttu-id="6ef70-107">Les pratiques suivantes peuvent vous aider à éviter des erreurs de programmation courantes mais subtiles.</span><span class="sxs-lookup"><span data-stu-id="6ef70-107">Following these practices can help you to avoid some common but subtle programming errors.</span></span>

-   [<span data-ttu-id="6ef70-108">Meilleures pratiques pour les applications</span><span class="sxs-lookup"><span data-stu-id="6ef70-108">Best Practices for Applications</span></span>](#best-practices-for-applications)
-   [<span data-ttu-id="6ef70-109">Meilleures pratiques pour les composants Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6ef70-109">Best Practices for Media Foundation Components</span></span>](#best-practices-for-media-foundation-components)
-   [<span data-ttu-id="6ef70-110">Résumé</span><span class="sxs-lookup"><span data-stu-id="6ef70-110">Summary</span></span>](#summary)
-   [<span data-ttu-id="6ef70-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6ef70-111">Related topics</span></span>](#related-topics)

## <a name="best-practices-for-applications"></a><span data-ttu-id="6ef70-112">Meilleures pratiques pour les applications</span><span class="sxs-lookup"><span data-stu-id="6ef70-112">Best Practices for Applications</span></span>

<span data-ttu-id="6ef70-113">Dans Media Foundation, le traitement asynchrone et les rappels sont gérés par les [files d’attente de travail](work-queues.md).</span><span class="sxs-lookup"><span data-stu-id="6ef70-113">In Media Foundation, asynchronous processing and callbacks are handled by [work queues](work-queues.md).</span></span> <span data-ttu-id="6ef70-114">Les files d’attente de travail ont toujours des threads de cloisonnement multithread (MTA). par conséquent, une application aura une implémentation plus simple si elle s’exécute également sur un thread MTA.</span><span class="sxs-lookup"><span data-stu-id="6ef70-114">Work queues always have multithreaded apartment (MTA) threads, so an application will have a simpler implementation if it runs on an MTA thread as well.</span></span> <span data-ttu-id="6ef70-115">Par conséquent, il est recommandé d’appeler [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) avec l’indicateur **coinit \_ multithread** .</span><span class="sxs-lookup"><span data-stu-id="6ef70-115">Therefore, it is recommended to call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) with the **COINIT\_MULTITHREADED** flag.</span></span>

<span data-ttu-id="6ef70-116">Media Foundation ne marshale pas les objets cloisonnés (STA) à thread unique pour les threads de file d’attente de travail.</span><span class="sxs-lookup"><span data-stu-id="6ef70-116">Media Foundation does not marshal single-threaded apartment (STA) objects to work queue threads.</span></span> <span data-ttu-id="6ef70-117">Cela ne garantit pas non plus que les invariants STA sont conservés.</span><span class="sxs-lookup"><span data-stu-id="6ef70-117">Nor does it ensure that STA invariants are maintained.</span></span> <span data-ttu-id="6ef70-118">Par conséquent, une application STA doit veiller à ne pas passer des objets STA ou des proxies à des API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6ef70-118">Therefore, an STA application must be careful to not pass STA objects or proxies to Media Foundation APIs.</span></span> <span data-ttu-id="6ef70-119">Les objets qui sont STA uniquement ne sont pas pris en charge dans Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6ef70-119">Objects that are STA-only are not supported in Media Foundation.</span></span>

<span data-ttu-id="6ef70-120">Si vous avez un proxy STA vers un objet MTA ou un objet thread libre, l’objet peut être marshalé vers un proxy MTA à l’aide d’un rappel de file d’attente de travail.</span><span class="sxs-lookup"><span data-stu-id="6ef70-120">If you have an STA proxy to an MTA or free-threaded object, the object can be marshaled to an MTA proxy by using a work-queue callback.</span></span> <span data-ttu-id="6ef70-121">La fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) peut retourner un pointeur brut ou un proxy STA, en fonction du modèle d’objet défini dans le registre pour ce CLSID.</span><span class="sxs-lookup"><span data-stu-id="6ef70-121">The [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function can return either a raw pointer or an STA proxy, depending on the object model defined in the registry for that CLSID.</span></span> <span data-ttu-id="6ef70-122">Si un proxy STA est retourné, vous ne devez pas passer le pointeur à une API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6ef70-122">If an STA proxy is returned, you must not pass the pointer to a Media Foundation API.</span></span>

<span data-ttu-id="6ef70-123">Supposons, par exemple, que vous souhaitiez passer un pointeur **IPropertyStore** à la méthode [**IMFSourceResolver :: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) .</span><span class="sxs-lookup"><span data-stu-id="6ef70-123">For example, suppose that you want to pass an **IPropertyStore** pointer to the [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) method.</span></span> <span data-ttu-id="6ef70-124">Vous pouvez appeler **PSCreateMemoryPropertyStore** pour créer le pointeur **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="6ef70-124">You might call **PSCreateMemoryPropertyStore** to create the **IPropertyStore** pointer.</span></span> <span data-ttu-id="6ef70-125">Si vous appelez à partir d’un STA, vous devez marshaler le pointeur avant de le passer à **BeginCreateObjectFromURL**.</span><span class="sxs-lookup"><span data-stu-id="6ef70-125">If you are calling from an STA, you must marshal the pointer before passing it to **BeginCreateObjectFromURL**.</span></span>

<span data-ttu-id="6ef70-126">Le code suivant montre comment marshaler un proxy STA vers une API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6ef70-126">The following code shows how to marshal an STA proxy to a Media Foundation API.</span></span>


```C++
class CCreateSourceMarshalCallback
    : public IMFAsyncCallback
{
public:
    CCreateSourceMarshalCallback(
        LPCWSTR szURL, 
        IMFSourceResolver* pResolver, 
        IPropertyStore* pSourceProps, 
        IMFAsyncCallback* pCompletionCallback, 
        HRESULT& hr
        )
        : m_szURL(szURL), 
          m_pResolver(pResolver), 
          m_pCompletionCallback(pCompletionCallback),
          m_pGIT(NULL),
          m_cRef(1)
    {
        hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable, NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&m_pGIT));

        if(SUCCEEDED(hr))
        {
            hr = m_pGIT->RegisterInterfaceInGlobal(
                pSourceProps, IID_IPropertyStore, &m_dwInterfaceCookie);
        }
    }
    ~CCreateSourceMarshalCallback()
    {
        SafeRelease(&m_pResolver);
        SafeRelease(&m_pCompletionCallback);
        SafeRelease(&m_pGIT);
    }


    STDMETHOD_(ULONG, AddRef)()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHOD_(ULONG, Release)()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (0 == cRef)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHOD(QueryInterface)(REFIID riid, LPVOID* ppvObject)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CCreateSourceMarshalCallback, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppvObject);

    }

    STDMETHOD(GetParameters)(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        return E_NOTIMPL;
    }

    STDMETHOD(Invoke)(IMFAsyncResult* pResult)
    {
        IPropertyStore *pSourceProps = NULL;

        HRESULT hr = m_pGIT->GetInterfaceFromGlobal(
            m_dwInterfaceCookie, 
            IID_PPV_ARGS(&pSourceProps)
            );

        if(SUCCEEDED(hr))
        {
            hr = m_pResolver->BeginCreateObjectFromURL(
                m_szURL, MF_RESOLUTION_MEDIASOURCE, pSourceProps, NULL, 
                m_pCompletionCallback, NULL);
        }

        SafeRelease(&pSourceProps);
        return hr;
    }

private:
    LPCWSTR m_szURL;
    IMFSourceResolver *m_pResolver;
    IMFAsyncCallback *m_pCompletionCallback;
    IGlobalInterfaceTable *m_pGIT;
    DWORD m_dwInterfaceCookie;
    LONG m_cRef;
};
```



<span data-ttu-id="6ef70-127">Pour plus d’informations sur la table d’interface globale, consultez [**IGlobalInterfaceTable**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span><span class="sxs-lookup"><span data-stu-id="6ef70-127">For more information about the global interface table, see [**IGlobalInterfaceTable**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span></span>

<span data-ttu-id="6ef70-128">Si vous utilisez Media Foundation in-process, les objets retournés à partir de Media Foundation méthodes et fonctions sont des pointeurs directs vers l’objet.</span><span class="sxs-lookup"><span data-stu-id="6ef70-128">If you are using Media Foundation in-process, objects returned from Media Foundation methods and functions are direct pointers to the object.</span></span> <span data-ttu-id="6ef70-129">Pour les Media Foundation interprocessus, ces objets peuvent être des proxies MTA et doivent être marshalés dans un thread STA, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="6ef70-129">For cross-process Media Foundation, these objects may be MTA proxies, and should be marshaled into an STA thread if needed there.</span></span> <span data-ttu-id="6ef70-130">De même, les objets obtenus à l’intérieur d’un rappel, par exemple une topologie de l’événement [MESessionTopologyStatus](mesessiontopologystatus.md) , sont des pointeurs directs lorsque Media Foundation est utilisé dans le processus, mais sont des proxies MTA quand Media Foundation est utilisé interprocessus.</span><span class="sxs-lookup"><span data-stu-id="6ef70-130">Similarly, objects obtained inside a callback — for example, a topology from the [MESessionTopologyStatus](mesessiontopologystatus.md) event — are direct pointers when Media Foundation is used in-process, but are MTA proxies when Media Foundation is used cross-process.</span></span>

> [!Note]  
> <span data-ttu-id="6ef70-131">Le scénario le plus courant pour l’utilisation de Media Foundation interprocessus consiste à utiliser le [chemin d’accès du média protégé](protected-media-path.md) (PMP).</span><span class="sxs-lookup"><span data-stu-id="6ef70-131">The most common scenario for using Media Foundation cross-process is with the [Protected Media Path](protected-media-path.md) (PMP).</span></span> <span data-ttu-id="6ef70-132">Toutefois, ces remarques s’appliquent à toutes les situations où des API Media Foundation sont utilisées par le biais de RPC.</span><span class="sxs-lookup"><span data-stu-id="6ef70-132">However, these remarks apply to any situation when Media Foundation APIs are used through RPC.</span></span>

 

<span data-ttu-id="6ef70-133">Toutes les implémentations de [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) doivent être compatibles avec le MTA.</span><span class="sxs-lookup"><span data-stu-id="6ef70-133">All implementations of [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) should be MTA-compatible.</span></span> <span data-ttu-id="6ef70-134">Il n’est pas nécessaire que ces objets soient des objets COM.</span><span class="sxs-lookup"><span data-stu-id="6ef70-134">These objects do not need to be COM objects at all.</span></span> <span data-ttu-id="6ef70-135">Mais s’ils sont, ils ne peuvent pas s’exécuter dans le STA.</span><span class="sxs-lookup"><span data-stu-id="6ef70-135">But if they are, they cannot run in the STA.</span></span> <span data-ttu-id="6ef70-136">La fonction [**IMFAsyncCallback :: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) sera appelée sur un thread MTA workqueue, et l’objet [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) fourni sera soit un pointeur d’objet direct, soit un proxy MTA.</span><span class="sxs-lookup"><span data-stu-id="6ef70-136">The [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) function will be invoked on an MTA workqueue thread, and the provided [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) object will be either a direct object pointer or an MTA proxy.</span></span>

## <a name="best-practices-for-media-foundation-components"></a><span data-ttu-id="6ef70-137">Meilleures pratiques pour les composants Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6ef70-137">Best Practices for Media Foundation Components</span></span>

<span data-ttu-id="6ef70-138">Il existe deux catégories d’objets Media Foundation qui doivent se préoccuper de COM.</span><span class="sxs-lookup"><span data-stu-id="6ef70-138">There are two categories of Media Foundation objects that need to be concerned about COM.</span></span> <span data-ttu-id="6ef70-139">Certains composants, tels que les transformations ou les gestionnaires de flux d’octets, sont des objets COM complets créés par CLSID.</span><span class="sxs-lookup"><span data-stu-id="6ef70-139">Some components, such as transforms or byte stream handlers, are full COM objects created by CLSID.</span></span> <span data-ttu-id="6ef70-140">Ces objets doivent suivre les règles pour les cloisonnements COM, pour les Media Foundation interprocessus et in-process.</span><span class="sxs-lookup"><span data-stu-id="6ef70-140">These objects must follow the rules for COM apartments, for both in-process and cross-process Media Foundation.</span></span> <span data-ttu-id="6ef70-141">Les autres composants de Media Foundation ne sont pas des objets COM complets, mais ils ont besoin de proxys COM pour la lecture inter-processus.</span><span class="sxs-lookup"><span data-stu-id="6ef70-141">Other Media Foundation components are not full COM objects, but do need COM proxies for cross-process playback.</span></span> <span data-ttu-id="6ef70-142">Les objets de cette catégorie incluent les sources de média et l’objet d’activation.</span><span class="sxs-lookup"><span data-stu-id="6ef70-142">Objects in this category include media sources and activation object.</span></span> <span data-ttu-id="6ef70-143">Ces objets peuvent ignorer les problèmes de cloisonnement s’ils sont utilisés uniquement pour les Media Foundation in-process.</span><span class="sxs-lookup"><span data-stu-id="6ef70-143">These objects can ignore apartment issues if they will be used only for in-process Media Foundation.</span></span>

<span data-ttu-id="6ef70-144">Bien que tous les objets Media Foundation ne soient pas des objets COM, toutes les interfaces Media Foundation dérivent de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="6ef70-144">Although not all Media Foundation objects are COM objects, all Media Foundation interfaces derive from [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="6ef70-145">Par conséquent, tous les objets Media Foundation doivent implémenter **IUnknown** conformément aux spécifications com, y compris les règles pour le décompte de références et [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="6ef70-145">Therefore, all Media Foundation objects must implement **IUnknown** according to COM specifications, including the rules for reference counting and [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="6ef70-146">Tous les objets de référence décomptés doivent également s’assurer que [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) n’autorise pas le déchargement du module tant que les objets persistent.</span><span class="sxs-lookup"><span data-stu-id="6ef70-146">All reference counted objects should also ensure that [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) will not allow the module to be unloaded while the objects still persist.</span></span>

<span data-ttu-id="6ef70-147">Les composants Media Foundation ne peuvent pas être des objets STA.</span><span class="sxs-lookup"><span data-stu-id="6ef70-147">Media Foundation components cannot be STA objects.</span></span> <span data-ttu-id="6ef70-148">De nombreux objets Media Foundation n’ont pas besoin d’être des objets COM.</span><span class="sxs-lookup"><span data-stu-id="6ef70-148">Many Media Foundation objects do not need to be COM objects at all.</span></span> <span data-ttu-id="6ef70-149">Mais s’ils sont, ils ne peuvent pas s’exécuter dans le STA.</span><span class="sxs-lookup"><span data-stu-id="6ef70-149">But if they are, they cannot run in the STA.</span></span> <span data-ttu-id="6ef70-150">Tous les composants Media Foundation doivent être thread-safe.</span><span class="sxs-lookup"><span data-stu-id="6ef70-150">All Media Foundation components must be thread-safe.</span></span> <span data-ttu-id="6ef70-151">Certains objets Media Foundation doivent également être à threads libres ou à Neutral Apartment.</span><span class="sxs-lookup"><span data-stu-id="6ef70-151">Some Media Foundation objects must be free-threaded or apartment-neutral as well.</span></span> <span data-ttu-id="6ef70-152">Le tableau suivant spécifie les conditions requises pour les implémentations d’interfaces personnalisées :</span><span class="sxs-lookup"><span data-stu-id="6ef70-152">The following table specifies the requirements for custom interface implementations:</span></span>



| <span data-ttu-id="6ef70-153">Interface</span><span class="sxs-lookup"><span data-stu-id="6ef70-153">Interface</span></span>                                                          | <span data-ttu-id="6ef70-154">Category</span><span class="sxs-lookup"><span data-stu-id="6ef70-154">Category</span></span>            | <span data-ttu-id="6ef70-155">Cloisonnement requis</span><span class="sxs-lookup"><span data-stu-id="6ef70-155">Required apartment</span></span>       |
|--------------------------------------------------------------------|---------------------|--------------------------|
| [<span data-ttu-id="6ef70-156">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="6ef70-156">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)                                 | <span data-ttu-id="6ef70-157">Proxy inter-processus</span><span class="sxs-lookup"><span data-stu-id="6ef70-157">Cross-process proxy</span></span> | <span data-ttu-id="6ef70-158">Libre-thread ou neutre</span><span class="sxs-lookup"><span data-stu-id="6ef70-158">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="6ef70-159">**IMFByteStreamHandler**</span><span class="sxs-lookup"><span data-stu-id="6ef70-159">**IMFByteStreamHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)               | <span data-ttu-id="6ef70-160">Objet COM</span><span class="sxs-lookup"><span data-stu-id="6ef70-160">COM object</span></span>          | <span data-ttu-id="6ef70-161">MTA</span><span class="sxs-lookup"><span data-stu-id="6ef70-161">MTA</span></span>                      |
| [<span data-ttu-id="6ef70-162">**IMFContentProtectionManager**</span><span class="sxs-lookup"><span data-stu-id="6ef70-162">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) | <span data-ttu-id="6ef70-163">Proxy inter-processus</span><span class="sxs-lookup"><span data-stu-id="6ef70-163">Cross-process proxy</span></span> | <span data-ttu-id="6ef70-164">Libre-thread ou neutre</span><span class="sxs-lookup"><span data-stu-id="6ef70-164">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="6ef70-165">**IMFQualityManager**</span><span class="sxs-lookup"><span data-stu-id="6ef70-165">**IMFQualityManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)                     | <span data-ttu-id="6ef70-166">Objet COM</span><span class="sxs-lookup"><span data-stu-id="6ef70-166">COM object</span></span>          | <span data-ttu-id="6ef70-167">Libre-thread ou neutre</span><span class="sxs-lookup"><span data-stu-id="6ef70-167">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="6ef70-168">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="6ef70-168">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                           | <span data-ttu-id="6ef70-169">Proxy inter-processus</span><span class="sxs-lookup"><span data-stu-id="6ef70-169">Cross-process proxy</span></span> | <span data-ttu-id="6ef70-170">Libre-thread ou neutre</span><span class="sxs-lookup"><span data-stu-id="6ef70-170">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="6ef70-171">**IMFSchemeHandler**</span><span class="sxs-lookup"><span data-stu-id="6ef70-171">**IMFSchemeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)                       | <span data-ttu-id="6ef70-172">Objet COM</span><span class="sxs-lookup"><span data-stu-id="6ef70-172">COM object</span></span>          | <span data-ttu-id="6ef70-173">MTA</span><span class="sxs-lookup"><span data-stu-id="6ef70-173">MTA</span></span>                      |
| [<span data-ttu-id="6ef70-174">**IMFTopoLoader**</span><span class="sxs-lookup"><span data-stu-id="6ef70-174">**IMFTopoLoader**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)                             | <span data-ttu-id="6ef70-175">Objet COM</span><span class="sxs-lookup"><span data-stu-id="6ef70-175">COM object</span></span>          | <span data-ttu-id="6ef70-176">Libre-thread ou neutre</span><span class="sxs-lookup"><span data-stu-id="6ef70-176">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="6ef70-177">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="6ef70-177">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                               | <span data-ttu-id="6ef70-178">Objet COM</span><span class="sxs-lookup"><span data-stu-id="6ef70-178">COM object</span></span>          | <span data-ttu-id="6ef70-179">MTA</span><span class="sxs-lookup"><span data-stu-id="6ef70-179">MTA</span></span>                      |



 

<span data-ttu-id="6ef70-180">Il peut y avoir des exigences supplémentaires en fonction de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="6ef70-180">There may be additional requirements depending upon the implementation.</span></span> <span data-ttu-id="6ef70-181">Par exemple, si un récepteur multimédia implémente une autre interface qui permet à l’application d’effectuer des appels de fonction directs au récepteur, le récepteur doit être libre de thread ou neutre, afin qu’il puisse gérer les appels inter-processus directs.</span><span class="sxs-lookup"><span data-stu-id="6ef70-181">For example, if a media sink implements another interface that enables the application to make direct function calls to the sink, the sink would need to be free-threaded or neutral, so that it could handle direct cross-process calls.</span></span> <span data-ttu-id="6ef70-182">Tout objet peut être libre de threads ; ce tableau spécifie la configuration minimale requise.</span><span class="sxs-lookup"><span data-stu-id="6ef70-182">Any object may be free-threaded; this table specifies the minimum requirements.</span></span>

<span data-ttu-id="6ef70-183">La méthode recommandée pour implémenter des objets à thread libre ou neutre consiste à agréger le marshaleur libre de threads.</span><span class="sxs-lookup"><span data-stu-id="6ef70-183">The recommended way to implement free-threaded or neutral objects is by aggregating the free-threaded marshaler.</span></span> <span data-ttu-id="6ef70-184">Pour plus d’informations, consultez la documentation MSDN sur [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler).</span><span class="sxs-lookup"><span data-stu-id="6ef70-184">For more details, see the MSDN documentation on [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler).</span></span> <span data-ttu-id="6ef70-185">Conformément à la nécessité de ne pas passer des objets STA ou des proxies à des API Media Foundation, les objets à thread libre n’ont pas besoin de se préoccuper du marshaling des pointeurs d’entrée STA dans les composants à threads libres.</span><span class="sxs-lookup"><span data-stu-id="6ef70-185">In accordance with the requirement not to pass STA objects or proxies to Media Foundation APIs, free-threaded objects do not need to worry about marshaling STA input pointers in free-threaded components.</span></span>

<span data-ttu-id="6ef70-186">Les composants qui utilisent la file d’attente de travail de longue durée (**\_ fonction de \_ \_ longue durée \_ de la file d’attente de rappel MFASYNC**) doivent faire preuve de prudence.</span><span class="sxs-lookup"><span data-stu-id="6ef70-186">Components that use the long-function work queue (**MFASYNC\_CALLBACK\_QUEUE\_LONG\_FUNCTION**) must exercise more care.</span></span> <span data-ttu-id="6ef70-187">Les threads de la fonction long workqueue créent leur propre STA.</span><span class="sxs-lookup"><span data-stu-id="6ef70-187">Threads in the long function workqueue create their own STA.</span></span> <span data-ttu-id="6ef70-188">Les composants qui utilisent la fonction long workqueue pour les rappels doivent éviter de créer des objets COM sur ces threads et doivent être prudents pour marshaler les proxies vers le STA en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="6ef70-188">Components that use the long function workqueue for callbacks should avoid creating COM objects on these threads, and need to be careful to marshal proxies to the STA as necessary.</span></span>

## <a name="summary"></a><span data-ttu-id="6ef70-189">Résumé</span><span class="sxs-lookup"><span data-stu-id="6ef70-189">Summary</span></span>

<span data-ttu-id="6ef70-190">Les applications auront plus de temps si elles interagissent avec les Media Foundation à partir d’un thread MTA, mais il est possible d’utiliser des Media Foundation à partir d’un thread STA.</span><span class="sxs-lookup"><span data-stu-id="6ef70-190">Applications will have an easier time if they interact with Media Foundation from an MTA thread, but it is possible with some care to use Media Foundation from an STA thread.</span></span> <span data-ttu-id="6ef70-191">Media Foundation ne gère pas les composants STA, et les applications doivent veiller à ne pas passer des objets STA à des API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6ef70-191">Media Foundation does not handle STA components, and applications should be careful not to pass STA objects to Media Foundation APIs.</span></span> <span data-ttu-id="6ef70-192">Certains objets ont des exigences supplémentaires, en particulier les objets qui s’exécutent dans une situation inter-processus.</span><span class="sxs-lookup"><span data-stu-id="6ef70-192">Some objects have additional requirements, especially objects that run in a cross-process situation.</span></span> <span data-ttu-id="6ef70-193">Le respect de ces recommandations permet d’éviter les erreurs COM, les blocages et les retards inattendus dans le traitement multimédia.</span><span class="sxs-lookup"><span data-stu-id="6ef70-193">Following these guidelines will help avoid COM errors, deadlocks, and unexpected delays in media processing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ef70-194">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6ef70-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ef70-195">API de plateforme Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6ef70-195">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> <dt>

[<span data-ttu-id="6ef70-196">Architecture Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6ef70-196">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 
