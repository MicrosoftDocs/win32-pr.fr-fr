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
ms.openlocfilehash: c10d7ae91d29f3bee72ef43b11b9f30f6229d4a43df4ace213d943b333bffd3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136242"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



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

 

 





