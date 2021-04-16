---
description: Certaines propriétés et certains champs de données contiennent des tableaux d’informations.
ms.assetid: 85e3b953-be36-4d60-b04e-4f572d0b9564
title: Récupération des types de vecteurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4945b45e4e78b6c4f9f9e0fb4b3848f813549105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525653"
---
# <a name="retrieving-vector-types"></a><span data-ttu-id="3fe1c-103">Récupération des types de vecteurs</span><span class="sxs-lookup"><span data-stu-id="3fe1c-103">Retrieving Vector Types</span></span>

<span data-ttu-id="3fe1c-104">Certaines propriétés et certains champs de données contiennent des tableaux d’informations.</span><span class="sxs-lookup"><span data-stu-id="3fe1c-104">Some properties and data fields contain arrays of information.</span></span> <span data-ttu-id="3fe1c-105">Par exemple, la propriété \_ \_ de la \_ courbe de réponse légère de la propriété de capteur \_ contient un tableau d’entiers non signés de 4 octets.</span><span class="sxs-lookup"><span data-stu-id="3fe1c-105">For example, the SENSOR\_PROPERTY\_LIGHT\_RESPONSE\_CURVE property contains an array of 4-byte unsigned integers.</span></span> <span data-ttu-id="3fe1c-106">Toutefois, lorsque vous recevez ces tableaux via l’API de capteur, ils sont toujours représentés en tant que type VT \_ Vector \| UI1, un tableau de caractères codés sur un octet, quel que soit le type réel des données dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="3fe1c-106">However, when you receive such arrays through the Sensor API, they are always represented as type VT\_VECTOR\|UI1, an array of single-byte characters, regardless of the actual type of the data in the array.</span></span> <span data-ttu-id="3fe1c-107">Pour ces types, vous devez veiller à convertir les variables de tableau en type de données correct pour la propriété ou le champ de données.</span><span class="sxs-lookup"><span data-stu-id="3fe1c-107">For these types, you must be careful to cast array variables to the correct data type for the property or data field.</span></span>

<span data-ttu-id="3fe1c-108">Pour plus d’informations sur les propriétés, les champs de données et leurs types, consultez [constantes](constants.md).</span><span class="sxs-lookup"><span data-stu-id="3fe1c-108">For information about properties, data fields, and their types, see [Constants](constants.md).</span></span>

<span data-ttu-id="3fe1c-109">L’exemple de code suivant montre comment effectuer un cast des données récupérées dans \_ \_ \_ la courbe de réponse claire de la propriété du capteur \_ vers le type approprié.</span><span class="sxs-lookup"><span data-stu-id="3fe1c-109">The following example code shows how to cast the data retrieved in SENSOR\_PROPERTY\_LIGHT\_RESPONSE\_CURVE to the correct type.</span></span>


```C++
PROPVARIANT pvCurve;
PropVariantInit(&pvCurve);

// Retrieve the property value.
hr = pSensor->GetProperty(SENSOR_PROPERTY_LIGHT_RESPONSE_CURVE, &pvCurve);
if (SUCCEEDED(hr))
{
    if ((VT_UI1|VT_VECTOR) == V_VT(pvCurve)) // Note actual type of UI1
    {
        // Cast the array to UINT, a 4-byte unsigned integer.

        // Item count for the array.
        UINT  cElement = pvCurve.caub.cElems/sizeof(UINT);
        // Array pointer.
        UINT* pElement = (UINT*)(pvCurve.caub.pElems);

        // Use the array.
    }
}

// Remember to free the PROPVARIANT when done.
PropVariantClear(&pvCurve);
```



 

 



