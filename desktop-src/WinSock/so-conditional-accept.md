---
description: Est conçu pour permettre à une application de décider s’il faut ou non accepter une connexion entrante sur un socket d’écoute.
ms.assetid: 964683eb-5dfc-4441-abb7-315be8b89a19
title: Option de socket SO_CONDITIONAL_ACCEPT (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badfdd1f8aac49ae05fa6b77dadb2561ba5ea02f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529344"
---
# <a name="so_conditional_accept-socket-option"></a><span data-ttu-id="94ce9-103">\_Option de \_ Socket d’acceptation conditionnelle</span><span class="sxs-lookup"><span data-stu-id="94ce9-103">SO\_CONDITIONAL\_ACCEPT socket option</span></span>

<span data-ttu-id="94ce9-104">L’option de socket d' **\_ \_ acceptation conditionnelle so** est conçue pour permettre à une application de décider s’il faut ou non accepter une connexion entrante sur un socket d’écoute.</span><span class="sxs-lookup"><span data-stu-id="94ce9-104">The **SO\_CONDITIONAL\_ACCEPT** socket option is designed to allow an application to decide whether or not to accept an incoming connection on a listening socket.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="94ce9-105">Valeur d’option de socket</span><span class="sxs-lookup"><span data-stu-id="94ce9-105">Socket option value</span></span>

<span data-ttu-id="94ce9-106">La constante qui représente cette option de socket est 0x3002.</span><span class="sxs-lookup"><span data-stu-id="94ce9-106">The constant that represents this socket option is 0x3002.</span></span>

## <a name="syntax"></a><span data-ttu-id="94ce9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94ce9-107">Syntax</span></span>


```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_CONDITIONAL_ACCEPT, // optname
  (char *) optval,         // input buffer,
  (int) optlen,       // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="94ce9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="94ce9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94ce9-109"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="94ce9-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94ce9-110">Descripteur identifiant le Socket.</span><span class="sxs-lookup"><span data-stu-id="94ce9-110">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="94ce9-111">de *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="94ce9-111">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94ce9-112">Niveau auquel l’option est définie.</span><span class="sxs-lookup"><span data-stu-id="94ce9-112">The level at which the option is defined.</span></span> <span data-ttu-id="94ce9-113">Utilisez **le \_ Socket sol** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="94ce9-113">Use **SOL\_SOCKET** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="94ce9-114">*nom_d* \[ ' $ dans\]</span><span class="sxs-lookup"><span data-stu-id="94ce9-114">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94ce9-115">Option de socket pour laquelle la valeur doit être définie.</span><span class="sxs-lookup"><span data-stu-id="94ce9-115">The socket option for which the value is to be set.</span></span> <span data-ttu-id="94ce9-116">Utilisez **l' \_ \_ acceptation conditionnelle** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="94ce9-116">Use **SO\_CONDITIONAL\_ACCEPT** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="94ce9-117">*optval* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="94ce9-117">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94ce9-118">Pointeur vers la mémoire tampon contenant la valeur de l’option à définir.</span><span class="sxs-lookup"><span data-stu-id="94ce9-118">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="94ce9-119">Ce paramètre doit pointer vers une mémoire tampon égale ou supérieure à la taille d’une valeur **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="94ce9-119">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="94ce9-120">Cette valeur est traitée comme une valeur booléenne avec 0 utilisé pour indiquer **false** (désactivé) et une valeur différente de zéro pour indiquer la valeur **true** (activé).</span><span class="sxs-lookup"><span data-stu-id="94ce9-120">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="94ce9-121">*optlen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="94ce9-121">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="94ce9-122">Pointeur vers la taille, en octets, de la mémoire tampon *optval* .</span><span class="sxs-lookup"><span data-stu-id="94ce9-122">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="94ce9-123">Cette taille doit être supérieure ou égale à la taille d’une valeur **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="94ce9-123">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94ce9-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="94ce9-124">Return value</span></span>

<span data-ttu-id="94ce9-125">Si l’opération se termine correctement, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="94ce9-125">If the operation completes successfully, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) returns zero.</span></span>

<span data-ttu-id="94ce9-126">Si l’opération échoue, une valeur d’erreur de SOCKET \_ est renvoyée et un code d’erreur spécifique peut être récupéré en appelant [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="94ce9-126">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="94ce9-127">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="94ce9-127">Error code</span></span>                                                                                                                                              | <span data-ttu-id="94ce9-128">Signification</span><span class="sxs-lookup"><span data-stu-id="94ce9-128">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="94ce9-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="94ce9-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="94ce9-130">Un appel [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) réussi doit se produire avant l’utilisation de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="94ce9-130">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="94ce9-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="94ce9-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="94ce9-132">Le sous-système réseau a échoué.</span><span class="sxs-lookup"><span data-stu-id="94ce9-132">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="94ce9-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="94ce9-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="94ce9-134">L’un des paramètres *optval* ou *optlen* pointent vers la mémoire qui n’est pas dans une partie valide de l’espace d’adressage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="94ce9-134">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="94ce9-135">Cette erreur est également retournée si la valeur vers laquelle pointe le paramètre *optlen* est inférieure à la taille d’une valeur **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="94ce9-135">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="94ce9-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="94ce9-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="94ce9-137">Un appel de blocage de Windows Sockets 1,1 est en cours, ou le fournisseur de services traite toujours une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="94ce9-137">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="94ce9-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="94ce9-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="94ce9-139">Le paramètre de *niveau* est inconnu ou non valide.</span><span class="sxs-lookup"><span data-stu-id="94ce9-139">The *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="94ce9-140">Cette erreur est également retournée si le socket était déjà à l’état d’écoute.</span><span class="sxs-lookup"><span data-stu-id="94ce9-140">This error is also returned if the socket was already in a listening state.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="94ce9-141"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="94ce9-141"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="94ce9-142">L’option est inconnue ou non prise en charge par la famille de protocoles indiquée.</span><span class="sxs-lookup"><span data-stu-id="94ce9-142">The option is unknown or unsupported by the indicated protocol family.</span></span><br/>                                                                                                                                                                          |
| <dl> <span data-ttu-id="94ce9-143"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="94ce9-143"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="94ce9-144">Le descripteur n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="94ce9-144">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="94ce9-145">Notes</span><span class="sxs-lookup"><span data-stu-id="94ce9-145">Remarks</span></span>

<span data-ttu-id="94ce9-146">La fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) appelée avec l’option de socket d' **\_ \_ acceptation conditionnelle** permet à une application de décider s’il faut ou non accepter une connexion entrante sur un socket d’écoute.</span><span class="sxs-lookup"><span data-stu-id="94ce9-146">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the **SO\_CONDITIONAL\_ACCEPT** socket option allows an application to decide whether or not to accept an incoming connection on a listening socket.</span></span> <span data-ttu-id="94ce9-147">L’option d’acceptation conditionnelle pour un socket est désactivée (définie sur **false**) par défaut.</span><span class="sxs-lookup"><span data-stu-id="94ce9-147">The conditional accept option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="94ce9-148">Lorsque cette option de socket est activée, la pile TCP n’accepte pas automatiquement les connexions.</span><span class="sxs-lookup"><span data-stu-id="94ce9-148">When this socket option is enabled, the TCP stack does not automatically accept connections.</span></span> <span data-ttu-id="94ce9-149">Elle attend que l’application indique qu’elle accepte la connexion via le rappel d’acceptation conditionnel inscrit avec la fonction [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) .</span><span class="sxs-lookup"><span data-stu-id="94ce9-149">It waits for the application to indicate that it accepts the connection via the conditional accept callback registered with [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function.</span></span> <span data-ttu-id="94ce9-150">Une fois qu’une demande de connexion est reçue, Winsock appelle le rappel d’acceptation conditionnel inscrit par l’application.</span><span class="sxs-lookup"><span data-stu-id="94ce9-150">Once a connection request is received, Winsock invokes the conditional accept callback registered by the application.</span></span> <span data-ttu-id="94ce9-151">Uniquement lorsque le rappel d’acceptation conditionnelle retourne **CF \_ Accept** , Winsock notifie le transport pour accepter entièrement la connexion.</span><span class="sxs-lookup"><span data-stu-id="94ce9-151">Only when the conditional accept callback returns **CF\_ACCEPT** will Winsock notify the transport to fully accept the connection.</span></span>

<span data-ttu-id="94ce9-152">Lorsque l’option de socket d' **\_ \_ acceptation conditionnelle so** est définie sur Enabled (définie à **true**), cela a plusieurs effets secondaires sur le Socket :</span><span class="sxs-lookup"><span data-stu-id="94ce9-152">When the **SO\_CONDITIONAL\_ACCEPT** socket option is set to enabled (set to **TRUE**), this has several side effects on the socket:</span></span>

-   <span data-ttu-id="94ce9-153">Cela désactive les défenses de protection contre les attaques SYN intégrées de la pile TCP, puisque l’application est maintenant propriétaire de l’acceptation des connexions.</span><span class="sxs-lookup"><span data-stu-id="94ce9-153">This disables the TCP stack's built-in SYN attack protection defenses, since the application is now taking ownership of accepting connections.</span></span>
-   <span data-ttu-id="94ce9-154">Cela désactive efficacement le backlog d’écoute, car les connexions ne sont pas acceptées pour le compte d’un socket d’écoute.</span><span class="sxs-lookup"><span data-stu-id="94ce9-154">This effectively disables the listen backlog since connections aren't accepted on behalf of a listening socket.</span></span> <span data-ttu-id="94ce9-155">Une connexion n’est jamais entièrement acceptée tant que l’application n’accepte pas complètement l’utilisation du mécanisme d' **\_ acceptation CF** .</span><span class="sxs-lookup"><span data-stu-id="94ce9-155">A connection is never fully accepted until the application fully accepts using the **CF\_ACCEPT** mechanism.</span></span>
-   <span data-ttu-id="94ce9-156">Cela signifie également que l’application doit toujours être dans un État pour gérer facilement les rappels d’acceptation afin d’accepter la connexion.</span><span class="sxs-lookup"><span data-stu-id="94ce9-156">This also means the application take care to always be in a state to readily handle the accept callbacks to accept the connection.</span></span> <span data-ttu-id="94ce9-157">Si l’application est occupée par un autre traitement, le côté client peut expirer avant que l’application n’accepte réellement la connexion.</span><span class="sxs-lookup"><span data-stu-id="94ce9-157">If the application is busy doing other processing, then the client side may time out before the application actually accepts the connection.</span></span> <span data-ttu-id="94ce9-158">Cela provoque une expérience client médiocre.</span><span class="sxs-lookup"><span data-stu-id="94ce9-158">This leads to a poor client experience.</span></span>

<span data-ttu-id="94ce9-159">En règle générale, la raison principale pour laquelle les applications utilisent l’acceptation conditionnelle est d’inspecter l’adresse IP ou le port source utilisé par le client qui se connecte, puis de décider d’accepter ou de refuser la connexion.</span><span class="sxs-lookup"><span data-stu-id="94ce9-159">Generally, the main reason applications use conditional accept is to inspect the source IP address or port used by the connecting client and then decide to accept or reject the connection.</span></span> <span data-ttu-id="94ce9-160">Toutefois, les applications sont susceptibles d’être plus performantes si l' \_ option accepter la condition conditionnelle \_ n’est pas activée et que l’application autorise la pile TCP et le backlog d’écoute à fonctionner comme prévu.</span><span class="sxs-lookup"><span data-stu-id="94ce9-160">However, applications are likely to perform better if the SO\_CONDITIONAL\_ACCEPT option is not enabled and the application allows the TCP stack and the listen backlog to work as expected.</span></span> <span data-ttu-id="94ce9-161">Ensuite, lorsque l’application gère la connexion acceptée, si elle provient d’une adresse ou d’un port source IP incorrect, l’application peut simplement fermer le Socket.</span><span class="sxs-lookup"><span data-stu-id="94ce9-161">Then when the application handles the accepted connection, if it is from a improper IP source address or port, the application can just close the socket.</span></span> <span data-ttu-id="94ce9-162">L’inconvénient en matière de sécurité de ce comportement est que, à présent, le client a la confirmation que l’application est à l’écoute sur une adresse IP et un port, car elle a forcé de fermer la connexion précédemment acceptée.</span><span class="sxs-lookup"><span data-stu-id="94ce9-162">The security drawback to this behavior is that now the client has confirmation that the application is listening on an IP address and port since it forcefully closed the previously accepted connection.</span></span> <span data-ttu-id="94ce9-163">Toutefois, les inconvénients de l’activation de l' **\_ \_ acceptation conditionnelle** l’emportent généralement sur cette limitation.</span><span class="sxs-lookup"><span data-stu-id="94ce9-163">However, the drawbacks to enabling **SO\_CONDITIONAL\_ACCEPT** generally outweigh this limitation.</span></span>

<span data-ttu-id="94ce9-164">La fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) appelée avec l’option de socket d' **\_ \_ acceptation conditionnelle** permet à une application de récupérer l’état actuel de l’option d’acceptation conditionnelle, bien qu’il s’agisse d’une fonctionnalité qui n’est généralement pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="94ce9-164">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the **SO\_CONDITIONAL\_ACCEPT** socket option allows an application to retrieve the current state of the conditional accept option, although this is feature not normally used.</span></span> <span data-ttu-id="94ce9-165">Si une application doit activer l’acceptation conditionnelle sur un socket, elle appelle la fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) pour activer l’option.</span><span class="sxs-lookup"><span data-stu-id="94ce9-165">If an application needs to enable conditional accept on a socket, it justs calls the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to enable the option.</span></span>

<span data-ttu-id="94ce9-166">Notez que le fichier d’en-tête *Ws2def. h* est automatiquement inclus dans *Winsock2. h* et ne doit jamais être utilisé directement.</span><span class="sxs-lookup"><span data-stu-id="94ce9-166">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="94ce9-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94ce9-167">Requirements</span></span>



| <span data-ttu-id="94ce9-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94ce9-168">Requirement</span></span> | <span data-ttu-id="94ce9-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="94ce9-169">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94ce9-170">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94ce9-170">Minimum supported client</span></span><br/> | <span data-ttu-id="94ce9-171">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94ce9-171">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="94ce9-172">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94ce9-172">Minimum supported server</span></span><br/> | <span data-ttu-id="94ce9-173">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94ce9-173">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="94ce9-174">En-tête</span><span class="sxs-lookup"><span data-stu-id="94ce9-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="94ce9-175"><dt>Ws2def. h (inclure Winsock2. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94ce9-175"><dt>Ws2def.h (include Winsock2.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94ce9-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94ce9-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94ce9-177">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="94ce9-177">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="94ce9-178">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="94ce9-178">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="94ce9-179">**WSAAccept**</span><span class="sxs-lookup"><span data-stu-id="94ce9-179">**WSAAccept**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)
</dt> </dl>

 

 




