---
description: Lorsque vous ajoutez la prise en charge d’IPv6, vous devez vous assurer que votre application définit des structures de données de taille correcte.
ms.assetid: 2bf353e2-38d5-462c-9e6c-65886b617215
title: Modification des structures de données pour IPv6 Winsock appications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2c91e19ed733d111bd4e12d824da6ee1a988e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515452"
---
# <a name="changing-data-structures-for-ipv6-winsock-appications"></a><span data-ttu-id="29a1c-103">Modification des structures de données pour IPv6 Winsock appications</span><span class="sxs-lookup"><span data-stu-id="29a1c-103">Changing Data Structures for IPv6 Winsock Appications</span></span>

<span data-ttu-id="29a1c-104">Lorsque vous ajoutez la prise en charge d’IPv6, vous devez vous assurer que votre application définit des structures de données de taille correcte.</span><span class="sxs-lookup"><span data-stu-id="29a1c-104">When adding support for IPv6, you must ensure that your application defines properly sized data structures.</span></span> <span data-ttu-id="29a1c-105">La taille d’une adresse IPv6 est bien supérieure à celle d’une adresse IPv4.</span><span class="sxs-lookup"><span data-stu-id="29a1c-105">The size of an IPv6 address is much larger than an IPv4 address.</span></span> <span data-ttu-id="29a1c-106">Les structures qui sont codées en dur pour gérer la taille d’une adresse IPv4 lors du stockage d’une adresse IP entraînent des problèmes dans votre application et doivent être modifiées.</span><span class="sxs-lookup"><span data-stu-id="29a1c-106">Structures that are hard-coded to handle the size of an IPv4 address when storing an IP address will cause problems in your application, and must be modified.</span></span>

<span data-ttu-id="29a1c-107">Bonne pratique</span><span class="sxs-lookup"><span data-stu-id="29a1c-107">Best Practice</span></span>

<span data-ttu-id="29a1c-108">La meilleure approche pour s’assurer que vos structures sont correctement dimensionnées consiste à utiliser la structure de [**\_ stockage sockaddr**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="29a1c-108">The best approach to ensuring that your structures are properly sized is to use the [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) structure.</span></span> <span data-ttu-id="29a1c-109">La structure de **\_ stockage sockaddr** est agnostique à la version de l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="29a1c-109">The **SOCKADDR\_STORAGE** structure is agnostic to IP address version.</span></span> <span data-ttu-id="29a1c-110">Lorsque la structure de **\_ stockage sockaddr** est utilisée pour stocker des adresses IP, les adresses IPv4 et IPv6 peuvent être gérées correctement avec une seule base de code.</span><span class="sxs-lookup"><span data-stu-id="29a1c-110">When the **SOCKADDR\_STORAGE** structure is used to store IP addresses, IPv4 and IPv6 addresses can be properly handled with one code base.</span></span>

<span data-ttu-id="29a1c-111">L’exemple suivant, qui est un extrait du fichier Server. c figurant dans l’annexe B, identifie une utilisation appropriée de la structure **de \_ stockage sockaddr** .</span><span class="sxs-lookup"><span data-stu-id="29a1c-111">The following example, which is an excerpt taken from the Server.c file found in Appendix B, identifies an appropriate use of the **SOCKADDR\_STORAGE** structure.</span></span> <span data-ttu-id="29a1c-112">Notez que la structure, quand elle est utilisée correctement, comme le montre cet exemple, gère correctement une adresse IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="29a1c-112">Notice that the structure, when used properly as this example shows, gracefully handles either an IPv4 or IPv6 address.</span></span>


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
> <span data-ttu-id="29a1c-113">La structure de [**\_ stockage sockaddr**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) est une nouveauté pour Windows XP.</span><span class="sxs-lookup"><span data-stu-id="29a1c-113">The [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) structure is new for Windows XP.</span></span>

 

<span data-ttu-id="29a1c-114">Code pour éviter</span><span class="sxs-lookup"><span data-stu-id="29a1c-114">Code To Avoid</span></span>

<span data-ttu-id="29a1c-115">En règle générale, de nombreuses applications utilisaient la structure [**sockaddr**](sockaddr-2.md) pour stocker des adresses indépendantes du protocole ou **sockaddr \_ dans** une structure pour les adresses IP.</span><span class="sxs-lookup"><span data-stu-id="29a1c-115">Typically, many applications used the [**sockaddr**](sockaddr-2.md) structure to store protocol-independent addresses, or the **sockaddr\_in** structure for IP addresses.</span></span> <span data-ttu-id="29a1c-116">Ni la structure sockaddr ni le **sockaddr \_ de** structure ne sont suffisamment volumineux pour contenir des adresses IPv6, et par conséquent, les deux sont insuffisantes si votre application doit être compatible avec IPv6.</span><span class="sxs-lookup"><span data-stu-id="29a1c-116">Neither the sockaddr structure nor the **sockaddr\_in** structure is large enough to hold IPv6 addresses, and therefore both are insufficient if your application is to be IPv6 compatible.</span></span>

<span data-ttu-id="29a1c-117">Tâche de codage</span><span class="sxs-lookup"><span data-stu-id="29a1c-117">Coding Task</span></span>

<span data-ttu-id="29a1c-118">**Pour modifier votre base de code existante de IPv4 en IPv4 et IPv6-interopérabilité**</span><span class="sxs-lookup"><span data-stu-id="29a1c-118">**To modify your existing code base from IPv4 to IPv4- and IPv6-interoperability**</span></span>

1.  <span data-ttu-id="29a1c-119">Acquérir l’utilitaire Checkv4.exe.</span><span class="sxs-lookup"><span data-stu-id="29a1c-119">Acquire the Checkv4.exe utility.</span></span> <span data-ttu-id="29a1c-120">L’utilitaire est inclus dans le kit de développement logiciel (SDK) Microsoft Windows, qui est disponible par le biais de votre abonnement MSDN, ou à partir du Web en téléchargement.</span><span class="sxs-lookup"><span data-stu-id="29a1c-120">The utility is included with the Microsoft Windows Software Development Kit (SDK) which is made available through your MSDN subscription, or from the web as a download.</span></span>
2.  <span data-ttu-id="29a1c-121">Exécutez l’utilitaire Checkv4.exe sur votre code.</span><span class="sxs-lookup"><span data-stu-id="29a1c-121">Run the Checkv4.exe utility against your code.</span></span> <span data-ttu-id="29a1c-122">Découvrez comment exécuter l’utilitaire Checkv4.exe sur vos fichiers dans la section relative à l' [utilisation de l’utilitaire Checkv4.exe](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="29a1c-122">Learn about how to run the Checkv4.exe utility against your files in the section on [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span>
3.  <span data-ttu-id="29a1c-123">L’utilitaire vous avertit de l’utilisation de **sockaddr** ou **sockaddr \_ dans** les structures, et fournit des recommandations sur la façon de remplacer soit par la structure compatible IPv6 [**sockaddr le \_ stockage**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="29a1c-123">The utility alerts you to usage of **sockaddr** or **sockaddr\_in** structures, and provides recommendations on how to replace either with the IPv6 compatible structure [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)).</span></span>
4.  <span data-ttu-id="29a1c-124">Remplacez toutes les instances de ce type et le code associé selon le cas, pour utiliser la structure de **\_ stockage sockaddr** .</span><span class="sxs-lookup"><span data-stu-id="29a1c-124">Replace any such instances, and associated code as appropriate, to use the **SOCKADDR\_STORAGE** structure.</span></span>

<span data-ttu-id="29a1c-125">Vous pouvez également rechercher dans votre base de code des instances de **sockaddr** et **sockaddr \_ dans** les structures, puis modifier toute l’utilisation (et tout autre code associé, le cas échéant) vers la structure de **\_ stockage sockaddr** .</span><span class="sxs-lookup"><span data-stu-id="29a1c-125">Alternatively, you can search your code base for instances of the **sockaddr** and **sockaddr\_in** structures, and change all such usage (and other associated code, as appropriate) to the **SOCKADDR\_STORAGE** structure.</span></span>

> [!Note]  
> <span data-ttu-id="29a1c-126">Les structures de **\_ stockage** **addrinfo** et sockaddr incluent respectivement les membres de famille de protocole et d’adresse (famille **ai \_** et **SS \_**).</span><span class="sxs-lookup"><span data-stu-id="29a1c-126">The **addrinfo** and **SOCKADDR\_STORAGE** structures include protocol and address family members (**ai\_family** and **ss\_family**), respectively.</span></span> <span data-ttu-id="29a1c-127">La RFC 2553 spécifie le membre de la **\_ famille ai** de [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) en tant que int, tandis que la **\_ famille SS** est spécifiée en tant que Short. par conséquent, une copie directe entre ces membres entraîne une erreur du compilateur.</span><span class="sxs-lookup"><span data-stu-id="29a1c-127">RFC 2553 specifies the **ai\_family** member of [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) as an int, while **ss\_family** is specified as a short; as such, a direct copy between those members results in a compiler error.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="29a1c-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="29a1c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29a1c-129">Guide IPv6 pour les applications Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="29a1c-129">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="29a1c-130">Sockets à double pile pour les applications Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="29a1c-130">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="29a1c-131">Appels de fonction pour les applications Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="29a1c-131">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
</dt> <dt>

[<span data-ttu-id="29a1c-132">Utilisation d’adresses IPv4 codées en dur</span><span class="sxs-lookup"><span data-stu-id="29a1c-132">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="29a1c-133">Problèmes d’interface utilisateur pour les applications Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="29a1c-133">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> <dt>

[<span data-ttu-id="29a1c-134">Protocoles sous-jacents pour les applications Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="29a1c-134">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
</dt> </dl>

 

 
