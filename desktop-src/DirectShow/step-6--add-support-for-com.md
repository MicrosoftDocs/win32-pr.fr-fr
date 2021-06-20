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
# <a name="step-6-add-support-for-com"></a>Étape 6. Ajouter la prise en charge de COM

Il s’agit de l’étape 6 du didacticiel [écriture de filtres de transformation](writing-transform-filters.md).

La dernière étape consiste à ajouter la prise en charge de COM.

## <a name="reference-counting"></a>Décompte de références

Vous n’avez pas à implémenter [**IUnknown :: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) ou [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Toutes les classes de filtre et de code confidentiel dérivent de [**CUnknown**](cunknown.md), qui gère le décompte de références.

## <a name="queryinterface"></a>QueryInterface

Toutes les classes de filtre et de code confidentiel implémentent [**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour toutes les interfaces COM qu’elles héritent. Par exemple, [**CTransformFilter**](ctransformfilter.md) hérite de [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (via [**CBaseFilter**](cbasefilter.md)). Si votre filtre n’expose pas d’interfaces supplémentaires, vous n’avez rien à faire d’autre.

Pour exposer des interfaces supplémentaires, substituez la méthode [**CUnknown :: NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) . Par exemple, supposons que votre filtre implémente une interface personnalisée nommée IMyCustomInterface. Pour exposer cette interface aux clients, procédez comme suit :

-   Dérivez votre classe de filtre à partir de cette interface.
-   Placez la macro [**Declare \_ IUnknown**](declare-iunknown.md) dans la section Déclaration publique.
-   Substituez [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) pour vérifier l’IID de votre interface et retourner un pointeur vers votre filtre.

Le code suivant illustre ces étapes :


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



Pour plus d’informations, consultez [comment implémenter IUnknown](how-to-implement-iunknown.md).

## <a name="object-creation"></a>Création d’objets

Si vous envisagez de créer un package de votre filtre dans une DLL et de le mettre à la disposition d’autres clients, vous devez prendre en charge [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) et d’autres fonctions com associées. La bibliothèque de classes de base implémente la plupart de ces. il vous suffit de fournir des informations sur votre filtre. Cette section donne un bref aperçu de ce que vous devez faire. Pour plus d’informations, voir [How to Create a DirectShow Filter dll](how-to-create-a-dll.md).

Tout d’abord, écrivez une méthode de classe statique qui retourne une nouvelle instance de votre filtre. Vous pouvez nommer cette méthode comme vous le souhaitez, mais la signature doit correspondre à celle illustrée dans l’exemple suivant :


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



Ensuite, déclarez un tableau global d’instances de la classe [**CFactoryTemplate**](cfactorytemplate.md) , nommé *g \_ Templates*. Chaque classe **CFactoryTemplate** contient des informations de Registre pour un filtre. Plusieurs filtres peuvent résider dans une seule DLL ; incluez simplement des entrées **CFactoryTemplate** supplémentaires. Vous pouvez également déclarer d’autres objets COM, tels que des pages de propriétés.


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



Définissez un entier global nommé *g \_ cTemplates* dont la valeur est égale à la longueur du tableau de *\_ modèles g* :


```C++
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);  
```



Enfin, implémentez les fonctions d’inscription de DLL. L’exemple suivant illustre l’implémentation minimale pour ces fonctions :


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



## <a name="filter-registry-entries"></a>Filtrer les entrées de Registre

Les exemples précédents montrent comment inscrire le CLSID d’un filtre pour COM. Pour de nombreux filtres, cela suffit. Le client est alors censé créer le filtre à l’aide de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) et l’ajouter au graphique de filtre en appelant [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter). Toutefois, dans certains cas, vous souhaiterez peut-être fournir des informations supplémentaires sur le filtre dans le registre. Ces informations effectuent les opérations suivantes :

-   Permet aux clients de découvrir le filtre à l’aide du [Mappeur de filtre](filter-mapper.md) ou de l' [énumérateur du périphérique système](system-device-enumerator.md).
-   Permet au gestionnaire de graphique de filtre de découvrir le filtre pendant la génération automatique de graphiques.

L’exemple suivant enregistre le filtre d’encodeur RLE dans la catégorie de compresseur vidéo. Pour plus d’informations, consultez [comment inscrire des filtres DirectShow](how-to-register-directshow-filters.md). Veillez à lire la section [instructions pour l’inscription des filtres](guidelines-for-registering-filters.md), qui décrit les pratiques recommandées pour l’inscription de filtres.


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



En outre, les filtres n’ont pas besoin d’être empaquetés dans des dll. Dans certains cas, vous pouvez écrire un filtre spécialisé conçu uniquement pour une application spécifique. Dans ce cas, vous pouvez compiler la classe de filtre directement dans votre application et la créer avec l' `new` opérateur, comme illustré dans l’exemple suivant :


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Connexion intelligente](intelligent-connect.md)
</dt> <dt>

[Écriture de filtres DirectShow](writing-directshow-filters.md)
</dt> <dt>

[Écriture de filtres de transformation](writing-transform-filters.md)
</dt> </dl>

 

 
