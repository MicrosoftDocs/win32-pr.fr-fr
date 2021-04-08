---
title: Types d’interruptions SNMPv1 (SNMP. h)
description: Les types d’interruptions SNMPv1 décrivent un ensemble prédéfini de types d’interruptions génériques mis en forme pour être conformes à la norme de l’IPDU de l’interruption SNMPv1.
ms.assetid: 3a652b8f-2ae1-4f8c-b0d6-388bc9171427
topic_type:
- apiref
api_name:
- SNMP_GENERICTRAP_COLDSTART
- SNMP_GENERICTRAP_WARMSTART
- SNMP_GENERICTRAP_LINKDOWN
- SNMP_GENERICTRAP_LINKUP
- SNMP_GENERICTRAP_AUTHFAILURE
- SNMP_GENERICTRAP_EGPNEIGHLOSS
- SNMP_GENERICTRAP_ENTERSPECIFIC
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1091bc6af4fa4b1ddfadbaf35e3e69250ded6dcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844326"
---
# <a name="snmpv1-trap-types"></a>Types d’interruptions SNMPv1

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

Les types d’interruptions SNMPv1 décrivent un ensemble prédéfini de types d’interruptions génériques mis en forme pour être conformes à la norme de l’IPDU de l’interruption SNMPv1.



| Constante                                                                                                                                                                                                          | Description                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_GENERICTRAP_COLDSTART"></span><span id="snmp_generictrap_coldstart"></span><dl> <dt>**\_COLDSTART GENERICTRAP \_ SNMP**</dt> </dl>             | Indique une interruption de démarrage à froid. L’agent initialise les entités de protocole sur le mode géré. Il peut modifier les objets dans sa vue.<br/>                                               |
| <span id="SNMP_GENERICTRAP_WARMSTART"></span><span id="snmp_generictrap_warmstart"></span><dl> <dt>**\_WARMSTART GENERICTRAP \_ SNMP**</dt> </dl>             | Indique une interruption de démarrage à chaud. L’agent se réinitialise lui-même, mais il ne modifie pas les objets dans sa vue.<br/>                                                                    |
| <span id="SNMP_GENERICTRAP_LINKDOWN"></span><span id="snmp_generictrap_linkdown"></span><dl> <dt>**\_LINKDOWN GENERICTRAP \_ SNMP**</dt> </dl>                | Indique une interruption de liaison. Une interface attachée est passée de l’état actif à l’état inactif. La première variable de la liste liaisons de variables identifie l’interface.<br/> |
| <span id="SNMP_GENERICTRAP_LINKUP"></span><span id="snmp_generictrap_linkup"></span><dl> <dt>**\_LinkUp GENERICTRAP \_ SNMP**</dt> </dl>                      | Indique une interruption de liaison. Une interface attachée est passée de l’état de démarrage à l’état inactif. La première variable de la liste liaisons de variables identifie l’interface.<br/>   |
| <span id="SNMP_GENERICTRAP_AUTHFAILURE"></span><span id="snmp_generictrap_authfailure"></span><dl> <dt>**\_AUTHFAILURE GENERICTRAP \_ SNMP**</dt> </dl>       | Indique une interruption d’échec d’authentification. Une entité SNMP a envoyé un message SNMP, mais son appartenance à une communauté connue a été affirmée.<br/>                                 |
| <span id="SNMP_GENERICTRAP_EGPNEIGHLOSS"></span><span id="snmp_generictrap_egpneighloss"></span><dl> <dt>**\_EGPNEIGHLOSS GENERICTRAP \_ SNMP**</dt> </dl>    | Indique un piège de perte de voisinage EGP. Un homologue EGP est passé à l’état arrêté. La première variable de la liste liaisons de variables identifie l’adresse IP de l’homologue EGP.<br/>   |
| <span id="SNMP_GENERICTRAP_ENTERSPECIFIC"></span><span id="snmp_generictrap_enterspecific"></span><dl> <dt>**\_ENTERSPECIFIC GENERICTRAP \_ SNMP**</dt> </dl> | Indique une interruption spécifique à l’entreprise. Un événement extraordinaire s’est produit. Elle est identifiée dans le paramètre *specificTrap* par une valeur spécifique à l’entreprise.<br/>               |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                        |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>SNMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du protocole SNMP (Simple Network Management Protocol)](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[Référence SNMP](snmp-reference.md)
</dt> <dt>

[Constantes SNMP](snmp-constants.md)
</dt> </dl>

 

