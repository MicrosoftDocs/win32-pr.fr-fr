---
description: Le code de contrôle interroge les paramètres de transport sur un Socket.
ms.assetid: 3845BE07-A414-4118-96E8-8BEF1DEDB1D3
title: Code de contrôle SIO_QUERY_TRANSPORT_SETTING
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 592301f0fcdbbb0d3d5babba446583d2e48db086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863805"
---
# <a name="sio_query_transport_setting-control-code"></a><span data-ttu-id="0904c-103">Code de contrôle SIO_QUERY_TRANSPORT_SETTING</span><span class="sxs-lookup"><span data-stu-id="0904c-103">SIO_QUERY_TRANSPORT_SETTING Control Code</span></span>

## <a name="description"></a><span data-ttu-id="0904c-104">Description</span><span class="sxs-lookup"><span data-stu-id="0904c-104">Description</span></span>

<span data-ttu-id="0904c-105">Le code de contrôle du **\_ paramètre de \_ transport \_ de requête SIO** interroge les paramètres de transport sur un Socket.</span><span class="sxs-lookup"><span data-stu-id="0904c-105">The **SIO\_QUERY\_TRANSPORT\_SETTING** control code queries the transport settings on a socket.</span></span>

<span data-ttu-id="0904c-106">Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="0904c-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="0904c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0904c-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="0904c-108">s</span><span class="sxs-lookup"><span data-stu-id="0904c-108">s</span></span>

<span data-ttu-id="0904c-109">Descripteur identifiant un Socket.</span><span class="sxs-lookup"><span data-stu-id="0904c-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="0904c-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="0904c-110">dwIoControlCode</span></span>

<span data-ttu-id="0904c-111">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="0904c-111">The control code for the operation.</span></span>
<span data-ttu-id="0904c-112">Utilisez **le \_ \_ \_ paramètre de transport de requête SIO** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="0904c-112">Use **SIO\_QUERY\_TRANSPORT\_SETTING** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="0904c-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="0904c-113">lpvInBuffer</span></span>

<span data-ttu-id="0904c-114">Pointeur vers la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0904c-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="0904c-115">Ce paramètre contient un pointeur vers une structure dans laquelle le premier membre de la structure est une structure [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) qui détermine le paramètre de transport interrogé.</span><span class="sxs-lookup"><span data-stu-id="0904c-115">This parameter contains a pointer to a structure where the first member of the structure is a [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) structure that determines what transport setting is being queried.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="0904c-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="0904c-116">cbInBuffer</span></span>

<span data-ttu-id="0904c-117">Taille, en octets, de la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0904c-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="0904c-118">Ce paramètre dépend du paramètre de transport en cours d’interrogation.</span><span class="sxs-lookup"><span data-stu-id="0904c-118">This parameter depends on the transport setting being queried.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="0904c-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="0904c-119">lpvOutBuffer</span></span>

<span data-ttu-id="0904c-120">Pointeur vers la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="0904c-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="0904c-121">Ce paramètre dépend du paramètre de transport interrogé si les paramètres *lpOverlapped* et *LpCompletionRoutine* ont la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="0904c-121">This parameter depends on the transport setting being queried if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="0904c-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="0904c-122">cbOutBuffer</span></span>

<span data-ttu-id="0904c-123">Taille, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="0904c-123">The size, in bytes, of the output buffer.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="0904c-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="0904c-124">lpcbBytesReturned</span></span>

<span data-ttu-id="0904c-125">Pointeur vers une variable qui reçoit la taille, en octets, des données stockées dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="0904c-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="0904c-126">Si la mémoire tampon de sortie est trop petite, l’appel échoue, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [**WSAEINVAL**](windows-sockets-error-codes-2.md)et le paramètre *LpcbBytesReturned* pointe vers une valeur **DWORD** égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="0904c-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="0904c-127">Si *lpOverlapped* a la valeur **null**, la valeur **DWORD** vers laquelle pointe le paramètre *lpcbBytesReturned* retourné sur un appel réussi ne peut pas être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="0904c-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="0904c-128">Si le paramètre *lpOverlapped* n’a pas la **valeur null** pour les sockets superposés, les opérations qui ne peuvent pas être terminées immédiatement seront lancées et l’achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="0904c-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="0904c-129">La valeur **DWORD** pointée par le paramètre *lpcbBytesReturned* retourné peut être égale à zéro, car la taille des données stockées ne peut pas être déterminée tant que l’opération avec chevauchement n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="0904c-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="0904c-130">L’état d’achèvement final peut être récupéré lorsque la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="0904c-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="0904c-131">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="0904c-131">lpvOverlapped</span></span>

<span data-ttu-id="0904c-132">Pointeur vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="0904c-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="0904c-133">Si le socket *s* a été créé sans l’attribut Overlapped, le paramètre *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="0904c-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="0904c-134">Si *s* a été ouvert avec l’attribut Overlapped et que le paramètre *lpOverlapped* n’a pas la **valeur null**, l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="0904c-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="0904c-135">Dans ce cas, le paramètre *lpOverlapped* doit pointer vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="0904c-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="0904c-136">Pour les opérations avec chevauchement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne immédiatement, et la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="0904c-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="0904c-137">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="0904c-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="0904c-138">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="0904c-138">lpCompletionRoutine</span></span>

<span data-ttu-id="0904c-139">Type : \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="0904c-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="0904c-140">Pointeur vers la routine de saisie semi-automatique appelée lorsque l’opération est terminée (ignoré pour les sockets non superposés).</span><span class="sxs-lookup"><span data-stu-id="0904c-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="0904c-141">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="0904c-141">lpThreadId</span></span>

<span data-ttu-id="0904c-142">Pointeur vers une structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) qui doit être utilisée par le fournisseur dans un appel ultérieur à [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="0904c-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="0904c-143">Le fournisseur doit stocker la structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) référencée (pas le pointeur vers le même) jusqu’à ce que la fonction [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) soit retournée.</span><span class="sxs-lookup"><span data-stu-id="0904c-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="0904c-144">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="0904c-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="0904c-145">lpErrno</span><span class="sxs-lookup"><span data-stu-id="0904c-145">lpErrno</span></span>

<span data-ttu-id="0904c-146">Pointeur vers le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0904c-146">A pointer to the error code.</span></span>

<span data-ttu-id="0904c-147">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="0904c-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="0904c-148">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0904c-148">Return value</span></span>

<span data-ttu-id="0904c-149">Si l’opération se termine correctement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="0904c-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="0904c-150">Si l’opération échoue ou est en attente, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne une **\_ erreur de socket**.</span><span class="sxs-lookup"><span data-stu-id="0904c-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="0904c-151">Pour afficher les informations d’erreur étendues, appelez [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="0904c-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="0904c-152">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="0904c-152">Error code</span></span> | <span data-ttu-id="0904c-153">Signification</span><span class="sxs-lookup"><span data-stu-id="0904c-153">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="0904c-154">**ERREUR \_ de \_ mémoire tampon insuffisante**</span><span class="sxs-lookup"><span data-stu-id="0904c-154">**ERROR\_INSUFFICIENT\_BUFFER**</span></span> | <span data-ttu-id="0904c-155">La zone de données passée à un appel système est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="0904c-155">The data area passed to a system call is too small.</span></span> <span data-ttu-id="0904c-156">Cette erreur est retournée si la mémoire tampon vers laquelle pointe le paramètre *lpvOutBuffer* avec une taille de mémoire tampon passée dans le paramètre *cbOutBuffer* est trop petite.</span><span class="sxs-lookup"><span data-stu-id="0904c-156">This error is returned if the buffer pointed to by the *lpvOutBuffer* parameter with a buffer size passed in the *cbOutBuffer* parameter is too small.</span></span> <span data-ttu-id="0904c-157">La taille de la mémoire tampon requise est retournée dans le paramètre *lpcbBytesReturned* .</span><span class="sxs-lookup"><span data-stu-id="0904c-157">The buffer size required will be returned in the *lpcbBytesReturned* parameter.</span></span> |
| <span data-ttu-id="0904c-158">**\_e/s WSA \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="0904c-158">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="0904c-159">Une opération avec chevauchement a été correctement initiée et l’achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="0904c-159">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="0904c-160">**\_opération WSA \_ abandonnée**</span><span class="sxs-lookup"><span data-stu-id="0904c-160">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="0904c-161">Une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO \_ flush** ioctl.</span><span class="sxs-lookup"><span data-stu-id="0904c-161">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="0904c-162">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="0904c-162">**WSAEFAULT**</span></span> | <span data-ttu-id="0904c-163">Le paramètre *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0904c-163">The *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped*, or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="0904c-164">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="0904c-164">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="0904c-165">La fonction est appelée lorsqu’un rappel est en cours.</span><span class="sxs-lookup"><span data-stu-id="0904c-165">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="0904c-166">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="0904c-166">**WSAEINTR**</span></span> | <span data-ttu-id="0904c-167">Une opération de blocage a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="0904c-167">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="0904c-168">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="0904c-168">**WSAEINVAL**</span></span> | <span data-ttu-id="0904c-169">Le paramètre *dwIoControlCode* n’est pas une commande valide, ou un paramètre d’entrée spécifié n’est pas acceptable, ou la commande n’est pas applicable au type de socket spécifié.</span><span class="sxs-lookup"><span data-stu-id="0904c-169">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="0904c-170">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="0904c-170">**WSAENETDOWN**</span></span> | <span data-ttu-id="0904c-171">Le sous-système réseau a échoué.</span><span class="sxs-lookup"><span data-stu-id="0904c-171">The network subsystem has failed.</span></span> |
| <span data-ttu-id="0904c-172">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="0904c-172">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="0904c-173">L’option de socket n’est pas prise en charge sur le protocole spécifié.</span><span class="sxs-lookup"><span data-stu-id="0904c-173">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="0904c-174">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="0904c-174">**WSAENOTCONN**</span></span> | <span data-ttu-id="0904c-175">Le socket n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="0904c-175">The socket s is not connected.</span></span> |
| <span data-ttu-id="0904c-176">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="0904c-176">**WSAENOTSOCK**</span></span> | <span data-ttu-id="0904c-177">Le descripteur s n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="0904c-177">The descriptor s is not a socket.</span></span> |
| <span data-ttu-id="0904c-178">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="0904c-178">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="0904c-179">La commande IOCTL spécifiée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0904c-179">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="0904c-180">Cette erreur est retournée si **le \_ \_ \_ paramètre de transport IOCTL de requête SIO** n’est pas pris en charge par le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="0904c-180">This error is returned if the **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="0904c-181">Notes</span><span class="sxs-lookup"><span data-stu-id="0904c-181">Remarks</span></span>

<span data-ttu-id="0904c-182">Le **\_ paramètre de \_ transport \_ de requête SIO** IOCTL est pris en charge sur windows 8, Windows Server 2012 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0904c-182">The **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="0904c-183">Le **\_ paramètre de \_ transport \_ de requête SIO** IOCTL est un ioctl générique utilisé pour interroger les paramètres de transport sur un Socket.</span><span class="sxs-lookup"><span data-stu-id="0904c-183">The **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL is a generic IOCTL used to query the transport settings on a socket.</span></span>
<span data-ttu-id="0904c-184">Le paramètre de transport interrogé est basé sur le [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passé dans le paramètre *lpvInBuffer* .</span><span class="sxs-lookup"><span data-stu-id="0904c-184">The transport setting being queried is based on the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the *lpvInBuffer* parameter.</span></span>

<span data-ttu-id="0904c-185">Le seul paramètre de transport actuellement défini est pour la fonctionnalité de **\_ fonctionnalité de \_ notification \_ en temps réel** sur un socket TCP.</span><span class="sxs-lookup"><span data-stu-id="0904c-185">The only transport setting currently defines is for the **REAL\_TIME\_NOTIFICATION\_CAPABILITY** capability on a TCP socket.</span></span>

<span data-ttu-id="0904c-186">Si le [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passé dans le paramètre *lpvInBuffer* a le membre GUID défini sur **la \_ \_ \_ fonctionnalité de notification en temps réel**, il s’agit d’une demande d’interrogation des paramètres de notification en temps réel pour le socket TCP utilisé avec [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) pour recevoir des notifications de réseau en arrière-plan dans une application du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="0904c-186">If the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the *lpvInBuffer* parameter has the Guid member set to **REAL\_TIME\_NOTIFICATION\_CAPABILITY**, then this is a request to query the real time notification settings for the TCP socket used with the [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) to receive background network notifications in a Windows Store app.</span></span>
<span data-ttu-id="0904c-187">Le paramètre *lpvInBuffer* doit pointer vers une structure [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) .</span><span class="sxs-lookup"><span data-stu-id="0904c-187">The *lpvInBuffer* parameter should point to a [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) structure.</span></span>
<span data-ttu-id="0904c-188">Le paramètre *lpvOutBuffer* doit pointer vers une structure de sortie de **paramètre de \_ notification en temps \_ \_ \_ réel** .</span><span class="sxs-lookup"><span data-stu-id="0904c-188">The *lpvOutBuffer* parameter should point to a **REAL\_TIME\_NOTIFICATION\_SETTING\_OUTPUT** structure.</span></span>
<span data-ttu-id="0904c-189">Ce paramètre de transport s’applique uniquement aux sockets TCP.</span><span class="sxs-lookup"><span data-stu-id="0904c-189">This transport setting applies only to TCP sockets.</span></span>
<span data-ttu-id="0904c-190">Ce paramètre de transport permet à WinInet ou aux services réseau similaires d’interroger un socket TCP donné pour déterminer l’état de [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) .</span><span class="sxs-lookup"><span data-stu-id="0904c-190">This transport setting provides a way for WinInet or similar network services to query a given TCP socket to determine the [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) status.</span></span>
<span data-ttu-id="0904c-191">Une application du Windows Store n’appellera pas cette IOCTL directement.</span><span class="sxs-lookup"><span data-stu-id="0904c-191">A Windows Store app will not call this IOCTL directly.</span></span>
<span data-ttu-id="0904c-192">Si l’appel [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** réussit, cette IOCTL retourne une structure de sortie de **\_ \_ \_ paramètre \_ de notification en temps réel** avec l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="0904c-192">If the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** call is successful, this IOCTL returns a **REAL\_TIME\_NOTIFICATION\_SETTING\_OUTPUT** structure with the current status.</span></span>

<span data-ttu-id="0904c-193">Le **\_ paramètre de \_ transport \_ de requête SIO** IOCTL permet à WinInet ou aux services réseau similaires d’interroger l’état du paramètre de transport d’un socket TCP donné pour déterminer si [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) est activé sur le Socket.</span><span class="sxs-lookup"><span data-stu-id="0904c-193">The **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL provides a way for WinInet or similar network services to query for the transport setting status for a given TCP socket to determine if [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) is enabled on the socket.</span></span>
<span data-ttu-id="0904c-194">Une application du Windows Store n’appellera pas cette IOCTL directement.</span><span class="sxs-lookup"><span data-stu-id="0904c-194">A Windows Store app will not call this IOCTL directly.</span></span>

<span data-ttu-id="0904c-195">Cette IOCTL s’applique uniquement aux sockets TCP.</span><span class="sxs-lookup"><span data-stu-id="0904c-195">This IOCTL applies only to TCP sockets.</span></span>

## <a name="see-also"></a><span data-ttu-id="0904c-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0904c-196">See also</span></span>

[<span data-ttu-id="0904c-197">**CONTROL_CHANNEL_TRIGGER_STATUS**</span><span class="sxs-lookup"><span data-stu-id="0904c-197">**CONTROL_CHANNEL_TRIGGER_STATUS**</span></span>](/windows/desktop/api/mstcpip/ne-mstcpip-control_channel_trigger_status)

[<span data-ttu-id="0904c-198">**ControlChannelTrigger**</span><span class="sxs-lookup"><span data-stu-id="0904c-198">**ControlChannelTrigger**</span></span>](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[<span data-ttu-id="0904c-199">**REAL_TIME_NOTIFICATION_SETTING_OUTPUT**</span><span class="sxs-lookup"><span data-stu-id="0904c-199">**REAL_TIME_NOTIFICATION_SETTING_OUTPUT**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-real_time_notification_setting_output)

[<span data-ttu-id="0904c-200">**SIO_APPLY_TRANSPORT_SETTING**</span><span class="sxs-lookup"><span data-stu-id="0904c-200">**SIO_APPLY_TRANSPORT_SETTING**</span></span>](sio-apply-transport-setting.md)

[<span data-ttu-id="0904c-201">socle</span><span class="sxs-lookup"><span data-stu-id="0904c-201">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="0904c-202">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="0904c-202">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="0904c-203">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="0904c-203">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="0904c-204">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="0904c-204">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="0904c-205">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="0904c-205">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="0904c-206">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="0904c-206">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="0904c-207">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="0904c-207">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
