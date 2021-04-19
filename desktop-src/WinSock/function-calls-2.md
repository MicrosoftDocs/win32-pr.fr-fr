---
description: De nouvelles fonctions ont été introduites dans l’interface Windows Sockets spécifiquement conçues pour faciliter la programmation de Windows Sockets. L’un des avantages de ces nouvelles fonctions Windows Sockets est la prise en charge intégrée pour IPv6 et IPv4.
ms.assetid: 83262f2b-a335-4bbd-b2e3-6c7744b3ee50
title: Appels de fonction pour les applications Winsock IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a56fe5087e17a9a4eb1337ac803b8500b1fe9c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513407"
---
# <a name="function-calls-for-ipv6-winsock-applications"></a><span data-ttu-id="2a218-104">Appels de fonction pour les applications Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="2a218-104">Function Calls for IPv6 Winsock Applications</span></span>

<span data-ttu-id="2a218-105">De nouvelles fonctions ont été introduites dans l’interface Windows Sockets spécifiquement conçues pour faciliter la programmation de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="2a218-105">New functions have been introduced to the Windows Sockets interface specifically designed to make Windows Sockets programming easier.</span></span> <span data-ttu-id="2a218-106">L’un des avantages de ces nouvelles fonctions Windows Sockets est la prise en charge intégrée pour IPv6 et IPv4.</span><span class="sxs-lookup"><span data-stu-id="2a218-106">One of the benefits of these new Windows Sockets functions is integrated support for both IPv6 and IPv4.</span></span>

<span data-ttu-id="2a218-107">Ces nouvelles fonctions de Windows Sockets sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2a218-107">These new Windows Sockets functions include the following:</span></span>

-   [<span data-ttu-id="2a218-108">**WSAConnectByName**</span><span class="sxs-lookup"><span data-stu-id="2a218-108">**WSAConnectByName**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)
-   [<span data-ttu-id="2a218-109">**WSAConnectByList**</span><span class="sxs-lookup"><span data-stu-id="2a218-109">**WSAConnectByList**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)
-   <span data-ttu-id="2a218-110">famille de fonctions de [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) (**getaddrinfo**, [**API getaddrinfoex**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa), [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow), [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo), [**FreeAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex), [**FreeAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow)et [**SetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa))</span><span class="sxs-lookup"><span data-stu-id="2a218-110">[**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) family of functions (**getaddrinfo**, [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa), [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow), [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo), [**FreeAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex), [**FreeAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow), and [**SetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa))</span></span>
-   <span data-ttu-id="2a218-111">famille de fonctions [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) (**GetNameInfo** et [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow))</span><span class="sxs-lookup"><span data-stu-id="2a218-111">[**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) family of functions (**getnameinfo** and [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow))</span></span>

<span data-ttu-id="2a218-112">En outre, de nouvelles fonctions d’assistance IP avec prise en charge de IPv6 et IPv4 ont été ajoutées pour simplifier la programmation Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="2a218-112">In addition, new IP Helper functions with support for both IPv6 and IPv4 have been added to simplify Windows Sockets programming.</span></span> <span data-ttu-id="2a218-113">Ces nouvelles fonctions d’assistance IP sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2a218-113">These new IP Helper functions include the following:</span></span>

-   [<span data-ttu-id="2a218-114">**GetAdaptersAddresses**</span><span class="sxs-lookup"><span data-stu-id="2a218-114">**GetAdaptersAddresses**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

<span data-ttu-id="2a218-115">Lors de l’ajout de la prise en charge IPv6 à une application, les instructions suivantes doivent être utilisées :</span><span class="sxs-lookup"><span data-stu-id="2a218-115">When adding IPv6 support to an application the following guidelines should be used:</span></span>

-   <span data-ttu-id="2a218-116">Utilisez [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) pour établir une connexion à un point de terminaison en fonction d’un nom d’hôte et d’un port.</span><span class="sxs-lookup"><span data-stu-id="2a218-116">Use [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) to establish a connection to an endpoint given a host name and port.</span></span> <span data-ttu-id="2a218-117">La fonction **WSAConnectByName** est disponible sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2a218-117">The **WSAConnectByName** function is available on Windows Vista and later.</span></span>
-   <span data-ttu-id="2a218-118">Utilisez [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) pour établir une connexion à un à partir d’une collection de points de terminaison possibles représentés par un ensemble d’adresses de destination (noms d’hôte et ports).</span><span class="sxs-lookup"><span data-stu-id="2a218-118">Use [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) to establish a connection to one out of a collection of possible endpoints represented by a set of destination addresses (host names and ports).</span></span> <span data-ttu-id="2a218-119">La fonction **WSAConnectByList** est disponible sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2a218-119">The **WSAConnectByList** function is available on Windows Vista and later.</span></span>
-   <span data-ttu-id="2a218-120">Remplacez les appels de fonction [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) par des appels à l’une des nouvelles fonctions de Windows Sockets [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .</span><span class="sxs-lookup"><span data-stu-id="2a218-120">Replace [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function calls with calls to one of the new [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) Windows Sockets functions.</span></span> <span data-ttu-id="2a218-121">La fonction **getaddrinfo** avec prise en charge du protocole IPv6 est disponible sur Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2a218-121">The **getaddrinfo** function with support for the IPv6 protocol is available on Windows XP and later.</span></span> <span data-ttu-id="2a218-122">Le protocole IPv6 est également pris en charge sur Windows 2000 quand la version préliminaire de la technologie IPv6 pour Windows 2000 est installée.</span><span class="sxs-lookup"><span data-stu-id="2a218-122">The IPv6 protocol is also supported on Windows 2000 when the IPv6 Technology Preview for Windows 2000 is installed.</span></span>
-   <span data-ttu-id="2a218-123">Remplacez les appels de fonction [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) par des appels à l’une des nouvelles fonctions Windows Sockets [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="2a218-123">Replace [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) function calls with calls to one of the new [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) Windows Sockets functions.</span></span> <span data-ttu-id="2a218-124">La fonction **GetNameInfo** avec prise en charge du protocole IPv6 est disponible sur Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2a218-124">The **getnameinfo** function with support for the IPv6 protocol is available on Windows XP and later.</span></span> <span data-ttu-id="2a218-125">Le protocole IPv6 est également pris en charge sur Windows 2000 quand la version préliminaire de la technologie IPv6 pour Windows 2000 est installée.</span><span class="sxs-lookup"><span data-stu-id="2a218-125">The IPv6 protocol is also supported on Windows 2000 when the IPv6 Technology Preview for Windows 2000 is installed.</span></span>

## <a name="wsaconnectbyname"></a><span data-ttu-id="2a218-126">WSAConnectByName</span><span class="sxs-lookup"><span data-stu-id="2a218-126">WSAConnectByName</span></span>

<span data-ttu-id="2a218-127">La fonction [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) simplifie la connexion à un point de terminaison à l’aide d’un socket basé sur un flux, étant donné le nom d’hôte ou l’adresse IP de la destination (IPv4 ou IPv6).</span><span class="sxs-lookup"><span data-stu-id="2a218-127">The [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function simplifies connecting to an endpoint using a stream-based socket given the destination's hostname or IP address (IPv4 or IPv6).</span></span> <span data-ttu-id="2a218-128">Cette fonction réduit le code source nécessaire à la création d’une application IP qui est indépendante de la version du protocole IP utilisé.</span><span class="sxs-lookup"><span data-stu-id="2a218-128">This function reduces the source code required to create an IP application that is agnostic to the version of the IP protocol used.</span></span> <span data-ttu-id="2a218-129">**WSAConnectByName** remplace les étapes suivantes dans une application TCP standard par un appel de fonction unique :</span><span class="sxs-lookup"><span data-stu-id="2a218-129">**WSAConnectByName** replaces the following steps in a typical TCP application to a single function call:</span></span>

-   <span data-ttu-id="2a218-130">Résolution d’un nom d’hôte en un ensemble d’adresses IP.</span><span class="sxs-lookup"><span data-stu-id="2a218-130">Resolve a hostname to a set of IP addresses.</span></span>
-   <span data-ttu-id="2a218-131">Pour chaque adresse IP :</span><span class="sxs-lookup"><span data-stu-id="2a218-131">For each IP address:</span></span>
    -   <span data-ttu-id="2a218-132">Créez un socket de la famille d’adresses appropriée.</span><span class="sxs-lookup"><span data-stu-id="2a218-132">Create a socket of the appropriate address family.</span></span>
    -   <span data-ttu-id="2a218-133">Tente de se connecter à l’adresse IP distante.</span><span class="sxs-lookup"><span data-stu-id="2a218-133">Attempts to connect to the remote IP address.</span></span> <span data-ttu-id="2a218-134">Si la connexion a réussi, elle retourne la valeur ; dans le cas contraire, l’adresse IP distante suivante pour l’hôte est tentée.</span><span class="sxs-lookup"><span data-stu-id="2a218-134">If the connection was successful, it returns; otherwise the next remote IP address for the host is tried.</span></span>

<span data-ttu-id="2a218-135">La fonction [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) va au-delà de la résolution du nom et de la tentative de connexion.</span><span class="sxs-lookup"><span data-stu-id="2a218-135">The [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function goes beyond just resolving the name and then attempting to connect.</span></span> <span data-ttu-id="2a218-136">La fonction utilise toutes les adresses distantes retournées par la résolution de noms et toutes les adresses IP sources de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="2a218-136">The function uses all of the remote addresses returned by name resolution and all of the local machine's source IP addresses.</span></span> <span data-ttu-id="2a218-137">Il tente d’abord de se connecter en utilisant des paires d’adresses avec les chances de réussite les plus élevées.</span><span class="sxs-lookup"><span data-stu-id="2a218-137">It first attempts to connect using address pairs with the highest chance of success.</span></span> <span data-ttu-id="2a218-138">Par conséquent, **WSAConnectByName** garantit non seulement qu’une connexion sera établie si possible, mais elle réduit également le temps nécessaire à l’établissement de la connexion.</span><span class="sxs-lookup"><span data-stu-id="2a218-138">Therefore, **WSAConnectByName** not only ensures that a connection will be established if possible, but it also minimizes the time to establish the connection.</span></span>

<span data-ttu-id="2a218-139">Pour activer les communications IPv6 et IPv4, utilisez la méthode suivante :</span><span class="sxs-lookup"><span data-stu-id="2a218-139">To enable both IPv6 and IPv4 communications, use the following method:</span></span>

-   <span data-ttu-id="2a218-140">La fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) doit être appelée sur un socket créé pour la \_ famille d’adresses d’adresses inet6 AF pour désactiver l’option de socket **IPv6 \_ V6ONLY** avant d’appeler [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea).</span><span class="sxs-lookup"><span data-stu-id="2a218-140">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function must be called on a socket created for the AF\_INET6 address family to disable the **IPV6\_V6ONLY** socket option before calling [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea).</span></span> <span data-ttu-id="2a218-141">Pour ce faire, vous devez appeler la fonction **setsockopt** sur le socket avec le paramètre *Level* défini sur **IPPROTO \_ IPv6** (voir [options de \_ Socket IPPROTO IPv6](ipproto-ipv6-socket-options.md)), le paramètre *nom_option* défini sur **IPv6 \_ V6ONLY** et la valeur de paramètre *optvalue* définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="2a218-141">This is accomplished by calling the **setsockopt** function on the socket with the *level* parameter set to **IPPROTO\_IPV6** (see [IPPROTO\_IPV6 Socket Options](ipproto-ipv6-socket-options.md)), the *optname* parameter set to **IPV6\_V6ONLY**, and the *optvalue* parameter value set to zero.</span></span>

<span data-ttu-id="2a218-142">Si une application doit établir une liaison à une adresse ou à un port local spécifique, [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) ne peut pas être utilisé, car le paramètre socket de **WSAConnectByName** doit être un socket indépendant.</span><span class="sxs-lookup"><span data-stu-id="2a218-142">If an application needs to bind to a specific local address or port, then [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) cannot be used since the socket parameter to **WSAConnectByName** must be an unbound socket.</span></span>

<span data-ttu-id="2a218-143">L’exemple de code ci-dessous montre que quelques lignes de code sont nécessaires pour utiliser cette fonction pour implémenter une application qui est indépendante de la version IP.</span><span class="sxs-lookup"><span data-stu-id="2a218-143">The code example below shows only a few lines of code are needed to use this function to implement an application that is agnostic to the IP version.</span></span>

<span data-ttu-id="2a218-144">Établir une connexion à l’aide de [ **WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)</span><span class="sxs-lookup"><span data-stu-id="2a218-144">Establish a connection using [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(LPWSTR NodeName, LPWSTR PortName) 
{
    SOCKET ConnSocket;
    DWORD ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);
  
    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    bSuccess = WSAConnectByName(ConnSocket, NodeName, 
            PortName, &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}
```



## <a name="wsaconnectbylist"></a><span data-ttu-id="2a218-145">WSAConnectByList</span><span class="sxs-lookup"><span data-stu-id="2a218-145">WSAConnectByList</span></span>

<span data-ttu-id="2a218-146">La fonction [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) établit une connexion à un hôte en fonction d’un ensemble d’hôtes possibles (représentés par un ensemble d’adresses IP et de ports de destination).</span><span class="sxs-lookup"><span data-stu-id="2a218-146">The [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) function establishes a connection to a host given a set of possible hosts (represented by a set of destination IP addresses and ports).</span></span> <span data-ttu-id="2a218-147">La fonction prend toutes les adresses IP et tous les ports pour le point de terminaison et toutes les adresses IP de l’ordinateur local et tente une connexion à l’aide de toutes les combinaisons d’adresses possibles.</span><span class="sxs-lookup"><span data-stu-id="2a218-147">The function takes all IP addresses and ports for the endpoint and all of the local machine's IP addresses, and attempts a connection using all possible address combinations.</span></span>

<span data-ttu-id="2a218-148">[**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) est lié à la fonction [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) .</span><span class="sxs-lookup"><span data-stu-id="2a218-148">[**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) is related to the [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function.</span></span> <span data-ttu-id="2a218-149">Au lieu d’accepter un seul nom d’hôte, **WSAConnectByList** accepte une liste d’hôtes (adresses de destination et paires de ports) et se connecte à l’une des adresses et des ports de la liste fournie.</span><span class="sxs-lookup"><span data-stu-id="2a218-149">Instead of taking a single hostname, **WSAConnectByList** accepts a list of hosts (destination addresses and port pairs) and connects to one of the addresses and ports in the provided list.</span></span> <span data-ttu-id="2a218-150">Cette fonction est conçue pour prendre en charge les scénarios dans lesquels une application doit se connecter à n’importe quel hôte disponible en dehors d’une liste d’hôtes potentiels.</span><span class="sxs-lookup"><span data-stu-id="2a218-150">This function is designed to support scenarios in which an application needs to connect to any available host out of a list of potential hosts.</span></span>

<span data-ttu-id="2a218-151">Comme pour [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea), la fonction [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) réduit considérablement le code source nécessaire à la création, à la liaison et à la connexion d’un Socket.</span><span class="sxs-lookup"><span data-stu-id="2a218-151">Similar to [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea), the [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) function significantly reduces the source code required to create, bind and connect a socket.</span></span> <span data-ttu-id="2a218-152">Grâce à cette fonction, il est beaucoup plus facile d’implémenter une application qui est indépendante de la version IP.</span><span class="sxs-lookup"><span data-stu-id="2a218-152">This function makes it much easier to implement an application that is agnostic to the IP version.</span></span> <span data-ttu-id="2a218-153">La liste des adresses d’un hôte accepté par cette fonction peut être des adresses IPv6 ou IPv4.</span><span class="sxs-lookup"><span data-stu-id="2a218-153">The list of addresses for a host accepted by this function may be IPv6 or IPv4 addresses.</span></span>

<span data-ttu-id="2a218-154">Pour permettre aux adresses IPv6 et IPv4 d’être transmises dans la liste d’adresses unique acceptée par la fonction, les étapes suivantes doivent être effectuées avant d’appeler la fonction :</span><span class="sxs-lookup"><span data-stu-id="2a218-154">To enable both IPv6 and IPv4 addresses to be passed in the single address list accepted by the function, the following steps must be performed prior to calling the function:</span></span>

-   <span data-ttu-id="2a218-155">La fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) doit être appelée sur un socket créé pour la \_ famille d’adresses d’adresses inet6 AF pour désactiver l’option de socket **IPv6 \_ V6ONLY** avant d’appeler [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist).</span><span class="sxs-lookup"><span data-stu-id="2a218-155">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function must be called on a socket created for the AF\_INET6 address family to disable the **IPV6\_V6ONLY** socket option before calling [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist).</span></span> <span data-ttu-id="2a218-156">Pour ce faire, vous devez appeler la fonction **setsockopt** sur le socket avec le paramètre *Level* défini sur **IPPROTO \_ IPv6** (voir [options de \_ Socket IPPROTO IPv6](ipproto-ipv6-socket-options.md)), le paramètre *nom_option* défini sur **IPv6 \_ V6ONLY** et la valeur de paramètre *optvalue* définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="2a218-156">This is accomplished by calling the **setsockopt** function on the socket with the *level* parameter set to **IPPROTO\_IPV6** (see [IPPROTO\_IPV6 Socket Options](ipproto-ipv6-socket-options.md)), the *optname* parameter set to **IPV6\_V6ONLY**, and the *optvalue* parameter value set to zero.</span></span>
-   <span data-ttu-id="2a218-157">Toutes les adresses IPv4 doivent être représentées dans le format d’adresse IPv6 mappée IPv4, ce qui permet à une application IPv6 uniquement de communiquer avec un nœud IPv4.</span><span class="sxs-lookup"><span data-stu-id="2a218-157">Any IPv4 addresses must be represented in the IPv4-mapped IPv6 address format which enables an IPv6 only application to communicate with an IPv4 node.</span></span> <span data-ttu-id="2a218-158">Le format d’adresse IPv6 mappée IPv4 permet à l’adresse IPv4 d’un nœud IPv4 d’être représentée comme une adresse IPv6.</span><span class="sxs-lookup"><span data-stu-id="2a218-158">The IPv4-mapped IPv6 address format allows the IPv4 address of an IPv4 node to be represented as an IPv6 address.</span></span> <span data-ttu-id="2a218-159">L’adresse IPv4 est encodée dans les bits de poids faible 32 de l’adresse IPv6, et les bits de poids fort 96 contiennent le préfixe fixe 0:0 : 0:0 : 0 : FFFF.</span><span class="sxs-lookup"><span data-stu-id="2a218-159">The IPv4 address is encoded into the low-order 32 bits of the IPv6 address, and the high-order 96 bits hold the fixed prefix 0:0:0:0:0:FFFF.</span></span> <span data-ttu-id="2a218-160">Le format d’adresse IPv6 mappée IPv4 est spécifié dans le document RFC 4291.</span><span class="sxs-lookup"><span data-stu-id="2a218-160">The IPv4-mapped IPv6 address format is specified in RFC 4291.</span></span> <span data-ttu-id="2a218-161">Pour plus d’informations, consultez [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291).</span><span class="sxs-lookup"><span data-stu-id="2a218-161">For more information, see [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291).</span></span> <span data-ttu-id="2a218-162">La \_ macro IN6ADDR SETV4MAPPED dans *Mstcpip. h* peut être utilisée pour convertir une adresse IPv4 au format d’adresse IPv6 mappé IPv4 requis.</span><span class="sxs-lookup"><span data-stu-id="2a218-162">The IN6ADDR\_SETV4MAPPED macro in *Mstcpip.h* can be used to convert an IPv4 address to the required IPv4-mapped IPv6 address format.</span></span>

<span data-ttu-id="2a218-163">Établir une connexion à l’aide de [ **WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)</span><span class="sxs-lookup"><span data-stu-id="2a218-163">Establish a Connection Using [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(SOCKET_ADDRESS_LIST *AddressList) 
{
    SOCKET ConnSocket;
    DWORD ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);

    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    // AddressList may contain IPv6 and/or IPv4Mapped addresses
    bSuccess = WSAConnectByList(ConnSocket,
            AddressList,
            &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}
```



## <a name="getaddrinfo"></a><span data-ttu-id="2a218-164">getaddrinfo</span><span class="sxs-lookup"><span data-stu-id="2a218-164">getaddrinfo</span></span>

<span data-ttu-id="2a218-165">La fonction **getaddrinfo** effectue également le travail de traitement de nombreuses fonctions.</span><span class="sxs-lookup"><span data-stu-id="2a218-165">The **getaddrinfo** function also performs the processing work of many functions.</span></span> <span data-ttu-id="2a218-166">Auparavant, les appels à plusieurs fonctions Windows Sockets devaient créer, ouvrir, puis lier une adresse à un Socket.</span><span class="sxs-lookup"><span data-stu-id="2a218-166">Previously, calls to a number of Windows Sockets functions were required to create, open, and then bind an address to a socket.</span></span> <span data-ttu-id="2a218-167">Avec la fonction **getaddrinfo** , les lignes de code source nécessaires pour effectuer ce travail peuvent être réduites de manière significative.</span><span class="sxs-lookup"><span data-stu-id="2a218-167">With the **getaddrinfo** function, the lines of source code necessary to perform such work can be significantly reduced.</span></span> <span data-ttu-id="2a218-168">Les deux exemples suivants illustrent le code source nécessaire à l’exécution de ces tâches avec et sans la fonction **getaddrinfo** .</span><span class="sxs-lookup"><span data-stu-id="2a218-168">The following two examples illustrate the source code necessary to perform these tasks with and without the **getaddrinfo** function.</span></span>

<span data-ttu-id="2a218-169">Effectuer une ouverture, une connexion et une liaison à l’aide de **getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="2a218-169">Perform an Open, Connect, and Bind Using **getaddrinfo**</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *ServerName, char *PortName, int SocketType)
{
    SOCKET ConnSocket;
    ADDRINFO *AI;

    if (getaddrinfo(ServerName, PortName, NULL, &AI) != 0) {
        return INVALID_SOCKET;
    }

    ConnSocket = socket(AI->ai_family, SocketType, 0);
    if (ConnSocket == INVALID_SOCKET) {
        freeaddrinfo(AI);
        return INVALID_SOCKET;
    }

    if (connect(ConnSocket, AI->ai_addr, (int) AI->ai_addrlen) == SOCKET_ERROR) {
        closesocket(ConnSocket);
        freeaddrinfo(AI);
        return INVALID_SOCKET;
    }

    return ConnSocket;
}
```



<span data-ttu-id="2a218-170">Effectuer une ouverture, une connexion et une liaison sans utiliser **getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="2a218-170">Perform an Open, Connect, and Bind Without Using **getaddrinfo**</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *ServerName, unsigned short Port, int SocketType) 
{
    SOCKET ConnSocket;
    LPHOSTENT hp;
    SOCKADDR_IN ServerAddr;
    
    ConnSocket = socket(AF_INET, SocketType, 0); /* Open a socket */
    if (ConnSocket < 0 ) {
        return INVALID_SOCKET;
    }

    memset(&ServerAddr, 0, sizeof(ServerAddr));
    ServerAddr.sin_family = AF_INET;
    ServerAddr.sin_port = htons(Port);

    if (isalpha(ServerName[0])) {   /* server address is a name */
        hp = gethostbyname(ServerName);
        if (hp == NULL) {
            return INVALID_SOCKET;
        }
        ServerAddr.sin_addr.s_addr = (ULONG) hp->h_addr;
    } else { /* Convert nnn.nnn address to a usable one */
        ServerAddr.sin_addr.s_addr = inet_addr(ServerName);
    } 

    if (connect(ConnSocket, (LPSOCKADDR)&ServerAddr, 
        sizeof(ServerAddr)) == SOCKET_ERROR)
    {
        closesocket(ConnSocket);
        return INVALID_SOCKET;
    }

    return ConnSocket;
}
```



<span data-ttu-id="2a218-171">Notez que ces deux exemples de code source effectuent les mêmes tâches, mais le premier exemple, à l’aide de la fonction **getaddrinfo** , requiert moins de lignes de code source et peut gérer des adresses IPv6 ou IPv4.</span><span class="sxs-lookup"><span data-stu-id="2a218-171">Notice that both of these source code examples perform the same tasks, but the first example, using the **getaddrinfo** function, requires fewer lines of source code, and can handle either IPv6 or IPv4 addresses.</span></span> <span data-ttu-id="2a218-172">Le nombre de lignes de code source supprimées à l’aide de la fonction **getaddrinfo** varie.</span><span class="sxs-lookup"><span data-stu-id="2a218-172">The number of lines of source code eliminated by using the **getaddrinfo** function varies.</span></span>

> [!Note]  
> <span data-ttu-id="2a218-173">Dans le code source de production, votre application itère au sein de l’ensemble d’adresses renvoyé par la fonction [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) ou [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .</span><span class="sxs-lookup"><span data-stu-id="2a218-173">In production source code, your application would iterate through the set of addresses returned by the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) or [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function.</span></span> <span data-ttu-id="2a218-174">Ces exemples omettent cette étape en faveur de la simplicité.</span><span class="sxs-lookup"><span data-stu-id="2a218-174">These examples omit that step in favor of simplicity.</span></span>

 

<span data-ttu-id="2a218-175">Un autre problème que vous devez résoudre lorsque vous modifiez une application IPv4 existante pour prendre en charge IPv6 est associé à l’ordre dans lequel les fonctions sont appelées.</span><span class="sxs-lookup"><span data-stu-id="2a218-175">Another issue you must address when modifying an existing IPv4 application to support IPv6 is associated with the order in which functions are called.</span></span> <span data-ttu-id="2a218-176">Les options [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) et [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) requièrent qu’une séquence d’appels de fonction soit effectuée dans un ordre spécifique.</span><span class="sxs-lookup"><span data-stu-id="2a218-176">Both [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) require that a sequence of function calls are made in a specific order.</span></span>

<span data-ttu-id="2a218-177">Sur les plateformes où IPv4 et IPv6 sont tous deux utilisés, la famille d’adresses du nom d’hôte distant n’est pas connue à l’avance.</span><span class="sxs-lookup"><span data-stu-id="2a218-177">On platforms where both IPv4 and IPv6 are used, the address family of the remote host name is not known ahead of time.</span></span> <span data-ttu-id="2a218-178">Par conséquent, la résolution d’adresses à l’aide de la fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) doit être exécutée en premier pour déterminer l’adresse IP et la famille d’adresses de l’hôte distant.</span><span class="sxs-lookup"><span data-stu-id="2a218-178">So address resolution using the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function must be executed first to determine the IP address and address family of the remote host.</span></span> <span data-ttu-id="2a218-179">La fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) peut ensuite être appelée pour ouvrir un socket de la famille d’adresses retournée par [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo).</span><span class="sxs-lookup"><span data-stu-id="2a218-179">Then the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function can be called to open a socket of the address family returned by [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo).</span></span> <span data-ttu-id="2a218-180">Il s’agit d’un changement important dans la façon dont les applications Windows Sockets sont écrites, car de nombreuses applications IPv4 ont tendance à utiliser un ordre différent d’appels de fonction.</span><span class="sxs-lookup"><span data-stu-id="2a218-180">This is an important change in how Windows Sockets applications are written, since many IPv4 applications tend to use a different order of function calls.</span></span>

<span data-ttu-id="2a218-181">La plupart des applications IPv4 créent d’abord un socket pour la \_ famille d’adresses d’inet AF, puis effectuent la résolution de noms, puis utilisent le socket pour se connecter à l’adresse IP résolue.</span><span class="sxs-lookup"><span data-stu-id="2a218-181">Most IPv4 applications first create a socket for the AF\_INET address family, then do name resolution, and then use the socket to connect to the resolved IP address.</span></span> <span data-ttu-id="2a218-182">Lorsque vous rendez ces applications compatibles IPv6, l’appel de fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) doit être retardé jusqu’à la résolution de noms lorsque la famille d’adresses a été deteremined.</span><span class="sxs-lookup"><span data-stu-id="2a218-182">When making such applications IPv6-capable, the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function call must be delayed until after name resolution when the address family has been deteremined.</span></span> <span data-ttu-id="2a218-183">Notez que si la résolution de noms retourne des adresses IPv4 et IPv6, des sockets IPv4 et IPv6 distincts doivent être utilisés pour se connecter à ces adresses de destination.</span><span class="sxs-lookup"><span data-stu-id="2a218-183">Note that if name resolution returns both IPv4 and IPv6 addresses, then separate IPv4 and IPv6 sockets must be used to connect to these destination addresses.</span></span> <span data-ttu-id="2a218-184">Toutes ces complexités peuvent être évitées à l’aide de la fonction [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) sur Windows Vista et versions ultérieures, afin que les développeurs d’applications soient encouragés à utiliser cette nouvelle fonction.</span><span class="sxs-lookup"><span data-stu-id="2a218-184">All of these complexities can be avoided by using the [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function on Windows Vista and later, so application developers are encouraged to use this new function.</span></span>

<span data-ttu-id="2a218-185">L’exemple de code suivant montre la séquence appropriée pour effectuer d’abord la résolution de noms (effectuée à la quatrième ligne de l’exemple de code source suivant), puis ouvrir un socket (effectué dans la<sup>troisième ligne de</sup> l’exemple de code suivant).</span><span class="sxs-lookup"><span data-stu-id="2a218-185">The following code example shows the proper sequence for performing name resolution first (performed in the fourth line in the following source code example), then opening a socket (performed in the 19<sup>th</sup> line in the following code example).</span></span> <span data-ttu-id="2a218-186">Cet exemple est un extrait du fichier client. c figurant dans le [code client compatible IPv6](ipv6-enabled-client-code-2.md) de l’annexe B. La fonction PrintError appelée dans l’exemple de code suivant est indiquée dans l’exemple client. c.</span><span class="sxs-lookup"><span data-stu-id="2a218-186">This example is an excerpt from the Client.c file found in the [IPv6-Enabled Client Code](ipv6-enabled-client-code-2.md) in Appendix B. The PrintError function called in the following code example is listed in the Client.c sample.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *Server, char *PortName, int Family, int SocketType)
{

    int iResult = 0;
    SOCKET ConnSocket = INVALID_SOCKET;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;
    ADDRINFO Hints;

    char *AddrName = NULL;

    memset(&Hints, 0, sizeof (Hints));
    Hints.ai_family = Family;
    Hints.ai_socktype = SocketType;

    iResult = getaddrinfo(Server, PortName, &Hints, &AddrInfo);
    if (iResult != 0) {
        printf("Cannot resolve address [%s] and port [%s], error %d: %s\n",
               Server, PortName, WSAGetLastError(), gai_strerror(iResult));
        return INVALID_SOCKET;
    }
    //
    // Try each address getaddrinfo returned, until we find one to which
    // we can successfully connect.
    //
    for (AI = AddrInfo; AI != NULL; AI = AI->ai_next) {

        // Open a socket with the correct address family for this address.
        ConnSocket = socket(AI->ai_family, AI->ai_socktype, AI->ai_protocol);
        if (ConnSocket == INVALID_SOCKET) {
            printf("Error Opening socket, error %d\n", WSAGetLastError());
            continue;
        }
        //
        // Notice that nothing in this code is specific to whether we 
        // are using UDP or TCP.
        //
        // When connect() is called on a datagram socket, it does not 
        // actually establish the connection as a stream (TCP) socket
        // would. Instead, TCP/IP establishes the remote half of the
        // (LocalIPAddress, LocalPort, RemoteIP, RemotePort) mapping.
        // This enables us to use send() and recv() on datagram sockets,
        // instead of recvfrom() and sendto().
        //

        printf("Attempting to connect to: %s\n", Server ? Server : "localhost");
        if (connect(ConnSocket, AI->ai_addr, (int) AI->ai_addrlen) != SOCKET_ERROR)
            break;

        if (getnameinfo(AI->ai_addr, (socklen_t) AI->ai_addrlen, AddrName,
                        sizeof (AddrName), NULL, 0, NI_NUMERICHOST) != 0) {
            strcpy_s(AddrName, sizeof (AddrName), "<unknown>");
            printf("connect() to %s failed with error %d\n", AddrName, WSAGetLastError());
            closesocket(ConnSocket);
            ConnSocket = INVALID_SOCKET;
        }    
    }
    return ConnSocket;
}

```



## <a name="ip-helper-functions"></a><span data-ttu-id="2a218-187">Fonctions de l’assistance IP</span><span class="sxs-lookup"><span data-stu-id="2a218-187">IP Helper Functions</span></span>

<span data-ttu-id="2a218-188">Enfin, les applications qui utilisent la fonction d’assistance IP [**GetAdaptersInfo**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo)et les informations de l' [**\_ adaptateur IP \_**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info)de la structure associée doivent reconnaître que cette fonction et cette structure sont toutes deux limitées aux adresses IPv4.</span><span class="sxs-lookup"><span data-stu-id="2a218-188">Finally, applications making use of the IP Helper function [**GetAdaptersInfo**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo), and its associated structure [**IP\_ADAPTER\_INFO**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info), must recognize that both this function and structure are limited to IPv4 addresses.</span></span> <span data-ttu-id="2a218-189">Les remplacements compatibles IPv6 pour cette fonction et cette structure sont la fonction [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) et la structure d' [**\_ \_ adresses IP**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) de la carte.</span><span class="sxs-lookup"><span data-stu-id="2a218-189">IPv6-enabled replacements for this function and structure are the [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) function and the [**IP\_ADAPTER\_ADDRESSES**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) structure.</span></span> <span data-ttu-id="2a218-190">Les applications compatibles IPv6 utilisant l’API d’assistance IP doivent utiliser la fonction **GetAdaptersAddresses** et la structure d’adresses de l' **\_ adaptateur \_ IP** IPv6 correspondante, toutes deux définies dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2a218-190">IPv6-enabled applications making use of the IP Helper API should use the **GetAdaptersAddresses** function and the corresponding IPv6-enabled **IP\_ADAPTER\_ADDRESSES** structure, both defined in the Microsoft Windows Software Development Kit (SDK).</span></span>

## <a name="recommendations"></a><span data-ttu-id="2a218-191">Recommandations</span><span class="sxs-lookup"><span data-stu-id="2a218-191">Recommendations</span></span>

<span data-ttu-id="2a218-192">La meilleure approche pour s’assurer que votre application utilise des appels de fonction compatibles IPv6 consiste à utiliser la fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) pour obtenir une traduction d’hôte à adresse.</span><span class="sxs-lookup"><span data-stu-id="2a218-192">The best approach to ensure your application is using IPv6-compatible function calls is to use the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function for obtaining host-to-address translation.</span></span> <span data-ttu-id="2a218-193">À partir de Windows XP, la fonction **getaddrinfo** rend la fonction [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) inutile, et votre application doit donc utiliser la fonction **getaddrinfo** à la place pour les futurs projets de programmation.</span><span class="sxs-lookup"><span data-stu-id="2a218-193">Beginning with Windows XP, the **getaddrinfo** function makes the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function unnecessary, and your application should therefore use the **getaddrinfo** function instead for future programming projects.</span></span> <span data-ttu-id="2a218-194">Alors que Microsoft continuera à prendre en charge **gethostbyname**, cette fonction ne sera pas étendue pour prendre en charge IPv6.</span><span class="sxs-lookup"><span data-stu-id="2a218-194">While Microsoft will continue to support **gethostbyname**, this function will not be extended to support IPv6.</span></span> <span data-ttu-id="2a218-195">Pour une prise en charge transparente de l’obtention des informations sur l’hôte IPv6 et IPv4, vous devez utiliser **getaddrinfo**.</span><span class="sxs-lookup"><span data-stu-id="2a218-195">For transparent support for obtaining IPv6 and IPv4 host information, you must use **getaddrinfo**.</span></span>

<span data-ttu-id="2a218-196">L’exemple suivant montre comment utiliser au mieux la fonction **getaddrinfo** .</span><span class="sxs-lookup"><span data-stu-id="2a218-196">The following example shows how to best use the **getaddrinfo** function.</span></span> <span data-ttu-id="2a218-197">Notez que la fonction, quand elle est utilisée correctement comme illustré dans cet exemple, gère correctement la conversion d’hôte à adresse IPv6 et IPv4, mais elle obtient également d’autres informations utiles sur l’hôte, telles que le type de sockets pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2a218-197">Notice that the function, when used properly as this example demonstrates, handles both IPv6 and IPv4 host-to-address translation properly, but it also obtains other useful information about the host, such as the type of sockets supported.</span></span> <span data-ttu-id="2a218-198">Cet exemple est un extrait de l’exemple client. c figurant dans l’annexe B.</span><span class="sxs-lookup"><span data-stu-id="2a218-198">This sample is an excerpt from the Client.c sample found in Appendix B.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

int ResolveName(char *Server, char *PortName, int Family, int SocketType)
{

    int iResult = 0;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;
    ADDRINFO Hints;

   //
    // By not setting the AI_PASSIVE flag in the hints to getaddrinfo, we're
    // indicating that we intend to use the resulting address(es) to connect
    // to a service.  This means that when the Server parameter is NULL,
    // getaddrinfo will return one entry per allowed protocol family
    // containing the loopback address for that family.
    //
    
    memset(&Hints, 0, sizeof(Hints));
    Hints.ai_family = Family;
    Hints.ai_socktype = SocketType;
    iResult = getaddrinfo(Server, PortName, &Hints, &AddrInfo);
    if (iResult != 0) {
        printf("Cannot resolve address [%s] and port [%s], error %d: %s\n",
               Server, PortName, WSAGetLastError(), gai_strerror(iResult));
        return SOCKET_ERROR;
    }
     return 0;
}
```



> [!Note]  
> <span data-ttu-id="2a218-199">La version de la fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) qui prend en charge IPv6 est une nouveauté pour la version Windows XP de Windows.</span><span class="sxs-lookup"><span data-stu-id="2a218-199">The version of the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function that supports IPv6 is new for the Windows XP release of Windows.</span></span>

 

<span data-ttu-id="2a218-200">Code pour éviter</span><span class="sxs-lookup"><span data-stu-id="2a218-200">Code to Avoid</span></span>

<span data-ttu-id="2a218-201">La traduction d’adresses d’hôte a traditionnellement été obtenue à l’aide de la fonction [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) .</span><span class="sxs-lookup"><span data-stu-id="2a218-201">Host address translation has traditionally been achieved using the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function.</span></span> <span data-ttu-id="2a218-202">À partir de Windows XP :</span><span class="sxs-lookup"><span data-stu-id="2a218-202">Beginning with Windows XP:</span></span>

-   <span data-ttu-id="2a218-203">La fonction **getaddrinfo** rend la fonction **gethostbyname** obsolète.</span><span class="sxs-lookup"><span data-stu-id="2a218-203">The **getaddrinfo** function makes the **gethostbyname** function obsolete.</span></span>
-   <span data-ttu-id="2a218-204">Vos applications doivent utiliser la fonction **getaddrinfo** au lieu de la fonction **gethostbyname** .</span><span class="sxs-lookup"><span data-stu-id="2a218-204">Your applications should use the **getaddrinfo** function instead of the **gethostbyname** function.</span></span>

<span data-ttu-id="2a218-205">Tâches de codage</span><span class="sxs-lookup"><span data-stu-id="2a218-205">Coding Tasks</span></span>

<span data-ttu-id="2a218-206">**Pour modifier une application IPv4 existante afin d’ajouter la prise en charge d’IPv6**</span><span class="sxs-lookup"><span data-stu-id="2a218-206">**To modify an existing IPv4 application to add support for IPv6**</span></span>

1.  <span data-ttu-id="2a218-207">Acquérir l’utilitaire Checkv4.exe.</span><span class="sxs-lookup"><span data-stu-id="2a218-207">Acquire the Checkv4.exe utility.</span></span> <span data-ttu-id="2a218-208">Cet utilitaire est installé dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="2a218-208">This utility is installed as part of the Windows SDK.</span></span> <span data-ttu-id="2a218-209">Le SDK Windows est disponible via un abonnement MSDN et peut également être téléchargé à partir du site Web de Microsoft ( https://msdn.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="2a218-209">The Windows SDK is available through an MSDN subscription and can also be downloaded from the Microsoft website (https://msdn.microsoft.com).</span></span> <span data-ttu-id="2a218-210">Une version antérieure de l’outil *Checkv4.exe* était également incluse dans le cadre de la version préliminaire de la technologie Microsoft IPv6 pour Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2a218-210">An older version of the *Checkv4.exe* tool was also as included as part of the Microsoft IPv6 Technology Preview for Windows 2000.</span></span>
2.  <span data-ttu-id="2a218-211">Exécutez l’utilitaire *Checkv4.exe* sur votre code.</span><span class="sxs-lookup"><span data-stu-id="2a218-211">Run the *Checkv4.exe* utility against your code.</span></span> <span data-ttu-id="2a218-212">Consultez [utilisation de l’utilitaire de Checkv4.exe](using-the-checkv4-exe-utility-2.md) pour en savoir plus sur l’exécution de l’utilitaire de version sur vos fichiers.</span><span class="sxs-lookup"><span data-stu-id="2a218-212">See [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md) to learn about running the version utility against your files.</span></span>
3.  <span data-ttu-id="2a218-213">L’utilitaire vous avertit de l’utilisation des fonctions [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)et d’autres fonctions IPv4 uniquement, et fournit des recommandations sur la façon de les remplacer par la fonction compatible IPv6, par exemple [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) et [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo).</span><span class="sxs-lookup"><span data-stu-id="2a218-213">The utility alerts you to usage of the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr), and other IPv4-only functions, and provides recommendations on how to replace them with the IPv6-compatible function such as [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo).</span></span>
4.  <span data-ttu-id="2a218-214">Remplacez toutes les instances de la fonction **gethostbyname** et le code associé, le cas échéant, par la fonction **getaddrinfo** .</span><span class="sxs-lookup"><span data-stu-id="2a218-214">Replace any instances of the **gethostbyname** function, and associated code as appropriate, with the **getaddrinfo** function.</span></span> <span data-ttu-id="2a218-215">Sur Windows Vista, utilisez la fonction [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) ou [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="2a218-215">On Windows Vista, use the [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) or [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) function when appropriate.</span></span>
5.  <span data-ttu-id="2a218-216">Remplacez toutes les instances de la fonction [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) et le code associé, le cas échéant, par la fonction [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="2a218-216">Replace any instances of the [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) function, and associated code as appropriate, with the [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) function.</span></span>

<span data-ttu-id="2a218-217">Vous pouvez également rechercher dans votre base de code les instances des fonctions **gethostbyname** et [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) , puis modifier toute l’utilisation (et tout autre code associé, le cas échéant) vers les fonctions **getaddrinfo** et [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="2a218-217">Alternatively, you can search your code base for instances of the **gethostbyname** and [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) functions, and change all such usage (and other associated code, as appropriate) to the **getaddrinfo** and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a218-218">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2a218-218">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a218-219">Guide IPv6 pour les applications Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="2a218-219">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="2a218-220">Modification des structures de données pour IPv6 Winsock appications</span><span class="sxs-lookup"><span data-stu-id="2a218-220">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="2a218-221">Sockets à double pile pour les applications Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="2a218-221">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="2a218-222">Utilisation d’adresses IPv4 codées en dur</span><span class="sxs-lookup"><span data-stu-id="2a218-222">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="2a218-223">Problèmes d’interface utilisateur pour les applications Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="2a218-223">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> <dt>

[<span data-ttu-id="2a218-224">Protocoles sous-jacents pour les applications Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="2a218-224">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
</dt> </dl>

 

 
