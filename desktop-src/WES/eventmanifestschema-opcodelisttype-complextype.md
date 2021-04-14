---
title: Type complexe OpcodeListType
description: Définit une liste d’OpCodes utilisés pour identifier les opérations d’un composant de l’application.
ms.assetid: 0cbca036-b32e-4fc4-96ee-1dd5bee019bf
keywords:
- OpcodeListType type complexe EventLog
topic_type:
- apiref
api_name:
- OpcodeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dce0942ef0268f50b25987a6be0fd4fffeebd614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465182"
---
# <a name="opcodelisttype-complex-type"></a>Type complexe OpcodeListType

Définit une liste d’OpCodes utilisés pour identifier les opérations d’un composant de l’application.

``` syntax
<xs:complexType name="OpcodeListType">
    <xs:sequence>
        <xs:element name="opcode"
            type="OpcodeType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                             | Type                                                             | Description                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------|
| [**OpCode**](eventmanifestschema-opcode-opcodelisttype-element.md) | [**OpcodeType**](eventmanifestschema-opcodetype-complextype.md) | Définit une opération dans un composant de l’application.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





