---
description: Est conçu pour permettre à une application d’activer des paquets Keep-Alive pour une connexion de Socket.
ms.assetid: d6da7761-7a09-4c91-9737-550590a773b3
title: Option de socket SO_KEEPALIVE (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d829f957e23c48a325444de7d992397fba26d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521306"
---
# <a name="so_keepalive-socket-option"></a><span data-ttu-id="74578-103">\_Option de socket KeepAlive</span><span class="sxs-lookup"><span data-stu-id="74578-103">SO\_KEEPALIVE socket option</span></span>

<span data-ttu-id="74578-104">L’option **so \_ KeepAlive** Socket est conçue pour permettre à une application d’activer des paquets Keep-Alive pour une connexion de Socket.</span><span class="sxs-lookup"><span data-stu-id="74578-104">The **SO\_KEEPALIVE** socket option is designed to allow an application to enable keep-alive packets for a socket connection.</span></span>

<span data-ttu-id="74578-105">Pour interroger l’état de cette option de socket, appelez la fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) .</span><span class="sxs-lookup"><span data-stu-id="74578-105">To query the status of this socket option, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function.</span></span> <span data-ttu-id="74578-106">Pour définir cette option, appelez la fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="74578-106">To set this option, call the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="74578-107">Valeur d’option de socket</span><span class="sxs-lookup"><span data-stu-id="74578-107">Socket option value</span></span>

<span data-ttu-id="74578-108">La constante qui représente cette option de socket est 0x0008.</span><span class="sxs-lookup"><span data-stu-id="74578-108">The constant that represents this socket option is 0x0008.</span></span>

## <a name="syntax"></a><span data-ttu-id="74578-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74578-109">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="74578-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74578-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74578-111"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="74578-111">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74578-112">Descripteur identifiant le Socket.</span><span class="sxs-lookup"><span data-stu-id="74578-112">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="74578-113">de *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="74578-113">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74578-114">Niveau auquel l’option est définie.</span><span class="sxs-lookup"><span data-stu-id="74578-114">The level at which the option is defined.</span></span> <span data-ttu-id="74578-115">Utilisez **le \_ Socket sol** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="74578-115">Use **SOL\_SOCKET** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="74578-116">*nom_d* \[ ' $ dans\]</span><span class="sxs-lookup"><span data-stu-id="74578-116">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74578-117">Option de socket pour laquelle la valeur doit être définie.</span><span class="sxs-lookup"><span data-stu-id="74578-117">The socket option for which the value is to be set.</span></span> <span data-ttu-id="74578-118">Utilisez **donc \_ KeepAlive** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="74578-118">Use **SO\_KEEPALIVE** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="74578-119">*optval* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="74578-119">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74578-120">Pointeur vers la mémoire tampon contenant la valeur de l’option à définir.</span><span class="sxs-lookup"><span data-stu-id="74578-120">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="74578-121">Ce paramètre doit pointer vers une mémoire tampon égale ou supérieure à la taille d’une valeur **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="74578-121">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="74578-122">Cette valeur est traitée comme une valeur booléenne avec 0 utilisé pour indiquer **false** (désactivé) et une valeur différente de zéro pour indiquer la valeur **true** (activé).</span><span class="sxs-lookup"><span data-stu-id="74578-122">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="74578-123">*optlen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="74578-123">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="74578-124">Pointeur vers la taille, en octets, de la mémoire tampon *optval* .</span><span class="sxs-lookup"><span data-stu-id="74578-124">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="74578-125">Cette taille doit être supérieure ou égale à la taille d’une valeur **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="74578-125">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74578-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="74578-126">Return value</span></span>

<span data-ttu-id="74578-127">Si l’opération se termine correctement, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="74578-127">If the operation completes successfully, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) returns zero.</span></span>

<span data-ttu-id="74578-128">Si l’opération échoue, une valeur d’erreur de SOCKET \_ est renvoyée et un code d’erreur spécifique peut être récupéré en appelant [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="74578-128">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="74578-129">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="74578-129">Error code</span></span>                                                                                                                                              | <span data-ttu-id="74578-130">Signification</span><span class="sxs-lookup"><span data-stu-id="74578-130">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="74578-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="74578-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="74578-132">Un appel [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) réussi doit se produire avant l’utilisation de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="74578-132">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="74578-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="74578-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="74578-134">Le sous-système réseau a échoué.</span><span class="sxs-lookup"><span data-stu-id="74578-134">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="74578-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="74578-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="74578-136">L’un des paramètres *optval* ou *optlen* pointent vers la mémoire qui n’est pas dans une partie valide de l’espace d’adressage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="74578-136">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="74578-137">Cette erreur est également retournée si la valeur vers laquelle pointe le paramètre *optlen* est inférieure à la taille d’une valeur **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="74578-137">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="74578-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="74578-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="74578-139">Un appel de blocage de Windows Sockets 1,1 est en cours, ou le fournisseur de services traite toujours une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="74578-139">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="74578-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="74578-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="74578-141">Le paramètre de *niveau* est inconnu ou non valide.</span><span class="sxs-lookup"><span data-stu-id="74578-141">The *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="74578-142">Sur Windows Vista et versions ultérieures, cette erreur est également retournée si le socket était dans un état de transition.</span><span class="sxs-lookup"><span data-stu-id="74578-142">On Windows Vista and later, this error is also returned if the socket was in a transitional state.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="74578-143"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="74578-143"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="74578-144">L’option est inconnue ou non prise en charge par la famille de protocoles indiquée.</span><span class="sxs-lookup"><span data-stu-id="74578-144">The option is unknown or unsupported by the indicated protocol family.</span></span> <span data-ttu-id="74578-145">Cette erreur est retournée si le descripteur de socket passé dans le paramètre *s* était pour un socket datagramme.</span><span class="sxs-lookup"><span data-stu-id="74578-145">This error is returned if the socket descriptor passed in the *s* parameter was for a datagram socket.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="74578-146"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="74578-146"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="74578-147">Le descripteur n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="74578-147">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="74578-148">Notes</span><span class="sxs-lookup"><span data-stu-id="74578-148">Remarks</span></span>

<span data-ttu-id="74578-149">La fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) appelée avec l’option de socket **\_ KeepAlive** permet à une application de récupérer l’état actuel de l’option KeepAlive, bien qu’il s’agisse d’une fonctionnalité qui n’est généralement pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="74578-149">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the **SO\_KEEPALIVE** socket option allows an application to retrieve the current state of the keepalive option, although this is feature not normally used.</span></span> <span data-ttu-id="74578-150">Si une application doit activer des paquets KeepAlive sur un socket, elle appelle simplement la fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) pour activer l’option.</span><span class="sxs-lookup"><span data-stu-id="74578-150">If an application needs to enable keepalive packets on a socket, it justs calls the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to enable the option.</span></span>

<span data-ttu-id="74578-151">La fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) appelée avec l’option de socket **\_ KeepAlive** permet à une application d’activer des paquets Keep-Alive pour une connexion de Socket.</span><span class="sxs-lookup"><span data-stu-id="74578-151">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the **SO\_KEEPALIVE** socket option allows an application to enable keep-alive packets for a socket connection.</span></span> <span data-ttu-id="74578-152">L’option **so \_ KeepAlive** pour un socket est désactivée (définie sur **false**) par défaut.</span><span class="sxs-lookup"><span data-stu-id="74578-152">The **SO\_KEEPALIVE** option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="74578-153">Lorsque cette option de socket est activée, la pile TCP envoie des paquets Keep-Alive quand aucun paquet de données ou d’accusé de réception n’a été reçu pour la connexion dans un intervalle.</span><span class="sxs-lookup"><span data-stu-id="74578-153">When this socket option is enabled, the TCP stack sends keep-alive packets when no data or acknowledgement packets have been received for the connection within an interval.</span></span> <span data-ttu-id="74578-154">Pour plus d’informations sur l’option Keep-Alive, consultez la section 4.2.3.6 sur la *Configuration requise pour les hôtes Internet — couches de communication* spécifiées dans le document RFC 1122 disponible sur le [site Web](https://www.ietf.org/rfc/rfc1122.txt)de l’IETF.</span><span class="sxs-lookup"><span data-stu-id="74578-154">For more information on the keep-alive option, see section 4.2.3.6 on the *Requirements for Internet Hosts—Communication Layers* specified in RFC 1122 available at the [IETF website](https://www.ietf.org/rfc/rfc1122.txt).</span></span> <span data-ttu-id="74578-155">(Cette ressource peut uniquement être disponible en anglais.)</span><span class="sxs-lookup"><span data-stu-id="74578-155">(This resource may only be available in English.)</span></span>

<span data-ttu-id="74578-156">L’option **so \_ KeepAlive** Socket est valide uniquement pour les protocoles qui prennent en charge la notion de Keep-Alive (protocoles orientés connexion).</span><span class="sxs-lookup"><span data-stu-id="74578-156">The **SO\_KEEPALIVE** socket option is valid only for protocols that support the notion of keep-alive (connection-oriented protocols).</span></span> <span data-ttu-id="74578-157">Pour TCP, le délai d’expiration de la conservation par défaut est de 2 heures et l’intervalle de maintien de l’activité est de 1 seconde.</span><span class="sxs-lookup"><span data-stu-id="74578-157">For TCP, the default keep-alive timeout is 2 hours and the keep-alive interval is 1 second.</span></span> <span data-ttu-id="74578-158">Le nombre par défaut de sondes KeepAlive varie en fonction de la version de Windows.</span><span class="sxs-lookup"><span data-stu-id="74578-158">The default number of keep-alive probes varies based on the version of Windows.</span></span>

<span data-ttu-id="74578-159">Le code de contrôle [**\_ KeepAlive \_ Vals SIO**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) peut être utilisé pour activer ou désactiver Keep-Alive, et ajuster le délai d’expiration et l’intervalle pour une connexion unique.</span><span class="sxs-lookup"><span data-stu-id="74578-159">The [**SIO\_KEEPALIVE\_VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) control code can be used to enable or disable keep-alive, and adjust the timeout and interval, for a single connection.</span></span> <span data-ttu-id="74578-160">Si Keep-Alive est activé avec **\_ KeepAlive**, les paramètres TCP par défaut sont utilisés pour le délai d’expiration et l’intervalle Keep-Alive, sauf si ces valeurs ont été modifiées à l’aide de **SIO \_ KeepAlive \_ Vals**.</span><span class="sxs-lookup"><span data-stu-id="74578-160">If keep-alive is enabled with **SO\_KEEPALIVE**, then the default TCP settings are used for keep-alive timeout and interval unless these values have been changed using **SIO\_KEEPALIVE\_VALS**.</span></span>

<span data-ttu-id="74578-161">La valeur par défaut au niveau du système du délai d’expiration Keep-Alive est contrôlable via le paramètre de Registre [keepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) qui prend une valeur en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="74578-161">The default system-wide value of the keep-alive timeout is controllable through the [KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) registry setting which takes a value in milliseconds.</span></span> <span data-ttu-id="74578-162">La valeur par défaut à l’ensemble du système de l’intervalle Keep-Alive est contrôlable via le paramètre de Registre [keepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) qui prend une valeur en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="74578-162">The default system-wide value of the keep-alive interval is controllable through the [KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) registry setting which takes a value in milliseconds.</span></span>

<span data-ttu-id="74578-163">Sur Windows Vista et versions ultérieures, le nombre de sondes KeepAlive (retransmissions de données) est défini sur 10 et ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="74578-163">On Windows Vista and later, the number of keep-alive probes (data retransmissions) is set to 10 and cannot be changed.</span></span>

<span data-ttu-id="74578-164">Sur Windows Server 2003, Windows XP et Windows 2000, le paramètre par défaut pour le nombre de sondes KeepAlive est 5.</span><span class="sxs-lookup"><span data-stu-id="74578-164">On Windows Server 2003, Windows XP, and Windows 2000, the default setting for number of keep-alive probes is 5.</span></span> <span data-ttu-id="74578-165">Le nombre de sondes KeepAlive est contrôlable via les paramètres de Registre [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) et [PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) .</span><span class="sxs-lookup"><span data-stu-id="74578-165">The number of keep-alive probes is controllable through the [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) and [PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) registry settings.</span></span> <span data-ttu-id="74578-166">Le nombre de sondes KeepAlive est défini sur la plus grande des deux valeurs de clé de registre.</span><span class="sxs-lookup"><span data-stu-id="74578-166">The number of keep-alive probes is set to the larger of the two registry key values.</span></span> <span data-ttu-id="74578-167">Si ce nombre est 0, les sondes de conservation des connexions actives ne sont pas envoyées.</span><span class="sxs-lookup"><span data-stu-id="74578-167">If this number is 0, then keep-alive probes will not be sent.</span></span> <span data-ttu-id="74578-168">Si ce nombre est supérieur à 255, il est ajusté à 255.</span><span class="sxs-lookup"><span data-stu-id="74578-168">If this number is above 255, then it is adjusted to 255.</span></span>

<span data-ttu-id="74578-169">Sur Windows Vista et versions ultérieures, l’option de socket **\_ KeepAlive** ne peut être définie qu’à l’aide de la fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) lorsque le socket est dans un état connu et non transitoire.</span><span class="sxs-lookup"><span data-stu-id="74578-169">On Windows Vista and later, the **SO\_KEEPALIVE** socket option can only be set using the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function when the socket is in a well-known state not a transitional state.</span></span> <span data-ttu-id="74578-170">Pour TCP, l’option de socket **\_ KeepAlive de ce** type doit être définie avant que la fonction Connect ([**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)ou [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)) soit appelée, ou une fois que la demande de connexion est effectivement terminée.</span><span class="sxs-lookup"><span data-stu-id="74578-170">For TCP, the **SO\_KEEPALIVE** socket option should be set either before the connect function ([**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist), or [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)) is called, or after the connection request is actually completed.</span></span> <span data-ttu-id="74578-171">Si la fonction Connect a été appelée de façon asynchrone, cela nécessite l’attente de la fin de la connexion avant d’essayer de définir l’option **so \_ KeepAlive** Socket.</span><span class="sxs-lookup"><span data-stu-id="74578-171">If the connect function was called asynchronously, then this requires waiting for the connection completion before trying to set the **SO\_KEEPALIVE** socket option.</span></span> <span data-ttu-id="74578-172">Si une application tente de définir l’option de socket **\_ KeepAlive** si une demande de connexion est toujours en cours, la fonction **setsockopt** échoue et retourne [WSAEINVAL](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="74578-172">If an application attempts to set the **SO\_KEEPALIVE** socket option when a connection request is still in process, the **setsockopt** function will fail and return [WSAEINVAL](windows-sockets-error-codes-2.md).</span></span>

<span data-ttu-id="74578-173">Sur Windows Server 2003, Windows XP et Windows 2000, l’option de socket **\_ KeepAlive** peut être définie à l’aide de la fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) lorsque le socket est un état transitoire (une demande de connexion est toujours en cours), ainsi qu’un état connu.</span><span class="sxs-lookup"><span data-stu-id="74578-173">On Windows Server 2003, Windows XP, and Windows 2000, the **SO\_KEEPALIVE** socket option can be set using the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function when the socket is a transitional state (a connection request is still in progress) as well as a well-known state.</span></span>

<span data-ttu-id="74578-174">Notez que le fichier d’en-tête *Ws2def. h* est automatiquement inclus dans *Winsock2. h* et ne doit jamais être utilisé directement.</span><span class="sxs-lookup"><span data-stu-id="74578-174">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="74578-175">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74578-175">Requirements</span></span>



| <span data-ttu-id="74578-176">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74578-176">Requirement</span></span> | <span data-ttu-id="74578-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="74578-177">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74578-178">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74578-178">Minimum supported client</span></span><br/> | <span data-ttu-id="74578-179">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74578-179">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="74578-180">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74578-180">Minimum supported server</span></span><br/> | <span data-ttu-id="74578-181">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74578-181">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="74578-182">En-tête</span><span class="sxs-lookup"><span data-stu-id="74578-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="74578-183"><dt>Ws2def. h (inclure Winsock2. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74578-183"><dt>Ws2def.h (include Winsock2.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74578-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74578-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74578-185">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="74578-185">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="74578-186">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="74578-186">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

<span data-ttu-id="74578-187">[KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="74578-187">[KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="74578-188">[KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="74578-188">[KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="74578-189">[PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="74578-189">[PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="74578-190">**socle**</span><span class="sxs-lookup"><span data-stu-id="74578-190">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

<span data-ttu-id="74578-191">[**SIO \_ KeepAlive \_ Vals**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="74578-191">[**SIO\_KEEPALIVE\_VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="74578-192">[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="74578-192">[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="74578-193">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="74578-193">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 
