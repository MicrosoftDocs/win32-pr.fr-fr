---
title: Élément EapType (mspeapconnectionpropertiesv1schema)
description: Cet élément est un type dérivé de l’élément EapType du schéma BaseEapConnectionProperties. Pour mspeapconnectionpropertiesv1schema.
ms.assetid: 13238968-f3ef-4e9c-a525-d1f6efbaee0d
keywords:
- Élément EapType EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3336e943170afa0ec1f239d4cf7a0c603a0c8e71
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106533526"
---
# <a name="eaptype-element-mspeapconnectionpropertiesv1schema"></a>Élément EapType (mspeapconnectionpropertiesv1schema)

L’élément **EapType** est un type dérivé de l’élément [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) du schéma [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) .

Cet élément **EapType** dérivé contient les éléments suivants : [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md), [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md), [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md), [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md), [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md), [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) et [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md).

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="IdentityPrivacy"
                        type="IdentityPrivacyParameters"
                        minOccurs="0"
                     />
                    <xs:element name="FastReconnect"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element name="InnerEapOptional"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="EnableQuarantineChecks"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="RequireCryptoBinding"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="PeapExtensions"
                        type="PeapExtensionsType"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                                     | Type                                                                                                            | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md)                                              |                                                                                                                 | Décrit la méthode interne et la configuration de la méthode. Si l’élément [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) a la valeur true, l’élément [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) doit être présent. Si l’élément [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) a la valeur false, l’élément [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) doit être absent.<br/>           |
| [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) | boolean                                                                                                         | Indique s’il faut effectuer des vérifications de la protection d’accès réseau (NAP). Si l’élément [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) a la valeur true, PEAP effectue des vérifications NAP. Si la valeur FALSe, PEAP n’effectue pas de vérifications NAP. L’élément [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) est facultatif.<br/>                                                                                |
| [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md)                   | boolean                                                                                                         | Indique s’il faut effectuer une reconnexion rapide. Si l’élément [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) a la valeur true, PEAP tente d’effectuer une reconnexion rapide ; Si la valeur est FALSe, PEAP effectue l’authentification complète. L’élément [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) est facultatif.<br/>                                                                                                                       |
| [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)          | [**IdentityPrivacyParameters**](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)         | Windows 7 ou version ultérieure : indique si l’identité réelle d’un utilisateur ou une identité anonyme est envoyée. L’élément [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md) est facultatif.<br/>                                                                                                                                                                                                                                                                                 |
| [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md)             | boolean                                                                                                         | Indique s’il faut effectuer l’accès invité. Si l’élément [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) a la valeur true, l’élément [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) doit être présent et décrire la méthode interne et sa configuration. Si la valeur est FALSe, PEAP effectue un accès invité. L’élément [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) est facultatif.<br/>            |
| [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)                 | [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)                 | L’élément [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) active les améliorations futures du schéma. L’élément [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) est facultatif.<br/>                                                                                                                                                                                                                                    |
| [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md)     | boolean                                                                                                         | Indique s’il faut s’authentifier auprès des serveurs qui prennent en charge TLV. Si l’élément [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) a la valeur true, PEAP s’authentifie auprès des serveurs qui ne prennent pas en charge TLV ; Si la valeur est FALSe, PEAP s’authentifie uniquement avec les serveurs qui prennent en charge TLV. L’élément [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) est facultatif.<br/> |
| [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)             | [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) | Contient des informations sur la façon d’effectuer la validation du serveur. L’élément [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md) est facultatif.<br/>                                                                                                                                                                                                                                                                                                                      |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Éléments de schéma mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





