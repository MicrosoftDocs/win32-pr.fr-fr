---
description: 'L’API du fournisseur d’espace de noms PNRP utilise les structures suivantes :'
ms.assetid: 697fb99a-259f-429c-8818-0d725255bc86
title: Structures PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78e2ee85f3673395ade31417c79c010354f16b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518482"
---
# <a name="pnrp-structures"></a>Structures PNRP

L’API du fournisseur d’espace de noms PNRP utilise les structures suivantes :



| Structure                                                             | Description                                                                                                                                                         |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ informations sur le point de terminaison PNRP homologue \_**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_endpoint_info)         | Contient les adresses IP et les données associées à un point de terminaison homologue.                                                                                                 |
| [**\_ \_ informations sur le Cloud PNRP homologue \_**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_cloud_info)               | Contient des informations sur un Cloud PNRP (Peer Name Resolution Protocol).                                                                                            |
| [**\_ \_ informations d’inscription PNRP de l’homologue \_**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_registration_info) | Contient les informations fournies par une identité d’homologue lorsqu’elle s’inscrit auprès d’un Cloud PNRP.                                                                           |
| [PNRP et objet BLOB](pnrp-and-blob.md)                                    | Transmet des données à la structure [**WSAQUERYSET**](winsock-nsp-reference-links.md) lors des appels à plusieurs fonctions.                                                  |
| [PNRP et WSAQUERYSET](pnrp-and-wsaqueryset.md)                      | Facilite la résolution des noms et l’énumération des noms et des clouds.                                                                                         |
| [**\_ID de Cloud PNRP \_**](/windows/desktop/api/Pnrpdef/ns-pnrpdef-pnrp_cloud_id)                              | Contient les valeurs qui définissent un Cloud réseau.                                                                                                                    |
| [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)                                | Pointé par le membre **lpBlob** de la structure [**WSAQUERYSET**](winsock-nsp-reference-links.md) .                                                            |
| [**PNRPINFO \_ v1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)                                      | Pointé par le membre **lpBlob** de la structure [**WSAQUERYSET**](winsock-nsp-reference-links.md)                                                             |
| [**PNRPINFO \_ v2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))                                   | Pointé par le membre **lpBlob** de la structure [**WSAQUERYSET**](winsock-nsp-reference-links.md) , et fournit la prise en charge des données opaques spécifiques à l’application. |



 

 

 
