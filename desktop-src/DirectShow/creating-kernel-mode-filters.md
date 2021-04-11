---
description: Création de filtres de Kernel-Mode
ms.assetid: cbc86a5d-c53a-44a0-aa81-5c41527a8f67
title: Création de filtres de Kernel-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c915a08312e33f0e35245325fd8bce7e55e486c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109778"
---
# <a name="creating-kernel-mode-filters"></a>Création de filtres de Kernel-Mode

Certains filtres en mode noyau ne peuvent pas être créés via **CoCreateInstance** et n’ont donc pas de CLSID. Ces filtres incluent le [convertisseur tee/Sink-to-Sink](tee-sink-to-sink-converter.md), le filtre de [décodeur CC](cc-decoder-filter.md) et le filtre de [codec WST](wst-codec-filter.md) . Pour créer l’un de ces filtres, utilisez l’objet [énumérateur de périphérique système](system-device-enumerator.md) et recherchez le nom du filtre.

1.  Créez l’énumérateur du périphérique système.
2.  Appelez la méthode [**ICreateDevEnum :: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) avec le CLSID de la catégorie de filtre pour ce filtre. Cette méthode crée un énumérateur pour la catégorie de filtre. (Un *énumérateur* est simplement un objet qui retourne une liste d’autres objets, à l’aide d’une interface com définie.) L’énumérateur retourne les pointeurs **IMoniker** , qui représentent les filtres de cette catégorie.
3.  Pour chaque moniker, appelez **IMoniker :: BindToStorage** pour obtenir une interface **IPropertyBag** .
4.  Appelez **IPropertyBag :: Read** pour obtenir le nom du filtre.
5.  Si le nom correspond, appelez **IMoniker :: BindToObject** pour créer le filtre.

Le code suivant illustre une fonction qui effectue les étapes suivantes :


```C++
HRESULT CreateKernelFilter(
    const GUID &guidCategory,  // Filter category.
    LPCOLESTR szName,          // The name of the filter.
    IBaseFilter **ppFilter     // Receives a pointer to the filter.
)
{
    HRESULT hr;
    ICreateDevEnum *pDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    if (!szName || !ppFilter) 
    {
        return E_POINTER;
    }

    // Create the system device enumerator.
    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC,
        IID_ICreateDevEnum, (void**)&pDevEnum);
    if (FAILED(hr))
    {
        return hr;
    }

    // Create a class enumerator for the specified category.
    hr = pDevEnum->CreateClassEnumerator(guidCategory, &pEnum, 0);
    pDevEnum->Release();
    if (hr != S_OK) // S_FALSE means the category is empty.
    {
        return E_FAIL;
    }

    // Enumerate devices within this category.
    bool bFound = false;
    IMoniker *pMoniker;
    while (!bFound && (S_OK == pEnum->Next(1, &pMoniker, 0)))
    {
        IPropertyBag *pBag = NULL;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, (void **)&pBag);
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        // Check the friendly name.
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(L"FriendlyName", &var, NULL);
        if (SUCCEEDED(hr) && (lstrcmpiW(var.bstrVal, szName) == 0))
        {
            // This is the right filter.
            hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter,
                (void**)ppFilter);
            bFound = true;
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnum->Release();
    return (bFound ? hr : E_FAIL);
}
```



L’exemple de code suivant utilise cette fonction pour créer le filtre de décodeur CC et l’ajouter au graphique de filtre :


```C++
IBaseFilter *pCC = NULL;
hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
    OLESTR("CC Decoder"), &pCC);
if (SUCCEEDED(hr))
{
    hr = pGraph->AddFilter(pCC, L"CC Decoder");
    pCC->Release();
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rubriques avancées sur la capture](advanced-capture-topics.md)
</dt> <dt>

[Utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md)
</dt> </dl>

 

 



