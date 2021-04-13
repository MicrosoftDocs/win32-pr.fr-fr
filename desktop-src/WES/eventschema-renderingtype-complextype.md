---
title: Type complexe RenderingInfoType
description: Définit les messages rendus pour l’événement.
ms.assetid: 85a4cfc6-6277-4af8-af4e-cae3bd3aac13
keywords:
- RenderingInfoType type complexe EventLog
topic_type:
- apiref
api_name:
- RenderingInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d0e4224ec9b90e84cbacbf5ede852763edd8e4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466691"
---
# <a name="renderinginfotype-complex-type"></a>Type complexe RenderingInfoType

Définit les messages rendus pour l’événement.

``` syntax
<xs:complexType name="RenderingInfoType">
    <xs:sequence>
        <xs:element name="Message"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Channel"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Provider"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="Keyword"
                        type="string"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="Culture"
        type="language"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                             | Type   | Description                                                                   |
|---------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| [**Channel**](eventschema-task-renderingtype-element.md)           | string | Chaîne de message rendue du canal spécifié dans l’événement.<br/> |
| [**Mot**](eventschema-keyword-keywords-element.md)             | string | Chaîne de message rendue d’un mot clé spécifié dans l’événement.<br/>   |
| [**Mots clés**](eventschema-keywords-renderingtype-element.md)      |        | Liste de mots clés rendus.<br/>                                       |
| [**Niveau**](eventschema-level-renderingtype-element.md)            | string | Chaîne de message rendue du niveau spécifié dans l’événement.<br/>   |
| [**Message**](eventschema-message-renderingtype-element.md)        | string | Chaîne de message rendue de l’événement.<br/>                          |
| [**Opcode**](eventschema-opcode-renderingtype-element.md)          | string | Chaîne de message rendue de l’opcode spécifié dans l’événement.<br/>  |
| [**Fournisseur**](eventschema-publisher-renderinginfotype-element.md) | string | Chaîne de message rendue pour le fournisseur.<br/>                      |
| [**Tâche**](eventschema-task-renderingtype-element.md)              | string | Chaîne de message rendue de la tâche spécifiée dans l’événement.<br/>    |



## <a name="attributes"></a>Attributs



| Nom    | Type     | Description                                                                                                      |
|---------|----------|------------------------------------------------------------------------------------------------------------------|
| Culture | langage | Nom de la langue (par exemple, en-US) qui identifie les paramètres régionaux utilisés pour afficher les chaînes de message.<br/> |



## <a name="remarks"></a>Notes

Seuls les événements qui ont été collectés à l’aide du service [collecteur d’événements Windows](/windows/desktop/WEC/windows-event-collector) contiendront cette section.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

