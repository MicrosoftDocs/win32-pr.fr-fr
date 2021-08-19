---
title: Élément Resources (LocalizationType)
description: Définit un groupe de tables de chaînes qui contiennent les chaînes localisées que vous référencez dans votre manifeste.
ms.assetid: b984894a-0ae8-49be-af93-3acdcce53ee9
keywords:
- élément Resources EventLog
topic_type:
- apiref
api_name:
- resources
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3075b2b1741079f80c34e5acf9783b13b74b6973c1d16f2cd323890bcea5d0d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120576"
---
# <a name="resources-localizationtype-element"></a>Élément Resources (LocalizationType)

Définit un groupe de tables de chaînes qui contiennent les chaînes localisées que vous référencez dans votre manifeste.

``` syntax
<xs:element name="resources">
    <xs:complexType>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="stringTable"
                type="StringTableType"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                namespace="##other"
             />
        </xs:choice>
        <xs:attribute name="culture"
            type="string"
            default="##fallback"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

L’élément **Resources** est défini par le type complexe [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md) .

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                  | Type                                                                       | Description                                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**stringTable**](eventmanifestschema-stringtable-resources-element.md) | [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) | Définit une liste de chaînes localisées que vous pouvez référencer dans votre manifeste.<br/> |



## <a name="attributes"></a>Attributs



| Nom    | Type   | Description                                                                                                                                            |
|---------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| culture | string | Nom de langage qui identifie la culture des chaînes localisées dans la table de chaînes. Par exemple, « en-US » pour l’anglais (États-Unis).<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**localisation (instrumentationManifest)**](eventmanifestschema-localization-instrumentationmanifest-element.md)
</dt> </dl>

 

 





