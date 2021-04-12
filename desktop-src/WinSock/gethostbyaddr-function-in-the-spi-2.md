---
description: La requête WSALookupServiceBegin utilise SVCID \_ inet \_ HOSTNAMEBYADDR comme GUID de classe de service.
ms.assetid: 6fd54708-dbd0-4402-8eb8-9cdc42cd56ad
title: Fonction gethostbyaddr dans le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c94f4cdead3a19814e535e2dee80dfdcd0c9fa26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526170"
---
# <a name="gethostbyaddr-function-in-the-spi"></a><span data-ttu-id="19cd7-103">Fonction gethostbyaddr dans le SPI</span><span class="sxs-lookup"><span data-stu-id="19cd7-103">gethostbyaddr Function in the SPI</span></span>

<span data-ttu-id="19cd7-104">La requête [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) utilise SVCID \_ inet \_ HOSTNAMEBYADDR comme GUID de classe de service.</span><span class="sxs-lookup"><span data-stu-id="19cd7-104">The [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) query uses SVCID\_INET\_HOSTNAMEBYADDR as the service class GUID.</span></span> <span data-ttu-id="19cd7-105">L’adresse de l’hôte est fournie dans *lpszServiceInstanceName* sous la forme d’une chaîne d’adresse IPv4 décimale séparée par des points (par exemple, 192.9.200.120).</span><span class="sxs-lookup"><span data-stu-id="19cd7-105">The host address is supplied in *lpszServiceInstanceName* as a dotted-decimal IPv4 address string (for example, 192.9.200.120).</span></span> <span data-ttu-id="19cd7-106">L' *\_32.dllWs2* spécifie \_ lup \_ et le NSP place une structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans l’objet BLOB (à l’aide de décalages au lieu de pointeurs comme décrit ci-dessus).</span><span class="sxs-lookup"><span data-stu-id="19cd7-106">The *Ws2\_32.dll* specifies LUP\_RETURN\_BLOB and the NSP places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="19cd7-107">Les NSP doivent également honorer ces autres \_ \_ \* indicateurs de retour lup.</span><span class="sxs-lookup"><span data-stu-id="19cd7-107">NSPs should honor these other LUP\_RETURN\_\* flags as well.</span></span>



| <span data-ttu-id="19cd7-108">Indicateur</span><span class="sxs-lookup"><span data-stu-id="19cd7-108">Flag</span></span>              | <span data-ttu-id="19cd7-109">Description</span><span class="sxs-lookup"><span data-stu-id="19cd7-109">Description</span></span>                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19cd7-110">LUP \_ nom de retour \_</span><span class="sxs-lookup"><span data-stu-id="19cd7-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="19cd7-111">Retourne le membre de **\_ nom h** de la structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="19cd7-111">Returns the **h\_name** member from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                     |
| <span data-ttu-id="19cd7-112">LUP \_ retour \_ addr</span><span class="sxs-lookup"><span data-stu-id="19cd7-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="19cd7-113">Retourne les informations d’adressage de [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans les structures d' [**\_ informations CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , les informations de port sont par défaut égales à zéro.</span><span class="sxs-lookup"><span data-stu-id="19cd7-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> |



 

 

 
