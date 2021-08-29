---
description: Certaines propriétés et certains champs de données contiennent des tableaux d’informations.
ms.assetid: 85e3b953-be36-4d60-b04e-4f572d0b9564
title: Récupération des types de vecteurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15579d7067d0eafba0d181d8e8845dfa1bd78b060fb5fba8b08f196d2107d3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739459"
---
# <a name="retrieving-vector-types"></a>Récupération des types de vecteurs

Certaines propriétés et certains champs de données contiennent des tableaux d’informations. Par exemple, la propriété \_ \_ de la \_ courbe de réponse légère de la propriété de capteur \_ contient un tableau d’entiers non signés de 4 octets. Toutefois, lorsque vous recevez ces tableaux via l’API de capteur, ils sont toujours représentés en tant que type VT \_ Vector \| UI1, un tableau de caractères codés sur un octet, quel que soit le type réel des données dans le tableau. Pour ces types, vous devez veiller à convertir les variables de tableau en type de données correct pour la propriété ou le champ de données.

Pour plus d’informations sur les propriétés, les champs de données et leurs types, consultez [constantes](constants.md).

L’exemple de code suivant montre comment effectuer un cast des données récupérées dans \_ \_ \_ la courbe de réponse claire de la propriété du capteur \_ vers le type approprié.


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



 

 



