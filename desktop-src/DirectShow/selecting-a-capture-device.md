---
description: Sélection d’un périphérique de capture
ms.assetid: 8f92873d-569a-48af-a913-6d4cce65640f
title: Sélection d’un périphérique de capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b599728c6bd2d98b89285b6008923aa4fb2a3aef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106543068"
---
# <a name="selecting-a-capture-device"></a><span data-ttu-id="716b4-103">Sélection d’un périphérique de capture</span><span class="sxs-lookup"><span data-stu-id="716b4-103">Selecting a Capture Device</span></span>

<span data-ttu-id="716b4-104">Pour sélectionner un périphérique de capture audio ou vidéo, utilisez l' [énumérateur de périphérique système](system-device-enumerator.md), décrit dans la rubrique [utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="716b4-104">To select an audio or video capture device, use the [System Device Enumerator](system-device-enumerator.md), described in the topic [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span> <span data-ttu-id="716b4-105">L’énumérateur de périphérique système retourne une collection de monikers de périphérique, sélectionnée par catégorie d’appareil.</span><span class="sxs-lookup"><span data-stu-id="716b4-105">The System Device Enumerator returns a collection of device monikers, selected by device category.</span></span> <span data-ttu-id="716b4-106">Un *moniker* est un objet com qui contient des informations sur un autre objet.</span><span class="sxs-lookup"><span data-stu-id="716b4-106">A *moniker* is a COM object that contains information about another object.</span></span> <span data-ttu-id="716b4-107">Les monikers permettent à l’application d’obtenir des informations sur un objet sans réellement créer l’objet.</span><span class="sxs-lookup"><span data-stu-id="716b4-107">Monikers enable the application to get information about an object without actually creating the object.</span></span> <span data-ttu-id="716b4-108">Plus tard, l’application peut utiliser le moniker pour créer l’objet.</span><span class="sxs-lookup"><span data-stu-id="716b4-108">Later, the application can use the moniker to create the object.</span></span> <span data-ttu-id="716b4-109">Pour plus d’informations sur les monikers, consultez la documentation de [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker).</span><span class="sxs-lookup"><span data-stu-id="716b4-109">For more information about monikers, see the documentation for [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker).</span></span>

<span data-ttu-id="716b4-110">Pour utiliser l’énumérateur de périphérique système, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="716b4-110">To use the System Device Enumerator, perform the following steps.</span></span>

1.  <span data-ttu-id="716b4-111">Appelez [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer une instance de l’énumérateur du périphérique système.</span><span class="sxs-lookup"><span data-stu-id="716b4-111">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create an instance of the System Device Enumerator.</span></span>
2.  <span data-ttu-id="716b4-112">Appelez [**ICreateDevEnum :: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) et spécifiez la catégorie d’appareil en tant que GUID.</span><span class="sxs-lookup"><span data-stu-id="716b4-112">Call [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) and specify the device category as a GUID.</span></span> <span data-ttu-id="716b4-113">Pour les périphériques de capture, les catégories suivantes sont pertinentes.</span><span class="sxs-lookup"><span data-stu-id="716b4-113">For capture devices, the following categories are relevant.</span></span> 

    | <span data-ttu-id="716b4-114">GUID de la catégorie</span><span class="sxs-lookup"><span data-stu-id="716b4-114">Category GUID</span></span>                       | <span data-ttu-id="716b4-115">Description</span><span class="sxs-lookup"><span data-stu-id="716b4-115">Description</span></span>           |
    |-------------------------------------|-----------------------|
    | <span data-ttu-id="716b4-116">**CLSID \_ AudioInputDeviceCategory**</span><span class="sxs-lookup"><span data-stu-id="716b4-116">**CLSID\_AudioInputDeviceCategory**</span></span> | <span data-ttu-id="716b4-117">Périphériques de capture audio</span><span class="sxs-lookup"><span data-stu-id="716b4-117">Audio capture devices</span></span> |
    | <span data-ttu-id="716b4-118">**CLSID \_ VideoInputDeviceCategory**</span><span class="sxs-lookup"><span data-stu-id="716b4-118">**CLSID\_VideoInputDeviceCategory**</span></span> | <span data-ttu-id="716b4-119">Périphériques de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="716b4-119">Video capture devices</span></span> |

    

     

    <span data-ttu-id="716b4-120">Si une caméra vidéo a un microphone intégré, elle apparaît dans les deux catégories.</span><span class="sxs-lookup"><span data-stu-id="716b4-120">If a video camera has an integrated microphone, it appears in both categories.</span></span> <span data-ttu-id="716b4-121">Toutefois, la caméra et le microphone sont traités comme des appareils distincts par le système, à des fins d’énumération, de création d’appareils et de diffusion de données.</span><span class="sxs-lookup"><span data-stu-id="716b4-121">However, the camera and microphone are treated as separate devices by the system, for purposes of enumeration, device creation, and data streaming.</span></span>

3.  <span data-ttu-id="716b4-122">La méthode [**CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) retourne un pointeur vers l’interface [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) .</span><span class="sxs-lookup"><span data-stu-id="716b4-122">The [**CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) method returns a pointer to the [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) interface.</span></span> <span data-ttu-id="716b4-123">Pour énumérer les monikers, appelez [**IEnumMoniker :: Next**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next).</span><span class="sxs-lookup"><span data-stu-id="716b4-123">To enumerate the monikers, call [**IEnumMoniker::Next**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next).</span></span>

<span data-ttu-id="716b4-124">Le code suivant crée un énumérateur pour une catégorie d’appareils spécifiée.</span><span class="sxs-lookup"><span data-stu-id="716b4-124">The following code creates an enumerator for a specified device category.</span></span>


```C++
#include <windows.h>
#include <dshow.h>

#pragma comment(lib, "strmiids")

HRESULT EnumerateDevices(REFGUID category, IEnumMoniker **ppEnum)
{
    // Create the System Device Enumerator.
    ICreateDevEnum *pDevEnum;
    HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL,  
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pDevEnum));

    if (SUCCEEDED(hr))
    {
        // Create an enumerator for the category.
        hr = pDevEnum->CreateClassEnumerator(category, ppEnum, 0);
        if (hr == S_FALSE)
        {
            hr = VFW_E_NOT_FOUND;  // The category is empty. Treat as an error.
        }
        pDevEnum->Release();
    }
    return hr;
}
```



<span data-ttu-id="716b4-125">L’interface [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) énumère une liste d’interfaces [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) , chacune représentant un moniker de périphérique.</span><span class="sxs-lookup"><span data-stu-id="716b4-125">The [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) interface enumerates a list of [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interfaces, each of which represents a device moniker.</span></span> <span data-ttu-id="716b4-126">L’application peut lire les propriétés du moniker ou utiliser le moniker pour créer un filtre de capture DirectShow pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="716b4-126">The application can read properties from the moniker, or use the moniker to create a DirectShow capture filter for the device.</span></span> <span data-ttu-id="716b4-127">Les propriétés du moniker sont retournées en tant que valeurs de **type Variant** .</span><span class="sxs-lookup"><span data-stu-id="716b4-127">Moniker properties are returned as **VARIANT** values.</span></span> <span data-ttu-id="716b4-128">Les propriétés suivantes sont prises en charge par les monikers de périphérique.</span><span class="sxs-lookup"><span data-stu-id="716b4-128">The following properties are supported by device monikers.</span></span>



| <span data-ttu-id="716b4-129">Propriété</span><span class="sxs-lookup"><span data-stu-id="716b4-129">Property</span></span>       | <span data-ttu-id="716b4-130">Description</span><span class="sxs-lookup"><span data-stu-id="716b4-130">Description</span></span>                                                               | <span data-ttu-id="716b4-131">Type VARIANT</span><span class="sxs-lookup"><span data-stu-id="716b4-131">VARIANT Type</span></span> |
|----------------|---------------------------------------------------------------------------|--------------|
| <span data-ttu-id="716b4-132">Convivial</span><span class="sxs-lookup"><span data-stu-id="716b4-132">"FriendlyName"</span></span> | <span data-ttu-id="716b4-133">Nom de l’appareil</span><span class="sxs-lookup"><span data-stu-id="716b4-133">The name of the device.</span></span>                                                   | <span data-ttu-id="716b4-134">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="716b4-134">**VT\_BSTR**</span></span> |
| <span data-ttu-id="716b4-135">Descriptive</span><span class="sxs-lookup"><span data-stu-id="716b4-135">"Description"</span></span>  | <span data-ttu-id="716b4-136">Description de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="716b4-136">A description of the device.</span></span>                                              | <span data-ttu-id="716b4-137">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="716b4-137">**VT\_BSTR**</span></span> |
| <span data-ttu-id="716b4-138">DevicePath</span><span class="sxs-lookup"><span data-stu-id="716b4-138">"DevicePath"</span></span>   | <span data-ttu-id="716b4-139">Chaîne unique qui identifie l’appareil.</span><span class="sxs-lookup"><span data-stu-id="716b4-139">A unique string that identifies the device.</span></span> <span data-ttu-id="716b4-140">(Périphériques de capture vidéo uniquement.)</span><span class="sxs-lookup"><span data-stu-id="716b4-140">(Video capture devices only.)</span></span> | <span data-ttu-id="716b4-141">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="716b4-141">**VT\_BSTR**</span></span> |
| <span data-ttu-id="716b4-142">"WaveInID"</span><span class="sxs-lookup"><span data-stu-id="716b4-142">"WaveInID"</span></span>     | <span data-ttu-id="716b4-143">Identificateur d’un périphérique de capture audio.</span><span class="sxs-lookup"><span data-stu-id="716b4-143">The identifier for an audio capture device.</span></span> <span data-ttu-id="716b4-144">(Périphériques de capture audio uniquement.)</span><span class="sxs-lookup"><span data-stu-id="716b4-144">(Audio capture devices only.)</span></span> | <span data-ttu-id="716b4-145">**VT \_**</span><span class="sxs-lookup"><span data-stu-id="716b4-145">**VT\_I4**</span></span>   |



 

<span data-ttu-id="716b4-146">Les propriétés « FriendlyName » et « description » conviennent à l’affichage dans une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="716b4-146">The "FriendlyName" and "Description" properties are suitable for displaying in a UI.</span></span>

-   <span data-ttu-id="716b4-147">La propriété « FriendlyName » est disponible pour chaque appareil.</span><span class="sxs-lookup"><span data-stu-id="716b4-147">The "FriendlyName" property is available for every device.</span></span> <span data-ttu-id="716b4-148">Il contient un nom explicite pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="716b4-148">It contains a human-readable name for the device.</span></span>
-   <span data-ttu-id="716b4-149">La propriété « Description » est disponible uniquement pour les appareils caméscopes DV et D-VHS/MPEG.</span><span class="sxs-lookup"><span data-stu-id="716b4-149">The "Description" property is available only for DV and D-VHS/MPEG camcorder devices.</span></span> <span data-ttu-id="716b4-150">Pour plus d’informations, consultez [pilote MSDV](msdv-driver.md) et [pilote MSTape](mstape-driver.md).</span><span class="sxs-lookup"><span data-stu-id="716b4-150">For more information, see [MSDV Driver](msdv-driver.md) and [MSTape Driver](mstape-driver.md).</span></span> <span data-ttu-id="716b4-151">S’il est disponible, il contient une description de l’appareil qui est plus spécifique que la propriété « FriendlyName ».</span><span class="sxs-lookup"><span data-stu-id="716b4-151">If available, it contains a description of the device which is more specific than the "FriendlyName" property.</span></span> <span data-ttu-id="716b4-152">En général, il comprend le nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="716b4-152">Typically it includes the vendor name.</span></span>
-   <span data-ttu-id="716b4-153">La propriété « DevicePath » n’est pas une chaîne explicite, mais elle est toujours unique pour chaque périphérique de capture vidéo sur le système.</span><span class="sxs-lookup"><span data-stu-id="716b4-153">The "DevicePath" property is not a human-readable string, but is guaranteed to be unique for each video capture device on the system.</span></span> <span data-ttu-id="716b4-154">Vous pouvez utiliser cette propriété pour faire la distinction entre deux ou plusieurs instances du même modèle de périphérique.</span><span class="sxs-lookup"><span data-stu-id="716b4-154">You can use this property to distinguish between two or more instances of the same model of device.</span></span>
-   <span data-ttu-id="716b4-155">Si la propriété « WaveInID » est présente, cela signifie que le filtre de capture DirectShow utilise les API [audio Waveform](../multimedia/waveform-audio.md) en interne pour communiquer avec l’appareil.</span><span class="sxs-lookup"><span data-stu-id="716b4-155">If the "WaveInID" property is present, it means the DirectShow capture filter uses the [Waveform Audio](../multimedia/waveform-audio.md) APIs internally to communicate with the device.</span></span> <span data-ttu-id="716b4-156">La valeur de la propriété « WaveInID » correspond à l’identificateur utilisé par les fonctions «*Wave \**», telles que [_ *waveInOpen* \*](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen).</span><span class="sxs-lookup"><span data-stu-id="716b4-156">The value of the "WaveInID" property corresponds to the identifier used by the \**waveIn\** _ functions, such as [_ *waveInOpen*\*](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen).</span></span>

<span data-ttu-id="716b4-157">Pour lire les propriétés du moniker, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="716b4-157">To read properties from the moniker, perform the following steps.</span></span>

1.  <span data-ttu-id="716b4-158">Appelez [**IMoniker :: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) pour obtenir un pointeur vers l’interface [**IPropertyBag**](../com/ipropertybag-and-ipersistpropertybag.md) .</span><span class="sxs-lookup"><span data-stu-id="716b4-158">Call [**IMoniker::BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) to get a pointer to the [**IPropertyBag**](../com/ipropertybag-and-ipersistpropertybag.md) interface.</span></span>
2.  <span data-ttu-id="716b4-159">Appelez **IPropertyBag :: Read** pour lire la propriété.</span><span class="sxs-lookup"><span data-stu-id="716b4-159">Call **IPropertyBag::Read** to read the property.</span></span>

<span data-ttu-id="716b4-160">L’exemple de code suivant montre comment énumérer une liste de monikers de périphériques et obtenir les propriétés.</span><span class="sxs-lookup"><span data-stu-id="716b4-160">The following code example shows how to enumerate a list of device monikers and get the properties.</span></span>


```C++
void DisplayDeviceInformation(IEnumMoniker *pEnum)
{
    IMoniker *pMoniker = NULL;

    while (pEnum->Next(1, &pMoniker, NULL) == S_OK)
    {
        IPropertyBag *pPropBag;
        HRESULT hr = pMoniker->BindToStorage(0, 0, IID_PPV_ARGS(&pPropBag));
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue;  
        } 

        VARIANT var;
        VariantInit(&var);

        // Get description or friendly name.
        hr = pPropBag->Read(L"Description", &var, 0);
        if (FAILED(hr))
        {
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
        }
        if (SUCCEEDED(hr))
        {
            printf("%S\n", var.bstrVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Write(L"FriendlyName", &var);

        // WaveInID applies only to audio capture devices.
        hr = pPropBag->Read(L"WaveInID", &var, 0);
        if (SUCCEEDED(hr))
        {
            printf("WaveIn ID: %d\n", var.lVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Read(L"DevicePath", &var, 0);
        if (SUCCEEDED(hr))
        {
            // The device path is not intended for display.
            printf("Device path: %S\n", var.bstrVal);
            VariantClear(&var); 
        }

        pPropBag->Release();
        pMoniker->Release();
    }
}

void main()
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        IEnumMoniker *pEnum;

        hr = EnumerateDevices(CLSID_VideoInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        hr = EnumerateDevices(CLSID_AudioInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        CoUninitialize();
    }
}
```



<span data-ttu-id="716b4-161">Pour créer un filtre de capture DirectShow pour l’appareil, appelez la méthode [**IMoniker :: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) pour obtenir un pointeur [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="716b4-161">To create a DirectShow capture filter for the device, call the [**IMoniker::BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) method to get an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span> <span data-ttu-id="716b4-162">Appelez ensuite [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) pour ajouter le filtre au graphique de filtre :</span><span class="sxs-lookup"><span data-stu-id="716b4-162">Then call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the filter graph:</span></span>


```C++
IBaseFilter *pCap = NULL;
hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter, (void**)&pCap);
if (SUCCEEDED(hr))
{
    hr = m_pGraph->AddFilter(pCap, L"Capture Filter");
}
```



## <a name="related-topics"></a><span data-ttu-id="716b4-163">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="716b4-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="716b4-164">Capture audio</span><span class="sxs-lookup"><span data-stu-id="716b4-164">Audio Capture</span></span>](audio-capture.md)
</dt> <dt>

[<span data-ttu-id="716b4-165">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="716b4-165">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 
