---
description: voici un guide pas-à-pas pour la mise en route de la programmation de Windows sockets.
ms.assetid: 905cd5bc-44af-4d3f-841a-9e9a2700a785
title: Prise en main avec Winsock
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: c22a4f837506a4ed01de73fe5b9997df7868e127
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008271"
---
# <a name="getting-started-with-winsock"></a>Prise en main avec Winsock

voici un guide pas-à-pas pour la mise en route de la programmation de Windows sockets. Il est conçu pour vous permettre de comprendre les fonctions et structures de données de base de Winsock, et comment elles fonctionnent ensemble.

L’application cliente et serveur utilisée pour l’illustration est un client et un serveur de base. vous trouverez des exemples de code plus avancés dans les exemples inclus dans le kit de développement logiciel (SDK) de Microsoft Windows.

Les premières étapes sont identiques pour les applications client et serveur.

- [À propos des serveurs et des clients](about-clients-and-servers.md)
- [Création d’une application Winsock de base](creating-a-basic-winsock-application.md)
- [Initialisation de Winsock](initializing-winsock.md)

Les sections suivantes décrivent les étapes restantes pour créer une application cliente Winsock.

- [Création d’un socket pour le client](creating-a-socket-for-the-client.md)
- [Connexion à un socket](connecting-to-a-socket.md)
- [Envoi et réception de données sur le client](sending-and-receiving-data-on-the-client.md)
- [Déconnexion du client](disconnecting-the-client.md)

Les sections suivantes décrivent les étapes restantes pour créer une application de serveur Winsock.

- [Création d’un socket pour le serveur](creating-a-socket-for-the-server.md)
- [Liaison d’un socket](binding-a-socket.md)
- [Écoute sur un socket](listening-on-a-socket.md)
- [Acceptation d’une connexion](accepting-a-connection.md)
- [Réception et envoi de données sur le serveur](receiving-and-sending-data-on-the-server.md)
- [Déconnexion du serveur](disconnecting-the-server.md)

Le code source complet de ces exemples de base.

- [Exécution de l’exemple de code du client et du serveur Winsock](finished-server-and-client-code.md)
- [Code client Winsock complet](complete-client-code.md)
- [Compléter le code du serveur Winsock](complete-server-code.md)

## <a name="advanced-winsock-samples"></a>Exemples de Winsock avancés

Plusieurs exemples de serveur et de client Winsock plus avancés sont disponibles [sur GitHub](https://github.com/microsoft/Windows-classic-samples/tree/main/Samples/Win7Samples/netds/winsock). Elles sont répertoriées ci-dessous dans l’ordre dans lequel elles sont plus élevées pour réduire les performances et se trouvent dans les répertoires suivants :

- iocp

    Ce répertoire contient trois exemples de programmes qui utilisent des ports de terminaison d’e/s. Les programmes incluent un serveur Winsock (iocpserver) qui utilise la fonction [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) , un serveur Winsock (iocpserverex) qui utilise la fonction [**accepteur**](/windows/win32/api/mswsock/nf-mswsock-acceptex) et un client Winsock multithread simple (iocpclient) utilisé pour tester l’un de ces serveurs. Les programmes serveur prennent en charge plusieurs clients qui se connectent via TCP/IP et envoient des tampons de données de taille arbitraire que le serveur renvoie ensuite au client. Pour des raisons pratiques, un programme client simple, iocpclient, a été développé pour se connecter et envoyer continuellement des données au serveur afin de le stresser à l’aide de plusieurs threads. Les serveurs Winsock qui utilisent des ports de terminaison d’e/s offrent la plus grande capacité de performances.

- éviter

    Ce répertoire contient un exemple de programme serveur qui utilise des e/s avec chevauchement. L’exemple de programme utilise la fonction [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) et des e/s avec chevauchement pour gérer efficacement plusieurs demandes de connexion asynchrones des clients. Le serveur utilise la fonction **AcceptEx** pour multiplexer différentes connexions clientes dans une application Win32 à thread unique. L’utilisation des e/s avec chevauchement permet une plus grande évolutivité.

- WSAPoll

    Ce répertoire contient un exemple de programme de base qui illustre l’utilisation de la fonction [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) . Le programme client et serveur combiné est non bloquant et utilise la fonction **WSAPoll** pour déterminer quand il est possible d’envoyer ou de recevoir sans blocage. Cet exemple est plus pour l’illustration et n’est pas un serveur à hautes performances.

- simple

    Ce répertoire contient trois exemples de programmes de base qui illustrent l’utilisation de plusieurs threads par un serveur. Les programmes incluent un serveur TCP/UDP simple (simple), un serveur TCP uniquement (simple \_ IOCTL) qui utilise la fonction [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) dans une application console Win32 pour prendre en charge plusieurs requêtes client et un programme TCP/UDP client (simplec) pour tester les serveurs. Les serveurs illustrent l’utilisation de plusieurs threads pour gérer plusieurs demandes du client. Cette méthode présente des problèmes d’extensibilité, car un thread distinct est créé pour chaque demande du client.

- accepter

    Ce répertoire contient un exemple de serveur et un programme client de base. Le serveur montre l’utilisation d’une acceptation non bloquante à l’aide de la fonction [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou d’une acceptation asynchrone à l’aide de la fonction [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) . Cet exemple est plus pour l’illustration et n’est pas un serveur à hautes performances.
