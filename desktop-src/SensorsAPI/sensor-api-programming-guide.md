---
description: Cette section fournit des informations, y compris des exemples de code, sur l’utilisation des fonctionnalités de l’API de capteur. Pour obtenir des informations générales sur les différentes interfaces de programmation, consultez à propos de l’API de capteur.
ms.assetid: 4c2ffd22-49ee-4318-bfa0-e0ce4d8c67bb
title: Guide de programmation de l’API de capteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5886564e66a0a8db64713b280b44f85a197430dc23523266bc45e66e44c956b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073239"
---
# <a name="sensor-api-programming-guide"></a>Guide de programmation de l’API de capteur

Cette section fournit des informations, y compris des exemples de code, sur l’utilisation des fonctionnalités de l’API de capteur. Pour obtenir des informations générales sur les différentes interfaces de programmation, consultez [à propos de l’API de capteur](about-the-sensor-api.md).

L’exemple de code dans cette section utilise les en-têtes include supplémentaires suivants.


```C++
#include <windows.h>
#include <initguid.h>
#include <propkeydef.h>


#include <iostream>
#include <propvarutil.h>
#include <functiondiscoverykeys.h>
#include <assert.h>
```





Vous devez également créer un lien vers ces fichiers de bibliothèque associés supplémentaires : propsys. lib et PortableDeviceGuids. lib.

L’exemple de code dans cette section utilise les constantes suivantes pour les catégories de capteurs, les types et les champs de données. ces constantes sont des valeurs personnalisées définies par l’exemple de pilote TimeSensor dans le Kit de pilotes Windows. Notez que, bien que la plateforme de capteur permette de définir et d’utiliser des types personnalisés tels que ceux-là, vous devez utiliser des types définis par la plateforme dans la mesure du possible.


```C++
// Define an object ID.
// {0D77BEE3-7169-42bf-8379-28F9A9B59A57}
DEFINE_GUID(SAMPLE_SENSOR_TIME_ID, 
0xd77bee3, 0x7169, 0x42bf, 0x83, 0x79, 0x28, 0xf9, 0xa9, 0xb5, 0x9a, 0x57);

// Define a custom category.
// {062A5C3B-44C1-4ad1-8EFC-0F65B2E4AD48}
DEFINE_GUID(SAMPLE_SENSOR_CATEGORY_DATE_TIME, 
0x62a5c3b, 0x44c1, 0x4ad1, 0x8e, 0xfc, 0xf, 0x65, 0xb2, 0xe4, 0xad, 0x48);

// Define a custom type.
// {5F199A84-409F-4e35-B2DD-F9C79F5318A0}
DEFINE_GUID(SAMPLE_SENSOR_TYPE_TIME, 
0x5f199a84, 0x409f, 0x4e35, 0xb2, 0xdd, 0xf9, 0xc7, 0x9f, 0x53, 0x18, 0xa0);

// Time sensor fields.
// Because these are related, each field uses the same GUID, but changes the PID.
// {340946F2-9A77-42b0-8176-57D4DF00E5CA}
DEFINE_PROPERTYKEY(SAMPLE_SENSOR_DATA_TYPE_HOUR, 
0x340946f2, 0x9a77, 0x42b0, 0x81, 0x76, 0x57, 0xd4, 0xdf, 0x0, 0xe5, 0xca, PID_FIRST_USABLE); // PID = 2

DEFINE_PROPERTYKEY(SAMPLE_SENSOR_DATA_TYPE_MINUTE, 
0x340946f2, 0x9a77, 0x42b0, 0x81, 0x76, 0x57, 0xd4, 0xdf, 0x0, 0xe5, 0xca, PID_FIRST_USABLE + 1); // PID = 3

DEFINE_PROPERTYKEY(SAMPLE_SENSOR_DATA_TYPE_SECOND, 
0x340946f2, 0x9a77, 0x42b0, 0x81, 0x76, 0x57, 0xd4, 0xdf, 0x0, 0xe5, 0xca, PID_FIRST_USABLE + 2); // PID = 4
```



L’exemple de code dans cette section utilise les variables suivantes.


```C++
HRESULT hr = S_OK;

// Sensor interface pointers
ISensorManager* pSensorManager = NULL;    
ISensorCollection* pSensorColl = NULL;
ISensor* pSensor = NULL; 
ISensorDataReport* pReport = NULL;

// Time sensor data field variables
ULONG ulHour, ulMinute, ulSecond = 0;

```



L’exemple de code dans cette section utilise la fonction suivante pour libérer des pointeurs d’interface COM.


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



## <a name="in-this-section"></a>Dans cette section

-   [Récupération d’un objet capteur](retrieving-a-sensor.md)
-   [Demande d’autorisations utilisateur](requesting-user-permissions.md)
-   [Récupération et définition des propriétés de capteur](setting-and-retrieving-sensor-properties.md)
-   [Recherche des champs de données de capteur pris en charge](checking-for-supported-sensor-data-fields.md)
-   [Utilisation d’événements d’API de capteur](using-sensor-api-events.md)
-   [Récupération des valeurs de données de capteur](retrieving-sensor-data-fields.md)
-   [Récupération des types de vecteurs](retrieving-vector-types.md)
-   [Utilisation de capteurs logiques](using-logical-sensors.md)
-   [Création d' Light-Aware interfaces utilisateur](creating-light-aware-user-interfaces.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de l’API de capteur](about-the-sensor-api.md)
</dt> </dl>

 

 



