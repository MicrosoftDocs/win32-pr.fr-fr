---
description: La requête WSALookupServiceBegin utilise SVCID \_ inet \_ HOSTNAMEBYADDR comme GUID de classe de service.
ms.assetid: 6fd54708-dbd0-4402-8eb8-9cdc42cd56ad
title: Fonction gethostbyaddr dans le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e343bcd66b7b1482f14a07239ae73710fd789486633219952696406dd8f1bd3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132312"
---
# <a name="gethostbyaddr-function-in-the-spi"></a>Fonction gethostbyaddr dans le SPI

La requête [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) utilise SVCID \_ inet \_ HOSTNAMEBYADDR comme GUID de classe de service. L’adresse de l’hôte est fournie dans *lpszServiceInstanceName* sous la forme d’une chaîne d’adresse IPv4 décimale séparée par des points (par exemple, 192.9.200.120). L' *\_32.dllWs2* spécifie \_ lup \_ et le NSP place une structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans l’objet BLOB (à l’aide de décalages au lieu de pointeurs comme décrit ci-dessus). Les NSP doivent également honorer ces autres \_ \_ \* indicateurs de retour lup.



| Indicateur              | Description                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LUP \_ nom de retour \_ | Retourne le membre de **\_ nom h** de la structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans *lpszServiceInstanceName*.                                                     |
| LUP \_ retour \_ addr | Retourne les informations d’adressage de [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans les structures d' [**\_ informations CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , les informations de port sont par défaut égales à zéro. |



 

 

 
