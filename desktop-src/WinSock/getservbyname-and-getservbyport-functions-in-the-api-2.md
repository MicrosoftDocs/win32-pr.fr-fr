---
description: Les fonctions getservbyname et getservbyport utilisent la fonction WSALookupServiceBegin pour interroger SVCID \_ inet \_ SERVICEBYNAME en tant que GUID de classe de service.
ms.assetid: 6d4eb1d4-1498-4367-886b-6b08e87bc4a0
title: Fonctions getservbyname et getservbyport dans l’API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0028b9ed090463234d01e2b13191ff2328baf2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517693"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-api"></a>Fonctions getservbyname et getservbyport dans l’API

Les fonctions [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) et [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) utilisent la fonction [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) pour interroger SVCID \_ inet \_ SERVICEBYNAME en tant que GUID de classe de service. Le membre *lpszServiceInstanceName* de la structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passé à la fonction **WSALookupServiceBegin** fait référence à une chaîne pour indiquer le nom de service ou le port de service, et (éventuellement) le protocole de service. La mise en forme de la chaîne est illustrée par FTP ou TCP ou 21/TCP ou simplement via FTP. La chaîne ne respecte pas la casse. La barre oblique, le cas échéant, sépare l’identificateur de protocole de la partie précédente de la chaîne. L' \_32.dll Ws2 spécifie l' \_ objet blob de retour lup \_ et le fournisseur d’espaces de noms place une structure [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) dans l’objet BLOB (en utilisant des décalages au lieu des pointeurs comme décrit ci-dessus). Les fournisseurs d’espaces de noms doivent également respecter ces autres \_ \_ \* indicateurs de retour lup.

| Indicateur              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LUP \_ nom de retour \_ | Retourne le **membre \_ Name** de la structure [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) dans *lpszServiceInstanceName*.                                                                                                                                                                                                                                                                                                                                                                                                               |
| \_type de retour lup \_ | Retourne un GUID canonique dans *lpServiceClassId* . il est entendu qu’un service identifié comme FTP ou 21 peut se trouver sur un autre port conformément aux conventions établies localement. Le paramètre de **\_ port s** de la structure [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) doit indiquer où le service peut être contacté dans l’environnement local. Le GUID canonique retourné lorsque le \_ \_ type de retour lup est défini doit être l’un des GUID prédéfinis de svc. h qui correspond au numéro de port indiqué dans la structure **servent** . |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[résolution de noms Compatible pour TCP/IP dans l’API Windows sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Résolution de noms indépendante du protocole](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Inscription et résolution de noms](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



