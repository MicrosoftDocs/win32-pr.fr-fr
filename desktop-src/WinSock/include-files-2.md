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
# <a name="include-files"></a><span data-ttu-id="d07c9-103">Fichiers include</span><span class="sxs-lookup"><span data-stu-id="d07c9-103">Include Files</span></span>

<span data-ttu-id="d07c9-104">Le fichier include d’origine à utiliser avec Windows Sockets 1,1 était le fichier d’en-tête *Winsock. h* .</span><span class="sxs-lookup"><span data-stu-id="d07c9-104">The original include file for use with Windows Sockets 1.1 was the *Winsock.h* header file.</span></span> <span data-ttu-id="d07c9-105">Pour faciliter le portage du code source existant basé sur des sockets Berkeley UNIX vers Windows Sockets, les kits de développement Windows Sockets pour Winsock 1,1 ont été encouragés à être fournis avec plusieurs fichiers include portant le même nom que les fichiers d’en-tête UNIX */Socket. h* et ARPA/inet. h, par exemple).</span><span class="sxs-lookup"><span data-stu-id="d07c9-105">To ease porting existing source code based on Berkeley UNIX sockets to Windows sockets, Windows Sockets development kits for Winsock 1.1 were encouraged to be supplied with several include files with the same names as standard UNIX include files (the *sys/socket.h* and arpa/inet.h header files, for example).</span></span> <span data-ttu-id="d07c9-106">Toutefois, ces fichiers d’en-tête Winsock de même nom contiennent simplement une directive pour inclure le fichier d’en-tête *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="d07c9-106">However, these similarly-name Winsock header files merely contained a directive to include the *Winsock2.h* header file.</span></span>

<span data-ttu-id="d07c9-107">Lorsque Windows Sockets 2 a été publié, le fichier include principal pour une utilisation avec Windows Sockets a été renommé *Winsock2. h*.</span><span class="sxs-lookup"><span data-stu-id="d07c9-107">When Windows Sockets 2 was released, the primary include file for use with Windows Sockets was renamed to *Winsock2.h*.</span></span> <span data-ttu-id="d07c9-108">L’ancien fichier d’en-tête *Winsock. h* d’origine pour Winsock 1,1 a également été conservé pour la compatibilité avec les applications plus anciennes.</span><span class="sxs-lookup"><span data-stu-id="d07c9-108">The older original *Winsock.h* header file for Winsock 1.1 was also retained for compatibility with older applications.</span></span> <span data-ttu-id="d07c9-109">Le développement d’applications compatibles Winsock 1,1 est déconseillé depuis la sortie de Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d07c9-109">The development of Winsock 1.1 compatible applications has been deprecated since Windows 2000 was released.</span></span> <span data-ttu-id="d07c9-110">Toutes les applications doivent maintenant utiliser la directive include *Winsock2. h* dans les fichiers sources de l’application Winsock.</span><span class="sxs-lookup"><span data-stu-id="d07c9-110">All applications should now use use the include *Winsock2.h* directive in Winsock application source files.</span></span>

<span data-ttu-id="d07c9-111">Le fichier d’en-tête *Winsock2. h* contient la plupart des fonctions, structures et définitions Winsock.</span><span class="sxs-lookup"><span data-stu-id="d07c9-111">The *Winsock2.h* header file contains most of the Winsock functions, structures, and definitions.</span></span> <span data-ttu-id="d07c9-112">Le fichier d’en-tête *Ws2tcpip. h* contient les définitions présentées dans le document de l’annexe WinSock 2 Protocol-Specific pour TCP/IP, qui inclut des fonctions et structures plus récentes utilisées pour récupérer des adresses IP.</span><span class="sxs-lookup"><span data-stu-id="d07c9-112">The *Ws2tcpip.h* header file contains definitions introduced in the WinSock 2 Protocol-Specific Annex document for TCP/IP that includes newer functions and structures used to retrieve IP addresses.</span></span> <span data-ttu-id="d07c9-113">Il s’agit notamment de la famille de fonctions [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) et [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) qui fournissent la résolution de noms pour les adresses IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="d07c9-113">These include the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) family of functions that provide name resolution for both IPv4 or IPv6 addresses.</span></span> <span data-ttu-id="d07c9-114">Le fichier d’en-tête *Ws2tcpip. h* n’est nécessaire que si ces fonctions d’attribution de noms IP indépendantes sont requises par l’application.</span><span class="sxs-lookup"><span data-stu-id="d07c9-114">The *Ws2tcpip.h* header file is only needed if these IP-agnostic naming functions are required by the application.</span></span>

<span data-ttu-id="d07c9-115">Le fichier d’en-tête *mswsock. h* contient des définitions pour les extensions spécifiques à Microsoft pour Windows Sockets 2 ([**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile), [**accepted**](/windows/win32/api/mswsock/nf-mswsock-acceptex)et [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), par exemple).</span><span class="sxs-lookup"><span data-stu-id="d07c9-115">The *Mswsock.h* header file contains definitions for Microsoft-specific extensions to the Windows Sockets 2 ([**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), and [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), for example).</span></span> <span data-ttu-id="d07c9-116">Le fichier d’en-tête *mswsock. h* n’est normalement pas nécessaire, sauf si ces extensions spécifiques à Microsoft sont utilisées par l’application.</span><span class="sxs-lookup"><span data-stu-id="d07c9-116">The *Mswsock.h* header file is not normally needed unless these Microsoft-specific extensions are used by the application.</span></span>

<span data-ttu-id="d07c9-117">Le fichier d’en-tête *Winsock2. h* inclut en interne les éléments principaux du fichier d’en-tête *Windows. h* . il n’y a donc pas \# de ligne include pour le fichier d’en-tête *Windows. h* dans les applications Winsock.</span><span class="sxs-lookup"><span data-stu-id="d07c9-117">The *Winsock2.h* header file internally includes core elements from the *Windows.h* header file, so there is not usually an \#include line for the *Windows.h* header file in Winsock applications.</span></span> <span data-ttu-id="d07c9-118">Si une \# ligne include est nécessaire pour le fichier d’en-tête *Windows. h* , elle doit être précédée de la \# macro define Win32 \_ maigre \_ and \_ Mean.</span><span class="sxs-lookup"><span data-stu-id="d07c9-118">If an \#include line is needed for the *Windows.h* header file, this should be preceded with the \#define WIN32\_LEAN\_AND\_MEAN macro.</span></span> <span data-ttu-id="d07c9-119">Pour des raisons historiques, l’en-tête *Windows. h* inclut par défaut le fichier d’en-tête *Winsock. h* pour Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="d07c9-119">For historical reasons, the *Windows.h* header defaults to including the *Winsock.h* header file for Windows Sockets 1.1.</span></span> <span data-ttu-id="d07c9-120">Les déclarations du fichier d’en-tête *Winsock. h* sont en conflit avec les déclarations dans le fichier d’en-tête *Winsock2. h* requis par Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="d07c9-120">The declarations in the *Winsock.h* header file will conflict with the declarations in the *Winsock2.h* header file required by Windows Sockets 2.</span></span> <span data-ttu-id="d07c9-121">La \_ \_ \_ macro moyenne et moyenne Win32 empêche l’inclusion de *Winsock. h* par l’en-tête *Windows. h* .</span><span class="sxs-lookup"><span data-stu-id="d07c9-121">The WIN32\_LEAN\_AND\_MEAN macro prevents the *Winsock.h* from being included by the *Windows.h* header.</span></span> <span data-ttu-id="d07c9-122">Vous trouverez ci-dessous un exemple illustrant cette illustration.</span><span class="sxs-lookup"><span data-stu-id="d07c9-122">An example illustrating this is shown below.</span></span>


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



## <a name="related-topics"></a><span data-ttu-id="d07c9-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d07c9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d07c9-124">Création d’une application Winsock de base</span><span class="sxs-lookup"><span data-stu-id="d07c9-124">Creating a Basic Winsock Application</span></span>](creating-a-basic-winsock-application.md)
</dt> <dt>

[<span data-ttu-id="d07c9-125">Prise en main avec Winsock</span><span class="sxs-lookup"><span data-stu-id="d07c9-125">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="d07c9-126">Portage d’applications de socket vers Winsock</span><span class="sxs-lookup"><span data-stu-id="d07c9-126">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="d07c9-127">Considérations sur la programmation Winsock</span><span class="sxs-lookup"><span data-stu-id="d07c9-127">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 
