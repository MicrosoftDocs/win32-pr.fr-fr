---
description: Pour récupérer un objet capteur, vous utilisez l’interface ISensorManager. Vous pouvez considérer cette interface comme l’interface racine de l’API de capteur. Pour utiliser ISensorManager, vous devez d’abord appeler la méthode COM CoCreateInstance.
ms.assetid: 36631bae-f237-4951-9959-6ab6286bd1f7
title: Récupération d’un objet capteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cda6ea04d1a0580c38aef5a0b9c4186b908300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951070"
---
# <a name="retrieving-a-sensor-object"></a>Récupération d’un objet capteur

Pour récupérer un objet capteur, vous utilisez l’interface [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager) . Vous pouvez considérer cette interface comme l’interface racine de l’API de capteur. Pour utiliser **ISensorManager**, vous devez d’abord appeler la méthode com **CoCreateInstance** .

L’exemple de code suivant crée une instance du gestionnaire de capteurs.


```C++
// Create the sensor manager.
hr = CoCreateInstance(CLSID_SensorManager, 
                        NULL, CLSCTX_INPROC_SERVER,
                        IID_PPV_ARGS(&pSensorManager));

if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DISABLED_BY_POLICY))
{
    // Unable to retrieve sensor manager due to 
    // group policy settings. Alert the user.
}
```



Après la récupération réussie d’un pointeur vers [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager), vous pouvez récupérer les capteurs par catégorie, type ou ID. Si vous récupérez des capteurs par type ou par catégorie, vous recevez un pointeur vers une interface [**ISensorCollection**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection) qui contient tous les capteurs disponibles qui appartiennent au type ou à la catégorie demandé. Si vous récupérez un capteur par son ID, vous recevez un pointeur vers une interface [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) qui représente le capteur unique que vous avez demandé.

L’exemple de code suivant récupère une collection de capteurs appartenant à la catégorie nommée exemple de \_ catégorie de capteur \_ \_ date/ \_ heure. Le code récupère ensuite le premier capteur de la collection par son index.


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByCategory(SAMPLE_SENSOR_CATEGORY_DATE_TIME, &pSensorColl);
  
if(SUCCEEDED(hr))
{
    ULONG ulCount = 0;

    // Verify that the collection contains
    // at least one sensor.
    hr = pSensorColl->GetCount(&ulCount);

    if(SUCCEEDED(hr))
    {
        if(ulCount < 1)
        {
            wprintf_s(L"\nNo sensors of the requested category.\n");
            hr = E_UNEXPECTED;
        }
    }
}

if(SUCCEEDED(hr))
{
    // Get the first available sensor.
    hr = pSensorColl->GetAt(0, &pSensor);
}
```



Notez que vous pouvez récupérer tous les capteurs disponibles à l’aide de la \_ catégorie capteur \_ tout.

De la même façon, vous pouvez récupérer des capteurs d’un type particulier.

L’exemple de code suivant récupère une collection de capteurs du type nommé SAMPLE \_ Sensor \_ type \_ Time. Le code récupère ensuite le premier capteur de la collection par son index.


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByType(SAMPLE_SENSOR_TYPE_TIME, &pSensorColl);
  
if(SUCCEEDED(hr))
{
    ULONG ulCount = 0;

    // Verify that the collection contains
    // at least one sensor.
    hr = pSensorColl->GetCount(&ulCount);

    if(SUCCEEDED(hr))
    {
        if(ulCount < 1)
        {
            wprintf_s(L"\nNo sensors of the requested type.\n");
            hr = E_UNEXPECTED;
        }
    }
}

if(SUCCEEDED(hr))
{
    // Get the first available sensor.
    hr = pSensorColl->GetAt(0, &pSensor);
}
```



Pour récupérer un capteur par son ID, vous devez connaître l’ID unique du capteur. Les capteurs génèrent généralement cet ID lors de la première connexion pour vous permettre d’identifier plusieurs capteurs de la même marque et du même modèle. Cela signifie que vous ne connaissez probablement pas l’ID de capteur à l’avance. Toutefois, si vous avez stocké une copie d’un ID de capteur particulier que vous avez récupéré précédemment, par exemple en appelant [**ISensor :: GetId**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getid), vous souhaiterez peut-être récupérer le même capteur.

L’exemple de code suivant montre comment récupérer un capteur à l’aide de son ID.


```C++
ISensor* pSensor = NULL;

// Get the sensor collection.
hr = pSensorManager->GetSensorByID(SAMPLE_SENSOR_TIME_ID, &pSensor);

```



Vous pouvez également récupérer des capteurs lorsqu’ils sont disponibles en recevant un événement à partir du gestionnaire de capteurs. Pour plus d’informations, consultez [**ISensorManager :: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ISensorManagerEvents::OnSensorEnter**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanagerevents-onsensorenter)
</dt> </dl>

 

 
