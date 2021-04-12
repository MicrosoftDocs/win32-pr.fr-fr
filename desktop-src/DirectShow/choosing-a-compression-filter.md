---
description: Choix d’un filtre de compression
ms.assetid: 9a2c3c48-771e-44db-a042-3db0fd9a6c76
title: Choix d’un filtre de compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64ebebf41c35ed6aed9ab47d853c03ba720a31
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109842"
---
# <a name="choosing-a-compression-filter"></a><span data-ttu-id="47afe-103">Choix d’un filtre de compression</span><span class="sxs-lookup"><span data-stu-id="47afe-103">Choosing a Compression Filter</span></span>

<span data-ttu-id="47afe-104">Plusieurs types de composants logiciels peuvent effectuer une compression vidéo ou audio, par exemple :</span><span class="sxs-lookup"><span data-stu-id="47afe-104">Several types of software components can perform video or audio compression, such as:</span></span>

-   <span data-ttu-id="47afe-105">Filtres DirectShow natifs</span><span class="sxs-lookup"><span data-stu-id="47afe-105">Native DirectShow filters</span></span>
-   <span data-ttu-id="47afe-106">Codecs du gestionnaire de compression vidéo (VCM)</span><span class="sxs-lookup"><span data-stu-id="47afe-106">Video Compression Manager (VCM) codecs</span></span>
-   <span data-ttu-id="47afe-107">Codecs de gestionnaire de compression audio (ACM)</span><span class="sxs-lookup"><span data-stu-id="47afe-107">Audio Compression Manager (ACM) codecs</span></span>
-   <span data-ttu-id="47afe-108">Objets DMOs (DirectX Media Objects)</span><span class="sxs-lookup"><span data-stu-id="47afe-108">DirectX Media Objects (DMOs)</span></span>

<span data-ttu-id="47afe-109">Dans DirectShow, les codecs VCM sont encapsulés par le [filtre de compresseur AVI](avi-compressor-filter.md), et les codecs ACM sont encapsulés par le [filtre de wrappers ACM](acm-wrapper-filter.md).</span><span class="sxs-lookup"><span data-stu-id="47afe-109">In DirectShow, VCM codecs are wrapped by the [AVI Compressor Filter](avi-compressor-filter.md), and ACM codecs are wrapped by the [ACM Wrapper Filter](acm-wrapper-filter.md).</span></span> <span data-ttu-id="47afe-110">Les DMOs sont encapsulés par le [filtre de wrappers DMO](dmo-wrapper-filter.md).</span><span class="sxs-lookup"><span data-stu-id="47afe-110">DMOs are wrapped by the [DMO Wrapper Filter](dmo-wrapper-filter.md).</span></span> <span data-ttu-id="47afe-111">L’énumérateur de périphérique système fournit une méthode cohérente pour énumérer et créer l’un de ces types de compresseur, sans vous soucier du modèle sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="47afe-111">The system device enumerator provides a consistent way to enumerate and create any of these compressor types, without worrying about the underlying model.</span></span>

<span data-ttu-id="47afe-112">Pour plus d’informations sur l’énumérateur de périphérique système, consultez [utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="47afe-112">For details about the system device enumerator, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span> <span data-ttu-id="47afe-113">Brièvement, tous les filtres DirectShow sont classés par catégorie, et chaque catégorie est identifiée par un GUID.</span><span class="sxs-lookup"><span data-stu-id="47afe-113">Briefly, all DirectShow filters are classified by category, and each category is identified by a GUID.</span></span> <span data-ttu-id="47afe-114">Pour les compresseurs vidéo, le GUID de la catégorie est CLSID \_ VideoCompressorCategory.</span><span class="sxs-lookup"><span data-stu-id="47afe-114">For video compressors, the category GUID is CLSID\_VideoCompressorCategory.</span></span> <span data-ttu-id="47afe-115">Pour les compresseurs audio, il s’agit du CLSID \_ AudioCompressorCategory.</span><span class="sxs-lookup"><span data-stu-id="47afe-115">For audio compressors, it is CLSID\_AudioCompressorCategory.</span></span> <span data-ttu-id="47afe-116">Pour énumérer une catégorie particulière, l’énumérateur de périphérique système crée un objet *énumérateur* qui prend en charge l’interface [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) .</span><span class="sxs-lookup"><span data-stu-id="47afe-116">To enumerate a particular category, the system device enumerator creates an *enumerator* object that supports the [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) interface.</span></span> <span data-ttu-id="47afe-117">L’application utilise cette interface pour récupérer des monikers de périphérique, où chaque moniker de périphérique représente une instance d’un filtre DirectShow.</span><span class="sxs-lookup"><span data-stu-id="47afe-117">The application uses this interface to retrieve device monikers, where each device moniker represents an instance of a DirectShow filter.</span></span> <span data-ttu-id="47afe-118">Vous pouvez utiliser le moniker pour créer le filtre, ou pour récupérer le nom convivial de l’appareil sans créer le filtre.</span><span class="sxs-lookup"><span data-stu-id="47afe-118">You can use the moniker to create the filter, or to get the device's friendly name without creating the filter.</span></span>

<span data-ttu-id="47afe-119">Pour énumérer les compresseurs vidéo ou audio disponibles sur le système de l’utilisateur, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="47afe-119">To enumerate the video or audio compressors available on the user's system, do the following:</span></span>

1.  <span data-ttu-id="47afe-120">Appelez [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer l’énumérateur du périphérique système, qui a l’ID de classe CLSID \_ SystemDeviceEnum.</span><span class="sxs-lookup"><span data-stu-id="47afe-120">Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the system device enumerator, which has a class ID of CLSID\_SystemDeviceEnum.</span></span>
2.  <span data-ttu-id="47afe-121">Appelez [**ICreateDevEnum :: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) avec le GUID de catégorie de filtre.</span><span class="sxs-lookup"><span data-stu-id="47afe-121">Call [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) with the filter category GUID.</span></span> <span data-ttu-id="47afe-122">La méthode retourne un pointeur d’interface **IEnumMoniker** .</span><span class="sxs-lookup"><span data-stu-id="47afe-122">The method returns an **IEnumMoniker** interface pointer.</span></span>
3.  <span data-ttu-id="47afe-123">Utilisez la méthode IEnumMoniker :: Next pour énumérer les monikers d’appareil.</span><span class="sxs-lookup"><span data-stu-id="47afe-123">Use the IEnumMoniker::Next method to enumerate the device monikers.</span></span> <span data-ttu-id="47afe-124">Cette méthode retourne une interface [**IMoniker**](/windows/desktop/api/objidl/nn-objidl-imoniker) , qui représente le moniker.</span><span class="sxs-lookup"><span data-stu-id="47afe-124">This method returns an [**IMoniker**](/windows/desktop/api/objidl/nn-objidl-imoniker) interface, which represents the moniker.</span></span>

<span data-ttu-id="47afe-125">Pour obtenir le nom convivial d’un moniker, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="47afe-125">To get the friendly name from a moniker, do the following:</span></span>

1.  <span data-ttu-id="47afe-126">Appelez la méthode **IMoniker :: BindToStorage** .</span><span class="sxs-lookup"><span data-stu-id="47afe-126">Call the **IMoniker::BindToStorage** method.</span></span> <span data-ttu-id="47afe-127">Cette méthode retourne un pointeur d’interface **IPropertyBag** .</span><span class="sxs-lookup"><span data-stu-id="47afe-127">This method returns an **IPropertyBag** interface pointer.</span></span>
2.  <span data-ttu-id="47afe-128">Utilisez la méthode **IPropertyBag :: Read** pour lire la propriété **FriendlyName** .</span><span class="sxs-lookup"><span data-stu-id="47afe-128">Use the **IPropertyBag::Read** method to read the **FriendlyName** property.</span></span>

<span data-ttu-id="47afe-129">En règle générale, une application affiche une liste de compresseurs, afin que l’utilisateur puisse en choisir une.</span><span class="sxs-lookup"><span data-stu-id="47afe-129">Typically, an application would display a list of compressors, so that the user could choose one.</span></span> <span data-ttu-id="47afe-130">Par exemple, le code suivant remplit une zone de liste avec les noms des compressions vidéo disponibles.</span><span class="sxs-lookup"><span data-stu-id="47afe-130">For example, the following code populates a list box with the names of the available video compressors.</span></span>


```C++
void OnInitDialog(HWND hDlg)
{
    HRESULT hr;
    ICreateDevEnum *pSysDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    IMoniker *pMoniker = NULL;

    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, 
        (void**)&pSysDevEnum);
    if (FAILED(hr))
    {
        // Handle the error.
    }    

    hr = pSysDevEnum->CreateClassEnumerator(
             CLSID_VideoCompressorCategory, &pEnum, 0);
    if (hr == S_OK)  // S_FALSE means nothing in this category.
    {
        while (S_OK == pEnum->Next(1, &pMoniker, NULL))
        {
            IPropertyBag *pPropBag = NULL;
            pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
                (void **)&pPropBag);
            VARIANT var;
            VariantInit(&var);
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
            if (SUCCEEDED(hr))
            {
                LRESULT iSel = AddString(GetDlgItem(hDlg, 
                    IDC_CODEC_LIST), var.bstrVal);
            }   
            VariantClear(&var); 
            pPropBag->Release();
            pMoniker->Release();
        }
    }

    SendDlgItemMessage(hDlg, IDC_CODEC_LIST, 
                       LB_SETCURSEL, 0, 0);
    pSysDevEnum->Release();
    pEnum->Release();
}
```



<span data-ttu-id="47afe-131">Pour créer une instance de filtre à partir du moniker, appelez la méthode **IMoniker :: BindToObject** .</span><span class="sxs-lookup"><span data-stu-id="47afe-131">To create a filter instance from the moniker, call the **IMoniker::BindToObject** method.</span></span> <span data-ttu-id="47afe-132">La méthode retourne un pointeur [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="47afe-132">The method returns an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span>


```C++
IBaseFilter *pFilter = NULL;
hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, 
                                       (void**)&pFilter);
if (SUCCEEDED(hr))
{
    // Use the filter. 
    // Remember to release the IBaseFilter interface.
}
```



<span data-ttu-id="47afe-133">Pour les codecs VCM, chaque moniker représente un codec particulier, même si tous les codecs sont encapsulés par le même filtre de compression AVI.</span><span class="sxs-lookup"><span data-stu-id="47afe-133">For VCM codecs, each moniker represents one particular codec, even though all of the codecs are wrapped by the same AVI Compression filter.</span></span> <span data-ttu-id="47afe-134">L’appel de **BindToObject** crée une instance de ce filtre, initialisée pour ce codec.</span><span class="sxs-lookup"><span data-stu-id="47afe-134">Calling **BindToObject** creates an instance of this filter, initialized for that codec.</span></span> <span data-ttu-id="47afe-135">Pour cette raison, vous ne pouvez pas appeler **CoCreateInstance** directement sur le filtre de compression avi.</span><span class="sxs-lookup"><span data-stu-id="47afe-135">For this reason, you cannot call **CoCreateInstance** directly on the AVI Compression filter.</span></span> <span data-ttu-id="47afe-136">Vous devez passer par l’énumérateur du périphérique système.</span><span class="sxs-lookup"><span data-stu-id="47afe-136">You must go through the system device enumerator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47afe-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="47afe-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47afe-138">Recompression d’un fichier AVI</span><span class="sxs-lookup"><span data-stu-id="47afe-138">Recompressing an AVI File</span></span>](recompressing-an-avi-file.md)
</dt> </dl>

 

 
