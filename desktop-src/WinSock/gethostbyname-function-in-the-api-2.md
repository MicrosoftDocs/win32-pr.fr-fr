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
# <a name="gethostbyname-function-in-the-api"></a>Fonction gethostbyname dans l’API

La fonction [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) utilise la fonction [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) pour interroger SVCID \_ inet \_ HOSTADDRBYNAME en tant que GUID de classe de service. Le nom d’hôte est fourni dans le membre **lpszServiceInstanceName** de la structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passée à la fonction **WSALookupServiceBegin** . Le \_32.dll Ws2 spécifie l' \_ objet blob de retour lup \_ et le fournisseur de services de noms place une structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans l’objet BLOB (en utilisant des décalages au lieu des pointeurs comme décrit ci-dessus). Les fournisseurs de services de noms doivent également respecter ces autres \_ \_ \* indicateurs de retour lup.

| Indicateur              | Description                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LUP \_ nom de retour \_ | Retourne le membre de **\_ nom h** à partir de la structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans *lpszServiceInstanceName*.                                                                                                                                           |
| LUP \_ retour \_ addr | Retourne les informations d’adressage de [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans les structures d' [**\_ informations CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , les informations de port sont par défaut égales à zéro. Notez que cette routine ne résout pas les noms d’hôte qui se composent d’une adresse IPv4 en pointillés. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution de noms compatible pour TCP/IP dans l’API Windows Sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Résolution de noms indépendante du protocole](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Inscription et résolution de noms](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
