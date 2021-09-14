---
description: L' \_ option de socket so EXCLUSIVEADDRUSE empêche d’autres Sockets d’être liés de force à la même adresse et au même port.
ms.assetid: ce0d8188-54be-46e8-8753-d0680f690b84
title: Option de socket SO_EXCLUSIVEADDRUSE (Winsock2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d4747150f918a7e9c4ce37ec209e7261d1a00c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292223"
---
# <a name="so_exclusiveaddruse-socket-option"></a>SO \_ EXCLUSIVEADDRUSE option de socket

L' \_ option de socket so EXCLUSIVEADDRUSE empêche d’autres Sockets d’être liés de force à la même adresse et au même port.

## <a name="syntax"></a>Syntaxe

L' \_ option so EXCLUSIVEADDRUSE empêche d’autres Sockets d’être liés de force à la même adresse et au même port, une pratique activée par l' \_ option de socket REUSEADDR. Une telle réutilisation peut être exécutée par des applications malveillantes pour interrompre l’application. L' \_ option so EXCLUSIVEADDRUSE est très utile pour les services système nécessitant une haute disponibilité.

L’exemple de code suivant illustre la définition de cette option.


```C++
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>
#include <stdlib.h>             // Needed for _wtoi

#pragma comment(lib, "Ws2_32.lib")

int __cdecl wmain(int argc, wchar_t ** argv)
{
    WSADATA wsaData;
    int iResult = 0;
    int iError = 0;

    SOCKET s = INVALID_SOCKET;
    SOCKADDR_IN saLocal;
    int iOptval = 0;

    int iFamily = AF_UNSPEC;
    int iType = 0;
    int iProtocol = 0;

    int iPort = 0;

    // Validate the parameters
    if (argc != 5) {
        wprintf(L"usage: %ws <addressfamily> <type> <protocol> <port>\n", argv[0]);
        wprintf(L"    opens a socket for the specified family, type, & protocol\n");
        wprintf(L"    sets the SO_EXCLUSIVEADDRUSE socket option on the socket\n");
        wprintf(L"    then tries to bind the port specified on the command-line\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 0 2 17 5150\n", argv[0]);
        wprintf(L"   where AF_UNSPEC=0 SOCK_DGRAM=2 IPPROTO_UDP=17  PORT=5150\n",
                argv[0]);
        wprintf(L"   %ws 2 1 17 5150\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_STREAM=1 IPPROTO_TCP=6  PORT=5150\n", argv[0]);
        wprintf(L"   See the documentation for the socket function for other values\n");
        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    iPort = _wtoi(argv[4]);

    if (iFamily != AF_INET && iFamily != AF_INET6) {
        wprintf(L"Address family must be either AF_INET (2) or AF_INET6 (23)\n");
        return 1;
    }

    if (iPort <= 0 || iPort >= 65535) {
        wprintf(L"Port specified must be greater than 0 and less than 65535\n");
        return 1;
    }
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error: %d\n", iResult);
        return 1;
    }
    // Create the socket
    s = socket(iFamily, iType, iProtocol);
    if (s == INVALID_SOCKET) {
        wprintf(L"socket failed with error: %ld\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    // Set the exclusive address option
    iOptval = 1;
    iResult = setsockopt(s, SOL_SOCKET, SO_EXCLUSIVEADDRUSE,
                         (char *) &iOptval, sizeof (iOptval));
    if (iResult == SOCKET_ERROR) {
        wprintf(L"setsockopt for SO_EXCLUSIVEADDRUSE failed with error: %ld\n",
                WSAGetLastError());
    }

    saLocal.sin_family = (ADDRESS_FAMILY) iFamily;
    saLocal.sin_port = htons( (u_short) iPort);
    saLocal.sin_addr.s_addr = htonl(INADDR_ANY);

    // Bind the socket
    iResult = bind(s, (SOCKADDR *) & saLocal, sizeof (saLocal));
    if (iResult == SOCKET_ERROR) {

        // Most errors related to setting SO_EXCLUSIVEADDRUSE
        //    will occur at bind.
        iError = WSAGetLastError();
        if (iError == WSAEACCES)
            wprintf(L"bind failed with WSAEACCES (access denied)\n");
        else
            wprintf(L"bind failed with error: %ld\n", iError);

    } else {
        wprintf(L"bind on socket with SO_EXCLUSIVEADDRUSE succeeded to port: %ld\n",
                iPort);
    }

    // cleanup
    closesocket(s);
    WSACleanup();

    return 0;
}

```



Pour avoir un effet, l' \_ option so EXCLUSIVADDRUSE doit être définie avant l’appel de la fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) (cela s’applique également à l' \_ option so REUSEADDR). Le tableau 1 répertorie les effets de la définition de l' \_ option so EXCLUSIVEADDRUSE. Caractère générique indique la liaison à l’adresse générique, telle que 0.0.0.0 pour IPv4 et :: pour IPv6. Spécifique indique la liaison à une interface spécifique, telle que la liaison d’une adresse IP assignée à un adaptateur. Specific2 indique la liaison à une adresse spécifique autre que l’adresse liée dans le cas spécifique.

> [!Note]  
> Le cas Specific2 s’applique uniquement lorsque la première liaison est effectuée avec une adresse spécifique ; dans le cas où le premier Socket est lié au caractère générique, l’entrée pour spécifique couvre tous les cas d’adresse spécifiques.

 

Par exemple, imaginez un ordinateur avec deux interfaces IP : 10.0.0.1 et 10.99.99.99. Si la première liaison a pour valeur 10.0.0.1 et le port 5150 avec l' \_ option so EXCLUSIVEADDRUSE définie, alors la deuxième liaison à 10.99.99.99 et le port 5150 avec une ou plusieurs options définies (ou aucune) sont exécutées. Toutefois, si le premier Socket est lié à l’adresse générique (0.0.0.0) et au port 5150 avec \_ EXCLUSIVEADDRUSE défini, toute liaison suivante au même port, quelle que soit l’adresse IP, échouera avec WSAEADDRINUSE (10048) ou WSAEACCESS (10013), selon les options définies sur le deuxième socket de liaison.

### <a name="bind-behavior-with-various-options-set"></a>Comportement de liaison avec les différentes options définies



Deuxième liaison

Première liaison

*\_EXCLUSIVEADDRUSE*

*Aucune option* ou *\_ REUSEADDR*

*Caractère générique*

*Plus*

*Caractère générique*

*Plus*

$ {ROWSPAN3} $*donc \_ EXCLUSIVEADDRUSE*$ {Remove} $  

*Caractère générique*

Échec (10048)

Échec (10048)

Échec (10048)

Échec (10048)

*Plus*

Échec (10048)

Échec (10048)

Échec (10048)

Échec (10048)

*Specific2*

n/a

Succès

n/a

Succès

$ {ROWSPAN3} $*no options*$ {Remove} $  

*Caractère générique*

Échec (10048)

Échec (10048)

Échec (10048)

Échec (10048)

*Plus*

Échec (10048)

Échec (10048)

Échec (10048)

Échec (10048)

*Specific2*

n/a

Succès

n/a

Succès

$ {ROWSPAN3} $*donc \_ REUSEADDR*$ {Remove} $  

*Caractère générique*

Échec (10013)

Échec (10013)

Opération réussie\*

Succès

*Plus*

Échec (10013)

Échec (10013)

Succès

Opération réussie\*

*Specific2*

n/a

Succès

n/a

Succès

\* Le comportement n’est pas défini en ce qui concerne le socket qui recevra les paquets.



 

Dans le cas où la première liaison ne définit aucune option ou \_ REUSEADDR, et que la deuxième liaison exécute un so \_ REUSEADDR, le deuxième Socket a détenir le port et le comportement concernant le socket qui recevra les paquets. \_EXCLUSIVEADDRUSE a donc été introduit pour résoudre ce problème.

Un socket avec \_ EXCLUSIVEADDRUSE Set ne peut pas toujours être réutilisé immédiatement après la fermeture du Socket. Par exemple, si un socket d’écoute avec l’ensemble d’indicateurs exclusifs accepte une connexion après laquelle le socket d’écoute est fermé, un autre socket ne peut pas se lier au même port que le premier socket d’écoute avec l’indicateur exclusif tant que la connexion acceptée n’est plus active.

Cette situation peut être assez compliquée ; même si le socket a été fermé, le transport sous-jacent peut ne pas mettre fin à sa connexion. Même après la fermeture du socket, le système doit envoyer toutes les données mises en mémoire tampon, transmettre une déconnexion normale à l’homologue et attendre une déconnexion normale de l’homologue. Il est donc possible que le transport sous-jacent ne libère jamais la connexion, par exemple lorsque l’homologue publie une fenêtre de taille nulle, ou d’autres attaques. Dans l’exemple précédent, le socket d’écoute a été fermé après l’acceptation d’une connexion cliente. Désormais, même si la connexion client est fermée, le port ne peut pas être réutilisé si la connexion cliente reste dans un état actif en raison de données non acquittées, etc.

Pour éviter cette situation, les applications doivent garantir un arrêt correct : appeler [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) avec l' \_ indicateur SD Send, puis attendre dans une boucle [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) jusqu’à ce que zéro octet soit retourné. Cela permet d’éviter le problème associé à la réutilisation des ports, garantit que toutes les données ont été reçues par l’homologue et vérifie que toutes les données ont été reçues avec succès.

L’option si oui \_ peut être définie sur un socket pour empêcher le port de passer à l’un des États d’attente actifs ; Toutefois, cette opération est déconseillée, car cela peut entraîner des effets indésirables, car cela peut entraîner la réinitialisation de la connexion. Par exemple, si les données ont été reçues mais n’ont pas encore été acceptées par l’homologue, et que l’ordinateur local ferme le socket avec l’ensemble des éléments restants \_ , la connexion est réinitialisée et l’homologue ignore les données non acquittées. En outre, il est difficile de choisir une durée de maintien appropriée. une valeur trop petite entraîne de nombreuses connexions abandonnées, tandis qu’un délai d’expiration important peut rendre le système vulnérable aux attaques par déni de service en établissant de nombreuses connexions et en bloquant de nombreux threads d’application.

> [!Note]  
> Un socket qui utilise l’option SO \_ EXCLUSIVEADDRUSE doit être arrêté correctement avant de le fermer. Dans le cas contraire, vous risquez de provoquer une attaque par déni de service si le service associé doit redémarrer.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Winsock2. h</dt> </dl> |



 

 




