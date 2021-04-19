---
description: Le code de contrôle récupère les statistiques TCP (Transmission Control Protocol) pour un socket spécifié.
ms.assetid: AB5F25B6-D2D2-42D7-8189-06CAC4842C66
title: Code de contrôle SIO_TCP_INFO
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: cea9a2d31654d1263f285ee9967b24700fe25138
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106522907"
---
# <a name="sio_tcp_info-control-code"></a><span data-ttu-id="ad5eb-103">Code de contrôle SIO_TCP_INFO</span><span class="sxs-lookup"><span data-stu-id="ad5eb-103">SIO_TCP_INFO Control Code</span></span>

## <a name="description"></a><span data-ttu-id="ad5eb-104">Description</span><span class="sxs-lookup"><span data-stu-id="ad5eb-104">Description</span></span>

<span data-ttu-id="ad5eb-105">Le code de contrôle d' **\_ \_ informations TCP SIO** récupère les statistiques TCP (Transmission Control Protocol) pour un socket spécifié.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-105">The **SIO\_TCP\_INFO** control code retrieves the Transmission Control Protocol (TCP) statistics for a specified socket.</span></span>

<span data-ttu-id="ad5eb-106">Pour effectuer cette opération, appelez la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INFO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a DWORD
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to a TCP_INFO_v0 structure
  (DWORD) cbOutBuffer,       // size of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INFO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a DWORD
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to a TCP_INFO_v0 structure
  (DWORD) cbOutBuffer,       // size of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="ad5eb-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad5eb-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="ad5eb-108">s</span><span class="sxs-lookup"><span data-stu-id="ad5eb-108">s</span></span>

<span data-ttu-id="ad5eb-109">Descripteur qui identifie un Socket.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-109">A descriptor that identifies a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="ad5eb-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="ad5eb-110">dwIoControlCode</span></span>

<span data-ttu-id="ad5eb-111">Code de contrôle de l’opération.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-111">The control code for the operation.</span></span>
<span data-ttu-id="ad5eb-112">Utilisez **les \_ \_ informations TCP SIO** pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-112">Use **SIO\_TCP\_INFO** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="ad5eb-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="ad5eb-113">lpvInBuffer</span></span>

<span data-ttu-id="ad5eb-114">Pointeur vers la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="ad5eb-115">Ce paramètre contient un pointeur vers une **valeur DWORD** qui spécifie la version du code de contrôle d' **\_ \_ informations TCP SIO** que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-115">This parameter contains a pointer to a **DWORD** that specifies the version of the **SIO\_TCP\_INFO** control code that you are using.</span></span> <span data-ttu-id="ad5eb-116">Spécifiez 0 pour utiliser [TCP_INFO_v0](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0).</span><span class="sxs-lookup"><span data-stu-id="ad5eb-116">Specify 0 to use [TCP_INFO_v0](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0).</span></span> <span data-ttu-id="ad5eb-117">Spécifiez 1 pour utiliser [TCP_INFO_v1](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1), qui povides plus de champs.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-117">Specify 1 to use [TCP_INFO_v1](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1), which povides more fields.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="ad5eb-118">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="ad5eb-118">cbInBuffer</span></span>

<span data-ttu-id="ad5eb-119">Taille, en octets, de la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-119">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="ad5eb-120">Ce paramètre doit correspondre à la taille du type de données **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="ad5eb-120">This parameter should be the size of the **DWORD** data type.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="ad5eb-121">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="ad5eb-121">lpvOutBuffer</span></span>

<span data-ttu-id="ad5eb-122">Pointeur vers la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-122">A pointer to the output buffer.</span></span>
<span data-ttu-id="ad5eb-123">En cas de sortie réussie, ce paramètre contient un pointeur vers une structure [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) qui contient les statistiques TCP pour le socket spécifié.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-123">On successful output, this parameter contains a pointer to a [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) structure that contains the TCP statistics for the specified socket.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="ad5eb-124">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="ad5eb-124">cbOutBuffer</span></span>

<span data-ttu-id="ad5eb-125">Taille, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-125">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="ad5eb-126">Ce paramètre doit avoir au moins la taille de la structure [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) .</span><span class="sxs-lookup"><span data-stu-id="ad5eb-126">This parameter must be at least the size of the [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) structure.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="ad5eb-127">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="ad5eb-127">lpcbBytesReturned</span></span>

<span data-ttu-id="ad5eb-128">Pointeur vers une variable qui reçoit la taille, en octets, des données stockées dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-128">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="ad5eb-129">Si la mémoire tampon de sortie est trop petite, l’appel échoue, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne [**WSAEINVAL**](windows-sockets-error-codes-2.md)et le paramètre *LpcbBytesReturned* pointe vers une valeur **DWORD** égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-129">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="ad5eb-130">Si *lpOverlapped* a la valeur **null**, la valeur **DWORD** vers laquelle pointe le paramètre *lpcbBytesReturned* retourné sur un appel réussi ne peut pas être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-130">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="ad5eb-131">Si le paramètre *lpOverlapped* n’a pas la **valeur null** pour les sockets superposés, les opérations qui ne peuvent pas être terminées immédiatement seront lancées et l’achèvement sera indiqué ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-131">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="ad5eb-132">La valeur **DWORD** pointée par le paramètre *lpcbBytesReturned* retourné peut être égale à zéro, car la taille des données stockées ne peut pas être déterminée tant que l’opération avec chevauchement n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-132">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="ad5eb-133">L’état d’achèvement final peut être récupéré lorsque la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-133">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="ad5eb-134">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="ad5eb-134">lpvOverlapped</span></span>

<span data-ttu-id="ad5eb-135">Pointeur vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="ad5eb-135">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="ad5eb-136">Si le socket *s* a été créé sans l’attribut Overlapped, le paramètre *lpOverlapped* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-136">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="ad5eb-137">Si *s* a été ouvert avec l’attribut Overlapped et que le paramètre *lpOverlapped* n’a pas la **valeur null**, l’opération est exécutée en tant qu’opération Overlapped (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="ad5eb-137">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="ad5eb-138">Dans ce cas, le paramètre *lpOverlapped* doit pointer vers une structure [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valide.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-138">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="ad5eb-139">Pour les opérations avec chevauchement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne immédiatement, et la méthode d’achèvement appropriée est signalée lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-139">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="ad5eb-140">Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-140">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="ad5eb-141">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="ad5eb-141">lpCompletionRoutine</span></span>

<span data-ttu-id="ad5eb-142">Type : \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="ad5eb-142">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="ad5eb-143">Pointeur vers la routine de saisie semi-automatique appelée lorsque l’opération est terminée (ignoré pour les sockets non superposés).</span><span class="sxs-lookup"><span data-stu-id="ad5eb-143">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="ad5eb-144">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="ad5eb-144">lpThreadId</span></span>

<span data-ttu-id="ad5eb-145">Pointeur vers une structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) qui doit être utilisée par le fournisseur dans un appel ultérieur à [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="ad5eb-145">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="ad5eb-146">Le fournisseur doit stocker la structure [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) référencée (pas le pointeur vers le même) jusqu’à ce que la fonction [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) soit retournée.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-146">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="ad5eb-147">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="ad5eb-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="ad5eb-148">lpErrno</span><span class="sxs-lookup"><span data-stu-id="ad5eb-148">lpErrno</span></span>

<span data-ttu-id="ad5eb-149">Pointeur vers le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-149">A pointer to the error code.</span></span>

<span data-ttu-id="ad5eb-150">**Remarque**  Ce paramètre s’applique uniquement à la fonction **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="ad5eb-150">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="ad5eb-151">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ad5eb-151">Return value</span></span>

<span data-ttu-id="ad5eb-152">Si l’opération se termine correctement, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-152">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="ad5eb-153">Si l’opération échoue ou est en attente, la fonction [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retourne une **\_ erreur de socket**.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-153">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="ad5eb-154">Pour afficher les informations d’erreur étendues, appelez [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="ad5eb-154">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="ad5eb-155">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="ad5eb-155">Error code</span></span> | <span data-ttu-id="ad5eb-156">Signification</span><span class="sxs-lookup"><span data-stu-id="ad5eb-156">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="ad5eb-157">**WSAEMSGSIZE**</span><span class="sxs-lookup"><span data-stu-id="ad5eb-157">**WSAEMSGSIZE**</span></span> | <span data-ttu-id="ad5eb-158">Le pointeur vers la mémoire tampon d’entrée a la **valeur null**, ou la taille spécifiée de la mémoire tampon d’entrée est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-158">The pointer to the input buffer was **NULL**, or the specified size of the input buffer was not correct.</span></span> |
| <span data-ttu-id="ad5eb-159">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="ad5eb-159">**WSAEINVAL**</span></span> | <span data-ttu-id="ad5eb-160">Argument non valide fourni.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-160">An invalid argument was supplied.</span></span> <span data-ttu-id="ad5eb-161">Cette erreur est retournée si le paramètre *dwIoControlCode* n’est pas une commande valide, si un paramètre d’entrée spécifié n’est pas acceptable ou si la commande n’est pas applicable au type de socket spécifié.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-161">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |

## <a name="remarks"></a><span data-ttu-id="ad5eb-162">Notes</span><span class="sxs-lookup"><span data-stu-id="ad5eb-162">Remarks</span></span>

<span data-ttu-id="ad5eb-163">Contrairement à la récupération des statistiques TCP avec la fonction [**GetPerTcpConnectionEStats**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) , la récupération des statistiques TCP avec ce code de contrôle ne nécessite pas que le code utilisateur charge, stocke et filtre la table de connexion TCP et ne nécessite pas de privilèges élevés pour utiliser.</span><span class="sxs-lookup"><span data-stu-id="ad5eb-163">Unlike retrieving TCP statistics with the [**GetPerTcpConnectionEStats**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) function, retrieving TCP statistics with this control code does not require the user code to load, store, and filter the TCP connection table, and does not require elevated privileges to use.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad5eb-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad5eb-164">See also</span></span>

[<span data-ttu-id="ad5eb-165">socle</span><span class="sxs-lookup"><span data-stu-id="ad5eb-165">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="ad5eb-166">**TCP_INFO_v0**</span><span class="sxs-lookup"><span data-stu-id="ad5eb-166">**TCP_INFO_v0**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0)

[<span data-ttu-id="ad5eb-167">**GetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="ad5eb-167">**GetPerTcpConnectionEStats**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats)

[<span data-ttu-id="ad5eb-168">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="ad5eb-168">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="ad5eb-169">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="ad5eb-169">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="ad5eb-170">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="ad5eb-170">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="ad5eb-171">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="ad5eb-171">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="ad5eb-172">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="ad5eb-172">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="ad5eb-173">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="ad5eb-173">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
