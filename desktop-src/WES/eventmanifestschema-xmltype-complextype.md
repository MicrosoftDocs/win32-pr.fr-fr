---
title: Type complexe XmlType
description: Définit un fragment XML.
ms.assetid: ac6ce2a2-4584-4181-9a39-aceab85d5c51
keywords:
- Type complexe XmlType journal des événements
topic_type:
- apiref
api_name:
- XmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a4a4d71d7f4f2685d6c5f1c0626392c79436b68d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384620"
---
# <a name="xmltype-complex-type"></a>Type complexe XmlType

Définit un fragment XML. Toute instance de schéma est autorisée ; le nœud de niveau supérieur du fragment doit contenir un attribut d’espace de noms.

``` syntax
<xs:complexType name="XmlType">
    <xs:sequence>
        <xs:any
            processContents="skip"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





