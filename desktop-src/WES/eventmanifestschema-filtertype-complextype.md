---
title: FilterType (type complexe)
description: Définit un filtre de données utilisé par une session pour filtrer les événements en fonction des données d’événement.
ms.assetid: f2874b3f-cf3a-4dd9-b914-6adaac33cf7b
keywords:
- FilterType, type complexe EventLog
topic_type:
- apiref
api_name:
- FilterType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ef3d80b8cb5347c1adf0e2b21a745e4d4f5fae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467014"
---
# <a name="filtertype-complex-type"></a>FilterType (type complexe)

Définit un filtre de données utilisé par une session pour filtrer les événements en fonction des données d’événement.

``` syntax
<xs:complexType name="FilterType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="version"
                type="UInt8Type"
                use="optional"
             />
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="tid"
                type="token"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributs



| Nom    | Type                                                              | Description                                                                                                                                                                                                                                      |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Description localisée du filtre. La chaîne de message fait référence à une chaîne localisée dans la section [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) du manifeste.<br/>                                   |
| name    | **QName**                                                         | Nom qui identifie le filtre.<br/>                                                                                                                                                                                                    |
| symbole  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Symbole à utiliser pour référencer le filtre dans votre application. Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour le filtre dans le fichier d’en-tête généré par le compilateur.<br/> |
| tid     | token                                                             | Identificateur de modèle qui décrit les données de filtre que la session transmet au fournisseur lorsqu’elle active le fournisseur.<br/>                                                                                                            |
| value   | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Valeur entière qui identifie de façon unique le filtre dans la liste des filtres que vous définissez.<br/>                                                                                                                                      |
| version | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Valeur entière qui identifie cette version du filtre. S’il n’est pas spécifié, la valeur est zéro.<br/>                                                                                                                                     |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



 

 





