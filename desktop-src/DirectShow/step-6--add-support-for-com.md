---
description: Étape 6.
ms.assetid: 53e4f5b7-c85d-4b44-9a0c-0ad05ca872cc
title: Étape 6. Ajouter la prise en charge de COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e477cc22650604bce623874c0afbba1063609e44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534686"
---
# <a name="step-6-add-support-for-com"></a><span data-ttu-id="7ba13-104">Étape 6.</span><span class="sxs-lookup"><span data-stu-id="7ba13-104">Step 6.</span></span> <span data-ttu-id="7ba13-105">Ajouter la prise en charge de COM</span><span class="sxs-lookup"><span data-stu-id="7ba13-105">Add Support for COM</span></span>

<span data-ttu-id="7ba13-106">Il s’agit de l’étape 6 du didacticiel [écriture de filtres de transformation](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="7ba13-106">This is step 6 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="7ba13-107">La dernière étape consiste à ajouter la prise en charge de COM.</span><span class="sxs-lookup"><span data-stu-id="7ba13-107">The final step is to add support for COM.</span></span>

## <a name="reference-counting"></a><span data-ttu-id="7ba13-108">Décompte de références</span><span class="sxs-lookup"><span data-stu-id="7ba13-108">Reference Counting</span></span>

<span data-ttu-id="7ba13-109">Vous n’avez pas à implémenter [**IUnknown :: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) ou [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="7ba13-109">You do not have to implement [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) or [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="7ba13-110">Toutes les classes de filtre et de code confidentiel dérivent de [**CUnknown**](cunknown.md), qui gère le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="7ba13-110">All of the filter and pin classes derive from [**CUnknown**](cunknown.md), which handles reference counting.</span></span>

## <a name="queryinterface"></a><span data-ttu-id="7ba13-111">QueryInterface</span><span class="sxs-lookup"><span data-stu-id="7ba13-111">QueryInterface</span></span>

<span data-ttu-id="7ba13-112">Toutes les classes de filtre et de code confidentiel implémentent [**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour toutes les interfaces COM qu’elles héritent.</span><span class="sxs-lookup"><span data-stu-id="7ba13-112">All of the filter and pin classes implement [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for any COM interfaces they inherit.</span></span> <span data-ttu-id="7ba13-113">Par exemple, [**CTransformFilter**](ctransformfilter.md) hérite de [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (via [**CBaseFilter**](cbasefilter.md)).</span><span class="sxs-lookup"><span data-stu-id="7ba13-113">For example, [**CTransformFilter**](ctransformfilter.md) inherits [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (through [**CBaseFilter**](cbasefilter.md)).</span></span> <span data-ttu-id="7ba13-114">Si votre filtre n’expose pas d’interfaces supplémentaires, vous n’avez rien à faire d’autre.</span><span class="sxs-lookup"><span data-stu-id="7ba13-114">If your filter does not expose any additional interfaces, you do not have to do anything else.</span></span>

<span data-ttu-id="7ba13-115">Pour exposer des interfaces supplémentaires, substituez la méthode [**CUnknown :: NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="7ba13-115">To expose additional interfaces, override the [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method.</span></span> <span data-ttu-id="7ba13-116">Par exemple, supposons que votre filtre implémente une interface personnalisée nommée IMyCustomInterface.</span><span class="sxs-lookup"><span data-stu-id="7ba13-116">For example, suppose your filter implements a custom interface named IMyCustomInterface.</span></span> <span data-ttu-id="7ba13-117">Pour exposer cette interface aux clients, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7ba13-117">To expose this interface to clients, do the following:</span></span>

-   <span data-ttu-id="7ba13-118">Dérivez votre classe de filtre à partir de cette interface.</span><span class="sxs-lookup"><span data-stu-id="7ba13-118">Derive your filter class from that interface.</span></span>
-   <span data-ttu-id="7ba13-119">Placez la macro [**Declare \_ IUnknown**](declare-iunknown.md) dans la section Déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="7ba13-119">Put the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public declaration section.</span></span>
-   <span data-ttu-id="7ba13-120">Substituez [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) pour vérifier l’IID de votre interface et retourner un pointeur vers votre filtre.</span><span class="sxs-lookup"><span data-stu-id="7ba13-120">Override [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) to check for the IID of your interface and return a pointer to your filter.</span></span>

<span data-ttu-id="7ba13-121">Le code suivant illustre ces étapes :</span><span class="sxs-lookup"><span data-stu-id="7ba13-121">The following code shows these steps:</span></span>


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



<span data-ttu-id="7ba13-122">Pour plus d’informations, consultez [comment implémenter IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="7ba13-122">For more information, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

## <a name="object-creation"></a><span data-ttu-id="7ba13-123">Création d’objets</span><span class="sxs-lookup"><span data-stu-id="7ba13-123">Object Creation</span></span>

<span data-ttu-id="7ba13-124">Si vous envisagez de créer un package de votre filtre dans une DLL et de le mettre à la disposition d’autres clients, vous devez prendre en charge [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) et d’autres fonctions com associées.</span><span class="sxs-lookup"><span data-stu-id="7ba13-124">If you plan to package your filter in a DLL and make it available to other clients, you must support [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) and other related COM functions.</span></span> <span data-ttu-id="7ba13-125">La bibliothèque de classes de base implémente la plupart de ces. il vous suffit de fournir des informations sur votre filtre.</span><span class="sxs-lookup"><span data-stu-id="7ba13-125">The base class library implements most of this; you just need to provide some information about your filter.</span></span> <span data-ttu-id="7ba13-126">Cette section donne un bref aperçu de ce que vous devez faire.</span><span class="sxs-lookup"><span data-stu-id="7ba13-126">This section gives a brief overview of what to do.</span></span> <span data-ttu-id="7ba13-127">Pour plus d’informations, voir [How to Create a DirectShow Filter dll](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="7ba13-127">For details, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

<span data-ttu-id="7ba13-128">Tout d’abord, écrivez une méthode de classe statique qui retourne une nouvelle instance de votre filtre.</span><span class="sxs-lookup"><span data-stu-id="7ba13-128">First, write a static class method that returns a new instance of your filter.</span></span> <span data-ttu-id="7ba13-129">Vous pouvez nommer cette méthode comme vous le souhaitez, mais la signature doit correspondre à celle illustrée dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="7ba13-129">You can name this method anything you like, but the signature must match the one shown in the following example:</span></span>


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



<span data-ttu-id="7ba13-130">Ensuite, déclarez un tableau global d’instances de la classe [**CFactoryTemplate**](cfactorytemplate.md) , nommé *g \_ Templates*.</span><span class="sxs-lookup"><span data-stu-id="7ba13-130">Next, declare a global array of [**CFactoryTemplate**](cfactorytemplate.md) class instances, named *g\_Templates*.</span></span> <span data-ttu-id="7ba13-131">Chaque classe **CFactoryTemplate** contient des informations de Registre pour un filtre.</span><span class="sxs-lookup"><span data-stu-id="7ba13-131">Each **CFactoryTemplate** class contains registry information for one filter.</span></span> <span data-ttu-id="7ba13-132">Plusieurs filtres peuvent résider dans une seule DLL ; incluez simplement des entrées **CFactoryTemplate** supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="7ba13-132">Several filters can reside in a single DLL; simply include additional **CFactoryTemplate** entries.</span></span> <span data-ttu-id="7ba13-133">Vous pouvez également déclarer d’autres objets COM, tels que des pages de propriétés.</span><span class="sxs-lookup"><span data-stu-id="7ba13-133">You can also declare other COM objects, such as property pages.</span></span>


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



<span data-ttu-id="7ba13-134">Définissez un entier global nommé *g \_ cTemplates* dont la valeur est égale à la longueur du tableau de *\_ modèles g* :</span><span class="sxs-lookup"><span data-stu-id="7ba13-134">Define a global integer named *g\_cTemplates* whose value equals the length of the *g\_Templates* array:</span></span>


```C++
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);  
```



<span data-ttu-id="7ba13-135">Enfin, implémentez les fonctions d’inscription de DLL.</span><span class="sxs-lookup"><span data-stu-id="7ba13-135">Finally, implement the DLL registration functions.</span></span> <span data-ttu-id="7ba13-136">L’exemple suivant illustre l’implémentation minimale pour ces fonctions :</span><span class="sxs-lookup"><span data-stu-id="7ba13-136">The following example shows the minimal implementation for these functions:</span></span>


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



## <a name="filter-registry-entries"></a><span data-ttu-id="7ba13-137">Filtrer les entrées de Registre</span><span class="sxs-lookup"><span data-stu-id="7ba13-137">Filter Registry Entries</span></span>

<span data-ttu-id="7ba13-138">Les exemples précédents montrent comment inscrire le CLSID d’un filtre pour COM.</span><span class="sxs-lookup"><span data-stu-id="7ba13-138">The previous examples show how to register a filter's CLSID for COM.</span></span> <span data-ttu-id="7ba13-139">Pour de nombreux filtres, cela suffit.</span><span class="sxs-lookup"><span data-stu-id="7ba13-139">For many filters, this is sufficient.</span></span> <span data-ttu-id="7ba13-140">Le client est alors censé créer le filtre à l’aide de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) et l’ajouter au graphique de filtre en appelant [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter).</span><span class="sxs-lookup"><span data-stu-id="7ba13-140">The client is then expected to create the filter using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) and add it to the filter graph by calling [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter).</span></span> <span data-ttu-id="7ba13-141">Toutefois, dans certains cas, vous souhaiterez peut-être fournir des informations supplémentaires sur le filtre dans le registre.</span><span class="sxs-lookup"><span data-stu-id="7ba13-141">In some cases, however, you might want to provide additional information about the filter in the registry.</span></span> <span data-ttu-id="7ba13-142">Ces informations effectuent les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7ba13-142">This information does the following:</span></span>

-   <span data-ttu-id="7ba13-143">Permet aux clients de découvrir le filtre à l’aide du [Mappeur de filtre](filter-mapper.md) ou de l' [énumérateur du périphérique système](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="7ba13-143">Enables clients to discover the filter using the [Filter Mapper](filter-mapper.md) or the [System Device Enumerator](system-device-enumerator.md).</span></span>
-   <span data-ttu-id="7ba13-144">Permet au gestionnaire de graphique de filtre de découvrir le filtre pendant la génération automatique de graphiques.</span><span class="sxs-lookup"><span data-stu-id="7ba13-144">Enables the Filter Graph Manager to discover the filter during automatic graph building.</span></span>

<span data-ttu-id="7ba13-145">L’exemple suivant enregistre le filtre d’encodeur RLE dans la catégorie de compresseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="7ba13-145">The following example registers the RLE encoder filter in the video compressor category.</span></span> <span data-ttu-id="7ba13-146">Pour plus d’informations, consultez [comment inscrire des filtres DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="7ba13-146">For details, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="7ba13-147">Veillez à lire la section [instructions pour l’inscription des filtres](guidelines-for-registering-filters.md), qui décrit les pratiques recommandées pour l’inscription de filtres.</span><span class="sxs-lookup"><span data-stu-id="7ba13-147">Be sure to read the section [Guidelines for Registering Filters](guidelines-for-registering-filters.md), which describes the recommended practices for filter registration.</span></span>


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



<span data-ttu-id="7ba13-148">En outre, les filtres n’ont pas besoin d’être empaquetés dans des dll.</span><span class="sxs-lookup"><span data-stu-id="7ba13-148">Also, filters do not have to be packaged inside DLLs.</span></span> <span data-ttu-id="7ba13-149">Dans certains cas, vous pouvez écrire un filtre spécialisé conçu uniquement pour une application spécifique.</span><span class="sxs-lookup"><span data-stu-id="7ba13-149">In some cases, you might write a specialized filter that is designed only for a specific application.</span></span> <span data-ttu-id="7ba13-150">Dans ce cas, vous pouvez compiler la classe de filtre directement dans votre application et la créer avec l' `new` opérateur, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="7ba13-150">In that case, you can compile the filter class directly in your application, and create it with the `new` operator, as shown in the following example:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7ba13-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7ba13-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ba13-152">Connexion intelligente</span><span class="sxs-lookup"><span data-stu-id="7ba13-152">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> <dt>

[<span data-ttu-id="7ba13-153">Écriture de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="7ba13-153">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="7ba13-154">Écriture de filtres de transformation</span><span class="sxs-lookup"><span data-stu-id="7ba13-154">Writing Transform Filters</span></span>](writing-transform-filters.md)
</dt> </dl>

 

 
