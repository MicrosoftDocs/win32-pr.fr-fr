---
title: Récupération du nom d’utilisateur
description: Pour récupérer le nom de l’utilisateur associé soit avec un appareil local connecté à une ressource réseau, soit avec le nom d’un réseau, une application peut appeler la fonction WNetGetUser.
ms.assetid: aed410af-d5f0-4389-882b-5b4338b5f900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0aeb8df11187828be0865d6b73e08325f2e0e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199313"
---
# <a name="retrieving-the-user-name"></a><span data-ttu-id="3de37-103">Récupération du nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="3de37-103">Retrieving the User Name</span></span>

<span data-ttu-id="3de37-104">Pour récupérer le nom de l’utilisateur associé soit avec un appareil local connecté à une ressource réseau, soit avec le nom d’un réseau, une application peut appeler la fonction [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) .</span><span class="sxs-lookup"><span data-stu-id="3de37-104">To retrieve the name of the user associated either with a local device connected to a network resource or with the name of a network, an application can call the [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) function.</span></span>

<span data-ttu-id="3de37-105">L’exemple suivant utilise le nom de l’appareil pour récupérer le nom de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3de37-105">The following example uses the device name to retrieve the name of the user.</span></span> <span data-ttu-id="3de37-106">L’exemple appelle un gestionnaire d’erreurs défini par l’application pour traiter les erreurs et la fonction [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) pour l’impression.</span><span class="sxs-lookup"><span data-stu-id="3de37-106">The sample calls an application-defined error handler to process errors, and the [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) function for printing.</span></span>


```C++
CHAR szUserName[80]; 
DWORD dwResult, cchBuff = 80; 
 
// Call the WNetGetUser function.
//
dwResult = WNetGetUser("z:", 
    (LPSTR) szUserName, 
    &cchBuff); 
 
// If the call succeeds, print the user name.
//
if(dwResult == NO_ERROR) 
    printf("User name: %s\n", szUserName); 
 
// Handle the error.
//
else 
{ 
    printf("WNetGetUser failed.\n"); 
}
```



<span data-ttu-id="3de37-107">Pour plus d’informations sur l’utilisation d’un gestionnaire d’erreurs défini par l’application, consultez [récupération des erreurs réseau](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="3de37-107">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 