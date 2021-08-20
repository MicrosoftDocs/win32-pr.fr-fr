---
title: Valeurs de type de PDU (SNMP. h)
description: Les valeurs de type de PDU sont utilisées dans le champ type d’unité d’alimentation (PDU) \_ de l’unité d’alimentation pour décrire son type.
ms.assetid: 9d7a3f1c-7940-428b-a4e0-3c9e61dd755f
topic_type:
- apiref
api_name:
- SNMP_PDU_GET
- SNMP_PDU_GETNEXT
- SNMP_PDU_RESPONSE
- SNMP_PDU_SET
- SNMP_PDU_V1TRAP
- SNMP_PDU_GETBULK
- SNMP_PDU_INFORM
- SNMP_PDU_TRAP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e9346c313efccda6d3635da51919f52fae37dd901cc73cf1f119bffdf9c22c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009207"
---
# <a name="pdu-type-values"></a>Valeurs de type d’unité d’alimentation

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

Les valeurs de type de PDU sont utilisées dans le champ **\_ type d’unité** d’alimentation (PDU) de l’unité d’alimentation pour décrire son type.



| Constante                                                                                                                                                                   | Description                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_PDU_GET"></span><span id="snmp_pdu_get"></span><dl> <dt>**\_récupération du PDU SNMP \_**</dt> </dl>                | Recherchez et récupérez une valeur d’une variable SNMP spécifiée.<br/>                                       |
| <span id="SNMP_PDU_GETNEXT"></span><span id="snmp_pdu_getnext"></span><dl> <dt>**\_PDU SNMP \_ GetNext**</dt> </dl>    | Recherchez et récupérez la valeur d’une variable SNMP sans connaître le nom exact de la variable.<br/> |
| <span id="SNMP_PDU_RESPONSE"></span><span id="snmp_pdu_response"></span><dl> <dt>**\_réponse PDU \_ SNMP**</dt> </dl> | Répondez à une \_ demande d’alimentation de PDU SNMP \_ ou à une \_ demande d’alimentation PDU SNMP \_ .<br/>                                      |
| <span id="SNMP_PDU_SET"></span><span id="snmp_pdu_set"></span><dl> <dt>**\_ensemble d’PDU SNMP \_**</dt> </dl>                | Stocke une valeur dans une variable SNMP spécifiée.<br/>                                                       |
| <span id="SNMP_PDU_V1TRAP"></span><span id="snmp_pdu_v1trap"></span><dl> <dt>**\_V1TRAP PDU \_ SNMP**</dt> </dl>       | Indique que l’interruption de la PDU est mise en forme pour être conforme à la norme SNMPv1.<br/>                     |
| <span id="SNMP_PDU_GETBULK"></span><span id="snmp_pdu_getbulk"></span><dl> <dt>**\_GETBULK PDU \_ SNMP**</dt> </dl>    | Recherchez et récupérez plusieurs valeurs à l’aide d’une seule requête.<br/>                                        |
| <span id="SNMP_PDU_INFORM"></span><span id="snmp_pdu_inform"></span><dl> <dt>**\_avis du PDU SNMP \_**</dt> </dl>       | Indique un PDU de demande d’information.<br/>                                                                  |
| <span id="SNMP_PDU_TRAP"></span><span id="snmp_pdu_trap"></span><dl> <dt>**interruption de l' \_ PDU SNMP \_**</dt> </dl>             | Signale au système de gestion un événement extraordinaire sous SNMPv2C.<br/>                             |



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

 

