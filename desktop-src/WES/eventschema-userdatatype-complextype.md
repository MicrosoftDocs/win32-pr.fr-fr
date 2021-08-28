---
title: Type complexe UserDataType
description: Définit un fragment XML qui spécifie la disposition des données d’événement.
ms.assetid: 25147ace-cc36-43cc-ad85-6a1714f43dbe
keywords:
- UserDataType type complexe EventLog
topic_type:
- apiref
api_name:
- UserDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 747f2e30f6b2588cdfd6a9f0dd50187b73817996bd3725a571283a7929c91b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904189"
---
# <a name="userdatatype-complex-type"></a>Type complexe UserDataType

Définit un fragment XML qui spécifie la disposition des données d’événement.

``` syntax
<xs:complexType name="UserDataType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





