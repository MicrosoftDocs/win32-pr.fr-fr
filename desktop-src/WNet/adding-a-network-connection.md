---
title: Ajout d’une connexion réseau
description: Pour établir une connexion à une ressource réseau décrite par une structure Resource, une application peut appeler WNetAddConnection2, WNetAddConnection3 ou la fonction WnetUseConnection.
ms.assetid: 0dab9eed-9019-4075-833b-324e5caee257
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8298216ab277c5f0ec4a0db8c4d6d1b6c592a8b643e6c30de96731ae2a32632b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053387"
---
# <a name="adding-a-network-connection"></a>Ajout d’une connexion réseau

Pour établir une connexion à une ressource réseau décrite par une structure [**Resource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) , une application peut appeler [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a), [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)ou la fonction [**WnetUseConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona) . L’exemple suivant illustre l’utilisation de la fonction **WNetAddConnection2** .

L’exemple de code appelle la fonction **WNetAddConnection2** , en spécifiant que le système doit mettre à jour le profil de l’utilisateur avec les informations, en créant une connexion « mémorisée » ou persistante. L’exemple appelle un gestionnaire d’erreurs défini par l’application pour traiter les erreurs et la fonction [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) pour l’impression.


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



la fonction [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) est prise en charge pour la compatibilité avec les versions antérieures de Windows pour les groupes de travail. Les nouvelles applications doivent appeler la fonction [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) ou la fonction [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) .

Pour plus d’informations sur l’utilisation d’un gestionnaire d’erreurs défini par l’application, consultez [récupération des erreurs réseau](retrieving-network-errors.md).

 

 