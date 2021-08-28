---
description: Une fois que le socket est à l’écoute d’une connexion, le programme doit gérer les demandes de connexion sur ce Socket.
ms.assetid: d01f3d90-4d83-442e-aada-e7b082ef7699
title: acceptation d’une connexion (Windows sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 410dcdebb660ec290ee5723b569ca358e0317777300a479e17a516e594744b49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996889"
---
# <a name="accepting-a-connection-windows-sockets-2"></a>acceptation d’une connexion (Windows sockets 2)

Une fois que le socket est à l’écoute d’une connexion, le programme doit gérer les demandes de connexion sur ce Socket.

**Pour accepter une connexion sur un socket**

1.  Créez un objet **Socket** temporaire appelé ClientSocket pour accepter les connexions des clients.
    ```C++
    
    SOCKET ClientSocket;

    
    ```

    

2.  Normalement, une application serveur est conçue pour écouter les connexions à partir de plusieurs clients. Pour les serveurs à hautes performances, plusieurs threads sont couramment utilisés pour gérer les connexions client multiples.

    Il existe plusieurs techniques de programmation différentes utilisant Winsock qui peuvent être utilisées pour écouter plusieurs connexions client. Une technique de programmation consiste à créer une boucle continue qui vérifie les demandes de connexion à l’aide de la fonction [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) (voir [écoute sur un socket](listening-on-a-socket.md)). Si une demande de connexion se produit, l’application appelle la fonction [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**accepted**](/windows/win32/api/mswsock/nf-mswsock-acceptex)ou [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) et transmet le travail à un autre thread pour traiter la demande. Plusieurs autres techniques de programmation sont possibles.

    Notez que cet exemple de base est très simple et n’utilise pas plusieurs threads. L’exemple écoute également uniquement et accepte une seule connexion.

    ```C++
    
    ClientSocket = INVALID_SOCKET;

    // Accept a client socket
    ClientSocket = accept(ListenSocket, NULL, NULL);
    if (ClientSocket == INVALID_SOCKET) {
        printf("accept failed: %d\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
     
    
    ```

    

3.  Lorsque la connexion cliente a été acceptée, une application serveur transmet normalement le socket client accepté (la variable ClientSocket dans l’exemple de code ci-dessus) à un thread de travail ou à un port de terminaison d’e/s et continue d’accepter des connexions supplémentaires. Dans cet exemple de base, le serveur continue à l’étape suivante.

    Il existe un certain nombre d’autres techniques de programmation qui peuvent être utilisées pour écouter et accepter plusieurs connexions. Celles-ci incluent l’utilisation des fonctions [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) . des exemples de certaines de ces différentes techniques de programmation sont illustrés dans les [exemples Winsock avancés](getting-started-with-winsock.md) inclus dans le kit de développement logiciel (SDK) de Microsoft Windows.

    > [!Note]  
    > Sur les systèmes UNIX, une technique de programmation courante pour les serveurs était de faire en sorte qu’une application écoute les connexions. Lorsqu’une connexion a été acceptée, le processus parent appelle la fonction de **branchement** pour créer un processus enfant afin de gérer la connexion du client, en héritant du socket du parent. cette technique de programmation n’est pas prise en charge sur Windows, dans la mesure où la fonction **fork** n’est pas prise en charge. Cette technique n’est pas non plus adaptée aux serveurs hautes performances, car les ressources nécessaires à la création d’un nouveau processus sont beaucoup plus importantes que celles nécessaires pour un thread.

     

Étape suivante : [réception et envoi de données sur le serveur](receiving-and-sending-data-on-the-server.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Application de serveur Winsock](winsock-server-application.md)
</dt> <dt>

[Écoute sur un socket](listening-on-a-socket.md)
</dt> </dl>

 

 
