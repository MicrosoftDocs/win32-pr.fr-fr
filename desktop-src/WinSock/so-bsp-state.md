---
description: Retourne l’adresse locale, le port local, l’adresse distante, le port distant, le type de socket et le protocole utilisés par un Socket.
ms.assetid: 2628f47e-3e73-4e02-91b8-ba4cb0800864
title: Option de socket SO_BSP_STATE (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10e391d70dd67190e1aec803036d019261c9000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755060"
---
# <a name="so_bsp_state-socket-option"></a><span data-ttu-id="ef26a-103">\_Option de \_ Socket d’État BSP</span><span class="sxs-lookup"><span data-stu-id="ef26a-103">SO\_BSP\_STATE socket option</span></span>

<span data-ttu-id="ef26a-104">L’option de socket de l' **\_ \_ État BSP** retourne l’adresse locale, le port local, l’adresse distante, le port distant, le type de socket et le protocole utilisés par un Socket.</span><span class="sxs-lookup"><span data-stu-id="ef26a-104">The **SO\_BSP\_STATE** socket option returns the local address, local port, remote address, remote port, socket type, and protocol used by a socket.</span></span>

<span data-ttu-id="ef26a-105">Pour effectuer cette opération, appelez la fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="ef26a-105">To perform this operation, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="ef26a-106">Valeur d’option de socket</span><span class="sxs-lookup"><span data-stu-id="ef26a-106">Socket option value</span></span>

<span data-ttu-id="ef26a-107">La constante qui représente cette option de socket est 0x1009.</span><span class="sxs-lookup"><span data-stu-id="ef26a-107">The constant that represents this socket option is 0x1009.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef26a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef26a-108">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_BSP_STATE, // optname
  (char *) optval,         // output buffer,
  (int) *optlen,       // size of output buffer
);
```



## <a name="parameters"></a><span data-ttu-id="ef26a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef26a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef26a-110"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef26a-110">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef26a-111">Descripteur identifiant le Socket.</span><span class="sxs-lookup"><span data-stu-id="ef26a-111">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="ef26a-112">de *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef26a-112">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef26a-113">Niveau auquel l’option est définie.</span><span class="sxs-lookup"><span data-stu-id="ef26a-113">The level at which the option is defined.</span></span> <span data-ttu-id="ef26a-114">Utilisez **le \_ Socket sol** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="ef26a-114">Use **SOL\_SOCKET** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="ef26a-115">*nom_d* \[ ' $ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef26a-115">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef26a-116">Option de socket pour laquelle la valeur doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="ef26a-116">The socket option for which the value is to be retrieved.</span></span> <span data-ttu-id="ef26a-117">Utilisez **l' \_ \_ État BSP** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="ef26a-117">Use **SO\_BSP\_STATE** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="ef26a-118">*optval* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ef26a-118">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef26a-119">Pointeur vers la mémoire tampon dans laquelle la valeur de l’option demandée doit être retournée.</span><span class="sxs-lookup"><span data-stu-id="ef26a-119">A pointer to the buffer in which the value for the requested option is to be returned.</span></span> <span data-ttu-id="ef26a-120">Ce paramètre doit pointer vers une mémoire tampon égale ou supérieure à la taille d’une structure [**CSADDR \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .</span><span class="sxs-lookup"><span data-stu-id="ef26a-120">This parameter should point to buffer equal to or larger than the size of a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ef26a-121">*optlen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ef26a-121">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef26a-122">Pointeur vers la taille, en octets, de la mémoire tampon *optval* .</span><span class="sxs-lookup"><span data-stu-id="ef26a-122">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="ef26a-123">Cette taille doit être supérieure ou égale à la taille d’une structure [**CSADDR \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .</span><span class="sxs-lookup"><span data-stu-id="ef26a-123">This size must be equal to or larger than the size of a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef26a-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef26a-124">Return value</span></span>

<span data-ttu-id="ef26a-125">Si l’opération se termine avec succès, [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="ef26a-125">If the operation completes successfully, [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) returns zero.</span></span>

<span data-ttu-id="ef26a-126">Si l’opération échoue, une valeur d’erreur de SOCKET \_ est renvoyée et un code d’erreur spécifique peut être récupéré en appelant [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="ef26a-126">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="ef26a-127">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="ef26a-127">Error code</span></span>                                                                                                                                              | <span data-ttu-id="ef26a-128">Signification</span><span class="sxs-lookup"><span data-stu-id="ef26a-128">Meaning</span></span>                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef26a-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="ef26a-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="ef26a-130">Un appel [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) réussi doit se produire avant l’utilisation de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="ef26a-130">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="ef26a-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="ef26a-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="ef26a-132">Le sous-système réseau a échoué.</span><span class="sxs-lookup"><span data-stu-id="ef26a-132">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="ef26a-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="ef26a-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="ef26a-134">L’un des paramètres *optval* ou *optlen* pointent vers la mémoire qui n’est pas dans une partie valide de l’espace d’adressage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ef26a-134">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="ef26a-135">Cette erreur est également retournée si la valeur vers laquelle pointe le paramètre *optlen* est inférieure à la taille d’une structure [**CSADDR \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .</span><span class="sxs-lookup"><span data-stu-id="ef26a-135">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span><br/> |
| <dl> <span data-ttu-id="ef26a-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="ef26a-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="ef26a-137">Un appel de blocage de Windows Sockets 1,1 est en cours, ou le fournisseur de services traite toujours une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="ef26a-137">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                                                            |
| <dl> <span data-ttu-id="ef26a-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="ef26a-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="ef26a-139">Le paramètre de *niveau* est inconnu ou non valide.</span><span class="sxs-lookup"><span data-stu-id="ef26a-139">The *level* parameter is unknown or invalid.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="ef26a-140"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="ef26a-140"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="ef26a-141">L’option est inconnue ou non prise en charge par la famille de protocoles indiquée.</span><span class="sxs-lookup"><span data-stu-id="ef26a-141">The option is unknown or unsupported by the indicated protocol family.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="ef26a-142"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="ef26a-142"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="ef26a-143">Le descripteur n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="ef26a-143">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="ef26a-144">Notes</span><span class="sxs-lookup"><span data-stu-id="ef26a-144">Remarks</span></span>

<span data-ttu-id="ef26a-145">La fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) appelée avec l’option de socket d' **\_ \_ État BSP** récupère l’adresse locale, le port local, l’adresse distante, le port distant, le type de socket et le protocole utilisés par un Socket.</span><span class="sxs-lookup"><span data-stu-id="ef26a-145">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the **SO\_BSP\_STATE** socket option retrieves the local address, local port, remote address, remote port, socket type, and protocol used by a socket.</span></span> <span data-ttu-id="ef26a-146">L’option de socket d' **\_ \_ État BSP so** fonctionne avec les sockets IPv6 ou IPv4 (familles d’adresses **AF \_ inet6** et **AF \_ inet** ).</span><span class="sxs-lookup"><span data-stu-id="ef26a-146">The **SO\_BSP\_STATE** socket option works with IPv6 or IPv4 sockets (the **AF\_INET6** and **AF\_INET** address families).</span></span>

<span data-ttu-id="ef26a-147">Si la fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) réussit, les informations sont retournées dans une structure [**CSADDR \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) dans la mémoire tampon vers laquelle pointe le paramètre *optval* .</span><span class="sxs-lookup"><span data-stu-id="ef26a-147">If the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function is successful, the information is returned in a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure in the buffer pointed to by the *optval* parameter.</span></span> <span data-ttu-id="ef26a-148">L’entier pointé par *optlen* doit contenir initialement la taille de cette mémoire tampon. lors du retour, elle est définie sur la longueur, en octets, de la valeur retournée dans le paramètre *optval* .</span><span class="sxs-lookup"><span data-stu-id="ef26a-148">The integer pointed to by *optlen* should originally contain the size of this buffer; on return, it will be set to the length, in bytes, of the value returned in the *optval* parameter.</span></span>

<span data-ttu-id="ef26a-149">Les membres **iSocketType** et **iProtocol** de la structure [**d' \_ informations CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) retournée sont renseignés pour le descripteur de socket dans le paramètre *s* .</span><span class="sxs-lookup"><span data-stu-id="ef26a-149">The **iSocketType** and **iProtocol** members in the returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure are filled in for the socket descriptor in the *s* parameter.</span></span>

<span data-ttu-id="ef26a-150">Si le socket est dans un état connecté ou lié, le membre **LocalAddr** de la structure [**CSADDR \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) retournée est défini sur une structure [sockaddr](sockaddr-2.md) représentant l’adresse et le port locaux.</span><span class="sxs-lookup"><span data-stu-id="ef26a-150">If the socket is in a connected or bound state, then the **LocalAddr** member of the returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure will be set to a [SOCKADDR](sockaddr-2.md) structure representing the local address and port.</span></span> <span data-ttu-id="ef26a-151">Si le socket est dans un état connecté, le membre **RemoteAddr** de la structure **CSADDR \_ info** retournée est défini sur une structure sockaddr représentant l’adresse et le port distants.</span><span class="sxs-lookup"><span data-stu-id="ef26a-151">If the socket is in a connected state, then the **RemoteAddr** member of the returned **CSADDR\_INFO** structure will be set to a SOCKADDR structure representing the remote address and port.</span></span>

<span data-ttu-id="ef26a-152">Si le socket n’est pas dans un état connecté ou lié, le membre **LocalAddr** de la structure [**CSADDR \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) retournée est retourné avec un pointeur **null** dans le membre **lpSockaddr** et le membre **iSockaddrLength** défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="ef26a-152">If the socket is not in a connected or bound state, then the **LocalAddr** member of the returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure is returned with a **NULL** pointer in the **lpSockaddr** member and the **iSockaddrLength** member set to zero.</span></span> <span data-ttu-id="ef26a-153">Si le socket n’est pas dans un État lié, le membre **RemoteAddr** de la structure **CSADDR \_ info** retournée est retourné avec un pointeur **null** dans le membre **lpSockaddr** et le membre **iSockaddrLength** défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="ef26a-153">If the socket is not in a bound state, then the **RemoteAddr** member of the returned **CSADDR\_INFO** structure is returned with a **NULL** pointer in the **lpSockaddr** member and the **iSockaddrLength** member set to zero.</span></span>

<span data-ttu-id="ef26a-154">Si la fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) échoue, les *paramètres optval* et *optlen* restent inchangés et le paramètre *optval* ne pointe pas vers une structure [**\_ info CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) retournée.</span><span class="sxs-lookup"><span data-stu-id="ef26a-154">If the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function fails, the *optval* and *optlen* parameters are left unchanged and the *optval* parameter does not point to a returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span>

<span data-ttu-id="ef26a-155">Notez que le fichier d’en-tête *Ws2def. h* est automatiquement inclus dans *Winsock2. h* et ne doit jamais être utilisé directement.</span><span class="sxs-lookup"><span data-stu-id="ef26a-155">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef26a-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef26a-156">Requirements</span></span>



| <span data-ttu-id="ef26a-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef26a-157">Requirement</span></span> | <span data-ttu-id="ef26a-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef26a-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef26a-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef26a-159">Minimum supported client</span></span><br/> | <span data-ttu-id="ef26a-160">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef26a-160">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ef26a-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef26a-161">Minimum supported server</span></span><br/> | <span data-ttu-id="ef26a-162">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef26a-162">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ef26a-163">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef26a-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef26a-164"><dt>Ws2def. h (inclure Winsock2. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef26a-164"><dt>Ws2def.h (include Winsock2.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef26a-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef26a-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef26a-166">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="ef26a-166">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="ef26a-167">**\_informations CSADDR**</span><span class="sxs-lookup"><span data-stu-id="ef26a-167">**CSADDR\_INFO**</span></span>](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[<span data-ttu-id="ef26a-168">SOCKADDR</span><span class="sxs-lookup"><span data-stu-id="ef26a-168">SOCKADDR</span></span>](sockaddr-2.md)
</dt> </dl>

 

 
