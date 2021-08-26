---
title: Type complexe StructDefinitionType
description: Définit une structure qui inclut un ou plusieurs éléments de données que vous souhaitez inclure avec l’événement. | Type complexe StructDefinitionType
ms.assetid: eb6b3682-1035-472b-8027-583d43c31748
keywords:
- StructDefinitionType type complexe EventLog
topic_type:
- apiref
api_name:
- StructDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 035b8abe5440ffb80b902e1f4b1564b2fb80b77ee34b20f4f068d298b251478a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124249"
---
# <a name="structdefinitiontype-complex-type"></a>Type complexe StructDefinitionType

Définit une structure qui inclut un ou plusieurs éléments de données que vous souhaitez inclure avec l’événement.

``` syntax
<xs:complexType name="StructDefinitionType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="data"
            type="DataDefinitionType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="length"
        type="LengthType"
        use="optional"
     />
    <xs:attribute name="count"
        type="CountType"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                               | Type                                                                             | Description                                                               |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**data**](eventmanifestschema-data-structdefinitiontype-element.md) | [**DataDefinitionType**](eventmanifestschema-datadefinitiontype-complextype.md) | Définit un élément de données que vous souhaitez inclure dans la structure.<br/> |



## <a name="attributes"></a>Attributs



| Nom   | Type                                                            | Description                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| count  | [**CountType**](eventmanifestschema-counttype-simpletype.md)   | Nombre d’éléments dans un tableau de structures. Cet attribut indique que la structure définit un tableau de structures. Vous pouvez spécifier le nombre réel ou le nom d’un élément de données en dehors de la structure qui contient le nombre. <br/>                               |
| length | [**LengthType**](eventmanifestschema-lengthtype-simpletype.md) | Non disponible.<br/> **Windows Server 2008 et Windows Vista :** Longueur de cette structure, en octets. non disponible à partir de Windows 7.<br/>                                                                                                                            |
| name   | string                                                          | Nom de la structure. Vous pouvez utiliser le nom pour faire référence à l’élément de données dans votre fragment XML si vous spécifiez une section [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) dans votre modèle.<br/> **Windows Vista :** Cet attribut est facultatif.<br/> |



## <a name="remarks"></a>Remarques

Les fournisseurs écrivent la structure en tant qu’objet BLOB et non en tant que membres individuels de la structure. Si la structure C que vous écrivez contient des pointeurs (par exemple, un pointeur de type LPWSTR), les données d’événement contiendront la valeur du pointeur, et non les données déréférencées.

Vous ne devez pas utiliser des structures mais devez plutôt définir des éléments de données pour chaque membre et les écrire séparément. Si vous décidez d’utiliser la structure, la structure doit contenir uniquement des types intégraux et vous devez vous assurer que les membres de la structure sont alignés sur une limite de 8 octets. Si vous ne le faites pas, vous risquez de recevoir des erreurs d’alignement quand vous tentez d’accéder aux données. Envisagez \# d’utiliser la directive pragma Pack () pour forcer l’alignement sur une limite de 8 octets.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





