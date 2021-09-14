---
description: Cette rubrique explique comment demander des autorisations à l’utilisateur pour utiliser des capteurs. Pour obtenir des informations générales sur les autorisations dans l’API de capteur, consultez Gestion des autorisations utilisateur.
ms.assetid: e43ad497-86f1-4804-a67a-0aeb56b80d7f
title: Demande d’autorisations utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41e103426388d2db49bb5a8fb01d3370207ec49b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008956"
---
# <a name="requesting-user-permissions"></a>Demande d’autorisations utilisateur

Cette rubrique explique comment demander des autorisations à l’utilisateur pour utiliser des capteurs. Pour obtenir des informations générales sur les autorisations dans l’API de capteur, consultez [gestion des autorisations utilisateur](managing-user-permissions.md).

Les exemples suivants illustrent une partie du scénario courant dans lequel vous pouvez choisir de demander des autorisations utilisateur.

L’exemple de code suivant demande simplement des autorisations pour tous les capteurs récupérés à partir du gestionnaire de capteurs, par type, à l’aide d’un appel de méthode asynchrone. La plateforme ouvre une boîte de dialogue qui invite l’utilisateur à activer uniquement les capteurs qui ne sont pas encore activés. Pour déterminer si l’utilisateur a activé des capteurs dans ce cas, vous devez gérer l’événement [**ISensorEvents :: OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) .


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByType(SAMPLE_SENSOR_TYPE_TIME, &pSensorColl);

if(SUCCEEDED(hr))
{
    // Request permissions for all sensors
    // in the collection.
    hr = pSensorManager->RequestPermissions(0, pSensorColl, FALSE);
}

```



Vous pouvez choisir de tester l’état du capteur de façon synchrone avant de tenter de récupérer les données. L’exemple de code suivant illustre cette technique.


```C++
if(SUCCEEDED(hr))
{
   // Check the current sensor state.
   SensorState state = SENSOR_STATE_NOT_AVAILABLE;

   hr = pSensor->GetState(&state);

   if(SUCCEEDED(hr))
   {
       if(state == SENSOR_STATE_ACCESS_DENIED)
       {
           wprintf_s(L"\nSensor not enabled, requesting permissions...\n");
           hr = pSensorManager->RequestPermissions(0, pSensorColl, TRUE);

           if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED) ||
              hr == HRESULT_FROM_WIN32(ERROR_CANCELLED)) 
           {
               wprintf_s(L"\nYou have previously denied access to this sensor.\n");
               wprintf_s(L"Please use the Location and Other Sensors control panel\n");
               wprintf_s(L"to enable the WDK Time Sensor and run this program again.\n");
           }
       }
   }
}

if(SUCCEEDED(hr))
{
    // Get the data report.
    hr = pSensor->GetData(&pReport);
}
```



L’exemple de code suivant demande à l’utilisateur des autorisations de capteur si une tentative de récupération d’un rapport de données à partir d’un capteur particulier échoue.


```C++
if(SUCCEEDED(hr))
{
    // Get the data report.
    hr = pSensor->GetData(&pReport);

    if(E_ACCESSDENIED == hr)
    {
       wprintf_s(L"\nSensor not enabled, requesting permissions...\n");
       hr = pSensorManager->RequestPermissions(0, pSensorColl, TRUE);

       if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED) ||
          hr == HRESULT_FROM_WIN32(ERROR_CANCELLED)) 
       {
           wprintf_s(L"\nYou have previously denied access to this sensor.\n");
           wprintf_s(L"Please use the Location and Other Sensors control panel\n");
           wprintf_s(L"to enable the WDK Time Sensor and run this program again.\n");
       }
    }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)
</dt> <dt>

[Gestion des autorisations utilisateur](managing-user-permissions.md)
</dt> </dl>

 

 
