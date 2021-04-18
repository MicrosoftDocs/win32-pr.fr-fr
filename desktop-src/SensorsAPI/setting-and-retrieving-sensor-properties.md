---
description: Cette rubrique explique comment récupérer et définir des valeurs pour les propriétés de capteur. L’interface ISensor fournit les méthodes permettant de définir et de récupérer des valeurs pour les propriétés de capteur.
ms.assetid: 7d10e5b4-bae7-4564-84eb-75c6a2eeef8f
title: Récupération et définition des propriétés de capteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f64bf0e253f47ae2d8cd1f4945f3b87aa3406b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542956"
---
# <a name="retrieving-and-setting-sensor-properties"></a><span data-ttu-id="23e19-104">Récupération et définition des propriétés de capteur</span><span class="sxs-lookup"><span data-stu-id="23e19-104">Retrieving and Setting Sensor Properties</span></span>

<span data-ttu-id="23e19-105">Cette rubrique explique comment récupérer et définir des valeurs pour les propriétés de capteur.</span><span class="sxs-lookup"><span data-stu-id="23e19-105">This topic describes how to retrieve and set values for sensor properties.</span></span> <span data-ttu-id="23e19-106">L’interface [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) fournit les méthodes permettant de définir et de récupérer des valeurs pour les propriétés de capteur.</span><span class="sxs-lookup"><span data-stu-id="23e19-106">The [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) interface provides the methods to set and retrieve values for sensor properties.</span></span>

## <a name="retrieving-sensor-properties"></a><span data-ttu-id="23e19-107">Récupération des propriétés de capteur</span><span class="sxs-lookup"><span data-stu-id="23e19-107">Retrieving Sensor Properties</span></span>

<span data-ttu-id="23e19-108">Vous pouvez récupérer des valeurs de propriété à partir d’un capteur avant que l’utilisateur ne l’ait activé.</span><span class="sxs-lookup"><span data-stu-id="23e19-108">You can retrieve some property values from a sensor before the user has enabled it.</span></span> <span data-ttu-id="23e19-109">Des informations telles que le nom du fabricant ou le modèle du capteur peuvent vous aider à déterminer si votre programme peut utiliser le capteur.</span><span class="sxs-lookup"><span data-stu-id="23e19-109">Information such as the manufacturer's name or the model of the sensor can help you to decide whether your program can use the sensor.</span></span>

<span data-ttu-id="23e19-110">Vous pouvez choisir de récupérer une seule valeur de propriété ou de récupérer une collection de valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="23e19-110">You can choose to retrieve a single property value, or to retrieve a collection of property values together.</span></span> <span data-ttu-id="23e19-111">Pour récupérer une valeur unique, appelez [**ISensor :: GetProperty**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperty).</span><span class="sxs-lookup"><span data-stu-id="23e19-111">To retrieve single value, call [**ISensor::GetProperty**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperty).</span></span> <span data-ttu-id="23e19-112">Pour récupérer une collection de valeurs, appelez [**ISensor :: GetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperties).</span><span class="sxs-lookup"><span data-stu-id="23e19-112">To retrieve a collection of values, call [**ISensor::GetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperties).</span></span> <span data-ttu-id="23e19-113">Vous pouvez récupérer toutes les propriétés d’un capteur en passant la **valeur null** via le premier paramètre à **ISensor :: GetProperties**.</span><span class="sxs-lookup"><span data-stu-id="23e19-113">You can retrieve all properties for a sensor by passing **NULL** through the first parameter to **ISensor::GetProperties**.</span></span>

<span data-ttu-id="23e19-114">L’exemple de code suivant crée une fonction d’assistance qui imprime la valeur d’une propriété unique.</span><span class="sxs-lookup"><span data-stu-id="23e19-114">The following example code creates a helper function that prints the value of a single property.</span></span> <span data-ttu-id="23e19-115">La fonction reçoit un pointeur vers le capteur à partir duquel récupérer la valeur et une clé de propriété qui contient la propriété à imprimer.</span><span class="sxs-lookup"><span data-stu-id="23e19-115">The function receives a pointer to the sensor from which to retrieve the value and a property key that contains the property to print.</span></span> <span data-ttu-id="23e19-116">La fonction peut imprimer des valeurs pour des nombres, des chaînes et des **GUID**, mais pas d’autres types plus complexes.</span><span class="sxs-lookup"><span data-stu-id="23e19-116">The function can print values for numbers, strings, and **GUID** s, but not other, more complex types.</span></span>


```C++
HRESULT PrintSensorProperty(ISensor* pSensor, REFPROPERTYKEY pk)
{
    assert(pSensor);

    HRESULT hr = S_OK;

    PROPVARIANT pv = {};

    hr = pSensor->GetProperty(pk, &pv);

    if(SUCCEEDED(hr))
    {
        if(pv.vt == VT_UI4)  // Number
        {
            wprintf_s(L"\nSensor integer value: %u\n", pv.ulVal);
        }
        else if(pv.vt == VT_LPWSTR)  // String
        {
            wprintf_s(L"\nSensor string value: %s\n", pv.pwszVal);
        }
        else if(pv.vt == VT_CLSID)  // GUID
        {
            int iRet = 0;

            // Convert the GUID to a string.
            OLECHAR wszGuid[39] = {}; // Buffer for string.
            iRet = ::StringFromGUID2(*(pv.puuid), wszGuid, 39);

            assert(39 == iRet); // Count of characters returned for GUID.

            wprintf_s(L"\nSensor GUID value: %s\n", wszGuid);
        }
        else  // Interface or vector
        {
            wprintf_s(L"\nSensor property is a compound type. Unable to print value.");
        }
    }

    PropVariantClear(&pv);

    return hr;    
}
```



<span data-ttu-id="23e19-117">L’exemple de code suivant crée une fonction qui récupère et imprime une collection de propriétés.</span><span class="sxs-lookup"><span data-stu-id="23e19-117">The following example code creates a function that retrieves and prints a collection of properties.</span></span> <span data-ttu-id="23e19-118">Le jeu de propriétés à imprimer est défini par le tableau nommé SensorProperties.</span><span class="sxs-lookup"><span data-stu-id="23e19-118">The set of properties to print is defined by the array named SensorProperties.</span></span>


```C++
HRESULT PrintSensorProperties(ISensor* pSensor)
{
    assert(pSensor);

    HRESULT hr = S_OK;

    DWORD cVals = 0; // Count of returned properties.
    IPortableDeviceKeyCollection* pKeys = NULL; // Input
    IPortableDeviceValues* pValues = NULL;  // Output

    // Properties to print.
    const PROPERTYKEY SensorProperties[] =
    {
        SENSOR_PROPERTY_MANUFACTURER,
        SENSOR_PROPERTY_SERIAL_NUMBER,
        SENSOR_PROPERTY_DESCRIPTION,
        SENSOR_PROPERTY_FRIENDLY_NAME
    };

    // CoCreate a key collection to store property keys.
    hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection, 
                                NULL, 
                                CLSCTX_INPROC_SERVER,                                 
                                IID_PPV_ARGS(&pKeys));

    if(SUCCEEDED(hr))
    {
        // Add the properties to the key collection.
        for (DWORD dwIndex = 0; dwIndex < ARRAYSIZE(SensorProperties); dwIndex++)
        {
            hr = pKeys->Add(SensorProperties[dwIndex]);

            if(FAILED(hr))
            {
                // Unexpected.
                // This example returns the failed HRESULT.
                // You may choose to ignore failures, here.
                break;
            }
        }
    }

    if(SUCCEEDED(hr))
    {
        // Retrieve the properties from the sensor.
        hr = pSensor->GetProperties(pKeys, &pValues);
    }

    if(SUCCEEDED(hr))
    {
        // Get the number of values returned.        
        hr = pValues->GetCount(&cVals);
    }

    if(SUCCEEDED(hr))
    {
        PROPERTYKEY pk; // Keys
        PROPVARIANT pv = {}; // Values

        // Loop through the values;
        for (DWORD i = 0; i < cVals; i++)
        {
            // Get the value at the current index.
            hr = pValues->GetAt(i, &pk, &pv);

            if(SUCCEEDED(hr))
            { 
                // Find and print the property.
                if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_MANUFACTURER))
                {
                    wprintf_s(L"\nManufacturer: %s\n", pv.pwszVal);
                }
                else if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_SERIAL_NUMBER))
                {
                    wprintf_s(L"Serial number: %s\n", pv.pwszVal);
                }
                else if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_FRIENDLY_NAME))
                {
                    wprintf_s(L"Friendly name: %s\n", pv.pwszVal);
                }
                else if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_DESCRIPTION))
                {
                    wprintf_s(L"Description: %s\n", pv.pwszVal);
                }
            }

            PropVariantClear(&pv);
        } // end i loop        
    }

    SafeRelease(&pKeys);
    SafeRelease(&pValues);

    return hr;
};
```



## <a name="setting-sensor-properties"></a><span data-ttu-id="23e19-119">Définition des propriétés d’un capteur</span><span class="sxs-lookup"><span data-stu-id="23e19-119">Setting Sensor Properties</span></span>

<span data-ttu-id="23e19-120">Avant de pouvoir définir des valeurs de propriété pour un capteur, l’utilisateur doit activer le capteur.</span><span class="sxs-lookup"><span data-stu-id="23e19-120">Before you can set property values for a sensor, the user must enable the sensor.</span></span> <span data-ttu-id="23e19-121">En outre, toutes les propriétés de capteur ne peuvent pas être définies.</span><span class="sxs-lookup"><span data-stu-id="23e19-121">Also, not all sensor properties can be set.</span></span>

<span data-ttu-id="23e19-122">Pour définir une ou plusieurs valeurs pour les propriétés, appelez [**ISensor :: SetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-setproperties).</span><span class="sxs-lookup"><span data-stu-id="23e19-122">To set one or more values for properties, call [**ISensor::SetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-setproperties).</span></span> <span data-ttu-id="23e19-123">Vous fournissez cette méthode avec un pointeur [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) qui contient la collection de propriétés à définir, ainsi que leurs valeurs associées.</span><span class="sxs-lookup"><span data-stu-id="23e19-123">You provide this method with an [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) pointer that contains the collection of properties to set, and their associated values.</span></span> <span data-ttu-id="23e19-124">La méthode retourne une interface [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) correspondante qui peut contenir des codes d’erreur pour les propriétés qui n’ont pas pu être définies.</span><span class="sxs-lookup"><span data-stu-id="23e19-124">The method returns a corresponding [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) interface that may contain error codes for properties that could not be set.</span></span>

<span data-ttu-id="23e19-125">L’exemple de code suivant crée une fonction d’assistance qui définit une nouvelle valeur pour la propriété capteur \_ \_ intervalle du \_ rapport actuel \_ .</span><span class="sxs-lookup"><span data-stu-id="23e19-125">The following example code creates a helper function that sets a new value for the SENSOR\_PROPERTY\_CURRENT\_REPORT\_INTERVAL property.</span></span> <span data-ttu-id="23e19-126">La fonction prend un pointeur vers le capteur pour lequel définir la propriété, et une valeur **ULong** qui indique le nouvel intervalle de rapport à définir.</span><span class="sxs-lookup"><span data-stu-id="23e19-126">The function takes a pointer to the sensor for which to set the property, and a **ULONG** value that indicates the new report interval to be set.</span></span> <span data-ttu-id="23e19-127">(Notez que la définition d’une valeur pour cette propriété particulière ne garantit pas que le capteur accepte la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="23e19-127">(Note that setting a value for this particular property does not guarantee that the sensor will accept the specified value.</span></span> <span data-ttu-id="23e19-128">Pour plus d’informations sur le fonctionnement de cette propriété, consultez [**Propriétés de capteur**](sensor-properties.md) .)</span><span class="sxs-lookup"><span data-stu-id="23e19-128">See [**Sensor Properties**](sensor-properties.md) for information about how this property works.)</span></span>


```C++
HRESULT SetCurrentReportInterval(ISensor* pSensor, ULONG ulNewInterval)
{
    assert(pSensor);

    HRESULT hr = S_OK;

    IPortableDeviceValues* pPropsToSet = NULL; // Input
    IPortableDeviceValues* pPropsReturn = NULL; // Output

    // Create the input object.
    hr = CoCreateInstance(__uuidof(PortableDeviceValues),
                            NULL,
                            CLSCTX_INPROC_SERVER,                           
                            IID_PPV_ARGS(&pPropsToSet));

    if(SUCCEEDED(hr))
    {
        // Add the current report interval property.
        hr = pPropsToSet->SetUnsignedIntegerValue(SENSOR_PROPERTY_CURRENT_REPORT_INTERVAL, ulNewInterval);
    }

    if(SUCCEEDED(hr))
    {
        // Only setting a single property, here.
        hr = pSensor->SetProperties(pPropsToSet, &pPropsReturn);
    }

    // Test for failure.
    if(hr == S_FALSE)
    {
        HRESULT hrError = S_OK;
      
        // Check results for failure.
        hr = pPropsReturn->GetErrorValue(SENSOR_PROPERTY_CURRENT_REPORT_INTERVAL, &hrError);

        if(SUCCEEDED(hr))
        {
            // Print an error message.
            wprintf_s(L"\nSetting current report interval failed with error 0x%X\n", hrError);

            // Return the error code.
            hr = hrError;
        }
    }
    else if(hr == E_ACCESSDENIED)
    {
        // No permission. Take appropriate action.
    }

    SafeRelease(&pPropsToSet);
    SafeRelease(&pPropsReturn);
   
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="23e19-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="23e19-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23e19-130">**Propriétés du capteur**</span><span class="sxs-lookup"><span data-stu-id="23e19-130">**Sensor Properties**</span></span>](sensor-properties.md)
</dt> </dl>

 

 
