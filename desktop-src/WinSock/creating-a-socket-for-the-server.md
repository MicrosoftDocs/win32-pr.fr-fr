---
description: Après l’initialisation, un objet SOCKET doit être instancié pour être utilisé par le serveur.
ms.assetid: 2f3a7cab-3296-41ec-ac7e-224655b92a7c
title: Création d’un socket pour le serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd3fb00cb8b1155f4d26d94c9a88328256effe23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113090"
---
# <a name="creating-a-socket-for-the-server"></a>Création d’un socket pour le serveur

Après l’initialisation, un objet **Socket** doit être instancié pour être utilisé par le serveur.

**Pour créer un socket pour le serveur**

1.  La fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) est utilisée pour déterminer les valeurs de la structure [**sockaddr**](sockaddr-2.md) :

    -   **AF \_ INET** est utilisé pour spécifier la famille d’adresses IPv4.
    -   **Chaussette \_ STREAM** est utilisé pour spécifier un socket de flux.
    -   **IPPROTO \_ TCP** est utilisé pour spécifier le protocole TCP.
    -   **IA \_ Indicateur passif** indique que l’appelant a l’intention d’utiliser la structure d’adresse de socket retournée dans un appel à la fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) . Lorsque l’indicateur **ai \_ passif** est défini et que le paramètre *nodename* à la fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) est un pointeur **null** , la partie adresse IP de la structure de l’adresse du socket est définie sur **inadr \_ any** pour les adresses IPv4 ou **IN6ADDR \_ Any \_ init** pour les adresses IPv6.
    -   27015 est le numéro de port associé au serveur auquel le client se connectera.

    La structure [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) est utilisée par la fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .

    ```C++
    #define DEFAULT_PORT "27015"

    struct addrinfo *result = NULL, *ptr = NULL, hints;

    ZeroMemory(&hints, sizeof (hints));
    hints.ai_family = AF_INET;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    hints.ai_flags = AI_PASSIVE;

    // Resolve the local address and port to be used by the server
    iResult = getaddrinfo(NULL, DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

2.  Créez un objet **Socket** appelé ListenSocket pour que le serveur écoute les connexions clientes.
    ```C++
    SOCKET ListenSocket = INVALID_SOCKET;
    ```

    

3.  Appelez la fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) et retournez sa valeur à la variable ListenSocket. Pour cette application serveur, utilisez la première adresse IP retournée par l’appel à [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) qui correspondait à la famille d’adresses, au type de socket et au protocole spécifiés dans le paramètre *Hints* . Dans cet exemple, un socket de flux TCP pour IPv4 a été demandé avec une famille d’adresses IPv4, un type de socket de flux de chaussette \_ et un protocole de \_ TCP IPPROTO. Une adresse IPv4 est donc demandée pour le ListenSocket.

    Si l’application serveur souhaite écouter IPv6, la famille d’adresses doit être définie sur AF \_ inet6 dans le paramètre *Hints* . Si un serveur souhaite écouter à la fois IPv6 et IPv4, deux sockets d’écoute doivent être créés, un pour IPv6 et un pour IPv4. Ces deux sockets doivent être gérés séparément par l’application.

    Windows Vista et les versions ultérieures offrent la possibilité de créer un seul socket IPv6 mis en mode pile double pour écouter à la fois IPv6 et IPv4. Pour plus d’informations sur cette fonctionnalité, consultez [sockets à double pile](dual-stack-sockets.md).

    ```C++
    // Create a SOCKET for the server to listen for client connections

    ListenSocket = socket(result->ai_family, result->ai_socktype, result->ai_protocol);
    ```

    

4.  Recherchez les erreurs pour vous assurer que le socket est un socket valide.
    ```C++
    if (ListenSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

Étape suivante : [liaison d’un socket](binding-a-socket.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Initialisation de Winsock](initializing-winsock.md)
</dt> <dt>

[Application de serveur Winsock](winsock-server-application.md)
</dt> </dl>

 

 
