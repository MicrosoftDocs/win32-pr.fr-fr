---
title: Annulation d’une connexion réseau
description: Pour annuler une connexion à une ressource réseau, une application peut appeler la fonction WNetCancelConnection2, comme indiqué dans l’exemple suivant.
ms.assetid: a1c80222-4986-4c51-86a5-a1caacb4b2fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22cc5fb9536a5d073a6c99d8b49a00e3c2771546
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311077"
---
# <a name="canceling-a-network-connection"></a>Annulation d’une connexion réseau

Pour annuler une connexion à une ressource réseau, une application peut appeler la fonction [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) , comme indiqué dans l’exemple suivant.

L’appel à **WNetCancelConnection2** spécifie qu’une connexion réseau ne doit plus être persistante. L’exemple appelle un gestionnaire d’erreurs défini par l’application pour traiter les erreurs et la fonction [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) pour l’impression.


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



la fonction [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) est prise en charge pour la compatibilité avec les versions antérieures de Windows pour les groupes de travail. Pour les nouvelles applications, utilisez [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).

Pour plus d’informations sur l’utilisation d’un gestionnaire d’erreurs défini par l’application, consultez [récupération des erreurs réseau](retrieving-network-errors.md).

 

 