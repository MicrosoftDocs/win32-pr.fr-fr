---
title: Valeurs de la syntaxe de l’application SNMP (SNMP. h)
description: Les valeurs de syntaxe d’application SNMP sont utilisées par les applications de gestion qui utilisent l’API de gestion SNMP de Microsoft.
ms.assetid: fa269f97-f9d3-49f4-b29b-8c4d71f075d0
topic_type:
- apiref
api_name:
- ASN_IPADDRESS
- ASN_COUNTER32
- ASN_GAUGE32
- ASN_TIMETICKS
- ASN_OPAQUE
- ASN_COUNTER64
- ASN_UINTEGER32
- ASN_RFC2578_UNSIGNED32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 787723780d5920aafc3c37c40ea995a675943d1e45873d5f30cd8cebb77b5b64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009027"
---
# <a name="snmp-application-syntax-values"></a>Valeurs de la syntaxe de l’application SNMP

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

Les valeurs de syntaxe d’application SNMP sont utilisées par les applications de gestion qui utilisent l’API de gestion SNMP de Microsoft.



| Constante                                                                                                                                                                                  | Description                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASN_IPADDRESS"></span><span id="asn_ipaddress"></span><dl> <dt>**\_adresse IP ASN**</dt> </dl>                             | Indique une variable d’adresse IP.<br/>                                                                                     |
| <span id="ASN_COUNTER32"></span><span id="asn_counter32"></span><dl> <dt>**\_COUNTER32 ASN**</dt> </dl>                             | Indique une variable de compteur.<br/>                                                                                         |
| <span id="ASN_GAUGE32"></span><span id="asn_gauge32"></span><dl> <dt>**\_Gauge32 ASN**</dt> </dl>                                   | Indique une variable de jauge. Cette variable décrit un type Unsigned32 conforme à la norme RFC 1902.<br/>                  |
| <span id="ASN_TIMETICKS"></span><span id="asn_timeticks"></span><dl> <dt>**\_graduations ASN**</dt> </dl>                             | Indique une variable graduations.<br/>                                                                                       |
| <span id="ASN_OPAQUE"></span><span id="asn_opaque"></span><dl> <dt>**ASN \_ opaque**</dt> </dl>                                      | Indique une variable opaque.<br/>                                                                                         |
| <span id="ASN_COUNTER64"></span><span id="asn_counter64"></span><dl> <dt>**\_COUNTER64 ASN**</dt> </dl>                             | Indique une variable de compteur qui augmente jusqu’à ce qu’elle atteigne la valeur maximale (2 ^ 64)-1.<br/>                           |
| <span id="ASN_UINTEGER32"></span><span id="asn_uinteger32"></span><dl> <dt>**\_UINTEGER32 ASN**</dt> </dl>                          | Indique une variable de type entier non signé 32 bits. Cette variable décrit un type UInteger32 conforme à la norme RFC 1442.<br/> |
| <span id="ASN_RFC2578_UNSIGNED32"></span><span id="asn_rfc2578_unsigned32"></span><dl> <dt>**ASN \_ RFC2578 \_ UNSIGNED32**</dt> </dl> | Voir ASN \_ gauge32.<br/>                                                                                                     |



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

 

