---
description: L' \_ erreur de socket de constante de manifeste est fournie pour vérifier l’échec de la fonction. Bien que l’utilisation de cette constante ne soit pas obligatoire, elle est recommandée. L’exemple suivant illustre l’utilisation de la constante d' \_ erreur de Socket.
ms.assetid: b46203dc-5666-413b-90fe-8432318f3037
title: Valeurs de retour en cas d’échec de la fonction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94280d47d705833528c03c0d98a4a31232a0c6a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416116"
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

 

 



