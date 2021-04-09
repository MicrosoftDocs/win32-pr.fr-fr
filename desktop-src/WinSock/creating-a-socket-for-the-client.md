---
description: Après l’initialisation, un objet SOCKET doit être instancié pour être utilisé par le client.
ms.assetid: 088a79ef-b430-4860-8edc-902a1a03ed0d
title: Création d’un socket pour le client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64467406f13ed40bdbe134e7796dd2aa5ff7bee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862577"
---
# <a name="creating-a-socket-for-the-client"></a>Création d’un socket pour le client

Après l’initialisation, un objet **Socket** doit être instancié pour être utilisé par le client.

**Pour créer un socket**

1.  Déclarez un objet [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) qui contient une structure [**sockaddr**](sockaddr-2.md) et initialisez ces valeurs. Pour cette application, la famille d’adresses Internet n’est pas spécifiée, de sorte qu’une adresse IPv6 ou IPv4 puisse être retournée. L’application demande que le type de socket soit un socket de flux pour le protocole TCP.
    ```C++
    struct addrinfo *result = NULL,
                    *ptr = NULL,
                    hints;

    ZeroMemory( &hints, sizeof(hints) );
    hints.ai_family = AF_UNSPEC;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    ```

    

2.  Appelez la fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) en demandant l’adresse IP pour le nom de serveur transmis sur la ligne de commande. Le port TCP sur le serveur auquel le client se connectera est défini par défaut sur le \_ port 27015 dans cet exemple. La fonction **getaddrinfo** retourne sa valeur sous la forme d’un entier dont les erreurs sont vérifiées.
    ```C++
    #define DEFAULT_PORT "27015"

    // Resolve the server address and port
    iResult = getaddrinfo(argv[1], DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

3.  Créez un objet **Socket** appelé ConnectSocket.
    ```C++
    SOCKET ConnectSocket = INVALID_SOCKET;
    ```

    

4.  Appelez la fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) et retournez sa valeur à la variable ConnectSocket. Pour cette application, utilisez la première adresse IP retournée par l’appel à [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) qui correspondait à la famille d’adresses, au type de socket et au protocole spécifiés dans le paramètre *Hints* . Dans cet exemple, un socket de flux TCP a été spécifié avec un type de socket de flux de chaussette \_ et un protocole \_ TCP IPPROTO. L’adresse \_ IP retournée peut être une adresse IPv6 ou IPv4 pour le serveur, car la famille d’adresses n’a pas été spécifiée (AF non spec).

    Si l’application cliente souhaite se connecter en utilisant uniquement IPv6 ou IPv4, la famille d’adresses doit être définie sur AF \_ inet6 pour IPv6 ou AF \_ inet pour IPv4 dans le paramètre *Hints* .

    ```C++
    // Attempt to connect to the first address returned by
    // the call to getaddrinfo
    ptr=result;

    // Create a SOCKET for connecting to server
    ConnectSocket = socket(ptr->ai_family, ptr->ai_socktype, 
        ptr->ai_protocol);
    ```

    

5.  Recherchez les erreurs pour vous assurer que le socket est un socket valide.
    ```C++
    if (ConnectSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

Les paramètres passés à la fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) peuvent être modifiés pour différentes implémentations.

La détection d’erreurs est un élément clé du code réseau réussi. Si l’appel de [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) échoue, il retourne un socket non valide \_ . L’instruction **If** dans le code précédent est utilisée pour intercepter les erreurs qui se sont produites lors de la création du Socket. [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne un numéro d’erreur associé à la dernière erreur qui s’est produite.

> [!Note]  
> Des vérifications d’erreurs plus étendues peuvent être nécessaires en fonction de l’application.
>
> Par exemple, la définition de *hints.ai_family* sur **AF_UNSPEC** peut provoquer l’échec de l’appel de connexion. Si cela se produit, utilisez une valeur IPv4 (**AF_INET**) ou IPv6 (**AF_INET6**) spécifique à la place.

[**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) est utilisé pour mettre fin à l’utilisation de la \_ dll WS2 32.

Étape suivante : [connexion à un socket](connecting-to-a-socket.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Initialisation de Winsock](initializing-winsock.md)
</dt> <dt>

[Application cliente Winsock](winsock-client-application.md)
</dt> </dl>

 

 
