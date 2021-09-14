---
title: Types de demandes SNMP (SNMP. h)
description: Les types de demandes SNMP sont utilisés pour décrire l’opération que le service SNMP demande à l’agent d’extension d’effectuer.
ms.assetid: a359977f-2edb-4ffd-acba-e14ec8e92544
topic_type:
- apiref
api_name:
- SNMP_EXTENSION_GET
- SNMP_EXTENSION_GET_NEXT
- SNMP_EXTENSION_GET_BULK
- SNMP_EXTENSION_SET_TEST
- SNMP_EXTENSION_SET_COMMIT
- SNMP_EXTENSION_SET_UNDO
- SNMP_EXTENSION_SET_CLEANUP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c37b0064b66fd31f3dbd07dfb593b3fa5900e1e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013807"
---
# <a name="snmp-request-types"></a>Types de demandes SNMP

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

Les types de demandes SNMP sont utilisés pour décrire l’opération que le service SNMP demande à l’agent d’extension d’effectuer.



| Constante/valeur                                                                                                                                                                                                                                                          | Description                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_EXTENSION_GET"></span><span id="snmp_extension_get"></span><dl> <dt>**Protocole SNMP \_ récupération \_**</dt> de l’extension du <dt> \_ PDU \_ SNMP</dt> </dl>                       | Récupère la valeur des valeurs des variables spécifiées.<br/>                                                                                                                                                                                         |
| <span id="SNMP_EXTENSION_GET_NEXT"></span><span id="snmp_extension_get_next"></span><dl> <dt>**Protocole SNMP \_ EXTENSION \_ d' \_ extraction**</dt> de la <dt> \_ \_ PDU SNMP</dt> suivante </dl>   | Récupère la ou les valeurs du successeur lexicographique des variables spécifiées.<br/>                                                                                                                                                          |
| <span id="SNMP_EXTENSION_GET_BULK"></span><span id="snmp_extension_get_bulk"></span><dl> <dt>**Protocole SNMP \_ EXTENSION \_ récupération \_ en bloc**</dt> de la <dt> \_ PDU SNMP \_ GETBULK</dt> </dl>   | Recherchez et récupérez plusieurs valeurs à l’aide d’une seule requête.<br/>                                                                                                                                                                                       |
| <span id="SNMP_EXTENSION_SET_TEST"></span><span id="snmp_extension_set_test"></span><dl> <dt>**\_test de \_ groupe d’extensions SNMP \_**</dt> </dl>                                                                           | Validez les valeurs des variables spécifiées. Cette opération maximise la probabilité d’une opération d’écriture réussie pendant la demande de validation. Pour plus d’informations, consultez la fonction [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) .<br/> |
| <span id="SNMP_EXTENSION_SET_COMMIT"></span><span id="snmp_extension_set_commit"></span><dl> <dt>**Protocole SNMP \_ \_ \_**</dt> ensemble d’extensions <dt> \_ PDU SNMP \_</dt> de validation de jeu d’extensions </dl> | Écrit les nouvelles valeurs dans les variables spécifiées.<br/>                                                                                                                                                                                                 |
| <span id="SNMP_EXTENSION_SET_UNDO"></span><span id="snmp_extension_set_undo"></span><dl> <dt>**\_annulation du \_ jeu d’extensions SNMP \_**</dt> </dl>                                                                           | Réinitialisez les valeurs des variables spécifiées à leurs valeurs avant la demande de validation.<br/>                                                                                                                                                           |
| <span id="SNMP_EXTENSION_SET_CLEANUP"></span><span id="snmp_extension_set_cleanup"></span><dl> <dt>**\_nettoyage du \_ jeu d’extensions SNMP \_**</dt> </dl>                                                                  | Libère les ressources allouées dans les requêtes et les opérations précédentes.<br/>                                                                                                                                                                             |



## <a name="requirements"></a>Spécifications



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

 

