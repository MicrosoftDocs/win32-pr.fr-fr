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
# <a name="creating-kernel-mode-filters"></a><span data-ttu-id="0804b-103">Création de filtres de Kernel-Mode</span><span class="sxs-lookup"><span data-stu-id="0804b-103">Creating Kernel-Mode Filters</span></span>

<span data-ttu-id="0804b-104">Certains filtres en mode noyau ne peuvent pas être créés via **CoCreateInstance** et n’ont donc pas de CLSID.</span><span class="sxs-lookup"><span data-stu-id="0804b-104">Certain kernel-mode filters cannot be created through **CoCreateInstance**, and thus do not have CLSIDs.</span></span> <span data-ttu-id="0804b-105">Ces filtres incluent le [convertisseur tee/Sink-to-Sink](tee-sink-to-sink-converter.md), le filtre de [décodeur CC](cc-decoder-filter.md) et le filtre de [codec WST](wst-codec-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="0804b-105">These filters include the [Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md), the [CC Decoder](cc-decoder-filter.md) filter, and the [WST Codec](wst-codec-filter.md) filter.</span></span> <span data-ttu-id="0804b-106">Pour créer l’un de ces filtres, utilisez l’objet [énumérateur de périphérique système](system-device-enumerator.md) et recherchez le nom du filtre.</span><span class="sxs-lookup"><span data-stu-id="0804b-106">To create one of these filters, use the [System Device Enumerator](system-device-enumerator.md) object and search by the filter's name.</span></span>

1.  <span data-ttu-id="0804b-107">Créez l’énumérateur du périphérique système.</span><span class="sxs-lookup"><span data-stu-id="0804b-107">Create the System Device Enumerator.</span></span>
2.  <span data-ttu-id="0804b-108">Appelez la méthode [**ICreateDevEnum :: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) avec le CLSID de la catégorie de filtre pour ce filtre.</span><span class="sxs-lookup"><span data-stu-id="0804b-108">Call the [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) method with the CLSID of the filter category for that filter.</span></span> <span data-ttu-id="0804b-109">Cette méthode crée un énumérateur pour la catégorie de filtre.</span><span class="sxs-lookup"><span data-stu-id="0804b-109">This method creates an enumerator for the filter category.</span></span> <span data-ttu-id="0804b-110">(Un *énumérateur* est simplement un objet qui retourne une liste d’autres objets, à l’aide d’une interface com définie.) L’énumérateur retourne les pointeurs **IMoniker** , qui représentent les filtres de cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="0804b-110">(An *enumerator* is simply an object that returns a list of other objects, using a defined COM interface.) The enumerator returns **IMoniker** pointers, which represent the filters in that category.</span></span>
3.  <span data-ttu-id="0804b-111">Pour chaque moniker, appelez **IMoniker :: BindToStorage** pour obtenir une interface **IPropertyBag** .</span><span class="sxs-lookup"><span data-stu-id="0804b-111">For each moniker, call **IMoniker::BindToStorage** to get an **IPropertyBag** interface.</span></span>
4.  <span data-ttu-id="0804b-112">Appelez **IPropertyBag :: Read** pour obtenir le nom du filtre.</span><span class="sxs-lookup"><span data-stu-id="0804b-112">Call **IPropertyBag::Read** to get the name of the filter.</span></span>
5.  <span data-ttu-id="0804b-113">Si le nom correspond, appelez **IMoniker :: BindToObject** pour créer le filtre.</span><span class="sxs-lookup"><span data-stu-id="0804b-113">If the name matches, call **IMoniker::BindToObject** to create the filter.</span></span>

<span data-ttu-id="0804b-114">Le code suivant illustre une fonction qui effectue les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0804b-114">The following code shows a function that performs these steps:</span></span>


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



<span data-ttu-id="0804b-115">L’exemple de code suivant utilise cette fonction pour créer le filtre de décodeur CC et l’ajouter au graphique de filtre :</span><span class="sxs-lookup"><span data-stu-id="0804b-115">The following code example uses this function to create the CC Decoder filter and add it to the filter graph:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0804b-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0804b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0804b-117">Rubriques avancées sur la capture</span><span class="sxs-lookup"><span data-stu-id="0804b-117">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="0804b-118">Utilisation de l’énumérateur de périphérique système</span><span class="sxs-lookup"><span data-stu-id="0804b-118">Using the System Device Enumerator</span></span>](using-the-system-device-enumerator.md)
</dt> </dl>

 

 



