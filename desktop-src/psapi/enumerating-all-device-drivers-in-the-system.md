---
title: Énumération de tous les pilotes de périphérique dans le système
description: L’exemple de code suivant utilise la fonction EnumDeviceDrivers pour énumérer les pilotes de périphérique actuels dans le système.
ms.assetid: 047d8541-e17e-4738-8453-674db69365df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7b02345f5d59979fe3576fd952c056ca808e6ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939772"
---
# <a name="enumerating-all-device-drivers-in-the-system"></a><span data-ttu-id="965d2-103">Énumération de tous les pilotes de périphérique dans le système</span><span class="sxs-lookup"><span data-stu-id="965d2-103">Enumerating All Device Drivers in the System</span></span>

<span data-ttu-id="965d2-104">L’exemple de code suivant utilise la fonction [**EnumDeviceDrivers**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) pour énumérer les pilotes de périphérique actuels dans le système.</span><span class="sxs-lookup"><span data-stu-id="965d2-104">The following sample code uses the [**EnumDeviceDrivers**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) function to enumerate the current device drivers in the system.</span></span> <span data-ttu-id="965d2-105">Elle transmet les adresses de chargement récupérées à partir de cet appel de fonction à la fonction [**GetDeviceDriverBaseName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea) pour récupérer un nom qui peut être affiché.</span><span class="sxs-lookup"><span data-stu-id="965d2-105">It passes the load addresses retrieved from this function call to the [**GetDeviceDriverBaseName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea) function to retrieve a name that can be displayed.</span></span>


```C++
#include <windows.h>
#include <psapi.h>
#include <tchar.h>
#include <stdio.h>

// To ensure correct resolution of symbols, add Psapi.lib to TARGETLIBS
// and compile with -DPSAPI_VERSION=1

#define ARRAY_SIZE 1024

int main( void )
{
   LPVOID drivers[ARRAY_SIZE];
   DWORD cbNeeded;
   int cDrivers, i;

   if( EnumDeviceDrivers(drivers, sizeof(drivers), &cbNeeded) && cbNeeded < sizeof(drivers))
   { 
      TCHAR szDriver[ARRAY_SIZE];

      cDrivers = cbNeeded / sizeof(drivers[0]);

      _tprintf(TEXT("There are %d drivers:\n"), cDrivers);      
      for (i=0; i < cDrivers; i++ )
      {
         if(GetDeviceDriverBaseName(drivers[i], szDriver, sizeof(szDriver) /              sizeof(szDriver[0])))
         {
            _tprintf(TEXT("%d: %s\n"), i+1, szDriver);
         }
      }
   }
   else 
   {
        _tprintf(TEXT("EnumDeviceDrivers failed; array size needed is %d\n"),             cbNeeded / sizeof(LPVOID));
        return 1;
   }

return 0;
}
```



 

 




