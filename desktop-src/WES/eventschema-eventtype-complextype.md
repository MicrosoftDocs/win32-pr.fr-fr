---
title: Type complexe EventType
description: Définit le nœud racine du schéma d’événement.
ms.assetid: 1ff9299b-71ee-4bb3-8a9a-fb9880dbf577
keywords:
- EventType type complexe EventType EventLog
topic_type:
- apiref
api_name:
- EventType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1103570b6c1d9f51a8cbe8fe5628460690fb32cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324321"
---
# <a name="eventtype-complex-type"></a>Type complexe EventType

Définit le nœud racine du schéma d’événement.

``` syntax
<xs:complexType name="EventType">
    <xs:sequence>
        <xs:element name="System"
            type="SystemPropertiesType"
         />
        <xs:choice>
            <xs:element name="EventData"
                type="EventDataType"
                minOccurs="0"
             />
            <xs:element name="UserData"
                type="UserDataType"
                minOccurs="0"
             />
            <xs:element name="DebugData"
                type="DebugDataType"
                minOccurs="0"
             />
            <xs:element name="BinaryEventData"
                type="hexBinary"
                minOccurs="0"
             />
            <xs:element name="ProcessingErrorData"
                type="ProcessingErrorDataType"
                minOccurs="0"
             />
        </xs:choice>
        <xs:element name="RenderingInfo"
            type="RenderingInfoType"
            minOccurs="0"
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



| Élément                                                                          | Type                                                                               | Description                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BinaryEventData**](eventschema-binaryeventdata-eventtype-element.md)         | hexBinary                                                                          | Contient les données d’événement sous la forme d’un objet blob binaire. Les données d’événement sont rendues sous la forme d’un objet blob binaire si la fonction de rendu ne peut pas trouver les métadonnées utilisées pour décoder l’événement.<br/>                                                                                                                                                            |
| [**DebugData**](eventschema-debugdata-eventtype-element.md)                     | [**DebugDataType**](eventschema-debugdatatype-complextype.md)                     | contient les données qui peuvent être journalisées pour Windows événements du préprocesseur de trace logiciel (WPP).<br/>                                                                                                                                                                                                                                    |
| [**EventData**](eventschema-eventdata-eventtype-element.md)                     | [**EventDataType**](eventschema-eventdatatype-complextype.md)                     | Contient les données d'événement. L’ordre des éléments de données dans le modèle détermine la disposition des données d’événement.<br/>                                                                                                                                                                                                                 |
| [**ProcessingErrorData**](eventschema-processingerrordata-eventtype-element.md) | [**ProcessingErrorDataType**](eventschema-processingerrordatatype-complextype.md) | Contient les détails de l’erreur qui s’est produite lors de la tentative de rendu de l’événement. Cela peut se produire si les données d’événement ne correspondent pas à la définition des données d’événement dans le manifeste. Les données d’événement sont incluses en tant qu’objet blob binaire.<br/>                                                                                                         |
| [**RenderingInfo**](eventschema-renderinginfo-eventtype-element.md)             | [**RenderingInfoType**](eventschema-renderingtype-complextype.md)                 | Contient les chaînes de message rendues pour l’événement (inclut la chaîne de message de l’événement et les chaînes de message pour l’une des propriétés de l’événement, telles que le niveau, la tâche et l’opcode). seuls les événements qui ont été collectés à l’aide du service [collecteur d’événements Windows](/windows/desktop/WEC/windows-event-collector) contiennent cette section.<br/> |
| [**Système**](eventschema-system-eventtype-element.md)                           | [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)       | Contient des informations qui identifient le fournisseur et comment il a été activé, l’événement, le canal vers lequel l’événement a été écrit et des informations système telles que les ID de processus et de thread.<br/>                                                                                                                                   |
| [**UserData**](eventschema-userdata-eventtype-element.md)                       | [**UserDataType**](eventschema-userdatatype-complextype.md)                       | Contient les données d'événement. La section données utilisateur du modèle détermine la disposition des données d’événement.<br/>                                                                                                                                                                                                                       |



## <a name="remarks"></a>Notes

En règle générale, cette section contient la section **EventData** ou **UserData** . La section **EventData** est utilisée si le modèle ne contient pas de section **UserData** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

