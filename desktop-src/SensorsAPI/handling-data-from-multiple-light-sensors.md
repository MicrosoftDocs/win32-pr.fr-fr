---
description: Utilisation des données de capteur de lumière
ms.assetid: 98272df5-08c0-4392-a74b-2919bbdcb022
title: Utilisation des données de capteur de lumière
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ccf1c032b4100174afd6073d8c43db27bce3892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521891"
---
# <a name="using-light-sensor-data"></a>Utilisation des données de capteur de lumière

Il existe deux méthodes recommandées pour interpréter et utiliser des données en Lux provenant de capteurs de lumière ambiante.

-   Appliquez une transformation aux données afin que le niveau de lumière normalisée puisse être utilisé en proportion directe des comportements de programme ou des interactions. Un exemple consiste à faire varier la taille d’un bouton dans votre programme en proportion directe des données normalisées (ou d’une plage de données normalisées, qui correspond à l’extérieur, par exemple). Cette approche offre une implémentation optimale.
-   Traitez les plages de données en lux et mappez les comportements et les réactions des programmes aux seuils supérieur et inférieur de ces plages de données en lux. Il s’agit d’un moyen simple de répondre aux conditions d’éclairage et peut ne pas produire l’expérience utilisateur optimale. Toutefois, cette approche fonctionne correctement si les transitions lisses ne sont pas réalisables.

## <a name="handling-data-from-multiple-light-sensors"></a>Gestion de données à partir de plusieurs capteurs de lumière

Pour obtenir une approximation précise des conditions d’éclairage actuelles, vous pouvez utiliser les données de plusieurs capteurs de lumière ambiante. Étant donné que les capteurs de lumière ambiante peuvent être partiellement ou entièrement obscurcis par des ombres ou des objets qui couvrent le capteur, plusieurs capteurs placés à distance peuvent fournir une meilleure approximation des conditions d’éclairage actuelles par rapport à un seul capteur.

Pour effectuer le suivi des données provenant de plusieurs capteurs, vous pouvez utiliser les deux techniques suivantes :

-   La valeur de données la plus récente pour chaque capteur de lumière ambiante peut être conservée, ainsi que l’horodatage du rapport de données de capteur pour chacune de ces lectures. Le dernier [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) reçu pour chaque lecture de capteur a pu être conservé et peut fournir les deux valeurs pour une référence ultérieure. En faisant référence à l’horodatage de chaque rapport de données de capteur, les données peuvent être gérées en fonction de leur ancienneté. Par exemple, si les données sont âgées de plus de 2 secondes, elles peuvent être omises. En fonction des valeurs de données de capteur les plus récentes, la lecture la plus élevée peut être utilisée, car le capteur correspondant est supposé ne pas être masqué.
-   Vous pouvez utiliser la dernière valeur de capteur d’éclairage ambiant signalée. Cette implémentation n’est pas optimale, car les valeurs de plusieurs capteurs ne sont pas comparées les unes aux autres pour obtenir le résultat le plus précis. Nous déconseillons cette méthode.

## <a name="example-code"></a>Exemple de code

L’exemple de code suivant illustre une implémentation de l’événement [**OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) . Le gestionnaire d’événements appelle une fonction d’assistance, nommée **UpdateUI**, qui modifie l’interface utilisateur en fonction de la valeur de Lux. L’écriture de l’implémentation de UpdateUI dépend de vous.


```C++
// Override of ISensorEvents::OnDataUpdated
// Part of an event sink implementation for ISensorEvents
STDMETHODIMP CALSEventSink::OnDataUpdated(
    ISensor* pSensor, 
    ISensorDataReport* pNewData)
{
    HRESULT hr = S_OK;
   
    if(pSensor == NULL ||
       pNewData == NULL)
    {
         return E_POINTER;
    }

    // Declare and initialize the PROPVARIANT
    PROPVARIANT lightLevel;
    PropVariantInit(&lightLevel);

    // Get the sensor reading from the ISensorDataReport object
    hr = pNewData->GetSensorValue(
        SENSOR_DATA_TYPE_LIGHT_LEVEL_LUX, 
        &lightLevel);

    if(SUCCEEDED(hr))
    {
        if(lightlevel.vt == VT_R4)
        {
            // Extract the float value from the PROPVARIANT object
            float luxValue = lightLevel.fltVal;

            // Normalize the light sensor data
            double lightNormalized = ::log10(luxValue) / 5.0;

            // Handle UI changes based on the normalized LUX data
            // which ranges from 0.0 - 1.0 for a lux range of 
            // 0 lux to 100,000 lux. 
            UpdateUI(lightNormalized);
        }
    }

    // Release the variant.     
    PropVariantClear(&lightLevel);

    return hr;
}
```



 

 
