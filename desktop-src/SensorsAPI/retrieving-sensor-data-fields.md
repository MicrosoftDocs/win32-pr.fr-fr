---
description: Cette rubrique explique comment récupérer des données à partir d’un capteur, de façon synchrone et asynchrone.
ms.assetid: 4ae80816-5e53-4ed1-9300-4b38c22d65e2
title: Récupération des valeurs de données de capteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4642f120e549cd77b1b37610037092facf2ead1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517248"
---
# <a name="retrieving-sensor-data-values"></a><span data-ttu-id="5c6e5-103">Récupération des valeurs de données de capteur</span><span class="sxs-lookup"><span data-stu-id="5c6e5-103">Retrieving Sensor Data Values</span></span>

<span data-ttu-id="5c6e5-104">Cette rubrique explique comment récupérer des données à partir d’un capteur, de façon synchrone et asynchrone.</span><span class="sxs-lookup"><span data-stu-id="5c6e5-104">This topic describes how to retrieve data from a sensor, synchronously and asynchronously.</span></span>

## <a name="retrieving-data-synchronously"></a><span data-ttu-id="5c6e5-105">Récupération de données de façon synchrone</span><span class="sxs-lookup"><span data-stu-id="5c6e5-105">Retrieving Data Synchronously</span></span>

<span data-ttu-id="5c6e5-106">Vous pouvez récupérer des données de capteur de façon synchrone en appelant [**ISensor :: GetData**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getdata).</span><span class="sxs-lookup"><span data-stu-id="5c6e5-106">You can retrieve sensor data synchronously by calling [**ISensor::GetData**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getdata).</span></span>

<span data-ttu-id="5c6e5-107">L’exemple de code suivant récupère un rapport de données de capteur, puis récupère trois valeurs de champ de données individuelles.</span><span class="sxs-lookup"><span data-stu-id="5c6e5-107">The following example code retrieves a sensor data report, and then retrieves three individual data field values.</span></span> <span data-ttu-id="5c6e5-108">L’exemple de capteur fournit des données personnalisées sur l’heure locale actuelle dans les champs de données Hour, minute et second.</span><span class="sxs-lookup"><span data-stu-id="5c6e5-108">The sample sensor provides custom data about the current local time in hour, minute, and second data fields.</span></span> <span data-ttu-id="5c6e5-109">La variable nommée pSensor contient un pointeur vers [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) qui représente le capteur qui fournit les données.</span><span class="sxs-lookup"><span data-stu-id="5c6e5-109">The variable named pSensor contains a pointer to [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) that represents the sensor that supplies the data.</span></span>


```C++
if(SUCCEEDED(hr))
{
    // Get the data report.
    hr = pSensor->GetData(&pReport);
}
  
if(SUCCEEDED(hr))
{
    PROPVARIANT var = {};

    hr = pReport->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_HOUR, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulHour = var.ulVal;                
        }
    }

    PropVariantClear(&var);

    hr = pReport->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_MINUTE, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulMinute = var.ulVal;
        }
    }

    PropVariantClear(&var);

    hr = pReport->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_SECOND, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulSecond = var.ulVal;
        }
    }

    PropVariantClear(&var);        

    if(SUCCEEDED(hr))
    {
        // Print the local time to the console window.
        wprintf_s(L"\nCurrent local time is: \n");
        wprintf_s(L"%02d:%02d:%02d (synchronous)\n\n", ulHour, ulMinute, ulSecond);
    }

```



## <a name="retrieving-data-asynchronously"></a><span data-ttu-id="5c6e5-110">Récupération de données de façon asynchrone</span><span class="sxs-lookup"><span data-stu-id="5c6e5-110">Retrieving Data Asynchronously</span></span>

<span data-ttu-id="5c6e5-111">Vous pouvez recevoir des données de capteur de manière asynchrone en vous inscrivant pour recevoir l’événement [**ISensorEvents :: OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) .</span><span class="sxs-lookup"><span data-stu-id="5c6e5-111">You can receive sensor data asynchronously by registering to receive the [**ISensorEvents::OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) event.</span></span> <span data-ttu-id="5c6e5-112">Pour comprendre comment recevoir des rappels d’événements de capteur, consultez [utilisation des événements de l’API de capteur](using-sensor-api-events.md).</span><span class="sxs-lookup"><span data-stu-id="5c6e5-112">To understand how to receive sensor event callbacks, see [Using Sensor API Events](using-sensor-api-events.md).</span></span>

<span data-ttu-id="5c6e5-113">L’exemple de code suivant illustre une implémentation de [**ISensorEvents :: OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) qui récupère des valeurs de données à partir du rapport de données fourni par l’événement.</span><span class="sxs-lookup"><span data-stu-id="5c6e5-113">The following example code shows an implementation of [**ISensorEvents::OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) that retrieves data values from the data report provided by the event.</span></span> <span data-ttu-id="5c6e5-114">L’exemple de capteur fournit des données personnalisées sur l’heure locale actuelle dans les champs de données Hour, minute et second.</span><span class="sxs-lookup"><span data-stu-id="5c6e5-114">The sample sensor provides custom data about the current local time in hour, minute, and second data fields.</span></span>


```C++
STDMETHODIMP OnDataUpdated(
        ISensor *pSensor,
        ISensorDataReport *pNewData)
{
    HRESULT hr = S_OK;

    if(NULL == pNewData ||
       NULL == pSensor)
    {
        return E_INVALIDARG;
    }

    ULONG ulHour = 0;
    ULONG ulMinute = 0;
    ULONG ulSecond = 0;

    PROPVARIANT var = {};

    hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_HOUR, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulHour = var.ulVal;                
        }
    }

    PropVariantClear(&var);

    if(SUCCEEDED(hr))
    {
        hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_MINUTE, &var);
    }

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulMinute = var.ulVal;
        }
    }

    PropVariantClear(&var);

    if(SUCCEEDED(hr))
    {
        hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_SECOND, &var);
    }

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulSecond = var.ulVal;
        }
    }

    PropVariantClear(&var);

    if(SUCCEEDED(hr))
    {
        // Print
        wprintf_s(L"Current local time is: \n");
        wprintf_s(L"%02d:%02d:%02d (asynchronous)\n", ulHour, ulMinute, ulSecond);
    }

    return hr;
}
```



 

 
