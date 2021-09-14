---
title: Type complexe EapMethodType
description: Définit les éléments qui identifient de manière unique un type de méthode EAP, un ID de type, un type de caractère et un ID d’auteur unique.
ms.assetid: 3ef96187-7376-438d-9d47-a87d5a6c9b8b
keywords:
- EapMethodType type complexe EAPHost
topic_type:
- apiref
api_name:
- EapMethodType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cea2448111266696398d1581aaecdbec2fb5859e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127221476"
---
# <a name="eapmethodtype-complex-type"></a>Type complexe EapMethodType

Le type complexe **EapMethodType** définit les éléments qui identifient de façon unique une méthode EAP unique : type, [](eapcommonschema-vendortype-eapmethodtype-element.md)ID de [**type, type de type**](eapcommonschema-type-eapmethodtype-element.md)et [**ID**](eapcommonschema-vendorid-eapmethodtype-element.md)d' [**auteur**](eapcommonschema-authorid-eapmethodtype-element.md).

Le [**type**](eapcommonschema-type-eapmethodtype-element.md) et l’ID d' [**auteur**](eapcommonschema-authorid-eapmethodtype-element.md) sont des éléments obligatoires, alors que les [**types de type**](eapcommonschema-vendortype-eapmethodtype-element.md) et [**ID**](eapcommonschema-vendorid-eapmethodtype-element.md) de l’élément sont requis uniquement lorsque l’élément de **type** est 254 (méthode EAP développée).

``` syntax
<xs:complexType name="EapMethodType">
    <xs:sequence>
        <xs:element name="Type"
            type="unsignedByte"
         />
        <xs:element name="VendorId"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="VendorType"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="AuthorId"
            type="unsignedInt"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                | Type         | Description                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Faut**](eapcommonschema-authorid-eapmethodtype-element.md)     | unsignedInt  | Fait référence à l’auteur de la méthode. <br/>                                                                                                                                                                                                                 |
| [**Entrer**](eapcommonschema-type-eapmethodtype-element.md)             | unsignedByte | Fait référence au type de méthode EAP. <br/>                                                                                                                                                                                                               |
| [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md)     | unsignedInt  | Fait référence au fournisseur qui a défini la méthode-si l’élément [**type**](eapcommonschema-type-eapmethodtype-element.md) est 254 (méthode EAP développée). Le [**ID**](eapcommonschema-vendorid-eapmethodtype-element.md) de l’argument est facultatif. <br/> |
| [**#D3**](eapcommonschema-vendortype-eapmethodtype-element.md) | unsignedInt  | Est le type défini par le fournisseur pour la méthode. Le [**module**](eapcommonschema-vendortype-eapmethodtype-element.md) de la est facultatif. <br/>                                                                                                           |



## <a name="remarks"></a>Notes

Il n’est pas [**nécessaire que les**](eapcommonschema-authorid-eapmethodtype-element.md) éléments de réfaut de réfaut et [**ID**](eapcommonschema-vendorid-eapmethodtype-element.md) de données soient identiques pour une méthode particulière.

Les [**éléments de**](eapcommonschema-authorid-eapmethodtype-element.md)réfaut-réid, type, [**ID**](eapcommonschema-vendorid-eapmethodtype-element.md) de [**certificat et**](eapcommonschema-vendortype-eapmethodtype-element.md) [**type**](eapcommonschema-type-eapmethodtype-element.md)d’élément sont chacun un numéro unique émis par l’IANA (Internet Assigned Numbers Authority).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma eapcommon](eapcommonschema-schema.md)
</dt> </dl>

 

 





