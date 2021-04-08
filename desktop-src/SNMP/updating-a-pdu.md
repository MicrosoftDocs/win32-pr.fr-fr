---
title: Mise à jour d’une PDU
description: Une application WinSNMP peut récupérer et mettre à jour les champs de la PDU sélectionnée à l’aide des fonctions SnmpGetPduData et SnmpSetPduData.
ms.assetid: 001f5252-aa54-490b-8ff0-39a7780baff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678f980882b350669321cf676f9bc69af4369de8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675090"
---
# <a name="updating-a-pdu"></a>Mise à jour d’une PDU

Une application WinSNMP peut récupérer et mettre à jour les champs de la PDU sélectionnée à l’aide des fonctions [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) et [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) .

L’application peut récupérer les champs type d’unité d’alimentation, identificateur de la demande, état de l’erreur et index des erreurs d’une PDU spécifique. Il peut également récupérer le descripteur de la liste de liaisons de variables. L’application peut mettre à jour le **\_ type d’unité d’alimentation** et les champs d' **\_ ID de demande** .

Si le type de PDU est égal à la \_ PDU SNMP \_ GETBULK, l’application peut également mettre à jour les champs **non \_ répéteurs** et **nombre maximal de \_ répétitions** de la PDU.

 

 




