---
description: Une fois que le serveur a terminé de recevoir les données du client et de renvoyer les données au client, le serveur se déconnecte du client et arrête le Socket.
ms.assetid: 67f33645-d57a-48bd-9f0c-9e816f528204
title: Déconnexion du serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6abf7754da39a891b3d29c69f6c835706debd36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862573"
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

    Lorsque l’application cliente est terminée à l’aide de la DLL Windows Sockets, la fonction [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) est appelée pour libérer des ressources.

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

 

 



