---
description: La fonction gethostbyaddr utilise la fonction WSALookupServiceBegin pour interroger SVCID \_ inet \_ HOSTNAMEBYADDR en tant que GUID de classe de service.
ms.assetid: 9b1e3f3f-bfc0-4099-b699-af56019055e6
title: Fonction gethostbyaddr dans l’API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04141d65161831a60ec663f0dee4a9647792ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515848"
---
# <a name="gethostbyaddr-function-in-the-api"></a><span data-ttu-id="225cb-103">Fonction gethostbyaddr dans l’API</span><span class="sxs-lookup"><span data-stu-id="225cb-103">gethostbyaddr Function in the API</span></span>

<span data-ttu-id="225cb-104">La fonction [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) utilise la fonction [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) pour interroger SVCID \_ inet \_ HOSTNAMEBYADDR en tant que GUID de classe de service.</span><span class="sxs-lookup"><span data-stu-id="225cb-104">The [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) function uses the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_INET\_HOSTNAMEBYADDR as the service class GUID.</span></span> <span data-ttu-id="225cb-105">L’adresse de l’hôte est fournie sous la forme d’une chaîne IPv4 decimnal séparée par des points (par exemple, « 192.9.200.120 ») dans le membre *lpszServiceInstanceName* de la structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) transmise à la fonction **WSALookupServiceBegin** .</span><span class="sxs-lookup"><span data-stu-id="225cb-105">The host address is supplied as a dotted decimnal IPv4 string (for example, "192.9.200.120") in the *lpszServiceInstanceName* member of the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function.</span></span> <span data-ttu-id="225cb-106">Le \_32.dll Ws2 spécifie l' \_ objet blob de retour lup \_ et le fournisseur de services de noms place une structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans l’objet BLOB (en utilisant des décalages au lieu des pointeurs comme décrit ci-dessus).</span><span class="sxs-lookup"><span data-stu-id="225cb-106">The Ws2\_32.dll specifies LUP\_RETURN\_BLOB and the name service provider places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="225cb-107">Les fournisseurs de services de noms doivent également respecter ces autres \_ \_ \* indicateurs de retour lup.</span><span class="sxs-lookup"><span data-stu-id="225cb-107">Name service providers should honor these other LUP\_RETURN\_\* flags as well.</span></span> 

| <span data-ttu-id="225cb-108">Indicateur</span><span class="sxs-lookup"><span data-stu-id="225cb-108">Flag</span></span>              | <span data-ttu-id="225cb-109">Description</span><span class="sxs-lookup"><span data-stu-id="225cb-109">Description</span></span>                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="225cb-110">LUP \_ nom de retour \_</span><span class="sxs-lookup"><span data-stu-id="225cb-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="225cb-111">Retourne le membre de **\_ nom h** de la structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="225cb-111">Returns the **h\_name** member from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                     |
| <span data-ttu-id="225cb-112">LUP \_ retour \_ addr</span><span class="sxs-lookup"><span data-stu-id="225cb-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="225cb-113">Retourne les informations d’adressage de [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans les structures d' [**\_ informations CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , les informations de port sont par défaut égales à zéro.</span><span class="sxs-lookup"><span data-stu-id="225cb-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="225cb-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="225cb-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="225cb-115">Résolution de noms compatible pour TCP/IP dans l’API Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="225cb-115">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="225cb-116">Résolution de noms indépendante du protocole</span><span class="sxs-lookup"><span data-stu-id="225cb-116">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="225cb-117">Inscription et résolution de noms</span><span class="sxs-lookup"><span data-stu-id="225cb-117">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
