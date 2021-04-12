---
title: Exemple de code pour la publication du point de connexion RnR
description: L’exemple de code suivant est utilisé par le service Winsock pour inscrire le point de connexion RnR pour le service.
ms.assetid: dd2c7ac9-76fc-4366-8654-8048e6793a16
ms.tgt_platform: multiple
keywords:
- Exemple de code pour la publication du point de connexion RnR AD
- Inscription et résolution Windows Sockets Active Directory, exemple de code, publication du point de connexion RnR
- Publication du point de connexion RnR AD, exemple de code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e8f5337f80f9d05bcd1e9b25a963dadba4da21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190762"
---
# <a name="example-code-for-publishing-the-rnr-connection-point"></a><span data-ttu-id="f4fa0-106">Exemple de code pour la publication du point de connexion RnR</span><span class="sxs-lookup"><span data-stu-id="f4fa0-106">Example Code for Publishing the RnR Connection Point</span></span>

<span data-ttu-id="f4fa0-107">L’exemple de code suivant est utilisé par le service Winsock pour inscrire le point de connexion RnR pour le service.</span><span class="sxs-lookup"><span data-stu-id="f4fa0-107">The following code example is used by the Winsock service to register the RnR connection point for the service.</span></span>


```C++
#include <winsock2.h>
#include <stdio.h>

/***************************************************************************

    serverRegister()

    Registers the RnR connection point for the specified service. WSAStartup 
    must be called before calling this function.

***************************************************************************/

INT serverRegister(SOCKADDR * sa, 
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
    // data that clients use to establish a connection.
    //
    // Be aware that LocalAddr is set to zero because dynamically
    // assigned port numbers are used.
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
                         RNRSERVICE_REGISTER,
                         SERVICE_MULTIPLE);

    return(ret);
}
```



 

 




