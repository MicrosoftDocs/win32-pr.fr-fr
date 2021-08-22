---
description: dans les applications Winsock, les codes d’erreur sont récupérés à l’aide de la fonction WSAGetLastError, le remplacement des sockets Windows pour la fonction Windows GetLastError.
ms.assetid: cb73fc92-74bd-4c8b-a1c0-6daf4d298aa1
title: Codes d’erreur-errno, h_errno et WSAGetLastError
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2e9c4372bd479ee4b94bd3226128737dae3d5637be94046eb013716590ac285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132632"
---
# <a name="error-codes---errno-h_errno-and-wsagetlasterror"></a>Codes d’erreur-errno, h \_ errno et WSAGetLastError

dans les applications Winsock, les codes d’erreur sont récupérés à l’aide de la fonction [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) , le remplacement des sockets Windows pour la fonction Windows [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) . les codes d’erreur retournés par Windows sockets sont similaires aux constantes de code d’erreur de socket UNIX, mais les constantes sont toutes précédées de WSA. par conséquent, dans les applications Winsock, le code d’erreur WSAEWOULDBLOCK est retourné, tandis que dans UNIX applications, le code d’erreur EWOULDBLOCK serait retourné.

les codes d’erreur définis par Windows sockets ne sont pas mis à disposition par le biais de la variable *errno* . En outre, pour la classe **getXbyY** des fonctions, les codes d’erreur ne sont pas rendus disponibles par le biais de la variable *h \_ errno* . La fonction [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) est conçue pour fournir un moyen fiable pour un thread dans un processus multithread d’obtenir des informations sur les erreurs par thread.

à des fins de compatibilité avec Berkeley UNIX (BSD), les premières versions de Windows (Windows 95 avec la mise à jour Windows Socket 2 et Windows 98, par exemple) redéfinissent les constantes d’erreur Berkeley standard qui se trouvent généralement dans *errno. h* sur BSD en tant qu’erreurs de sockets de Windows équivalentes. Par exemple, ECONNREFUSED a été défini en tant que **WSAECONNREFUSED** dans le fichier d’en-tête *Winsock. h* . dans les versions ultérieures de Windows (Windows NT 3,1 et versions ultérieures), ces définitions ont été commentées afin d’éviter les conflits avec *errno. h* utilisé avec Microsoft C/C++ et Visual Studio.

le fichier d’en-tête *Winsock2. h* inclus dans le kit de développement logiciel (sdk) de Microsoft Windows, le kit de développement logiciel (sdk) de la plateforme, et Visual Studio contient toujours un bloc de définitions commentées dans un \# bloc ifdef 0 et \# endif qui définissent les codes d’erreur de socket BSD comme les constantes d’erreur WSA. elles peuvent être utilisées pour fournir une certaine compatibilité avec la programmation de sockets UNIX, BSD et Linux. Pour la compatibilité avec BSD, une application peut choisir de modifier *Winsock2. h* et de supprimer les marques de commentaire de ce bloc. Toutefois, les développeurs d’applications sont fortement déconseillés de supprimer les marques de commentaire de ce bloc en raison de conflits inévitables avec *errno. h* dans la plupart des applications. en outre, les erreurs de socket BSD sont définies sur des valeurs très différentes de celles utilisées dans les programmes UNIX, BSD et Linux. Les développeurs d’applications sont fortement encouragés à utiliser les constantes d’erreur WSA dans les applications de Socket.

Ces définitions restent commentées dans l’en-tête *Winsock2. h* au sein d’un \# bloc ifdef 0 et \# endif. Si un développeur d’applications insiste sur l’utilisation des codes d’erreur BSD pour la compatibilité, une application peut choisir d’inclure une ligne du formulaire :


```C++
#include <windows.h>

#define errno WSAGetLastError()
```



Cela permet de disposer d’un code de mise en réseau écrit pour utiliser le *errno* global pour fonctionner correctement dans un environnement à thread unique. Il existe des inconvénients très sérieux. Si un fichier source comprend du code qui inspecte *errno* pour les fonctions socket et non socket, ce mécanisme ne peut pas être utilisé. En outre, il n’est pas possible pour une application d’affecter une nouvelle valeur à *errno*. (dans Windows sockets, la fonction [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) peut être utilisée à cet effet.)

Style BSD classique


```C++
r = recv(...);
if (r == -1
    && errno == EWOULDBLOCK)
    {...}
```



Style préféré


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == EWOULDBLOCK)
    {...}
```



Bien que les constantes d’erreur cohérentes avec les sockets Berkeley 4,3 soient fournies à des fins de compatibilité, les applications sont vivement encouragées à utiliser les définitions de code d’erreur WSA. cela est dû au fait que les codes d’erreur retournés par certaines fonctions Windows sockets se trouvent dans la plage standard de codes d’erreur, comme défini par Microsoft C ©. Par conséquent, une meilleure version du fragment de code source précédent est :


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == WSAEWOULDBLOCK)
    {...}
```



La spécification Winsock 1,1 d’origine définie dans 1995 a recommandé un ensemble de codes d’erreur et répertorie les erreurs possibles qui peuvent être retournées à la suite de chaque fonction. Windows les sockets 2 ont ajouté des fonctions et des fonctionnalités avec d’autres codes d’erreur de Windows sockets retournés en plus de ceux listés dans la spécification Winsock d’origine. Des fonctions supplémentaires ont été ajoutées au fil du temps pour améliorer Winsock pour une utilisation par les développeurs. par exemple, de nouvelles fonctions de service de nom ([**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) et [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo), par exemple) ont été ajoutées pour prendre en charge IPv6 et IPv4 sur Windows XP et versions ultérieures. Certaines des anciennes fonctions de service de nom IPv4 uniquement (la classe **getXbyY** des fonctions, par exemple) ont été dépréciées.

la liste complète des codes d’erreur possibles retournés par Windows fonctions sockets est indiquée dans la section sur les [codes d’erreur des sockets Windows](windows-sockets-error-codes-2.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des erreurs Winsock](handling-winsock-errors.md)
</dt> <dt>

[Portage d’applications de socket vers Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Windows Codes d’erreur des sockets](windows-sockets-error-codes-2.md)
</dt> <dt>

[Considérations sur la programmation Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 
