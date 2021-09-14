---
description: Utilisez les éléments de programmation de l’alimentation de l’appareil pour gérer la façon dont les appareils s’exécutent lorsque le système est en état de veille.
ms.assetid: 44479f5d-2e92-4802-a633-3e0bb7d61e94
title: Utilisation de l’API Power de l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cabd7a54efc0979360a863dc9c0cf16d69d8d22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119081"
---
# <a name="using-the-device-power-api"></a>Utilisation de l’API Power de l’appareil

Utilisez les éléments de programmation de l’alimentation de l’appareil pour gérer la façon dont les appareils s’exécutent lorsque le système est en état de veille.

## <a name="opening-and-closing-the-device-list"></a>Ouverture et fermeture de la liste des appareils

L’ouverture et la fermeture de la liste des appareils sont un processus coûteux en termes de temps processeur. Les fonctions [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) et [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) ne sont nécessaires que si l’application doit interroger plusieurs fois la liste d’appareils.

Si [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) est appelé, [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) doit être appelé lorsque les requêtes de la liste des appareils sont terminées. [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) et [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) ne ferment pas la liste des appareils s’ils ont été explicitement ouverts par **DevicePowerOpen**.

## <a name="enumerating-devices"></a>Énumération des appareils

La fonction [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) détecte si la liste des appareils est ouverte et, dans le cas contraire, l’ouvre. **DevicePowerEnumDevices** énumère les appareils en fonction des critères de recherche spécifiés. Si la liste d’appareils a été ouverte par la fonction, elle est fermée avant le retour de la fonction.

## <a name="enabling-and-disabling-a-device-from-waking-the-system"></a>Activation et désactivation d’un appareil à partir du réveil du système

La fonction [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) , similaire à [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices), détecte si la liste des appareils est ouverte et, dans le cas contraire, l’ouvre. **DevicePowerSetDeviceState** définit ensuite les critères spécifiés pour l’appareil spécifié. Si la liste d’appareils a été ouverte par la fonction, elle est fermée avant le retour de la fonction.

## <a name="example-code"></a>Exemple de code

L’exemple suivant illustre l’utilisation de l’API Power de l’appareil.


```C++
#define _WIN32_WINNT 0x0600
#include <Windows.h>
#include <PowrProf.h>
#include <stdio.h>
#include <tchar.h>

#pragma comment(lib, "PowrProf.lib")

int __cdecl main()
{
 // Define and initialize our return variables.
 LPWSTR  pRetBuf = NULL;
 ULONG bufSize = MAX_PATH * sizeof(WCHAR);
 ULONG uIndex = 0;
 BOOLEAN bRet = FALSE;

 // Open the device list, querying all devices
 if (!DevicePowerOpen(0)) 
  {
   printf("ERROR: The device database failed to initialize.\n");
   return FALSE;
  }

 // Enumerate the device list, searching for devices that support 
 // waking from either the S1 or S2 sleep state and are currently 
 // present in the system, and not devices that have drivers 
 // installed but are not currently attached to the system, such as 
 // in a laptop docking station.

 pRetBuf = (LPWSTR)LocalAlloc(LPTR, bufSize);

 while (NULL != pRetBuf && 
        0 != (bRet = DevicePowerEnumDevices(uIndex,
           DEVICEPOWER_FILTER_DEVICES_PRESENT,
           PDCAP_WAKE_FROM_S1_SUPPORTED|PDCAP_WAKE_FROM_S2_SUPPORTED,
           (PBYTE)pRetBuf,
           &bufSize)))
  {
   printf("Device name: %S\n", pRetBuf);

   // For the devices we found that have support for waking from 
   // S1 and S2 sleep states, disable them from waking the system.
   bRet = (0 != DevicePowerSetDeviceState((LPCWSTR)pRetBuf, 
                                  DEVICEPOWER_CLEAR_WAKEENABLED, 
                                  NULL));

   if (0 != bRet) 
    {
     printf("Warning: Failed to set device state.\n");
    }
   uIndex++;
  }

 // Close the device list.
 DevicePowerClose();
 if (pRetBuf!= NULL) LocalFree(pRetBuf);
 pRetBuf = NULL;

 return TRUE;
}
```



Dans cet exemple, la liste des appareils est ouverte une seule fois et fermée une fois. Si les fonctions [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) et [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) n’ont pas été appelées, la liste des appareils a été ouverte et fermée par chaque appel à [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) et [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate). En utilisant **DevicePowerOpen** et **DevicePowerClose** , nous avons enregistré l’ouverture de la liste des appareils deux fois plus souvent.

 

 



