---
description: Vous pouvez utiliser l’assistance IP pour effectuer des opérations ARP (Address Resolution Protocol) pour l’ordinateur local. Utilisez les fonctions suivantes pour récupérer et modifier la table ARP.
ms.assetid: 2c5dc1f8-590f-4b41-b6bb-f82ab093252f
title: Utilisation du protocole de résolution d’adresses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ca1ef7e5d657476ff85a8893d71e197a034c70234e44f32317b7b05f58c9b94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290009"
---
# <a name="using-the-address-resolution-protocol"></a>Utilisation du protocole de résolution d’adresses

Vous pouvez utiliser l’assistance IP pour effectuer des opérations ARP (Address Resolution Protocol) pour l’ordinateur local. Utilisez les fonctions suivantes pour récupérer et modifier la table ARP.

Le [**GetIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) récupère la table ARP. La table ARP contient le mappage d’adresses IP à des adresses physiques. Les adresses physiques sont parfois appelées adresses MAC (Media Access Controller).

Utilisez les fonctions [**CreateIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) et [**DeleteIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) pour ajouter ou supprimer des entrées ARP particulières vers ou à partir de la table. La fonction [**FlushIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) supprime toutes les entrées de la table.

Pour créer ou supprimer des entrées de proxy ARP, utilisez les fonctions [**CreateProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) et [**DeleteProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry) .

La fonction [**SendARP**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) envoie une requête ARP au réseau local.

 

 



