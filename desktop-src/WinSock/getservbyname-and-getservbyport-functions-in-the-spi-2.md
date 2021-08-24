---
description: La requête WSALookupServiceBegin utilise SVCID \_ inet \_ SERVICEBYNAME comme GUID de classe de service.
ms.assetid: 72ee4a10-2864-48e3-a72c-ae069eb5aef3
title: Fonctions getservbyname et getservbyport dans l’index SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 466966db2fc605b4043355746a1e606626e3d5d518452d1fab661dcfb68b3238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132162"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-spi"></a>Fonctions getservbyname et getservbyport dans l’index SPI

La requête [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) utilise SVCID \_ inet \_ SERVICEBYNAME comme GUID de classe de service. Le paramètre *lpszServiceInstanceName* fait référence à une chaîne qui indique le nom de service ou le port de service, et (éventuellement) le protocole de service. La mise en forme de la chaîne est illustrée par FTP/TCP ou 21/TCP ou simplement via FTP. La chaîne ne respecte pas la casse. La barre oblique, le cas échéant, sépare l’identificateur de protocole de la partie précédente de la chaîne. Le \_32.dll Ws2 spécifie l' \_ objet blob de retour lup \_ et le NSP place une structure [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) dans l’objet BLOB (à l’aide de décalages à la place des pointeurs comme décrit ci-dessus). Les NSP doivent également honorer ces autres \_ \_ \* indicateurs de retour lup.



| Indicateur              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LUP \_ nom de retour \_ | Retourne le **membre \_ Name** de la structure [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) dans *lpszServiceInstanceName*.                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_type de retour lup \_ | Retourne un GUID canonique dans *lpServiceClassId* . il est entendu qu’un service identifié comme FTP ou 21 peut se trouver sur un autre port conformément aux conventions établies localement. Le membre de **\_ port s** de la structure [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) doit indiquer l’emplacement où le service peut être contacté dans l’environnement local. Le GUID canonique retourné lorsque le \_ \_ type de retour lup est défini doit être l’un des GUID prédéfinis de svc. h qui correspond au numéro de port indiqué dans la structure **servent** . |



 

 

 



