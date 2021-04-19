---
description: Permet à une application d’activer ou de désactiver le retour des informations de paquet par la fonction WSARecvMsg sur un socket IPv6.
ms.assetid: 7BF17538-BE92-44FE-BA3C-6B44F61D478A
title: Option de socket IPV6_PKTINFO (Ws2ipdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5afd5b19cbaba7f6a66f5ba6fbd85d74eb2f2e3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516462"
---
# <a name="ipv6_pktinfo-socket-option"></a><span data-ttu-id="c8714-103">\_Option de socket PKTINFO IPv6</span><span class="sxs-lookup"><span data-stu-id="c8714-103">IPV6\_PKTINFO socket option</span></span>

<span data-ttu-id="c8714-104">L' \_ option de socket PKTINFO IPv6 permet à une application d’activer ou de désactiver le retour des informations de paquets par la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) sur un socket IPv6.</span><span class="sxs-lookup"><span data-stu-id="c8714-104">The IPV6\_PKTINFO socket option allows an application to enable or disable the return of packet information by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function on an IPv6 socket..</span></span>

<span data-ttu-id="c8714-105">Pour interroger l’état de cette option de socket, appelez la fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) .</span><span class="sxs-lookup"><span data-stu-id="c8714-105">To query the status of this socket option, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function.</span></span> <span data-ttu-id="c8714-106">Pour définir cette option, appelez la fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="c8714-106">To set this option, call the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="c8714-107">Valeur d’option de socket</span><span class="sxs-lookup"><span data-stu-id="c8714-107">Socket option value</span></span>

<span data-ttu-id="c8714-108">La constante qui représente cette option de socket est 19.</span><span class="sxs-lookup"><span data-stu-id="c8714-108">The constant that represents this socket option is 19.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8714-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8714-109">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IPV6,   // level
  (int) IPV6_PKTINFO, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IPV6,   // level
  (int) IPV6_PKTINFO, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="c8714-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8714-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8714-111"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c8714-111">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8714-112">Descripteur identifiant le Socket.</span><span class="sxs-lookup"><span data-stu-id="c8714-112">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="c8714-113">de *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c8714-113">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8714-114">Niveau auquel l’option est définie.</span><span class="sxs-lookup"><span data-stu-id="c8714-114">The level at which the option is defined.</span></span> <span data-ttu-id="c8714-115">Utilisez **IPPROTO \_ IPv6** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="c8714-115">Use **IPPROTO\_IPV6** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="c8714-116">*nom_d* \[ ' $ dans\]</span><span class="sxs-lookup"><span data-stu-id="c8714-116">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8714-117">Option de socket pour laquelle obtenir ou définir la valeur.</span><span class="sxs-lookup"><span data-stu-id="c8714-117">The socket option for which to get or set the value.</span></span> <span data-ttu-id="c8714-118">Utilisez IPV6 \_ PKTINFO pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="c8714-118">Use IPV6\_PKTINFO for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="c8714-119">*optval* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c8714-119">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8714-120">Pointeur vers la mémoire tampon contenant la valeur de l’option à définir.</span><span class="sxs-lookup"><span data-stu-id="c8714-120">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="c8714-121">Ce paramètre doit pointer vers une mémoire tampon égale ou supérieure à la taille d’une valeur **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="c8714-121">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="c8714-122">Cette valeur est traitée comme une valeur booléenne avec 0 utilisé pour indiquer **false** (désactivé) et une valeur différente de zéro pour indiquer la valeur **true** (activé).</span><span class="sxs-lookup"><span data-stu-id="c8714-122">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="c8714-123">*optlen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c8714-123">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8714-124">Pointeur vers la taille, en octets, de la mémoire tampon *optval* .</span><span class="sxs-lookup"><span data-stu-id="c8714-124">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="c8714-125">Cette taille doit être supérieure ou égale à la taille d’une valeur **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="c8714-125">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8714-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c8714-126">Return value</span></span>

<span data-ttu-id="c8714-127">Si l’opération se termine avec succès, la fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) ou [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="c8714-127">If the operation completes successfully, the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) or [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function returns zero.</span></span>

<span data-ttu-id="c8714-128">Si l’opération échoue, une valeur d’erreur de SOCKET \_ est renvoyée et un code d’erreur spécifique peut être récupéré en appelant [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="c8714-128">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="c8714-129">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="c8714-129">Error code</span></span>                                                                                                                                              | <span data-ttu-id="c8714-130">Signification</span><span class="sxs-lookup"><span data-stu-id="c8714-130">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c8714-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="c8714-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="c8714-132">Un appel [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) réussi doit se produire avant l’utilisation de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="c8714-132">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="c8714-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="c8714-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="c8714-134">Le sous-système réseau a échoué.</span><span class="sxs-lookup"><span data-stu-id="c8714-134">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="c8714-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="c8714-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="c8714-136">L’un des paramètres *optval* ou *optlen* pointent vers la mémoire qui n’est pas dans une partie valide de l’espace d’adressage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c8714-136">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="c8714-137">Cette erreur est également retournée si la valeur vers laquelle pointe le paramètre *optlen* est inférieure à la taille d’une valeur **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="c8714-137">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="c8714-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="c8714-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="c8714-139">Un appel de blocage de Windows Sockets 1,1 est en cours, ou le fournisseur de services traite toujours une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="c8714-139">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="c8714-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="c8714-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="c8714-141">Argument non valide fourni.</span><span class="sxs-lookup"><span data-stu-id="c8714-141">An invalid argument was supplied.</span></span> <span data-ttu-id="c8714-142">Cette erreur est retournée si le paramètre de *niveau* est inconnu ou non valide.</span><span class="sxs-lookup"><span data-stu-id="c8714-142">This error is returned if the *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="c8714-143">Sur Windows Vista et versions ultérieures, cette erreur est également retournée si le socket était dans un état de transition.</span><span class="sxs-lookup"><span data-stu-id="c8714-143">On Windows Vista and later, this error is also returned if the socket was in a transitional state.</span></span><br/>                                     |
| <dl> <span data-ttu-id="c8714-144"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="c8714-144"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="c8714-145">L’option est inconnue ou non prise en charge par la famille de protocoles indiquée.</span><span class="sxs-lookup"><span data-stu-id="c8714-145">The option is unknown or unsupported by the indicated protocol family.</span></span> <span data-ttu-id="c8714-146">Cette erreur est retournée si le paramètre de *type* pour le descripteur de socket passé dans le paramètre *s* n’était pas **chaussette \_ DGRAM** ou **chaussette \_ RAW**.</span><span class="sxs-lookup"><span data-stu-id="c8714-146">This error is returned if the *type* parameter for the socket descriptor passed in the *s* parameter was not **SOCK\_DGRAM** or **SOCK\_RAW**.</span></span> <br/>                          |
| <dl> <span data-ttu-id="c8714-147"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="c8714-147"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="c8714-148">Le descripteur n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="c8714-148">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="c8714-149">Notes</span><span class="sxs-lookup"><span data-stu-id="c8714-149">Remarks</span></span>

<span data-ttu-id="c8714-150">La fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) appelée avec l' \_ option de socket IPv6 PKTINFO permet à une application de déterminer si les informations de paquet doivent être retournées par la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)pour un socket IPv6.</span><span class="sxs-lookup"><span data-stu-id="c8714-150">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the IPV6\_PKTINFO socket option allows an application to determine if packet information is to be returned by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)function for an IPv6 socket.</span></span>

<span data-ttu-id="c8714-151">La fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) appelée avec l' \_ option de socket PKTINFO IPv6 permet à une application d’activer ou de désactiver le retour des informations de paquets par la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="c8714-151">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the IPV6\_PKTINFO socket option allows an application to enable or disable the return of packet information by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function.</span></span> <span data-ttu-id="c8714-152">L' \_ option IPv6 PKTINFO pour un socket est désactivée (définie sur **false**) par défaut.</span><span class="sxs-lookup"><span data-stu-id="c8714-152">The IPV6\_PKTINFO option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="c8714-153">Lorsque cette option de socket est activée sur un socket IPv6 de **type chaussette \_ DGRAM** ou **chaussette \_ RAW**, la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retourne des informations de paquets dans la structure [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) vers laquelle pointe le paramètre *lpMsg* .</span><span class="sxs-lookup"><span data-stu-id="c8714-153">When this socket option is enabled on an IPv6 socket of type **SOCK\_DGRAM** or **SOCK\_RAW**, the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function returns packet information in the [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure pointed to by the *lpMsg* parameter.</span></span> <span data-ttu-id="c8714-154">L’un des objets de données de contrôle de la structure **WSAMSG** retournée contient une structure [**in6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) utilisée pour stocker les informations d’adresse de paquet reçues.</span><span class="sxs-lookup"><span data-stu-id="c8714-154">One of the control data objects in the returned **WSAMSG** structure will contain an [**in6\_pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) structure used to store received packet address information.</span></span>

<span data-ttu-id="c8714-155">Pour les datagrammes reçus par la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) sur IPv6, le membre du **contrôle** de la structure [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) reçu contient une structure [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) qui contient une structure **WSACMSGHDR** .</span><span class="sxs-lookup"><span data-stu-id="c8714-155">For datagrams received by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function over IPv6, the **Control** member of the [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure received will contain a [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) structure that contains a **WSACMSGHDR** structure.</span></span> <span data-ttu-id="c8714-156">Le membre de **\_ niveau CMSG** de cette structure **WSACMSGHDR** contiendra **IPPROTO \_ IPv6**, le membre de **\_ type CMSG** de cette structure contiendrait **IPv6 \_ PKTINFO** et le membre de **\_ données CMSG** contiendrait une structure in6 [**\_ PKTINFO**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) utilisée pour stocker les informations d’adresse de paquet IPv6 reçues.</span><span class="sxs-lookup"><span data-stu-id="c8714-156">The **cmsg\_level** member of this **WSACMSGHDR** structure would contain **IPPROTO\_IPV6**, the **cmsg\_type** member of this structure would contain **IPV6\_PKTINFO**, and the **cmsg\_data** member would contain an [**in6\_pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) structure used to store received IPv6 packet address information.</span></span> <span data-ttu-id="c8714-157">L’adresse IPv6 de la structure **in6 \_ pktinfo** est l’adresse IPv6 à partir de laquelle le paquet a été reçu.</span><span class="sxs-lookup"><span data-stu-id="c8714-157">The IPv6 address in the **in6\_pktinfo** structure is the IPv6 address from which the packet was received.</span></span>

<span data-ttu-id="c8714-158">Pour un socket de datagramme à double pile, si une application requiert la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) pour retourner les informations de paquets dans une structure [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) pour les datagrammes reçus sur IPv4, l’option de socket [IP \_ PKTINFO](ip-pktinfo.md) doit avoir la valeur true sur le Socket.</span><span class="sxs-lookup"><span data-stu-id="c8714-158">For a dual-stack datagram socket, if an application requires the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function to return packet information in a [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure for datagrams received over IPv4, then [IP\_PKTINFO](ip-pktinfo.md) socket option must be set to true on the socket.</span></span> <span data-ttu-id="c8714-159">Si seule l' \_ option IPv6 PKTINFO a la valeur true sur le socket, des informations de paquet sont fournies pour les datagrammes reçus via IPv6, mais elles peuvent ne pas être fournies pour les datagrammes reçus sur IPv4.</span><span class="sxs-lookup"><span data-stu-id="c8714-159">If only the IPV6\_PKTINFO option is set to true on the socket, packet information will be provided for datagrams received over IPv6 but may not be provided for datagrams received over IPv4.</span></span>

<span data-ttu-id="c8714-160">Notez que le fichier d’en-tête *Ws2ipdef. h* est automatiquement inclus dans *Ws2tcpip. h* et ne doit jamais être utilisé directement.</span><span class="sxs-lookup"><span data-stu-id="c8714-160">Note that the *Ws2ipdef.h* header file is automatically included in *Ws2tcpip.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8714-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8714-161">Requirements</span></span>



| <span data-ttu-id="c8714-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8714-162">Requirement</span></span> | <span data-ttu-id="c8714-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8714-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8714-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8714-164">Minimum supported client</span></span><br/> | <span data-ttu-id="c8714-165">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8714-165">Windows XP \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="c8714-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8714-166">Minimum supported server</span></span><br/> | <span data-ttu-id="c8714-167">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8714-167">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c8714-168">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8714-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8714-169"><dt>Ws2ipdef. h (inclure Ws2tcpip. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8714-169"><dt>Ws2ipdef.h (include Ws2tcpip.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8714-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8714-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8714-171">Sockets à double pile</span><span class="sxs-lookup"><span data-stu-id="c8714-171">Dual-Stack Sockets</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="c8714-172">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="c8714-172">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="c8714-173">**in6 \_ pktinfo**</span><span class="sxs-lookup"><span data-stu-id="c8714-173">**in6\_pktinfo**</span></span>](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)
</dt> <dt>

[<span data-ttu-id="c8714-174">\_PKTINFO IP</span><span class="sxs-lookup"><span data-stu-id="c8714-174">IP\_PKTINFO</span></span>](ip-pktinfo.md)
</dt> <dt>

[<span data-ttu-id="c8714-175">**\_Options de socket IPv6 IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="c8714-175">**IPPROTO\_IPV6 Socket Options**</span></span>](ipproto-ipv6-socket-options.md)
</dt> <dt>

[<span data-ttu-id="c8714-176">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="c8714-176">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="c8714-177">**socle**</span><span class="sxs-lookup"><span data-stu-id="c8714-177">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[<span data-ttu-id="c8714-178">**WSAMSG**</span><span class="sxs-lookup"><span data-stu-id="c8714-178">**WSAMSG**</span></span>](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[<span data-ttu-id="c8714-179">**LPFN_WSARECVMSG (WSARecvMsg)**</span><span class="sxs-lookup"><span data-stu-id="c8714-179">**LPFN_WSARECVMSG (WSARecvMsg)**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
