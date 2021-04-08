---
title: Type complexe EventDataType
description: Définit les éléments de données d’événement et les structures qui contiennent les données d’événement.
ms.assetid: 9531163f-34ce-4673-b2d8-636042915c73
keywords:
- EventDataType type complexe EventLog
topic_type:
- apiref
api_name:
- EventDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a93695db477ebb0c7b5652419198f8f5c6370dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740373"
---
# <a name="eventdatatype-complex-type"></a>Type complexe EventDataType

Définit les éléments de données d’événement et les structures qui contiennent les données d’événement.

``` syntax
<xs:complexType name="EventDataType">
    <xs:sequence>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="Data"
                type="DataType"
             />
            <xs:element name="ComplexData"
                type="ComplexDataType"
             />
        </xs:choice>
        <xs:element name="Binary"
            type="hexBinary"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                              | Type                                                               | Description                                                                                          |
|----------------------------------------------------------------------|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**Binary**](eventschema-binary-eventdatatype-element.md)           | hexBinary                                                          | Objet blob de données binaires pour les événements écrits à l’aide de la [journalisation des événements](/windows/desktop/EventLog/event-logging).<br/> |
| [**ComplexData**](eventschema-complexdata-eventdatatype-element.md) | [**ComplexDataType**](eventschema-complexdatatype-complextype.md) | Structure définie dans le modèle pour l’événement.<br/>                                |
| [**Données**](eventschema-data-eventdatatype-element.md)               | [**DataType**](eventschema-datafieldtype-complextype.md)          | Élément de données de niveau supérieur défini dans le modèle pour l’événement.<br/>                      |



## <a name="attributes"></a>Attributs



| Nom | Type   | Description                                                       |
|------|--------|-------------------------------------------------------------------|
| Nom | string | Nom du modèle qui contient les éléments de données.<br/> |



## <a name="remarks"></a>Notes

La fonction [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) affiche des tableaux et des structures sous forme d’objets BLOB binaires.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

