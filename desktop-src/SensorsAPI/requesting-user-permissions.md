---
description: Cette rubrique explique comment demander des autorisations à l’utilisateur pour utiliser des capteurs. Pour obtenir des informations générales sur les autorisations dans l’API de capteur, consultez Gestion des autorisations utilisateur.
ms.assetid: e43ad497-86f1-4804-a67a-0aeb56b80d7f
title: Demande d’autorisations utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41e103426388d2db49bb5a8fb01d3370207ec49b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525654"
---
# <a name="requesting-user-permissions"></a><span data-ttu-id="d869b-104">Demande d’autorisations utilisateur</span><span class="sxs-lookup"><span data-stu-id="d869b-104">Requesting User Permissions</span></span>

<span data-ttu-id="d869b-105">Cette rubrique explique comment demander des autorisations à l’utilisateur pour utiliser des capteurs.</span><span class="sxs-lookup"><span data-stu-id="d869b-105">This topic describes how to request permissions from the user to use sensors.</span></span> <span data-ttu-id="d869b-106">Pour obtenir des informations générales sur les autorisations dans l’API de capteur, consultez [gestion des autorisations utilisateur](managing-user-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="d869b-106">For background information about permissions in the Sensor API, see [Managing User Permissions](managing-user-permissions.md).</span></span>

<span data-ttu-id="d869b-107">Les exemples suivants illustrent une partie du scénario courant dans lequel vous pouvez choisir de demander des autorisations utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d869b-107">The following examples illustrate some of the common scenarious where you can choose to request user permissions.</span></span>

<span data-ttu-id="d869b-108">L’exemple de code suivant demande simplement des autorisations pour tous les capteurs récupérés à partir du gestionnaire de capteurs, par type, à l’aide d’un appel de méthode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="d869b-108">The following example code simply requests permissions for all sensors retrieved from the sensor manager, by type, using an asynchronous method call.</span></span> <span data-ttu-id="d869b-109">La plateforme ouvre une boîte de dialogue qui invite l’utilisateur à activer uniquement les capteurs qui ne sont pas encore activés.</span><span class="sxs-lookup"><span data-stu-id="d869b-109">The platform will open a dialog box to prompt the user only to enable sensors that are not already enabled.</span></span> <span data-ttu-id="d869b-110">Pour déterminer si l’utilisateur a activé des capteurs dans ce cas, vous devez gérer l’événement [**ISensorEvents :: OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) .</span><span class="sxs-lookup"><span data-stu-id="d869b-110">To determine whether the user enabled any sensors in this case, you must handle the [**ISensorEvents::OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) event.</span></span>


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



<span data-ttu-id="d869b-111">Vous pouvez choisir de tester l’état du capteur de façon synchrone avant de tenter de récupérer les données.</span><span class="sxs-lookup"><span data-stu-id="d869b-111">You can choose to test the sensor state synchronously before attempting to retrieve data.</span></span> <span data-ttu-id="d869b-112">L’exemple de code suivant illustre cette technique.</span><span class="sxs-lookup"><span data-stu-id="d869b-112">The following example code demonstrates this technique.</span></span>


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



<span data-ttu-id="d869b-113">L’exemple de code suivant demande à l’utilisateur des autorisations de capteur si une tentative de récupération d’un rapport de données à partir d’un capteur particulier échoue.</span><span class="sxs-lookup"><span data-stu-id="d869b-113">The following example code prompts the user for sensor permissions if an attempt to retrieve a data report from a particular sensor fails.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d869b-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d869b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d869b-115">**ISensorManager**</span><span class="sxs-lookup"><span data-stu-id="d869b-115">**ISensorManager**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)
</dt> <dt>

[<span data-ttu-id="d869b-116">Gestion des autorisations utilisateur</span><span class="sxs-lookup"><span data-stu-id="d869b-116">Managing User Permissions</span></span>](managing-user-permissions.md)
</dt> </dl>

 

 
