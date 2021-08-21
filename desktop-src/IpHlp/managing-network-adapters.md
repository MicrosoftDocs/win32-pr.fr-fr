---
description: L’assistance IP fournit des fonctionnalités pour la gestion des cartes réseau. Il existe une correspondance un-à-un entre les interfaces et les adaptateurs sur un ordinateur donné. Une interface est une abstraction au niveau de l’adresse IP, alors qu’un adaptateur est une abstraction de niveau de liaison de liaison.
ms.assetid: fbb32941-2add-4f74-90c4-1dc1bfebd64c
title: Gestion des cartes réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1e1fd02426b27e3c07d4634edbe0215efa1c5c25c7a9c3abde32e991f766daf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078259"
---
# <a name="managing-network-adapters"></a>Gestion des cartes réseau

L’assistance IP fournit des fonctionnalités pour la gestion des cartes réseau. Il existe une correspondance un-à-un entre les interfaces et les adaptateurs sur un ordinateur donné. Une interface est une abstraction au niveau de l’adresse IP, alors qu’un adaptateur est une abstraction de niveau de liaison de liaison.

Utilisez les fonctions décrites dans les paragraphes suivants pour récupérer des informations sur les cartes réseau de l’ordinateur local.

La fonction [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) retourne un tableau de structures d' [**\_ \_ informations de cartes IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) , une pour chaque carte de l’ordinateur local. La fonction [**GetPerAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo) retourne des informations supplémentaires sur un adaptateur spécifique. La fonction **GetPerAdapterInfo** oblige l’appelant à spécifier l’index de l’adaptateur. Pour obtenir l’index de l’adaptateur à partir du nom de l’adaptateur, utilisez la fonction [**GetAdapterIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex) .

Certaines applications utilisent des adaptateurs qui reçoivent des datagrammes, mais ne peuvent pas les transmettre. Pour obtenir des informations sur ces adaptateurs, utilisez la fonction [**GetUniDirectionalAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo) .

La fonction [**GetAdaptersAddresses**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses) vous permet de récupérer les adresses IP associées à un adaptateur particulier. Cette fonction prend en charge l’adressage IPv4 et IPv6.

-   Pour obtenir des exemples de code impliquant des [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) , consultez [gestion des cartes réseau à l’aide de GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).

 

 



