---
title: Bluetooth et Socket
description: Crée un socket pour les connexions entrantes ou sortantes.
ms.assetid: 21b9cf1f-1a85-4a4b-9557-faa4f32c3696
keywords:
- Bluetooth Bluetooth
- Bluetooth Socket
- Bluetooth et Bluetooth Socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2c2085ee0c61941bab93ed25dd86f5c102d0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727652"
---
# <a name="bluetooth-and-socket"></a><span data-ttu-id="223ff-106">Bluetooth et Socket</span><span class="sxs-lookup"><span data-stu-id="223ff-106">Bluetooth and socket</span></span>

<span data-ttu-id="223ff-107">La fonction [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) crée un socket pour les connexions entrantes ou sortantes. :</span><span class="sxs-lookup"><span data-stu-id="223ff-107">The [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) function creates a socket for incoming or outgoing connections.:</span></span>

<span data-ttu-id="223ff-108">Pour créer un socket à l’aide de Bluetooth, utilisez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="223ff-108">To create a socket using Bluetooth, use the following settings:</span></span>

-   <span data-ttu-id="223ff-109">Le paramètre *AF* de la fonction [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) est toujours défini sur **AF \_ BTH** pour les sockets Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="223ff-109">The *af* parameter of the [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) function is always set to **AF\_BTH** for Bluetooth sockets.</span></span>
-   <span data-ttu-id="223ff-110">Le paramètre de *type* de la fonction de [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) est toujours un **\_ flux de chaussette**; **Chaussette \_** Les sockets DGRAM ne sont pas pris en charge par Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="223ff-110">The *type* parameter of the [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) function is always **SOCK\_STREAM**; **SOCK\_DGRAM** sockets are not supported by Bluetooth.</span></span>
-   <span data-ttu-id="223ff-111">Pour le paramètre de *protocole* , **BTHPROTO \_ RFCOMM** est le protocole pris en charge.</span><span class="sxs-lookup"><span data-stu-id="223ff-111">For the *protocol* parameter, **BTHPROTO\_RFCOMM** is the supported protocol.</span></span>

<span data-ttu-id="223ff-112">Pour plus d’informations, consultez [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2).</span><span class="sxs-lookup"><span data-stu-id="223ff-112">For more information, see [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2).</span></span>

## <a name="related-topics"></a><span data-ttu-id="223ff-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="223ff-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="223ff-114">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="223ff-114">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="223ff-115">**socle**</span><span class="sxs-lookup"><span data-stu-id="223ff-115">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)
</dt> </dl>

 

 