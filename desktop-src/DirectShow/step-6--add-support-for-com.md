---
description: Ajoutez la prise en charge de COM dans le cadre de l’écriture d’un filtre de transformation. Il s’agit de la dernière étape de ce didacticiel.
ms.assetid: 53e4f5b7-c85d-4b44-9a0c-0ad05ca872cc
title: Étape 6. Ajouter la prise en charge de COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097d51fa440812311edde9ce448916c66721a507
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406772"
---
# <a name="step-6-add-support-for-com"></a><span data-ttu-id="c2140-105">Étape 6.</span><span class="sxs-lookup"><span data-stu-id="c2140-105">Step 6.</span></span> <span data-ttu-id="c2140-106">Ajouter la prise en charge de COM</span><span class="sxs-lookup"><span data-stu-id="c2140-106">Add Support for COM</span></span>

<span data-ttu-id="c2140-107">Il s’agit de l’étape 6 du didacticiel [écriture de filtres de transformation](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="c2140-107">This is step 6 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="c2140-108">La dernière étape consiste à ajouter la prise en charge de COM.</span><span class="sxs-lookup"><span data-stu-id="c2140-108">The final step is to add support for COM.</span></span>

## <a name="reference-counting"></a><span data-ttu-id="c2140-109">Décompte de références</span><span class="sxs-lookup"><span data-stu-id="c2140-109">Reference Counting</span></span>

<span data-ttu-id="c2140-110">Vous n’avez pas à implémenter [**IUnknown :: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) ou [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="c2140-110">You do not have to implement [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) or [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="c2140-111">Toutes les classes de filtre et de code confidentiel dérivent de [**CUnknown**](cunknown.md), qui gère le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="c2140-111">All of the filter and pin classes derive from [**CUnknown**](cunknown.md), which handles reference counting.</span></span>

## <a name="queryinterface"></a><span data-ttu-id="c2140-112">QueryInterface</span><span class="sxs-lookup"><span data-stu-id="c2140-112">QueryInterface</span></span>

<span data-ttu-id="c2140-113">Toutes les classes de filtre et de code confidentiel implémentent [**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour toutes les interfaces COM qu’elles héritent.</span><span class="sxs-lookup"><span data-stu-id="c2140-113">All of the filter and pin classes implement [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for any COM interfaces they inherit.</span></span> <span data-ttu-id="c2140-114">Par exemple, [**CTransformFilter**](ctransformfilter.md) hérite de [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (via [**CBaseFilter**](cbasefilter.md)).</span><span class="sxs-lookup"><span data-stu-id="c2140-114">For example, [**CTransformFilter**](ctransformfilter.md) inherits [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (through [**CBaseFilter**](cbasefilter.md)).</span></span> <span data-ttu-id="c2140-115">Si votre filtre n’expose pas d’interfaces supplémentaires, vous n’avez rien à faire d’autre.</span><span class="sxs-lookup"><span data-stu-id="c2140-115">If your filter does not expose any additional interfaces, you do not have to do anything else.</span></span>

<span data-ttu-id="c2140-116">Pour exposer des interfaces supplémentaires, substituez la méthode [**CUnknown :: NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="c2140-116">To expose additional interfaces, override the [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method.</span></span> <span data-ttu-id="c2140-117">Par exemple, supposons que votre filtre implémente une interface personnalisée nommée IMyCustomInterface.</span><span class="sxs-lookup"><span data-stu-id="c2140-117">For example, suppose your filter implements a custom interface named IMyCustomInterface.</span></span> <span data-ttu-id="c2140-118">Pour exposer cette interface aux clients, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="c2140-118">To expose this interface to clients, do the following:</span></span>

-   <span data-ttu-id="c2140-119">Dérivez votre classe de filtre à partir de cette interface.</span><span class="sxs-lookup"><span data-stu-id="c2140-119">Derive your filter class from that interface.</span></span>
-   <span data-ttu-id="c2140-120">Placez la macro [**Declare \_ IUnknown**](declare-iunknown.md) dans la section Déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="c2140-120">Put the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public declaration section.</span></span>
-   <span data-ttu-id="c2140-121">Substituez [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) pour vérifier l’IID de votre interface et retourner un pointeur vers votre filtre.</span><span class="sxs-lookup"><span data-stu-id="c2140-121">Override [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) to check for the IID of your interface and return a pointer to your filter.</span></span>

<span data-ttu-id="c2140-122">Le code suivant illustre ces étapes :</span><span class="sxs-lookup"><span data-stu-id="c2140-122">The following code shows these steps:</span></span>


```C++
CMyFilter : public CBaseFilter, public IMyCustomInterface
{
public:
    DECLARE_IUNKNOWN
    STDMETHODIMP NonDelegatingQueryInterface(REFIID iid, void **ppv);
};
STDMETHODIMP CMyFilter::NonDelegatingQueryInterface(REFIID iid, void **ppv)
{
    if (riid == IID_IMyCustomInterface) {
        return GetInterface(static_cast<IMyCustomInterface*>(this), ppv);
    }
    return CBaseFilter::NonDelegatingQueryInterface(riid,ppv);
}
```



<span data-ttu-id="c2140-123">Pour plus d’informations, consultez [comment implémenter IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="c2140-123">For more information, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

## <a name="object-creation"></a><span data-ttu-id="c2140-124">Création d’objets</span><span class="sxs-lookup"><span data-stu-id="c2140-124">Object Creation</span></span>

<span data-ttu-id="c2140-125">Si vous envisagez de créer un package de votre filtre dans une DLL et de le mettre à la disposition d’autres clients, vous devez prendre en charge [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) et d’autres fonctions com associées.</span><span class="sxs-lookup"><span data-stu-id="c2140-125">If you plan to package your filter in a DLL and make it available to other clients, you must support [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) and other related COM functions.</span></span> <span data-ttu-id="c2140-126">La bibliothèque de classes de base implémente la plupart de ces. il vous suffit de fournir des informations sur votre filtre.</span><span class="sxs-lookup"><span data-stu-id="c2140-126">The base class library implements most of this; you just need to provide some information about your filter.</span></span> <span data-ttu-id="c2140-127">Cette section donne un bref aperçu de ce que vous devez faire.</span><span class="sxs-lookup"><span data-stu-id="c2140-127">This section gives a brief overview of what to do.</span></span> <span data-ttu-id="c2140-128">Pour plus d’informations, voir [How to Create a DirectShow Filter dll](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="c2140-128">For details, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

<span data-ttu-id="c2140-129">Tout d’abord, écrivez une méthode de classe statique qui retourne une nouvelle instance de votre filtre.</span><span class="sxs-lookup"><span data-stu-id="c2140-129">First, write a static class method that returns a new instance of your filter.</span></span> <span data-ttu-id="c2140-130">Vous pouvez nommer cette méthode comme vous le souhaitez, mais la signature doit correspondre à celle illustrée dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="c2140-130">You can name this method anything you like, but the signature must match the one shown in the following example:</span></span>


```C++
CUnknown * WINAPI CRleFilter::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr)
{
    CRleFilter *pFilter = new CRleFilter();
    if (pFilter== NULL) 
    {
        *pHr = E_OUTOFMEMORY;
    }
    return pFilter;
}
```



<span data-ttu-id="c2140-131">Ensuite, déclarez un tableau global d’instances de la classe [**CFactoryTemplate**](cfactorytemplate.md) , nommé *g \_ Templates*.</span><span class="sxs-lookup"><span data-stu-id="c2140-131">Next, declare a global array of [**CFactoryTemplate**](cfactorytemplate.md) class instances, named *g\_Templates*.</span></span> <span data-ttu-id="c2140-132">Chaque classe **CFactoryTemplate** contient des informations de Registre pour un filtre.</span><span class="sxs-lookup"><span data-stu-id="c2140-132">Each **CFactoryTemplate** class contains registry information for one filter.</span></span> <span data-ttu-id="c2140-133">Plusieurs filtres peuvent résider dans une seule DLL ; incluez simplement des entrées **CFactoryTemplate** supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="c2140-133">Several filters can reside in a single DLL; simply include additional **CFactoryTemplate** entries.</span></span> <span data-ttu-id="c2140-134">Vous pouvez également déclarer d’autres objets COM, tels que des pages de propriétés.</span><span class="sxs-lookup"><span data-stu-id="c2140-134">You can also declare other COM objects, such as property pages.</span></span>


```C++
static WCHAR g_wszName[] = L"My RLE Encoder";
CFactoryTemplate g_Templates[] = 
{
  { 
    g_wszName,
    &CLSID_RLEFilter,
    CRleFilter::CreateInstance,
    NULL,
    NULL
  }
};
```



<span data-ttu-id="c2140-135">Définissez un entier global nommé *g \_ cTemplates* dont la valeur est égale à la longueur du tableau de *\_ modèles g* :</span><span class="sxs-lookup"><span data-stu-id="c2140-135">Define a global integer named *g\_cTemplates* whose value equals the length of the *g\_Templates* array:</span></span>


```C++
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);  
```



<span data-ttu-id="c2140-136">Enfin, implémentez les fonctions d’inscription de DLL.</span><span class="sxs-lookup"><span data-stu-id="c2140-136">Finally, implement the DLL registration functions.</span></span> <span data-ttu-id="c2140-137">L’exemple suivant illustre l’implémentation minimale pour ces fonctions :</span><span class="sxs-lookup"><span data-stu-id="c2140-137">The following example shows the minimal implementation for these functions:</span></span>


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}
STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



## <a name="filter-registry-entries"></a><span data-ttu-id="c2140-138">Filtrer les entrées de Registre</span><span class="sxs-lookup"><span data-stu-id="c2140-138">Filter Registry Entries</span></span>

<span data-ttu-id="c2140-139">Les exemples précédents montrent comment inscrire le CLSID d’un filtre pour COM.</span><span class="sxs-lookup"><span data-stu-id="c2140-139">The previous examples show how to register a filter's CLSID for COM.</span></span> <span data-ttu-id="c2140-140">Pour de nombreux filtres, cela suffit.</span><span class="sxs-lookup"><span data-stu-id="c2140-140">For many filters, this is sufficient.</span></span> <span data-ttu-id="c2140-141">Le client est alors censé créer le filtre à l’aide de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) et l’ajouter au graphique de filtre en appelant [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter).</span><span class="sxs-lookup"><span data-stu-id="c2140-141">The client is then expected to create the filter using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) and add it to the filter graph by calling [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter).</span></span> <span data-ttu-id="c2140-142">Toutefois, dans certains cas, vous souhaiterez peut-être fournir des informations supplémentaires sur le filtre dans le registre.</span><span class="sxs-lookup"><span data-stu-id="c2140-142">In some cases, however, you might want to provide additional information about the filter in the registry.</span></span> <span data-ttu-id="c2140-143">Ces informations effectuent les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c2140-143">This information does the following:</span></span>

-   <span data-ttu-id="c2140-144">Permet aux clients de découvrir le filtre à l’aide du [Mappeur de filtre](filter-mapper.md) ou de l' [énumérateur du périphérique système](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="c2140-144">Enables clients to discover the filter using the [Filter Mapper](filter-mapper.md) or the [System Device Enumerator](system-device-enumerator.md).</span></span>
-   <span data-ttu-id="c2140-145">Permet au gestionnaire de graphique de filtre de découvrir le filtre pendant la génération automatique de graphiques.</span><span class="sxs-lookup"><span data-stu-id="c2140-145">Enables the Filter Graph Manager to discover the filter during automatic graph building.</span></span>

<span data-ttu-id="c2140-146">L’exemple suivant enregistre le filtre d’encodeur RLE dans la catégorie de compresseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="c2140-146">The following example registers the RLE encoder filter in the video compressor category.</span></span> <span data-ttu-id="c2140-147">Pour plus d’informations, consultez [comment inscrire des filtres DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="c2140-147">For details, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="c2140-148">Veillez à lire la section [instructions pour l’inscription des filtres](guidelines-for-registering-filters.md), qui décrit les pratiques recommandées pour l’inscription de filtres.</span><span class="sxs-lookup"><span data-stu-id="c2140-148">Be sure to read the section [Guidelines for Registering Filters](guidelines-for-registering-filters.md), which describes the recommended practices for filter registration.</span></span>


```C++
// Declare media type information.
FOURCCMap fccMap = FCC('MRLE'); 
REGPINTYPES sudInputTypes = { &MEDIATYPE_Video, &GUID_NULL };
REGPINTYPES sudOutputTypes = { &MEDIATYPE_Video, (GUID*)&fccMap };

// Declare pin information.
REGFILTERPINS sudPinReg[] = {
    // Input pin.
    { 0, FALSE, // Rendered?
         FALSE, // Output?
         FALSE, // Zero?
         FALSE, // Many?
         0, 0, 
         1, &sudInputTypes  // Media types.
    },
    // Output pin.
    { 0, FALSE, // Rendered?
         TRUE, // Output?
         FALSE, // Zero?
         FALSE, // Many?
         0, 0, 
         1, &sudOutputTypes      // Media types.
    }
};
 
// Declare filter information.
REGFILTER2 rf2FilterReg = {
    1,                // Version number.
    MERIT_DO_NOT_USE, // Merit.
    2,                // Number of pins.
    sudPinReg         // Pointer to pin information.
};

STDAPI DllRegisterServer(void)
{
    HRESULT hr = AMovieDllRegisterServer2(TRUE);
    if (FAILED(hr))
    {
        return hr;
    }
    IFilterMapper2 *pFM2 = NULL;
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);
    if (SUCCEEDED(hr))
    {
        hr = pFM2->RegisterFilter(
            CLSID_RLEFilter,                // Filter CLSID. 
            g_wszName,                       // Filter name.
            NULL,                            // Device moniker. 
            &CLSID_VideoCompressorCategory,  // Video compressor category.
            g_wszName,                       // Instance data.
            &rf2FilterReg                    // Filter information.
            );
        pFM2->Release();
    }
    return hr;
}

STDAPI DllUnregisterServer()
{
    HRESULT hr = AMovieDllRegisterServer2(FALSE);
    if (FAILED(hr))
    {
        return hr;
    }
    IFilterMapper2 *pFM2 = NULL;
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);
    if (SUCCEEDED(hr))
    {
        hr = pFM2->UnregisterFilter(&CLSID_VideoCompressorCategory, 
            g_wszName, CLSID_RLEFilter);
        pFM2->Release();
    }
    return hr;
}
```



<span data-ttu-id="c2140-149">En outre, les filtres n’ont pas besoin d’être empaquetés dans des dll.</span><span class="sxs-lookup"><span data-stu-id="c2140-149">Also, filters do not have to be packaged inside DLLs.</span></span> <span data-ttu-id="c2140-150">Dans certains cas, vous pouvez écrire un filtre spécialisé conçu uniquement pour une application spécifique.</span><span class="sxs-lookup"><span data-stu-id="c2140-150">In some cases, you might write a specialized filter that is designed only for a specific application.</span></span> <span data-ttu-id="c2140-151">Dans ce cas, vous pouvez compiler la classe de filtre directement dans votre application et la créer avec l' `new` opérateur, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="c2140-151">In that case, you can compile the filter class directly in your application, and create it with the `new` operator, as shown in the following example:</span></span>


```C++
#include "MyFilter.h"  // Header file that declares the filter class.
// Compile and link MyFilter.cpp.
int main()
{
    IBaseFilter *pFilter = 0;
    {
        // Scope to hide pF.
        CMyFilter* pF = new MyFilter();
        if (!pF)
        {
            printf("Could not create MyFilter.\n");
            return 1;
        }
        pF->QueryInterface(IID_IBaseFilter, 
            reinterpret_cast<void**>(&pFilter));
    }
    
    /* Now use pFilter as normal. */
    
    pFilter->Release();  // Deletes the filter.
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="c2140-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2140-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2140-153">Connexion intelligente</span><span class="sxs-lookup"><span data-stu-id="c2140-153">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> <dt>

[<span data-ttu-id="c2140-154">Écriture de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="c2140-154">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="c2140-155">Écriture de filtres de transformation</span><span class="sxs-lookup"><span data-stu-id="c2140-155">Writing Transform Filters</span></span>](writing-transform-filters.md)
</dt> </dl>

 

 
