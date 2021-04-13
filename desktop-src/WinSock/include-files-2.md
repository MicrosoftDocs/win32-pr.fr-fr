---
description: Le fichier include d’origine à utiliser avec Windows Sockets 1,1 était le fichier d’en-tête Winsock. h.
ms.assetid: 0536abcc-4277-4bd8-927c-3bf429bc65bb
title: Fichiers include
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf7a4edcd70e6a6280b26f7b6ab9f0f1dab674e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318377"
---
# <a name="include-files"></a>Fichiers include

Le fichier include d’origine à utiliser avec Windows Sockets 1,1 était le fichier d’en-tête *Winsock. h* . Pour faciliter le portage du code source existant basé sur des sockets Berkeley UNIX vers Windows Sockets, les kits de développement Windows Sockets pour Winsock 1,1 ont été encouragés à être fournis avec plusieurs fichiers include portant le même nom que les fichiers d’en-tête UNIX */Socket. h* et ARPA/inet. h, par exemple). Toutefois, ces fichiers d’en-tête Winsock de même nom contiennent simplement une directive pour inclure le fichier d’en-tête *Winsock2. h* .

Lorsque Windows Sockets 2 a été publié, le fichier include principal pour une utilisation avec Windows Sockets a été renommé *Winsock2. h*. L’ancien fichier d’en-tête *Winsock. h* d’origine pour Winsock 1,1 a également été conservé pour la compatibilité avec les applications plus anciennes. Le développement d’applications compatibles Winsock 1,1 est déconseillé depuis la sortie de Windows 2000. Toutes les applications doivent maintenant utiliser la directive include *Winsock2. h* dans les fichiers sources de l’application Winsock.

Le fichier d’en-tête *Winsock2. h* contient la plupart des fonctions, structures et définitions Winsock. Le fichier d’en-tête *Ws2tcpip. h* contient les définitions présentées dans le document de l’annexe WinSock 2 Protocol-Specific pour TCP/IP, qui inclut des fonctions et structures plus récentes utilisées pour récupérer des adresses IP. Il s’agit notamment de la famille de fonctions [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) et [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) qui fournissent la résolution de noms pour les adresses IPv4 ou IPv6. Le fichier d’en-tête *Ws2tcpip. h* n’est nécessaire que si ces fonctions d’attribution de noms IP indépendantes sont requises par l’application.

Le fichier d’en-tête *mswsock. h* contient des définitions pour les extensions spécifiques à Microsoft pour Windows Sockets 2 ([**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile), [**accepted**](/windows/win32/api/mswsock/nf-mswsock-acceptex)et [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), par exemple). Le fichier d’en-tête *mswsock. h* n’est normalement pas nécessaire, sauf si ces extensions spécifiques à Microsoft sont utilisées par l’application.

Le fichier d’en-tête *Winsock2. h* inclut en interne les éléments principaux du fichier d’en-tête *Windows. h* . il n’y a donc pas \# de ligne include pour le fichier d’en-tête *Windows. h* dans les applications Winsock. Si une \# ligne include est nécessaire pour le fichier d’en-tête *Windows. h* , elle doit être précédée de la \# macro define Win32 \_ maigre \_ and \_ Mean. Pour des raisons historiques, l’en-tête *Windows. h* inclut par défaut le fichier d’en-tête *Winsock. h* pour Windows Sockets 1,1. Les déclarations du fichier d’en-tête *Winsock. h* sont en conflit avec les déclarations dans le fichier d’en-tête *Winsock2. h* requis par Windows Sockets 2. La \_ \_ \_ macro moyenne et moyenne Win32 empêche l’inclusion de *Winsock. h* par l’en-tête *Windows. h* . Vous trouverez ci-dessous un exemple illustrant cette illustration.


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une application Winsock de base](creating-a-basic-winsock-application.md)
</dt> <dt>

[Prise en main avec Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Portage d’applications de socket vers Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considérations sur la programmation Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 
