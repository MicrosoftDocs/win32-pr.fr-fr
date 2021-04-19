---
description: Énumération des effets et des transitions
ms.assetid: 364b7bfb-5d6e-4ca6-b0c8-7a0180c3f61a
title: Énumération des effets et des transitions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e533f36501ac8da6015cc31eea6c2c111bf6a208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516151"
---
# <a name="enumerating-effects-and-transitions"></a><span data-ttu-id="8407e-103">Énumération des effets et des transitions</span><span class="sxs-lookup"><span data-stu-id="8407e-103">Enumerating Effects and Transitions</span></span>

<span data-ttu-id="8407e-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="8407e-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="8407e-105">DirectShow fournit un objet [énumérateur de périphérique système](system-device-enumerator.md) pour l’énumération des appareils.</span><span class="sxs-lookup"><span data-stu-id="8407e-105">DirectShow provides a [System Device Enumerator](system-device-enumerator.md) object for enumerating devices.</span></span> <span data-ttu-id="8407e-106">Vous pouvez l’utiliser pour récupérer les monikers des effets ou des transitions installés sur le système de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8407e-106">You can use it to retrieve monikers for effects or transitions installed on the user's system.</span></span>

<span data-ttu-id="8407e-107">L’énumérateur de périphérique système expose l’interface [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) .</span><span class="sxs-lookup"><span data-stu-id="8407e-107">The system device enumerator exposes the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface.</span></span> <span data-ttu-id="8407e-108">Elle retourne les énumérateurs de catégorie pour les catégories d’appareils spécifiées.</span><span class="sxs-lookup"><span data-stu-id="8407e-108">It returns category enumerators for specified device categories.</span></span> <span data-ttu-id="8407e-109">Un énumérateur de catégorie, à son tour, expose l’interface [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) et retourne des monikers pour chaque appareil de la catégorie.</span><span class="sxs-lookup"><span data-stu-id="8407e-109">A category enumerator, in turn, exposes the [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) interface and returns monikers for each device in the category.</span></span> <span data-ttu-id="8407e-110">Pour une présentation détaillée de l’utilisation de **ICreateDevEnum**, consultez [énumération d’appareils et de filtres](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="8407e-110">For a detailed discussion of using **ICreateDevEnum**, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span> <span data-ttu-id="8407e-111">Voici un bref résumé, spécifique aux services de modification DirectShow.</span><span class="sxs-lookup"><span data-stu-id="8407e-111">The following is a brief summary, specific to DirectShow Editing Services.</span></span>

<span data-ttu-id="8407e-112">Pour énumérer des effets ou des transitions, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="8407e-112">To enumerate effects or transitions, perform the following steps.</span></span>

1.  <span data-ttu-id="8407e-113">Créez une instance de l’énumérateur du périphérique système.</span><span class="sxs-lookup"><span data-stu-id="8407e-113">Create an instance of the system device enumerator.</span></span>
2.  <span data-ttu-id="8407e-114">Appelez la méthode [**ICreateDevEnum :: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) pour récupérer un énumérateur de catégorie.</span><span class="sxs-lookup"><span data-stu-id="8407e-114">Call the [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) method to retrieve a category enumerator.</span></span> <span data-ttu-id="8407e-115">Les catégories sont définies par des identificateurs de classe (CLSID).</span><span class="sxs-lookup"><span data-stu-id="8407e-115">Categories are defined by class identifiers (CLSIDs).</span></span> <span data-ttu-id="8407e-116">Utilisez CLSID \_ VideoEffects1Category pour les effets ou les \_ VideoEffects2Category CLSID pour les transitions.</span><span class="sxs-lookup"><span data-stu-id="8407e-116">Use CLSID\_VideoEffects1Category for effects or CLSID\_VideoEffects2Category for transitions.</span></span>
3.  <span data-ttu-id="8407e-117">Appelez **IEnumMoniker :: Next** pour récupérer chaque moniker dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="8407e-117">Call **IEnumMoniker::Next** to retrieve each moniker in the enumeration.</span></span>
4.  <span data-ttu-id="8407e-118">Pour chaque moniker, appelez **IMoniker :: BindToStorage** pour récupérer son conteneur de propriétés associé.</span><span class="sxs-lookup"><span data-stu-id="8407e-118">For each moniker, call **IMoniker::BindToStorage** to retrieve its associated property bag.</span></span>

<span data-ttu-id="8407e-119">Le conteneur de propriétés contient le nom convivial et l’identificateur global unique (GUID) de l’effet ou de la transition.</span><span class="sxs-lookup"><span data-stu-id="8407e-119">The property bag contains the friendly name and the globally unique identifier (GUID) for the effect or transition.</span></span> <span data-ttu-id="8407e-120">Une application peut afficher une liste de noms conviviaux, puis obtenir le GUID correspondant.</span><span class="sxs-lookup"><span data-stu-id="8407e-120">An application can display a list of friendly names and then obtain the corresponding GUID.</span></span>

<span data-ttu-id="8407e-121">L’exemple de code suivant illustre ces étapes.</span><span class="sxs-lookup"><span data-stu-id="8407e-121">The following code example illustrates these steps.</span></span>


```C++
ICreateDevEnum *pCreateDevEnum = NULL;
IEnumMoniker *pEnumMoniker = NULL;

// Create the System Device Enumerator.
HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
    CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, (void**)&pCreateDevEnum);
if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

// Create an enumerator for the video effects category.
hr = pCreateDevEnum->CreateClassEnumerator(
    CLSID_VideoEffects1Category,  // Video effects category. 
    &pEnumMoniker, 0);               

// Note: Use CLSID_VideoEffects2Category for video transitions.

if (hr == S_OK)  // S_FALSE means the category is empty.
{
    // Enumerate each video effect.
    IMoniker *pMoniker;
    while (S_OK == pEnumMoniker->Next(1, &pMoniker, NULL))
    {
        IPropertyBag *pBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pBag);
        if(FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(OLESTR("FriendlyName"), &var, NULL);
        if (SUCCEEDED(hr))
        {
            if ( ... )  // Check if var.bstrVal is the name you want.
            {
                VARIANT var2;
                GUID guid;
                var2.vt = VT_BSTR;
                pBag->Read(OLESTR("guid"), &var2, NULL);
                CLSIDFromString(var2.bstrVal, &guid);
                VariantClear(&var2);
                // GUID is now the CLSID for the effect.
            }
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnumMoniker->Release();
}
pCreateDevEnum->Release();
```



## <a name="related-topics"></a><span data-ttu-id="8407e-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8407e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8407e-123">Utilisation des effets et des transitions</span><span class="sxs-lookup"><span data-stu-id="8407e-123">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
