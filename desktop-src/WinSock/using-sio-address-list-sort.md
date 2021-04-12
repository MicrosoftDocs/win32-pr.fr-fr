---
description: La \_ \_ liste d’adresses SIO \_ trie IOCTL permet aux développeurs d’applications de trier une liste d’adresses de destination IPv6 et IPv4 pour déterminer la meilleure adresse disponible pour établir une connexion. La \_ \_ liste d’adresses SIO \_ Tri IOCTL est prise en charge sur Windows XP et versions ultérieures.
ms.assetid: bf380ddf-8171-4ef4-be47-94c7a6aabf0a
title: Utilisation de SIO_ADDRESS_LIST_SORT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6452023b69ccf72c78b393c5059fee497997af51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210227"
---
# <a name="using-sio_address_list_sort"></a><span data-ttu-id="866b5-104">Utilisation du \_ \_ tri de liste d’adresses SIO \_</span><span class="sxs-lookup"><span data-stu-id="866b5-104">Using SIO\_ADDRESS\_LIST\_SORT</span></span>

<span data-ttu-id="866b5-105">La **\_ liste d’adresses SIO \_ \_ trie** IOCTL permet aux développeurs d’applications de trier une liste d’adresses de destination IPv6 et IPv4 pour déterminer la meilleure adresse disponible pour établir une connexion.</span><span class="sxs-lookup"><span data-stu-id="866b5-105">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL allows application developers to sort a list of IPv6 and IPv4 destination addresses to determine the best available address for making a connection.</span></span> <span data-ttu-id="866b5-106">La **\_ liste d’adresses SIO \_ \_ Tri** IOCTL est prise en charge sur Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="866b5-106">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL is supported on Windows XP and later.</span></span>

<span data-ttu-id="866b5-107">Sur Windows Vista et versions ultérieures, la fonction [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) prend la liste fournie d’adresses de destination IP potentielles, associe les adresses de destination aux adresses IP locales de l’ordinateur hôte et trie les paires en fonction de la meilleure correspondance d’adresse pour les communications entre les deux pairs.</span><span class="sxs-lookup"><span data-stu-id="866b5-107">On Windows Vista and later, the [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) function takes a supplied list of potential IP destination addresses, pairs the destination addresses with the host machine's local IP addresses, and sorts the pairs according to which address pair is best suited for communication between the two peers.</span></span> <span data-ttu-id="866b5-108">La fonction **CreateSortedAddressPairs** doit être utilisée à la place de la **liste d’adresses SIO \_ \_ \_ Tri** IOCTL sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="866b5-108">The **CreateSortedAddressPairs** function should be used instead of the **SIO\_ADDRESS\_LIST\_SORT** IOCTL on Windows Vista and later.</span></span>

<span data-ttu-id="866b5-109">Les sections suivantes décrivent les considérations relatives à l’utilisation du **\_ tri de \_ liste \_ d’adresses SIO**.</span><span class="sxs-lookup"><span data-stu-id="866b5-109">The following sections describe usage considerations for **SIO\_ADDRESS\_LIST\_SORT**.</span></span>

## <a name="parameters"></a><span data-ttu-id="866b5-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="866b5-110">Parameters</span></span>

<span data-ttu-id="866b5-111">La mémoire tampon transmise à **SIO \_ address \_ List \_ sort** est une structure de [**\_ \_ liste d’adresses de sockets**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="866b5-111">The buffer passed to **SIO\_ADDRESS\_LIST\_SORT** is a [**SOCKET\_ADDRESS\_LIST**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) structure.</span></span> <span data-ttu-id="866b5-112">Chaque [**\_ adresse de socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) de la liste doit être au \_ format sockaddr in6.</span><span class="sxs-lookup"><span data-stu-id="866b5-112">Each [**SOCKET\_ADDRESS**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) in the list must be in SOCKADDR\_IN6 format.</span></span>

<span data-ttu-id="866b5-113">La **\_ liste d’adresses SIO \_ \_ Trier** IOCTL trie les adresses IPv6 et IPv4 sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="866b5-113">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL sorts both IPv6 and IPv4 addresses on Windows Vista and later.</span></span> <span data-ttu-id="866b5-114">Toutes les adresses IPv4 de la liste à trier doivent être au format d’adresse IPv6 mappé IPv4.</span><span class="sxs-lookup"><span data-stu-id="866b5-114">Any IPv4 addresses in the list to be sorted must be in the IPv4-mapped IPv6 address format.</span></span> <span data-ttu-id="866b5-115">Pour plus d’informations sur le format d’adresse IPv6 mappée IPv4, consultez [sockets à double pile](dual-stack-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="866b5-115">For more information on the IPv4-mapped IPv6 address format, see [Dual-Stack Sockets](dual-stack-sockets.md).</span></span>

<span data-ttu-id="866b5-116">Sur Windows Server 2003 et Windows XP, le **tri de la \_ \_ liste \_ d’adresses SIO** trie uniquement les adresses IPv6.</span><span class="sxs-lookup"><span data-stu-id="866b5-116">On Windows Server 2003, and Windows XP, **SIO\_ADDRESS\_LIST\_SORT** sorts only IPv6 addresses.</span></span> <span data-ttu-id="866b5-117">Les adresses IPv4 dans le format d’adresse IPv6 mappée IPv4 ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="866b5-117">IPv4 addresses in the IPv4-mapped IPv6 address format are not supported.</span></span>

<span data-ttu-id="866b5-118">Lors de la sortie, le membre **iAddressCount** de la structure de [**liste d' \_ adresses \_ de sockets**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) peut être plus petit que en entrée si le code IOCTL détermine que certaines adresses de destination ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="866b5-118">On output, the **iAddressCount** member of the [**SOCKET\_ADDRESS\_LIST**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) structure may be smaller than on input if the IOCTL code determines that some destination addresses are invalid.</span></span>

## <a name="sorting-determination"></a><span data-ttu-id="866b5-119">Détermination du tri</span><span class="sxs-lookup"><span data-stu-id="866b5-119">Sorting Determination</span></span>

<span data-ttu-id="866b5-120">L’ordre de tri des adresses IPv6 pour le \_ tri de la liste d’adresses SIO \_ \_ est basé sur la table de stratégie de préfixe.</span><span class="sxs-lookup"><span data-stu-id="866b5-120">The sorting order for IPv6 addresses for the SIO\_ADDRESS\_LIST\_SORT IOCTL is based on the prefix policy table.</span></span> <span data-ttu-id="866b5-121">La table de stratégie de préfixe est configurée à l’aide de l’utilitaire de ligne de commande *Netsh.exe* .</span><span class="sxs-lookup"><span data-stu-id="866b5-121">The prefix policy table is configured using the *Netsh.exe* command line utility.</span></span> <span data-ttu-id="866b5-122">Les extraits de ligne de commande suivants illustrent les commandes de configuration de la table de préfixe *Netsh.exe* de base :</span><span class="sxs-lookup"><span data-stu-id="866b5-122">The following command line snippets illustrate basic *Netsh.exe* prefix policy table configuration commands:</span></span>

``` syntax
netsh interface ipv6 show prefixpolicies
netsh interface ipv6 add prefixpolicy ::/96 3 4
netsh interface ipv6 delete prefixpolicy ::/96
netsh interface ipv6 set prefixpolicy ::/96 3 4
```

> [!Note]  
> <span data-ttu-id="866b5-123">Sur Windows Server 2003 et Windows XP, la première commande netsh listée ci-dessus était la suivante.</span><span class="sxs-lookup"><span data-stu-id="866b5-123">On Windows Server 2003 and Windows XP, the first netsh command listed above was as follows.</span></span> <span data-ttu-id="866b5-124">Toutes les autres commandes associées sont identiques.</span><span class="sxs-lookup"><span data-stu-id="866b5-124">All other related commands are the same.</span></span>

 

``` syntax
netsh interface ipv6 show prefixpolicy
```

<span data-ttu-id="866b5-125">Le classement des adresses est également déterminé par un algorithme décrit dans le document RFC 3484 sur la *sélection d’adresses par défaut pour le protocole IPv6 (Internet Protocol version 6)* publié par l’IETF.</span><span class="sxs-lookup"><span data-stu-id="866b5-125">Address ordering is also determined by an algorithm outlined in the RFC 3484 on *Default Address Selection for Internet Protocol version 6 (IPv6)* published by the IETF.</span></span> <span data-ttu-id="866b5-126">Pour plus d’informations, consultez [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484).</span><span class="sxs-lookup"><span data-stu-id="866b5-126">For more information, see [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484).</span></span> <span data-ttu-id="866b5-127">(Cette ressource peut uniquement être disponible en anglais.)</span><span class="sxs-lookup"><span data-stu-id="866b5-127">(This resource may only be available in English.)</span></span>

<span data-ttu-id="866b5-128">La **\_ liste d’adresses SIO \_ \_ sort** d’IOCTL trie les adresses du meilleur au pire, et renseigne les membres de l' **\_ \_ ID d’étendue Sin6** , si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="866b5-128">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL sorts addresses from best to worst, and fills in **sin6\_scope\_id** members, if needed.</span></span> <span data-ttu-id="866b5-129">Pour les adresses locales de site, le tri de la \_ liste d’adresses SIO \_ \_ peut remplir l’ID de l’étendue ou supprimer l’adresse.</span><span class="sxs-lookup"><span data-stu-id="866b5-129">For site-local addresses, SIO\_ADDRESS\_LIST\_SORT either fills in the scope-id, or removes the address.</span></span>

<span data-ttu-id="866b5-130">La **\_ liste d’adresses SIO \_ \_ Tri** IOCTL ignore l’adresse source liée au socket et trie uniquement en fonction de la liste d’adresses de destination transmise en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="866b5-130">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL ignores the source address bound to the socket and only sorts by the destination address list passed as a parameter.</span></span>

<span data-ttu-id="866b5-131">La fonction [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) doit être utilisée à la place de la **liste d’adresses SIO \_ \_ \_ Tri** IOCTL sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="866b5-131">The [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) function should be used instead of the **SIO\_ADDRESS\_LIST\_SORT** IOCTL on Windows Vista and later.</span></span> <span data-ttu-id="866b5-132">La fonction **CreateSortedAddressPairs** retourne une liste de paires d’adresses qui contient une adresse source locale et une adresse de destination.</span><span class="sxs-lookup"><span data-stu-id="866b5-132">The **CreateSortedAddressPairs** function returns a list of address pairs that contains a local source address and a destination address.</span></span> <span data-ttu-id="866b5-133">Cela fournit à une application l’adresse source appropriée à utiliser pour chaque adresse de destination.</span><span class="sxs-lookup"><span data-stu-id="866b5-133">This provides an application the correct source address to use for each destination address.</span></span> <span data-ttu-id="866b5-134">Une application peut également filtrer les résultats en recherchant une adresse source spécifique.</span><span class="sxs-lookup"><span data-stu-id="866b5-134">An application can also filter the results by looking for a specific source address.</span></span> <span data-ttu-id="866b5-135">dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="866b5-135">in the results.</span></span>

## <a name="requirements"></a><span data-ttu-id="866b5-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="866b5-136">Requirements</span></span>

<span data-ttu-id="866b5-137">La **liste d’adresses SIO de \_ \_ \_ Tri** IOCTL est définie dans le fichier d’en-tête *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="866b5-137">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL is defined in the *Winsock2.h* header file.</span></span> <span data-ttu-id="866b5-138">Dans le kit de développement logiciel (SDK) Microsoft Windows publié pour Windows Vista et versions ultérieures, l’Organisation des fichiers d’en-tête a changé et **SIO \_ address \_ List \_ Tri** IOCTL est défini dans le fichier d’en-tête *Ws2def. h* .</span><span class="sxs-lookup"><span data-stu-id="866b5-138">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and **SIO\_ADDRESS\_LIST\_SORT** IOCTL is defined in the *Ws2def.h* header file.</span></span> <span data-ttu-id="866b5-139">Notez que le fichier d’en-tête *Ws2def. h* est automatiquement inclus dans *Winsock2. h* et ne doit jamais être utilisé directement.</span><span class="sxs-lookup"><span data-stu-id="866b5-139">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

<span data-ttu-id="866b5-140">La **\_ liste d’adresses SIO \_ \_ Tri** IOCTL est prise en charge sur Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="866b5-140">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL is supported on Windows XP and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="866b5-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="866b5-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="866b5-142">**CreateSortedAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="866b5-142">**CreateSortedAddressPairs**</span></span>](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs)
</dt> </dl>

 

 
