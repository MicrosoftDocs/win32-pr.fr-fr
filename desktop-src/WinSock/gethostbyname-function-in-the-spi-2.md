---
description: Fonction gethostbyname dans le SPI Winsock.
ms.assetid: 3e63a6db-1ecc-4ce1-b772-25dc9a57e0d9
title: Fonction gethostbyname dans le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a04f39ca00dc712ef7b8ce3bdef480aa253a5b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514178"
---
# <a name="gethostbyname-function-in-the-spi"></a><span data-ttu-id="57a82-103">Fonction gethostbyname dans le SPI</span><span class="sxs-lookup"><span data-stu-id="57a82-103">gethostbyname Function in the SPI</span></span>

<span data-ttu-id="57a82-104">La requête [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) utilise SVCID \_ inet \_ HOSTADDRBYNAME comme GUID de classe de service.</span><span class="sxs-lookup"><span data-stu-id="57a82-104">The [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) query uses SVCID\_INET\_HOSTADDRBYNAME as the service class GUID.</span></span> <span data-ttu-id="57a82-105">Le nom d’hôte est fourni dans *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="57a82-105">The host name is supplied in *lpszServiceInstanceName*.</span></span> <span data-ttu-id="57a82-106">L' *\_32.dllWs2* spécifie \_ lup \_ et le NSP place une structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans l’objet BLOB (à l’aide de décalages au lieu de pointeurs comme décrit ci-dessus).</span><span class="sxs-lookup"><span data-stu-id="57a82-106">The *Ws2\_32.dll* specifies LUP\_RETURN\_BLOB and the NSP places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="57a82-107">Les NSP doivent également honorer ces autres \_ \_ \* indicateurs de retour lup.</span><span class="sxs-lookup"><span data-stu-id="57a82-107">NSPs should honor these other LUP\_RETURN\_\* flags as well.</span></span>



| <span data-ttu-id="57a82-108">Indicateur</span><span class="sxs-lookup"><span data-stu-id="57a82-108">Flag</span></span>              | <span data-ttu-id="57a82-109">Description</span><span class="sxs-lookup"><span data-stu-id="57a82-109">Description</span></span>                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57a82-110">LUP \_ nom de retour \_</span><span class="sxs-lookup"><span data-stu-id="57a82-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="57a82-111">Retourne le membre de **\_ nom h** de la structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="57a82-111">Returns the **h\_name** member from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                                                                                                                            |
| <span data-ttu-id="57a82-112">LUP \_ retour \_ addr</span><span class="sxs-lookup"><span data-stu-id="57a82-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="57a82-113">Retourne les informations d’adressage de [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans les structures d' [**\_ informations CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , les informations de port sont par défaut égales à zéro.</span><span class="sxs-lookup"><span data-stu-id="57a82-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> <span data-ttu-id="57a82-114">Notez que cette routine ne résout pas les noms d’hôtes constitués d’une chaîne d’adresses IPv4 décimales en pointillés.</span><span class="sxs-lookup"><span data-stu-id="57a82-114">Note that this routine does not resolve host names consisting of a dotted-decimal IPv4 address string.</span></span> |



 

 

 
