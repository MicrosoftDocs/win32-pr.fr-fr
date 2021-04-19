---
description: Code de contrôle obtient une liste d’adresses de transport locales de la famille de protocoles du socket à laquelle l’application peut se lier.
ms.assetid: 6b23a019-812c-4623-941b-87928acabbd2
title: Code de contrôle SIO_ADDRESS_LIST_QUERY
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 7a728293afa51ceb58d61141e7184077478b787c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523331"
---
# <a name="sio_address_list_query-control-code"></a><span data-ttu-id="7f9b0-103">Code de contrôle SIO_ADDRESS_LIST_QUERY</span><span class="sxs-lookup"><span data-stu-id="7f9b0-103">SIO_ADDRESS_LIST_QUERY Control Code</span></span>

## <a name="description"></a><span data-ttu-id="7f9b0-104">Description</span><span class="sxs-lookup"><span data-stu-id="7f9b0-104">Description</span></span>

<span data-ttu-id="7f9b0-105">Le code de contrôle de requête de la **\_ liste d’adresses \_ \_ SIO** obtient une liste des adresses de transport locales de la famille de protocoles du socket à laquelle l’application peut se lier.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-105">The **SIO\_ADDRESS\_LIST\_QUERY** control code obtains a list of local transport addresses of the socket's protocol family to which the application can bind.</span></span>
<span data-ttu-id="7f9b0-106">La liste des adresses varie en fonction de la famille d’adresses et certaines adresses sont exclues de la liste.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-106">The list of addresses varies based on address family and some addresses are excluded from the list.</span></span>

<span data-ttu-id="7f9b0-107">Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-107">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="7f9b0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f9b0-108">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="7f9b0-109">s</span><span class="sxs-lookup"><span data-stu-id="7f9b0-109">s</span></span>

<span data-ttu-id="7f9b0-110">Descripteur identifiant un Socket.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-110">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="7f9b0-111">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="7f9b0-111">dwIoControlCode</span></span>

<span data-ttu-id="7f9b0-112">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-112">The control code for the operation.</span></span>
<span data-ttu-id="7f9b0-113">Utilisez **la \_ \_ \_ requête de liste d’adresses SIO** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-113">Use **SIO\_ADDRESS\_LIST\_QUERY** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="7f9b0-114">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="7f9b0-114">lpvInBuffer</span></span>

<span data-ttu-id="7f9b0-115">Pointeur vers la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-115">A pointer to the input buffer.</span></span>
<span data-ttu-id="7f9b0-116">Ce paramètre n’est pas utilisé pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-116">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="7f9b0-117">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="7f9b0-117">cbInBuffer</span></span>

<span data-ttu-id="7f9b0-118">Taille, en octets, de la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-118">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="7f9b0-119">Ce paramètre n’est pas utilisé pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-119">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="7f9b0-120">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="7f9b0-120">lpvOutBuffer</span></span>

<span data-ttu-id="7f9b0-121">Pointeur vers la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-121">A pointer to the output buffer.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="7f9b0-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="7f9b0-122">cbOutBuffer</span></span>

<span data-ttu-id="7f9b0-123">Taille, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-123">The size, in bytes, of the output buffer.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="7f9b0-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="7f9b0-124">lpcbBytesReturned</span></span>

<span data-ttu-id="7f9b0-125">Pointeur vers une variable qui reçoit la taille, en octets, des données stockées dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="7f9b0-126">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="7f9b0-126">lpvOverlapped</span></span>

<span data-ttu-id="7f9b0-127">Pointeur vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="7f9b0-127">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="7f9b0-128">Si le socket *s* a été créé sans l’attribut Overlapped, le paramètre *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-128">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="7f9b0-129">Si *s* a été ouvert avec l’attribut Overlapped et que le paramètre *lpOverlapped* n’a pas la **valeur null**, l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="7f9b0-129">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="7f9b0-130">Dans ce cas, le paramètre *lpOverlapped* doit pointer vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-130">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="7f9b0-131">Pour les opérations avec chevauchement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne immédiatement, et la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-131">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="7f9b0-132">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-132">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="7f9b0-133">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="7f9b0-133">lpCompletionRoutine</span></span>

<span data-ttu-id="7f9b0-134">Type : \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="7f9b0-134">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="7f9b0-135">Pointeur vers la routine de saisie semi-automatique appelée lorsque l’opération est terminée (ignoré pour les sockets non superposés).</span><span class="sxs-lookup"><span data-stu-id="7f9b0-135">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="7f9b0-136">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="7f9b0-136">lpThreadId</span></span>

<span data-ttu-id="7f9b0-137">Pointeur vers une structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) qui doit être utilisée par le fournisseur dans un appel ultérieur à [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="7f9b0-137">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="7f9b0-138">Le fournisseur doit stocker la structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) référencée (pas le pointeur vers le même) jusqu’à ce que la fonction [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) soit retournée.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-138">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="7f9b0-139">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="7f9b0-139">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="7f9b0-140">lpErrno</span><span class="sxs-lookup"><span data-stu-id="7f9b0-140">lpErrno</span></span>

<span data-ttu-id="7f9b0-141">Pointeur vers le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-141">A pointer to the error code.</span></span>

<span data-ttu-id="7f9b0-142">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="7f9b0-142">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="7f9b0-143">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7f9b0-143">Return value</span></span>

<span data-ttu-id="7f9b0-144">Si l’opération se termine correctement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-144">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="7f9b0-145">Si l’opération échoue ou est en attente, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne une **\_ erreur de socket**.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-145">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="7f9b0-146">Pour afficher les informations d’erreur étendues, appelez [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="7f9b0-146">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="7f9b0-147">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="7f9b0-147">Error code</span></span> | <span data-ttu-id="7f9b0-148">Signification</span><span class="sxs-lookup"><span data-stu-id="7f9b0-148">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="7f9b0-149">**\_e/s WSA \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-149">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="7f9b0-150">Une opération avec chevauchement a été correctement initiée et l’achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-150">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="7f9b0-151">**\_opération WSA \_ abandonnée**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-151">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="7f9b0-152">Une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO \_ flush** ioctl.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-152">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="7f9b0-153">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-153">**WSAEFAULT**</span></span> | <span data-ttu-id="7f9b0-154">Le paramètre *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-154">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="7f9b0-155">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-155">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="7f9b0-156">La fonction est appelée lorsqu’un rappel est en cours.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-156">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="7f9b0-157">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-157">**WSAEINTR**</span></span> | <span data-ttu-id="7f9b0-158">Une opération de blocage a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-158">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="7f9b0-159">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-159">**WSAEINVAL**</span></span> | <span data-ttu-id="7f9b0-160">Le paramètre *dwIoControlCode* n’est pas une commande valide, ou un paramètre d’entrée spécifié n’est pas acceptable, ou la commande n’est pas applicable au type de socket spécifié.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-160">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="7f9b0-161">Cette erreur est retournée si le paramètre *cbInBuffer* n’a pas la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-161">This error is returned if the *cbInBuffer* parameter is not set to **NULL**.</span></span> |
| <span data-ttu-id="7f9b0-162">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-162">**WSAENETDOWN**</span></span> | <span data-ttu-id="7f9b0-163">Le sous-système réseau a échoué.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-163">The network subsystem has failed.</span></span> |
| <span data-ttu-id="7f9b0-164">**WSAENOBUFS**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-164">**WSAENOBUFS**</span></span> | <span data-ttu-id="7f9b0-165">Aucun espace de mémoire tampon n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-165">No buffer space available.</span></span> |
| <span data-ttu-id="7f9b0-166">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-166">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="7f9b0-167">L’option de socket n’est pas prise en charge sur le protocole spécifié.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-167">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="7f9b0-168">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-168">**WSAENOTSOCK**</span></span> | <span data-ttu-id="7f9b0-169">Le descripteur *s* n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-169">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="7f9b0-170">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-170">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="7f9b0-171">La commande IOCTL spécifiée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-171">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="7f9b0-172">Cette erreur est retournée si l’IOCTL de la **\_ requête de \_ liste \_ d’adresses SIO** n’est pas prise en charge par le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-172">This error is returned if the **SIO\_ADDRESS\_LIST\_QUERY** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="7f9b0-173">Notes</span><span class="sxs-lookup"><span data-stu-id="7f9b0-173">Remarks</span></span>

<span data-ttu-id="7f9b0-174">La **requête IOCTL de \_ \_ liste \_ d’adresses SIO** est prise en charge sur Windows 2000 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-174">The **SIO\_ADDRESS\_LIST\_QUERY** IOCTL is supported on Windows 2000 and later versions of the operating system.</span></span>

<span data-ttu-id="7f9b0-175">Le code de contrôle de requête de la **\_ liste d’adresses \_ \_ SIO** obtient une liste des adresses de transport locales de la famille de protocoles du socket à laquelle l’application peut se lier.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-175">The **SIO\_ADDRESS\_LIST\_QUERY** control code obtains a list of local transport addresses of the socket's protocol family to which the application can bind.</span></span>
<span data-ttu-id="7f9b0-176">La liste des adresses varie en fonction de la famille d’adresses.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-176">The list of addresses varies based on address family.</span></span>

<span data-ttu-id="7f9b0-177">Pour la famille d’adresses inet6 de la même \_ façon, toutes les adresses sont retournées, à l’exception des suivantes :</span><span class="sxs-lookup"><span data-stu-id="7f9b0-177">For the AF\_INET6 address family, all addresses are returned except for the following:</span></span>

* <span data-ttu-id="7f9b0-178">Toute adresse IP où l’état de détection d’adresse dupliquée (DAD) n’est pas IpDadStatePreferred.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-178">Any IP address where the duplicate address detection (DAD) state is not IpDadStatePreferred.</span></span>
* <span data-ttu-id="7f9b0-179">Toute adresse IP avec un niveau d’étendue inférieur à ScopeLevelSubnet sur une interface où le type d’interface est **si le \_ type de \_ \_ bouclage logiciel** est activé.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-179">Any IP address with a scope level lower than ScopeLevelSubnet on an interface where the interface type is **IF\_TYPE\_SOFTWARE\_LOOPBACK**.</span></span>
<span data-ttu-id="7f9b0-180">Cela signifie que les adresses Link-local (FE80 : \*) et de bouclage ( :: 1) sur les interfaces de si le type de **\_ \_ \_ bouclage logiciel** est exclu, mais pas si ces adresses se trouvent sur une interface avec un type différent.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-180">This means link-local (fe80:\*) and loopback (::1) addresses on interfaces of **IF\_TYPE\_SOFTWARE\_LOOPBACK** type are excluded, but not if these addresses are on an interface with a different type.</span></span>

<span data-ttu-id="7f9b0-181">Pour la famille d’adresses d' **\_ inet AF** , toutes les adresses sont retournées, à l’exception des suivantes :</span><span class="sxs-lookup"><span data-stu-id="7f9b0-181">For the **AF\_INET** address family, all addresses are returned except for the following:</span></span>

* <span data-ttu-id="7f9b0-182">Toute adresse IP où l’état de détection d’adresse dupliquée (DAD) n’est pas IpDadStatePreferred.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-182">Any IP address where the duplicate address detection (DAD) state is not IpDadStatePreferred.</span></span>
* <span data-ttu-id="7f9b0-183">Toute adresse IP sur une interface où le type d’interface est **si le \_ type de \_ \_ bouclage logiciel** et le lien est local.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-183">Any IP address on an interface where the interface type is **IF\_TYPE\_SOFTWARE\_LOOPBACK** and link is local.</span></span>
<span data-ttu-id="7f9b0-184">Cela signifie que les adresses lien-local (169,254.*) et de bouclage (127.*) sur les interfaces de si le type de **\_ \_ \_ bouclage logiciel** est exclu, mais pas si ces adresses se trouvent sur une interface avec un type différent.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-184">This means link-local (169.254.*) and loopback (127.*) addresses on interfaces of **IF\_TYPE\_SOFTWARE\_LOOPBACK** type are excluded, but not if these addresses are on an interface with a different type.</span></span>

<span data-ttu-id="7f9b0-185">Pour plus d’informations sur l’État DAD, consultez la documentation d’assistance IP sur l’énumération [**IP \_ Dad \_ State**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) et la structure d' [**\_ \_ \_ adresse de monodiffusion de carte IP**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) et la documentation MIB sur la structure de [**\_ \_ ligne MIB UNICASTIPADDRESS**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row) .</span><span class="sxs-lookup"><span data-stu-id="7f9b0-185">For more information on DAD state, see the IP Helper documentation on the [**IP\_DAD\_STATE**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) enumeration and [**IP\_ADAPTER\_UNICAST\_ADDRESS**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) structure and the MIB documentation on the [**MIB\_UNICASTIPADDRESS\_ROW**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row) structure.</span></span>
<span data-ttu-id="7f9b0-186">Pour plus d’informations sur le type d’interface, consultez la documentation d’assistance IP sur la structure d' [**\_ \_ adresses IP**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) et la fonction [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) et la documentation MIB sur [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) structure.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-186">For more information on interface type, see the IP Helper documentation on the [**IP\_ADAPTER\_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) structure and the [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) function and the MIB documentation on [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) structure.</span></span>
<span data-ttu-id="7f9b0-187">Pour plus d’informations sur le niveau de l’étendue, consultez la documentation d’assistance IP sur la structure [**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) et l’énumération [**\_ au niveau**](/windows/desktop/api/ws2def/ne-ws2def-scope_level) de l’étendue.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-187">For more information on the scope level, see the IP Helper documentation on the [**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) structure and the [**SCOPE\_LEVEL**](/windows/desktop/api/ws2def/ne-ws2def-scope_level) enumeration.</span></span>

<span data-ttu-id="7f9b0-188">La liste renvoyée dans la mémoire tampon de sortie vers laquelle pointe le paramètre *lpvOutBuffer* se présente sous la forme d’une structure de [**liste d' \_ adresses \_ de sockets**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list) .</span><span class="sxs-lookup"><span data-stu-id="7f9b0-188">The list returned in the output buffer pointed to by the *lpvOutBuffer* parameter is in the form of a [**SOCKET\_ADDRESS\_LIST**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list) structure.</span></span>

<span data-ttu-id="7f9b0-189">Si la mémoire tampon de sortie spécifiée dans le paramètre *lpvOutBuffer* n’est pas assez grande pour contenir la liste d’adresses, l' **\_ erreur de socket** est retournée comme résultat de cette IOCTL et [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [WSAEFAULT](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="7f9b0-189">If the output buffer specified in the *lpvOutBuffer* parameter is not large enough to contain the address list, **SOCKET\_ERROR** is returned as the result of this IOCTL and [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [WSAEFAULT](windows-sockets-error-codes-2.md).</span></span>
<span data-ttu-id="7f9b0-190">La taille requise, en octets, de la mémoire tampon de sortie est retournée dans le paramètre *lpcbBytesReturned* dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-190">The required size, in bytes, for the output buffer is returned in the *lpcbBytesReturned* parameter in this case.</span></span>
<span data-ttu-id="7f9b0-191">Notez que le code d’erreur [WSAEFAULT](windows-sockets-error-codes-2.md) est également retourné si le paramètre *lpvInBuffer*, *lpvOutBuffer* ou *lpcbBytesReturned* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-191">Note the [WSAEFAULT](windows-sockets-error-codes-2.md) error code is also returned if the *lpvInBuffer*, *lpvOutBuffer*, or *lpcbBytesReturned* parameter is not completely contained in a valid part of the user address space.</span></span>

<span data-ttu-id="7f9b0-192">La requête IOCTL de la **\_ liste d’adresses \_ \_ SIO** est normalement appelée de façon synchrone avec le paramètre *lpvOverlapped* défini sur **null**, car la liste des adresses est immédiatement retournée.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-192">The **SIO\_ADDRESS\_LIST\_QUERY** IOCTL is normally called synchronously with the *lpvOverlapped* parameter set to **NULL**, since the list of addresses is returned immediately.</span></span>

<span data-ttu-id="7f9b0-193">**Remarque**  Dans les environnements plug-and-Play Windows, les adresses peuvent être ajoutées et supprimées dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-193">**Note**  In Windows Plug-n-Play environments, addresses can be added and removed dynamically.</span></span>
<span data-ttu-id="7f9b0-194">Par conséquent, les applications ne peuvent pas compter sur la persistance des informations retournées par la **\_ requête de \_ liste \_ d’adresses SIO** .</span><span class="sxs-lookup"><span data-stu-id="7f9b0-194">Therefore, applications cannot rely on the information returned by **SIO\_ADDRESS\_LIST\_QUERY** to be persistent.</span></span>
<span data-ttu-id="7f9b0-195">Les applications peuvent s’inscrire à des notifications de changement d’adresse par le biais de l’IOCTL de **\_ modification de \_ liste \_ d’adresses SIO** qui fournit une notification par le biais d’un événement d’e/s ou de modification de la **\_ \_ liste \_ d’adresses FD** .</span><span class="sxs-lookup"><span data-stu-id="7f9b0-195">Applications may register for address change notifications through the **SIO\_ADDRESS\_LIST\_CHANGE** IOCTL which provides for notification through either overlapped I/O or **FD\_ADDRESS\_LIST\_CHANGE** event.</span></span>
<span data-ttu-id="7f9b0-196">La séquence d’actions suivante peut être utilisée pour garantir que l’application dispose toujours des informations de liste d’adresses actuelles :</span><span class="sxs-lookup"><span data-stu-id="7f9b0-196">The following sequence of actions can be used to guarantee that the application always has current address list information:</span></span>

* <span data-ttu-id="7f9b0-197">Émettre l’IOCTL de modification de la **\_ liste d’adresses \_ \_ SIO**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-197">Issue the **SIO\_ADDRESS\_LIST\_CHANGE** IOCTL</span></span>
* <span data-ttu-id="7f9b0-198">Émettre l’IOCTL de **\_ requête de \_ liste \_ d’adresses SIO**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-198">Issue the **SIO\_ADDRESS\_LIST\_QUERY** IOCTL</span></span>
* <span data-ttu-id="7f9b0-199">Chaque fois que l’appel de la **\_ liste d’adresses SIO \_ \_ change** IOCTL notifie l’application d’une modification de liste d’adresses (via des e/s avec chevauchement ou en signalant un événement de modification de **\_ \_ liste \_ d’adresses FD** ), toute la séquence d’actions doit être répétée.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-199">Whenever the **SIO\_ADDRESS\_LIST\_CHANGE** IOCTL call notifies the application of an address list change (either through overlapped I/O or by signaling **FD\_ADDRESS\_LIST\_CHANGE** event), the whole sequence of actions should be repeated.</span></span>

<span data-ttu-id="7f9b0-200">Dans le kit de développement logiciel (SDK) Microsoft Windows publié pour Windows Vista et versions ultérieures, l’Organisation des fichiers d’en-tête a changé et le code de contrôle de **\_ requête de \_ liste \_ d’adresses SIO** est défini dans le fichier d’en-tête *Ws2def. h* .</span><span class="sxs-lookup"><span data-stu-id="7f9b0-200">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the **SIO\_ADDRESS\_LIST\_QUERY** control code is defined in the *Ws2def.h* header file.</span></span>
<span data-ttu-id="7f9b0-201">Notez que le fichier d’en-tête *Ws2def. h* est automatiquement inclus dans *Winsock2. h* et ne doit jamais être utilisé directement.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-201">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f9b0-202">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f9b0-202">See also</span></span>

[<span data-ttu-id="7f9b0-203">**GetAdaptersAddresses**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-203">**GetAdaptersAddresses**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

[<span data-ttu-id="7f9b0-204">**IP_ADAPTER_ADDRESSES**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-204">**IP_ADAPTER_ADDRESSES**</span></span>](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp)

[<span data-ttu-id="7f9b0-205">**IP_ADAPTER_UNICAST_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-205">**IP_ADAPTER_UNICAST_ADDRESS**</span></span>](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh)

[<span data-ttu-id="7f9b0-206">**IP_DAD_STATE**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-206">**IP_DAD_STATE**</span></span>](/windows/desktop/api/nldef/ne-nldef-nl_dad_state)

[<span data-ttu-id="7f9b0-207">**MIB_IF_ROW2**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-207">**MIB_IF_ROW2**</span></span>](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2)

[<span data-ttu-id="7f9b0-208">**MIB_UNICASTIPADDRESS_ROW**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-208">**MIB_UNICASTIPADDRESS_ROW**</span></span>](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)

[<span data-ttu-id="7f9b0-209">**SCOPE_LEVEL**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-209">**SCOPE_LEVEL**</span></span>](/windows/desktop/api/ws2def/ne-ws2def-scope_level)

[<span data-ttu-id="7f9b0-210">**SOCKET_ADDRESS_LIST**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-210">**SOCKET_ADDRESS_LIST**</span></span>](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)

[<span data-ttu-id="7f9b0-211">**socle**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-211">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="7f9b0-212">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-212">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="7f9b0-213">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-213">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="7f9b0-214">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-214">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="7f9b0-215">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-215">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="7f9b0-216">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-216">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="7f9b0-217">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="7f9b0-217">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
