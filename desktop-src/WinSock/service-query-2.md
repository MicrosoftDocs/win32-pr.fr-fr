---
description: Requête de nom de service dans Windows Sockets (Winsock).
ms.assetid: 94d77f7b-824a-4686-b270-9c662976bbc0
title: Requête de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951ad1950c0f1d97ab0ca6d06f79ed6ff0180d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034314"
---
# <a name="service-query"></a>Requête de service

-   [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)
-   [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext)
-   [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend)

Une requête de service de nom implique une série d’appels : [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin), suivie d’un ou plusieurs appels à [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) et se terminant par un appel à [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend). [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) prend une structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) comme entrée afin de définir les paramètres de requête avec un ensemble d’indicateurs pour fournir un contrôle supplémentaire sur l’opération de recherche. Elle retourne un handle de requête qui est utilisé dans les appels suivants à **NSPLookupServiceNext** et **NSPLookupServiceEnd**.

Le client SPI d’espace de noms appelle [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) pour obtenir les résultats de la requête, avec les résultats fournis dans une mémoire tampon [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fournie par le client. Le client continue d’appeler **NSPLookupServiceNext** jusqu’à ce que le code d’erreur « wsa \_ E » \_ \_ soit retourné, indiquant que tous les résultats ont été récupérés. La recherche est ensuite terminée par un appel à [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend). La fonction **NSPLookupServiceEnd** peut également être utilisée pour annuler un **NSPLookupServiceNext** actuellement en attente en cas d’appel à partir d’un autre thread.

Dans Windows Sockets 2, les codes d’erreur en conflit sont définis pour WSAENOMORE (10102) et WSA \_ E \_ \_ (10110). Le code d’erreur WSAENOMORE sera supprimé dans une version ultérieure et seul le WSA \_ E ne \_ \_ sera pas conservé. Les fournisseurs d’espaces de noms doivent passer à l’utilisation du WSA \_ E \_ \_ plus de code d’erreur dès que possible pour maintenir la compatibilité avec la plus grande plage possible d’applications.

 

 



