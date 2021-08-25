---
title: Structures SNMP
description: Le tableau suivant répertorie les structures utilisées avec SNMP.
ms.assetid: b6dacc85-893d-4825-93df-729333b491b3
keywords:
- SNMP de structures SNMP
- Structures SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb5cf0920d9387fb24874cc92a8e7fa623617d89f3578cb181805eb56f35546
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886349"
---
# <a name="snmp-structures"></a>Structures SNMP

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

Le tableau suivant répertorie les structures utilisées avec SNMP.



| Structure SNMP                                         | Description                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany)                           | Décrit le type et la valeur d’une variable SNMP spécifiée.                                              |
| [**AsnCounter64**](/previous-versions/windows/desktop/legacy/aa377953(v=vs.85))               | Contient un compteur 64 bits qui est spécifié par deux valeurs décrivant ses bits de poids faible et de poids fort. |
| [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) | Décrit un identificateur d’objet (OID).                                                                   |
| [**AsnOctetString**](/windows/desktop/api/Snmp/ns-snmp-asnoctetstring)           | Représente une chaîne d’octets, généralement en valeurs d’octets.                                                  |
| [**SnmpVarBind**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind)                 | Décrit une liaison de variable SNMP.                                                                     |
| [**SnmpVarBindList**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist)         | Contient une liste de liaisons de variable SNMP.                                                              |



 

 

 