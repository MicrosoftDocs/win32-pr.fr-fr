---
title: Type complexe DataDefinitionType
description: Définit un élément de données que vous souhaitez inclure avec l’événement. | Type complexe DataDefinitionType
ms.assetid: f4234e54-a5a8-48e4-941f-05107dcd3f88
keywords:
- DataDefinitionType type complexe EventLog
topic_type:
- apiref
api_name:
- DataDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a637166d261c4148a81baee3597d4090542b8612
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919556"
---
# <a name="datadefinitiontype-complex-type"></a>Type complexe DataDefinitionType

Définit un élément de données que vous souhaitez inclure avec l’événement.

``` syntax
<xs:complexType name="DataDefinitionType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="inType"
                type="QName"
                use="required"
             />
            <xs:attribute name="outType"
                type="QName"
                use="optional"
             />
            <xs:attribute name="map"
                type="string"
                use="optional"
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
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributs




| Nom | Type | Description | 
|------|------|-------------|
| count | <a href="eventmanifestschema-counttype-simpletype.md"><strong>CountType</strong></a> | Nombre d’éléments dans le tableau si l’élément de données est un tableau. Vous pouvez spécifier le nombre réel ou le nom d’un autre élément de données qui contient le nombre. <br /> | 
| InType | <strong>QName</strong> | Type de données de cet élément de données. Pour obtenir la liste des types de données d’entrée prédéfinis, consultez le type complexe <a href="eventmanifestschema-inputtype-complextype.md"><strong>InputType</strong></a> .<br /> | 
| length | <a href="eventmanifestschema-lengthtype-simpletype.md"><strong>LengthType</strong></a> | Longueur d’un élément de données de longueur variable, telle qu’un objet blob binaire. Pour les données binaires, spécifiez la longueur en octets et pour les données de type chaîne, spécifiez la longueur en caractères. Vous pouvez spécifier la longueur réelle ou le nom d’un autre élément de données qui contient la longueur.<br /> Si vous utilisez l’attribut length pour spécifier une chaîne de longueur fixe, vous devez remplir la chaîne à sa longueur fixe, ce qui permet d’utiliser le caractère de fin null à la fin (par exemple, si la longueur est égale à 5, la chaîne « ABC » doit être complétée comme « ABC ». La longueur de chaîne doit inclure le caractère de fin null.<br /> | 
| carte | string | Nom de la carte nom/valeur à utiliser pour mapper des valeurs entières à des chaînes. Le type de données de l’élément de données doit être de l’un des types suivants :<br /><ul><li>win:UInt8</li><li>win:UInt16</li><li>win:UInt32</li></ul> | 
| name | string | Nom de l'élément de données. Vous pouvez utiliser le nom pour faire référence à cet élément de données dans votre fragment XML si vous spécifiez une section <a href="eventmanifestschema-userdata-templateitemtype-element.md"><strong>UserData</strong></a> dans votre modèle. Vous pouvez également faire référence à ce nom dans un attribut de longueur ou de nombre d’un autre élément de données si cet élément de données contient sa valeur de longueur ou de nombre.<br /><strong>Windows Vista :</strong> Cet attribut est facultatif.<br /> | 
| Type de | <strong>QName</strong> | Type de données à utiliser lors du rendu de cet élément de données. Pour obtenir la liste des types de données de sortie prédéfinis, consultez le type complexe <a href="eventmanifestschema-outputtype-complextype.md"><strong>OutputType</strong></a> .<br /><strong>Windows Vista :</strong> Le type de sortie est ignoré et le service détermine le type en fonction du type d’entrée.<br /> | 




## <a name="remarks"></a>Notes

Pour les types d’entrée de longueur variable, tels que les objets BLOB binaires, vous devez utiliser l’attribut length pour spécifier explicitement la taille des données. Pour les chaînes, spécifiez l’attribut length uniquement si les chaînes ont une longueur fixe.

## <a name="examples"></a>Exemples

Voici quelques exemples de définitions d’éléments de données.


```XML
<!-- The data item is an 8-bit integer -->
<data name="binaryChar" inType="win:UInt8">
 
<!-- The data item is a single ANSI character -->
<data name="ansiChar" inType="win:UInt8" outtype="xs:string">
 
<!-- The data item is a single Unicode character -->
<data name="unicodeChar" inType="win:UInt16" outtype="xs:string">
 
<!-- The data item is an IP address that is rendered as a dot separated list of interger values -->
<data name="ipAddress" inType="win:UInt32" outtype="win:IPv4">
 
<!-- The data item is a Boolean value -->
<data name="success" inType="win:boolean">
 
<!-- The data item is a null-terminated ANSI string -->
<data name="string" inType="win:AnsiString"> 

<!-- The data item is a fixed length ANSI string -->
<data name="string" inType="win:AnsiString" length="42"> 
 
<!-- The data item is a fixed length array of null-terminated ANSI strings -->
<data name="strings" inType="win:AnsiString" count="20">
 
<!-- The data item is a fixed length array of fixed length ANSI strings -->
<data name="strings" inType="win:AnsiString" length="42" count="20">
 
<!-- The data item is a variable length array of same sized ANSI strings -->
<data name="stringLength" inType="win:UInt16">
<data name="arrayCount" inType="win:Uint16">
<data name="strings" inType="win:AnsiString" length="stringLength" count="arrayCount"> 
 
<!-- For binary data, you must specify the size.
<!-- The data item is a fixed length array of fixed length binary blobs -->
<data name="blobs" inType="win:Binary" length="42" count="20">

<!-- The data item is a fixed length binary blob -->
<data name="blob" inType="win:Binary" length="42">

<!-- The following are illegal binary data definitions -->
<!-- This definition is illegal because no length is specified -->
<data name="blob" inType="win:Binary"> 
 
<!-- This definition is illegal because you cannot determine the length of each binary blob -->
<data name="blob" inType="win:Binary" count="20"> 
 
<!-- The data item is a variable length array of structures. Each structure -->
<!-- contains an array of same sized ANSI strings --> 
<data name="arrayStructCount" inType="win:UInt16">
<struct name="countedStrings" count="arrayStructCount">
      <data name="stringLength" inType="win:UInt16">
      <data name="string" inType="win:AnsiString" length="stringLength">
</struct>
 
<!-- The data item is a time stamp that is rendered in 100ns units -->
<data name="timestamp" inType="win:UInt32" outType="win:ETWTIME">

<!-- The data item is a fixed length array of integers --> 
<data name="integers" inType="win:UInt32" count="20">

<!-- The data item is a variable length array of integers -->
<data name="arrayCount" inType="win:UInt16"> 
<data name="integers" inType="win:UInt32" count="arrayCount"> 

<!-- The following is illegal because you cannot assign a length value to a data type of a known size -->
<data name="integer" inType="win:UInt32" length="42">
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





