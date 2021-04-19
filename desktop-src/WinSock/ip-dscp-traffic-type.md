---
description: Le tableau suivant décrit les \_ options de socket de type de trafic IP DSCP \_ \_ .
ms.assetid: 0042B53F-B84E-453A-8E18-87052280DAD5
title: IP_DSCP_TRAFFIC_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IP_DSCP_TRAFFIC_TYPE
api_type:
- HeaderDef
api_location:
- N/A
ms.openlocfilehash: 80cbe41e58cf36cd366015d83af380f5952630ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525488"
---
# <a name="ip_dscp_traffic_type"></a>\_type de \_ trafic \_ DSCP IP

Le tableau suivant décrit les \_ options de socket de type de trafic IP DSCP \_ \_ .

<dl> <dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**\_type de \_ trafic \_ DSCP IP**</dt> <dd> <dl> <dt> 

| Option              | Obtenir | Définissez | Type Optval | Description                                                                                                                                                                                                                                                                                                                                      |
|---------------------|-----|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_type de trafic DSCP \_ | Oui | Oui | DWORD       | En définissant cette valeur sur les valeurs définies dans **\_ \_ type de trafic DSCP**, une application peut demander à ses paquets réseau d’être traités en fonction du type de service demandé. De même, les appels à [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) peuvent être utilisés pour obtenir le paramètre actuel pour le type de trafic demandé sur le socket donné. |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|--------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows 10<br/>                                                          |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2016<br/>                                                 |
| En-tête<br/>                | <dl> <dt>N/A</dt> </dl> |



 

 




