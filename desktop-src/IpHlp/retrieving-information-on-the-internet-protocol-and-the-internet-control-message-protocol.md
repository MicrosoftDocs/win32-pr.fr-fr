---
description: L’assistance IP fournit des fonctionnalités de récupération des informations qui sont utiles pour l’administration réseau de l’ordinateur local.
ms.assetid: b50b3927-6c74-4282-b79b-c86d72d93ae3
title: Récupération d’informations sur le protocole Internet et le protocole de message de contrôle Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b5d009ea045e66a65cf585b2196c56ea13ea95c14938b838d1572c9d563a303
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897809"
---
# <a name="retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol"></a>Récupération d’informations sur le protocole Internet et le protocole de message de contrôle Internet

L’assistance IP fournit des fonctionnalités de récupération des informations qui sont utiles pour l’administration réseau de l’ordinateur local. Les fonctions suivantes récupèrent les statistiques pour le protocole IP (Internet Protocol) et le protocole ICMP (Internet Control Message Protocol). Vous pouvez également utiliser ces fonctions pour définir certains paramètres de configuration pour l’adresse IP.

La fonction [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) récupère les statistiques IP actuelles pour l’ordinateur local. Pour obtenir des exemples de code impliquant des **GetIpStatistics** , consultez [extraction d’informations à l’aide de GetIpStatistics](retrieving-information-using-getipstatistics.md).

La fonction [**GetIcmpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-geticmpstatistics) récupère les statistiques ICMP actuelles.

Utilisez la fonction [**SetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatistics) pour activer ou désactiver le transfert IP. Cette fonction vous permet également de définir la durée de vie (TTL) par défaut des datagrammes IP. Vous pouvez également définir la durée de vie à l’aide de la fonction [**SetIpTTL**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipttl) .

 

 



