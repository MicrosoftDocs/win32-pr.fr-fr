---
description: Cette rubrique explique comment récupérer des données à partir d’un capteur, de façon synchrone et asynchrone.
ms.assetid: 4ae80816-5e53-4ed1-9300-4b38c22d65e2
title: Récupération des valeurs de données de capteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e240b9bc14d917db0e0c4280ad957aa139369eb7762abfcd69441d25e66857d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960029"
---
# <a name="retrieving-sensor-data-values"></a>Récupération des valeurs de données de capteur

Cette rubrique explique comment récupérer des données à partir d’un capteur, de façon synchrone et asynchrone.

## <a name="retrieving-data-synchronously"></a>Récupération de données de façon synchrone

Vous pouvez récupérer des données de capteur de façon synchrone en appelant [**ISensor :: GetData**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getdata).

L’exemple de code suivant récupère un rapport de données de capteur, puis récupère trois valeurs de champ de données individuelles. L’exemple de capteur fournit des données personnalisées sur l’heure locale actuelle dans les champs de données Hour, minute et second. La variable nommée pSensor contient un pointeur vers [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) qui représente le capteur qui fournit les données.


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



## <a name="retrieving-data-asynchronously"></a>Récupération de données de façon asynchrone

Vous pouvez recevoir des données de capteur de manière asynchrone en vous inscrivant pour recevoir l’événement [**ISensorEvents :: OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) . Pour comprendre comment recevoir des rappels d’événements de capteur, consultez [utilisation des événements de l’API de capteur](using-sensor-api-events.md).

L’exemple de code suivant illustre une implémentation de [**ISensorEvents :: OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) qui récupère des valeurs de données à partir du rapport de données fourni par l’événement. L’exemple de capteur fournit des données personnalisées sur l’heure locale actuelle dans les champs de données Hour, minute et second.


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



 

 
