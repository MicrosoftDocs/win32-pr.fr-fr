---
description: Une fois que le socket est lié à une adresse IP et à un port sur le système, le serveur doit ensuite écouter cette adresse IP et ce port pour les demandes de connexion entrante.
ms.assetid: 83c9f0e7-2e6d-449b-8d97-3d13154112cd
title: Écoute sur un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d6d98a13fc6e994fb5a264827b6b93047fd24e03d3e3f9953203b1fa15140f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569779"
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

 

 



