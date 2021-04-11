---
description: Fonction gethostbyname dans l’API Winsock.
ms.assetid: 015637ed-7a3e-49eb-96ef-8fe82d2902f5
title: Fonction gethostbyname dans l’API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3881897a0c971c48ca9a02e6205ec1cae0476f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113075"
---
# <a name="gethostbyname-function-in-the-api"></a><span data-ttu-id="d8f69-103">Fonction gethostbyname dans l’API</span><span class="sxs-lookup"><span data-stu-id="d8f69-103">gethostbyname Function in the API</span></span>

<span data-ttu-id="d8f69-104">La fonction [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) utilise la fonction [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) pour interroger SVCID \_ inet \_ HOSTADDRBYNAME en tant que GUID de classe de service.</span><span class="sxs-lookup"><span data-stu-id="d8f69-104">The [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function uses the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_INET\_HOSTADDRBYNAME as the service class GUID.</span></span> <span data-ttu-id="d8f69-105">Le nom d’hôte est fourni dans le membre **lpszServiceInstanceName** de la structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passée à la fonction **WSALookupServiceBegin** .</span><span class="sxs-lookup"><span data-stu-id="d8f69-105">The host name is supplied in the **lpszServiceInstanceName** member in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function.</span></span> <span data-ttu-id="d8f69-106">Le \_32.dll Ws2 spécifie l' \_ objet blob de retour lup \_ et le fournisseur de services de noms place une structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans l’objet BLOB (en utilisant des décalages au lieu des pointeurs comme décrit ci-dessus).</span><span class="sxs-lookup"><span data-stu-id="d8f69-106">The Ws2\_32.dll specifies LUP\_RETURN\_BLOB and the name service provider places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="d8f69-107">Les fournisseurs de services de noms doivent également respecter ces autres \_ \_ \* indicateurs de retour lup.</span><span class="sxs-lookup"><span data-stu-id="d8f69-107">Name service providers should honor these other LUP\_RETURN\_\* flags as well.</span></span>

| <span data-ttu-id="d8f69-108">Indicateur</span><span class="sxs-lookup"><span data-stu-id="d8f69-108">Flag</span></span>              | <span data-ttu-id="d8f69-109">Description</span><span class="sxs-lookup"><span data-stu-id="d8f69-109">Description</span></span>                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8f69-110">LUP \_ nom de retour \_</span><span class="sxs-lookup"><span data-stu-id="d8f69-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="d8f69-111">Retourne le membre de **\_ nom h** à partir de la structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="d8f69-111">Returns the **h\_name** member from the [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                                                                                                           |
| <span data-ttu-id="d8f69-112">LUP \_ retour \_ addr</span><span class="sxs-lookup"><span data-stu-id="d8f69-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="d8f69-113">Retourne les informations d’adressage de [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans les structures d' [**\_ informations CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , les informations de port sont par défaut égales à zéro.</span><span class="sxs-lookup"><span data-stu-id="d8f69-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> <span data-ttu-id="d8f69-114">Notez que cette routine ne résout pas les noms d’hôte qui se composent d’une adresse IPv4 en pointillés.</span><span class="sxs-lookup"><span data-stu-id="d8f69-114">Note that this routine does not resolve host names that consist of a dotted IPv4 address.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d8f69-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d8f69-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8f69-116">Résolution de noms compatible pour TCP/IP dans l’API Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="d8f69-116">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="d8f69-117">Résolution de noms indépendante du protocole</span><span class="sxs-lookup"><span data-stu-id="d8f69-117">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="d8f69-118">Inscription et résolution de noms</span><span class="sxs-lookup"><span data-stu-id="d8f69-118">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
