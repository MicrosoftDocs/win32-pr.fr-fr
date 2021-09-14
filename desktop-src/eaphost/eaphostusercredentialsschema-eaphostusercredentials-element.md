---
title: Élément EapHostUserCredentials
description: Contient l’élément EapMethod, ainsi que les informations d’identification ou l’élément CredentialsBlob.
ms.assetid: 6d0d41c8-560c-4d42-83c9-865053aef47a
keywords:
- Élément EapHostUserCredentials EAPHost
topic_type:
- apiref
api_name:
- EapHostUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 690770091219e51b3ebb550a1a72e50f76b20542
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127221401"
---
# <a name="eaphostusercredentials-element"></a>Élément EapHostUserCredentials

L’élément **EapHostUserCredentials** contient l’élément [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md) , ainsi que les [**informations d’identification**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) ou l’élément [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) .

``` syntax
<xs:element name="EapHostUserCredentials">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Credentials"
                    type="BaseEapMethodUserCredentials"
                 />
                <xs:element name="CredentialsBlob"
                    type="hexBinary"
                 />
            </xs:choice>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                                | Type                                                                                                                | Description                                                                                      |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Informations d'identification**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md)         | [**BaseEapMethodUserCredentials**](baseeapmethodusercredentialsschema-baseeapmethodusercredentials-complextype.md) | Est utilisé lorsque la configuration de la méthode est au format texte XML au lieu d’un objet BLOB binaire.<br/>   |
| [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) | hexBinary                                                                                                           | Est utilisé lorsque la configuration de la méthode est un objet BLOB binaire au lieu du format texte XML.<br/> |
| [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md)             | [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)                                                  | Identifie la méthode référencée. <br/>                                             |



## <a name="remarks"></a>Notes

Les [**informations d’identification**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) et les éléments [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) ne peuvent pas être utilisés simultanément.

Il existe un point d’extension pour d’autres espaces de noms.

L’élément **processContents** active les futures améliorations du schéma. L’élément **processContents** est facultatif.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma eaphostusercredentials](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





