---
title: Annulation d’une connexion réseau
description: Pour annuler une connexion à une ressource réseau, une application peut appeler la fonction WNetCancelConnection2, comme indiqué dans l’exemple suivant.
ms.assetid: a1c80222-4986-4c51-86a5-a1caacb4b2fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22cc5fb9536a5d073a6c99d8b49a00e3c2771546
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842578"
---
# <a name="canceling-a-network-connection"></a><span data-ttu-id="6851b-103">Annulation d’une connexion réseau</span><span class="sxs-lookup"><span data-stu-id="6851b-103">Canceling a Network Connection</span></span>

<span data-ttu-id="6851b-104">Pour annuler une connexion à une ressource réseau, une application peut appeler la fonction [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) , comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="6851b-104">To cancel a connection to a network resource, an application can call the [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) function, as shown in the following example.</span></span>

<span data-ttu-id="6851b-105">L’appel à **WNetCancelConnection2** spécifie qu’une connexion réseau ne doit plus être persistante.</span><span class="sxs-lookup"><span data-stu-id="6851b-105">The call to **WNetCancelConnection2** specifies that a network connection should no longer be persistent.</span></span> <span data-ttu-id="6851b-106">L’exemple appelle un gestionnaire d’erreurs défini par l’application pour traiter les erreurs et la fonction [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) pour l’impression.</span><span class="sxs-lookup"><span data-stu-id="6851b-106">The sample calls an application-defined error handler to process errors, and the [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) function for printing.</span></span>


```C++
DWORD dwResult; 
 
// Call the WNetCancelConnection2 function, specifying
//  that the connection should no longer be a persistent one.
//
dwResult = WNetCancelConnection2("z:", 
    CONNECT_UPDATE_PROFILE, // remove connection from profile 
    FALSE);                 // fail if open files or jobs 
 
// Process errors.
//  The device is not a local redirected device.
//
if (dwResult == ERROR_NOT_CONNECTED) 
{ 
    printf("Drive z: not connected.\n"); 
    return dwResult; 
} 
 
// Call an application-defined error handler.
//
else if(dwResult != NO_ERROR) 
{ 
    printf("WNetCancelConnection2 failed.\n"); 
    return dwResult; 
}
//
// Otherwise, report canceling the connection.
//
printf("Connection closed for z: drive.\n"); 
```



<span data-ttu-id="6851b-107">La fonction [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) est prise en charge pour la compatibilité avec les versions antérieures de Windows pour les groupes de travail.</span><span class="sxs-lookup"><span data-stu-id="6851b-107">The [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) function is supported for compatibility with earlier versions of Windows for Workgroups.</span></span> <span data-ttu-id="6851b-108">Pour les nouvelles applications, utilisez [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).</span><span class="sxs-lookup"><span data-stu-id="6851b-108">For new applications, use [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).</span></span>

<span data-ttu-id="6851b-109">Pour plus d’informations sur l’utilisation d’un gestionnaire d’erreurs défini par l’application, consultez [récupération des erreurs réseau](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="6851b-109">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 