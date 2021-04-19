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
# <a name="gethostbyname-function-in-the-spi"></a>Fonction gethostbyname dans le SPI

La requête [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) utilise SVCID \_ inet \_ HOSTADDRBYNAME comme GUID de classe de service. Le nom d’hôte est fourni dans *lpszServiceInstanceName*. L' *\_32.dllWs2* spécifie \_ lup \_ et le NSP place une structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans l’objet BLOB (à l’aide de décalages au lieu de pointeurs comme décrit ci-dessus). Les NSP doivent également honorer ces autres \_ \_ \* indicateurs de retour lup.



| Indicateur              | Description                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LUP \_ nom de retour \_ | Retourne le membre de **\_ nom h** de la structure [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans *lpszServiceInstanceName*.                                                                                                                                                            |
| LUP \_ retour \_ addr | Retourne les informations d’adressage de [**Hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) dans les structures d' [**\_ informations CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , les informations de port sont par défaut égales à zéro. Notez que cette routine ne résout pas les noms d’hôtes constitués d’une chaîne d’adresses IPv4 décimales en pointillés. |



 

 

 
