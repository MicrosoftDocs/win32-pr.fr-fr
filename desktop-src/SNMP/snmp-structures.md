---
title: Structures SNMP
description: Le tableau suivant répertorie les structures utilisées avec SNMP.
ms.assetid: b6dacc85-893d-4825-93df-729333b491b3
keywords:
- SNMP de structures SNMP
- Structures SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f254dfebeb3d468add8871d4b6f28f268341e9ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011358"
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



 

 

 