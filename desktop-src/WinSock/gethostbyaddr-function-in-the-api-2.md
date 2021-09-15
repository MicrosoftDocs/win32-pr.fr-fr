---
description: La fonction gethostbyaddr utilise la fonction WSALookupServiceBegin pour interroger SVCID \_ inet \_ HOSTNAMEBYADDR en tant que GUID de classe de service.
ms.assetid: 9b1e3f3f-bfc0-4099-b699-af56019055e6
title: Fonction gethostbyaddr dans l’API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04141d65161831a60ec663f0dee4a9647792ff6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517701"
---
# <a name="gethostbyaddr-function-in-the-api"></a>Fonction gethostbyaddr dans l’API

La fonction [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) utilise la fonction [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) pour interroger SVCID \_ inet \_ HOSTNAMEBYADDR en tant que GUID de classe de service. L’adresse de l’hôte est fournie sous la forme d’une chaîne IPv4 decimnal séparée par des points (par exemple, « 192.9.200.120 ») dans le membre *lpszServiceInstanceName* de la structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) transmise à la fonction **WSALookupServiceBegin** . Le \_32.dll Ws2 spécifie l' \_ objet blob de retour lup \_ et le fournisseur de services de noms place une structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans l’objet BLOB (en utilisant des décalages au lieu des pointeurs comme décrit ci-dessus). Les fournisseurs de services de noms doivent également respecter ces autres \_ \_ \* indicateurs de retour lup. 

| Indicateur              | Description                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LUP \_ nom de retour \_ | Retourne le membre de **\_ nom h** de la structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans *lpszServiceInstanceName*.                                                     |
| LUP \_ retour \_ addr | Retourne les informations d’adressage de [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans les structures d' [**\_ informations CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , les informations de port sont par défaut égales à zéro. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[résolution de noms Compatible pour TCP/IP dans l’API Windows sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Résolution de noms indépendante du protocole](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Inscription et résolution de noms](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
