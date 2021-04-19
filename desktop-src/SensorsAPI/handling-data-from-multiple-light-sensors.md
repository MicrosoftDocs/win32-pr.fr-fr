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
# <a name="using-light-sensor-data"></a><span data-ttu-id="723e9-103">Utilisation des données de capteur de lumière</span><span class="sxs-lookup"><span data-stu-id="723e9-103">Using Light Sensor Data</span></span>

<span data-ttu-id="723e9-104">Il existe deux méthodes recommandées pour interpréter et utiliser des données en Lux provenant de capteurs de lumière ambiante.</span><span class="sxs-lookup"><span data-stu-id="723e9-104">There are two recommended ways of interpreting and using lux data that comes from ambient light sensors.</span></span>

-   <span data-ttu-id="723e9-105">Appliquez une transformation aux données afin que le niveau de lumière normalisée puisse être utilisé en proportion directe des comportements de programme ou des interactions.</span><span class="sxs-lookup"><span data-stu-id="723e9-105">Apply a transform to the data so that the normalized light level can be used in direct proportion to program behaviors or interactions.</span></span> <span data-ttu-id="723e9-106">Un exemple consiste à faire varier la taille d’un bouton dans votre programme en proportion directe des données normalisées (ou d’une plage de données normalisées, qui correspond à l’extérieur, par exemple).</span><span class="sxs-lookup"><span data-stu-id="723e9-106">An example would be to vary the size of a button in your program in direct proportion to the normalized data (or a range of the normalized data, corresponding to outdoors, for example).</span></span> <span data-ttu-id="723e9-107">Cette approche offre une implémentation optimale.</span><span class="sxs-lookup"><span data-stu-id="723e9-107">This approach gives the optimal implementation.</span></span>
-   <span data-ttu-id="723e9-108">Traitez les plages de données en lux et mappez les comportements et les réactions des programmes aux seuils supérieur et inférieur de ces plages de données en lux.</span><span class="sxs-lookup"><span data-stu-id="723e9-108">Deal with ranges of lux data, and map program behaviors and reactions to the upper and lower thresholds of these ranges of lux data.</span></span> <span data-ttu-id="723e9-109">Il s’agit d’un moyen simple de répondre aux conditions d’éclairage et peut ne pas produire l’expérience utilisateur optimale.</span><span class="sxs-lookup"><span data-stu-id="723e9-109">This is a simple way to respond to lighting conditions and may not yield the optimal user experience.</span></span> <span data-ttu-id="723e9-110">Toutefois, cette approche fonctionne correctement si les transitions lisses ne sont pas réalisables.</span><span class="sxs-lookup"><span data-stu-id="723e9-110">However, this approach works fine if smooth transitions are not feasible.</span></span>

## <a name="handling-data-from-multiple-light-sensors"></a><span data-ttu-id="723e9-111">Gestion de données à partir de plusieurs capteurs de lumière</span><span class="sxs-lookup"><span data-stu-id="723e9-111">Handling Data from Multiple Light Sensors</span></span>

<span data-ttu-id="723e9-112">Pour obtenir une approximation précise des conditions d’éclairage actuelles, vous pouvez utiliser les données de plusieurs capteurs de lumière ambiante.</span><span class="sxs-lookup"><span data-stu-id="723e9-112">To produce the most accurate approximation of the current lighting conditions, you can use data from multiple ambient light sensors.</span></span> <span data-ttu-id="723e9-113">Étant donné que les capteurs de lumière ambiante peuvent être partiellement ou entièrement obscurcis par des ombres ou des objets qui couvrent le capteur, plusieurs capteurs placés à distance peuvent fournir une meilleure approximation des conditions d’éclairage actuelles par rapport à un seul capteur.</span><span class="sxs-lookup"><span data-stu-id="723e9-113">Because ambient light sensors can be partly or fully obscured by shadows or objects that cover the sensor, multiple sensors placed some distance apart can provide a much better approximation of the current lighting conditions than a single sensor.</span></span>

<span data-ttu-id="723e9-114">Pour effectuer le suivi des données provenant de plusieurs capteurs, vous pouvez utiliser les deux techniques suivantes :</span><span class="sxs-lookup"><span data-stu-id="723e9-114">To keep track of the data coming from multiple sensors, you can use the following two techniques:</span></span>

-   <span data-ttu-id="723e9-115">La valeur de données la plus récente pour chaque capteur de lumière ambiante peut être conservée, ainsi que l’horodatage du rapport de données de capteur pour chacune de ces lectures.</span><span class="sxs-lookup"><span data-stu-id="723e9-115">The most recent data value for each ambient light sensor can be retained, along with the time stamp from the sensor data report for each of these readings.</span></span> <span data-ttu-id="723e9-116">Le dernier [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) reçu pour chaque lecture de capteur a pu être conservé et peut fournir les deux valeurs pour une référence ultérieure.</span><span class="sxs-lookup"><span data-stu-id="723e9-116">The last [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) received for each sensor reading could be retained and could provide both values for later reference.</span></span> <span data-ttu-id="723e9-117">En faisant référence à l’horodatage de chaque rapport de données de capteur, les données peuvent être gérées en fonction de leur ancienneté.</span><span class="sxs-lookup"><span data-stu-id="723e9-117">By referring to the time stamp for each sensor data report, the data can be managed based on its age.</span></span> <span data-ttu-id="723e9-118">Par exemple, si les données sont âgées de plus de 2 secondes, elles peuvent être omises.</span><span class="sxs-lookup"><span data-stu-id="723e9-118">For example, if the data is more than 2 seconds old, it could be omitted.</span></span> <span data-ttu-id="723e9-119">En fonction des valeurs de données de capteur les plus récentes, la lecture la plus élevée peut être utilisée, car le capteur correspondant est supposé ne pas être masqué.</span><span class="sxs-lookup"><span data-stu-id="723e9-119">Based on the newer sensor data values, the highest reading could be used because the corresponding sensor would be presumed not to be obscured.</span></span>
-   <span data-ttu-id="723e9-120">Vous pouvez utiliser la dernière valeur de capteur d’éclairage ambiant signalée.</span><span class="sxs-lookup"><span data-stu-id="723e9-120">You can use the last ambient light sensor value reported.</span></span> <span data-ttu-id="723e9-121">Cette implémentation n’est pas optimale, car les valeurs de plusieurs capteurs ne sont pas comparées les unes aux autres pour obtenir le résultat le plus précis.</span><span class="sxs-lookup"><span data-stu-id="723e9-121">This implementation would not be optimal because the values from multiple sensors are not compared to one another to obtain the most accurate result.</span></span> <span data-ttu-id="723e9-122">Nous déconseillons cette méthode.</span><span class="sxs-lookup"><span data-stu-id="723e9-122">We do not recommend this method.</span></span>

## <a name="example-code"></a><span data-ttu-id="723e9-123">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="723e9-123">Example Code</span></span>

<span data-ttu-id="723e9-124">L’exemple de code suivant illustre une implémentation de l’événement [**OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) .</span><span class="sxs-lookup"><span data-stu-id="723e9-124">The following example code shows an implementation for the [**OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) event.</span></span> <span data-ttu-id="723e9-125">Le gestionnaire d’événements appelle une fonction d’assistance, nommée **UpdateUI**, qui modifie l’interface utilisateur en fonction de la valeur de Lux.</span><span class="sxs-lookup"><span data-stu-id="723e9-125">The event handler calls a helper function, named **UpdateUI**, that changes the user interface based on the lux value.</span></span> <span data-ttu-id="723e9-126">L’écriture de l’implémentation de UpdateUI dépend de vous.</span><span class="sxs-lookup"><span data-stu-id="723e9-126">Writing the implementation of UpdateUI is up to you.</span></span>


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



 

 
