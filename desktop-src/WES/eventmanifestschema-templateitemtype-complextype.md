---
title: Type complexe TemplateItemType
description: Modèle qui définit les données à inclure avec un événement. | Type complexe TemplateItemType
ms.assetid: 1681af7d-03ef-47bc-bc02-ce1a9903fb44
keywords:
- TemplateItemType type complexe EventLog
topic_type:
- apiref
api_name:
- TemplateItemType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94ae108ceed3285fe7e57461611d94b1147d94e7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211518"
---
# <a name="templateitemtype-complex-type"></a>Type complexe TemplateItemType

Modèle qui définit les données à inclure avec un événement.

``` syntax
<xs:complexType name="TemplateItemType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:choice
            maxOccurs="unbounded"
            minOccurs="0"
        >
            <xs:element name="data"
                type="DataDefinitionType"
             />
            <xs:element name="struct"
                type="StructDefinitionType"
             />
        </xs:choice>
        <xs:element name="binary"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="name"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="UserData"
            type="XmlType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="tid"
        type="token"
        use="required"
     />
    <xs:attribute name="name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                   | Type                                                                                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**binaire2**](eventmanifestschema-binary-templateitemtype-element.md)     |                                                                                      | Réservé à un usage interne uniquement.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**métadonnée**](eventmanifestschema-data-templateitemtype-element.md)         | [**DataDefinitionType**](eventmanifestschema-datadefinitiontype-complextype.md)     | Définit un élément de données que vous souhaitez inclure avec l’événement.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**modélis**](eventmanifestschema-struct-templateitemtype-element.md)     | [**StructDefinitionType**](eventmanifestschema-structdefinitiontype-complextype.md) | Définit une structure qui inclut un ou plusieurs éléments de données que vous souhaitez inclure avec l’événement. Les fournisseurs écrivent la structure en tant qu’objet BLOB et non en tant que membres individuels de la structure.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) | [**XmlType**](eventmanifestschema-xmltype-complextype.md)                           | Fragment XML utilisé pour restituer les données d’événement. Si vous n’incluez pas le fragment, les données d’événement sont rendues dans l’ordre dans lequel les éléments de données sont définis dans le modèle. Le contenu de cet élément est tout fragment XML valide. Le fragment ne doit contenir qu’un seul nœud de niveau supérieur et le nœud de niveau supérieur doit spécifier son propre espace de noms. <br/> Pour référencer un élément de données dans le fragment, définissez le corps du texte d’un nœud dans le fragment sur%*n*, où *n* est l’index de base un des éléments de données de niveau supérieur dans la liste des éléments de données (vous ne pouvez pas référencer les membres d’une structure). La valeur d’index que vous spécifiez ne doit pas être supérieure au nombre d’éléments de données de niveau supérieur dans le modèle.<br/> Cet élément suit tous les éléments de **données** et de **struct** . <br/> |



## <a name="attributes"></a>Attributs



| Nom | Type   | Description                                                                                                                                                                                           |
|------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name | string | Réservé à un usage interne uniquement.<br/>                                                                                                                                                            |
| name | string | Nom du modèle.<br/>                                                                                                                                                                  |
| tid  | token  | Identificateur qui identifie de façon unique le modèle dans la liste des modèles que le fournisseur définit. Utilisez ce nom pour faire référence au modèle lorsque vous définissez votre définition d’événement.<br/> |



## <a name="remarks"></a>Notes

La définition de modèle doit avoir au moins un élément enfant de données ou struct. Le fournisseur doit écrire les données d’événement dans l’ordre des éléments de données définis dans le modèle.

La taille de tous les éléments de données du modèle doit être inférieure à 64 Ko.

## <a name="examples"></a>Exemples

L’exemple suivant montre comment créer une définition de modèle.


```XML
<templates>
   <template tid="T1">
       <data name="PrinterName" intype="win:UnicodeString" />
       <UserData>
          <PrinterConnectionFailure 
              xmlns="schemas.microsoft.com/schemas/event/Microsoft.Windows.PrintSpooler/1.0.1.0/6382e26fc390d748">
              <PrinterName>%1</PrinterName>
          </PrinterConnectionFailure>
       </xml>
   </template>
</templates>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





