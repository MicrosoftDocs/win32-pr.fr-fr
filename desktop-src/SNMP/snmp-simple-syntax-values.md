---
title: Valeurs de syntaxe simple SNMP (SNMP. h)
description: Les valeurs de syntaxe simple SNMP sont utilisées pour indiquer un type de variable SNMP.
ms.assetid: 42b681e5-721d-4d41-bc1a-c9f0005cde87
topic_type:
- apiref
api_name:
- ASN_INTEGER
- ASN_BITS
- ASN_OCTETSTRING
- ASN_NULL
- ASN_OBJECTIDENTIFIER
- ASN_INTEGER32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ffcd3f8e692dec2040b2b5cc86585d0ca40dd6a664c249d922eb84a16d78fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886429"
---
# <a name="snmp-simple-syntax-values"></a>Valeurs de syntaxe simple SNMP

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

Les valeurs de syntaxe simple SNMP sont utilisées pour indiquer un type de variable SNMP.



| Constante                                                                                                                                                                           | Description                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| <span id="ASN_INTEGER"></span><span id="asn_integer"></span><dl> <dt>**\_entier ASN**</dt> </dl>                            | Indique une variable entière signée 32 bits.<br/>                |
| <span id="ASN_BITS"></span><span id="asn_bits"></span><dl> <dt>**\_bits ASN**</dt> </dl>                                     | Indique une variable qui est une énumération de bits nommés.<br/> |
| <span id="ASN_OCTETSTRING"></span><span id="asn_octetstring"></span><dl> <dt>**\_OCTETSTRING ASN**</dt> </dl>                | Indique une variable de chaîne d’octets.<br/>                        |
| <span id="ASN_NULL"></span><span id="asn_null"></span><dl> <dt>**ASN \_ null**</dt> </dl>                                     | Indique une valeur **null** .<br/>                                |
| <span id="ASN_OBJECTIDENTIFIER"></span><span id="asn_objectidentifier"></span><dl> <dt>**\_OBJECTIDENTIFIER ASN**</dt> </dl> | Indique une variable d’identificateur d’objet.<br/>                   |
| <span id="ASN_INTEGER32"></span><span id="asn_integer32"></span><dl> <dt>**\_INTEGER32 ASN**</dt> </dl>                      | Indique une valeur entière signée 32 bits.<br/>                   |



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

 

