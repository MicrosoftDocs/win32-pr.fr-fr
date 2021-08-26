---
title: Élément TimeCreated (SystemPropertiesType)
description: Horodatage qui identifie le moment où l’événement a été enregistré.
ms.assetid: 16b2b71b-078e-4862-b1be-ef7cec315bc5
keywords:
- EventLog, élément TimeCreated
topic_type:
- apiref
api_name:
- TimeCreated
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5026bed56e3e065a403c0e6076daa0ec478223c4d742db0a35109a41cc98d5c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005299"
---
# <a name="timecreated-systempropertiestype-element"></a>Élément TimeCreated (SystemPropertiesType)

Horodatage qui identifie le moment où l’événement a été enregistré.

``` syntax
<xs:element name="TimeCreated">
    <xs:complexType>
        <xs:attribute name="SystemTime"
            type="dateTime"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

L’élément **TimeCreated** est défini par le type complexe [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .

## <a name="attributes"></a>Attributs



| Nom       | Type     | Description                                              |
|------------|----------|----------------------------------------------------------|
| SystemTime | dateTime | Heure système de la journalisation de l’événement.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**Système (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





