---
description: La liste suivante fournit des descriptions concises de chaque structure Winsock ATM. Pour plus d’informations sur n’importe quelle structure, cliquez sur le nom de la structure.
ms.assetid: ce80ef1f-9a76-4a6f-a7ce-f166bc46ca08
title: Structures ATM Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf28266de89e5346727a9ad42fdb90d9167bc9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529715"
---
# <a name="winsock-atm-structures"></a><span data-ttu-id="7190e-104">Structures ATM Winsock</span><span class="sxs-lookup"><span data-stu-id="7190e-104">Winsock ATM Structures</span></span>

<span data-ttu-id="7190e-105">La liste suivante fournit des descriptions concises de chaque structure Winsock ATM.</span><span class="sxs-lookup"><span data-stu-id="7190e-105">The following list provides concise descriptions of each Winsock ATM structure.</span></span> <span data-ttu-id="7190e-106">Pour plus d’informations sur n’importe quelle structure, cliquez sur le nom de la structure.</span><span class="sxs-lookup"><span data-stu-id="7190e-106">For additional information on any structure, click the structure name.</span></span>



| <span data-ttu-id="7190e-107">Structure ATM</span><span class="sxs-lookup"><span data-stu-id="7190e-107">ATM Structure</span></span>                           | <span data-ttu-id="7190e-108">Description</span><span class="sxs-lookup"><span data-stu-id="7190e-108">Description</span></span>                                                |
|-----------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="7190e-109">**\_adresse ATM**</span><span class="sxs-lookup"><span data-stu-id="7190e-109">**ATM\_ADDRESS**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_address)   | <span data-ttu-id="7190e-110">Stocke les données d’adresse ATM pour les sockets ATM.</span><span class="sxs-lookup"><span data-stu-id="7190e-110">Stores ATM address data for ATM-based sockets.</span></span>             |
| [<span data-ttu-id="7190e-111">**\_BHLI ATM**</span><span class="sxs-lookup"><span data-stu-id="7190e-111">**ATM\_BHLI**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_bhli)         | <span data-ttu-id="7190e-112">Identifie les informations B-HLI pour un socket ATM associé.</span><span class="sxs-lookup"><span data-stu-id="7190e-112">Identifies B-HLI information for an associated ATM socket.</span></span> |
| [<span data-ttu-id="7190e-113">**\_BLLI ATM**</span><span class="sxs-lookup"><span data-stu-id="7190e-113">**ATM\_BLLI**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_blli)         | <span data-ttu-id="7190e-114">Identifie les informations de B-LLI pour un socket ATM associé.</span><span class="sxs-lookup"><span data-stu-id="7190e-114">Identifies B-LLI information for an associated ATM socket.</span></span> |
| [<span data-ttu-id="7190e-115">**sockaddr \_ ATM**</span><span class="sxs-lookup"><span data-stu-id="7190e-115">**sockaddr\_atm**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) | <span data-ttu-id="7190e-116">Stocke les informations d’adresse de socket pour les sockets ATM.</span><span class="sxs-lookup"><span data-stu-id="7190e-116">Stores socket address information for ATM sockets.</span></span>         |



 

<span data-ttu-id="7190e-117">Pour les services ATM natifs, utilisez \_ le DAB AF pour la famille d’adresses et la structure d’adresse de socket [**\_ ATM sockaddr**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) .</span><span class="sxs-lookup"><span data-stu-id="7190e-117">For native ATM services, use AF\_ATM for address family and the [**sockaddr\_atm**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) socket address structure.</span></span> <span data-ttu-id="7190e-118">Pour ouvrir un socket ATM natif, transmettez AF- \_ ATM, chaussette \_ RAW, ATMPROTO \_ AAL5 ou ATMPROTO \_ AALUSER à la fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="7190e-118">To open a native ATM socket, pass AF\_ATM, SOCK\_RAW, and ATMPROTO\_AAL5 or ATMPROTO\_AALUSER into the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function, respectively.</span></span>

 

 



