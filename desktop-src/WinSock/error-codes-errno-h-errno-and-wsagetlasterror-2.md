---
description: Dans les applications Winsock, les codes d’erreur sont récupérés à l’aide de la fonction WSAGetLastError, le substitut Windows Sockets pour la fonction Windows GetLastError.
ms.assetid: cb73fc92-74bd-4c8b-a1c0-6daf4d298aa1
title: Codes d’erreur-errno, h_errno et WSAGetLastError
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b547e0b580599aaec27a0b77bfad0ffaa8966e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515240"
---
# <a name="error-codes---errno-h_errno-and-wsagetlasterror"></a><span data-ttu-id="f21e2-103">Codes d’erreur-errno, h \_ errno et WSAGetLastError</span><span class="sxs-lookup"><span data-stu-id="f21e2-103">Error Codes - errno, h\_errno and WSAGetLastError</span></span>

<span data-ttu-id="f21e2-104">Dans les applications Winsock, les codes d’erreur sont récupérés à l’aide de la fonction [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) , le substitut Windows Sockets pour la fonction Windows [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="f21e2-104">In Winsock applications, error codes are retrieved using the [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) function, the Windows Sockets substitute for the Windows [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span> <span data-ttu-id="f21e2-105">Les codes d’erreur retournés par Windows Sockets sont similaires aux constantes de code d’erreur de socket UNIX, mais les constantes sont toutes précédées de WSA.</span><span class="sxs-lookup"><span data-stu-id="f21e2-105">The error codes returned by Windows Sockets are similar to UNIX socket error code constants, but the constants are all prefixed with WSA.</span></span> <span data-ttu-id="f21e2-106">Par conséquent, dans les applications Winsock, le code d’erreur WSAEWOULDBLOCK est retourné, tandis que dans les applications UNIX, le code d’erreur EWOULDBLOCK est retourné.</span><span class="sxs-lookup"><span data-stu-id="f21e2-106">So in Winsock applications the WSAEWOULDBLOCK error code would be returned, while in UNIX applications the EWOULDBLOCK error code would be returned.</span></span>

<span data-ttu-id="f21e2-107">Les codes d’erreur définis par Windows Sockets ne sont pas mis à disposition par le biais de la variable *errno* .</span><span class="sxs-lookup"><span data-stu-id="f21e2-107">Error codes set by Windows Sockets are not made available through the *errno* variable.</span></span> <span data-ttu-id="f21e2-108">En outre, pour la classe **getXbyY** des fonctions, les codes d’erreur ne sont pas rendus disponibles par le biais de la variable *h \_ errno* .</span><span class="sxs-lookup"><span data-stu-id="f21e2-108">Additionally, for the **getXbyY** class of functions, error codes are not made available through the *h\_errno* variable.</span></span> <span data-ttu-id="f21e2-109">La fonction [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) est conçue pour fournir un moyen fiable pour un thread dans un processus multithread d’obtenir des informations sur les erreurs par thread.</span><span class="sxs-lookup"><span data-stu-id="f21e2-109">The [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) function is intended to provide a reliable way for a thread in a multithreaded process to obtain per-thread error information.</span></span>

<span data-ttu-id="f21e2-110">Pour la compatibilité avec Berkeley UNIX (BSD), les versions antérieures de Windows (Windows 95 avec la mise à jour de Windows Socket 2 et Windows 98, par exemple) redéfinissent les constantes d’erreur Berkeley standard généralement présentes dans *errno. h* sur BSD en tant qu’erreurs WSA Windows Sockets équivalentes.</span><span class="sxs-lookup"><span data-stu-id="f21e2-110">For compatibility with Berkeley UNIX (BSD), early versions of Windows (Windows 95 with the Windows Socket 2 Update and Windows 98, for example) redefined regular Berkeley error constants typically found in *errno.h* on BSD as the equivalent Windows Sockets WSA errors.</span></span> <span data-ttu-id="f21e2-111">Par exemple, ECONNREFUSED a été défini en tant que **WSAECONNREFUSED** dans le fichier d’en-tête *Winsock. h* .</span><span class="sxs-lookup"><span data-stu-id="f21e2-111">So for example, ECONNREFUSED was defined as **WSAECONNREFUSED** in the *Winsock.h* header file.</span></span> <span data-ttu-id="f21e2-112">Dans les versions ultérieures de Windows (Windows NT 3,1 et versions ultérieures), ces définitions ont été commentées afin d’éviter les conflits avec *errno. h* utilisé avec Microsoft C/C++ et Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f21e2-112">In subsequent versions of Windows (Windows NT 3.1 and later) these defines were commented out to avoid conflicts with *errno.h* used with Microsoft C/C++ and Visual Studio.</span></span>

<span data-ttu-id="f21e2-113">Le fichier d’en-tête *Winsock2. h* inclus dans le kit de développement logiciel (SDK) Microsoft Windows, le kit de développement logiciel (SDK) de la plate-forme et Visual Studio contient toujours un bloc de définitions commentés dans un \# bloc ifdef 0 et \# endif qui définissent les codes d’erreur de socket BSD comme les constantes d’erreur wsa.</span><span class="sxs-lookup"><span data-stu-id="f21e2-113">The *Winsock2.h* header file included with the Microsoft Windows Software Development Kit (SDK), Platform Software Development Kit (SDK), and Visual Studio still contains a commented out block of defines within an \#ifdef 0 and \#endif block that define the BSD socket error codes to be the same as the WSA error constants.</span></span> <span data-ttu-id="f21e2-114">Elles peuvent être utilisées pour fournir une certaine compatibilité avec la programmation de sockets UNIX, BSD et Linux.</span><span class="sxs-lookup"><span data-stu-id="f21e2-114">These can be used to provide some compatibility with UNIX, BSD, and Linux socket programming.</span></span> <span data-ttu-id="f21e2-115">Pour la compatibilité avec BSD, une application peut choisir de modifier *Winsock2. h* et de supprimer les marques de commentaire de ce bloc.</span><span class="sxs-lookup"><span data-stu-id="f21e2-115">For compatibility with BSD, an application may choose to change the *Winsock2.h* and uncomment this block.</span></span> <span data-ttu-id="f21e2-116">Toutefois, les développeurs d’applications sont fortement déconseillés de supprimer les marques de commentaire de ce bloc en raison de conflits inévitables avec *errno. h* dans la plupart des applications.</span><span class="sxs-lookup"><span data-stu-id="f21e2-116">However, application developers are strongly discouraged from uncommenting this block because of inevitable conflicts with *errno.h* in most applications.</span></span> <span data-ttu-id="f21e2-117">En outre, les erreurs de socket BSD sont définies sur des valeurs très différentes de celles utilisées dans les programmes UNIX, BSD et Linux.</span><span class="sxs-lookup"><span data-stu-id="f21e2-117">Also, the BSD socket errors are defined to very different values than are used in UNIX, BSD, and Linux programs.</span></span> <span data-ttu-id="f21e2-118">Les développeurs d’applications sont fortement encouragés à utiliser les constantes d’erreur WSA dans les applications de Socket.</span><span class="sxs-lookup"><span data-stu-id="f21e2-118">Application developers are very strongly encouraged to use the WSA error constants in socket applications.</span></span>

<span data-ttu-id="f21e2-119">Ces définitions restent commentées dans l’en-tête *Winsock2. h* au sein d’un \# bloc ifdef 0 et \# endif.</span><span class="sxs-lookup"><span data-stu-id="f21e2-119">These defines remain commented out in the *Winsock2.h* header within an \#ifdef 0 and \#endif block.</span></span> <span data-ttu-id="f21e2-120">Si un développeur d’applications insiste sur l’utilisation des codes d’erreur BSD pour la compatibilité, une application peut choisir d’inclure une ligne du formulaire :</span><span class="sxs-lookup"><span data-stu-id="f21e2-120">If an application developer insists on using the BSD error codes for compatibility, then an application may choose to include a line of the form:</span></span>


```C++
#include <windows.h>

#define errno WSAGetLastError()
```



<span data-ttu-id="f21e2-121">Cela permet de disposer d’un code de mise en réseau écrit pour utiliser le *errno* global pour fonctionner correctement dans un environnement à thread unique.</span><span class="sxs-lookup"><span data-stu-id="f21e2-121">This allows networking code which was written to use the global *errno* to work correctly in a single-threaded environment.</span></span> <span data-ttu-id="f21e2-122">Il existe des inconvénients très sérieux.</span><span class="sxs-lookup"><span data-stu-id="f21e2-122">There are some very serious drawbacks.</span></span> <span data-ttu-id="f21e2-123">Si un fichier source comprend du code qui inspecte *errno* pour les fonctions socket et non socket, ce mécanisme ne peut pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="f21e2-123">If a source file includes code which inspects *errno* for both socket and non-socket functions, this mechanism cannot be used.</span></span> <span data-ttu-id="f21e2-124">En outre, il n’est pas possible pour une application d’affecter une nouvelle valeur à *errno*.</span><span class="sxs-lookup"><span data-stu-id="f21e2-124">Furthermore, it is not possible for an application to assign a new value to *errno*.</span></span> <span data-ttu-id="f21e2-125">(Dans Windows Sockets, la fonction [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) peut être utilisée à cet effet.)</span><span class="sxs-lookup"><span data-stu-id="f21e2-125">(In Windows Sockets, the function [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) may be used for this purpose.)</span></span>

<span data-ttu-id="f21e2-126">Style BSD classique</span><span class="sxs-lookup"><span data-stu-id="f21e2-126">Typical BSD Style</span></span>


```C++
r = recv(...);
if (r == -1
    && errno == EWOULDBLOCK)
    {...}
```



<span data-ttu-id="f21e2-127">Style préféré</span><span class="sxs-lookup"><span data-stu-id="f21e2-127">Preferred Style</span></span>


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == EWOULDBLOCK)
    {...}
```



<span data-ttu-id="f21e2-128">Bien que les constantes d’erreur cohérentes avec les sockets Berkeley 4,3 soient fournies à des fins de compatibilité, les applications sont vivement encouragées à utiliser les définitions de code d’erreur WSA.</span><span class="sxs-lookup"><span data-stu-id="f21e2-128">Although error constants consistent with Berkeley Sockets 4.3 are provided for compatibility purposes, applications are strongly encouraged to use the WSA error code definitions.</span></span> <span data-ttu-id="f21e2-129">Cela est dû au fait que les codes d’erreur retournés par certaines fonctions Windows Sockets se trouvent dans la plage standard de codes d’erreur, comme défini par Microsoft C ©.</span><span class="sxs-lookup"><span data-stu-id="f21e2-129">This is because error codes returned by certain Windows Sockets functions fall into the standard range of error codes as defined by Microsoft C©.</span></span> <span data-ttu-id="f21e2-130">Par conséquent, une meilleure version du fragment de code source précédent est :</span><span class="sxs-lookup"><span data-stu-id="f21e2-130">Thus, a better version of the preceding source code fragment is:</span></span>


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == WSAEWOULDBLOCK)
    {...}
```



<span data-ttu-id="f21e2-131">La spécification Winsock 1,1 d’origine définie dans 1995 a recommandé un ensemble de codes d’erreur et répertorie les erreurs possibles qui peuvent être retournées à la suite de chaque fonction.</span><span class="sxs-lookup"><span data-stu-id="f21e2-131">The original Winsock 1.1 specification defined in 1995 recommended a set of error codes, and listed the possible errors that can be returned as a result of each function.</span></span> <span data-ttu-id="f21e2-132">Windows Sockets 2 a ajouté des fonctions et des fonctionnalités avec d’autres codes d’erreur Windows Sockets retournés en plus de ceux listés dans la spécification Winsock d’origine.</span><span class="sxs-lookup"><span data-stu-id="f21e2-132">Windows Sockets 2 added functions and features with other Windows Sockets error codes returned in addition to those listed in the original Winsock specification.</span></span> <span data-ttu-id="f21e2-133">Des fonctions supplémentaires ont été ajoutées au fil du temps pour améliorer Winsock pour une utilisation par les développeurs.</span><span class="sxs-lookup"><span data-stu-id="f21e2-133">Additional functions have been added over time to enhance Winsock for use by developers.</span></span> <span data-ttu-id="f21e2-134">Par exemple, de nouvelles fonctions de service de nom ([**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) et [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo), par exemple) ont été ajoutées pour prendre en charge les protocoles IPv6 et IPv4 sur Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f21e2-134">For example, new name service functions ([**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo), for example) were added that support both IPv6 and IPv4 on Windows XP and later.</span></span> <span data-ttu-id="f21e2-135">Certaines des anciennes fonctions de service de nom IPv4 uniquement (la classe **getXbyY** des fonctions, par exemple) ont été dépréciées.</span><span class="sxs-lookup"><span data-stu-id="f21e2-135">Some of the older IPv4-only name service functions (the **getXbyY** class of functions, for example) have been deprecated.</span></span>

<span data-ttu-id="f21e2-136">La liste complète des codes d’erreur possibles renvoyés par les fonctions Windows Sockets est indiquée dans la section [codes d’erreur des Windows Sockets](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="f21e2-136">A complete list of possible error codes returned by Windows Sockets functions is given in the section on [Windows Sockets Error Codes](windows-sockets-error-codes-2.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f21e2-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f21e2-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f21e2-138">Gestion des erreurs Winsock</span><span class="sxs-lookup"><span data-stu-id="f21e2-138">Handling Winsock Errors</span></span>](handling-winsock-errors.md)
</dt> <dt>

[<span data-ttu-id="f21e2-139">Portage d’applications de socket vers Winsock</span><span class="sxs-lookup"><span data-stu-id="f21e2-139">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="f21e2-140">Codes d’erreur de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="f21e2-140">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> <dt>

[<span data-ttu-id="f21e2-141">Considérations sur la programmation Winsock</span><span class="sxs-lookup"><span data-stu-id="f21e2-141">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 
