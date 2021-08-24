---
description: Une fois que le serveur a terminé de recevoir les données du client et de renvoyer les données au client, le serveur se déconnecte du client et arrête le Socket.
ms.assetid: 67f33645-d57a-48bd-9f0c-9e816f528204
title: Déconnexion du serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f644b8727898a9d77ab5aa5fb10b0a0ae5b58cdf88a3beb1b9642215d142b6b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898359"
---
# <a name="disconnecting-the-server"></a>Déconnexion du serveur

Une fois que le serveur a terminé de recevoir les données du client et de renvoyer les données au client, le serveur se déconnecte du client et arrête le Socket.

**Pour déconnecter et arrêter un socket**

1.  Une fois que le serveur a terminé l’envoi de données au client, la fonction [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) peut être appelée en spécifiant \_ l’envoi SD pour arrêter le côté envoi du Socket. Cela permet au client de libérer certaines des ressources pour ce Socket. L’application serveur peut toujours recevoir des données sur le Socket.
    ```C++
    // shutdown the send half of the connection since no more data will be sent
    iResult = shutdown(ClientSocket, SD_SEND);
    if (iResult == SOCKET_ERROR) {
        printf("shutdown failed: %d\n", WSAGetLastError());
        closesocket(ClientSocket);
        WSACleanup();
        return 1;
    }
    ```

    

2.  Lorsque l’application cliente reçoit des données, la fonction [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) est appelée pour fermer le Socket.

    lorsque l’application cliente est exécutée à l’aide de la DLL Windows sockets, la fonction [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) est appelée pour libérer des ressources.

    ```C++
    // cleanup
    closesocket(ClientSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-server-source-code"></a>Compléter le code source du serveur

-   [Compléter le code serveur](complete-server-code.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Application de serveur Winsock](winsock-server-application.md)
</dt> <dt>

[Réception et envoi de données sur le serveur](receiving-and-sending-data-on-the-server.md)
</dt> <dt>

[Exécution de l’exemple de code du client et du serveur Winsock](finished-server-and-client-code.md)
</dt> </dl>

 

 



