---
description: Active l’extensibilité de port local pour un Socket.
ms.assetid: c5142baf-9e2d-4c06-8719-9090fd2d9487
title: SO_PORT_SCALABILITY (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565caeb472ac5cb15061d32b47a048a9a210885e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113003"
---
# <a name="so_port_scalability"></a><span data-ttu-id="8f6ea-103">\_ \_ l’évolutivité des ports</span><span class="sxs-lookup"><span data-stu-id="8f6ea-103">SO\_PORT\_SCALABILITY</span></span>

<span data-ttu-id="8f6ea-104">L’option de socket d' **\_ \_ extensibilité de port so** active l’évolutivité de port local pour un Socket.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-104">The **SO\_PORT\_SCALABILITY** socket option enables local port scalability for a socket.</span></span>

<dl> <dt>

<span data-ttu-id="8f6ea-105"><span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**\_ \_ l’évolutivité des ports**</span><span class="sxs-lookup"><span data-stu-id="8f6ea-105"><span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**SO\_PORT\_SCALABILITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f6ea-106">0x3006</span><span class="sxs-lookup"><span data-stu-id="8f6ea-106">0x3006</span></span>
</dt> <dt>



<span data-ttu-id="8f6ea-107">L’option de socket d' **\_ \_ extensibilité de port so** permet l’évolutivité de port local en permettant l’optimisation de l’allocation de port en allouant des ports génériques plusieurs fois pour différentes paires de ports d’adresse locale sur un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-107">The **SO\_PORT\_SCALABILITY** socket option enables local port scalability by allowing port allocation to be maximized by allocating wildcard ports multiple times for different local address port pairs on a local machine.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f6ea-108">Notes</span><span class="sxs-lookup"><span data-stu-id="8f6ea-108">Remarks</span></span>

<span data-ttu-id="8f6ea-109">Remarque : sur les plateformes où \_ \_ l’évolutivité des ports et la \_ réutilisation \_ UNICASTPORT sont prises en charge, préférez utiliser \_ \_ UNICASTPORT.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-109">Note: on platforms where both SO\_PORT\_SCALABILITY and SO\_REUSE\_UNICASTPORT are supported, prefer to use SO\_REUSE\_UNICASTPORT.</span></span>

<span data-ttu-id="8f6ea-110">Les environnements de serveur proxy présentent des problèmes d’évolutivité en raison de la disponibilité limitée du port local.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-110">Proxy server environments have scalability issues because of limited local port availability.</span></span> <span data-ttu-id="8f6ea-111">Pour contourner ce cas, vous pouvez ajouter d’autres adresses IP à la machine.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-111">One way to work around this is to add more IP addresses to the machine.</span></span> <span data-ttu-id="8f6ea-112">Toutefois, par défaut, les ports génériques utilisés avec la fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) sont limités à la taille de la plage de ports dynamiques sur l’ordinateur local (jusqu’à 64 Ko de ports, mais généralement moins), quel que soit le nombre d’adresses IP sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-112">However, by default wildcard ports used with the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function are limited to the size of the dynamic port range on the local machine (up to 64K ports, but usually less) no matter the number of IP addresses on the local machine.</span></span> <span data-ttu-id="8f6ea-113">Pour contourner ce dysfonctionnement, l’application doit conserver son propre pool de ports avec la réservation de port ou à l’aide de l’heuristique.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-113">Working around this requires the application to maintain its own port pool either with port reservation or by using heuristics.</span></span>

<span data-ttu-id="8f6ea-114">Pour éviter que chaque application nécessitant une évolutivité gère son propre pool de ports et qu’elle permet une plus grande évolutivité tout en conservant la compatibilité des applications, Windows Server 2008 a introduit l’option de socket de mise à l' **\_ \_ échelle des ports afin** d’optimiser l’allocation des ports génériques.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-114">To avoid having every application that requires scalability manage its own port pool, and to allow for greater scalability while maintaining application compatibility, Windows Server 2008 introduced the **SO\_PORT\_SCALABILITY** socket option to help maximize wildcard port allocation.</span></span> <span data-ttu-id="8f6ea-115">L’allocation de port est optimisée en permettant à une application d’allouer des ports génériques pour chaque paire adresse locale et port unique.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-115">Port allocation is maximized by allowing an application to allocate wildcard ports for each unique local address and port pair.</span></span> <span data-ttu-id="8f6ea-116">Par conséquent, si un ordinateur local possède quatre adresses IP, il est possible d’allouer jusqu’à 256 K ports génériques (64 ports × 4 adresses IP) par des demandes de fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) de caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-116">So if a local machine has four IP addresses, then up to 256 K wildcard ports (64 K ports × 4 IP addresses) can be allocated by wildcard [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function requests.</span></span>

<span data-ttu-id="8f6ea-117">Lorsque l’option de socket d' **\_ \_ extensibilité de port so** est définie sur un socket et qu’un appel à la fonction [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) est effectué pour une adresse spécifiée et un port générique (le paramètre *Name* est défini avec une adresse spécifique et un port de 0), Winsock alloue un port pour l’adresse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-117">When the **SO\_PORT\_SCALABILITY** socket option is set on a socket and a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is made for a specified address and wildcard port (the *name* parameter is set with a specific address and a port of 0), Winsock will allocate a port for the specified address.</span></span> <span data-ttu-id="8f6ea-118">Cette allocation sera basée sur toutes les adresses IP et ports/par adresse possibles sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-118">This allocation will be based on all of the possible IP addresses and ports/per address on the local computer.</span></span> <span data-ttu-id="8f6ea-119">Si un port générique est acquis à l’aide de l’option de mise à l' **\_ \_ échelle du port** , ce port ne peut pas être alloué par un autre socket sans l’option de mise à l' **\_ \_ échelle du port** .</span><span class="sxs-lookup"><span data-stu-id="8f6ea-119">If a wildcard port is acquired using the **SO\_PORT\_SCALABILITY** option, that port cannot be allocated by another socket without the **SO\_PORT\_SCALABILITY** option.</span></span> <span data-ttu-id="8f6ea-120">Cette restriction est en place afin d’éviter les problèmes de compatibilité descendante avec les applications qui supposent qu’un port local générique ne peut pas être réutilisé.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-120">This restriction is in place to avoid backward-compatibility problems with applications that assume a wildcard local port cannot be reused.</span></span> <span data-ttu-id="8f6ea-121">Notez que cela signifie que les applications qui acquièrent un grand nombre de ports à l’aide de **pour \_ \_ l’évolutivité** des ports peuvent priver des applications héritées de ports.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-121">Note that this means that applications which acquire a large number of ports using **SO\_PORT\_SCALABILITY** can starve legacy applications of ports.</span></span> <span data-ttu-id="8f6ea-122">Si tous les ports éphémères disponibles ont été acquis pour au moins une adresse avec l' **\_ \_ évolutivité des ports** , aucune allocation de port générique n’est alors possible sans l’option de Socket.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-122">If all available ephemeral ports have been acquired for at least one address with **SO\_PORT\_SCALABILITY** , then no more wildcard port allocations are possible without the socket option.</span></span>

<span data-ttu-id="8f6ea-123">Pour avoir un effet, l’option de mise à l' **\_ \_ échelle du port** doit être définie avant l’appel de la fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) .</span><span class="sxs-lookup"><span data-stu-id="8f6ea-123">To have any effect, the **SO\_PORT\_SCALABILITY** option must be set before the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called.</span></span> <span data-ttu-id="8f6ea-124">Vous trouverez ci-dessous un exemple de l’utilisation de cette méthode sur un ordinateur avec deux adresses :</span><span class="sxs-lookup"><span data-stu-id="8f6ea-124">An example of how this would be used on a computer with two addresses is outlined below:</span></span>

-   <span data-ttu-id="8f6ea-125">La fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) est appelée par un processus pour créer un Socket.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-125">The [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function is called by a process to create a socket.</span></span>
-   <span data-ttu-id="8f6ea-126">La fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) est appelée pour activer l’option de socket de mise à l' **\_ \_ échelle du port,** sur le socket nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-126">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function is called to enable the **SO\_PORT\_SCALABILITY** socket option on the newly created socket.</span></span>
-   <span data-ttu-id="8f6ea-127">La fonction [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) est appelée pour effectuer une liaison sur l’une des adresses IP de l’ordinateur local et le port 0.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-127">The [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called to do a bind on one of the local computer's IP addresses and port 0.</span></span>
-   <span data-ttu-id="8f6ea-128">La fonction [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) est ensuite appelée pour se connecter à une adresse IP distante.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-128">The [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function is then called to connect to a remote IP address.</span></span> <span data-ttu-id="8f6ea-129">Le socket est utilisé par l’application en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-129">The socket is used by the application as needed.</span></span>
-   <span data-ttu-id="8f6ea-130">Une fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) est appelée par le même processus (éventuellement un thread différent) pour créer un deuxième Socket.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-130">A [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function is called by the same process (possibly a different thread) to create a second socket.</span></span>
-   <span data-ttu-id="8f6ea-131">La fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) est appelée pour activer l’option de socket de mise à l' **\_ \_ échelle du port,** sur le second Socket nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-131">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function is called to enable the **SO\_PORT\_SCALABILITY** socket option on the newly created second socket.</span></span>
-   <span data-ttu-id="8f6ea-132">La fonction [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) est appelée avec la deuxième adresse IP et le port 0 de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-132">The [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called with the local computer's second IP address and port 0.</span></span> <span data-ttu-id="8f6ea-133">Même lorsque tous les ports ont été alloués précédemment, cet appel réussit, car plusieurs adresses IP sont disponibles sur l’ordinateur local et l’option de socket de mise à l' **\_ \_ échelle du port so** a été définie sur les deux sockets dans le même processus.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-133">Even when all ports have been previously allocated, this call succeeds because there are multiple IP addresses available on the local computer and the **SO\_PORT\_SCALABILITY** socket option was set on both sockets in the same process.</span></span>
-   <span data-ttu-id="8f6ea-134">La fonction [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) est ensuite appelée pour se connecter à une adresse IP distante.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-134">The [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function is then called to connect to a remote IP address.</span></span> <span data-ttu-id="8f6ea-135">Le deuxième Socket est utilisé par l’application en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-135">The second socket is used by the application as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f6ea-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f6ea-136">Requirements</span></span>



| <span data-ttu-id="8f6ea-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f6ea-137">Requirement</span></span> | <span data-ttu-id="8f6ea-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f6ea-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8f6ea-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f6ea-139">Minimum supported client</span></span><br/> | <span data-ttu-id="8f6ea-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f6ea-140">None supported</span></span><br/>                                                           |
| <span data-ttu-id="8f6ea-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f6ea-141">Minimum supported server</span></span><br/> | <span data-ttu-id="8f6ea-142">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f6ea-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8f6ea-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="8f6ea-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f6ea-144"><dt>Ws2def. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f6ea-144"><dt>Ws2def.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f6ea-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f6ea-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f6ea-146">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="8f6ea-146">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="8f6ea-147">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="8f6ea-147">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="8f6ea-148">**Options de socket de socket SOL \_**</span><span class="sxs-lookup"><span data-stu-id="8f6ea-148">**SOL\_SOCKET Socket Options**</span></span>](sol-socket-socket-options.md)
</dt> <dt>

[<span data-ttu-id="8f6ea-149">**Options de socket**</span><span class="sxs-lookup"><span data-stu-id="8f6ea-149">**Socket Options**</span></span>](socket-options.md)
</dt> </dl>

 

 




