---
title: Type complexe de type de données
description: Définit les types de métadonnées que vous pouvez définir dans la section métadonnées du manifeste.
ms.assetid: 602bafe7-940e-4313-9da5-54c6aa7f60a2
keywords:
- Journal des événements de type complexe de type de données
topic_type:
- apiref
api_name:
- MetadataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69b140a2b65d47d563fd88f49d6818efc13613f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033217"
---
# <a name="metadatatype-complex-type"></a>Type complexe de type de données

Définit les types de métadonnées que vous pouvez définir dans la section métadonnées du manifeste.

``` syntax
<xs:complexType name="MetadataType">
    <xs:sequence>
        <xs:element name="channels"
            type="ChannelListType"
         />
        <xs:element name="levels"
            type="LevelListType"
         />
        <xs:element name="tasks"
            type="TaskListType"
         />
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="KeywordListType"
            minOccurs="0"
         />
        <xs:element name="types"
            type="TypeListType"
            minOccurs="0"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
            minOccurs="0"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                       | Type                                                                       | Description                                                                                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**couche**](eventmanifestschema-channels-metadatatype-element.md)         | [**ChannelListType**](eventmanifestschema-channellisttype-complextype.md) | Définit une liste de canaux auxquels les fournisseurs peuvent enregistrer des événements. Un fournisseur peut ensuite importer un ou plusieurs canaux dans son manifeste.<br/>               |
| [**mot**](eventmanifestschema-keywords-metadatatype-element.md)         | [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md) | Définit une liste de mots clés qui déterminent la catégorie d’événements que le fournisseur écrit.<br/>                                                            |
| [**Balance**](eventmanifestschema-levels-metadatatype-element.md)             | [**LevelListType**](eventmanifestschema-levellisttype-complextype.md)     | Définit une liste de niveaux qui spécifient la gravité d’un événement.<br/>                                                                                       |
| **message**                                                                   |                                                                            | Définit une chaîne de message.<br/>                                                                                                                             |
| **messageTable**                                                              |                                                                            | Définit une liste de chaînes de message.<br/>                                                                                                                    |
| [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) | [**NamedQueryType**](eventmanifestschema-namedquerytype-complextype.md)   | Définit une liste de requêtes nommées qui utilisent des expressions régulières pour effectuer des actions de recherche et de remplacement dans la chaîne de message d’un événement.<br/>                        |
| [**OpCodes**](eventmanifestschema-opcodes-metadatatype-element.md)           | [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md)   | Définit une liste d’OpCodes que vous pouvez utiliser pour regrouper des événements au sein d’une tâche.<br/>                                                                             |
| **tasks**                                                                     | [**TaskListType**](eventmanifestschema-tasklisttype-complextype.md)       | Définit une liste de tâches qu’un fournisseur peut utiliser pour regrouper des événements. En général, vous utilisez des tâches pour regrouper des événements pour une fonctionnalité ou un composant du fournisseur.<br/> |
| [**modes**](eventmanifestschema-types-metadatatype-element.md)               | [**TypeListType**](eventmanifestschema-typelisttype-complextype.md)       | Définit une liste de types XML.<br/>                                                                                                                          |



## <a name="attributes"></a>Attributs



| Nom    | Type                                                              | Description                                                                                        |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Référence à la chaîne localisée dans la table de chaînes.<br/>                                |
| mid     | xs:string                                                         | Non utilisé.<br/>                                                                               |
| name    | anyURI                                                            | URI du fichier méta. <br/>                                                              |
| symbole  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Nom symbolique que vous souhaitez que le compilateur de message crée pour cette chaîne de message.<br/> |
| value   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Nombre à utiliser comme identificateur de message pour ce message.<br/>                           |



## <a name="remarks"></a>Notes

Bien que vous puissiez créer un manifeste qui contient une section de métadonnées, le service ne l’utilise pas. les seules métadonnées reconnues par le service sont les métadonnées trouvées dans le fichier Winmeta.xml.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





