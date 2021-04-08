---
description: Le code de contrôle interroge l’association entre un socket et un cœur de processeur RSS et un nœud NUMA.
ms.assetid: DAF18C92-B479-474F-B438-0746CBA20653
title: Code de contrôle SIO_QUERY_RSS_PROCESSOR_INFO
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: a2d251fa4fee996adaec51599e7b1d140a296b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951169"
---
# <a name="sio_query_rss_processor_info-control-code"></a><span data-ttu-id="ad7e7-103">Code de contrôle SIO_QUERY_RSS_PROCESSOR_INFO</span><span class="sxs-lookup"><span data-stu-id="ad7e7-103">SIO_QUERY_RSS_PROCESSOR_INFO Control Code</span></span>

## <a name="description"></a><span data-ttu-id="ad7e7-104">Description</span><span class="sxs-lookup"><span data-stu-id="ad7e7-104">Description</span></span>

<span data-ttu-id="ad7e7-105">Le code de contrôle **\_ \_ \_ \_ informations sur le processeur RSS de la requête SIO** interroge l’association entre un socket et un cœur de processeur RSS et un nœud NUMA.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-105">The **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** control code queries the association between a socket and an RSS processor core and NUMA node.</span></span>

<span data-ttu-id="ad7e7-106">Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="ad7e7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad7e7-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="ad7e7-108">s</span><span class="sxs-lookup"><span data-stu-id="ad7e7-108">s</span></span>

<span data-ttu-id="ad7e7-109">Descripteur identifiant un Socket.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="ad7e7-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="ad7e7-110">dwIoControlCode</span></span>

<span data-ttu-id="ad7e7-111">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-111">The control code for the operation.</span></span>
<span data-ttu-id="ad7e7-112">Utilisez **les \_ \_ informations du \_ processeur \_ RSS de la requête SIO** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-112">Use **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="ad7e7-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="ad7e7-113">lpvInBuffer</span></span>

<span data-ttu-id="ad7e7-114">Pointeur vers la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="ad7e7-115">Ce paramètre n’est pas utilisé pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="ad7e7-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="ad7e7-116">cbInBuffer</span></span>

<span data-ttu-id="ad7e7-117">Taille, en octets, de la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="ad7e7-118">Ce paramètre n’est pas utilisé pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="ad7e7-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="ad7e7-119">lpvOutBuffer</span></span>

<span data-ttu-id="ad7e7-120">Pointeur vers la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="ad7e7-121">Ce paramètre doit pointer vers une structure d' [**\_ \_ affinité de processeur de socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) si les paramètres *LpOverlapped* et *lpCompletionRoutine* ont la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-121">This parameter should point to a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="ad7e7-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="ad7e7-122">cbOutBuffer</span></span>

<span data-ttu-id="ad7e7-123">Taille, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="ad7e7-124">Ce paramètre doit avoir au moins la taille d’une structure d' [**\_ \_ affinité du processeur de sockets**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) .</span><span class="sxs-lookup"><span data-stu-id="ad7e7-124">This parameter must be at least the size of a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="ad7e7-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="ad7e7-125">lpcbBytesReturned</span></span>

<span data-ttu-id="ad7e7-126">Pointeur vers une variable qui reçoit la taille, en octets, des données stockées dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="ad7e7-127">Si la mémoire tampon de sortie est trop petite, l’appel échoue, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [**WSAEINVAL**](windows-sockets-error-codes-2.md)et le paramètre *LpcbBytesReturned* pointe vers une valeur *DWORD* égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a *DWORD* value of zero.</span></span>

<span data-ttu-id="ad7e7-128">Si *lpOverlapped* a la valeur **null**, la valeur **DWORD** vers laquelle pointe le paramètre *lpcbBytesReturned* retourné sur un appel réussi ne peut pas être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="ad7e7-129">Si le paramètre *lpOverlapped* n’a pas la **valeur null** pour les sockets superposés, les opérations qui ne peuvent pas être terminées immédiatement seront lancées et l’achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="ad7e7-130">La valeur **DWORD** pointée par le paramètre *lpcbBytesReturned* retourné peut être égale à zéro, car la taille des données stockées ne peut pas être déterminée tant que l’opération avec chevauchement n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="ad7e7-131">L’état d’achèvement final peut être récupéré lorsque la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="ad7e7-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="ad7e7-132">lpvOverlapped</span></span>

<span data-ttu-id="ad7e7-133">Pointeur vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="ad7e7-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="ad7e7-134">Si le socket *s* a été créé sans l’attribut Overlapped, le paramètre *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="ad7e7-135">Si *s* a été ouvert avec l’attribut Overlapped et que le paramètre *lpOverlapped* n’a pas la **valeur null**, l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="ad7e7-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="ad7e7-136">Dans ce cas, le paramètre *lpOverlapped* doit pointer vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="ad7e7-137">Pour les opérations avec chevauchement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne immédiatement, et la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="ad7e7-138">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="ad7e7-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="ad7e7-139">lpCompletionRoutine</span></span>

<span data-ttu-id="ad7e7-140">Type : \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="ad7e7-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="ad7e7-141">Pointeur vers la routine de saisie semi-automatique appelée lorsque l’opération est terminée (ignoré pour les sockets non superposés).</span><span class="sxs-lookup"><span data-stu-id="ad7e7-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="ad7e7-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="ad7e7-142">lpThreadId</span></span>

<span data-ttu-id="ad7e7-143">Pointeur vers une structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) qui doit être utilisée par le fournisseur dans un appel ultérieur à [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="ad7e7-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="ad7e7-144">Le fournisseur doit stocker la structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) référencée (pas le pointeur vers le même) jusqu’à ce que la fonction [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) soit retournée.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="ad7e7-145">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="ad7e7-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="ad7e7-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="ad7e7-146">lpErrno</span></span>

<span data-ttu-id="ad7e7-147">Pointeur vers le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-147">A pointer to the error code.</span></span>

<span data-ttu-id="ad7e7-148">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="ad7e7-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="ad7e7-149">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ad7e7-149">Return value</span></span>

<span data-ttu-id="ad7e7-150">Si l’opération se termine correctement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="ad7e7-151">Si l’opération échoue ou est en attente, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne une **\_ erreur de socket**.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="ad7e7-152">Pour afficher les informations d’erreur étendues, appelez [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="ad7e7-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="ad7e7-153">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="ad7e7-153">Error code</span></span> | <span data-ttu-id="ad7e7-154">Signification</span><span class="sxs-lookup"><span data-stu-id="ad7e7-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="ad7e7-155">**ERREUR \_ de \_ mémoire tampon insuffisante**</span><span class="sxs-lookup"><span data-stu-id="ad7e7-155">**ERROR\_INSUFFICIENT\_BUFFER**</span></span> | <span data-ttu-id="ad7e7-156">La zone de données passée à un appel système est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-156">The data area passed to a system call is too small.</span></span> <span data-ttu-id="ad7e7-157">Cette erreur est retournée si la mémoire tampon vers laquelle pointe le paramètre *lpvOutBuffer* avec une taille de mémoire tampon passée dans le paramètre *cbOutBuffer* est trop petite.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-157">This error is returned if the buffer pointed to by the *lpvOutBuffer* parameter with a buffer size passed in the *cbOutBuffer* parameter is too small.</span></span> <span data-ttu-id="ad7e7-158">La taille de la mémoire tampon requise est retournée dans le paramètre *lpcbBytesReturned* .</span><span class="sxs-lookup"><span data-stu-id="ad7e7-158">The buffer size required will be returned in the *lpcbBytesReturned* parameter.</span></span> <span data-ttu-id="ad7e7-159">Cette erreur est retournée si le paramètre *cbOutBuffer* est inférieur à la taille d’une structure d' [**affinité du \_ processeur \_ de sockets**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) .</span><span class="sxs-lookup"><span data-stu-id="ad7e7-159">This error is returned if the *cbOutBuffer* parameter is less than the size of a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure.</span></span> |
| <span data-ttu-id="ad7e7-160">**\_e/s WSA \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="ad7e7-160">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="ad7e7-161">Une opération avec chevauchement a été correctement initiée et l’achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-161">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="ad7e7-162">**\_opération WSA \_ abandonnée**</span><span class="sxs-lookup"><span data-stu-id="ad7e7-162">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="ad7e7-163">Une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande **SIO \_ flush** ioctl.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-163">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="ad7e7-164">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="ad7e7-164">**WSAEFAULT**</span></span> | <span data-ttu-id="ad7e7-165">Le paramètre *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* n’est pas entièrement contenu dans une partie valide de l’espace d’adressage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-165">The *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="ad7e7-166">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="ad7e7-166">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="ad7e7-167">La fonction est appelée lorsqu’un rappel est en cours.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-167">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="ad7e7-168">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="ad7e7-168">**WSAEINTR**</span></span> | <span data-ttu-id="ad7e7-169">Une opération de blocage a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-169">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="ad7e7-170">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="ad7e7-170">**WSAEINVAL**</span></span> | <span data-ttu-id="ad7e7-171">Le paramètre *dwIoControlCode* n’est pas une commande valide, ou un paramètre d’entrée spécifié n’est pas acceptable, ou la commande n’est pas applicable au type de socket spécifié.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-171">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="ad7e7-172">Cette erreur est retournée si le paramètre *cbOutBuffer* est inférieur à la taille d’une structure d' [**affinité du \_ processeur \_ de sockets**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) .</span><span class="sxs-lookup"><span data-stu-id="ad7e7-172">This error is returned if the *cbOutBuffer* parameter is less than the size of a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure.</span></span>
| <span data-ttu-id="ad7e7-173">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="ad7e7-173">**WSAENETDOWN**</span></span> | <span data-ttu-id="ad7e7-174">Le sous-système réseau a échoué.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-174">The network subsystem has failed.</span></span> |
| <span data-ttu-id="ad7e7-175">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="ad7e7-175">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="ad7e7-176">L’option de socket n’est pas prise en charge sur le protocole spécifié.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-176">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="ad7e7-177">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="ad7e7-177">**WSAENOTCONN**</span></span> | <span data-ttu-id="ad7e7-178">Le socket *n'* est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-178">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="ad7e7-179">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="ad7e7-179">**WSAENOTSOCK**</span></span> | <span data-ttu-id="ad7e7-180">Le descripteur *s* n’est pas un Socket.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-180">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="ad7e7-181">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="ad7e7-181">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="ad7e7-182">La commande IOCTL spécifiée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-182">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="ad7e7-183">Cette erreur est retournée si le fournisseur de transport ne prend pas en charge l’IOCTL de l' **\_ \_ \_ \_ information sur le processeur RSS de la requête SIO** .</span><span class="sxs-lookup"><span data-stu-id="ad7e7-183">This error is returned if the **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="ad7e7-184">Notes</span><span class="sxs-lookup"><span data-stu-id="ad7e7-184">Remarks</span></span>

<span data-ttu-id="ad7e7-185">Les **informations IOCTL du \_ \_ \_ processeur \_ RSS de la requête SIO** sont prises en charge sur Windows 8, Windows Server 2012 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-185">The **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="ad7e7-186">Les **informations IOCTL du \_ \_ \_ processeur \_ RSS de la requête SIO** permettent de déterminer l’association entre un socket et un cœur de processeur RSS et un nœud NUMA.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-186">The **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL is used to determine the association between a socket and an RSS processor core and NUMA node.</span></span>
<span data-ttu-id="ad7e7-187">Cette IOCTL retourne une structure d' [**\_ \_ affinité de processeur de socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) qui contient le [**\_ numéro de processeur**](/windows/desktop/api/winnt/ns-winnt-processor_number) et l’ID de nœud NUMA.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-187">This IOCTL returns a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure that contains the [**PROCESSOR\_NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number) and the NUMA node ID.</span></span>
<span data-ttu-id="ad7e7-188">La structure retournée du [**\_ numéro de processeur**](/windows/desktop/api/winnt/ns-winnt-processor_number) contient un numéro de groupe et un numéro de processeur relatif dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-188">The returned [**PROCESSOR\_NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number) structure contains a group number and relative processor number within the group.</span></span>

<span data-ttu-id="ad7e7-189">Si le socket est un socket UDP, le socket doit être connecté pour que l’IOCTL de l’information sur le **\_ \_ \_ processeur \_ RSS de la requête SIO** fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="ad7e7-189">If the socket is a UDP socket, the socket must be connected for the **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL to work properly.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad7e7-190">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad7e7-190">See also</span></span>

[<span data-ttu-id="ad7e7-191">**PROCESSOR_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="ad7e7-191">**PROCESSOR_NUMBER**</span></span>](/windows/desktop/api/winnt/ns-winnt-processor_number)

[<span data-ttu-id="ad7e7-192">**socle**</span><span class="sxs-lookup"><span data-stu-id="ad7e7-192">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="ad7e7-193">**SOCKET_PROCESSOR_AFFINITY**</span><span class="sxs-lookup"><span data-stu-id="ad7e7-193">**SOCKET_PROCESSOR_AFFINITY**</span></span>](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)

[<span data-ttu-id="ad7e7-194">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="ad7e7-194">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="ad7e7-195">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="ad7e7-195">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="ad7e7-196">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="ad7e7-196">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="ad7e7-197">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="ad7e7-197">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="ad7e7-198">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="ad7e7-198">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="ad7e7-199">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="ad7e7-199">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
