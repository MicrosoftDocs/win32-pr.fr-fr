---
description: Un thread peut, à tout moment, appeler WSAIsBlocking pour déterminer si un appel bloquant est actuellement en cours.
ms.assetid: 6213ded4-feab-404f-86a0-3db9a0a42769
title: Annulation des opérations bloquantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 502870b8935dc97c1d6c3714808d1c6532780f7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536968"
---
# <a name="canceling-blocking-operations"></a><span data-ttu-id="a721b-103">Annulation des opérations bloquantes</span><span class="sxs-lookup"><span data-stu-id="a721b-103">Canceling Blocking Operations</span></span>

<span data-ttu-id="a721b-104">Un thread peut, à tout moment, appeler [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) pour déterminer si un appel bloquant est actuellement en cours.</span><span class="sxs-lookup"><span data-stu-id="a721b-104">A thread may, at any time, call [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) to determine whether or not a blocking call is currently in progress.</span></span> <span data-ttu-id="a721b-105">(Cette fonction est implémentée dans les shims de compatibilité Windows Sockets 1,1 et n’a donc aucun équivalent SPI.) Cela est clairement possible uniquement lorsque le Pseudo-blocage, par opposition au blocage réel, est utilisé par le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="a721b-105">(This function is implemented within the Windows Sockets 1.1 compatibility shims and hence has no SPI counterpart.) Clearly this is only possible when pseudo blocking, as opposed to true blocking, is being employed by the service provider.</span></span> <span data-ttu-id="a721b-106">Si nécessaire, [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) peut être appelé à tout moment pour annuler une opération de Pseudo-blocage en cours.</span><span class="sxs-lookup"><span data-stu-id="a721b-106">When necessary, [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) may be called at any time to cancel any current pseudo blocking operation.</span></span>

 

 
