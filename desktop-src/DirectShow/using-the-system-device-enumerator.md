---
description: Utilisation de l’énumérateur de périphérique système
ms.assetid: 70db139c-2c5b-4574-bec3-dfe758b16715
title: Utilisation de l’énumérateur de périphérique système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f8f66cb64e9f7bb51d6b0716b9fa23cf531435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104561036"
---
# <a name="using-the-system-device-enumerator"></a><span data-ttu-id="3df3e-103">Utilisation de l’énumérateur de périphérique système</span><span class="sxs-lookup"><span data-stu-id="3df3e-103">Using the System Device Enumerator</span></span>

<span data-ttu-id="3df3e-104">L’énumérateur de périphérique système offre un moyen uniforme d’énumérer, par catégorie, les filtres inscrits sur le système d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3df3e-104">The System Device Enumerator provides a uniform way to enumerate, by category, the filters registered on a user's system.</span></span> <span data-ttu-id="3df3e-105">En outre, il fait la distinction entre les différents périphériques matériels, même si le même filtre les prend en charge.</span><span class="sxs-lookup"><span data-stu-id="3df3e-105">Moreover, it differentiates between individual hardware devices, even if the same filter supports them.</span></span> <span data-ttu-id="3df3e-106">Cela s’avère particulièrement utile pour les appareils qui utilisent le Windows Driver Model (WDM) et le filtre KSProxy.</span><span class="sxs-lookup"><span data-stu-id="3df3e-106">This is particularly useful for devices that use the Windows Driver Model (WDM) and the KSProxy filter.</span></span> <span data-ttu-id="3df3e-107">Par exemple, l’utilisateur peut avoir plusieurs périphériques de capture vidéo WDM, tous pris en charge par le même filtre.</span><span class="sxs-lookup"><span data-stu-id="3df3e-107">For example, the user might have several WDM video capture devices, all supported by the same filter.</span></span> <span data-ttu-id="3df3e-108">L’énumérateur de périphérique système les traite comme des instances d’appareil distinctes.</span><span class="sxs-lookup"><span data-stu-id="3df3e-108">The System Device Enumerator treats them as separate device instances.</span></span>

<span data-ttu-id="3df3e-109">L’énumérateur de périphérique système fonctionne en créant un énumérateur pour une catégorie spécifique, telle que la capture audio ou la compression vidéo.</span><span class="sxs-lookup"><span data-stu-id="3df3e-109">The System Device Enumerator works by creating an enumerator for a specific category, such as audio capture or video compression.</span></span> <span data-ttu-id="3df3e-110">L’énumérateur Category retourne un moniker unique pour chaque appareil de la catégorie.</span><span class="sxs-lookup"><span data-stu-id="3df3e-110">The category enumerator returns a unique moniker for each device in the category.</span></span> <span data-ttu-id="3df3e-111">L’énumérateur de catégorie comprend automatiquement tous les appareils Plug-and-Play pertinents dans la catégorie.</span><span class="sxs-lookup"><span data-stu-id="3df3e-111">The category enumerator automatically includes any relevant Plug and Play devices in the category.</span></span> <span data-ttu-id="3df3e-112">Pour obtenir la liste des catégories, consultez [Filtrer les catégories](filter-categories.md).</span><span class="sxs-lookup"><span data-stu-id="3df3e-112">For a list of categories, see [Filter Categories](filter-categories.md).</span></span>

<span data-ttu-id="3df3e-113">Pour utiliser l’énumérateur de périphérique système, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="3df3e-113">To use the System Device Enumerator, do the following:</span></span>

1.  <span data-ttu-id="3df3e-114">Créez l’énumérateur de périphérique système en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="3df3e-114">Create the system device enumerator by calling **CoCreateInstance**.</span></span> <span data-ttu-id="3df3e-115">L’identificateur de classe (CLSID) est CLSID \_ SystemDeviceEnum.</span><span class="sxs-lookup"><span data-stu-id="3df3e-115">The class identifier (CLSID) is CLSID\_SystemDeviceEnum.</span></span>
2.  <span data-ttu-id="3df3e-116">Obtenez un énumérateur de catégorie en appelant [**ICreateDevEnum :: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) avec le CLSID de la catégorie souhaitée.</span><span class="sxs-lookup"><span data-stu-id="3df3e-116">Obtain a category enumerator by calling [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) with the CLSID of the desired category.</span></span> <span data-ttu-id="3df3e-117">Cette méthode retourne un pointeur d’interface **IEnumMoniker** .</span><span class="sxs-lookup"><span data-stu-id="3df3e-117">This method returns an **IEnumMoniker** interface pointer.</span></span> <span data-ttu-id="3df3e-118">Si la catégorie est vide (ou n’existe pas), la méthode retourne S \_ false au lieu d’un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="3df3e-118">If the category is empty (or does not exist), the method returns S\_FALSE rather than an error code.</span></span> <span data-ttu-id="3df3e-119">Si c’est le cas, le pointeur **IEnumMoniker** retourné est **null** et son déréférencement entraîne une exception.</span><span class="sxs-lookup"><span data-stu-id="3df3e-119">If so, the returned **IEnumMoniker** pointer is **NULL** and dereferencing it will cause an exception.</span></span> <span data-ttu-id="3df3e-120">Par conséquent, testez explicitement les \_ OK quand vous appelez **CreateClassEnumerator**, au lieu d’appeler la macro **Succeeded** habituelle.</span><span class="sxs-lookup"><span data-stu-id="3df3e-120">Therefore, explicitly test for S\_OK when you call **CreateClassEnumerator**, instead of calling the usual **SUCCEEDED** macro.</span></span>
3.  <span data-ttu-id="3df3e-121">Utilisez la méthode **IEnumMoniker :: Next** pour énumérer chaque moniker.</span><span class="sxs-lookup"><span data-stu-id="3df3e-121">Use the **IEnumMoniker::Next** method to enumerate each moniker.</span></span> <span data-ttu-id="3df3e-122">Cette méthode retourne un pointeur d’interface **IMoniker** .</span><span class="sxs-lookup"><span data-stu-id="3df3e-122">This method returns an **IMoniker** interface pointer.</span></span> <span data-ttu-id="3df3e-123">Lorsque la méthode **suivante** atteint la fin de l’énumération, elle retourne également la \_ valeur false. par conséquent, vérifiez de nouveau si la valeur est \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3df3e-123">When the **Next** method reaches the end of the enumeration, it also returns S\_FALSE, so again check for S\_OK.</span></span>
4.  <span data-ttu-id="3df3e-124">Pour récupérer le nom convivial de l’appareil (par exemple, pour l’afficher dans l’interface utilisateur), appelez la méthode **IMoniker :: BindToStorage** .</span><span class="sxs-lookup"><span data-stu-id="3df3e-124">To retrieve the friendly name of the device (for example, to display in the user interface), call the **IMoniker::BindToStorage** method.</span></span>
5.  <span data-ttu-id="3df3e-125">Pour créer et initialiser le filtre DirectShow qui gère l’appareil, appelez **IMoniker :: BindToObject** sur le moniker.</span><span class="sxs-lookup"><span data-stu-id="3df3e-125">To create and initialize the DirectShow filter that manages the device, call **IMoniker::BindToObject** on the moniker.</span></span> <span data-ttu-id="3df3e-126">Appelez [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) pour ajouter le filtre au graphique.</span><span class="sxs-lookup"><span data-stu-id="3df3e-126">Call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the graph.</span></span>

<span data-ttu-id="3df3e-127">Le diagramme suivant illustre ce processus.</span><span class="sxs-lookup"><span data-stu-id="3df3e-127">The following diagram illustrates this process.</span></span>

![énumération des appareils](images/sysdevenum.png)

<span data-ttu-id="3df3e-129">L’exemple suivant montre comment énumérer les compressions vidéo installées sur le système de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3df3e-129">The following example shows how to enumerate the video compressors installed on the user's system.</span></span> <span data-ttu-id="3df3e-130">Par souci de concision, l’exemple effectue une vérification des erreurs minimale.</span><span class="sxs-lookup"><span data-stu-id="3df3e-130">For brevity, the example performs minimal error checking.</span></span>


```C++
// Create the System Device Enumerator.
HRESULT hr;
ICreateDevEnum *pSysDevEnum = NULL;
hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC_SERVER,
    IID_ICreateDevEnum, (void **)&pSysDevEnum);
if (FAILED(hr))
{
    return hr;
}

// Obtain a class enumerator for the video compressor category.
IEnumMoniker *pEnumCat = NULL;
hr = pSysDevEnum->CreateClassEnumerator(CLSID_VideoCompressorCategory, &pEnumCat, 0);

if (hr == S_OK) 
{
    // Enumerate the monikers.
    IMoniker *pMoniker = NULL;
    ULONG cFetched;
    while(pEnumCat->Next(1, &pMoniker, &cFetched) == S_OK)
    {
        IPropertyBag *pPropBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pPropBag);
        if (SUCCEEDED(hr))
        {
            // To retrieve the filter's friendly name, do the following:
            VARIANT varName;
            VariantInit(&varName);
            hr = pPropBag->Read(L"FriendlyName", &varName, 0);
            if (SUCCEEDED(hr))
            {
                // Display the name in your UI somehow.
            }
            VariantClear(&varName);

            // To create an instance of the filter, do the following:
            IBaseFilter *pFilter;
            hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter,
                (void**)&pFilter);
            // Now add the filter to the graph. 
            //Remember to release pFilter later.
            pPropBag->Release();
        }
        pMoniker->Release();
    }
    pEnumCat->Release();
}
pSysDevEnum->Release();
```



<span data-ttu-id="3df3e-131">**Monikers de périphérique**</span><span class="sxs-lookup"><span data-stu-id="3df3e-131">**Device Monikers**</span></span>

<span data-ttu-id="3df3e-132">Pour les monikers de périphérique, vous pouvez passer le moniker à la méthode [**IFilterGraph2 :: AddSourceFilterForMoniker**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) pour créer un filtre de capture pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3df3e-132">For device monikers, you can pass the moniker to the [**IFilterGraph2::AddSourceFilterForMoniker**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) method to create a capture filter for the device.</span></span> <span data-ttu-id="3df3e-133">Pour obtenir un exemple de code, consultez la documentation de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3df3e-133">For example code, see the documentation for that method.</span></span>

<span data-ttu-id="3df3e-134">La méthode **IMoniker :: GetDisplayName** retourne le nom complet du moniker.</span><span class="sxs-lookup"><span data-stu-id="3df3e-134">The **IMoniker::GetDisplayName** method returns the display name of the moniker.</span></span> <span data-ttu-id="3df3e-135">Bien que le nom d’affichage soit lisible, vous ne l’affichez généralement pas pour un utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="3df3e-135">Although the display name is readable, you would not typically display it to an end-user.</span></span> <span data-ttu-id="3df3e-136">À la place, récupérez le nom convivial à partir du conteneur des propriétés, comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="3df3e-136">Get the friendly name from the property bag instead, as described previously.</span></span>

<span data-ttu-id="3df3e-137">La méthode **IMoniker ::P arsedisplayname** ou la fonction **MkParseDisplayName** peut être utilisée pour créer un moniker de périphérique par défaut pour une catégorie de filtre donnée.</span><span class="sxs-lookup"><span data-stu-id="3df3e-137">The **IMoniker::ParseDisplayName** method or the **MkParseDisplayName** function can be used to create a default device moniker for a given filter category.</span></span> <span data-ttu-id="3df3e-138">Utilisez un nom complet au format `@device:*:{category-clsid}` , où `category-clsid` est la représentation sous forme de chaîne du GUID de la catégorie.</span><span class="sxs-lookup"><span data-stu-id="3df3e-138">Use a display name with the form `@device:*:{category-clsid}`, where `category-clsid` is the string representation of the category GUID.</span></span> <span data-ttu-id="3df3e-139">Le moniker par défaut est le premier moniker retourné par l’énumérateur d’appareil pour cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="3df3e-139">The default moniker is the first moniker returned by the device enumerator for that category.</span></span>

 

 



