---
title: Type complexe ComplexDataType
description: Définit une structure qui contient un ou plusieurs éléments de données.
ms.assetid: 1495daef-1dfd-4f62-9543-569cc74102f4
keywords:
- ComplexDataType type complexe EventLog
topic_type:
- apiref
api_name:
- ComplexDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 598f2cc02f1e3675ff0c8fd6eae7f9a5e02b9407
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192840"
---
# <a name="complexdatatype-complex-type"></a>Type complexe ComplexDataType

Définit une structure qui contient un ou plusieurs éléments de données.

``` syntax
<xs:complexType name="ComplexDataType">
    <xs:sequence>
        <xs:element name="Data"
            type="DataType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                  | Type                                                      | Description                                                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Métadonnée**](eventschema-data-complexdatatype-element.md) | [**Décimal**](eventschema-datafieldtype-complextype.md) | Liste des éléments de données de la structure. La liste des éléments se trouve dans le même ordre que celui défini dans le modèle.<br/> |



## <a name="attributes"></a>Attributs



| Nom | Type   | Description                                                                                                                                                                                                                  |
|------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nom | string | Nom de la structure. Il s’agit du nom qui est spécifié lorsque vous avez défini la structure dans le modèle (consultez le type complexe [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) ).<br/> |



## <a name="remarks"></a>Notes

La fonction [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) restitue le contenu d’une structure sous la forme d’un objet blob binaire ; la fonction ne rend pas les éléments de données individuels de la structure.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





