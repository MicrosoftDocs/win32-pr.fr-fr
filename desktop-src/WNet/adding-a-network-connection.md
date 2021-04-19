---
title: Ajout d’une connexion réseau
description: Pour établir une connexion à une ressource réseau décrite par une structure Resource, une application peut appeler WNetAddConnection2, WNetAddConnection3 ou la fonction WnetUseConnection.
ms.assetid: 0dab9eed-9019-4075-833b-324e5caee257
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 476e03193b919f17a2060e415db5e7ea60c8364e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106541158"
---
# <a name="adding-a-network-connection"></a><span data-ttu-id="cbfcc-103">Ajout d’une connexion réseau</span><span class="sxs-lookup"><span data-stu-id="cbfcc-103">Adding a Network Connection</span></span>

<span data-ttu-id="cbfcc-104">Pour établir une connexion à une ressource réseau décrite par une structure [**Resource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) , une application peut appeler [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a), [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)ou la fonction [**WnetUseConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona) .</span><span class="sxs-lookup"><span data-stu-id="cbfcc-104">To make a connection to a network resource described by a [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structure, an application can call the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a), the [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a), or the [**WNetUseConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona) function.</span></span> <span data-ttu-id="cbfcc-105">L’exemple suivant illustre l’utilisation de la fonction **WNetAddConnection2** .</span><span class="sxs-lookup"><span data-stu-id="cbfcc-105">The following example demonstrates use of the **WNetAddConnection2** function.</span></span>

<span data-ttu-id="cbfcc-106">L’exemple de code appelle la fonction **WNetAddConnection2** , en spécifiant que le système doit mettre à jour le profil de l’utilisateur avec les informations, en créant une connexion « mémorisée » ou persistante.</span><span class="sxs-lookup"><span data-stu-id="cbfcc-106">The code sample calls the **WNetAddConnection2** function, specifying that the system should update the user's profile with the information, creating a "remembered" or persistent connection.</span></span> <span data-ttu-id="cbfcc-107">L’exemple appelle un gestionnaire d’erreurs défini par l’application pour traiter les erreurs et la fonction [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) pour l’impression.</span><span class="sxs-lookup"><span data-stu-id="cbfcc-107">The sample calls an application-defined error handler to process errors, and the [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) function for printing.</span></span>


```C++
DWORD dwResult; 
NETRESOURCE nr; 
//
// Call the WNetAddConnection2 function to make the connection,
//   specifying a persistent connection.
//
dwResult = WNetAddConnection2(&nr, // NETRESOURCE from enumeration 
    (LPSTR) NULL,                  // no password 
    (LPSTR) NULL,                  // logged-in user 
    CONNECT_UPDATE_PROFILE);       // update profile with connect information 
 
// Process errors.
//  The local device is already connected to a network resource.
//
if (dwResult == ERROR_ALREADY_ASSIGNED) 
{ 
    printf("Already connected to specified resource.\n"); 
    return dwResult; 
} 
 
//  An entry for the local device already exists in the user profile.
//
else if (dwResult == ERROR_DEVICE_ALREADY_REMEMBERED) 
{ 
    printf("Attempted reassignment of remembered device.\n"); 
    return dwResult; 
} 
else if(dwResult != NO_ERROR) 
{ 
    //
    // Call an application-defined error handler.
    //
    printf("WNetAddConnection2 failed.\n"); 
    return dwResult; 
} 
 
//
// Otherwise, report a successful connection.
//
printf("Connected to the specified resource.\n"); 
```



<span data-ttu-id="cbfcc-108">La fonction [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) est prise en charge pour la compatibilité avec les versions antérieures de Windows pour les groupes de travail.</span><span class="sxs-lookup"><span data-stu-id="cbfcc-108">The [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) function is supported for compatibility with earlier versions of Windows for Workgroups.</span></span> <span data-ttu-id="cbfcc-109">Les nouvelles applications doivent appeler la fonction [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) ou la fonction [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) .</span><span class="sxs-lookup"><span data-stu-id="cbfcc-109">New applications should call the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) function or the [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) function.</span></span>

<span data-ttu-id="cbfcc-110">Pour plus d’informations sur l’utilisation d’un gestionnaire d’erreurs défini par l’application, consultez [récupération des erreurs réseau](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="cbfcc-110">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 