---
description: L' \_ erreur de socket de constante de manifeste est fournie pour vérifier l’échec de la fonction. Bien que l’utilisation de cette constante ne soit pas obligatoire, elle est recommandée. L’exemple suivant illustre l’utilisation de la constante d' \_ erreur de Socket.
ms.assetid: b46203dc-5666-413b-90fe-8432318f3037
title: Valeurs de retour en cas d’échec de la fonction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b277da114c8c86c53339590eeff3e831cbaf2a4277765bf53047b3d07991b026
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740931"
---
# <a name="return-values-on-function-failure"></a>Valeurs de retour en cas d’échec de la fonction

L’erreur de **socket \_** de constante de manifeste est fournie pour vérifier l’échec de la fonction. Bien que l’utilisation de cette constante ne soit pas obligatoire, elle est recommandée. L’exemple suivant illustre l’utilisation de la constante **d' \_ erreur de socket** .

Style BSD classique (ne fonctionne pas sur Windows)


```C++
        r = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (r == -1     /* or r < 0 */
            && errno == EWOULDBLOCK) {
            printf("recv failed with error: EWOULDBLOCK\n");
        }    
```



Windows Style


```C++
        iResult = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (iResult == SOCKET_ERROR ) {
            iError = WSAGetLastError();
            if (iError == WSAEWOULDBLOCK)
                printf("recv failed with error: WSAEWOULDBLOCK\n");
            else
                printf("recv failed with error: %ld\n", iError);

            closesocket(ClientSocket);
            WSACleanup();
            return 1;
        }    
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Codes d’erreur-errno, h \_ errno et WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[Gestion des erreurs Winsock](handling-winsock-errors.md)
</dt> <dt>

[Portage d’applications de socket vers Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considérations sur la programmation Winsock](winsock-programming-considerations.md)
</dt> <dt>

[Windows Codes d’erreur des sockets](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



