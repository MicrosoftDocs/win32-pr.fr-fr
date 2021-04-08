---
description: L’assistance IP permet d’accéder aux informations sur les protocoles réseau utilisés sur l’ordinateur local.
ms.assetid: 3ae07fbd-0b69-42d6-81ab-cc239c354bbb
title: Récupération d’informations sur le protocole de contrôle de transmission et le protocole de datagramme utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a73893bf379dda6a58f86854028967da806863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760845"
---
# <a name="retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol"></a>Récupération d’informations sur le protocole de contrôle de transmission et le protocole de datagramme utilisateur

L’assistance IP permet d’accéder aux informations sur les protocoles réseau utilisés sur l’ordinateur local. Utilisez les fonctions décrites dans les paragraphes suivants pour récupérer des informations sur le protocole TCP (Transmission Control Protocol) et le protocole UDP (User Datagram Protocol) sur l’ordinateur local.

La fonction [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) récupère les statistiques actuelles pour TCP. Pour obtenir des exemples de code impliquant des **GetTcpStatistics** , consultez [extraction d’informations à l’aide de GetTcpStatistics](retrieving-information-using-gettcpstatistics.md).

La fonction [**GetUdpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) récupère les statistiques actuelles pour UDP.

La fonction [**GetTcpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) récupère la table de connexion TCP. Le [**GetUdpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) récupère la table d’écouteurs UDP.

La fonction [**SetTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) permet à un développeur de définir l’état d’une connexion TCP spécifiée sur le TCB d’État TCP de la MIB \_ \_ \_ \_ .

 

 



