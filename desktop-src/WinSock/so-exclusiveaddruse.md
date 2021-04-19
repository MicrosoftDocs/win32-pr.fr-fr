---
description: L' \_ option de socket so EXCLUSIVEADDRUSE empêche d’autres Sockets d’être liés de force à la même adresse et au même port.
ms.assetid: ce0d8188-54be-46e8-8753-d0680f690b84
title: Option de socket SO_EXCLUSIVEADDRUSE (Winsock2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d4747150f918a7e9c4ce37ec209e7261d1a00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516870"
---
# <a name="so_exclusiveaddruse-socket-option"></a><span data-ttu-id="f7ce8-103">SO \_ EXCLUSIVEADDRUSE option de socket</span><span class="sxs-lookup"><span data-stu-id="f7ce8-103">SO\_EXCLUSIVEADDRUSE socket option</span></span>

<span data-ttu-id="f7ce8-104">L' \_ option de socket so EXCLUSIVEADDRUSE empêche d’autres Sockets d’être liés de force à la même adresse et au même port.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-104">The SO\_EXCLUSIVEADDRUSE socket option prevents other sockets from being forcibly bound to the same address and port.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7ce8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7ce8-105">Syntax</span></span>

<span data-ttu-id="f7ce8-106">L' \_ option so EXCLUSIVEADDRUSE empêche d’autres Sockets d’être liés de force à la même adresse et au même port, une pratique activée par l' \_ option de socket REUSEADDR.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-106">The SO\_EXCLUSIVEADDRUSE option prevents other sockets from being forcibly bound to the same address and port, a practice enabled by the SO\_REUSEADDR socket option.</span></span> <span data-ttu-id="f7ce8-107">Une telle réutilisation peut être exécutée par des applications malveillantes pour interrompre l’application.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-107">Such reuse can be executed by malicious applications to disrupt the application.</span></span> <span data-ttu-id="f7ce8-108">L' \_ option so EXCLUSIVEADDRUSE est très utile pour les services système nécessitant une haute disponibilité.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-108">The SO\_EXCLUSIVEADDRUSE option is very useful to system services requiring high availability.</span></span>

<span data-ttu-id="f7ce8-109">L’exemple de code suivant illustre la définition de cette option.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-109">The following code example illustrates setting this option.</span></span>


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



<span data-ttu-id="f7ce8-110">Pour avoir un effet, l' \_ option so EXCLUSIVADDRUSE doit être définie avant l’appel de la fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) (cela s’applique également à l' \_ option so REUSEADDR).</span><span class="sxs-lookup"><span data-stu-id="f7ce8-110">To have any effect, the SO\_EXCLUSIVADDRUSE option must be set before the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called (this also applies to the SO\_REUSEADDR option).</span></span> <span data-ttu-id="f7ce8-111">Le tableau 1 répertorie les effets de la définition de l' \_ option so EXCLUSIVEADDRUSE.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-111">Table 1 lists the effects of setting the SO\_EXCLUSIVEADDRUSE option.</span></span> <span data-ttu-id="f7ce8-112">Caractère générique indique la liaison à l’adresse générique, telle que 0.0.0.0 pour IPv4 et :: pour IPv6.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-112">Wildcard indicates binding to the wildcard address, such as 0.0.0.0 for IPv4 and :: for IPv6.</span></span> <span data-ttu-id="f7ce8-113">Spécifique indique la liaison à une interface spécifique, telle que la liaison d’une adresse IP assignée à un adaptateur.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-113">Specific indicates binding to a specific interface, such as binding an IP address assigned to an adapter.</span></span> <span data-ttu-id="f7ce8-114">Specific2 indique la liaison à une adresse spécifique autre que l’adresse liée dans le cas spécifique.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-114">Specific2 indicates binding to a specific address other than the address bound to in the Specific case.</span></span>

> [!Note]  
> <span data-ttu-id="f7ce8-115">Le cas Specific2 s’applique uniquement lorsque la première liaison est effectuée avec une adresse spécifique ; dans le cas où le premier Socket est lié au caractère générique, l’entrée pour spécifique couvre tous les cas d’adresse spécifiques.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-115">The Specific2 case is applicable only when the first bind is performed with a specific address; for the case in which the first socket is bound to the wildcard, the entry for Specific covers all specific address cases.</span></span>

 

<span data-ttu-id="f7ce8-116">Par exemple, imaginez un ordinateur avec deux interfaces IP : 10.0.0.1 et 10.99.99.99.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-116">For example, consider a computer with two IP interfaces: 10.0.0.1 and 10.99.99.99.</span></span> <span data-ttu-id="f7ce8-117">Si la première liaison a pour valeur 10.0.0.1 et le port 5150 avec l' \_ option so EXCLUSIVEADDRUSE définie, alors la deuxième liaison à 10.99.99.99 et le port 5150 avec une ou plusieurs options définies (ou aucune) sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-117">If the first bind is to 10.0.0.1 and port 5150 with the SO\_EXCLUSIVEADDRUSE option set, then the second bind to 10.99.99.99 and port 5150 with any or no options set succeeds.</span></span> <span data-ttu-id="f7ce8-118">Toutefois, si le premier Socket est lié à l’adresse générique (0.0.0.0) et au port 5150 avec \_ EXCLUSIVEADDRUSE défini, toute liaison suivante au même port, quelle que soit l’adresse IP, échouera avec WSAEADDRINUSE (10048) ou WSAEACCESS (10013), selon les options définies sur le deuxième socket de liaison.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-118">However, if the first socket is bound to the wildcard address (0.0.0.0) and port 5150 with SO\_EXCLUSIVEADDRUSE set, any subsequent bind to the same port—regardless of IP address—will fail with either WSAEADDRINUSE (10048) or WSAEACCESS (10013), depending on which options were set on the second bind socket.</span></span>

### <a name="bind-behavior-with-various-options-set"></a><span data-ttu-id="f7ce8-119">Comportement de liaison avec les différentes options définies</span><span class="sxs-lookup"><span data-stu-id="f7ce8-119">Bind Behavior with Various Options Set</span></span>



<span data-ttu-id="f7ce8-120">Deuxième liaison</span><span class="sxs-lookup"><span data-stu-id="f7ce8-120">Second bind</span></span>

<span data-ttu-id="f7ce8-121">Première liaison</span><span class="sxs-lookup"><span data-stu-id="f7ce8-121">First bind</span></span>

<span data-ttu-id="f7ce8-122">*\_EXCLUSIVEADDRUSE*</span><span class="sxs-lookup"><span data-stu-id="f7ce8-122">*SO\_EXCLUSIVEADDRUSE*</span></span>

<span data-ttu-id="f7ce8-123">*Aucune option* ou *\_ REUSEADDR*</span><span class="sxs-lookup"><span data-stu-id="f7ce8-123">*No options* or *SO\_REUSEADDR*</span></span>

<span data-ttu-id="f7ce8-124">*Caractère générique*</span><span class="sxs-lookup"><span data-stu-id="f7ce8-124">*Wildcard*</span></span>

<span data-ttu-id="f7ce8-125">*Spécifique*</span><span class="sxs-lookup"><span data-stu-id="f7ce8-125">*Specific*</span></span>

<span data-ttu-id="f7ce8-126">*Caractère générique*</span><span class="sxs-lookup"><span data-stu-id="f7ce8-126">*Wildcard*</span></span>

<span data-ttu-id="f7ce8-127">*Spécifique*</span><span class="sxs-lookup"><span data-stu-id="f7ce8-127">*Specific*</span></span>

<span data-ttu-id="f7ce8-128">$ {ROWSPAN3} $*donc \_ EXCLUSIVEADDRUSE*$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f7ce8-128">${ROWSPAN3}$*SO\_EXCLUSIVEADDRUSE*${REMOVE}$</span></span>  

<span data-ttu-id="f7ce8-129">*Caractère générique*</span><span class="sxs-lookup"><span data-stu-id="f7ce8-129">*Wildcard*</span></span>

<span data-ttu-id="f7ce8-130">Échec (10048)</span><span class="sxs-lookup"><span data-stu-id="f7ce8-130">Fail (10048)</span></span>

<span data-ttu-id="f7ce8-131">Échec (10048)</span><span class="sxs-lookup"><span data-stu-id="f7ce8-131">Fail (10048)</span></span>

<span data-ttu-id="f7ce8-132">Échec (10048)</span><span class="sxs-lookup"><span data-stu-id="f7ce8-132">Fail (10048)</span></span>

<span data-ttu-id="f7ce8-133">Échec (10048)</span><span class="sxs-lookup"><span data-stu-id="f7ce8-133">Fail (10048)</span></span>

<span data-ttu-id="f7ce8-134">*Spécifique*</span><span class="sxs-lookup"><span data-stu-id="f7ce8-134">*Specific*</span></span>

<span data-ttu-id="f7ce8-135">Échec (10048)</span><span class="sxs-lookup"><span data-stu-id="f7ce8-135">Fail (10048)</span></span>

<span data-ttu-id="f7ce8-136">Échec (10048)</span><span class="sxs-lookup"><span data-stu-id="f7ce8-136">Fail (10048)</span></span>

<span data-ttu-id="f7ce8-137">Échec (10048)</span><span class="sxs-lookup"><span data-stu-id="f7ce8-137">Fail (10048)</span></span>

<span data-ttu-id="f7ce8-138">Échec (10048)</span><span class="sxs-lookup"><span data-stu-id="f7ce8-138">Fail (10048)</span></span>

<span data-ttu-id="f7ce8-139">*Specific2*</span><span class="sxs-lookup"><span data-stu-id="f7ce8-139">*Specific2*</span></span>

<span data-ttu-id="f7ce8-140">n/a</span><span class="sxs-lookup"><span data-stu-id="f7ce8-140">n/a</span></span>

<span data-ttu-id="f7ce8-141">Succès</span><span class="sxs-lookup"><span data-stu-id="f7ce8-141">Success</span></span>

<span data-ttu-id="f7ce8-142">n/a</span><span class="sxs-lookup"><span data-stu-id="f7ce8-142">n/a</span></span>

<span data-ttu-id="f7ce8-143">Succès</span><span class="sxs-lookup"><span data-stu-id="f7ce8-143">Success</span></span>

<span data-ttu-id="f7ce8-144">$ {ROWSPAN3} $*no options*$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f7ce8-144">${ROWSPAN3}$*No options*${REMOVE}$</span></span>  

<span data-ttu-id="f7ce8-145">*Caractère générique*</span><span class="sxs-lookup"><span data-stu-id="f7ce8-145">*Wildcard*</span></span>

<span data-ttu-id="f7ce8-146">Échec (10048)</span><span class="sxs-lookup"><span data-stu-id="f7ce8-146">Fail (10048)</span></span>

<span data-ttu-id="f7ce8-147">Échec (10048)</span><span class="sxs-lookup"><span data-stu-id="f7ce8-147">Fail (10048)</span></span>

<span data-ttu-id="f7ce8-148">Échec (10048)</span><span class="sxs-lookup"><span data-stu-id="f7ce8-148">Fail (10048)</span></span>

<span data-ttu-id="f7ce8-149">Échec (10048)</span><span class="sxs-lookup"><span data-stu-id="f7ce8-149">Fail (10048)</span></span>

<span data-ttu-id="f7ce8-150">*Spécifique*</span><span class="sxs-lookup"><span data-stu-id="f7ce8-150">*Specific*</span></span>

<span data-ttu-id="f7ce8-151">Échec (10048)</span><span class="sxs-lookup"><span data-stu-id="f7ce8-151">Fail (10048)</span></span>

<span data-ttu-id="f7ce8-152">Échec (10048)</span><span class="sxs-lookup"><span data-stu-id="f7ce8-152">Fail (10048)</span></span>

<span data-ttu-id="f7ce8-153">Échec (10048)</span><span class="sxs-lookup"><span data-stu-id="f7ce8-153">Fail (10048)</span></span>

<span data-ttu-id="f7ce8-154">Échec (10048)</span><span class="sxs-lookup"><span data-stu-id="f7ce8-154">Fail (10048)</span></span>

<span data-ttu-id="f7ce8-155">*Specific2*</span><span class="sxs-lookup"><span data-stu-id="f7ce8-155">*Specific2*</span></span>

<span data-ttu-id="f7ce8-156">n/a</span><span class="sxs-lookup"><span data-stu-id="f7ce8-156">n/a</span></span>

<span data-ttu-id="f7ce8-157">Succès</span><span class="sxs-lookup"><span data-stu-id="f7ce8-157">Success</span></span>

<span data-ttu-id="f7ce8-158">n/a</span><span class="sxs-lookup"><span data-stu-id="f7ce8-158">n/a</span></span>

<span data-ttu-id="f7ce8-159">Succès</span><span class="sxs-lookup"><span data-stu-id="f7ce8-159">Success</span></span>

<span data-ttu-id="f7ce8-160">$ {ROWSPAN3} $*donc \_ REUSEADDR*$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f7ce8-160">${ROWSPAN3}$*SO\_REUSEADDR*${REMOVE}$</span></span>  

<span data-ttu-id="f7ce8-161">*Caractère générique*</span><span class="sxs-lookup"><span data-stu-id="f7ce8-161">*Wildcard*</span></span>

<span data-ttu-id="f7ce8-162">Échec (10013)</span><span class="sxs-lookup"><span data-stu-id="f7ce8-162">Fail (10013)</span></span>

<span data-ttu-id="f7ce8-163">Échec (10013)</span><span class="sxs-lookup"><span data-stu-id="f7ce8-163">Fail (10013)</span></span>

<span data-ttu-id="f7ce8-164">Opération réussie\*</span><span class="sxs-lookup"><span data-stu-id="f7ce8-164">Success\*</span></span>

<span data-ttu-id="f7ce8-165">Succès</span><span class="sxs-lookup"><span data-stu-id="f7ce8-165">Success</span></span>

<span data-ttu-id="f7ce8-166">*Spécifique*</span><span class="sxs-lookup"><span data-stu-id="f7ce8-166">*Specific*</span></span>

<span data-ttu-id="f7ce8-167">Échec (10013)</span><span class="sxs-lookup"><span data-stu-id="f7ce8-167">Fail (10013)</span></span>

<span data-ttu-id="f7ce8-168">Échec (10013)</span><span class="sxs-lookup"><span data-stu-id="f7ce8-168">Fail (10013)</span></span>

<span data-ttu-id="f7ce8-169">Succès</span><span class="sxs-lookup"><span data-stu-id="f7ce8-169">Success</span></span>

<span data-ttu-id="f7ce8-170">Opération réussie\*</span><span class="sxs-lookup"><span data-stu-id="f7ce8-170">Success\*</span></span>

<span data-ttu-id="f7ce8-171">*Specific2*</span><span class="sxs-lookup"><span data-stu-id="f7ce8-171">*Specific2*</span></span>

<span data-ttu-id="f7ce8-172">n/a</span><span class="sxs-lookup"><span data-stu-id="f7ce8-172">n/a</span></span>

<span data-ttu-id="f7ce8-173">Succès</span><span class="sxs-lookup"><span data-stu-id="f7ce8-173">Success</span></span>

<span data-ttu-id="f7ce8-174">n/a</span><span class="sxs-lookup"><span data-stu-id="f7ce8-174">n/a</span></span>

<span data-ttu-id="f7ce8-175">Succès</span><span class="sxs-lookup"><span data-stu-id="f7ce8-175">Success</span></span>

<span data-ttu-id="f7ce8-176">\* Le comportement n’est pas défini en ce qui concerne le socket qui recevra les paquets.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-176">\* The behavior is undefined as to which socket will receive packets.</span></span>



 

<span data-ttu-id="f7ce8-177">Dans le cas où la première liaison ne définit aucune option ou \_ REUSEADDR, et que la deuxième liaison exécute un so \_ REUSEADDR, le deuxième Socket a détenir le port et le comportement concernant le socket qui recevra les paquets.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-177">In the case where the first bind sets no options or SO\_REUSEADDR, and the second bind performs a SO\_REUSEADDR, the second socket has overtaken the port and behavior regarding which socket will receive packets is undetermined.</span></span> <span data-ttu-id="f7ce8-178">\_EXCLUSIVEADDRUSE a donc été introduit pour résoudre ce problème.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-178">SO\_EXCLUSIVEADDRUSE was introduced to address this situation.</span></span>

<span data-ttu-id="f7ce8-179">Un socket avec \_ EXCLUSIVEADDRUSE Set ne peut pas toujours être réutilisé immédiatement après la fermeture du Socket.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-179">A socket with SO\_EXCLUSIVEADDRUSE set cannot always be reused immediately after socket closure.</span></span> <span data-ttu-id="f7ce8-180">Par exemple, si un socket d’écoute avec l’ensemble d’indicateurs exclusifs accepte une connexion après laquelle le socket d’écoute est fermé, un autre socket ne peut pas se lier au même port que le premier socket d’écoute avec l’indicateur exclusif tant que la connexion acceptée n’est plus active.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-180">For example, if a listening socket with the exclusive flag set accepts a connection after which the listening socket is closed, another socket cannot bind to the same port as the first listening socket with the exclusive flag until the accepted connection is no longer active.</span></span>

<span data-ttu-id="f7ce8-181">Cette situation peut être assez compliquée ; même si le socket a été fermé, le transport sous-jacent peut ne pas mettre fin à sa connexion.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-181">This situation can be quite complicated; even though the socket has been closed, the underlying transport may not terminate its connection.</span></span> <span data-ttu-id="f7ce8-182">Même après la fermeture du socket, le système doit envoyer toutes les données mises en mémoire tampon, transmettre une déconnexion normale à l’homologue et attendre une déconnexion normale de l’homologue.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-182">Even after the socket is closed, the system must send all of the buffered data, transmit a graceful disconnect to the peer, and wait for a graceful disconnect from the peer.</span></span> <span data-ttu-id="f7ce8-183">Il est donc possible que le transport sous-jacent ne libère jamais la connexion, par exemple lorsque l’homologue publie une fenêtre de taille nulle, ou d’autres attaques.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-183">It is therefore possible that the underlying transport may never release the connection, such as when the peer advertises a zero-size window, or other such attacks.</span></span> <span data-ttu-id="f7ce8-184">Dans l’exemple précédent, le socket d’écoute a été fermé après l’acceptation d’une connexion cliente.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-184">In the previous example, the listening socket was closed after a client connection was accepted.</span></span> <span data-ttu-id="f7ce8-185">Désormais, même si la connexion client est fermée, le port ne peut pas être réutilisé si la connexion cliente reste dans un état actif en raison de données non acquittées, etc.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-185">Now even if the client connection is closed, the port still may not be reused if the client connection remains in an active state because of unacknowledged data, and so forth.</span></span>

<span data-ttu-id="f7ce8-186">Pour éviter cette situation, les applications doivent garantir un arrêt correct : appeler [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) avec l' \_ indicateur SD Send, puis attendre dans une boucle [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) jusqu’à ce que zéro octet soit retourné.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-186">To avoid this situation, applications should ensure a graceful shutdown: call [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) with the SD\_SEND flag, then wait in a [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) loop until zero bytes are returned.</span></span> <span data-ttu-id="f7ce8-187">Cela permet d’éviter le problème associé à la réutilisation des ports, garantit que toutes les données ont été reçues par l’homologue et vérifie que toutes les données ont été reçues avec succès.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-187">Doing so avoids the problem associated with port reuse, guarantees all data was received by the peer, and assures the peer that all its data was successfully received.</span></span>

<span data-ttu-id="f7ce8-188">L’option si oui \_ peut être définie sur un socket pour empêcher le port de passer à l’un des États d’attente actifs ; Toutefois, cette opération est déconseillée, car cela peut entraîner des effets indésirables, car cela peut entraîner la réinitialisation de la connexion.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-188">The SO\_LINGER option may be set on a socket to prevent the port going into one of the active wait states; however, doing so is discouraged because it can lead to undesired effects, because it can cause the connection to be reset.</span></span> <span data-ttu-id="f7ce8-189">Par exemple, si les données ont été reçues mais n’ont pas encore été acceptées par l’homologue, et que l’ordinateur local ferme le socket avec l’ensemble des éléments restants \_ , la connexion est réinitialisée et l’homologue ignore les données non acquittées.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-189">For example, if data has been received but not yet acknowledged by the peer, and the local computer closes the socket with SO\_LINGER set, the connection is reset and the peer discards the unacknowledged data.</span></span> <span data-ttu-id="f7ce8-190">En outre, il est difficile de choisir une durée de maintien appropriée. une valeur trop petite entraîne de nombreuses connexions abandonnées, tandis qu’un délai d’expiration important peut rendre le système vulnérable aux attaques par déni de service en établissant de nombreuses connexions et en bloquant de nombreux threads d’application.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-190">Also, picking a suitable time to linger is difficult; a value too small results in many aborted connections, while a large timeout can leave the system vulnerable to denial of service attacks by establishing many connections, and thereby stalling numerous application threads.</span></span>

> [!Note]  
> <span data-ttu-id="f7ce8-191">Un socket qui utilise l’option SO \_ EXCLUSIVEADDRUSE doit être arrêté correctement avant de le fermer.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-191">A socket that is using the SO\_EXCLUSIVEADDRUSE option must be shut down properly prior to closing it.</span></span> <span data-ttu-id="f7ce8-192">Dans le cas contraire, vous risquez de provoquer une attaque par déni de service si le service associé doit redémarrer.</span><span class="sxs-lookup"><span data-stu-id="f7ce8-192">Failure to do so can cause a denial of service attack if the associated service needs to restart.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f7ce8-193">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7ce8-193">Requirements</span></span>



| <span data-ttu-id="f7ce8-194">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7ce8-194">Requirement</span></span> | <span data-ttu-id="f7ce8-195">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7ce8-195">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7ce8-196">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7ce8-196">Minimum supported client</span></span><br/> | <span data-ttu-id="f7ce8-197">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7ce8-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f7ce8-198">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7ce8-198">Minimum supported server</span></span><br/> | <span data-ttu-id="f7ce8-199">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7ce8-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f7ce8-200">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7ce8-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7ce8-201"><dt>Winsock2. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7ce8-201"><dt>Winsock2.h</dt></span></span> </dl> |



 

 




