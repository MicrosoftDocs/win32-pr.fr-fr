---
description: Lorsque vous ajoutez la prise en charge d’IPv6, vous devez vous assurer que votre application définit des structures de données de taille correcte.
ms.assetid: 2bf353e2-38d5-462c-9e6c-65886b617215
title: Modification des structures de données pour IPv6 Winsock appications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2999c0d0c5a335c1367165c227fc1aad805579db5a790a19d316a1624e922947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741549"
---
# <a name="changing-data-structures-for-ipv6-winsock-appications"></a>Modification des structures de données pour IPv6 Winsock appications

Lorsque vous ajoutez la prise en charge d’IPv6, vous devez vous assurer que votre application définit des structures de données de taille correcte. La taille d’une adresse IPv6 est bien supérieure à celle d’une adresse IPv4. Les structures qui sont codées en dur pour gérer la taille d’une adresse IPv4 lors du stockage d’une adresse IP entraînent des problèmes dans votre application et doivent être modifiées.

Bonne pratique

La meilleure approche pour s’assurer que vos structures sont correctement dimensionnées consiste à utiliser la structure de [**\_ stockage sockaddr**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) . La structure de **\_ stockage sockaddr** est agnostique à la version de l’adresse IP. Lorsque la structure de **\_ stockage sockaddr** est utilisée pour stocker des adresses IP, les adresses IPv4 et IPv6 peuvent être gérées correctement avec une seule base de code.

L’exemple suivant, qui est un extrait du fichier Server. c figurant dans l’annexe B, identifie une utilisation appropriée de la structure **de \_ stockage sockaddr** . Notez que la structure, quand elle est utilisée correctement, comme le montre cet exemple, gère correctement une adresse IPv4 ou IPv6.


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

#define BUFFER_SIZE 512
#define DEFAULT_PORT "27015"

int main(int argc, char **argv)
{
    char Buffer[BUFFER_SIZE] = {0};
    char *Hostname;
    int Family = AF_UNSPEC;
    int SocketType = SOCK_STREAM;
    char *Port = DEFAULT_PORT;
    char *Address = NULL;
    int i = 0;
    DWORD dwRetval = 0;
    int iResult = 0;
    int FromLen = 0;
    int AmountRead = 0;

    SOCKADDR_STORAGE From;

    WSADATA wsaData;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;

    // Parse arguments
    if (argc >= 1) {
        Hostname = argv[1];
    }    

   // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }

    From.ss_family = (ADDRESS_FAMILY) Family;
    
    //...
        
        return 0;
}
```



> [!Note]  
> la structure de [**\_ stockage SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) est une nouveauté pour Windows XP.

 

Code pour éviter

En règle générale, de nombreuses applications utilisaient la structure [**sockaddr**](sockaddr-2.md) pour stocker des adresses indépendantes du protocole ou **sockaddr \_ dans** une structure pour les adresses IP. Ni la structure sockaddr ni le **sockaddr \_ de** structure ne sont suffisamment volumineux pour contenir des adresses IPv6, et par conséquent, les deux sont insuffisantes si votre application doit être compatible avec IPv6.

Tâche de codage

**Pour modifier votre base de code existante de IPv4 en IPv4 et IPv6-interopérabilité**

1.  Acquérir l’utilitaire Checkv4.exe. l’utilitaire est inclus dans le kit de développement logiciel (SDK) de Microsoft Windows, qui est disponible par le biais de votre abonnement MSDN, ou à partir du web en téléchargement.
2.  Exécutez l’utilitaire Checkv4.exe sur votre code. Découvrez comment exécuter l’utilitaire Checkv4.exe sur vos fichiers dans la section relative à l' [utilisation de l’utilitaire Checkv4.exe](using-the-checkv4-exe-utility-2.md).
3.  L’utilitaire vous avertit de l’utilisation de **sockaddr** ou **sockaddr \_ dans** les structures, et fournit des recommandations sur la façon de remplacer soit par la structure compatible IPv6 [**sockaddr le \_ stockage**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)).
4.  Remplacez toutes les instances de ce type et le code associé selon le cas, pour utiliser la structure de **\_ stockage sockaddr** .

Vous pouvez également rechercher dans votre base de code des instances de **sockaddr** et **sockaddr \_ dans** les structures, puis modifier toute l’utilisation (et tout autre code associé, le cas échéant) vers la structure de **\_ stockage sockaddr** .

> [!Note]  
> Les structures de **\_ stockage** **addrinfo** et sockaddr incluent respectivement les membres de famille de protocole et d’adresse (famille **ai \_** et **SS \_**). La RFC 2553 spécifie le membre de la **\_ famille ai** de [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) en tant que int, tandis que la **\_ famille SS** est spécifiée en tant que Short. par conséquent, une copie directe entre ces membres entraîne une erreur du compilateur.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide IPv6 pour les Applications Windows sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Sockets à double pile pour les applications Winsock IPv6](dual-stack-sockets.md)
</dt> <dt>

[Appels de fonction pour les applications Winsock IPv6](function-calls-2.md)
</dt> <dt>

[Utilisation d’adresses IPv4 codées en dur](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Problèmes d’interface utilisateur pour les applications Winsock IPv6](user-interface-issues-2.md)
</dt> <dt>

[Protocoles sous-jacents pour les applications Winsock IPv6](underlying-protocols-2.md)
</dt> </dl>

 

 
