---
description: Une fois que le socket est lié à une adresse IP et à un port sur le système, le serveur doit ensuite écouter cette adresse IP et ce port pour les demandes de connexion entrante.
ms.assetid: 83c9f0e7-2e6d-449b-8d97-3d13154112cd
title: Écoute sur un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c36fe1718493d1b92ca52bb3c648ebd1aa5b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515448"
---
# <a name="listening-on-a-socket"></a>Écoute sur un socket

Une fois que le socket est lié à une adresse IP et à un port sur le système, le serveur doit ensuite écouter cette adresse IP et ce port pour les demandes de connexion entrante.

## <a name="to-listen-on-a-socket"></a>Pour écouter sur un socket

Appelez la fonction [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) , en passant comme paramètres le socket créé et une valeur pour le *backlog*, longueur maximale de la file d’attente des connexions en attente à accepter. Dans cet exemple, le paramètre *backlog* a été défini sur **SOMAXCONN**. Cette valeur est une constante spéciale qui indique au fournisseur Winsock pour que ce Socket autorise un nombre maximal raisonnable de connexions en attente dans la file d’attente. Vérifiez la valeur de retour pour les erreurs générales.


```C++
if ( listen( ListenSocket, SOMAXCONN ) == SOCKET_ERROR ) {
    printf( "Listen failed with error: %ld\n", WSAGetLastError() );
    closesocket(ListenSocket);
    WSACleanup();
    return 1;
}
```



Étape suivante : [accepter une connexion](accepting-a-connection.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Application de serveur Winsock](winsock-server-application.md)
</dt> <dt>

[Liaison d’un socket](binding-a-socket.md)
</dt> </dl>

 

 



