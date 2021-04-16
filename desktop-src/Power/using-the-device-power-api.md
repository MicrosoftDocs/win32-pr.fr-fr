---
description: Utilisez les éléments de programmation de l’alimentation de l’appareil pour gérer la façon dont les appareils s’exécutent lorsque le système est en état de veille.
ms.assetid: 44479f5d-2e92-4802-a633-3e0bb7d61e94
title: Utilisation de l’API Power de l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cabd7a54efc0979360a863dc9c0cf16d69d8d22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529098"
---
# <a name="using-the-device-power-api"></a><span data-ttu-id="405b0-103">Utilisation de l’API Power de l’appareil</span><span class="sxs-lookup"><span data-stu-id="405b0-103">Using the Device Power API</span></span>

<span data-ttu-id="405b0-104">Utilisez les éléments de programmation de l’alimentation de l’appareil pour gérer la façon dont les appareils s’exécutent lorsque le système est en état de veille.</span><span class="sxs-lookup"><span data-stu-id="405b0-104">Use the Device Power programming elements to manage the way devices perform while the system is in a sleep state.</span></span>

## <a name="opening-and-closing-the-device-list"></a><span data-ttu-id="405b0-105">Ouverture et fermeture de la liste des appareils</span><span class="sxs-lookup"><span data-stu-id="405b0-105">Opening and closing the device list</span></span>

<span data-ttu-id="405b0-106">L’ouverture et la fermeture de la liste des appareils sont un processus coûteux en termes de temps processeur.</span><span class="sxs-lookup"><span data-stu-id="405b0-106">Opening and closing the device list is a costly process in terms of CPU time.</span></span> <span data-ttu-id="405b0-107">Les fonctions [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) et [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) ne sont nécessaires que si l’application doit interroger plusieurs fois la liste d’appareils.</span><span class="sxs-lookup"><span data-stu-id="405b0-107">The [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) and [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) functions that do this are only necessary if the application needs to query the device list multiple times.</span></span>

<span data-ttu-id="405b0-108">Si [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) est appelé, [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) doit être appelé lorsque les requêtes de la liste des appareils sont terminées.</span><span class="sxs-lookup"><span data-stu-id="405b0-108">If [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) is called, [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) must be called when device-list queries are complete.</span></span> <span data-ttu-id="405b0-109">[**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) et [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) ne ferment pas la liste des appareils s’ils ont été explicitement ouverts par **DevicePowerOpen**.</span><span class="sxs-lookup"><span data-stu-id="405b0-109">[**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) and [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) will not close the device list if it has been explicitly opened by **DevicePowerOpen**.</span></span>

## <a name="enumerating-devices"></a><span data-ttu-id="405b0-110">Énumération des appareils</span><span class="sxs-lookup"><span data-stu-id="405b0-110">Enumerating devices</span></span>

<span data-ttu-id="405b0-111">La fonction [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) détecte si la liste des appareils est ouverte et, dans le cas contraire, l’ouvre.</span><span class="sxs-lookup"><span data-stu-id="405b0-111">The [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) function detects whether the device list is open, and if not, opens it.</span></span> <span data-ttu-id="405b0-112">**DevicePowerEnumDevices** énumère les appareils en fonction des critères de recherche spécifiés.</span><span class="sxs-lookup"><span data-stu-id="405b0-112">**DevicePowerEnumDevices** enumerates the devices based on the specified search criteria.</span></span> <span data-ttu-id="405b0-113">Si la liste d’appareils a été ouverte par la fonction, elle est fermée avant le retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="405b0-113">If the device list was opened by the function, it is closed before the function returns.</span></span>

## <a name="enabling-and-disabling-a-device-from-waking-the-system"></a><span data-ttu-id="405b0-114">Activation et désactivation d’un appareil à partir du réveil du système</span><span class="sxs-lookup"><span data-stu-id="405b0-114">Enabling and disabling a device from waking the system</span></span>

<span data-ttu-id="405b0-115">La fonction [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) , similaire à [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices), détecte si la liste des appareils est ouverte et, dans le cas contraire, l’ouvre.</span><span class="sxs-lookup"><span data-stu-id="405b0-115">The [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) function, similar to [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices), detects whether the device list is open, and if not, opens it.</span></span> <span data-ttu-id="405b0-116">**DevicePowerSetDeviceState** définit ensuite les critères spécifiés pour l’appareil spécifié.</span><span class="sxs-lookup"><span data-stu-id="405b0-116">**DevicePowerSetDeviceState** then sets the specified criteria for the specified device.</span></span> <span data-ttu-id="405b0-117">Si la liste d’appareils a été ouverte par la fonction, elle est fermée avant le retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="405b0-117">If the device list was opened by the function, it is closed before the function returns.</span></span>

## <a name="example-code"></a><span data-ttu-id="405b0-118">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="405b0-118">Example Code</span></span>

<span data-ttu-id="405b0-119">L’exemple suivant illustre l’utilisation de l’API Power de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="405b0-119">The following example demonstrates the use of the Device Power API.</span></span>


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



<span data-ttu-id="405b0-120">Dans cet exemple, la liste des appareils est ouverte une seule fois et fermée une fois.</span><span class="sxs-lookup"><span data-stu-id="405b0-120">In this example the device list is opened once, and closed once.</span></span> <span data-ttu-id="405b0-121">Si les fonctions [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) et [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) n’ont pas été appelées, la liste des appareils a été ouverte et fermée par chaque appel à [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) et [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate).</span><span class="sxs-lookup"><span data-stu-id="405b0-121">If the [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) and [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) functions were not called, the device list would have been opened and closed by each call to [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) and [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate).</span></span> <span data-ttu-id="405b0-122">En utilisant **DevicePowerOpen** et **DevicePowerClose** , nous avons enregistré l’ouverture de la liste des appareils deux fois plus souvent.</span><span class="sxs-lookup"><span data-stu-id="405b0-122">By using **DevicePowerOpen** and **DevicePowerClose** we saved opening the device list two unnecessary times.</span></span>

 

 



