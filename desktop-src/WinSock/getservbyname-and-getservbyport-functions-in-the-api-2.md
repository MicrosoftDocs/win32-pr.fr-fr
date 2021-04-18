---
description: Les fonctions getservbyname et getservbyport utilisent la fonction WSALookupServiceBegin pour interroger SVCID \_ inet \_ SERVICEBYNAME en tant que GUID de classe de service.
ms.assetid: 6d4eb1d4-1498-4367-886b-6b08e87bc4a0
title: Fonctions getservbyname et getservbyport dans l’API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0028b9ed090463234d01e2b13191ff2328baf2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519297"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-api"></a><span data-ttu-id="a80bd-103">Fonctions getservbyname et getservbyport dans l’API</span><span class="sxs-lookup"><span data-stu-id="a80bd-103">getservbyname and getservbyport Functions in the API</span></span>

<span data-ttu-id="a80bd-104">Les fonctions [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) et [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) utilisent la fonction [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) pour interroger SVCID \_ inet \_ SERVICEBYNAME en tant que GUID de classe de service.</span><span class="sxs-lookup"><span data-stu-id="a80bd-104">The [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) and [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) functions use the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_INET\_SERVICEBYNAME as the service class GUID.</span></span> <span data-ttu-id="a80bd-105">Le membre *lpszServiceInstanceName* de la structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passé à la fonction **WSALookupServiceBegin** fait référence à une chaîne pour indiquer le nom de service ou le port de service, et (éventuellement) le protocole de service.</span><span class="sxs-lookup"><span data-stu-id="a80bd-105">The *lpszServiceInstanceName* member in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function references a string to indicate the service name or service port, and (optionally) the service protocol.</span></span> <span data-ttu-id="a80bd-106">La mise en forme de la chaîne est illustrée par FTP ou TCP ou 21/TCP ou simplement via FTP.</span><span class="sxs-lookup"><span data-stu-id="a80bd-106">The formatting of the string is illustrated as FTP or TCP or 21/TCP or just FTP.</span></span> <span data-ttu-id="a80bd-107">La chaîne ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="a80bd-107">The string is not case sensitive.</span></span> <span data-ttu-id="a80bd-108">La barre oblique, le cas échéant, sépare l’identificateur de protocole de la partie précédente de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="a80bd-108">The slash mark, if present, separates the protocol identifier from the preceding part of the string.</span></span> <span data-ttu-id="a80bd-109">L' \_32.dll Ws2 spécifie l' \_ objet blob de retour lup \_ et le fournisseur d’espaces de noms place une structure [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) dans l’objet BLOB (en utilisant des décalages au lieu des pointeurs comme décrit ci-dessus).</span><span class="sxs-lookup"><span data-stu-id="a80bd-109">The Ws2\_32.dll will specify LUP\_RETURN\_BLOB and the namespace provider will place a [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="a80bd-110">Les fournisseurs d’espaces de noms doivent également respecter ces autres \_ \_ \* indicateurs de retour lup.</span><span class="sxs-lookup"><span data-stu-id="a80bd-110">Namespace providers should honor these other LUP\_RETURN\_\* flags as well.</span></span>

| <span data-ttu-id="a80bd-111">Indicateur</span><span class="sxs-lookup"><span data-stu-id="a80bd-111">Flag</span></span>              | <span data-ttu-id="a80bd-112">Description</span><span class="sxs-lookup"><span data-stu-id="a80bd-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a80bd-113">LUP \_ nom de retour \_</span><span class="sxs-lookup"><span data-stu-id="a80bd-113">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="a80bd-114">Retourne le **membre \_ Name** de la structure [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) dans *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="a80bd-114">Returns the **s\_name** member from [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure in *lpszServiceInstanceName*.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="a80bd-115">\_type de retour lup \_</span><span class="sxs-lookup"><span data-stu-id="a80bd-115">LUP\_RETURN\_TYPE</span></span> | <span data-ttu-id="a80bd-116">Retourne un GUID canonique dans *lpServiceClassId* . il est entendu qu’un service identifié comme FTP ou 21 peut se trouver sur un autre port conformément aux conventions établies localement.</span><span class="sxs-lookup"><span data-stu-id="a80bd-116">Returns canonical GUID in *lpServiceClassId* It is understood that a service identified as FTP or 21 may be on another port according to locally established conventions.</span></span> <span data-ttu-id="a80bd-117">Le paramètre de **\_ port s** de la structure [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) doit indiquer où le service peut être contacté dans l’environnement local.</span><span class="sxs-lookup"><span data-stu-id="a80bd-117">The **s\_port** parameter of the [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure should indicate where the service can be contacted in the local environment.</span></span> <span data-ttu-id="a80bd-118">Le GUID canonique retourné lorsque le \_ \_ type de retour lup est défini doit être l’un des GUID prédéfinis de svc. h qui correspond au numéro de port indiqué dans la structure **servent** .</span><span class="sxs-lookup"><span data-stu-id="a80bd-118">The canonical GUID returned when LUP\_RETURN\_TYPE is set should be one of the predefined GUIDs from Svcs.h that corresponds to the port number indicated in the **SERVENT** structure.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a80bd-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a80bd-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a80bd-120">Résolution de noms compatible pour TCP/IP dans l’API Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="a80bd-120">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="a80bd-121">Résolution de noms indépendante du protocole</span><span class="sxs-lookup"><span data-stu-id="a80bd-121">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="a80bd-122">Inscription et résolution de noms</span><span class="sxs-lookup"><span data-stu-id="a80bd-122">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



