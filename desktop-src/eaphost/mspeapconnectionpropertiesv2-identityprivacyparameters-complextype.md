---
title: Type complexe IdentityPrivacyParameters
description: Contient des informations sur l’utilisation de l’identité anonyme pendant l’authentification PEAP.
ms.assetid: 81cf2403-ef25-4256-8d18-9d7b71792e6c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 18bef3eb69ab2799f7139fe2886d89e996fb8fb47d178997694c568450fb8340
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983899"
---
# <a name="identityprivacyparameters-complex-type"></a>Type complexe IdentityPrivacyParameters

Le type complexe **IdentityPrivacyParameters** contient des informations sur l’utilisation de l’identité anonyme pendant l’authentification PEAP.


```XML
<xs:complexType name="IdentityPrivacyParameters">
    <xs:sequence>
        <xs:element name="EnableIdentityPrivacy"
            type="xs:boolean"
            minOccurs="0"
        />
        <xs:element name="AnonymousUserName"
            type="xs:string"
            minOccurs="0"
        />
    </xs:sequence>
</xs:complexType>
```





| Élément                                                                                                               | Type    | Description                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) | boolean | Indique si l’identité réelle d’un utilisateur ou une identité anonyme est envoyée.                                                                                                                                                                                                                                                                           |
| [**AnonymousUserName**](mspeapconnectionpropertiesv2-anonymoususername-identityprivacyparameters-element.md)         | string  | contient une identité anonyme utilisée à la place de la véritable identification d’un utilisateur. Il est envoyé au cours de la première phase de l’authentification PEAP lorsque l' **identité** est envoyée en texte brut. L’utilisation de l’identité anonyme est déterminée par l’élément [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) . |



 

## <a name="remarks"></a>Remarques

L’élément IdentityPrivacyParameters est facultatif.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Types complexes mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> </dl>

 

 




