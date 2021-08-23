---
description: de nouvelles fonctions ont été introduites dans l’interface Windows sockets spécifiquement conçue pour faciliter la programmation de Windows sockets. l’un des avantages de ces nouvelles fonctions Windows sockets est la prise en charge intégrée pour IPv6 et IPv4.
ms.assetid: 83262f2b-a335-4bbd-b2e3-6c7744b3ee50
title: Appels de fonction pour les applications Winsock IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241db1f7e07264fe4f0c776834d17c48cff4780b06e6a42816d36a50fa22cef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051667"
---
# <a name="function-calls-for-ipv6-winsock-applications"></a>Appels de fonction pour les applications Winsock IPv6

de nouvelles fonctions ont été introduites dans l’interface Windows sockets spécifiquement conçue pour faciliter la programmation de Windows sockets. l’un des avantages de ces nouvelles fonctions Windows sockets est la prise en charge intégrée pour IPv6 et IPv4.

ces nouvelles fonctions Windows sockets sont les suivantes :

-   [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)
-   [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)
-   famille de fonctions de [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) (**getaddrinfo**, [**API getaddrinfoex**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa), [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow), [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo), [**FreeAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex), [**FreeAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow)et [**SetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa))
-   famille de fonctions [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) (**GetNameInfo** et [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow))

en outre, de nouvelles fonctions d’assistance IP avec prise en charge de IPv6 et IPv4 ont été ajoutées pour simplifier la programmation de Windows sockets. Ces nouvelles fonctions d’assistance IP sont les suivantes :

-   [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

Lors de l’ajout de la prise en charge IPv6 à une application, les instructions suivantes doivent être utilisées :

-   Utilisez [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) pour établir une connexion à un point de terminaison en fonction d’un nom d’hôte et d’un port. la fonction **WSAConnectByName** est disponible sur Windows Vista et versions ultérieures.
-   Utilisez [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) pour établir une connexion à un à partir d’une collection de points de terminaison possibles représentés par un ensemble d’adresses de destination (noms d’hôte et ports). la fonction **WSAConnectByList** est disponible sur Windows Vista et versions ultérieures.
-   remplacez les appels de fonction [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) par des appels à l’une des nouvelles fonctions de sockets [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) Windows. la fonction **getaddrinfo** avec prise en charge du protocole IPv6 est disponible sur Windows XP et versions ultérieures. le protocole ipv6 est également pris en charge sur Windows 2000 quand la version préliminaire de la technologie ipv6 pour Windows 2000 est installée.
-   remplacez les appels de fonction [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) par des appels à l’une des nouvelles fonctions [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) Windows sockets. la fonction **getnameinfo** avec prise en charge du protocole IPv6 est disponible sur Windows XP et versions ultérieures. le protocole ipv6 est également pris en charge sur Windows 2000 quand la version préliminaire de la technologie ipv6 pour Windows 2000 est installée.

## <a name="wsaconnectbyname"></a>WSAConnectByName

La fonction [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) simplifie la connexion à un point de terminaison à l’aide d’un socket basé sur un flux, étant donné le nom d’hôte ou l’adresse IP de la destination (IPv4 ou IPv6). Cette fonction réduit le code source nécessaire à la création d’une application IP qui est indépendante de la version du protocole IP utilisé. **WSAConnectByName** remplace les étapes suivantes dans une application TCP standard par un appel de fonction unique :

-   Résolution d’un nom d’hôte en un ensemble d’adresses IP.
-   Pour chaque adresse IP :
    -   Créez un socket de la famille d’adresses appropriée.
    -   Tente de se connecter à l’adresse IP distante. Si la connexion a réussi, elle retourne la valeur ; dans le cas contraire, l’adresse IP distante suivante pour l’hôte est tentée.

La fonction [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) va au-delà de la résolution du nom et de la tentative de connexion. La fonction utilise toutes les adresses distantes retournées par la résolution de noms et toutes les adresses IP sources de l’ordinateur local. Il tente d’abord de se connecter en utilisant des paires d’adresses avec les chances de réussite les plus élevées. Par conséquent, **WSAConnectByName** garantit non seulement qu’une connexion sera établie si possible, mais elle réduit également le temps nécessaire à l’établissement de la connexion.

Pour activer les communications IPv6 et IPv4, utilisez la méthode suivante :

-   La fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) doit être appelée sur un socket créé pour la \_ famille d’adresses d’adresses inet6 AF pour désactiver l’option de socket **IPv6 \_ V6ONLY** avant d’appeler [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea). Pour ce faire, vous devez appeler la fonction **setsockopt** sur le socket avec le paramètre *Level* défini sur **IPPROTO \_ IPv6** (voir [options de \_ Socket IPPROTO IPv6](ipproto-ipv6-socket-options.md)), le paramètre *nom_option* défini sur **IPv6 \_ V6ONLY** et la valeur de paramètre *optvalue* définie sur zéro.

Si une application doit établir une liaison à une adresse ou à un port local spécifique, [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) ne peut pas être utilisé, car le paramètre socket de **WSAConnectByName** doit être un socket indépendant.

L’exemple de code ci-dessous montre que quelques lignes de code sont nécessaires pour utiliser cette fonction pour implémenter une application qui est indépendante de la version IP.

Établir une connexion à l’aide de [ **WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(LPWSTR NodeName, LPWSTR PortName) 
{
    SOCKET ConnSocket;
    DWORD ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);
  
    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    bSuccess = WSAConnectByName(ConnSocket, NodeName, 
            PortName, &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}
```



## <a name="wsaconnectbylist"></a>WSAConnectByList

La fonction [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) établit une connexion à un hôte en fonction d’un ensemble d’hôtes possibles (représentés par un ensemble d’adresses IP et de ports de destination). La fonction prend toutes les adresses IP et tous les ports pour le point de terminaison et toutes les adresses IP de l’ordinateur local et tente une connexion à l’aide de toutes les combinaisons d’adresses possibles.

[**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) est lié à la fonction [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) . Au lieu d’accepter un seul nom d’hôte, **WSAConnectByList** accepte une liste d’hôtes (adresses de destination et paires de ports) et se connecte à l’une des adresses et des ports de la liste fournie. Cette fonction est conçue pour prendre en charge les scénarios dans lesquels une application doit se connecter à n’importe quel hôte disponible en dehors d’une liste d’hôtes potentiels.

Comme pour [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea), la fonction [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) réduit considérablement le code source nécessaire à la création, à la liaison et à la connexion d’un Socket. Grâce à cette fonction, il est beaucoup plus facile d’implémenter une application qui est indépendante de la version IP. La liste des adresses d’un hôte accepté par cette fonction peut être des adresses IPv6 ou IPv4.

Pour permettre aux adresses IPv6 et IPv4 d’être transmises dans la liste d’adresses unique acceptée par la fonction, les étapes suivantes doivent être effectuées avant d’appeler la fonction :

-   La fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) doit être appelée sur un socket créé pour la \_ famille d’adresses d’adresses inet6 AF pour désactiver l’option de socket **IPv6 \_ V6ONLY** avant d’appeler [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist). Pour ce faire, vous devez appeler la fonction **setsockopt** sur le socket avec le paramètre *Level* défini sur **IPPROTO \_ IPv6** (voir [options de \_ Socket IPPROTO IPv6](ipproto-ipv6-socket-options.md)), le paramètre *nom_option* défini sur **IPv6 \_ V6ONLY** et la valeur de paramètre *optvalue* définie sur zéro.
-   Toutes les adresses IPv4 doivent être représentées dans le format d’adresse IPv6 mappée IPv4, ce qui permet à une application IPv6 uniquement de communiquer avec un nœud IPv4. Le format d’adresse IPv6 mappée IPv4 permet à l’adresse IPv4 d’un nœud IPv4 d’être représentée comme une adresse IPv6. L’adresse IPv4 est encodée dans les bits de poids faible 32 de l’adresse IPv6, et les bits de poids fort 96 contiennent le préfixe fixe 0:0 : 0:0 : 0 : FFFF. Le format d’adresse IPv6 mappée IPv4 est spécifié dans le document RFC 4291. Pour plus d’informations, consultez [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291). La \_ macro IN6ADDR SETV4MAPPED dans *Mstcpip. h* peut être utilisée pour convertir une adresse IPv4 au format d’adresse IPv6 mappé IPv4 requis.

Établir une connexion à l’aide de [ **WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(SOCKET_ADDRESS_LIST *AddressList) 
{
    SOCKET ConnSocket;
    DWORD ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);

    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    // AddressList may contain IPv6 and/or IPv4Mapped addresses
    bSuccess = WSAConnectByList(ConnSocket,
            AddressList,
            &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}
```



## <a name="getaddrinfo"></a>getaddrinfo

La fonction **getaddrinfo** effectue également le travail de traitement de nombreuses fonctions. auparavant, les appels à plusieurs fonctions de Windows sockets devaient créer, ouvrir, puis lier une adresse à un socket. Avec la fonction **getaddrinfo** , les lignes de code source nécessaires pour effectuer ce travail peuvent être réduites de manière significative. Les deux exemples suivants illustrent le code source nécessaire à l’exécution de ces tâches avec et sans la fonction **getaddrinfo** .

effectuer une ouverture, une Connecter et une liaison à l’aide de **getaddrinfo**


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *ServerName, char *PortName, int SocketType)
{
    SOCKET ConnSocket;
    ADDRINFO *AI;

    if (getaddrinfo(ServerName, PortName, NULL, &AI) != 0) {
        return INVALID_SOCKET;
    }

    ConnSocket = socket(AI->ai_family, SocketType, 0);
    if (ConnSocket == INVALID_SOCKET) {
        freeaddrinfo(AI);
        return INVALID_SOCKET;
    }

    if (connect(ConnSocket, AI->ai_addr, (int) AI->ai_addrlen) == SOCKET_ERROR) {
        closesocket(ConnSocket);
        freeaddrinfo(AI);
        return INVALID_SOCKET;
    }

    return ConnSocket;
}
```



effectuer une ouverture, une Connecter et une liaison sans utiliser **getaddrinfo**


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *ServerName, unsigned short Port, int SocketType) 
{
    SOCKET ConnSocket;
    LPHOSTENT hp;
    SOCKADDR_IN ServerAddr;
    
    ConnSocket = socket(AF_INET, SocketType, 0); /* Open a socket */
    if (ConnSocket < 0 ) {
        return INVALID_SOCKET;
    }

    memset(&ServerAddr, 0, sizeof(ServerAddr));
    ServerAddr.sin_family = AF_INET;
    ServerAddr.sin_port = htons(Port);

    if (isalpha(ServerName[0])) {   /* server address is a name */
        hp = gethostbyname(ServerName);
        if (hp == NULL) {
            return INVALID_SOCKET;
        }
        ServerAddr.sin_addr.s_addr = (ULONG) hp->h_addr;
    } else { /* Convert nnn.nnn address to a usable one */
        ServerAddr.sin_addr.s_addr = inet_addr(ServerName);
    } 

    if (connect(ConnSocket, (LPSOCKADDR)&ServerAddr, 
        sizeof(ServerAddr)) == SOCKET_ERROR)
    {
        closesocket(ConnSocket);
        return INVALID_SOCKET;
    }

    return ConnSocket;
}
```



Notez que ces deux exemples de code source effectuent les mêmes tâches, mais le premier exemple, à l’aide de la fonction **getaddrinfo** , requiert moins de lignes de code source et peut gérer des adresses IPv6 ou IPv4. Le nombre de lignes de code source supprimées à l’aide de la fonction **getaddrinfo** varie.

> [!Note]  
> Dans le code source de production, votre application itère au sein de l’ensemble d’adresses renvoyé par la fonction [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) ou [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) . Ces exemples omettent cette étape en faveur de la simplicité.

 

Un autre problème que vous devez résoudre lorsque vous modifiez une application IPv4 existante pour prendre en charge IPv6 est associé à l’ordre dans lequel les fonctions sont appelées. Les options [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) et [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) requièrent qu’une séquence d’appels de fonction soit effectuée dans un ordre spécifique.

Sur les plateformes où IPv4 et IPv6 sont tous deux utilisés, la famille d’adresses du nom d’hôte distant n’est pas connue à l’avance. Par conséquent, la résolution d’adresses à l’aide de la fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) doit être exécutée en premier pour déterminer l’adresse IP et la famille d’adresses de l’hôte distant. La fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) peut ensuite être appelée pour ouvrir un socket de la famille d’adresses retournée par [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo). il s’agit d’un changement important dans la façon dont les applications de Windows sockets sont écrites, étant donné que de nombreuses applications IPv4 ont tendance à utiliser un ordre différent d’appels de fonction.

La plupart des applications IPv4 créent d’abord un socket pour la \_ famille d’adresses d’inet AF, puis effectuent la résolution de noms, puis utilisent le socket pour se connecter à l’adresse IP résolue. Lorsque vous rendez ces applications compatibles IPv6, l’appel de fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) doit être retardé jusqu’à la résolution de noms lorsque la famille d’adresses a été deteremined. Notez que si la résolution de noms retourne des adresses IPv4 et IPv6, des sockets IPv4 et IPv6 distincts doivent être utilisés pour se connecter à ces adresses de destination. toutes ces complexités peuvent être évitées à l’aide de la fonction [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) sur Windows Vista et versions ultérieures, afin que les développeurs d’applications soient encouragés à utiliser cette nouvelle fonction.

L’exemple de code suivant montre la séquence appropriée pour effectuer d’abord la résolution de noms (effectuée à la quatrième ligne de l’exemple de code source suivant), puis ouvrir un socket (effectué dans la<sup>troisième ligne de</sup> l’exemple de code suivant). Cet exemple est un extrait du fichier client. c figurant dans le [code client compatible IPv6](ipv6-enabled-client-code-2.md) de l’annexe B. La fonction PrintError appelée dans l’exemple de code suivant est indiquée dans l’exemple client. c.


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *Server, char *PortName, int Family, int SocketType)
{

    int iResult = 0;
    SOCKET ConnSocket = INVALID_SOCKET;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;
    ADDRINFO Hints;

    char *AddrName = NULL;

    memset(&Hints, 0, sizeof (Hints));
    Hints.ai_family = Family;
    Hints.ai_socktype = SocketType;

    iResult = getaddrinfo(Server, PortName, &Hints, &AddrInfo);
    if (iResult != 0) {
        printf("Cannot resolve address [%s] and port [%s], error %d: %s\n",
               Server, PortName, WSAGetLastError(), gai_strerror(iResult));
        return INVALID_SOCKET;
    }
    //
    // Try each address getaddrinfo returned, until we find one to which
    // we can successfully connect.
    //
    for (AI = AddrInfo; AI != NULL; AI = AI->ai_next) {

        // Open a socket with the correct address family for this address.
        ConnSocket = socket(AI->ai_family, AI->ai_socktype, AI->ai_protocol);
        if (ConnSocket == INVALID_SOCKET) {
            printf("Error Opening socket, error %d\n", WSAGetLastError());
            continue;
        }
        //
        // Notice that nothing in this code is specific to whether we 
        // are using UDP or TCP.
        //
        // When connect() is called on a datagram socket, it does not 
        // actually establish the connection as a stream (TCP) socket
        // would. Instead, TCP/IP establishes the remote half of the
        // (LocalIPAddress, LocalPort, RemoteIP, RemotePort) mapping.
        // This enables us to use send() and recv() on datagram sockets,
        // instead of recvfrom() and sendto().
        //

        printf("Attempting to connect to: %s\n", Server ? Server : "localhost");
        if (connect(ConnSocket, AI->ai_addr, (int) AI->ai_addrlen) != SOCKET_ERROR)
            break;

        if (getnameinfo(AI->ai_addr, (socklen_t) AI->ai_addrlen, AddrName,
                        sizeof (AddrName), NULL, 0, NI_NUMERICHOST) != 0) {
            strcpy_s(AddrName, sizeof (AddrName), "<unknown>");
            printf("connect() to %s failed with error %d\n", AddrName, WSAGetLastError());
            closesocket(ConnSocket);
            ConnSocket = INVALID_SOCKET;
        }    
    }
    return ConnSocket;
}

```



## <a name="ip-helper-functions"></a>Fonctions de l’assistance IP

Enfin, les applications qui utilisent la fonction d’assistance IP [**GetAdaptersInfo**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo)et les informations de l' [**\_ adaptateur IP \_**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info)de la structure associée doivent reconnaître que cette fonction et cette structure sont toutes deux limitées aux adresses IPv4. Les remplacements compatibles IPv6 pour cette fonction et cette structure sont la fonction [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) et la structure d' [**\_ \_ adresses IP**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) de la carte. les applications compatibles ipv6 utilisant l’API d’assistance ip doivent utiliser la fonction **GetAdaptersAddresses** et la structure d’adresses de l' **\_ adaptateur \_ ip** ipv6 correspondante, toutes deux définies dans le kit de développement logiciel (SDK) de Microsoft Windows.

## <a name="recommendations"></a>Recommandations

La meilleure approche pour s’assurer que votre application utilise des appels de fonction compatibles IPv6 consiste à utiliser la fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) pour obtenir une traduction d’hôte à adresse. à partir de Windows XP, la fonction **getaddrinfo** rend la fonction [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) inutile, et votre application doit donc utiliser la fonction **getaddrinfo** à la place pour les futurs projets de programmation. Alors que Microsoft continuera à prendre en charge **gethostbyname**, cette fonction ne sera pas étendue pour prendre en charge IPv6. Pour une prise en charge transparente de l’obtention des informations sur l’hôte IPv6 et IPv4, vous devez utiliser **getaddrinfo**.

L’exemple suivant montre comment utiliser au mieux la fonction **getaddrinfo** . Notez que la fonction, quand elle est utilisée correctement comme illustré dans cet exemple, gère correctement la conversion d’hôte à adresse IPv6 et IPv4, mais elle obtient également d’autres informations utiles sur l’hôte, telles que le type de sockets pris en charge. Cet exemple est un extrait de l’exemple client. c figurant dans l’annexe B.


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

int ResolveName(char *Server, char *PortName, int Family, int SocketType)
{

    int iResult = 0;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;
    ADDRINFO Hints;

   //
    // By not setting the AI_PASSIVE flag in the hints to getaddrinfo, we're
    // indicating that we intend to use the resulting address(es) to connect
    // to a service.  This means that when the Server parameter is NULL,
    // getaddrinfo will return one entry per allowed protocol family
    // containing the loopback address for that family.
    //
    
    memset(&Hints, 0, sizeof(Hints));
    Hints.ai_family = Family;
    Hints.ai_socktype = SocketType;
    iResult = getaddrinfo(Server, PortName, &Hints, &AddrInfo);
    if (iResult != 0) {
        printf("Cannot resolve address [%s] and port [%s], error %d: %s\n",
               Server, PortName, WSAGetLastError(), gai_strerror(iResult));
        return SOCKET_ERROR;
    }
     return 0;
}
```



> [!Note]  
> la version de la fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) qui prend en charge IPv6 est une nouveauté de la version Windows XP de Windows.

 

Code pour éviter

La traduction d’adresses d’hôte a traditionnellement été obtenue à l’aide de la fonction [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) . à partir de Windows XP :

-   La fonction **getaddrinfo** rend la fonction **gethostbyname** obsolète.
-   Vos applications doivent utiliser la fonction **getaddrinfo** au lieu de la fonction **gethostbyname** .

Tâches de codage

**Pour modifier une application IPv4 existante afin d’ajouter la prise en charge d’IPv6**

1.  Acquérir l’utilitaire Checkv4.exe. cet utilitaire est installé dans le cadre de la SDK Windows. le SDK Windows est disponible via un abonnement MSDN et peut également être téléchargé à partir du site web de Microsoft ( https://msdn.microsoft.com) . une version antérieure de l’outil *Checkv4.exe* était également incluse dans le cadre de la version préliminaire de la technologie Microsoft IPv6 pour Windows 2000.
2.  Exécutez l’utilitaire *Checkv4.exe* sur votre code. Consultez [utilisation de l’utilitaire de Checkv4.exe](using-the-checkv4-exe-utility-2.md) pour en savoir plus sur l’exécution de l’utilitaire de version sur vos fichiers.
3.  L’utilitaire vous avertit de l’utilisation des fonctions [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)et d’autres fonctions IPv4 uniquement, et fournit des recommandations sur la façon de les remplacer par la fonction compatible IPv6, par exemple [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) et [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo).
4.  Remplacez toutes les instances de la fonction **gethostbyname** et le code associé, le cas échéant, par la fonction **getaddrinfo** . sur Windows Vista, utilisez la fonction [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) ou [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) si nécessaire.
5.  Remplacez toutes les instances de la fonction [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) et le code associé, le cas échéant, par la fonction [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .

Vous pouvez également rechercher dans votre base de code les instances des fonctions **gethostbyname** et [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) , puis modifier toute l’utilisation (et tout autre code associé, le cas échéant) vers les fonctions **getaddrinfo** et [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide IPv6 pour les Applications Windows sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Modification des structures de données pour IPv6 Winsock appications](changing-data-structures-2.md)
</dt> <dt>

[Sockets à double pile pour les applications Winsock IPv6](dual-stack-sockets.md)
</dt> <dt>

[Utilisation d’adresses IPv4 codées en dur](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Problèmes d’interface utilisateur pour les applications Winsock IPv6](user-interface-issues-2.md)
</dt> <dt>

[Protocoles sous-jacents pour les applications Winsock IPv6](underlying-protocols-2.md)
</dt> </dl>

 

 
