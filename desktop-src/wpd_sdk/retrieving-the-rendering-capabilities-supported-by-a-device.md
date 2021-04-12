---
description: Récupération des fonctionnalités de rendu prises en charge par un appareil
ms.assetid: 2332e3cc-087c-49cf-bde9-7f86f65158e7
title: Récupération des fonctionnalités de rendu prises en charge par un appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 523f1f9bbcaefe1c502c7c74252582fddcadad4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320713"
---
# <a name="retrieving-the-rendering-capabilities-supported-by-a-device"></a><span data-ttu-id="7849c-103">Récupération des fonctionnalités de rendu prises en charge par un appareil</span><span class="sxs-lookup"><span data-stu-id="7849c-103">Retrieving the Rendering Capabilities Supported by a Device</span></span>

<span data-ttu-id="7849c-104">Les appareils mobiles Windows qui prennent en charge la catégorie fonctionnelle informations de rendu ( \_ informations de rendu de catégorie fonctionnelle wpd \_ \_ \_ ) renvoient des informations de rendu lorsqu’elles sont interrogées.</span><span class="sxs-lookup"><span data-stu-id="7849c-104">Windows Portable Devices that support the rendering information functional category (WPD\_FUNCTIONAL\_CATEGORY\_RENDERING\_INFORMATION) will return rendering information when queried.</span></span> <span data-ttu-id="7849c-105">Les informations de rendu décrivent les exigences et les restrictions imposées aux applications qui tentent d’écrire du contenu sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="7849c-105">The rendering information describes requirements and restrictions imposed on applications that attempt to write content to a device.</span></span>

<span data-ttu-id="7849c-106">La fonction ListRenderingCapabilityInformation, la fonction d’assistance SupportsFunctionalCategory et la fonction d’assistance ReadProfileInformationProperties dans le module DeviceCapabilities. cpp illustrent la récupération des fonctionnalités de rendu pour un appareil sélectionné.</span><span class="sxs-lookup"><span data-stu-id="7849c-106">The ListRenderingCapabilityInformation function, the SupportsFunctionalCategory helper function, and the ReadProfileInformationProperties helper function in the DeviceCapabilities.cpp module demonstrate the retrieval of rendering capabilities for a selected device.</span></span>

<span data-ttu-id="7849c-107">Votre application peut récupérer les fonctionnalités de rendu prises en charge par un appareil à l’aide des interfaces décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7849c-107">Your application can retrieve the rendering capabilities supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="7849c-108">Interface</span><span class="sxs-lookup"><span data-stu-id="7849c-108">Interface</span></span>                                                                                      | <span data-ttu-id="7849c-109">Description</span><span class="sxs-lookup"><span data-stu-id="7849c-109">Description</span></span>                                                 |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="7849c-110">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="7849c-110">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="7849c-111">Fournit l’accès à l’interface IPortableDeviceProperties.</span><span class="sxs-lookup"><span data-stu-id="7849c-111">Provides access to the IPortableDeviceProperties interface.</span></span> |
| [<span data-ttu-id="7849c-112">**Interface IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="7849c-112">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="7849c-113">Fournit l’accès aux méthodes spécifiques à la propriété.</span><span class="sxs-lookup"><span data-stu-id="7849c-113">Provides access to the property-specific methods.</span></span>           |
| [<span data-ttu-id="7849c-114">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="7849c-114">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="7849c-115">Utilisé pour stocker les clés de propriété pour le profil donné.</span><span class="sxs-lookup"><span data-stu-id="7849c-115">Used to store the property keys for the given profile.</span></span>      |
| [<span data-ttu-id="7849c-116">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="7849c-116">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="7849c-117">Utilisé pour stocker les valeurs de propriété pour le profil donné.</span><span class="sxs-lookup"><span data-stu-id="7849c-117">Used store the property values for the given profile.</span></span>       |
| [<span data-ttu-id="7849c-118">**Interface IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="7849c-118">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="7849c-119">Utilisé pour stocker les valeurs de propriété pour le profil donné.</span><span class="sxs-lookup"><span data-stu-id="7849c-119">Used store the property values for the given profile.</span></span>       |
| [<span data-ttu-id="7849c-120">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="7849c-120">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="7849c-121">Utilisé pour stocker les valeurs de propriété pour le profil donné.</span><span class="sxs-lookup"><span data-stu-id="7849c-121">Used store the property values for the given profile.</span></span>       |
| [<span data-ttu-id="7849c-122">**Interface IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="7849c-122">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)           | <span data-ttu-id="7849c-123">Utilisé pour stocker les valeurs de propriété pour le profil donné.</span><span class="sxs-lookup"><span data-stu-id="7849c-123">Used store the property values for the given profile.</span></span>       |



 

<span data-ttu-id="7849c-124">L’une des premières tâches accomplies par l’exemple d’application consiste à déterminer si l’appareil sélectionné est en capacité de répertorier les fonctionnalités de rendu.</span><span class="sxs-lookup"><span data-stu-id="7849c-124">One of the first tasks accomplished by the sample application is to determine whether the selected device is capable of listing rendering capabilities.</span></span> <span data-ttu-id="7849c-125">La fonction d’assistance SupportsFunctionalCategory détermine si c’est le cas en appelant la fonction d’assistance ListRenderingCapabilityInformation et en passant \_ \_ les informations de rendu de catégorie fonctionnelle wpd \_ \_ comme deuxième argument.</span><span class="sxs-lookup"><span data-stu-id="7849c-125">The SupportsFunctionalCategory helper function determines whether this is the case by calling the ListRenderingCapabilityInformation helper function and passing WPD\_FUNCTIONAL\_CATEGORY\_RENDERING\_INFORMATION as the second argument.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
if (SupportsFunctionalCategory(pDevice, WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION) == FALSE)
{
    printf("This device does not support device rendering information to display\n");
    return;
}
```



<span data-ttu-id="7849c-126">Si l’appareil est en mesure de répertorier les fonctionnalités de rendu, l’étape suivante implique la récupération d’un objet [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) et l’appel de la méthode [**GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) pour récupérer un identificateur d’objet pour l’objet d’informations de rendu.</span><span class="sxs-lookup"><span data-stu-id="7849c-126">If the device is capable of listing rendering capabilities, the next step entails retrieving an [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) object and invoking the [**GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) method to retrieve an object identifier for the rendering-information object.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}

// Get the functional object identifier for the rendering information object
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalObjects(WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION, &pRenderingInfoObjects);
    if (FAILED(hr))
    {
        printf("! Failed to get functional objects, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="7849c-127">L’étape suivante consiste à stocker l’identificateur d’objet d’informations de rendu qui vient d’être récupéré dans une variable de chaîne (strRenderingInfoObjectID), puis à appeler la fonction d’assistance ReadProfileInformationProperties.</span><span class="sxs-lookup"><span data-stu-id="7849c-127">The next step is to store the rendering-information object identifier that was just retrieved in a string variable (strRenderingInfoObjectID), and then to call the ReadProfileInformationProperties helper function.</span></span> <span data-ttu-id="7849c-128">(La variable, strRenderingInfoObjectID, est passée comme deuxième argument à la fonction d’assistance.)</span><span class="sxs-lookup"><span data-stu-id="7849c-128">(The variable, strRenderingInfoObjectID, is passed as the second argument to the helper function.)</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
if (SUCCEEDED(hr))
{
    PROPVARIANT pv = {0};
    PropVariantInit(&pv);
    hr = pRenderingInfoObjects->GetAt(0, &pv);
    if ((SUCCEEDED(hr))    &&
        (pv.vt== VT_LPWSTR) )
    {
        strRenderingInfoObjectID = pv.pwszVal;
    }
    else
    {
        printf("! Failed to get first rendering object's identifier, hr = 0x%lx\n", hr);
    }

    PropVariantClear(&pv);
}

if (SUCCEEDED(hr))
{
    hr = ReadProfileInformationProperties(pDevice,
                                          strRenderingInfoObjectID,
                                          &pRenderingInfoProfiles);
    // Error output statements are performed by the helper function, so they
    // are omitted here.
}
```



<span data-ttu-id="7849c-129">L’une des premières tâches accomplies par la fonction d’assistance consiste à récupérer un objet [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) , qu’il utilisera pour accéder aux méthodes spécifiques au contenu.</span><span class="sxs-lookup"><span data-stu-id="7849c-129">One of the first tasks accomplished by the helper function is to retrieve an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object, which it will use to access the content-specific methods.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="7849c-130">Ensuite, la fonction d’assistance récupère un objet [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) , qu’il utilisera pour accéder aux méthodes spécifiques à la propriété.</span><span class="sxs-lookup"><span data-stu-id="7849c-130">Next, the helper function retrieves an [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) object, which it will use to access the property-specific methods.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="7849c-131">L’étape suivante consiste à créer un objet [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) dans lequel les clés de propriété des informations de rendu sont stockées.</span><span class="sxs-lookup"><span data-stu-id="7849c-131">The next step is to create an [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) object into which the property keys for the rendering information are stored.</span></span> <span data-ttu-id="7849c-132">Une fois l’objet créé, la méthode [**IPortableDeviceKeyCollection :: Add**](iportabledevicekeycollection-add.md) est appelée pour ajouter les clés nécessaires.</span><span class="sxs-lookup"><span data-stu-id="7849c-132">Once the object is created, the [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) method is invoked to add the necessary keys.</span></span> <span data-ttu-id="7849c-133">(Il est nécessaire d’ajouter ces clés afin que les profils de rendu correspondants puissent être récupérés dans les étapes suivantes.)</span><span class="sxs-lookup"><span data-stu-id="7849c-133">(It is necessary to add these keys so that the corresponding rendering profiles can be retrieved in the subsequent steps.)</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IPortableDeviceKeyCollection,
                      (VOID**) &pPropertiesToRead);
if (SUCCEEDED(hr))
{
    // Populate the IPortableDeviceKeyCollection with the keys we wish to read.
    // NOTE: We are not handling any special error cases here so we can proceed with
    // adding as many of the target properties as we can.
    if (pPropertiesToRead != NULL)
    {
        HRESULT hrTemp = S_OK;
        hrTemp = pPropertiesToRead->Add(WPD_RENDERING_INFORMATION_PROFILES);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_RENDERING_INFORMATION_PROFILES to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }
    }
}
```



<span data-ttu-id="7849c-134">L’étape suivante consiste à récupérer les valeurs de propriété du pilote de périphérique en appelant la méthode [**IPortableDeviceProperties :: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) .</span><span class="sxs-lookup"><span data-stu-id="7849c-134">The next step is to retrieve the property values from the device driver by calling the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pProperties->GetValues(wszFunctionalObjectID, // The object whose properties we are reading
                                pPropertiesToRead,     // The properties we want to read
                                &pObjectProperties);   // Driver supplied property values for the specified object
    if (FAILED(hr))
    {
        printf("! Failed to get all properties for object '%ws', hr= 0x%lx\n", wszFunctionalObjectID, hr);
    }
}
```



<span data-ttu-id="7849c-135">L’étape suivante récupère le profil Rendering-information et le stocke dans l’argument ppRenderingInfoProfiles.</span><span class="sxs-lookup"><span data-stu-id="7849c-135">The next step retrieves the rendering-information profile and stores it in the ppRenderingInfoProfiles argument.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pObjectProperties->GetIPortableDeviceValuesCollectionValue(WPD_RENDERING_INFORMATION_PROFILES,
                                                                    &pRenderingInfoProfiles);
    if (FAILED(hr))
    {
        printf("! Failed to get WPD_RENDERING_INFORMATION_PROFILES from rendering information, hr= 0x%lx\n",  hr);
    }
}

// QueryInterface the interface into the out-going parameters.
if (SUCCEEDED(hr))
{
    hr = pRenderingInfoProfiles->QueryInterface(IID_PPV_ARGS(ppRenderingInfoProfiles));
    if (FAILED(hr))
    {
        printf("! Failed to QueryInterface for IPortableDeviceValuesCollection (Rendering information profiles), hr= 0x%lx\n",  hr);
    }
}
```



<span data-ttu-id="7849c-136">Une fois que la fonction d’assistance a lu les \_ Propriétés des profils d’informations de rendu wpd \_ \_ , les profils de rendu s’affichent.</span><span class="sxs-lookup"><span data-stu-id="7849c-136">After the helper function reads the WPD\_RENDERING\_INFORMATION\_PROFILES properties, the rendering profiles are displayed.</span></span> <span data-ttu-id="7849c-137">Ces profils sont affichés par la fonction d’assistance DisplayRenderingProfile.</span><span class="sxs-lookup"><span data-stu-id="7849c-137">These profiles are displayed by the DisplayRenderingProfile helper function.</span></span>


```C++
void DisplayRenderingProfile(
    IPortableDeviceValues* pProfile)
{
    HRESULT hr = S_OK;
    if (pProfile == NULL)
    {
        return;
    }

    if (SUCCEEDED(hr))
    {
        DWORD dwTotalBitrate    = 0;
        DWORD dwChannelCount    = 0;
        DWORD dwAudioFormatCode = 0;
        GUID  guidFormat        = WPD_OBJECT_FORMAT_UNSPECIFIED;

        // Display WPD_MEDIA_TOTAL_BITRATE
        hr = pProfile->GetUnsignedIntegerValue(WPD_MEDIA_TOTAL_BITRATE, &dwTotalBitrate);
        if (SUCCEEDED(hr))
        {
            printf("Total Bitrate: %d\n", dwTotalBitrate);
        }

        // If we fail to read the total bitrate as a single value, then it must be
        // a valid value set.  (i.e. returning IPortableDeviceValues as the value which
        // contains properties describing the valid values for this property.)
        if (hr == DISP_E_TYPEMISMATCH)
        {
            CComPtr<IPortableDeviceValues> pExpectedValues;
            hr = pProfile->GetIPortableDeviceValuesValue(WPD_MEDIA_TOTAL_BITRATE, &pExpectedValues);
            if (SUCCEEDED(hr))
            {
                printf("Total Bitrate: ");
                DisplayExpectedValues(pExpectedValues);
            }
        }

        // If we are still a failure here, report the error
        if (FAILED(hr))
        {

            printf("! Failed to get WPD_MEDIA_TOTAL_BITRATE from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_AUDIO_CHANNEL_COUNT
        hr = pProfile->GetUnsignedIntegerValue(WPD_AUDIO_CHANNEL_COUNT, &dwChannelCount);
        if (SUCCEEDED(hr))
        {
            printf("Channel Count: %d\n", dwChannelCount);
        }
        else
        {
            printf("! Failed to get WPD_AUDIO_CHANNEL_COUNT from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_AUDIO_FORMAT_CODE
        hr = pProfile->GetUnsignedIntegerValue(WPD_AUDIO_FORMAT_CODE,   &dwAudioFormatCode);
        if (SUCCEEDED(hr))
        {
            printf("Audio Format Code: %d\n", dwAudioFormatCode);
        }
        else
        {
            printf("! Failed to get WPD_AUDIO_FORMAT_CODE from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_OBJECT_FORMAT
        hr = pProfile->GetGuidValue(WPD_OBJECT_FORMAT, &guidFormat);
        if (SUCCEEDED(hr))
        {
            printf("Object Format: %ws\n", (LPWSTR)CComBSTR(guidFormat));
        }
        else
        {
            printf("! Failed to get WPD_OBJECT_FORMAT from rendering profile, hr = 0x%lx\n",hr);
        }
    }
}
```



<span data-ttu-id="7849c-138">Notez que puisque les profils de rendu sont statiques, votre application peut choisir de lire les profils et de les stocker localement (au lieu d’accéder à l’appareil chaque fois que les données sont nécessaires).</span><span class="sxs-lookup"><span data-stu-id="7849c-138">Note that since the rendering profiles are static, your application may choose to read the profiles and store them locally (instead of accessing the device each time the data is needed).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7849c-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7849c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7849c-140">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="7849c-140">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="7849c-141">**Interface IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="7849c-141">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="7849c-142">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="7849c-142">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="7849c-143">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="7849c-143">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="7849c-144">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="7849c-144">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="7849c-145">**Interface IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="7849c-145">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> <dt>

[<span data-ttu-id="7849c-146">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="7849c-146">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



