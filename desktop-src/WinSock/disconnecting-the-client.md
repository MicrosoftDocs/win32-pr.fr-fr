---
description: Une fois que le client a terminé l’envoi et la réception de données, le client se déconnecte du serveur et arrête le Socket.
ms.assetid: 33165e5b-e304-42b1-9542-45d8fe8a5218
title: Déconnexion du client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6ac34036cc92386d7d68b3d5debda4d37a92ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318389"
---
# <a name="disconnecting-the-client"></a>Déconnexion du client

Une fois que le client a terminé l’envoi et la réception de données, le client se déconnecte du serveur et arrête le Socket.

**Pour déconnecter et arrêter un socket**

1.  Lorsque le client a terminé d’envoyer des données au serveur, la fonction [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) peut être appelée en spécifiant \_ l’envoi SD pour arrêter le côté envoi du Socket. Cela permet au serveur de libérer certaines des ressources pour ce Socket. L’application cliente peut toujours recevoir des données sur le Socket.
    ```C++
    // shutdown the send half of the connection since no more data will be sent
    iResult = shutdown(ConnectSocket, SD_SEND);
    if (iResult == SOCKET_ERROR) {
        printf("shutdown failed: %d\n", WSAGetLastError());
        closesocket(ConnectSocket);
        WSACleanup();
        return 1;
    }
    ```

    

2.  Lorsque l’application cliente reçoit des données, la fonction [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) est appelée pour fermer le Socket.

    Lorsque l’application cliente est terminée à l’aide de la DLL Windows Sockets, la fonction [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) est appelée pour libérer des ressources.

    ```C++
    // cleanup
    closesocket(ConnectSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-client-source-code"></a>Code source complet du client

-   [Code client complet](complete-client-code.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Application cliente Winsock](winsock-client-application.md)
</dt> <dt>

[Envoi et réception de données sur le client](sending-and-receiving-data-on-the-client.md)
</dt> </dl>

 

 



