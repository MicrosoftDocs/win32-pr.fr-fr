---
title: Bluetooth et WSAQUERYSET pour la consultation des appareils
description: utilisé pour faciliter la découverte des appareils et services dans l’espace de noms Bluetooth, NS \_ BTH.
ms.assetid: 0c0d26f7-b6c3-42a9-8c01-118278c381cc
keywords:
- Bluetooth et WSAQUERYSET pour la consultation des appareils Bluetooth
- WSAQUERYSET Bluetooth, pour la consultation de l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a9250670fda52f2ecdc27ffee949b12049b8ec2860b7ee2df23631c4469076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959278"
---
# <a name="bluetooth-and-wsaqueryset-for-device-inquiry"></a>Bluetooth et WSAQUERYSET pour la consultation des appareils

dans Bluetooth, la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) est utilisée pour faciliter la découverte des appareils et des services dans l’espace de noms Bluetooth, NS \_ BTH.

Les fonctions [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) et [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) utilisent la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) pour obtenir des informations sur le processus de demande de l’appareil. Le tableau suivant répertorie et décrit les valeurs de membre dans la structure **WSAQUERYSET** .

| Membre                      | Entrée dans WSALookupServiceBegin avec des \_ conteneurs lup spécifiés                                                                                                                                              | Valeur retournée par WSALookupServiceNext                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize nul**                  | Doit être défini sur **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)).                                                                                                                                       | **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)) retourné par System.                                                                                                                                                                                                                                                                                                                                                        |
| **dwOutputFlags**           | Non utilisé.                                                                                                                                                                                                  | Peut avoir un ou plusieurs de ces indicateurs définis : **BTHNS \_ result \_ Device \_ Connected** spécifie que l’appareil est connecté.<br/> **BTHNS \_ RÉSULTAT de l' \_ appareil \_ mémorisé** spécifie que l’appareil est un appareil mémorisé. Tous les appareils mémorisés ne sont pas authentifiés.<br/> **BTHNS \_ RÉSULTAT de l' \_ \_ authentification** de l’appareil : spécifie que l’appareil est authentifié, couplé ou lié. Tous les appareils authentifiés sont mémorisés.<br/> |
| **lpszServiceInstanceName** | Non utilisé.                                                                                                                                                                                                  | nom complet de l’appareil, retourné à l’origine à partir d’une opération de demande de nom distant Bluetooth et éventuellement mis à jour par l’utilisateur local. Retourné si **lup \_ Return \_ Name** est spécifié.                                                                                                                                                                                                                                         |
| **lpServiceClassId**        | Non utilisé.                                                                                                                                                                                                  | le champ de la classe de l’appareil Bluetooth 32 bits (COD) mappé au membre **Data1** du GUID. Retourné si **le \_ \_ type de retour lup** est spécifié.                                                                                                                                                                                                                                                                                    |
| **lpVersion**               | Non utilisé.                                                                                                                                                                                                  | Non utilisé.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszComment**             | Non utilisé.                                                                                                                                                                                                  | Non utilisé.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNameSpace**             | Doit être NS \_ BTH.                                                                                                                                                                                           | Retourne **le \_ BTH NS**.                                                                                                                                                                                                                                                                                                                                                                                                            |
| **lpNSProviderId**          | Non utilisé.                                                                                                                                                                                                  | Non utilisé.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszContext**             | Non utilisé.                                                                                                                                                                                                  | Non utilisé.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNumberOfProtocols**     | Non utilisé.                                                                                                                                                                                                  | Non utilisé.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpafpProtocols**          | Non utilisé.                                                                                                                                                                                                  | Non utilisé.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszQueryString**         | Non utilisé.                                                                                                                                                                                                  | Non utilisé.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNumberOfCsAddrs**       | Non utilisé.                                                                                                                                                                                                  | Indique le nombre d’éléments dans le tableau de structures d' [**\_ informations CSADDR**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info) .                                                                                                                                                                                                                                                                                                                          |
| **lpcsaBuffer**             | Non utilisé.                                                                                                                                                                                                  | Pointeur vers une structure d' [**\_ informations CSADDR**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info) avec son membre **LocalAddr. lpSockaddr** pointant vers une structure [**sockaddr \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) avec l’adresse du périphérique distant. Retourné si **lup \_ renvoie \_ addr** est spécifié.                                                                                                                                                                  |
| **lpBlob**                  | Facultatif. Peut pointer vers une structure d' [**objet BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) qui pointe vers une structure d' [**\_ \_ appareil de requête BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) qui peut limiter la longueur des opérations de recherche de périphérique non mises en cache. | Pointeur vers une structure [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) qui pointe vers une structure d' [**\_ \_ informations d’appareil BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) . **lpBlob** est retourné si **l' \_ \_ objet blob de retour lup** est spécifié. Spécifiez le **\_ \_ nom de retour lup** pour récupérer le champ nom des **\_ \_ informations sur l’appareil BTH**.                                                                                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Bluetooth et WSAQUERYSET pour Set Service](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[Bluetooth et WSAQUERYSET pour la recherche de Service](bluetooth-and-wsaqueryset-for-service-inquiry.md)
</dt> <dt>

[Bluetooth et objet BLOB](bluetooth-and-blob.md)
</dt> <dt>

[Bluetooth et WSALookupServiceBegin](bluetooth-and-wsasetservice.md)
</dt> <dt>

[Bluetooth et WSALookupServiceNext](bluetooth-and-wsasetservice.md)
</dt> <dt>

[**OBJET BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**\_informations sur l’appareil BTH \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)
</dt> <dt>

[**\_périphérique de requête BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**\_informations CSADDR**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

