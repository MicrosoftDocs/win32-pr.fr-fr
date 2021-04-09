---
title: Élément opcode (OpcodeListType)
description: Contient une valeur numérique qui identifie l’activité ou un point dans une activité que l’application a exécutée lorsqu’elle a déclenché l’événement (par exemple, initialisation ou fermeture).
ms.assetid: 8c5cfbd3-6a74-452c-a12f-41d663426e2c
keywords:
- OpCode, élément EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9d02b77b4a36bac26d52d7bf8d849eab8731d27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106027"
---
# <a name="opcode-opcodelisttype-element"></a>Élément opcode (OpcodeListType)

Contient une valeur numérique qui identifie l’activité ou un point dans une activité que l’application a exécutée lorsqu’elle a déclenché l’événement (par exemple, initialisation ou fermeture).

``` syntax
<xs:element name="opcode"
    type="OpcodeType"
 />
```

L’élément **opcode** est défini par le type complexe [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Éléments parents**
</dt> <dt>

[**OpCodes (TaskType)**](eventmanifestschema-opcodes-tasktype-element.md)
</dt> <dt>

[**OpCodes (ProviderType)**](eventmanifestschema-opcodes-providertype-element.md)
</dt> <dt>

[**OpCodes (type de données)**](eventmanifestschema-opcodes-metadatatype-element.md)
</dt> </dl>

 

 





