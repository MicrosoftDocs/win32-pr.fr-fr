---
description: Définit la section du manifeste d’instrumentation qui identifie le fournisseur et les compteurs qu’ils fournissent.
ms.assetid: c661f1af-ebe8-4f8a-b77e-a2229f45facd
title: Type complexe des compteurs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ad87b79175b0cecdec17ad081340fa0be2b90b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952003"
---
# <a name="counters-complex-type"></a>Type complexe des compteurs

Définit la section du manifeste d’instrumentation qui identifie le fournisseur et les compteurs qu’ils fournissent.

``` syntax
<xs:complexType name="counters">
    <xs:choice
        minOccurs="1"
        maxOccurs="1"
    >
        <xs:element name="provider"
            type="man:provider"
         />
    </xs:choice>
    <xs:attribute name="schemaVersion"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="1.1"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément      | Type                                                               | Description                                              |
|--------------|--------------------------------------------------------------------|----------------------------------------------------------|
| **moteur** | [**homme : fournisseur**](performance-counters-provider-complex-type.md) | Identifie un fournisseur qui fournit des compteurs.<br/> |



## <a name="attributes"></a>Attributs



| Nom          | Type | Description                                                      |
|---------------|------|------------------------------------------------------------------|
| schemaVersion |      | Version du schéma utilisé pour écrire le manifeste.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Instrumentation**](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype)
</dt> </dl>

 

