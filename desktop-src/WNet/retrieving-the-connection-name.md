---
title: Récupération du nom de la connexion
description: Pour récupérer le nom de la ressource réseau associée à un appareil local, une application peut appeler la fonction WNetGetConnection, comme illustré dans l’exemple suivant.
ms.assetid: 7c02cf9a-cca3-47d8-8a4b-f2245f1db92a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ac84aec3c6aafb8a5113ea29251247a1de35aec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101965"
---
# <a name="retrieving-the-connection-name"></a><span data-ttu-id="d5312-103">Récupération du nom de la connexion</span><span class="sxs-lookup"><span data-stu-id="d5312-103">Retrieving the Connection Name</span></span>

<span data-ttu-id="d5312-104">Pour récupérer le nom de la ressource réseau associée à un appareil local, une application peut appeler la fonction [**WNetGetConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetconnectiona) , comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="d5312-104">To retrieve the name of the network resource associated with a local device, an application can call the [**WNetGetConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetconnectiona) function, as shown in the following sample.</span></span>

<span data-ttu-id="d5312-105">L’exemple suivant appelle un gestionnaire d’erreurs défini par l’application pour traiter les erreurs et la fonction [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) pour l’impression.</span><span class="sxs-lookup"><span data-stu-id="d5312-105">The following sample calls an application-defined error handler to process errors, and the [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) function for printing.</span></span>


```C++
TCHAR szDeviceName[80]; 
DWORD dwResult, cchBuff = sizeof(szDeviceName); 
 
// Call the WNetGetConnection function.
//
dwResult = WNetGetConnection(_T("z:"), 
    szDeviceName, 
    &cchBuff); 
 
switch (dwResult) 
{ 
    //
    // Print the connection name or process errors.
    //
    case NO_ERROR: 
        printf("Connection name: %s\n", szDeviceName); 
        break; 
    //
    // The device is not a redirected device.
    //
    case ERROR_NOT_CONNECTED: 
        printf("Device z: not connected.\n"); 
        break;
    //
    // The device is not currently connected, but it is a persistent connection.
    //
    case ERROR_CONNECTION_UNAVAIL: 
        printf("Connection unavailable.\n"); 
        break;
    //
    // Handle the error.
    //
    default: 
        printf("WNetGetConnection failed.\n"); 
}
```



<span data-ttu-id="d5312-106">Pour plus d’informations sur l’utilisation d’un gestionnaire d’erreurs défini par l’application, consultez [récupération des erreurs réseau](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="d5312-106">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 