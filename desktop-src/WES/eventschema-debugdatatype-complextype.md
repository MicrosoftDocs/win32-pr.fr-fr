---
title: Type complexe DebugDataType
description: définit les données qui peuvent être journalisées pour Windows événements du préprocesseur de trace logiciel (WPP).
ms.assetid: 75638e0f-7a26-473e-a0c4-bd8972ac171f
keywords:
- DebugDataType type complexe EventLog
topic_type:
- apiref
api_name:
- DebugDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c190d3b2b0e870ac249fed03485828685d5dc770
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324361"
---
# <a name="debugdatatype-complex-type"></a>Type complexe DebugDataType

définit les données qui peuvent être journalisées pour Windows événements du préprocesseur de trace logiciel (WPP).

``` syntax
<xs:complexType name="DebugDataType">
    <xs:sequence>
        <xs:element name="SequenceNumber"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="FlagsName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="LevelName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Component"
            type="string"
         />
        <xs:element name="SubComponent"
            type="string"
            minOccurs="0"
         />
        <xs:element name="FileLine"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Function"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="Message"
            type="string"
         />
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                    | Type        | Description                                                                                                        |
|----------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------|
| [**Composant**](eventschema-component-debugdatatype-element.md)           | string      | Nom du composant qui a consigné le message de trace.<br/>                                                |
| [**FileLine**](eventschema-fileline-debugdatatype-element.md)             | string      | Nom du fichier source et ligne dans le fichier source qui a consigné le message de trace.<br/>          |
| [**FlagsName**](eventschema-flagname-debugdatatype-element.md)            | string      | Valeur d’indicateur passée au fournisseur lorsqu’il a été activé.<br/>                                              |
| [**Function**](eventschema-function-debugdatatype-element.md)             | unsignedInt | Nom de la fonction qui a consigné le message de trace.<br/>                                                 |
| [**LevelName**](eventschema-levelname-debugdatatype-element.md)           | string      | Valeur de niveau passée au fournisseur lorsqu’il a été activé.<br/>                                             |
| [**Message**](eventschema-message-debugdatatype-element.md)               | string      | Chaîne du message. Le code XML contient cet élément si l’événement WPP a spécifié le champ FormattedString.<br/> |
| [**SequenceNumber**](eventschema-sequencenumber-debugdatatype-element.md) | unsignedInt | Numéro de séquence local ou global du message de trace.<br/>                                               |
| [**Sous-composant**](eventschema-subcomponent-debugdatatype-element.md)     | string      | Nom du sous-composant qui a consigné le message de trace.<br/>                                             |



## <a name="remarks"></a>Notes

Les éléments sont inclus uniquement si le fournisseur définit la \_ \_ variable d’environnement% préfixe de format de trace% pour les inclure. Pour plus d’informations sur ces éléments, consultez préfixe du message de suivi.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





