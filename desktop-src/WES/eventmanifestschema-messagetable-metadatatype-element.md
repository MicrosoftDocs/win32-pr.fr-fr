---
title: Élément messageTable (type de données)
description: Contient des références aux chaînes utilisées dans la section métadonnées du manifeste d’instrumentation d’événement. Les chaînes sont stockées dans un groupe d’éléments de message et d’ID associés.
ms.assetid: 868af191-0f9c-435b-878f-ef0584e097d1
keywords:
- EventLog, élément messageTable
topic_type:
- apiref
api_name:
- messageTable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb5efc261a2c055a95f71ba556c9acbc0ad45373
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103081"
---
# <a name="messagetable-metadatatype-element"></a>Élément messageTable (type de données)

Contient des références aux chaînes utilisées dans la section métadonnées du manifeste d’instrumentation d’événement. Les chaînes sont stockées dans un groupe d’éléments de [**message**](eventmanifestschema-message-messagetable-element.md) et d’ID associés.

``` syntax
<xs:element name="messageTable">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="message"
                minOccurs="0"
                maxOccurs="unbounded"
            >
                <xs:complexType>
                    <xs:attribute name="value"
                        type="string"
                        use="required"
                     />
                    <xs:attribute name="mid"
                        type="string"
                        use="optional"
                     />
                    <xs:attribute name="message"
                        type="string"
                        use="required"
                     />
                    <xs:attribute name="symbol"
                        type="string"
                        use="optional"
                     />
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

L’élément **messageTable** est défini par le type complexe de l’élément de [**données**](eventmanifestschema-metadatatype-complextype.md) .

## <a name="child-elements"></a>Éléments enfants



| Élément                                                             | Type | Description                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [**Message**](eventmanifestschema-message-messagetable-element.md) |      | Spécifie une référence à une chaîne dans la section localisation du manifeste.<br/> |



## <a name="attributes"></a>Attributs



| Nom    | Type   | Description                                                              |
|---------|--------|--------------------------------------------------------------------------|
| message | string | Référence à la chaîne localisée dans la table de chaînes.<br/>      |
| mid     | string | Non utilisé.<br/>                                                     |
| symbole  | string | Symbole utilisé pour référencer le message.<br/>                     |
| value   | string | Nombre à utiliser comme identificateur de message pour ce message.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**MetadataType**](eventmanifestschema-metadatatype-complextype.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**métadonnées (instrumentationManifest)**](eventmanifestschema-metadata-instrumentationmanifest-element.md)
</dt> </dl>

 

 





