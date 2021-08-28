---
title: Exemple de code pour la suppression du point de connexion RnR
description: L’exemple de code suivant est utilisé par l’exemple de code du service Winsock pour annuler l’inscription du point de connexion RnR pour le service.
ms.assetid: eee9b8b0-8566-442a-9a46-b6469e5bb1fc
ms.tgt_platform: multiple
keywords:
- Exemple de code pour la suppression du point de connexion RnR AD
- Windows Inscription et résolution des sockets Active Directory, exemple de code, suppression du point de connexion RnR
- Suppression du point de connexion RnR AD, exemple de code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b1dbeaecff3ced72ecce1ae4a789878c3cc5f00d333c4c19b5d5c8ef3b4abf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118693082"
---
# <a name="example-code-for-removing-the-rnr-connection-point"></a>Exemple de code pour la suppression du point de connexion RnR

L’exemple de code suivant est utilisé par l’exemple de code du service Winsock pour annuler l’inscription du point de connexion RnR pour le service.


```C++
#include <winsock2.h>
#include <stdio.h>
 
/***************************************************************************

    serverUnregister()

    Unregisters the RnR connection point for the specified service. 
    WSAStartup must be called before calling this function.

***************************************************************************/

INT serverUnregister(SOCKADDR *sa, 
                     GUID *pServiceID, 
                     LPTSTR pszServiceInstanceName, 
                     LPTSTR pszServiceInstanceComment)
{
    DWORD ret;
    WSAVERSION Version;
    WSAQUERYSET QuerySet;
    CSADDR_INFO CSAddrInfo[1];
    SOCKADDR sa_local;

    memset(&QuerySet, 0, sizeof(QuerySet));
    memset(&CSAddrInfo, 0, sizeof(CSAddrInfo));
    memset(&sa_local, 0, sizeof(SOCKADDR));
    sa_local.sa_family = AF_INET;

    // Build the CSAddrInfo structure to contain address
    // data. This is what clients use to create a connection.
    //
    // Be aware that the LocalAddr is set to zero because
    // dynamically assigned port numbers are used.
    //
    CSAddrInfo[0].LocalAddr.iSockaddrLength = sizeof(SOCKADDR);
    CSAddrInfo[0].LocalAddr.lpSockaddr = &sa_local;
    CSAddrInfo[0].RemoteAddr.iSockaddrLength = sizeof(SOCKADDR);
    CSAddrInfo[0].RemoteAddr.lpSockaddr = sa;
    CSAddrInfo[0].iSocketType = SOCK_STREAM;
    CSAddrInfo[0].iProtocol = PF_INET;

    QuerySet.dwSize = sizeof(WSAQUERYSET);
    QuerySet.lpServiceClassId = pServiceID;
    QuerySet.lpszServiceInstanceName = pszServiceInstanceName;
    QuerySet.lpszComment = pszServiceInstanceComment;
    QuerySet.lpVersion = &Version;
    QuerySet.lpVersion->dwVersion = 2;
    QuerySet.lpVersion->ecHow = COMP_NOTLESS;
    QuerySet.dwNameSpace = NS_NTDS;
    QuerySet.dwNumberOfCsAddrs = 1;
    QuerySet.lpcsaBuffer = CSAddrInfo;

    ret = WSASetService( &QuerySet,
                         RNRSERVICE_DEREGISTER,
                         SERVICE_MULTIPLE);

    return(ret);
}
```



 

 




