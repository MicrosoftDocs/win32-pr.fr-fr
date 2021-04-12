---
description: WSPCloseSocket libère le descripteur de socket afin que toutes les opérations en attente dans les threads du même processus soient abandonnées, et toute autre référence à ce dernier échoue.
ms.assetid: 658d0c35-05d4-4b51-a4d3-a3b441a2c735
title: Fermeture de Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d0c877767925f67e07427a77dc8ec8445f30c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526188"
---
# <a name="closing-sockets"></a><span data-ttu-id="915d1-103">Fermeture de Sockets</span><span class="sxs-lookup"><span data-stu-id="915d1-103">Closing Sockets</span></span>

<span data-ttu-id="915d1-104">[**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) libère le descripteur de socket afin que toutes les opérations en attente dans les threads du même processus soient abandonnées, et toute autre référence à ce dernier échoue.</span><span class="sxs-lookup"><span data-stu-id="915d1-104">[**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) releases the socket descriptor so that any pending operations in any threads of the same process will be aborted, and any further reference to it will fail.</span></span> <span data-ttu-id="915d1-105">Notez qu’un décompte de références doit être utilisé pour les sockets partagés et seulement s’il s’agit de la dernière référence à un Socket sous-jacent, si les informations associées à ce Socket doivent être ignorées, à condition que la fermeture normale ne soit pas demandée (autrement dit, \_ DONTLINGER n’est pas défini).</span><span class="sxs-lookup"><span data-stu-id="915d1-105">Note that a reference count should be employed for shared sockets, and only if this is the last reference to an underlying socket, should the information associated with this socket be discarded, provided graceful close is not requested (that is, SO\_DONTLINGER is not set).</span></span> <span data-ttu-id="915d1-106">Dans le cas où \_ DONTLINGER est défini, toutes les données mises en file d’attente pour la transmission sont envoyées, si possible, avant la publication des informations associées au socket.</span><span class="sxs-lookup"><span data-stu-id="915d1-106">In the case of SO\_DONTLINGER being set, any data queued for transmission will be sent, if possible, before information associated with the socket is released.</span></span> <span data-ttu-id="915d1-107">Pour plus d’informations, consultez **WSPCloseSocket** .</span><span class="sxs-lookup"><span data-stu-id="915d1-107">See **WSPCloseSocket** for more information.</span></span>

<span data-ttu-id="915d1-108">Pour les fournisseurs de services nonIFS, [**WPUCloseSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosesockethandle) doit être appelé pour libérer le handle de socket à la dll Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="915d1-108">For nonIFS service providers, [**WPUCloseSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosesockethandle) must be invoked to release the socket handle back to the Windows Sockets 2 DLL.</span></span>

 

 
